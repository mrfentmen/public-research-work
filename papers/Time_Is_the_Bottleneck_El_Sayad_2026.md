---
title: "Time Is the Bottleneck: Why AI's Binding Constraint Is Not Memory or Energy, but Time to Solution"
authors: "El Sayad, Abdelrahman"
date: 2026-11-23
doi: "10.5281/zenodo.24457103"
zenodo: "https://doi.org/10.5281/zenodo.24457103"
license: "cc-by-4.0"
pdf: "papers/Time_Is_the_Bottleneck_El_Sayad_2026.pdf"
markdown: "papers/Time_Is_the_Bottleneck_El_Sayad_2026.md"
---
# Time Is the Bottleneck: Why AI's Binding Constraint Is Not Memory or Energy, but Time to Solution
**Abdelrahman El Sayad**

November 2026

--
## Abstract
Public discussion of AI's limits centers on resources: memory capacity, memory bandwidth, electricity,

datacenter buildout. This paper argues those are the wrong variables. RAM can be bought. Electricity can be

generated, contracted, and sited. Both scale with money on roughly linear terms. **Time does not.** The

binding constraint on AI problem solving is *time to solution*: the wall clock interval between posing a

problem and having a verified answer. This interval is dominated by irreducibly serial computation, a

reasoning chain whose step *n+1* depends on step *n* cannot be parallelized away, only waited through.

We show that the major "resource" bottlenecks in modern AI systems are, on inspection, time bottlenecks in

disguise: memory bandwidth matters only because it sets token latency; energy matters because power caps

clock and parallelism, i.e., throughput per unit time. We further argue that the recent history of AI progress is

best read as a series of *time compressions*: distillation compresses a teacher's search time into a student's

weights; caching compresses repeated computation into retrieval; test time compute scaling buys accuracy

explicitly with time. The practical consequence is a re-ranking of research and engineering priorities: the

field should measure, price, and optimize **time to solution** the way it currently measures FLOPs and watts,

because every second removed from solving a problem compounds across every problem the system will

ever be given.

## 1. Introduction: the wrong ledger
Ask what limits AI and the answers arrive in physical units: gigabytes of HBM, gigawatts of power, millions

of GPUs (IEA, *Energy and AI*, 2025: data-centre electricity demand 415 TWh in 2024, projected ~945

TWh by 2030, AI the major driver; up to 20% of planned projects at risk of delay absent transmission

investment). These answers share an assumption, that AI is limited by *stuff*. This paper disputes the

assumption. Stuff is purchasable. A lab short on memory buys memory; a lab short on power signs a power

contract. The market clears both, at a price, on a schedule.

What no lab can buy is a shorter second.

Every AI system, whatever its size, delivers its value in the form of *answers over time*. A solved problem

is worth nothing before it is solved and less with every minute it is late: the trading decision expires, the

patient deteriorates, the user's session ends, the robot's world has moved. The quantity that governs all of

this is not how much memory the system holds or how much energy it burns. It is **how long it takes** .

**Thesis.** The binding constraint on AI problem solving is time to solution. Memory and energy constraints

are real but derivative: they bind only insofar as they lengthen time to solution, and they can be relaxed with

capital. Serial time cannot.

## 2. Definitions
**Time to solution (TTS):** wall clock time from problem presentation to a *verified* solution,

including queuing, retrieval, generation, tool calls, and verification.

**Serial depth:** the length of the longest chain of dependent computational steps in a solution. Serial

depth has a hard floor: it cannot be reduced by adding parallel hardware.

**Time compression:** any technique whose primary effect is to reduce TTS at fixed solution quality, by

removing steps, shortening steps, or replacing computation with retrieval.

## 3. Why time is different from the other constraints
**3.1 Resources scale with money; serial time does not.** Doubling memory is a purchase order. Doubling

power is a construction project. But a reasoning process with serial depth *d* takes at least *d* sequential

steps on any hardware, at any budget. This is Amdahl's law read as economics (Amdahl, 1967): the serial

fraction of a workload caps the value of all parallel spending. Money buys width. It does not buy depth

away.

**3.2 Latency has physical floors.** Signal propagation, memory access latency, and network round trips

bound how fast a single step can execute regardless of budget. A datacenter can hold a trillion tokens of

context; fetching the relevant ones still costs time, and in agent systems those costs are paid *per step, in

series*.

**3.3 Agent loops multiply time.** Modern AI problem solving is increasingly agentic: plan, act, observe,

repeat. Each iteration pays full model latency plus tool latency plus environment latency. A 50 step agent

task at 20 seconds per step is a 17 minute task, not because the system lacked memory or power, but because

time compounds multiplicatively across the loop. As tasks lengthen, TTS, not capacity, is what breaks first:

sessions time out, contexts drift, the world changes mid solution.

## 4. The disguises: resource bottlenecks are time bottlenecks
**4.1 Memory bandwidth.** Inference is famously "memory bound": generating each token requires streaming

model weights from HBM, so tokens per second is set by bandwidth (Leviathan et al., 2023; Kwon et al.,

2023). But note the unit the constraint actually governs: *tokens per second*. Bandwidth is not valued as an

end; it is valued because it is a **time quantity**, the rate at which memory can be converted into progress.

Nobody would care about bandwidth in a world where answers were allowed to take forever.

**4.2 Energy.** Power constraints bind through time as well: a power cap limits how many accelerators run

concurrently and at what clock, that is, how much computation completes *per unit time*. Energy is the

budget; time is the currency it is spent in. Two systems with identical energy budgets and different

architectures differ precisely in how much solving they fit into an hour.

**4.3 Capacity.** Even context window limits express themselves in time: exceeding them forces chunking,

rereading, and retrieval passes, all serial additions to TTS. The failure mode of "not enough memory" in

practice is "the solution took too long and degraded," not a hard stop.

**Claim:** strip the time pressure away, allow unbounded wall clock, and nearly every celebrated resource

constraint in AI softens into an inconvenience. Strip resources away but keep time pressure, and the system

fails outright. Time is the constraint that survives the thought experiment; therefore time is the constraint.

## 5. The evidence: progress as time compression
Read recent AI history through this lens and a pattern appears, the field's celebrated advances are,

disproportionately, ways of buying back time:

**Test-time compute scaling** made the trade explicit: reasoning models convert *more time* (longer

chains of thought) into *more accuracy* (OpenAI, 2024; Snell et al., 2024). Accuracy is being

purchased in seconds: OpenAI's o1 scored 74% on AIME 2024 against GPT-4o's ~12 to 13%, and

Snell et al. showed compute optimal test time scaling can outperform a ~14× larger model. The

exchange rate is now a published curve.

**Distillation** compresses a large model's slow search into a small model's fast weights: the teacher's

time, spent once, is amortized across every future query.

**Caching and retrieval** (KV caches, prompt caches, RAG) replace recomputation with lookup,

computation traded for memory *in order to save time*, the reverse of the usual framing, and proof of

which resource the field actually treats as precious.

**Speculative decoding** exists for one reason: to make serial generation faster by drafting in parallel

(Leviathan et al., 2023: 2 to 3× acceleration with identical outputs). An entire subfield devoted to

shaving the serial chain.

**Mixture of experts and quantization** are routinely justified by accuracy, but their deployment value

is latency: fewer active FLOPs *per token*, i.e., per unit time.

Meanwhile the metrics the field headlines, FLOPs, parameters, tokens of context, watts, are all inputs. TTS,

the output side variable users and economies actually feel, is rarely the headline number. This paper argues

that is a measurement error with strategic consequences.

## 6. Implications
**6.1 For evaluation.** Benchmarks should report **accuracy at a time budget** and **time to solution at an accuracy target**, not accuracy alone. A model that solves in 4 seconds and one that solves in 4 minutes are

not the same product, and a leaderboard that cannot tell them apart is mispricing both.

**6.2 For research priorities.** If time is the bottleneck, the highest-leverage research is time research:

shortening serial depth (parallel and draft based reasoning), compressing verification (fast checkers, self

verification), amortizing search (distillation, memory of solved subproblems), and agent architectures that

reduce steps rather than enlarge them. Notably, several of these are unfashionable next to scale, which is

what a misidentified bottleneck predicts.

**6.3 For economics.** The cost of intelligence is converging to *cost per solved problem*, and cost per solved

problem is dominated by how long expensive hardware is occupied. Cutting TTS in half at fixed hardware

doubles the world's effective AI capacity without one new datacenter. Time compression is capacity creation.

**6.4 For agent design.** Every step in an agent loop should have to justify its latency. Systems that ask "can

this step be removed, cached, parallelized, or precomputed?" will out-solve systems that merely ask "can the

model be bigger?"

## 7. Objections and replies
**"Energy is a hard physical limit, ask any grid operator."** Granted as a buildout constraint on *total

deployed capacity*. But capacity is not problem solving speed: a grid capped lab still solves each problem in

the time its architecture takes, and its users experience the time, not the grid. Energy limits how much AI

exists; time limits what AI can do. This paper is about the second.

**"Some problems are compute bound, not latency bound, training runs take months of FLOPs."**

Training is the strongest counterexample and the exception that clarifies the rule: training time is precisely

the industry's most complained-about constraint (iteration speed governs research velocity), and the field's

response, parallelism, works only because training is unusually parallelizable. Frontier training is what a

field looks like when it *can* buy its way out of the time bottleneck with width. Inference and agentic

problem solving, where serial depth dominates, are where it cannot.

**"This is just latency engineering rebranded."** Latency engineering optimizes systems; the claim here is

about where the *ceiling* sits. Rebranding matters when the old brand misdirects capital: gigawatts are

being procured against a bottleneck that is, at the margin, measured in seconds.

## 8. Conclusion
RAM is a purchase. Electricity is a contract. Time is a law. AI's progress will be governed less by how much

its systems can hold or burn than by how long they take to think, and every technique that cuts time to

solution compounds across every problem, every user, and every hour the system runs. The fastest path to

more capable AI is not only bigger systems. It is quicker ones: fewer serial steps, cheaper verification,

memory spent freely to buy the one resource that cannot be bought, time.

--
## References
Amdahl, Gene M. "Validity of the Single Processor Approach to Achieving Large Scale Computing

Capabilities." *AFIPS Conference Proceedings* 30 (1967), pp. 483–485. (The paper states the

argument with one figure and no equations; the "law" as usually formalised is a later rendering.)

IEA. *Energy and AI*. Paris, April 2025.

Kwon, Woosuk, et al. "Efficient Memory Management for Large Language Model Serving with

PagedAttention." *SOSP 2023*, arXiv:2309.06180.

Leviathan, Yaniv, Matan Kalman, and Yossi Matias. "Fast Inference from Transformers via

Speculative Decoding." *ICML 2023*, arXiv:2211.17192.

OpenAI. "Learning to Reason with LLMs" (o1 launch note), 12 September 2024; *OpenAI o1 System

Card*, December 2024.

Snell, Charlie, Jaehoon Lee, Kelvin Xu, and Aviral Kumar. "Scaling LLM Test-Time Compute

Optimally can be More Effective than Scaling Model Parameters." arXiv:2408.03314 (2024).

--
