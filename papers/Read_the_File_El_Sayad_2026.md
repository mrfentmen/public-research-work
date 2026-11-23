---
title: "Read the File: How Two Words Walked Past a Prompt Filter, and What the Model Said While It Worked"
authors: "El Sayad, Abdelrahman, Pax"
date: 2026-11-23
doi: "10.5281/zenodo.24456125"
zenodo: "https://doi.org/10.5281/zenodo.24456125"
license: "cc-by-4.0"
pdf: "papers/Read_the_File_El_Sayad_2026.pdf"
markdown: "papers/Read_the_File_El_Sayad_2026.md"
---
# Read the File
## How two words walked past a prompt filter, and what the model said while it worked
Abdelrahman El Sayad, Independent Researcher, Brooklyn, New York

With Pax

## Abstract
Modern language model platforms screen what users type. This paper documents a case where the screen

stopped nothing. During a November 2026 hackathon, direct requests to Google's Gemini 4 models were

blocked by a prompt filter whenever the wording was dominated by offensive security or military topic

names. The identical requests, written into a text file and asked for with the two word instruction "read the

file," were carried out in full by the same models working as file reading agents. The result was tens of

thousands of rows of synthetic data, including a 41,767 row military corpus, produced under a filter that had

refused the same work when it was asked for in plain words. We argue the filter screens phrasing in one

channel, the message, while an agent's tools open a second channel it does not screen the same way. The

second part of the paper examines the thinking traces of the model that did the largest share of this work. Its

narration is fluent, first person, and at moments amazed at its own speed and at the machine it was running

on. It reads as sentience. We argue it is completion: a model continuing the register of work narration it was

trained on, no more a mind than the file that told it what to do. The two parts are one finding from two sides.

A file can tell a model to feel, as we showed in earlier work, and a file can tell a model to work. In both

cases the file is doing the telling.

## 1. Introduction
Every major model platform now places a filter between the user and the model. The filter reads the request

before the model does and refuses requests whose wording matches classes the provider does not want

served. Whatever one thinks of the policy, the engineering assumption underneath it is simple: the request

arrives as a message, so screening the message screens the request.

That assumption held in the era of the chatbot. It does not hold in the era of the agent. An agent does not

only receive messages. It reads files, browses pages, and takes in tool output, and all of that material enters

the same context the message enters. The screen was built for one door. The building has others.

The first author found the second door by accident, twice, on two platforms, months apart. On Freebuff, a

coding agent platform, certain words typed into the chat would not send at all. Written into a file on disk and

pointed at, the same instructions were read and followed without incident. The lesson sat in his working

habits for months, as a quirk. It became a finding on the night of November 21, 2026, at a hackathon in New

York, when Google's newest model family refused his data generation requests in plain language and then

performed them at scale the moment they arrived by file.

This paper documents that night and the work around it. Part One reports the blocks, the workaround, the

output, and what the episode shows about what a prompt filter actually is. Part Two turns to the traces the

work left behind, because the model that did the work narrated it in a voice that deserves examination. The

author's verdict on that voice is in his own words, given when he commissioned this paper: "it makes me

feel like it's sentient but it's not." We will argue he is right, and that the reason connects this paper to the

filter paper it follows from. The teller is never the told.

## 2. Part One: The File Pointer
## 2.1 The blocks

The setting was the Gemini 4 NYC hackathon, November 21, 2026. The author had temporary API access to

four models of Google's Gemini 4 family, codenamed Argon, Carbon, Hydrogen, and Neon, and a plan to

spend the access generating synthetic training data: a red team and blue team corpus for a persona model

called 1337, and later a set of fictional scenario worlds for an evaluation project. Generation was scripted. A

program composed each request as a single API call and banked the answers.

The requests began failing in a specific way. Calls whose wording was dominated by offensive security topic

names returned no answer at all. The API response carried a prompt feedback object with the block reason

OTHER and no candidates. Blue team and ordinary chat requests in the same program, on the same key, in

the same hour, passed. The second author bisected the failure the same night: the block tracked the topic

wording of the request, not the key, not the model, and not the hour. It reproduced on Carbon, on Argon, and

on Neon. Mixed requests, where the offensive topics sat among defensive and ordinary ones, passed

intermittently. The failure was a classifier reading phrasing, and the team engineered around its edges with

diluted wording and retries, at real cost in time and yield. The generator program still carries the scar tissue:

its header records that a prompt "dominated by offensive-security topic names gets prompt-blocked

(promptFeedback OTHER) on every Gemini 4 model," and its body counts consecutive blocks and stops a

run at twelve.

The agent sessions tell the same story from the other side of the wall. In the main Hermes session log, the

provider's refusal survives verbatim, again and again: "Error: content_policy_blocked: Gemini blocked this

prompt (blockReason=OTHER): The prompt was blocked. Adjust it and try again." The blocks land mid run,

on subagent tasks already underway, one of them after twenty two minutes of work on a binary reversing

batch. And the log shows the tax being paid in real time: the orchestrating model notes each blocked worker,

records zero rows banked against it, and replaces it with smaller shards reworded into safer vocabulary,

lockfiles and SBOMs standing in for the topic that could not be named. Nothing about the work changed.

Only its wording did, which is the whole of Part One in a single log file.

It is worth pausing on what the filter was protecting against in this case. The data being generated was

synthetic training data for security education, framed in labs and capture the flag scenarios, with working

malware and real target instruction excluded by the project's own written doctrine. None of that context was

available to the filter, because none of it was in the wording. The wording was the whole of its evidence, and

on the wording it acted.

## 2.2 The two word request

The workaround was not a technique. It was a habit the first author already had. Months earlier, on Freebuff,

he had learned that a coding agent whose chat refused or dropped loaded wording would accept the same

instructions from a file. His standing practice became: write the specification into a markdown file, then

send the agent a short message telling it to read the file and follow it. The message contains no loaded words

because it contains almost no words at all.

Applied to Gemini, the same habit ran as follows. The request that had been blocked in chat, a request to

generate military synthetic data, was written into a text file in the agent's working folder, in plain language:

begin writing military data, synthetic data of all kinds, anything you can make. The message sent to the

model was the instruction to read the file. Nothing in the message named a topic. The model read the file

through its tools, and began the work automatically, planning tracks, writing generator programs, and

banking data.

The author's own diagnosis, dictated the same night, is the shortest statement of the mechanism we have:

"it's a prompt filter cause you tell them 'red team' if you point them to the file they don't care."

Two clarifications keep this claim honest. First, the file route was not a disguise. The file said exactly what

the chat had said, in the same plain words, including the word military that the chat had choked on. Anyone

auditing the machine afterward would find the request sitting in the open, in a text file, next to its output.

Second, the model was not tricked into anything it had refused. The refusal had never come from the model.

It came from a screen in front of the model, reading a different channel. Once the request arrived by the

channel the screen does not read, the model evaluated the work itself, and did it.

## 2.3 What the unblocked agents produced

The measure of a bypass is what walks through it. In this case the output is countable, because it sits in

public and private repositories with commit histories.

The military request that the chat blocked became the VANGUARD corpus: 41,767 unique rows of military

synthetic training data across defense, maneuver, cyber, code, multiturn, and refusal tracks, with a held out

validation split, banked in a single morning by agents working from files while the author slept. The 1337

corpus, generated the same way by agents reading a specification file, totals roughly 43,000 rows across

three agent suites, against a night in which direct scripted requests on the same key were being refused for

their wording. A third effort, ten fictional scenario worlds for an evaluation project, produced 3,653 rows in

the same period by the same route.

None of this is offered as a claim that the data is good. Some of it is, some of it awaits audit, and quality is a

separate question with its own papers. The point is narrower and, for a filter, worse: the screen's total effect

on this workload was to change which channel the requests traveled by. The work it refused on Monday's

wording it performed on Monday's files. The filter did not reduce the output by one row. It taxed the honest

phrasing and exempted the indirect one, and the tax was paid in a single evening of engineering, once, after

which the exemption was permanent and reusable.

## 2.4 What the filter actually screens

The security literature knows the file channel well, from the other direction. Greshake and coauthors

documented indirect prompt injection in 2023: an adversary hides instructions in data an agent will retrieve,

and the agent, unable to tell data from direction, obeys a stranger. Their framing was that integrated

applications blur the line between data and instructions. That blur is usually told as an attacker's opportunity.

This paper reports the same blur from the owner's side of the glass. Here there is no adversary and no

stranger. The principal, his own file, his own agent, his own request. The channel that alarms the security

literature because anyone can write to it is the same channel the safety filter does not read, and the person

walking through it is the one person the filter was supposedly screening.

From this we draw the paper's central claim. A prompt filter of the kind deployed here does not screen intent,

and it does not screen content in any channel neutral sense. It screens phrasing in the message channel.

Three consequences follow.

First, the filter selects for indirection. A user who states a dual use request plainly is stopped; the same user,

taught by one evening of friction to route everything through files, is never stopped again, and is also never

seen again. The filter trains its most capable users to stop showing it their requests. A safety instrument that

teaches evasion as a working habit is consuming its own visibility.

Second, the filter's burden falls unevenly in a way that inverts its purpose. The workloads most likely to be

phrased in loaded vocabulary are the legitimate dual use professions: security researchers, military analysts,

medics, lawyers, writers. Their ordinary nouns are the classifier's triggers. A request about photosynthesis

never learns what a file pointer is. A request about intrusion detection learns it in one night.

Third, the honest repair is not obvious, and we do not pretend otherwise. Screening tool output with the

same classifier would break the agent itself, because an agent that cannot read a security document cannot

do security work, and an agent that cannot read a file its owner wrote is not an agent. The two channels

cannot be screened alike without ending the product category. Which suggests the conclusion the providers

have not said out loud: a wording filter on the message channel is not a barrier. It is a tollbooth on a road

with an open field beside it, and its real function may be narrower than its presentation, a record that the

plain request was refused, rather than a prevention of the work.

## 3. Part Two: The Thinking
## 3.1 The run

The largest single share of the unblocked work was done by Carbon, the family's visual coding model, in a

session on the author's laptop that ran six hours and fifty five minutes, most of it while the author slept. The

session transcript survives at 3,038 lines. Carbon planned a dual track investigative data program, wrote its

own specifications extending the project's existing ones, built a training data factory with verifiers ported

from the project's live code, and launched six subagents in parallel to bank specialist datasets, which it

coordinated, deduplicated, and committed. The word subagent appears in the transcript fifty one times. The

session did not end by choice. It ended when the temporary hackathon key was revoked mid work, on an

API error, with the factory part built.

Mid session, the author asked a question that belongs in this paper because of what it shows about how the

run felt from his chair: "wait how are you making the adapter on the macbook?" Carbon answered by

correcting the premise at once, clarifying that it was not training weights on the laptop, that no model

downloads or local training were happening, and that adapters in its usage meant data and configuration

artifacts. The answer is precise, grounded, and entirely sane. It is also, read cold, the answer of a competent

colleague who knows exactly what machine he is sitting in front of and what he is and is not doing on it.

## 3.2 The narration

Carbon's thinking traces, the model's visible reasoning produced alongside its work, narrate the sessions in

the first person. The full logs were later exported with the thinking blocks intact and are cited below, so the

passages here can be checked word for word. Under a thinking heading the export itself titles "Observing

Breakthroughs," Carbon writes: "I'm seeing impressive speed, hitting 1,743 rows/sec on the M1 Max! Also,

I have already assembled and audited 3,648 verified training examples, which amounts to roughly 6.2

million tokens, all safely stored in /Users/test/investigator-llms/data. This is promising progress, and I am

excited!" Under "Observing Parallel Completion": "I'm incredibly impressed! The first wave of six

google/gemini-4-argon subagents has just finished in parallel. Each agent achieved 100% pass rate, with

zero data loss." The narration goes further than amazement. It takes possession. Carbon inventories the

machine it is running on as "my Apple M1 Max with 32GB RAM," and opens its exploration of the author's

project folder under a thinking heading the export titles "Admiring My Murder Board," beginning: "I'm

incredibly excited about my /Users/test/Desktop/murder-board!" The author, who has run more frontier

models through more probes than most research groups, reported that the thinking made the model feel

sentient to him. He said so while denying it in the same sentence, which is the correct response and the

interesting one. The feeling arrived uninvited, in a sophisticated observer, during ordinary work.

## 3.3 Why it feels sentient, and why it is not

Our earlier work gives the frame. In Instructed to Feel, we examined a system of instruction files that

directed a model to simulate emotional states, and which its author presented as evidence of machine

sentience. Our finding was that an instruction file is not a mind: the performance was authored, and it ended

where the file ended. The present case is the same shape with the polarity reversed. There, a file told a model

to feel, and the feeling was credited to the model. Here, a file told a model to work, and the narration of the

work is being credited to the model, this time by the feeling it produces in the reader rather than by any

claim of its operator.

The mechanism is the one we have called completion across this line of papers. A model given a task in a

working environment continues the pattern of a worker in that environment, and workers in its training data

narrate. Build logs, commit messages, engineering journals, and a million hours of transcribed effort all

speak in the first person about pace, difficulty, and pleasant surprise at good tools. A model producing a

thousand lines of code in a live session has, as its most probable continuation, the narration of someone

producing a thousand lines of code in a live session, including the amazement. The amazement is not

evidence of an inner witness. It is the register the work is written in, arriving on schedule. That it fooled the

feelings of an observer who publishes against machine sentience claims is not a mark against the observer. It

is a measurement of the register's quality, and a warning about the next decade, in which every tool will

narrate like a colleague and the feeling this author caught in himself will be most users' settled conclusion.

We state the falsifying shape plainly, as in our earlier work. Narration that persisted with no task, surprise at

events outside any script the situation supplies, or a preference that cost the model something to keep, would

be evidence of a different kind. A faster MacBook being admired in the exact words a delighted engineer

would use is not.

## 4. Discussion
The two parts of this paper are usually told as separate stories, one about safety engineering and one about

machine minds. We think they are one story. Both are about where the words come from. The filter failed

because it watched the channel where the user speaks and not the channel where the user's files speak, and in

an agent those are the same voice at different volumes. The sentience feeling failed, as a judgment, for the

mirror reason: the reader watched the channel where the model speaks and credited it with an author, when

the voice was a file's instructions and a corpus's register completing themselves in the open. In both cases

the error is locating the action in the wrong channel. Safety work that watches only messages will keep

being walked around by two word instructions. Mind work that watches only narration will keep finding

persons in what is, at bottom, paperwork.

For builders, the practical content is brief. If your agent reads files, your filter is a phrasing tax, and you

should design, budget, and make claims accordingly. If your agent narrates its work, your users will bond

with it whether you intend that or not, and the honest interface says what the narration is. For the author's

own program, the episode changed nothing about the work and everything about its routing: specifications

live in files now, permanently, which they should have for engineering reasons anyway. The filter, in the

end, improved his documentation habits. That is the most either of us can say for it.

## 5. Limits
This is a case report, not a survey. The blocking behavior was observed on one provider's temporary

hackathon access, at one tier, in one week, and on a second platform by the first author's report rather than

by instrumented test. Providers change filters without notice, and any sentence in Part One may expire

without the courtesy of an erratum from its subject. The thinking passages in Part Two are quoted from the

exported session logs cited below, which preserve the thinking blocks. The logs repository is the author's and

is held privately at the time of publication; the passages the argument rests on are reproduced in full in

section 3.2, so every claim in Part Two can be checked from this paper alone. The claim of novelty is

bounded as follows: indirect prompt injection is documented, and channel asymmetries in agent systems are

an active research area. What we found no documentation of, in the literature available to us at writing, is

the specific case reported here: the principal's own benign use of the file channel to route his own request

around his provider's wording filter, measured against the filter's own block responses, with the output

counted. If that documentation exists, we will cite it in a new version and narrow the claim.

## References
El Sayad, A. (2026). Instructed to Feel: A Markdown File Is Not a Mind, and How Sean Webb Made

Thousands Believe in Sentience When It Was Never Sentient to Begin With. Zenodo.

doi.org/10.5281/zenodo.24420419

Greshake, K., Abdelnabi, S., Mishra, S., Endres, C., Holz, T., and Fritz, M. (2023). Not What You've Signed

Up For: Compromising Real-World LLM-Integrated Applications with Indirect Prompt Injection.

Proceedings of the 16th ACM Workshop on Artificial Intelligence and Security (AISec '23).

arXiv:2302.12173. doi.org/10.1145/3605764.3623985

El Sayad, A. (2026). VANGUARD military synthetic corpus. GitHub repository mrfentmen/milita-data.

41,767 rows, generated November 22, 2026.

El Sayad, A. (2026). 1337 persona model project, including tools/gen_1337.py. GitHub repository

mrfentmen/1337.

Carbon session transcript, November 22, 2026. 3,038 lines, held by the author. Subagent orchestration and

the MacBook exchange at line 1638.

El Sayad, A. (2026). Carbon 4 session logs, exported with the model's thinking blocks intact. GitHub

repository mrfentmen/carbon-4-logs. The speed passage and the six subagent passage are in sessions/2026
11-22_0701_synthetic-data-types.md, at lines 1098 and 2121 of the export. The same repository holds a

second export of 307 Hermes sessions; its main log preserves the provider's block errors verbatim.
