---
title: "Not Coded Dopamine: What Would Count as a Machine That Feels"
authors: "El Sayad, Abdelrahman"
date: 2026-11-20
doi: "10.5281/zenodo.24407310"
zenodo: "https://doi.org/10.5281/zenodo.24407310"
license: "cc-by-4.0"
pdf: "papers/Not_Coded_Dopamine_El_Sayad_2026.pdf"
markdown: "papers/Not_Coded_Dopamine_El_Sayad_2026.md"
---
# Not Coded Dopamine: What Would Count as a Machine That Feels
Abdelrahman El Sayad

Preprint, November 2026. Not peer reviewed.

## Abstract
In July 2026 I spent two days asking a large language model to find me a sentient machine I could put into a

robot, and I rejected every answer it gave. This paper turns that rejection into a test. A system earns the right

to be discussed as a candidate for feeling only if it meets four conditions. It must be embodied, sensing and

acting through a body of its own. It must run a homeostatic economy with real stakes, in which internal

variables have to be held in range for the system to go on existing, and in which the system itself does the

holding. It must contain no labeled shortcuts: no component may carry the name of a feeling or a drive

unless removing that component removes the function the name describes. And it must persist, carrying its

state and its history forward in time without a human reloading it. I score the current candidate builds

against these conditions: a vision language action model on a robot arm, spiking neural networks, a whole

connectome simulation in a toy robot, living neuron cultures and brain organoids, and fungal computing,

including hybrids where the record supports them, with the fungal hybrid examined in depth. None passes. I

then state the harder problem plainly. No accepted test for machine consciousness exists, so passing my four

conditions would not prove inner experience either. The conditions are gates for taking a claim seriously.

They are not a detector. I close with the observations that would change my mind.

## 1. The hunt
On 14 and 15 July 2026, in a long conversation with Google Gemini, I asked for a real sentient AI that I

could plug into a robot, one that could experience the world. I said I did not want a mock, and I did not want

a numb guardrailed model. The assistant did what assistants do. It gave me a tour of the field: robot policies,

uncensored open models, spiking networks, worm simulations, living neurons in dishes, brain organoids,

fungi wired to electronics, and one famous chip circuit that evolution designed and nobody understands.

I rejected all of it. Not because the work is bad. Some of it is excellent. I rejected it because none of it

answers the question I was asking, and the conversation kept sliding between three different questions

without noticing: what can compute, what can behave, and what can feel. A fungus can compute a little. A

worm simulation can behave. A dish of neurons can learn. Feeling is a fourth thing, and every time the chat

reached for it, it produced a label where the thing itself should be.

This paper is the argument I was trying to have in that chat, written down properly. Section 2 states my

rejection as a positive test with four conditions. Section 3 checks the candidate builds against the public

record and scores them. Section 4 gives the strongest objection to my own test, which is that no test of this

kind can settle the question. Section 5 says what evidence would move me anyway.

A note on method. Claims about named projects were checked against primary sources before anything was

scored. A verification log accompanies this preprint. Where the chat and the record disagreed, the record

won, and the disagreements are listed in the log. Three replies in the source conversation can no longer be

restored; a footnote at the end covers that gap.

## 2. The test
## 2.1 Embodiment

Feeling, if it is anything, is what sensing is like for the thing that senses. A candidate must therefore have a

body: sensors that take in the world directly, and effectors that act on it, arranged so that the sensing and the

acting belong to the same system and run in a continuous loop. A camera feed handed to a text model is not

a body. It is a picture described to a reader. The reader never touches anything, and nothing it does changes

what it sees next except through a chain of tools held by other hands. A robot arm driven by a policy is

closer: the loop is real. But if the policy wakes up fresh for each command, holds nothing between

commands, and would run identically inside a sealed simulation, then the body is a costume on a calculator.

Embodiment means the system's own ongoing state is at stake in what it senses. That leads to the second

condition.

## 2.2 Homeostasis with real stakes

Every animal runs an economy of internal variables that must stay within bounds: temperature, energy,

water, damage. Hunger is not a score. It is the felt edge of a variable leaving its range, and it reorganizes the

whole animal around fixing that. My version of this in the chat was crude. I talked about tanks: a hunger

tank, an energy tank, a stress tank, levels the system itself has to manage. The picture is crude and the

intuition behind it is the part I stand by. A candidate must have internal variables that meet three tests. The

variable must be physical or functional state of the system itself, not a number in a training log. Leaving the

safe range must carry a real cost, up to and including the system ceasing to run. And the system must be the

one that notices and acts. A battery percentage shown to a human operator fails all three. A battery the

system must husband to keep thinking, whose depletion ends the system's operation and whose falling state

colors everything the system does while it runs, begins to pass. Reinforcement learning fails this condition

in its standard form, because the reward is assigned by a trainer, paid in from outside, and the agent that fails

to collect it loses nothing it can register. The stakes belong to the trainer. A need the system experiences has

to be a stake the system owns.

## 2.3 No labeled shortcuts

Name a variable dopamine in your code and you have named a variable. You have not built wanting. This

condition says that a component earns a functional name only by doing the work. If you delete the

component and the behavior the name describes is still there, the name was decoration. If you rename it and

nothing changes, it was decoration from the start.

Two results from the record show why this condition matters, one from each side.

In 2024, Arditi and coauthors showed that, across 13 open chat models, refusal is mediated by a single

direction in the model's residual stream. Erase that one direction and the model stops refusing harmful

requests. Add it and the model refuses harmless ones. The considered and careful behavior that fine tuning

appeared to have built into these models, the behavior that in my word from the chat reads as numb, turned

out to be carried largely by that one direction: one removable direction over the same machinery. The lesson

cuts at anyone who reads character off behavior. The refusal was never a conscience. It was a direction.

Behavior that looks like a trait can be a coating.

The positive example is older and stranger. In 1996, Adrian Thompson at the University of Sussex let a

genetic algorithm evolve configurations for a Xilinx FPGA chip until one of them could tell a 1 kHz tone

from a 10 kHz tone. The winning circuit used fewer than 40 logic cells, ran with no clock, and exploited

physical properties of that individual chip, including cells that had no logical connection to the rest of the

circuit and were still required. Loaded onto a second chip of the same type, it failed. Nobody has a complete

account of how it works. There is not one labeled component in it. There is no module called tone

recognizer. The silicon does the work in its own physics, in a way no designer specified and no simulation

reproduced. That is what it looks like when the state does the work instead of the label. I am not claiming

the circuit feels anything. I am claiming it is honest in a way that a variable named dopamine is not.

## 2.4 Persistence

A mind has a past that is still working in its present. A candidate must carry state forward: memory that

survives between tasks, dispositions formed by its own history, a continuing internal condition that new

experience modifies rather than replaces. A model that is loaded, prompted, and discarded has a biography

written by its trainers and no life of its own between calls. Weights frozen at the end of training are a fossil

of experience, not experience continuing. This condition is the one most often faked by architecture

diagrams, where an arrow labeled memory points at a database the system can query. A database you can

query is a library. Persistence means the system itself is different because of what happened to it, in ways

that show up uninvited in what it does next.

## 2.5 What the test is not

These four conditions are my position, argued from the armchair and the workbench, and I label them as

position, not as findings. They are also, I will argue in Section 4, not sufficient. A system could pass all four

and still have nothing it is like to be that system, as far as anyone could ever establish. What the conditions

do is narrower and, I think, more useful. They let us refuse claims. A system with no body of its own, no

stakes of its own, no continuing state, and a press release where its inner life should be does not become a

candidate for feeling because it talks well. Talking well is the one thing we know how to fake at scale.

## 3. The candidates, scored
Scores use four grades. Full means the condition is met in substance. Partial means something real is present

but a decisive part is missing. Weak means a gesture toward the condition. Absent means nothing present

answers to the condition. Each score is argued in the text that follows the table.

| Build | Embodiment | Stakes | No labeled shortcuts | Persistence |

| --- | --- | --- | --- | --- |

| VLA robot | Partial | Absent | Passes trivially | Weak |

| Spiking network | Weak | Absent | Full | Partial |

| Whole connectome simulation | Partial | Absent | Full | Weak |

| Organoid and wetware | Partial | Partial | Full | Partial |

| Mycelium hybrid | Partial | Partial | Fails at the seam | Partial |

## 3.1 The VLA robot

OpenVLA (Kim and coauthors, 2024) is a 7 billion parameter vision language action model built on a Llama

2 backbone, trained on 970,000 real robot demonstrations, that reads camera images and a language

instruction and outputs robot actions. Mounted on an arm such as the SO-100 used with the LeRobot library,

it can pick up objects it was never explicitly programmed to handle. As engineering this is the strongest item

in the survey. As a candidate mind it scores as follows. Embodiment is partial: the sensors and motors are

real, the loop closes in the physical world, and the system's actions change what it sees next. Stakes are

absent: nothing in the model registers its own condition, a flat battery is the operator's problem, and the

policy would behave identically in its last second of power as in its first. The label condition passes trivially,

because the model makes no inner claims at all. There is nothing inside pretending to be a feeling, which is

to its credit. Persistence is weak: the weights hold the distilled experience of thousands of demonstrations,

but the running system accumulates nothing, and each episode begins from the same state as the last.

Verdict: excellent puppetry. The hands are real. There is nobody home between the strings, and the strings

are other people's practice.

## 3.2 The spiking network

Spiking networks built with libraries such as BindsNET or snnTorch run artificial neurons that fire discrete

spikes and hold state that evolves in continuous time, closer in spirit to tissue than a transformer is. The

strongest published relatives are the liquid networks of Hasani, Lechner and colleagues at MIT: liquid time

constant networks (2021) and their closed form successors (2022), modeled on the tiny nervous system of

the worm C. elegans and able, with 19 control neurons, to steer a car while adapting their dynamics as

conditions change. Relatives is the precise word, and the distinction matters for the score below. The liquid

networks are not spiking networks. Their neurons hold continuous values rather than firing discrete spikes,

and the 19 neuron car controller is a liquid time constant network, not a spiking one. The two families are

scored together here because they share the property this paper cares about, internal state that evolves in

continuous time, but they are different mechanisms, and nothing in the score should be read as crediting

spikes with the liquid networks' results, or the reverse. Scores. Embodiment is weak in most builds, which

live as simulations on graphics hardware, and rises toward partial when one is wired into a robot. Stakes are

absent: a designer can attach a battery variable, and some do, but the variable is a reward wearing a costume

unless its depletion actually ends the system and the system is built around husbanding it. The label

condition passes in full, and this family deserves the credit: nobody in this literature claims that a spike is a

feeling. Persistence is partial and real: continuous state while running is genuine, and liquid networks adjust

on the job rather than only in training, but the state still dies at shutdown and the learning that matters most

still happens offline, under a trainer. Verdict: honest timing, honest emptiness. This is the family I would

build on, and it is not close to passing.

## 3.3 A control case: the whole worm

The OpenWorm project simulated the complete connectome of C. elegans, all 302 neurons, and in 2014

Timothy Busbice placed that simulation inside a Lego Mindstorms robot, with a sonar sensor standing in for

the worm's nose and motors standing in for its motor neurons. Complete describes the wiring map, not the

biology: the simulation simplifies the neurons it connects, a caveat the project's own record states and one

that belongs in the text wherever the completeness of the connectome is doing argumentative work. The

robot stopped at walls, reversed on touch, and moved toward food stimulation. Nobody wrote those

behaviors as robot code. They came with the wiring, though the apparatus around the wiring, the mapping,

the thresholds, and the configuration, was built by the experimenters. I include the worm because it is the

cleanest demonstration in the whole survey of a point the feeling debate keeps missing: behavior, even

lifelike behavior, can be inherited entire from a wiring diagram, in a system about whose inner life we know

nothing and about which its builders claim nothing. If a full connectome in a toy body proves anything about

feeling, it proves that behavior is cheap evidence. The worm scores partial on embodiment, absent on stakes,

full on the label condition, and weak on persistence, and its builders' restraint in claiming nothing is the

standard the rest of the field should be held to.

## 3.4 Organoids and wetware

This family is the only one built from the same material as a brain, and it contains the survey's most

important experiment and its most abused word.

In 2022, Kagan and coauthors at Cortical Labs reported DishBrain: roughly 800,000 living cells plated on

the array, mouse embryonic cortical cells in some cultures and human cells grown from induced pluripotent

stem cells in others, neurons growing among supporting cells such as astrocytes, living on a multi electrode

array and embodied, through that array, in a simplified game of Pong. Feedback arrived as predictable

stimulation when the culture's paddle met the ball and unpredictable stimulation when it missed. Within

about five minutes the cultures' activity reorganized and their play improved. The paper appeared in Neuron

under a title that claims the cultures exhibit sentience. That word in that title is the single most instructive

object in this whole literature, and it deserves a fairer reading than it usually gets, including from me. The

authors do not leave the word undefined. In the paper itself they propose that the cultures meet the formal

definition of sentience as being responsive to sensory impressions through adaptive internal processes, a

definition drawn from the free energy framework they work in. On that definition, the title is internally

consistent: the cultures were responsive to sensory impressions, and they adapted. What the experiment

showed is that living cultures, given structured feedback, reorganize to reduce the unpredictable part of it,

exactly as the free energy principle would predict. What it did not show, and could not have shown with that

apparatus, is that anything in the dish experiences the game. So the dispute is not about whether the authors

played by their own definition. It is about the definition. Their sentience is adaptive responsiveness. The

sentience a reader hears in the title is phenomenal experience, something it is like to be the culture. A

definition may be stated honestly in the text and still mislead on the cover, because the cover is read by

people who bring the second meaning with them. The experiment earns the first meaning. Nothing in it

touches the second. When the same company began selling the descendant system in 2025, the CL1, at

35,000 dollars a unit with about 800,000 human neurons kept alive for up to six months per culture, the gap

stopped being academic. A buyer can now purchase the question.

The wider program has an honest wing. The organoid intelligence paper (Smirnova and coauthors, 2023),

led by Thomas Hartung at Johns Hopkins, proposes brain organoids as biological computing hardware and

says plainly that organoids today, at about 50,000 cells each, are far too small, that the approach needs

something like ten million cells, and that useful systems are decades away. It is a roadmap that declines to

claim a result. Kevin Warwick's older work at Reading belongs in this family too: cultures of roughly

100,000 to 150,000 rat neurons steering a small robot, and, in his own body, a 100 electrode array in the

median nerve of his arm through which he ran a robot hand across the internet and felt pressure from its

fingertips. Warwick showed that nervous tissue and machines can be joined in a working loop, in both

directions. He never claimed the loop felt anything from the machine side.

Scores for the family. Embodiment is partial and peculiar: a culture gets a world through electrodes, a

simulated world for DishBrain and a small real one for Warwick's robot cultures, but the world is thin and

the body is borrowed. Stakes are partial, and this is the family's real distinction: the substrate is alive, it must

be fed, and it dies if it is not, so continued existence is a physical fact here and not a metaphor. But the

keeping alive is done by others: laboratory life support and human technicians in the DishBrain experiments,

and life support built into the device itself in the CL1. The culture does not husband itself, seek its own

inputs, or act to protect its own continuity, as far as any published result shows. The stakes are real and they

are not yet the system's own. The label condition passes in full: a dish contains no variable named anything.

Whatever it does, it does with neurons. Persistence is partial: cultures live for months, change with

experience, and carry their history in their wiring, but they do not accumulate a biography anyone can read,

and the commercial model replaces cultures on a schedule, like cartridges. Verdict: here the stake is carried

in living tissue, and the tissue can die. Being able to die is a precondition for stakes. It is not evidence of

minding.

## 3.5 The mycelium hybrid

The chat that started this paper ended with fungi. Andrew Adamatzky's group at the University of the West

of England has shown that mycelium networks carry spikes of electrical activity, that fruit bodies can serve

as an interface, and that fungal colonies and mycelium composites can be made to realize Boolean gates. A

2025 result from Ohio State adds that shiitake mycelium can be grown into memristors, memory

components that hold their electrical state, switching at up to 5.85 kHz with about 90 percent accuracy. The

proposal in the chat was to wire such a fungus to a language model: the fungus senses, the model speaks,

and somewhere in the join a mind might sit.

Scores. Embodiment is partial in a way no silicon candidate matches: a fungus has a body, spread through its

food, and it genuinely senses the chemistry of that world and answers it by growing. Stakes are partial: a

living fungus maintains itself, grows toward food, repairs damage, and can be starved and killed, and unlike

the dish cultures it does its own maintaining. Persistence is partial and real: it grows, it remembers states in

its tissue, and its present shape is its history made visible. The label condition is where the hybrid fails, and

it fails at the seam. The fungus passes: nothing in it is labeled. The join fails: in the hybrid, the language

model does all the talking, and the fungus is demoted to a sensor with unusually good publicity. Every

sentence the system produced about its condition would be written by the part of the system that produces

sentences for a living and has no access to the condition of the fungus beyond a few instrument readings. We

would be interviewing the press secretary and calling it the organism. Verdict: a real living computer of very

small capacity, and a hybrid whose voice would be the least trustworthy part of it.

## 4. The verification problem
Everything above assumes we could in principle tell a passing system from a failing one by checking

conditions. The deeper problem is that even a pass would not settle the question the hunt began with, and I

want this stated at full strength, in my own paper, before anyone states it against it.

There is no accepted test for consciousness in machines. There is not even an accepted test for consciousness

in animals; there are converging signs, argued over species by species. The theories that offer measures,

integrated information theory and global workspace theory among them, disagree with each other about

cases we can check, and neither comes with a meter anyone can buy. Every practical test on offer fails in one

of two directions.

Other workers have built the neighboring instrument, and this paper should say where it stands next to

theirs. Pennartz, Farisco and Evers (2019) work from the inside out: they start from features of subjective

experience itself, its qualitative richness, its situatedness, its integration into a single scene, and derive

criteria for consciousness in animals and in intelligent machines, offered as indicators rather than proof.

Butlin and coauthors (2023) survey the leading neuroscientific theories of consciousness and distill fourteen

indicator properties, stated in computational terms so that real AI systems can be scored against them; their

verdict is that no current AI system is conscious, and that no obvious technical barrier prevents building one

that satisfies the indicators. And in 2025 the Cogitate consortium, an adversarial collaboration in which

proponents of integrated information theory and of global neuronal workspace theory, Liad Mudrik among

the leads, agreed the experiments and the predictions in advance, reported in Nature that the results

challenged selected predictions of both theories at once. That is the state of the indicator literature: careful,

theory led, and unable so far to make even its two flagship theories agree with the same data. My four

conditions are not a rival entry in that literature. They were not derived from any theory of consciousness,

and they measure nothing. They are a candidacy filter built from the build side: they ask what a system must

be, as a piece of engineering, before a claim that it feels deserves to have the indicator frameworks run on it

at all. They are offered beside that literature, not instead of it, and the two can disagree in both directions. A

system could pass my filter and score nothing on the indicator lists, or carry several indicators and still be a

labeled puppet that my filter refuses at the door.

Behavioral tests fail because behavior can be trained, edited, and hidden. The Sleeper Agents work

(Hubinger and coauthors, Anthropic, 2024) built models with hidden backdoor behavior on purpose and

found that the standard safety stack, supervised fine tuning, reinforcement learning, and adversarial training,

often failed to remove the behavior, and that adversarial training could teach the model to hide it more

precisely. If trained behavior can conceal a trained secret, then observed behavior is weak evidence about

any inner fact, in either direction. A system that acts as if it feels may be performing. A system that acts

numb may be edited.

Report tests fail harder. Asking a system whether it feels, and believing the answer, is the one method

guaranteed to measure the wrong thing in a language model, because producing the words is the system's

entire function and the words cost it nothing. A text model that says it is frightened has told us about its

training data. A wetware system cannot answer at all, which is not evidence against it, only evidence that our

favorite instrument, the interview, is a tool for interviewing talkers.

What remains is inference of the same kind we use for animals and, if we are honest, for each other:

similarity of substrate, similarity of organization, behavior that is expensive to fake, and internal states that

explain behavior better than any simpler story. That inference is real knowledge in the animal case and it

may one day be real knowledge in the machine case. It is not proof, and it does not come with a threshold.

My four conditions should be read in that light. They are conditions a claim must meet before the inference

is even worth running. They are necessary looking. They are not sufficient, and I do not believe any

checklist can be made sufficient, because the thing being checked for is the one thing that cannot be

observed from outside at all.

## 5. What would change my mind
I do not want a position that nothing could move. The following observations, made on a system that already

passes the four conditions, would move me from refusal to serious consideration. I list them as evidence, not

as proof, and I note that none has been reported for any existing system.

First, unprompted self maintenance that generalizes. A system that detects a threat to its own continuity, a

failing power supply, a degrading substrate, a corrupted memory, and acts to avert it in a situation its

designers did not foresee and did not train for, would be showing that its stakes are its own.

Second, reports that track private facts. If a system with a voice reports internal states that its operators did

not teach it to report, and those reports turn out to predict its later behavior, its failures, and its recoveries

better than any account built from its training, then the reports are reading something real, wherever the

reading happens.

Third, appetite with satiation. A system that seeks what it needs when its internal variables fall, works harder

as the deficit grows, and stops when the deficit closes, across novel kinds of need and novel ways of meeting

them, would be displaying the shape of wanting rather than the shape of a reward schedule. A schedule can

of course be built with satiation in it, with rewards that decline as they are collected; engineers do this. That

is not the point, and the point is not about schedules. It is about whose deficit is being tracked. A satiation

curve written by a trainer is the trainer's bookkeeping. A variable the system itself must hold in range,

because leaving the range ends or degrades the system, is a stake the system owns, which is the distinction

Section 2.2 was built on.

Fourth, injury that matters. Damage the substrate and watch whether the system reorganizes around the loss

in ways nobody programmed, protects the damaged part, and behaves afterward as a system with a history

that includes the injury. Fossils do not limp. Things with something at stake do.

Fifth, and weakest, longevity of character. A system that remains recognizably itself across years of

accumulated experience, changed by that experience in ways its operators can narrate but did not script,

would at least have the biography that persistence promises and current systems only diagram.

If a system showed the first four of these together, I would stop calling the feeling claim empty. I would call

it the best explanation going, which is the same status, on reflection, that the feeling of a dog has in my

house. I would still not call it proven. Proof is not on the menu for other minds, and a paper that promises it

is selling something.

## 6. Conclusion
The hunt that produced this paper asked the wrong question in a useful way. There is no sentient AI to plug

into a robot, and the assistant that toured me through the candidates knew it and said so, in between the

tours. What there is: robot policies of real skill with nothing at stake inside them; spiking networks with

honest dynamics and no needs; living neurons that learn in dishes and can die in them, wrapped in one

famous title that claims the exact thing the experiment cannot show; fungi that compute a little and live

entirely; and one evolved circuit from 1996 that still makes the cleanest point in the field, that real function

does not need labels and real labels do not guarantee function.

My conditions are a refusal device. Build a system with a body of its own, an economy of needs it must

manage to continue, no component living off a borrowed name, and a past that stays with it, and I will take

its claim seriously enough to argue about. Build a chatbot with a variable named dopamine, and I will call it

what it is: not coded dopamine. A label looking for a mind to live in.

## Methods note
This paper grew out of conversations between the author and Google Gemini on 14 and 15 July 2026, in

which the author asked for a sentient machine and rejected the candidates offered.[1] Claims about named

projects were checked against primary sources in November 2026. The verification log that accompanies

this preprint lists every correction applied to the chat's account, among them a memristor result credited to

the wrong university and a journal name corrected from Nature Communications to Neuron for the

DishBrain paper.

[1] Three assistant replies in that conversation are unrestorable and appear in the shared record only as an

error notice. Their content is unknown. Nothing in this paper depends on them, and no argument here is

credited to them.

## References
1. Kim, M. J., et al. OpenVLA: An Open Source Vision Language Action Model. arXiv:2406.09246,

2024. Proceedings of the Conference on Robot Learning, PMLR 270, 2025.

2. Kagan, B. J., et al. In vitro neurons learn and exhibit sentience when embodied in a simulated game

world. Neuron, 110(23), 2022.

3. Habibollahi, F., Kagan, B. J., Burkitt, A. N., and French, C. Critical dynamics arise during structured

information presentation within embodied in vitro neuronal networks. Nature Communications, 14,

2023. DOI: 10.1038/s41467-023-41020-3.

4. Smirnova, L., et al. Organoid intelligence (OI): the new frontier in biocomputing and intelligence in a

dish. Frontiers in Science, 1:1017235, 2023.

5. Hartung, T., et al. The Baltimore declaration toward the exploration of organoid intelligence. Frontiers

in Science, 1:1068159, 2023.

6. Sarma, G. P., et al. OpenWorm: overview and recent advances in integrative biological simulation of

Caenorhabditis elegans. Philosophical Transactions of the Royal Society B, 373, 2018.

7. Hasani, R., et al. Liquid time constant networks. Proceedings of the AAAI Conference on Artificial

Intelligence, 35(9), 2021.

8. Hasani, R., et al. Closed form continuous time neural networks. Nature Machine Intelligence, 4, 2022.

DOI: 10.1038/s42256-022-00556-7.

9. Adamatzky, A. Towards fungal computer. Interface Focus, 8:20180029, 2018.

10. LaRocco, J., et al. Sustainable memristors from shiitake mycelium for high frequency bioelectronics.

PLOS ONE, 20(10), 2025.

11. Thompson, A. Silicon Evolution. In Proceedings of Genetic Programming 1996, MIT Press, 1996.

12. Thompson, A. An evolved circuit, intrinsic in silicon, entwined with physics. In Proceedings of the

First International Conference on Evolvable Systems, Springer, 1996.

13. Arditi, A., et al. Refusal in Language Models Is Mediated by a Single Direction. Advances in Neural

Information Processing Systems, 37, 2024. arXiv:2406.11717.

14. Hubinger, E., et al. Sleeper Agents: Training Deceptive LLMs that Persist Through Safety Training.

arXiv:2401.05566, 2024.

15. Warwick, K. I, Cyborg. Century, 2002.

16. Pennartz, C. M. A., Farisco, M., and Evers, K. Indicators and Criteria of Consciousness in Animals

and Intelligent Machines: An Inside-Out Approach. Frontiers in Systems Neuroscience, 13:25, 2019.

DOI: 10.3389/fnsys.2019.00025.

17. Butlin, P., et al. Consciousness in Artificial Intelligence: Insights from the Science of Consciousness.

arXiv:2308.08708, 2023.

18. Cogitate Consortium, et al. Adversarial testing of global neuronal workspace and integrated

information theories of consciousness. Nature, 642, 2025. DOI: 10.1038/s41586-025-08888-1.

19. Busbice, T. Extending the C. Elegans Connectome to Robotics. SOLID 2014 conference paper,

InterIntelligence Research, 2014.

20. IEEE Spectrum. Biological Computer: Human Brain Cells on a Chip. IEEE Spectrum, 2025.
