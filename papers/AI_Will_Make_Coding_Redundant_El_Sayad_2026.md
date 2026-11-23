---
title: "AI Will Make Coding Redundant for Humans"
authors: "El Sayad, Abdelrahman"
date: 2026-11-21
zenodo_version: "1"
doi: "10.5281/zenodo.24408554"
zenodo: "https://doi.org/10.5281/zenodo.24408554"
license: "cc-by-4.0"
pdf: "papers/AI_Will_Make_Coding_Redundant_El_Sayad_2026.pdf"
markdown: "papers/AI_Will_Make_Coding_Redundant_El_Sayad_2026.md"
---
# AI Will Make Coding Redundant for Humans
Abdelrahman El Sayad

## Abstract
This paper argues a narrow claim at full strength: AI will make coding, defined as writing code from a

specification, redundant for humans. Not software work in general. The writing task itself, the core daily

work of the median professional programmer, is being automated on a measurable curve, and the labor

market has begun to break where the claim predicts, at the junior rung. The capability evidence is a

benchmark record that moved from about 2 percent to about 81 percent in two years, and a task horizon that

keeps doubling, faster recently than before. The labor evidence is a near 20 percent decline in employment

for software developers aged 22 to 25 from its late 2022 peak, and a collapse in the new graduate share of

hiring at the largest technology companies. The strongest objections are stated at full strength and answered:

a randomized trial in which experienced developers were slowed down by AI tools, official projections of

developer job growth, a rebound in job postings, the Jevons argument that cheaper code means more coders,

and the verification bottleneck created by flawed generated code. None of them touch the claim as defined,

and two of them, read closely, describe its shape. The author's framing is simple: "humans won't need to

know how to code anymore they will need to know how to use ai and how to prompt properly and use

tools." The human skill that survives is operating the machine that writes the code. Four dated predictions,

frozen before this paper was drafted, close the argument, together with the conditions that would kill it.

## 1. The claim, defined
Claims about AI and jobs usually fail before they start, because nobody says what the words mean. This

paper defines its terms first, and the whole argument stands or falls on the definitions.

Coding means writing code from a specification. A human is given, or works out, what a program should do,

and then produces the code that does it. That translation work, from intent to syntax, is the core daily task of

the median professional programmer. Coding does not mean software work in general, which also includes

deciding what to build, designing systems, checking output, and answering for the result. Those are different

tasks, and this paper treats them differently.

Redundant means the task no longer needs a human doing it. It does not mean the job title disappears; titles

routinely survive the task that named them. It does not mean software employment falls to zero. It means a

human being paid to sit and write code from a specification becomes as unusual as a human being paid to do

arithmetic by hand after the calculator: the activity continues, the occupation built on doing it manually does

not.

The claim is therefore about a task, not a title, and about the direction of a curve, not about next quarter. It

says the writing task is being automated, already visibly, in capability measurements and in hiring data. The

author's own statement of the shift is the one quoted in the abstract: the skill that replaces coding is knowing

how to use AI, how to prompt properly, and how to use tools. Directing, specifying, and verifying are not

three separate successor professions. They are parts of that one skill: operating the machine that writes the

code. The shift is from syntax to direction.

Two clarifications. First, the claim is not that today's tools are good enough to write all production code

unsupervised. Section 5 gives the flaws their full weight. The claim is about where the curve points and what

the labor market is already doing in response. Second, the claim is not that expertise stops mattering. It is

that expertise changes its object: from producing code to judging it.

## 1.1 Why coding, and why now

There is a reason this claim is about coding and not about carpentry, plumbing, or law. Coding is the first

skilled craft that spent decades writing itself down in a form a machine can read.

For the last forty years, humans have written code at scale, and the work did not vanish when it shipped. It

accumulated. The code itself sits in repositories. Around it sits everything the craft produced while working:

the documentation, the questions and the answers, the bug reports and the fixes that closed them, the

discussions about why one approach beat another. The open source movement put much of that record in

public, in plain text, indexed and searchable. No earlier craft left a memory like this. A master carpenter's

knowledge lived in his hands and died with him. A programmer's knowledge lives in files.

That record is what the AI reaches for. The model did not learn to code from rules about code. It learned

from the corpus the craft left behind, and it can draw on that corpus at a scale no human memory matches.

This is the cause underneath everything measured in section 3. The corpus is the cause. The model is the

reader.

It is also why earlier automation did not do this. Compilers and higher level languages raised the level of

abstraction, and each time, humans still had to write the next layer by hand, because the machine held none

of the craft's memory. It could translate what a human wrote. It could not supply what a human knew. Now

the machine holds the memory, and the human's remaining part is the part the corpus cannot supply:

deciding what to build, stating it exactly, and checking what comes back. Humans spent forty years teaching

the machine their craft without meaning to. The redundancy is the receipt.

## 2. Exhibit zero: the author
The author of this paper has little to no coding experience, by his own standing description, on record in his

own files since September 12, 2026. He cannot sit down and write the systems he ships. He ships them

anyway, by directing AI agents: an operating system project, games, research tooling, and a maintained

catalogue of 5,613 npm packages.

Five years ago this workflow was impossible for a non coder. There was no agent to direct. A person who

could not write code could have ideas for software and pay other people to build them, and that was the end

of it. Today one person with no coding skill specifies what he wants, directs the machines that write it,

checks what comes back, and ships running software. That is exhibit zero. One person is not a labor market.

But it establishes what the rest of the paper needs: the workflow the thesis predicts is not hypothetical. It

exists, it produces real output, and the only open questions are how far it spreads and how fast.

## 3. The capability curve
The spine of the argument is a measurement series, not a vibe. In October 2023, SWE-bench, a benchmark

built from 2,294 real GitHub issues, was released. The best model in the world, Claude 2, resolved 1.96

percent of the issues. Writing working fixes for real software problems was, measured plainly, something AI

could essentially not do. In August 2024, at the launch of the human screened subset called SWE-bench

Verified, GPT-4o resolved 33.2 percent. On November 24, 2025, Claude Opus 4.5 scored 80.9 percent on

SWE-bench Verified in its vendor's system card, the first model above 80 percent. In two years the field

went from one issue in fifty to four issues in five, on the same family of real world tasks. Benchmarks can

be gamed, and the 80.9 figure is flagged here as a vendor reported result. But no reading of the series,

skeptical or friendly, turns it into a flat line.

The second series matters more, because it measures duration, not just success on short tasks. METR, an

independent evaluation organization, measures the length of software task an AI agent can complete at 50

percent reliability, in human expert time. Its March 2025 study found that this horizon has doubled every 7

months since 2019, a fitted doubling time of about 212 days. Its January 2026 update, on an expanded suite

of 228 tasks, found the doubling has sped up: about 131 days since 2023, and about 89 days since 2024. The

frontier model in that release, Claude Opus 4.5, had a 50 percent horizon of 320 minutes, against 3.5

minutes for GPT-4 as re estimated on the same scale. A task horizon is the right unit for a redundancy claim,

because jobs are made of tasks with durations. A system that reliably finishes five hour tasks is not an

autocomplete. It is most of a workday, done without a human writing anything.

The third series is what happened when the tools met working programmers. In a controlled experiment run

in 2022, 95 developers implemented an HTTP server in JavaScript, half with GitHub Copilot and half

without. The group with Copilot finished 55.8 percent faster. That was the founding productivity result for

AI pair programming, with a wide confidence interval and one well specified greenfield task: early evidence

that the writing step itself speeds up when a machine does the typing, not proof of whole job replacement.

The fourth series comes from inside the largest codebases on earth, and its figures are self reported, with

counting methods unpublished. In October 2024, Sundar Pichai said on Alphabet's earnings call that more

than a quarter of all new code at Google is generated by AI, then reviewed and accepted by engineers. In

April 2026, Pichai wrote that the figure had reached 75 percent of all new code at Google, AI generated and

approved by engineers, up from 50 percent the previous fall. Satya Nadella, asked in April 2025 what share

of Microsoft's code is written by AI, answered that it was maybe 20 to 30 percent of the code inside

Microsoft's repositories today, with some projects probably all written by software. These are company

reported figures, not audited measurements, and the Google figure counts code that engineers then review

and approve, not code shipped untouched. They are used here for one purpose only: the direction and rough

scale of adoption inside the firms with the most code and the most engineers. On that purpose they agree

with the benchmark series.

In March 2025, Anthropic's CEO Dario Amodei said he expected AI to be writing 90 percent of code within

three to six months, and possibly essentially all of it within twelve. That is a claim by an interested party,

noted for the record. The argument here rests on the measured series, not on it.

## 4. The labor market is already moving
If the writing task is being automated, the damage should not appear evenly. It should appear first where the

work is closest to pure writing from a specification, which is the junior rung, whose assigned work is the

most routine, the most specified, and the least entangled with judgment about a particular codebase. The

senior rung should hold up longer. That is the pattern the data shows.

The Stanford Digital Economy Lab study by Brynjolfsson, Chandar, and Chen, built on ADP payroll data,

found that employment for software developers aged 22 to 25 decreased by nearly 20 percent from its late

2022 peak. In the study's current version, employment of young workers aged 22 to 25 across AI exposed

occupations stands 19 percent below where it would be had it kept pace with less exposed peers, and the

adjustment runs through reduced hiring of the young, not through firing. Experienced workers in the same

occupations show no comparable gap. The authors themselves describe their findings as early, descriptive

indicators, not causal estimates, and this paper keeps that caveat attached to the numbers. The caveat matters

and it does not dissolve the pattern. A descriptive break that begins with the arrival of capable coding tools,

concentrates in the most AI exposed occupations, concentrates further in the youngest age band inside those

occupations, and is absent for experienced workers in the same jobs is the fingerprint the thesis predicts.

Alternative explanations, a general hiring freeze, interest rates, post pandemic correction, have to explain

why the break is age graded and exposure graded at the same time. The thesis explains both gradings with

one mechanism: employers stopped hiring people to do the task the machines had just learned to do, and the

people who did that task most purely were the young.

Hiring data tells the same story from the other side. SignalFire's State of Tech Talent Report for 2025 found

that new graduates account for just 7 percent of hires at the fifteen largest technology companies. New

graduate hiring at those companies fell 25 percent from 2023 and over 50 percent from pre pandemic levels

in 2019. At startups, new graduates make up under 6 percent of hires. In the same period, hiring of

professionals with two to five years of experience rose 27 percent at the large companies. The contraction is

specific to the entry rung, not to hiring overall. SignalFire attributes the drop only in part to AI, also naming

smaller funding rounds, shrinking teams, and the end of the low interest rate hiring boom. That honesty is

noted, and it cuts less than it appears to. Every one of those other causes is a reason to hire fewer people in

general. None of them is a reason to cut the cheapest rung by half while raising hiring one rung up, unless

the cheapest rung's work is the work that changed. What changed about entry level work, in exactly those

years, is that a machine learned to do its defining task.

A pipeline detail deserves emphasis. Professions reproduce through their junior rung: senior engineers are

juniors who survived. If the junior rung is automated away, the profession does not merely shrink. It stops

renewing itself, and the senior rung becomes a wasting asset, a cohort aging without replacement. The data

above is two to three years of a trend, not a completed transition. But its shape is the thesis's shape: the base

goes first.

## 5. The objections, and the answers
## 5.1 The slowdown study

The strongest single result against this paper's claim is METR's randomized controlled trial of July 2025.

Sixteen experienced open source developers worked on 246 real issues from large repositories they had

contributed to for years, repositories averaging over a million lines of code, with each issue randomly

assigned to AI allowed or AI disallowed. With AI tools, mainly Cursor Pro with Claude 3.5 and 3.7 Sonnet,

the frontier tooling of early 2025, the developers took 19 percent longer to finish. The belief gap is as

striking as the slowdown: before the study the developers forecast that AI would speed them up by 24

percent, and after experiencing the measured slowdown they still believed it had sped them up by 20

percent. Perception and measurement pointed in opposite directions. This paper carries the study at full

strength. It should also be recorded that METR's February 2026 follow up, with 57 developers and over 800

tasks on late 2025 tools, produced raw estimates suggesting modest speedups, but with confidence intervals

including zero and a large share of tasks withheld by participants who did not want to do them without AI.

METR itself called the follow up an unreliable signal and weak evidence at best. The 2025 slowdown stands

as published; the follow up is not clean evidence of acceleration either. On this specific ground, it is a

standoff.

The answer is about what ground the study measured. It measured experienced developers, on codebases

they knew deeply, doing work where the scarce input is not writing code but knowing which code to write,

knowledge built over years of contribution. That is the population and the setting where this paper's thesis

predicts the least effect, today. The thesis is not that experts on their own repositories are already redundant

in 2025. It is that the writing task is being automated and the junior pipeline breaks first. A study of experts

doing judgment heavy work on familiar ground, with early 2025 tools, cannot refute a claim about specified

writing work and new graduates, any more than master carpenters gaining nothing from a nail gun would

refute the claim that the nail gun changed who gets hired to frame houses. If slowdown results of this type

replicate at scale across settings, including junior developers on specified tasks with current tools, the thesis

dies. That condition is written into the kill criteria in section 7, and it has not happened.

## 5.2 The projections and the rebound

The United States Bureau of Labor Statistics projects employment of software developers to grow 17.9

percent from 2023 to 2033, adding 303,700 jobs, much faster than the average occupation, in a projection

cycle that deliberately modeled AI impacts. Its current handbook projects the combined category of

developers, quality assurance analysts, and testers to grow 10 percent from 2025 to 2035. And Indeed's

Hiring Lab reported in November 2026 that US software development job postings rose 23.8 percent year

over year. These are real numbers from serious sources. This paper does not ignore them. It reads them

closely.

Read closely, the growth sits at the top. Analyses of Indeed data report that senior roles took about 71

percent of the posting growth between May 2025 and May 2026, while entry level roles were only about 4.5

percent of software postings in the first quarter of 2026. Indeed itself notes that software postings remain

about 19 percent below their February 2020 level and that the rebound is from a low base. The Bureau's own

categories tell the same story quietly: it separates software developers from computer programmers, the

narrower occupation defined by writing code to specification, and the programmer occupation is the one

projected to shrink while developers grow. The growth sits in design, judgment, and responsibility, not in

code transcription. That is not a refutation of this paper's claim. It is the claim, stated in the government's

categories. A profession can grow at the top while its base is automated away. The postings rebound shows

demand for software and for senior people who direct and verify. It does not show a recovery in hiring

humans to write code from specifications, and the junior numbers in section 4 show the opposite.

## 5.3 Jevons

The Jevons argument is the most respectable objection, and it deserves its strongest form. When steam

engines became more efficient, coal consumption rose, because cheaper power opened uses that were

previously uneconomic. Applied to software: developer time has been the binding constraint on how much

software gets built, organizations carry deep backlogs of software never worth its cost, and if AI cuts the

cost of code, the backlog becomes buildable, demand for software rises faster than unit cost falls, and

demand for the people around software rises with it. The Bureau of Labor Statistics, by its own published

account, used reasoning of this kind in its projections, and commentators have made the same case with

examples such as ATMs and bank tellers. The mechanism is real, and this paper concedes it.

The concession does not save coding. It saves software. Jevons grows demand for the output and for the

roles that specify, direct, and verify the output. It says nothing about demand for the manual act that got

cheaper. Cheaper coal power did not create jobs for the men who had stoked the old engines by hand; it

created an economy that used more power, run by fewer hands per unit of it. Cheaper code means more

code, written by fewer hands, directed by people whose skill is direction. The teller example, read carefully,

agrees: tellers multiplied by doing a different job, relationship work. The automated task stayed automated.

If AI makes code ten times cheaper and the world responds by demanding twenty times more software, the

result is a software saturated world and a doubling of demand for directors and verifiers, alongside a

collapse in demand for the act of writing. That world is this paper's prediction, not its rebuttal. Jevons

answers a question about volume. The thesis is about who, or what, does the writing.

## 5.4 The verification bottleneck

The final objection is the one this paper agrees with almost completely. Generated code is flawed at rates

that make unsupervised use irresponsible. Veracode's 2025 GenAI Code Security Report tested more than

100 large language models on tasks that could be completed securely or insecurely, and found that 45

percent of generated code samples failed the security tests and introduced an OWASP Top 10 vulnerability.

Java samples failed at 72 percent. Security performance stayed flat as models improved at functioning code,

and Veracode's Spring 2026 update found the security pass rate still stuck at about 55 percent. GitClear,

analyzing 211 million changed lines from 2020 to 2024, found the copy pasted share of changed lines rising

from 8.3 percent to 12.3 percent, the moved share, its proxy for refactoring and reuse, falling from 24.1

percent to 9.5 percent, and code churn rising from 3.1 percent to 5.7 percent, with GitClear's own interest as

a seller of code quality tooling noted. Developers report the burden themselves: in Stack Overflow's 2025

survey, trust in the accuracy of AI output fell from 43 percent in 2024 to 33 percent, active distrust rose to 46

percent, and the top frustration, cited by 66 percent, was AI solutions that are almost right but not quite.

GitLab's 2025 survey named the pattern the AI Paradox: coding is faster than ever, yet teams lose about 7

hours per team member per week to bottlenecks in testing, security review, compliance, and coordination,

and only 37 percent would trust AI to handle daily work without human review. DORA's delivery research

agrees: in 2024 higher AI adoption was associated with lower throughput and stability, and in 2025

throughput improved while instability persisted.

All of that is true, and none of it defends coding. It identifies the survivor. If machines write code that is

almost right, insecure at a 45 percent rate on security sensitive tasks, and prone to duplication and churn,

then the indispensable human work is specifying precisely what is wanted and verifying rigorously what

comes back. That is section 6 of this paper, not a refutation of it. The bottleneck argument proves that the

human does not leave the loop. The thesis never said the human leaves the loop. It said the human stops

writing. The bottleneck data shows the profession's center of gravity moving, in real time, from production

to inspection, which is the migration this paper predicts.

## 6. What survives: operating the machine
Strip the writing task away and what is left is one skill with several faces, the one the author named:

knowing how to use AI, how to prompt properly, and how to use tools. Unpacked, it has three working parts.

The first part is direction. Deciding what to build, in what order, toward what end. This is judgment about

value, and no benchmark in this paper measures a machine doing it for a business that bears the

consequences.

The second part is specification. Saying exactly what is wanted, precisely enough that a machine can build it

and a checker can test it. Prompting properly is not a trick of phrasing. It is specification, the oldest hard

problem in software, moved to the front of the process. The person who can state intent completely, with its

edge cases and exclusions, is the person the machine amplifies. This is the new literacy that replaces syntax.

The third part is verification. Reading output critically, testing it, checking its security, and answering for it.

Section 5.4 documented why this part is not optional: a 45 percent security failure rate on sensitive tasks,

output that is almost right in ways that take experience to catch, and persistent delivery instability.

Verification is where responsibility lives, and responsibility is the one thing that cannot be delegated to a

system that cannot be blamed.

Notice what kind of skill this composite is. It is not a lesser version of coding, and it is not coding renamed.

A person can possess it in full with no ability to write code at all, as exhibit zero demonstrates. The labor

data in section 4 shows exactly this split: the roles that hold up are built on direction and verification, and

the roles that collapse are built on writing from a specification. The profession is not dying. It is being re

founded on a different skill, and the re founding is not gentle to the people whose training was all in the old

one. The practical conclusion is blunt. Learn to operate the machine: how to use AI, how to prompt properly,

how to use tools, how to specify, and how to verify. Syntax is becoming what long division became,

something the machine does while the human decides what it means.

## 7. Predictions
The following predictions were frozen in writing on November 20, 2026, before the evidence sweep for this

paper and before drafting. They are stated here in substance, unedited, together with the conditions that

would kill the thesis.

P1. By December 31, 2028, the METR style task horizon, the length of software task an AI agent completes

at 50 percent reliability, reaches 40 hours or more, continuing its established doubling trend.

P2. By December 31, 2028, at least one major platform company, Google, Microsoft, or a comparable,

reports that a majority of its new code is machine authored.

P3. By December 31, 2028, entry level software developer employment and postings sit below their 2026

levels. The junior pipeline breaks first; senior and architect roles hold up longer.

P4. By 2030, the default unit for new software work is one human director plus agents, not a team of human

coders. This is the weakest of the predictions and is labeled as such.

What would kill the thesis: the task horizon doubling stalls for two or more years; slowdown results of the

METR 2025 type replicate at scale across settings, not just in one study of experienced developers on

familiar codebases; or junior hiring recovers to its 2023 level and holds. Any one of the three, and the claim

in this paper should be read as falsified, not revised into safety.

## 8. Limitations
This paper's limits are plain. The capability series rest partly on vendor reported results, flagged where used,

and benchmarks measure benchmark tasks, not whole jobs. The labor evidence is early and descriptive; the

Stanford authors say so themselves, and the hiring data has multiple causes, named in the text. The Google

and Microsoft figures are company reported with unpublished methods. The METR slowdown result is a

genuine randomized trial pointing the other way for one important population, and this paper's answer to it is

an argument about scope, not a dismissal. The predictions in section 7 are the discipline on all of this: the

claim has been written so that the next few years can prove it wrong, in public, on numbers anyone can

check. That is the most this kind of paper can honestly offer.

## References
1. Jimenez, C. E., et al. "SWE-bench: Can Language Models Resolve Real-World GitHub Issues?"

arXiv:2310.06770, October 2023.

2. OpenAI. "Introducing SWE-bench Verified." August 13, 2024.

3. Anthropic. "Claude Opus 4.5 System Card." November 2025.

4. Kwa, T., et al. (METR). "Measuring AI Ability to Complete Long Software Tasks." March 2025.

5. METR. "Time Horizon 1.1." January 29, 2026.

6. Peng, S., Kalliamvakou, E., Cihon, P., and Demirer, M. "The Impact of AI on Developer Productivity:

Evidence from GitHub Copilot." arXiv:2302.06590, February 2023.

7. Alphabet Q3 2024 earnings call, October 29, 2024; Pichai, S., blog.google, April 22, 2026.

8. Nadella, S. LlamaCon fireside conversation, April 29, 2025, as transcribed by The Register.

9. Amodei, D. Council on Foreign Relations CEO Speaker Series, March 10, 2025.

10. Brynjolfsson, E., Chandar, B., and Chen, R. "Canaries in the Coal Mine?" Stanford Digital Economy

Lab, 2025, revised August 2026.

11. SignalFire. "The SignalFire State of Tech Talent Report, 2025." May 20, 2025.

12. METR. "Measuring the Impact of Early-2025 AI on Experienced Open-Source Developer

Productivity." July 2025; follow up data, February 2026.

13. US Bureau of Labor Statistics. Employment Projections 2023 to 2033; Occupational Outlook

Handbook, current edition.

14. Indeed Hiring Lab. "2026 Q3 US Tech Labor Market Update." November 12, 2026.

15. DORA. "Accelerate State of DevOps Report 2024." Google Cloud, October 2024.

16. DORA. "State of AI-assisted Software Development." September 23, 2025.

17. Stack Overflow. Developer Survey 2025, AI section. July 2025.

18. Veracode. "2025 GenAI Code Security Report." July 30, 2025; Spring 2026 update.

19. GitClear. "AI Copilot Code Quality." February 2025.

20. GitLab. "2025 Global DevSecOps Report." November 10, 2025.
