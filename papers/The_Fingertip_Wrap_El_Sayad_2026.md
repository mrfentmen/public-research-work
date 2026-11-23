---
title: "The Fingertip Wrap: A Low-Cost Vibrotactile Device Design for Tardive Dyskinesia"
authors: "El Sayad, Abdelrahman"
date: 2026-11-20
doi: "10.5281/zenodo.24407331"
zenodo: "https://doi.org/10.5281/zenodo.24407331"
license: "cc-by-4.0"
pdf: "papers/The_Fingertip_Wrap_El_Sayad_2026.pdf"
markdown: "papers/The_Fingertip_Wrap_El_Sayad_2026.md"
---
# The Fingertip Wrap: A Low-Cost Vibrotactile Device Design for Tardive Dyskinesia
Abdelrahman El Sayad

November 2026

Status: design preprint. This document describes a device design and a proposed self test. It reports no

results, because the device has not been tested yet. It is not medical advice, and it makes no claim that the

device works. Expanded in November 2026 at the author's direction: the fingertip cap was replaced by a

wrap, a constant micro vibration variant of the author's was added, and a second design, a body suit for

Parkinson's disease, was added as section 5. Neither device has been tested.

## Abstract
Tardive dyskinesia is an involuntary movement disorder caused by long term use of dopamine receptor

blocking drugs, most often antipsychotics. No device is approved or cleared specifically for it in the United

States, and no vibration device has ever been trialled in it. Device based neuromodulation has been tried

experimentally in the clinic, deep brain stimulation above all, with electroconvulsive therapy, repetitive

transcranial magnetic stimulation and transcranial direct current stimulation also in the literature, but those

are invasive or clinic based experiments in severe refractory cases, not wearable treatments; a 2026 scoping

review of seventeen studies of them found the strongest evidence for deep brain stimulation (Kololichalil

and co workers, 2026). The only treatments with regulatory approval in the United States are two drugs, and

both suppress symptoms rather than reverse the condition. This paper proposes a device for the form of the

disorder that affects the fingertips. The proposal borrows a stimulation method called coordinated reset,

which was developed for Parkinson's disease and is delivered in that field through a vibrating glove built at

Stanford University. In small studies in people with Parkinson's disease, fingertip vibration delivered in a

coordinated reset pattern for four hours a day reduced motor scores, and the gains were still present weeks

after stimulation stopped. No study of this method, or of any vibration device, has been run in tardive

dyskinesia. That gap is stated plainly here, because the diseases are different and the method may not

transfer. The first contribution of this paper is a design: thin wraps that wind around each finger instead of a

full glove, built from woven conductive sleeves, a coin vibration motor in each wrap, fabric tape conductors

running down the palm and a wrist worn controller, at a core parts cost of roughly 37 to 61 dollars. The

paper also sets out a single patient self test protocol with fixed outcome measures and stopping rules, written

down in advance so that the result, good or bad, means something. The paper then documents two

extensions by the same author. The first is a variant stimulation pattern of his own: a constant micro

vibration set below the level the wearer can feel, on his stated principle that what stops a shake is a smaller

shake. It differs from coordinated reset, which works in patterned bursts with built in silence, and it is

untested. The second is a second device built on the same principle at the scale of the whole body: a skin

tight suit with the same wiring woven into the cloth, worn under ordinary clothing, proposed for Parkinson's

disease, a disease with no cure. The suit is aimed at the symptom layer of that disease, above all at resting

tremor, the cardinal sign the author's principle addresses directly, and at the rigidity and slowness that travel

with it. It cannot restore the dopamine producing neurons the disease destroys, and this paper does not claim

otherwise. Both extensions are designs on paper, documented because they are the author's. No efficacy

claim is made for either disease.

## 1. The problem
Tardive dyskinesia, called TD from here on, develops in people who have taken dopamine receptor blocking

agents for months or years. The standard account of the condition is that long blockade leaves the dopamine

receptors of the striatum oversensitive, and the motor system begins to fire movements that the person did

not choose and cannot reliably stop. The movements most often involve the face, mouth and tongue. In

many people they also involve the hands and fingers.

The author is one of those people. His TD sits in his fingertips. On a bad day he cannot hold a pencil

between two fingers without the fingers spasming and shaking. He also has a strained left wrist, which

matters for design, because any device he wears for hours has to be light and has to keep its weight off a bad

wrist.

Treatment options are thin. Before 2017 there was no approved drug treatment for TD at all. Two drugs are

now approved in the United States, valbenazine and deutetrabenazine. Both block the vesicular monoamine

transporter 2 and so reduce dopamine release. In the valbenazine trial called KINECT 2, the average score

on the Abnormal Involuntary Movement Scale fell by 2.6 points on the drug against 0.2 points on placebo

(Patel and co workers, 2025; Touma and Scarff, 2018). These are real gains, and they are also modest ones.

The drugs suppress the movements while they are taken. They do not repair the underlying change. They are

expensive specialty medicines. They carry their own side effects, including sleepiness and parkinsonism,

and deutetrabenazine carries a boxed warning about depression and suicidal thoughts in people with

Huntington's disease. Stopping the antipsychotic that caused the TD is often not an option, because the

illness it treats is still there, and TD frequently persists even when the drug is stopped.

No device is approved or cleared specifically for TD, and none is sold with TD as its indication in the United

States. As far as a search of the published literature and the United States trial registry in November 2026

can establish, no trial of a vibration device in TD has ever been run. Section 3 returns to this point, because

it is the most important fact in the paper.

## 2. What the Parkinson's literature shows
The design in this paper borrows its stimulation pattern from a different disease, so the evidence for that

pattern has to be stated exactly, in the population where it was gathered.

In Parkinson's disease, neurons in the motor circuits fall into step with each other and fire in abnormal

synchrony, visible in recordings as exaggerated power in the beta band. Peter Tass and his co workers built a

stimulation method against that synchrony on theoretical grounds first. In that theoretical construction, and

in the electrical version of the method that followed it, coordinated reset delivers short bursts of stimulation

to separate sites in a set sequence. Each burst resets the phase of one subpopulation of neurons. Because the

resets land at staggered times, the population cannot hold its shared rhythm and falls out of step. With

repetition, the synaptic connections that held the rhythm in place are weakened by spike timing dependent

plasticity. The network, in the word the field uses, unlearns the synchrony. The effect is meant to outlast the

stimulation, and in the animal and human work below, it did.

The method was tested first with electrical stimulation delivered through deep brain electrodes. In

Parkinsonian monkeys, coordinated reset through implanted electrodes produced motor improvement that

lasted after stimulation ended. In a proof of concept study in six people with Parkinson's disease, three days

of coordinated reset through deep brain electrodes reduced subthalamic beta activity and improved motor

function.

The fingertip version came next. Vibration is a way to reach the same circuits from outside the body, but its

own source models it differently, and the difference matters. In the model Pfeifer and co workers built for

vibratory stimuli, the vibration does not produce a sharp phase reset of the neuronal oscillations. Instead,

neuronal responses phase lock to the vibration, which lets the timing of the stimulation steer the timing of

discharges in the subpopulations it reaches. The desynchronization and unlearning that are then meant to

follow are hypothesized to run through spike timing dependent plasticity, as in the electrical account, but for

the vibratory version that chain is supported by computational modelling, not directly observed in humans.

The fingertips are densely supplied with Pacinian corpuscles, which respond strongly to vibration near 250

Hz, and the fingertips hold an outsized share of the sensory cortex. Tass's group at Stanford built a glove that

delivers short vibratory bursts to the fingertips in the coordinated reset pattern (Tass, 2022). The published

human results are these:

In a first in human study, five people with Parkinson's disease received the stimulation for four hours

a day on three consecutive days. Four of the five were off their Parkinson's medication during the

stimulation days and the assessment visits that followed; one stayed on medication throughout.

Measures of gait asymmetry and gait arrhythmicity improved significantly, a measure of wrist

bradykinesia improved, and the gains were still present at visits one and four weeks after stimulation

ended. Blinded video ratings of the standard motor scale did not change significantly. There was no

sham control group, so placebo effects could not be ruled out, a limit the authors state themselves.

In a feasibility study of six people with Parkinson's disease, a version of the pattern with added timing

jitter was used daily for three months. Motor scores on the Movement Disorder Society revision of

the Unified Parkinson's Disease Rating Scale, part III, fell significantly after the first four hour day

and fell again, cumulatively, after three months. All six patients improved by more than the minimal

clinically important difference of 3.25 points. Recordings of brain activity showed a significant fall in

resting high beta power, 21 to 30 Hz, over the sensorimotor cortex. No side effects were reported.

A second small study followed three patients for more than six months and found motor scores

declining steadily across the treatment period.

That is the whole of the published clinical evidence: eight unique patients in the months long studies, five in

the three day study, and no sham controlled results. A double blind, sham controlled trial was registered and

run at Stanford under the protocol this literature published, enrolling 36 people against the 30 the protocol

planned, and the registry record shows it terminated in October 2022, with no reason given on the record and

no results posted. This paper offers no guess about why it ended. The consequence belongs in the open: the

field's one registered sham controlled trial ended without results, so the published evidence for vibrotactile

coordinated reset remains the small uncontrolled feasibility studies above, and nothing larger is on its way to

settle the question. Anyone citing this literature for more than it says is overstating it, and this paper does

not.

Two neighbouring devices are worth naming because they show what regulators have and have not accepted.

The Cala kIQ wristband delivers patterned electrical stimulation to the nerves of the wrist and is cleared by

the United States Food and Drug Administration for temporary relief of hand tremor in essential tremor, and

for postural and kinetic hand tremor in Parkinson's disease. The Felix NeuroAI wristband, also electrical,

was cleared in 2025 for essential tremor after a sham controlled trial. Neither device uses vibration, and

neither is cleared for TD. They matter here only as proof that a wrist worn stimulator for a movement

disorder can clear regulators and reach patients.

## 3. The honest gap
TD is not Parkinson's disease. The Parkinson's work rests on a synchrony story that is well documented in

that disease: too much beta synchrony in motor circuits, measured again and again. TD rests on a different

account, dopamine receptor supersensitivity after long blockade, with striatal injury from oxidative stress

also proposed. Abnormal synchrony may play a part in TD, but it has not been established as the driver of

TD the way beta synchrony has been established in Parkinson's disease.

So the argument of this paper is an extension, and it is labelled as one. The claim is narrow: fingertip

afferents give strong, cheap access to sensorimotor circuits; a patterned stimulus built to desynchronize has

shown measurable effects on motor output in one movement disorder, in small uncontrolled studies; and TD

is a movement disorder with no device approved or cleared specifically for it in the United States: device

based interventions exist in the experimental literature, as the abstract records, but no wearable vibrotactile

treatment for it has been established. That is enough to justify building the device and testing it honestly on

one person. It is not enough to predict that it will work, and this paper does not predict that it will work.

Three things would count against the idea and should be recorded if they appear. First, no change at all

across a full test, which would say the pattern does not reach whatever drives TD. Second, change only

while the device is buzzing and none the next morning, which would say the effect is masking, not

unlearning, and the device is then a far less interesting object. Third, worsening, which would say the input

aggravates the circuit and the whole direction should stop.

## 4. The design
The design is the author's. It came out of a simple refusal: he did not want a glove.

A glove covers the whole hand, traps heat, and puts fabric between the fingers and the world for hours a day.

The Stanford glove and the low cost glove built by Rice University students Emmie Casey and Tomi Kuye

both accept that cost, because a glove is the easy way to hold a motor against each fingertip. The Rice glove,

published openly in 2025, puts phone vibration motors in the fingertips of a soft glove with a circuit board at

the wrist, and it is the direct ancestor of this design. The author's changes are about the form the device takes

on the hand.

## 4.1 A wrap, not a glove

Each stimulator is a thin wrap that winds around one finger and nothing else. The first form of this design

was a cap: a small closed sleeve pulled over the fingertip. The author has replaced it, and the replacement is

recorded here as his decision. A cap is a cover, made in one size and closed at the end. A wrap is a band of

the same conductive cloth, wound around the finger and closed on itself, so it adjusts to any finger, sits

thinner than a cap, and leaves the end of the finger open. The wrap is the design from here on. The cap

survives in this paper only as the form it superseded. The paper's first title named the cap, and promised a fix

in its first word. During drafting the device was renamed from a cap to wraps, and on 20 November 2026, at

the author's ruling, the title was changed to name the wrap. The word Fix no longer appears in the title.

The cloth is cut from a ready made finger sleeve of the kind sold for mobile gaming. These sleeves are

knitted with silver coated fibre, which makes the fabric itself conductive, a fact the design uses in section

4.2. The wrap leaves the rest of the hand bare. The finger pad stays in contact with the inside of the wrap,

and the hand can still be used, washed around, and rested without taking a whole glove off. One wrap per

finger, four wraps for the fingers and an optional fifth for the thumb. The Stanford studies stimulated the

four fingers and left the thumb out, and the default build here does the same.

A search for fingertip only vibration devices, recorded in the verification log, found no wrap of this kind in

the published or marketed record. What exists at fingertip scale is a laboratory orthosis that absorbs finger

tremor mechanically, through a gel actuator in a printed frame (Liu and Zhang, 2024). That is a brace, not a

wrap, and it delivers no stimulation. There is also a research enhancer that mounts a piezoelectric actuator at

the side of one fingertip to sharpen touch in healthy volunteers (Kurita and co workers), which treats

sensation, not shaking. The fingertip stimulators that have reached patients sit inside gloves: the Stanford

glove and the Rice glove. A bare wrap that carries its own motor and leaves the hand otherwise open was not

located.

## 4.2 The motor and the wiring

Inside each wrap, over the finger pad, sits one coin vibration motor, 10 mm across and about 2 mm thick.

The motor is held flat against the pad by the tension of the wrap. How much tension that takes, and whether

the motor stays in place when the finger bends, when the skin sweats, or when the wrap rotates on the finger,

are unspecified in this design and have to be settled at first fitting, because the whole method depends on the

vibration landing on the same patch of skin every time. Two fine wires leave the motor and run inside the

wrap to the base of the finger. Every wire in this design runs the same way: back down the finger, across the

palm, and into the wrist unit. Nothing is carried on the back of the hand, and nothing crosses the knuckles

from above.

From the base of the finger, the signal path is conductive fabric tape: a nickel and copper ripstop tape with

conductive adhesive. Each motor is fed by two conductors, a drive line and a return line, and both have to

reach the wrist, so the tape run from each finger is two narrow strips side by side down the palm, one

carrying the drive line and one the return. The circuit for each finger is complete in its own pair of strips and

separate from its neighbours. The tape lies flat on the skin, adds almost no weight, and replaces the bundle

of loose wires a glove build would need. That contact carries a problem this design had not faced before this

round. The tape is nickel and copper, it sits against the palm for hours at a time, and nickel is a known

contact sensitizer: prolonged skin contact of exactly this kind is how a wearer becomes allergic to it. The

build therefore requires an insulating barrier between the conductors and the skin, a thin non conductive

layer under the tape runs, so that no bare conductor and no conductive adhesive touches the palm. Sweat and

moisture work against the whole arrangement, degrading both the adhesive that holds the tape and the

insulation that protects the skin, so the barrier and the runs are inspected at first fitting and whenever the

wrap is put on, and a run whose barrier has lifted or cracked is replaced, not worn. Solder joints are kept to

four small dots per finger: two where the motor wires meet the tape, two where the tape meets the wrist unit

lines.

No electrical data stands behind any of the textile parts. The resistance of the tape runs, the reliability of the

soldered contacts under repeated bending and moisture, and the durability of the conductive cloth have not

been measured. The design assumes those properties; it has not demonstrated them.

One engineering limit has to be stated. The Stanford work uses laboratory tactors driven at about 250 Hz. A

coin motor has no set frequency. It vibrates at its rotation speed, which depends on the voltage it is fed, and

common 10 mm coin motors at 3 volts run in the region of 150 to 200 Hz, drifting as the cell discharges.

The cheap build therefore cannot match the clinical stimulus exactly. What it can match exactly is the part

the theory cares most about: which finger is stimulated, in what order, for how long, and when the silence

falls. The durations and intervals behind those words are specified in section 4.4, at the values the Stanford

studies published. Whether the frequency difference matters is one of the things a test would begin to

answer. The Rice glove accepts the same compromise with phone motors, so the compromise has precedent,

though precedent is not evidence.

## 4.3 The wrist unit

All control sits at the wrist, in a plain neoprene athletic wrist wrap. The wrap holds a Seeed XIAO

microcontroller, a board smaller than a postage stamp, and a small lithium polymer cell of 100 to 150

milliamp hours. The board's outputs cannot drive the motors directly, because a microcontroller pin cannot

carry a motor's current, so each output feeds a transistor switch, one per output, and the switches sit in the

wrist unit beside the board and carry the motor current. The switch stage is specified at the level of

requirements, because its parts are chosen once the bench numbers exist. Each switch is a low side transistor

switch, and its current rating has to exceed the motor's measured draw at the drive levels used, the figure the

bench step at the head of section 6 records. Each motor gets transient protection across it, a flyback diode or

its equivalent, so the switching spikes of an inductive load do not reach the board. The controller itself

carries one hard requirement: at least four outputs with pulse width modulation, one per finger, and five if

the optional thumb wrap of section 4.1 is fitted, so each motor's level can be set independently and each

output has its own switch. The cell figure and the four hour day are, at this stage, an unworked estimate, and

the paper states that plainly: no power budget has been measured yet, no motor current at the drive levels

used, no total for the duty cycle the pattern imposes, no controller draw, and until the bench step at the head

of section 6 produces those numbers, four hours a day on this cell is a target rather than a specification. The

wrap is worn on the wrist of the hand under treatment, or, on days when the author's strained left wrist is the

treated side and is sore, the session is done seated with the forearm resting on a table so the wrap carries no

load. The whole wrist assembly is estimated at a few tens of grams; that figure is an estimate, not a

measurement, and the bench step of section 6 is where the build gets weighed. Nothing sits on the back of

the hand. This is a deliberate contrast with the GyroGlove, a Parkinson's and essential tremor device that

hangs a gyroscope module of about 580 grams on the back of the hand and steadies the hand by brute

mechanical resistance while it is worn. That device makes no attempt to change the brain signal, and it costs

5,899 dollars. The wrap aims at the opposite trade: almost no weight, almost no cost, and a bet on changing

the signal rather than resisting the movement.

## 4.4 The firing pattern

The pattern follows the published coordinated reset structure.

A cycle contains one short burst per finger, delivered one finger at a time, never two fingers at once.

The order of fingers is shuffled for every cycle by the controller, so the sequence is pseudorandom

rather than fixed.

The timing is the published timing, specified here so the pattern can be reproduced rather than

approximated. The published pattern is the reference: in it, each burst lasts 100 milliseconds and is

delivered as vibration at a 250 Hz carrier. The build specified in section 4.2 cannot match that carrier.

What it delivers is the pattern's timing, the burst length, the reset frequency, the on and off cycles and

the jitter, at whatever carrier its coin motors produce, which will not be 250 Hz. The cycle runs at a

coordinated reset frequency of 1.5 Hz, which puts 166.7 milliseconds between successive fingertip

stimulation points (Pfeifer and co workers, 2021).

Bursts are grouped in blocks of three cycles, followed by a silent gap of two cycles in which nothing

fires. The silence is part of the treatment, not a rest between treatments. In the Stanford design, the

pauses are there so the network can unlearn rather than merely pause: that is the rationale the pattern

was built on, stated here as the lab's design reasoning, not as a causal finding the human studies

separately established.

An optional noisy variant adds timing jitter of 23.5 percent to each burst onset, drawn from a uniform

distribution around the nominal onset time, copying the defined jitter of the noisy pattern used in the

six patient feasibility study.

Sessions run two hours, twice a day, for a total of four hours, matching the daily dose used in the

Stanford studies.

The code is simple enough to be written and checked in an afternoon: a loop, a shuffled list of four outputs,

timed bursts, timed silence. No network connection, no account, no data leaving the wrist.

## 4.5 The author's variant: a smaller shake that never stops

The pattern above is borrowed. The author also holds a simpler principle of his own, stated in his words:

what stops a shake is a smaller shake. On that principle the device would not fire in bursts at all. It would

run a constant micro vibration, set so low that the wearer cannot feel it, for as long as it is worn. The shake is

not retrained and not interrupted. It is met, continuously, by a smaller motion than itself.

The difference from coordinated reset has to be stated plainly, because the two ideas pull in opposite

directions. Coordinated reset is patterned, perceptible and intermittent, and its silence is part of the

treatment: the bursts are meant to desynchronize a network, and the pauses are meant to let the network

unlearn. A constant sub perceptual vibration has no pattern, no silence and no unlearning claim. If it does

anything, it does it only while it runs, which makes it a masking candidate in the terms of section 3. The self

test in section 6 is built to expose exactly that, with morning measurement before the first session of the day

and an off treatment follow up phase after the last one.

The variant is not without precedent, and the precedent has to be stated at its true size. Vibration set below

the threshold of perception is a documented treatment in one neighbouring field. Priplata and co workers

built insoles that fed subsensory mechanical noise to the soles of the feet, with the level set at 90 percent of

each wearer's sensory threshold, and measured reduced postural sway in young and elderly standers (2003),

and then in people with diabetic neuropathy and in people after stroke (2006). The mechanism proposed

there is stochastic resonance: a small amount of added noise lets a weak sensory signal cross the threshold of

detection, so the balance system works from better information. Seo and co workers applied subthreshold

white noise vibration to the wrist and measured better hand dexterity and stronger pinch in chronic stroke

survivors while the noise was on. In tremor itself, the documented vibration work is perceptible, not sub

perceptual: the coordinated reset bursts above, and a 2024 analysis in essential tremor in which a 250 Hz

stimulus was the only tested frequency that reduced tremor amplitude after the stimulation ended, an after

effect the authors put at about a minute (Cabral and co workers). So the honest position is this. Sub

perceptual vibration as a treatment exists in the record for balance and for hand function after stroke. Its use

as a constant, and its use against shaking, are the author's extension. No study of a constant sub perceptual

vibration used against shaking was located in any condition.

The wrist unit can deliver the variant with no new hardware: the same coin motors, run at reduced voltage,

with the level set by measurement, not by feel alone. The procedure the first build will use copies the

precedent's method. The wearer's just felt level is found by repeated trials, the drive raised and lowered

across several runs until the point where the motor is just felt is stable, and the constant level is then set at 90

percent of that measured threshold, the fraction Priplata's group used. Two cautions attach to that borrowing.

First, the signal differs in kind from the precedent's: the insole and wrist studies delivered noise, a random

signal, while a coin motor delivers a periodic signal at its rotation speed, and lowering the voltage makes

that signal smaller without making it random. Second, a measured threshold is only as steady as the motor

that delivers it: a coin motor's output drifts as the cell discharges, so the threshold is re measured as the build

settles and whenever the cell or a motor is changed, rather than assumed to hold. The variant borrows the

precedent's neighbourhood and its calibration method, not its mechanism. What the variant cannot borrow is

the Stanford dosing logic. Four hours a day in blocks belongs to the burst pattern and its unlearning claim. A

constant input raises a dosing question of its own, how many hours a day a person should carry a stimulus

they cannot feel, and the design has no answer to that question yet. It is recorded here as an open parameter,

not a detail.

## 4.6 The closed loop extension

The author also proposed a second stage, described here as a proposal only. Bands carrying motion sensors

would sit at the joints, at the wrist, the knuckles, the elbow or the knee. The sensors watch for the fast onset

signature of a spasm. When a spasm begins, the band fires a short counter burst in the same millisecond

window, either at the joint or through the fingertip wraps, aiming to interrupt the event rather than retrain the

circuit between events.

This is a different idea from coordinated reset, and it is weaker today for an honest reason: detecting the

onset of a TD spasm, and telling it apart from a voluntary movement, is itself an unsolved sensing problem.

A band that fires on voluntary movement would deliver stimulation at random times and would teach

nothing. The extension is recorded here because it is the author's, and it is marked as the part of the design

that needs a sensing study before it needs a circuit.

## 4.7 Parts and cost

Prices are approximate United States consumer prices for generic parts, checked against listings of the kind

any buyer would find. They are not quotes.

|Part|Approx. price|
|---|---|
|Conductive silver fibre finger sleeves, pack of 10 to 20, cut into wraps|$6 to $9|
|Coin vibration motors, 10 mm by 2 mm, pack of 5|$7 to $10|
|Conductive fabric tape, one roll|$8 to $12|
|Neoprene wrist wrap|$5 to $7|
|Seeed XIAO microcontroller|$6 to $15|
|Lithium polymer cell, 100 to 150 mAh|$5 to $8|
|Transistor switches, one per finger, with flyback diodes|not yet priced|
|Insulating barrier material for the palm runs|not yet priced|
|Connectors and strain relief|not yet priced|
|Cell charging and protection circuitry|not yet priced|
|**Total, core components**|**roughly $37 to $61**|

The total is the estimated cost of the core components, the rows with prices. The switching, insulation,

connection and charging items the design now requires are listed without prices because they have not been

priced yet, so the figure is an estimate of the core build, not a complete bill of materials.

For scale: the Rice team's planned commercial glove is priced at about 250 dollars, the Cala and Felix

wristbands are prescription devices sold at medical prices, and the GyroGlove sells at 5,899 dollars. Cost is

not a side detail in this design. A treatment a person can rebuild from a parts list is a different kind of object

from a treatment that needs a payer's permission.

## 5. The second design: a skin suit for Parkinson's disease
The author's larger claim is that the same approach scales. Some neurological conditions have no cure, and

for those conditions the honest target is not the disease but the layer of symptoms a person has to live inside.

His named case is Parkinson's disease, the same disease the borrowed pattern of section 2 comes from. The

hand device treats one symptom site, the fingertips, in one disorder. The suit treats the symptom layer of the

whole body in the disease where vibration has been studied most. This section documents the design at the

same standard as the hand device: what it is aimed at, what it cannot do, what already exists, and what a first

test would have to show.

## 5.1 What the suit is aimed at, and what it is not aimed at

Parkinson's disease is the progressive loss of dopamine producing neurons, above all in the substantia nigra.

The Parkinson's Foundation states the position without decoration: there is no cure yet, and treatment

manages symptoms rather than stopping the disease. No garment changes that, and this design does not

pretend to. A suit cannot restore a lost dopamine neuron. It cannot slow the progression. Anything sold as

more than symptom relief in Parkinson's disease is a false claim, and this paper does not make one.

What a garment could in principle reach is the symptom layer, and in this disease the layer is named in every

textbook. The cardinal motor signs of Parkinson's disease are resting tremor, rigidity, bradykinesia and loss

of postural reflexes, and freezing of gait travels with them as a classic feature of the condition. At the head

of that list sits the one symptom the author's principle was built for. His claim is that what stops a shake is a

smaller shake, and resting tremor is a shake: a rhythmic oscillation of about four to six cycles per second,

worst when the limb is still, in exactly the limbs a suit covers. Of the diseases a vibration garment could be

aimed at, this is the one where the target symptom and the proposed mechanism face each other directly. The

suit is aimed at tremor first, and at the rigidity and slowness of the same layer second. It is not aimed at the

disease.

## 5.2 The design

The suit is a skin tight base layer, a jacket and trousers or a single garment, cut from stretch cloth of the

same family as the finger sleeves. The conductive paths are woven into the cloth itself, as they are in the

wrap, so the wiring is the fabric and nothing rigid sits against the skin. Small flat vibration motors sit over

the major muscle groups of the arms, the legs, the back and the abdomen, held against the body by the

tension of the cloth. Every path runs back to one control unit at the waist, the grown up version of the wrist

unit in section 4.3. The suit is worn under ordinary clothing, as a layer nobody sees. That concealment is a

design requirement, not a decoration: the author's position is that the therapy should disappear into normal

dress, the way the wrap disappears onto a finger and the wiring disappears into the cloth.

The pattern the suit carries is the author's constant micro vibration of section 4.5, run below the level the

wearer can feel, across the muscle groups at once. Three engineering problems are stated rather than solved.

Power: dozens of motors cannot run for hours on the small cell that serves the wrist unit, so the suit needs a

larger battery at the waist, and its weight and heat have to be managed. Heat and skin: a tight layer carrying

warm electronics, worn for hours by a person whose hands may shake too much to adjust it easily, is a skin

risk before it is anything else. Washing: a garment with motors and woven conductors inside it cannot

simply go in a machine, and no answer to that is offered here. The suit is a design at garment scale. It has no

parts list and no price, because costing it now would mean inventing numbers.

## 5.3 The nearest neighbour, and a shelf that is not empty

One full body therapeutic garment already exists, and it is the honest comparison. The Exopulse Mollii suit,

made by Exoneural Network in Sweden and marketed by Ottobock, is a jacket and trousers carrying 58

electrodes that stimulate 40 muscle groups (Yen and co workers, 2026). It is not a vibration device. It

delivers low intensity electrical stimulation at 20 Hz to the antagonist of a spastic muscle, so the spastic

muscle relaxes through the reflex called reciprocal inhibition. Its stated uses, in the maker's own manual, are

the symptoms that follow cerebral palsy, multiple sclerosis, stroke and spinal cord injury. Parkinson's disease

is not among the named conditions. The one small study that gave the suit to people with Parkinson's disease

was an open label study of 200 adults with chronic pain diagnoses, 29 of them with Parkinson's disease, and

it measured pain, not tremor (Riachi and co workers, 2019; Perpetuini and co workers, 2023). Mollii is

prescribed and fitted, worn in sessions of about an hour every second day, and priced as a medical device.

The author's suit differs from it on every axis that matters here: vibration instead of electric current, constant

wear under street clothes instead of timed sessions, tremor as the named target, and a build meant to be

copied rather than prescribed. What Mollii proves is narrower and still useful: a powered garment covering

the whole body can be built, worn and sold, so the form factor is not fantasy. The mechanism and the target

are different, and the paper keeps them different.

Beyond Mollii, this disease is not an empty field, and the trial record belongs in the open. Vibration in

Parkinson's disease has been tested for twenty years, on platforms in clinics, not in garments. In the largest

early trial, 68 people with Parkinson's disease stood on a platform delivering random whole body vibration

in five series of one minute each. The standard motor score improved by about 17 percent immediately

afterwards, with tremor scores improved by about 25 percent and rigidity scores by about 24 percent (Haas

and co workers, 2006). The comparison was a resting period, not a sham platform, there was no washout

between the crossover arms, and the measurements were taken minutes after treatment. A double blind trial

of stochastic resonance platform vibration, five cycles of it given on three days against a 1 Hz sham,

improved the motor score by about 27 percent, with bradykinesia clearly better and the tremor reduction

short of the significance bar the authors set themselves (Kaut and co workers, 2011). The reviews that pool

this literature are cooler than its best trials. The Cochrane review of whole body vibration in

neurodegenerative disease found six Parkinson's trials and concluded that the evidence was insufficient for

the outcomes that matter. A pooled analysis of the multi session randomized trials, published in 2025, found

six studies and exactly one outcome better than active controls, static balance, with no difference in gait

speed, functional mobility or motor symptoms, and stated that no clinical recommendation can be made. A

2022 review of fourteen human studies found a small overall effect and called the human evidence

inconclusive. A 2021 systematic review and meta analysis of vibratory stimulation for balance and gait in

Parkinson's disease reviewed the same ground (Marazzi and co workers, 2021). So platform vibration in

Parkinson's disease is neither untried nor established. It is a shelf of small trials with mixed results, gathered

standing on machines.

The suit also enters the one disease where patterned vibration is a research programme rather than a

curiosity: the coordinated reset work of section 2 is Parkinson's work. The author's constant pattern is

therefore an alternative pattern hypothesis in the field where the patterned version is most studied, not an

extension into empty territory. That cuts both ways, and section 5.4 records the sharpest result it produced.

What the shelf does not contain is the author's form factor. No published or marketed full body vibration

garment for Parkinson's disease was located as of November 2026, at the strength of the searches recorded

in the verification log. The Parkinson's wearables that do exist are point devices: the CUE1 disk, worn on the

sternum, reported first in a pilot interventional study (Azoidou and co workers, 2025) and now, in its CUE1+

version, in a randomized sham controlled trial: fifty people with Parkinson's disease and gait problems,

twenty five on the active device and twenty five on sham, wearing the device eight hours a day for twelve

weeks, with exploratory differences favouring the active device on the standard motor score and on quality

of life, and with the authors stating plainly that the signals do not establish efficacy and require confirmation

in adequately powered trials (Azoidou and co workers, 2026; trial protocol in BMJ Open, 2025); and a 2026

preprint describing a single flexible patch with four motors worn on the thigh, delivering timed vibrotactile

cues for gait (the FlexAdapt Patch). A soft robotic garment has helped people with Parkinson's disease walk

in a Boston laboratory, but it pulls with cables and motors; it does not vibrate. The combination the author

describes, micro vibration woven into a concealed suit, worn constantly and aimed at tremor across the

whole body, has no located precedent. That is a statement about a search, not a claim about the whole world,

and it is worded that way on purpose.

## 5.4 The cautions that come first, and a first test

No published caution aimed at vibration wear in Parkinson's disease was located, and the cautions that do

exist are printed here at their true size. First, the platform trials were not careful about harm: the Cochrane

review found adverse events poorly reported, and in the trials that reported them the intervention appeared

safe. A training study of stochastic resonance platform vibration in 65 women over 50, split between two

training programs and trained twice a week for six weeks, found that the training can provoke or aggravate

back pain and lower limb pain, and about 12 percent of the women, roughly eight of them, did not finish for

health reasons (Hartman-Petrycka and co workers, 2021). It is a caution about standing on a shaking

platform, not about a garment, and it is recorded at that size. Second, the one Parkinson's specific warning is

about added noise. When subthreshold electrical noise was applied to the legs of fourteen people with

Parkinson's disease while they walked under visual perturbation, sway on the more affected side increased:

the noise made balance worse, and the authors concluded that this population may not need more sensory

noise (Alsaqabi and co workers). Noisy vestibular stimulation, in a separate trial of 32 people, produced no

gait benefit at all against sham (Peto and co workers, 2024). Neither study used mechanical vibration, and

neither settles the question for this suit. Together they say that a Parkinsonian sensory system does not

automatically thank you for extra input. Third, the only head to head test of the author's own pattern in this

disease went against it. In the thigh patch preprint named above, constant vibration was one of the

conditions, and it lost: timed, patterned cues reduced stride variability in 35 people with Parkinson's disease,

and constant vibration did not match them. The comparison has limits that belong on the same record: the

constant condition was perceptible stimulation, delivered to the thigh while the wearer walked, and

measured on gait, which is not the author's sub perceptual pattern aimed at tremor in a resting limb. The

preprint has not yet passed peer review, and a thigh patch is not a suit. It is still the strongest single piece of

evidence against the constant variant in the disease the author chose, and it is printed here rather than in a

footnote. No report of vibration worsening tremor or dyskinesia in Parkinson's disease was located, and no

study located documents whether a wearer habituates to a constant stimulus until it stops registering at all.

That last gap matters, because a stimulus the nervous system learns to ignore is the masking worry of section

3 in physiological dress. It is recorded as an unstudied risk, not a documented one.

Two wear rules are kept for this design on Parkinson's grounds. No stimulation over the chest in a first test,

because trunk stimulation is the least studied part of the design and a first test has no business there. No

wear during sleep, because resting tremor stops in sleep: a sleeping wearer would carry the skin and heat

risks with no symptom to aim at.

A first test, proposed here and labelled as a proposal, would have to show the following before anything

larger is discussed. One region only, a forearm or a calf, never the chest, in short supervised sessions, with

medication, dose and dose timing held fixed and every session run at the same point in the dose cycle. The

skin is inspected before and after, and the session stops for redness that does not fade, for heat at any motor

site, or for unusual fatigue. The measures are three. A small motion sensor taped to the limb records tremor

directly: its amplitude, and the share of each session it spends in the tremor band, with the same recording

taken the following morning before any session, so that carryover and masking can be told apart. The tremor

items of part III of the Movement Disorder Society revision of the Unified Parkinson's Disease Rating Scale

are scored by a clinician who does not know whether the motors ran. And the wearer keeps a diary of

freezing episodes and of sleep. No numeric bar is set for the suit in this paper. A first test of the suit would

set its own bar in advance, the way section 6 sets one for the hand device, and a result of no effect, or of

worse symptoms, would end the idea in print rather than quietly. Until a test of that kind exists, the suit

stands as what it is: a documented design, a real but mixed trial record behind the general idea, an empty

shelf behind the form factor, and one published comparison standing against its pattern.

## 6. A proposed n of 1 self test
The author is the intended first user, so the test is a single patient self test, an n of 1. A single patient test

cannot prove a treatment works in general. Done carelessly it cannot even prove it worked once, because TD

rises and falls with stress, sleep and the timing of medication doses. The protocol below is built to make one

person's result as hard to fool as it can be made.

**Bench characterization, before any wear.** The build is measured on the bench before it goes on the hand.

Record the vibration amplitude and frequency of each motor at the drive levels the pattern and the variant

use, the current each motor draws, the temperature of each motor after a full session's worth of sustained

running, and the actual runtime of the wrist unit on one charge against the four hour daily target. Those

measurements are the power budget section 4.3 says the design does not yet have. The bench gate has

criteria, and they are tied to the design's own numbers rather than to thresholds invented for the occasion.

The build passes if the measured runtime meets the four hour daily target at the pattern's duty cycle; if each

motor's temperature after sustained running stays within the limit its maker rates it for, a figure read from the

datasheet at build time; and if the measured burst timing and carrier match the specification of section 4.4 as

closely as coin motors allow, with any shortfall recorded rather than rounded away. The measured values are

written down either way, and they stand as the build's own specification. A build that cannot meet its own

numbers on the bench does not start the test.

**Fixed conditions.** Medication, dose and dose timing stay unchanged for the whole test. Sessions and

measurements happen at the same times of day. Any plan to change psychiatric medication is outside this

test entirely.

**Phase A, baseline, two weeks.** No device. The three core measures are taken every morning at the same

time, and the exploratory AIMS rating of measure 4 is made from the same morning videos. Before phase A

begins, the pencil and coin tasks are run daily for several days as familiarization, so the steepest part of the

practice curve is spent before the baseline starts rather than inside it.

**Phase B, treatment, four weeks.** The wraps are worn two hours twice a day on the worse hand. Outcome

measures are taken each morning before the first session. Morning measurement is deliberate: it tests what

carries over from the day before, not what the buzz does while it is on.

**Phase C, off treatment follow up, four weeks.** No device. Measures continue. The phase is a follow up,

not a washout: the hypothesis under test includes lasting effects, so the phase exists to watch whether a gain

fades or holds after stimulation ends, which is follow up logic. It runs four weeks because the first in human

study of section 2 found its gains still present at visits one and four weeks after stimulation ended, so a

shorter follow up could not tell a fading effect from a held one. If a gain was real learning, it should fade

slowly or hold. If it vanishes the first morning after the device stops, it was masking.

**Outcome measure 1, timed pencil grip.** Seated, forearm resting on the table. Grip a standard pencil

between the thumb and index finger of the tested hand and hold it clear of the table. Record the seconds until

the pencil drops, up to a cap of 120 seconds. Three tries, each one recorded, and the day's figure is the

median of the three, so one lucky grip cannot carry a day and practice across the weeks stays visible in the

record.

**Outcome measure 2, coin pickup.** Ten coins of mixed sizes sit on the table. Using only the tested hand,

pick the coins up one at a time and drop them in a cup. Record how many are banked in 60 seconds.

**Outcome measure 3, video rated spasm count.** A two minute phone video each morning: hands resting

palms down for thirty seconds, palms up for thirty seconds, then holding a sheet of paper at reading distance

for one minute. Count the visible involuntary finger movements per minute. What counts is defined in

advance: a spasm here is an involuntary finger movement of the choreic or athetoid kind, irregular and not

rhythmic. A rhythmic, regular, tremor like movement, if one appears in the videos, is recorded separately

and is not counted in the spasm figure, because the two are different phenomena and this test does not get to

blur them. The videos are saved, shuffled, and rated with their dates hidden. If a clinician or any second rater

can be found, that person rates them without knowing which phase each video came from.

**Outcome measure 4, a limited AIMS rating of the videos.** The same saved morning videos are also rated

against the Abnormal Involuntary Movement Scale, the scale the drug trials of section 1 report in, by the

blinded rater. The limits of that rating are stated plainly, because a two minute video of the hands is not an

AIMS examination. The scale's own procedure examines facial and oral movements, the extremities and the

trunk, and adds global judgments; the videos contain none of that. And the scale's upper extremity item, the

one item the videos could speak to, instructs the rater not to include tremor, which is one reason measure 3

defines its count the way it does. So the rating is scoped to what it can honestly be: an exploratory rating of

the upper extremity item only, made from the videos, and labelled exploratory wherever it is reported. Its

role is to stand alongside the three core measures as the clinical reference point, a check in the field's own

vocabulary. The success bar below stays on the core measures. That choice is named here rather than hidden,

and its weakness is plain: the core measures could clear the bar while this rating shows nothing. If that

happens, both results are reported, and the disagreement is part of the result.

**The bar, set in advance.** A change counts as a real signal only if the median of phase B beats the median of

phase A by at least 30 percent on at least two of the three core measures, and at least half of that gain is still

present in the fourth week of phase C. Percentage change is defined per measure against the phase A

median: for the pencil grip and the coin count, where more is better, it is the rise in the phase B median as a

share of the phase A median; for the spasm count, where fewer is better, it is the fall in the phase B median

as a share of the phase A median. The gain, for the retention rule, is the phase B median's improvement over

the phase A median in the measure's own units, and the fourth week of phase C is compared against that gain

in the same units. The retention rule is a tightening made in this revision: earlier drafts required only that

part of the gain remain in the fourth week of phase C, with no stated minimum. The 30 percent figure is an

exploratory pre commitment, chosen so the test has a fixed bar at all; it is not a clinical threshold and

corresponds to no established measure of meaningful change in TD. Anything less is recorded as no effect.

The numbers are published either way, including if the answer is no effect.

**Stopping rules.** Stop at once, and do not restart, for any of these: broken skin, a blister or a burn under a

wrap; a battery cell that is swollen, hot or damaged; new numbness or tingling in a fingertip that outlasts the

session. Stop and reassess if spasms are worse three days running, or if sleep is disturbed by lingering

sensations. The treating psychiatrist is told before the test starts, and a neurologist is told if one is involved

in the author's care. The device is never a reason to skip, delay or reduce prescribed medication.

## 7. Limitations and safety
This is a design paper. The device described here has not been built and tested by the author at the time of

writing, and nothing in this paper is a result.

The central limitation is the one in section 3: the stimulation pattern has its evidence, such as it is, in

Parkinson's disease, in small studies without sham controls, and TD is a different condition with a different

leading explanation. The pattern may do nothing in TD. The frequency and amplitude of a coin motor differ

from the laboratory tactors used at Stanford, which is a second, independent reason the effect may not

transfer.

The two extensions carry less evidence than the design they extend, and the difference should not blur. The

constant micro vibration variant of section 4.5 has no study behind it in any movement disorder. Its nearest

evidence sits in balance work and in stroke rehabilitation, gathered for different ends, and mostly for effects

measured while the stimulus was running. The Parkinson's suit of section 5 has no build, no parts list and no

test. It enters the disease with the strongest vibration literature of any condition this paper touches, and the

weakest novelty claim of anything in it: platforms have been tried there for twenty years with mixed results,

and the one wearable comparison located found constant vibration inferior to patterned cues. It is printed

because it is the author's design and because the prior art search behind it is itself a finding worth recording.

It is not printed as a recommendation that anyone build it or wear it.

The self test has the limits of its kind. The wearer cannot be blinded, because he can feel the device.

Expectation can move TD scores, as it moves most movement disorder scores. One person's fluctuation can

imitate a treatment effect across four weeks. Practice sits alongside expectation: the pencil and coin tasks are

learnable skills, and daily repetition across ten weeks would improve them with no device involved, which is

why the protocol spends familiarization runs before the baseline and records every try. The protocol narrows

these problems with morning measurement, an off treatment follow up phase and a bar set in advance. It

does not remove them.

**A note on the searches behind the novelty claims.** The statements in this paper that a device of a given

kind was not located rest on searches run on 20 November 2026 across the published literature, the United

States trial registry, maker documentation and patent records, recorded in the author's verification log. They

are statements about those searches, at that date, and are worded that way so a reader can weigh them.

Safety notes are plain. The wraps deliver mechanical vibration only, at an amplitude intended to be low, to

intact skin; low amplitude is a design intention, to be confirmed by the bench measurements of section 6, not

an established property of a build that does not exist yet. The palm runs are nickel bearing tape: the

insulating barrier described in section 4.2 is part of the safety case, and the build is not worn with a damaged

barrier, over skin that reddens or itches under the tape in a way that suggests nickel sensitivity, or with the

runs soaked through, because wet insulation is not insulation. The lithium polymer cell is the main hazard in

the build: charge it only with a proper charger, never puncture or bend it, and retire it at the first sign of

swelling. Do not wear the wraps on broken or irritated skin. Do not wear them in water. Anyone with an

implanted electrical device, a seizure disorder or a skin condition of the hands should not copy this build

without medical advice, and nobody should read this paper as permission to change a prescription.

## 8. Conclusion
TD leaves the people who have it with two approved drugs, modest average gains and no established

wearable device treatment made for it. A few miles of literature away, a patterned fingertip vibration built to

desynchronize motor circuits has produced small, careful, promising results in Parkinson's disease, and

students in Houston have shown the hardware can be copied for the price of a pizza night. This paper joins

those facts to one design decision, a wrap instead of a glove, and to one discipline, a test written down

before it is run. The design's core components cost roughly 37 to 61 dollars. The test costs ten weeks of

mornings. What it returns, if run as written, is an honest answer for one person, and a design that anyone

else with the same problem can follow once the open component choices named in section 4 are made. The

expansion adds the author's own pattern, a constant vibration too small to feel, and the same wiring grown to

the scale of a concealed suit for the symptom layer of Parkinson's disease, the condition the borrowed

pattern came from, and likewise a disease with no cure. Neither extension has been tested, and the suit has

not been built. They stand in this paper the way the wrap does: as the author's designs, with the record

behind each one stated at its true size, and with the next step for each one a test that is allowed to fail.

## References
1. Tass PA. A model of desynchronizing deep brain stimulation with a demand controlled coordinated

reset of neural subpopulations. Biological Cybernetics. 2003;89(2):81 to 88.

2. Tass PA, Qin L, Hauptmann C, et al. Coordinated reset has sustained aftereffects in Parkinsonian

monkeys. Annals of Neurology. 2012;72(5):816 to 820.

3. Adamchic I, Hauptmann C, Barnikol UB, et al. Coordinated reset neuromodulation for Parkinson's

disease: proof of concept study. Movement Disorders. 2014;29(13):1679 to 1684.

4. Syrkin-Nikolau J, et al. Coordinated reset vibrotactile stimulation shows prolonged improvement in

Parkinson's disease. Movement Disorders. 2018;33(1):179 to 180. doi: 10.1002/mds.27223

5. Pfeifer KJ, Kromer JA, Cook AJ, et al. Coordinated reset vibrotactile stimulation induces sustained

cumulative benefits in Parkinson's disease. Frontiers in Physiology. 2021;12:624317. doi:

10.3389/fphys.2021.624317

6. Pfeifer KJ, Cook AJ, Yankulova JK, et al. Clinical efficacy and dosing of vibrotactile coordinated

reset stimulation in motor and nonmotor symptoms of Parkinson's disease: a study protocol. Frontiers

in Neurology. 2021;12:758481. doi: 10.3389/fneur.2021.758481. Trial registration NCT04877015.

7. Tass PA. Vibrotactile coordinated reset stimulation for the treatment of Parkinson's disease. Neural

Regeneration Research. 2022;17(7):1495 to 1497. doi: 10.4103/1673-5374.329001

8. Azoidou V, et al. A pilot interventional study on feasibility and effectiveness of the CUE1 device in

Parkinson's disease. Parkinsonism and Related Disorders. 2025;133:107349.

9. Non invasive device to alleviate symptoms in people living with Parkinson's: study protocol for a

multicentre phase II double blind randomised controlled trial. BMJ Open. 2025;15(4):e096051. doi:

10.1136/bmjopen-2024-096051. Trial registration NCT06174948.

10. Rice University News and Media Relations. Rice students develop low cost vibrotactile glove to help

treat Parkinson's disease. April 9, 2025. https://news.rice.edu/news/2025/rice-students-develop-low
cost-vibrotactile-glove-help-treat-parkinsons-disease

11. Suk HJ, Buie N, Xu G, Banerjee A, Boyden ES, Tsai LH. Vibrotactile stimulation at gamma

frequency mitigates pathology related to neurodegeneration and improves motor function. Frontiers in

Aging Neuroscience. 2023;15:1129510. doi: 10.3389/fnagi.2023.1129510. Note: an animal study in

mouse models of Alzheimer's type neurodegeneration, cited here only to show that patterned vibration

can change cortical activity in animals.

12. United States Food and Drug Administration. 510(k) record K243848, Cala kIQ, Cala Health Inc.

Decision date January 16, 2025.

13. University of Minnesota College of Science and Engineering. University of Minnesota spin off

receives FDA clearance for AI powered essential tremor treatment. July 2, 2025.

14. Patel AR, Hauser RA, Citrome L, et al. VMAT2 inhibitors for the treatment of tardive dyskinesia: a

narrative review. CNS Spectrums. 2025;30(1):e90. doi: 10.1017/S1092852925100643

15. Touma KTB, Scarff JR. Valbenazine and deutetrabenazine for tardive dyskinesia. Innovations in

Clinical Neuroscience. 2018;15(5 to 6):13 to 16.

16. Yen JM, Kamsani NS, Lai HS, Tang N, Chew E. Clinical Outcomes of Individualized

Electrostimulation Using a Wearable Electro Suit and Qualitative Feedback From a Mixed Cohort of

Survivors of Stroke and Spinal Cord Injury With Spasticity: Case Series. JMIR Rehabilitation and

Assistive Technologies. 2026;13:e81522. Describes the Exopulse Mollii suit: 58 electrodes, electrical

stimulation, a different method from the one proposed here.

17. Engadget. GyroGlove is a hand stabilizing glove for people with tremors. January 2024.

18. Priplata AA, Niemi JB, Harry JD, Lipsitz LA, Collins JJ. Vibrating insoles and balance control in

elderly people. The Lancet. 2003;362(9390):1123 to 1124.

19. Priplata AA, Patritti BL, Niemi JB, et al. Noise enhanced balance control in patients with diabetes and

patients with stroke. Annals of Neurology. 2006;59(1):4 to 12. doi: 10.1002/ana.20670

20. Seo NJ, Kosmopoulos ML, Enders LR, Hur P. Effect of remote sensory noise on hand function post

stroke. Frontiers in Human Neuroscience. 2014;8:934. doi: 10.3389/fnhum.2014.00934

21. Cabral AM, Lora-Millán JS, Pereira AA, Rocon E, Andrade AO. On the effect of vibrotactile

stimulation in essential tremor. Healthcare. 2024;12(4):448. doi: 10.3390/healthcare12040448

22. Liu C, Zhang K. A wearable finger tremor suppression orthosis using the PVC gel linear actuator.

IEEE Robotics and Automation Letters. 2024. doi: 10.1109/LRA.2024.3369492

23. Kurita Y, Shinohara M, Ueda J. Wearable sensorimotor enhancer for a fingertip based on stochastic

resonance. Proceedings of the 2011 IEEE International Conference on Robotics and Automation.

2011:3790 to 3795. doi: 10.1109/ICRA.2011.5980283

24. Jankovic J. Parkinson's disease: clinical features and diagnosis. Journal of Neurology, Neurosurgery

and Psychiatry. 2008;79(4):368 to 376. Source of the cardinal signs named in section 5.1.

25. Parkinson's Foundation. About Parkinson's disease; and Treatment. parkinson.org. Sources of the

statement that there is no cure and that treatment manages symptoms, used in section 5.1.

26. Exoneural Network AB. EXOPULSE Mollii Suit user manual, version 1.6 EN, 2021; and Ottobock.

Exopulse Suit: information for practitioners. Sources of the mechanism, indications and session dose

used in section 5.3.

27. Haas CT, Turbanski S, Kessler K, Schmidtbleicher D. The effects of random whole-body vibration on

motor symptoms in Parkinson's disease. NeuroRehabilitation. 2006;21:29 to 36.

28. Kaut O, Allert N, Coch C, et al. Stochastic resonance therapy in Parkinson's disease.

NeuroRehabilitation. 2011;28(4):353 to 358. doi: 10.3233/NRE-2011-0663

29. Sitjà Rabert M, Rigau Comas D, Fort Vanmeerhaeghe A, et al. Whole-body vibration training for

patients with neurodegenerative disease. Cochrane Database of Systematic Reviews. 2012;(2).

30. González García P, et al. Multi session whole body vibration program on Parkinson's disease

symptoms: systematic review and meta analysis. Journal of Bodywork and Movement Therapies.

2025;45:853 to 863. doi: 10.1016/j.jbmt.2025.10.020

31. Arenales Arauz YL, Ahuja G, Kamsma YPT, Kortholt A, van der Zee EA, van Heuvelen MJG.

Potential of whole body vibration in Parkinson's disease: a systematic review and meta analysis of

human and animal studies. Biology. 2022;11(8):1238. doi: 10.3390/biology11081238

32. Marazzi S, Kiper P, Palmer K, Agostini M, Turolla A. Effects of vibratory stimulation on balance and

gait in Parkinson's disease: a systematic review and meta analysis. European Journal of Physical and

Rehabilitation Medicine. 2021;57(2):254 to 264. doi: 10.23736/S1973-9087.20.06099-2

33. Alsaqabi E, DiBianca S, Sansare A, Verma K, Reimann H, Jeka J. Stochastic resonance stimulation

effect on stability during walking in people with Parkinson disease. International Biomechanics.

2025;12(1):81 to 94. doi: 10.1080/23335432.2025.2584665. First reported as a conference abstract,

Movement Disorders. 2024;39(suppl 1). PMID 41195808.

34. Cheng T, Kong Y, Wu K, Liang Z, Yang B, Li J, Liu T, Chen C, Yang H, Pan B, Cheng J, Mo F. An

intelligent E-skin with spatiotemporal vibrotactile cues enable personalized gait rehabilitation in

Parkinson's disease (the FlexAdapt Patch). Research Square preprint, posted 18 February 2026. doi:

10.21203/rs.3.rs-8883462/v1. Not peer reviewed at the time of writing.

35. Kololichalil A, Jadeer KM, Ganesh R, Verma R, Patil V. Neuromodulation therapies in the

management of tardive dyskinesia: a scoping review. Indian Journal of Psychiatry. 2026;68(8):683 to

691. doi: 10.4103/indianjpsychiatry_1300_25.

36. Azoidou V, Bhadra E, Camboe E, et al. Sternum worn vibrotactile device in Parkinson's disease: a

randomised, double blind, placebo controlled pilot trial. npj Parkinson's Disease. 2026. doi:

10.1038/s41531-026-01448-y. Trial registration NCT06174948.

37. Perpetuini D, Russo EF, Cardone D, Palmieri R, De Giacomo A, Pellegrino R, Merla A, Calabrò RS,

Filoni S. Use and effectiveness of electrosuit in neurological disorders: a systematic review with

clinical implications. Bioengineering. 2023;10:680. doi: 10.3390/bioengineering10060680. A

systematic review of the Exopulse Mollii suit literature; its table of studies includes Riachi et al., one

hour sessions of the suit in people with chronic pain, among them people with Parkinson's disease,

with pain scores as the outcome.

38. Peto D, Schmidmeier F, Katzdobler S, Fietzek UM, Levin J, Wuehr M, Zwergal A. No evidence for

effects of low intensity vestibular noise stimulation on mild to moderate gait impairments in patients

with Parkinson's disease. Journal of Neurology. 2024;271:5489 to 5497. doi: 10.1007/s00415-024
12504-z

39. Hartman-Petrycka M, Lebiedowska A, Stolecka-Warzecha A, Szumski A, Błońska-Fajfrowska B. The

influence of stochastic resonance whole body vibration on women over 50 years of age: preliminary

studies based on patients' own experiences. Applied Sciences. 2021;11:3980. doi:

10.3390/app11093980

## Disclosure
The author has tardive dyskinesia and is the intended first user of the device described. The design was

developed in conversation with an AI assistant in July 2026; the design decisions, the form factor and the

closed loop extension are the author's. The November 2026 expansion is likewise the author's: the wrap form

factor that replaced the cap, the constant micro vibration principle, and the concealed body suit for

Parkinson's disease were all stated by him, in his words, and documented by the assistant. No funding was

received. No device described here has regulatory clearance for any condition, and the coordinated reset

glove research cited is investigational even in Parkinson's disease.
