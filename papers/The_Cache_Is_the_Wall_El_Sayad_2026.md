---
title: "The Cache Is the Wall: KV Cache, Not Weights, Is What Keeps Frontier Models Off Small Hardware"
authors: "El Sayad, Abdelrahman"
date: 2026-11-23
zenodo_version: "2"
doi: "10.5281/zenodo.24462968"
zenodo: "https://doi.org/10.5281/zenodo.24462968"
license: "cc-by-4.0"
pdf: "papers/The_Cache_Is_the_Wall_El_Sayad_2026.pdf"
markdown: "papers/The_Cache_Is_the_Wall_El_Sayad_2026.md"
---
# The Cache Is the Wall: KV Cache, Not Weights, Is What Keeps Frontier Models Off Small Hardware
**Abdelrahman El Sayad**

November 2026

*Companion to "Time Is the Bottleneck."*

**Correction note, version 2 (November 2026).** The first version's conclusion stated that a 32 GB MacBook can hold a frontier model's body. It cannot, on this paper's own numbers: a 70B class model's weights alone exceed the machine before any cache is stored. The abstract and conclusion are corrected to say so. Section 4 now applies the cache reductions the paper cites to the paper's own table, and one derivation label in Section 1 is corrected. No computed figure in Section 2 changes.

--
## Abstract
The race to run frontier level language models on consumer hardware is usually framed as a weights

problem: quantize the model small enough and it will fit. This paper argues the framing is wrong. Weights

are static, compressible, and paid once. The **KV cache**, the stored key and value vectors a transformer keeps

for every token of context, is dynamic, grows linearly with context length and with every concurrent session,

resists aggressive compression, and is the quantity that actually exhausts memory on small machines. On a

32 GB laptop, a frontier class model's weights do not fit at all, and the models whose weights do fit still

fail at frontier use, because the cache for a long context, or for the long reasoning chains that increasingly

*define* frontier capability, does not fit in what remains. We compute cache sizes from published architectures, show why each current

mitigation (grouped query attention, cache quantization, sliding windows, paged memory management)

moves the wall rather than removing it, and argue that the architectures that do remove it (compressed latent

attention, state space and hybrid models) amount to redesigning the transformer around the cache. Until the

cache problem is solved, not managed, solved, frontier level models will not run on small hardware, no

matter how small the weights get.

## 1. Introduction: the fit is a lie
"Runs on a 32 GB MacBook" is the most misleading sentence in local AI. It means the *weights* fit. A 70B

model at 4 bit quantization occupies roughly 35 to 40 GB in naive terms and ~40 GB is already too much,

but drop to a 32B model at 4 bit (~19 GB as shipped, of which the weights alone are 16 GB by parameter

count, the rest format overhead) and the weights fit comfortably on a 32 GB machine. Demos run.

Screenshots are posted.

Then the user does real work: a long document, a long conversation, a long reasoning trace, and the machine

swaps, thrashes, or the runtime silently truncates context. What grew? Not the weights. The cache.

The KV cache is the transformer's working memory of the conversation: for every token processed, every

layer stores a key vector and a value vector so that future tokens can attend back without recomputation. It is

the price attention pays to avoid rereading the past from scratch at every step. And unlike weights, it scales

with *use*: tokens of context × layers × attention width, per session, at runtime precision. Frontier

capability is increasingly defined by exactly the things that inflate it, hundred thousand token contexts and

reasoning traces tens of thousands of tokens long. The better the model gets at the things we now call

frontier, the bigger its cache grows. The wall is not behind us. It is in front of us, and it grows.

## 2. The arithmetic
KV cache size per token:

- **bytes/token = 2 (K and V) × layers × KV heads × head dimension × bytes per element**

Computed from published configurations (fp16 cache; decimal GB throughout, 17.18 GB = 16.0 GiB):

|Model|Layers|KV<br>heads|Head<br>dim|Bytes/token|Cache @ 8k<br>context|Cache @ 128k<br>context|
|---|---|---|---|---|---|---|
|Llama 3.1<br>8B|32|8<br>(GQA)|128|~131 KB|~1.1 GB|~17 GB|
|Llama 3.1<br>70B|80|8<br>(GQA)|128|~328 KB|~2.7 GB|~43 GB|

Read the second row against a 32 GB machine: the 70B's weights don't fit anyway, but even granting a

hypothetical ~18 GB 2 bit 70B, a single 128k context session needs **~43 GB of cache alone** . The first row is

the quiet scandal: an *8B* model, weights ~4 to 5 GB at 4 bit, needs **~17 GB of cache** to use its full

advertised context. On a 32 GB MacBook (unified memory, shared with the OS and every other app),

weights plus a full context cache come to ~21 to 22 GB: not over the line on paper, but close enough that the

OS, the runtime, and activations leave almost no headroom, and a second session, or one long reasoning

trace, tips it over. The context window on the box is a specification the hardware cannot honor. That gap,

advertised context vs. usable context, is the KV cache wall, measured.

Three multipliers make it worse in practice:

**Concurrency.** Every additional session, agent, or parallel sample carries its own cache. Agentic

workflows multiply cache the way they multiply everything.

**Reasoning length.** Test-time compute scaling means the model generates its own context: a 30k

token reasoning trace is 30k tokens of cache before the answer begins.

**Precision sensitivity.** The cache is typically held at higher precision than quantized weights, because

errors in it are reread at every subsequent step (see §4.2).

## 3. Why the cache, specifically, is the bottleneck
**3.1 Weights compress; the cache resists.** Weight quantization is a solved enough problem because weights

are static: calibrate once, accept small quality loss, ship it. The cache is generated live, is different for every

input, and exhibits outlier structure (a small number of channels and "attention sink" tokens carry outsized

magnitude (Xiao et al., 2023; Liu et al., 2024)) that naive quantization destroys, and a corrupted cache entry

is not read once but at *every future step*, so errors compound across the whole generation.

**3.2 The cache is where the time bottleneck lives on small hardware.** The companion paper argued AI's

binding constraint is time to solution. The KV cache is the mechanism that trades memory *for* time: it

exists to avoid quadratic recomputation. On a datacenter GPU with hundreds of gigabytes of HBM, that

trade is free. On a 32 GB laptop, the trade is unaffordable in both directions: keep the cache and you run out

of memory; drop or shrink it and you pay in recomputation time. Small hardware is where the memory wall

and the time wall are the same wall.

**3.3 The cache grows with capability, not against it.** Every frontier trend inflates it: longer contexts, longer

reasoning, more agents, more parallel sampling. A constraint that scales *with* the thing it constrains is not

an engineering detail. It is the bottleneck.

## 4. The mitigations move the wall; they do not remove it
**4.1 Grouped query / multi query attention (GQA/MQA).** Sharing KV heads across query heads cuts

cache by the sharing factor (the table above already assumes GQA-8; a full-MHA 70B would need ~8×

more). Real progress, and a constant factor. Linear growth in context remains linear. (Ainslie et al., 2023)

**4.2 KV cache quantization.** 4 bit and even 2 bit cache quantization exists (KIVI, KVQuant and successors;

Liu et al., 2024) and works better than expected, at the cost of the outlier problem in §3.1, extra

dequantization compute (time again), and quality risk concentrated exactly on the long contexts where the

cache matters most. A compressed cache is a smaller wall, not an open gate.

**4.3 Sliding-window attention.** Cap the cache by forgetting old tokens (Mistral style windows). This

"solves" the memory problem by surrendering the capability: the model no longer has the context it

advertised. For frontier use, the whole context is the point, this is amputation as cure.

**4.4 PagedAttention / vLLM style memory management.** Brilliant engineering that eliminates

fragmentation waste (Kwon et al., 2023). It optimizes the *packing* of the cache. It does not shrink the

cache by one byte. Managing a bottleneck is not removing it, and on a single user laptop the fragmentation

problem it solves is minor next to the raw size problem.

**4.5 What actually removes it, by redesigning around it.** Multi-head Latent Attention (DeepSeek)

compresses KV into a low rank latent vector, cutting per token cache by a reported 93.3% against DeepSeek

67B (DeepSeek-AI, 2024), by changing the architecture. State-space and linear-attention models (Mamba

and hybrids; Gu & Dao, 2023) replace the cache with a fixed-size state, by abandoning exact attention recall.

Both directions concede the thesis: **the cache is not a detail to be optimized but the structural problem the next architecture is being designed around.** And both pay for it, compressed or fixed state memory is

lossy memory, and whether it matches full attention at frontier scale on long context recall remains

genuinely contested (Hsieh et al., 2024; Waleffe et al., 2024: pure SSMs lag full attention on recall heavy

long context tasks while hybrids close the gap, and no controlled MLA vs attention recall study exists yet, so

the match is contested, not settled).

**4.6 The reductions, applied to this paper's own table.** Take the mitigations at their strongest and run

them against Section 2's numbers. Cache quantization at 4 bit takes the 70B's 128k cache from ~43 GB to

~11 GB, and at 2 bit to ~5.4 GB. Neither admits the model to a 32 GB machine, because its weights at 4 bit

are ~40 GB: the cache could be free and the body still would not fit. For the 8B the same arithmetic cuts

the other way, and this paper concedes it: 4 bit cache quantization takes its 128k cache from ~17 GB to

~4.3 GB, and that machine works. The wall moves for small models. It does not move for frontier class

models, where the binding order is weights first, cache second, both over the line. Multi-head Latent

Attention's reported 93.3% cut would take a 70B scale cache to ~2.9 GB, but MLA is not a setting applied

to an existing model; it is a different architecture. That is Section 5's point: the reductions that would

settle the question are the redesigns.

## 5. The claim, precisely
1. On small hardware (≤32 GB), **KV cache, not weights, is the first binding memory constraint** for every model whose weights can be made to fit, at the context lengths and reasoning lengths that define frontier use. For frontier class models proper, the weights alone already exceed the machine, and the cache exceeds it again; nothing about them runs on 32 GB, and Section 4.6 shows the current reductions do not change that.

2. All widely deployed mitigations are constant factor or capability surrendering; the growth law (linear

in context, per session) is untouched.

3. Therefore: **no frontier level model will run, at frontier context and reasoning lengths, on a 32 GB machine until the cache problem is solved architecturally**, regardless of further progress in weight

quantization.

4. Falsifiable corollary: "runs on 32 GB" claims should be required to state *usable context at stated

precision on that hardware*. Under that reporting standard, most current claims collapse, and that

collapse is measurable today.

## 6. Implications
**For local AI roadmaps:** stop advertising weight size as the portability metric. The honest spec sheet

is weights + cache at full context + concurrency, against total unified memory.

**For architecture research:** the cache is the design center. Latent compression, hybrid attention/SSM

stacks, and learned cache eviction with recall guarantees are not optimizations; they are the main

event for on device frontier AI.

**For the time thesis:** cache policy *is* time policy on small hardware. Eviction, compression, and

recomputation are three currencies for the same purchase, a usable past, and on a laptop all three are

scarce at once.

## 7. Conclusion
The weights were never the wall; they were the part of the wall we knew how to shrink. The KV cache is the

part that grows, with context, with reasoning, with agents, with ambition itself. A 32 GB MacBook cannot

hold a frontier model at all: not its memory of the conversation, and not even its body, which exceeds the

machine before the first token is stored. Frontier AI stays in the datacenter because the datacenter is

where the memory is. What the laptop can hold is a smaller model, and there the cache is the wall in its

purest form, a model of 4 to 5 GB of weights that needs ~17 GB to remember its own context. Until the

cache is solved, compressed without amnesia, or replaced without loss, local AI stays a demo with a

context window it cannot afford to use.

--
## References
Ainslie, Joshua, et al. "GQA: Training Generalized Multi-Query Transformer Models from Multi
Head Checkpoints." *EMNLP 2023*, arXiv:2305.13245.

DeepSeek-AI. "DeepSeek-V2: A Strong, Economical, and Efficient Mixture-of-Experts Language

Model." arXiv:2405.04434 (2024).

Dubey, Abhimanyu, et al. "The Llama 3 Herd of Models." arXiv:2407.21783 (2024). (Source of the

§2 configurations, Table 3.)

Gu, Albert, and Tri Dao. "Mamba: Linear-Time Sequence Modeling with Selective State Spaces."

arXiv:2312.00752 (2023).

Hsieh, Cheng-Ping, et al. "RULER: What's the Real Context Size of Your Long-Context Language

Models?" *COLM 2024*, arXiv:2404.06654.

Kwon, Woosuk, et al. "Efficient Memory Management for Large Language Model Serving with

PagedAttention." *SOSP 2023*, arXiv:2309.06180.

Liu, Zirui, et al. "KIVI: A Tuning-Free Asymmetric 2bit Quantization for KV Cache."

arXiv:2402.02750 (2024).

Waleffe, Roger, et al. "An Empirical Study of Mamba-based Language Models." arXiv:2406.07887

(2024).

Xiao, Guangxuan, et al. "Efficient Streaming Language Models with Attention Sinks." *ICLR 2024*,

arXiv:2309.17453.

--
