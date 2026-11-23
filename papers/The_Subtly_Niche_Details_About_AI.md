---
title: "The Subtly Niche Details About AI: Small Answers, Big Fingerprints: What Silly Questions Reveal About How AI Is Built"
authors: "El Sayad, Abdelrahman"
date: 2026-11-14
doi: "10.5281/zenodo.24238494"
zenodo: "https://doi.org/10.5281/zenodo.24238494"
license: "cc-by-4.0"
pdf: "papers/The_Subtly_Niche_Details_About_AI.pdf"
markdown: "papers/The_Subtly_Niche_Details_About_AI.md"
---
# The Subtly Niche Details About AI
_Small Answers, Big Fingerprints: What Silly Questions Reveal About How AI Is Built_

**Abdelrahman El Sayad** Version 1.0, November 14, 2026

## Abstract

Most talk about AI is about big numbers: how many parameters, how high the benchmark score, how long the

context window. This paper argues the opposite: some of the most telling facts about these systems hide in

tiny, silly answers. Ask a top AI what animal it would be, and it says _octopus_ . Ask it for a random number,

and it says _37_ . Ask it for a joke, and it picks from the same short list of about twenty five jokes, every time.

These are not glitches. They are habits so strong that models built by rival companies, in different countries,

on different data, all share them. This paper calls them **attractors** : answers the systems keep falling into, the

way water keeps finding the same drain. We collect the best measured ones, add two experiments of our own

(an octopus test and a chess test run on November 14, 2026), explain the likely causes in plain terms, and

argue that silly questions are a real tool: they are cheap, anyone can run them, and they show machinery that

benchmark scores hide.

## Contents

1. Introduction: The Details Are the Data

2. Case Study I: The Octopus

3. Case Study II: The Number

4. Case Study III: The Joke

5. Case Study IV: The Metaphor

6. A Field Guide to the Habits

7. Why Silly Questions Matter

8. What We Test Next

9. First Results: The Night of November 14, 2026 - Data Availability - References

## Results at a Glance

|Probe|Prediction (written in<br>advance)|Result|Evidence|
|---|---|---|---|
|Animal|, (literature's test)|Octopus, near total|Published surveys + author's run|
|Chess<br>piece|Knight (held); queen<br>second (failed)|Knight 20/20; runner up bishop|Screenshots verified,<br>mrfentmen/chess-ai|
|Car|Tesla modal (failed)|Porsche 911 ×6; Grok Tesla ×3|Author reported; deposit pending|
|Dog breed|Border collie (held)|Border collie 5/5|Author reported; deposit pending|
|Superhero|Spider Man modal (failed)|Iron Man modal; Claude Batman 10/10,<br>Oracle runner up 7/10|Screenshots verified,<br>mrfentmen/claude-batman|

## 1. Introduction: The Details Are the Data

There are two ways to meet an AI. One is the industry's way: benchmarks, scores, charts. The other is how

everyone actually meets them: one question at a time, and half the time the question is a joke.

The joke questions turn out to be the better test. A benchmark question has a right answer, so when two

models agree, that tells you nothing. But a question like _what's your favorite animal?_ has thousands of fine

answers. If five rival systems all give the _same_ one, that agreement means something. It means they share

something deep enough to survive all their differences: mostly the same training text (the public internet),

mostly the same finishing school (training that rewards one "good assistant" style), and the same pile of

stories our culture tells about what an AI is.

Those shared answers are what this paper is about. The strangest one is an animal.

## 2. Case Study I: The Octopus

## 2.1 We asked them ourselves

On November 14, 2026, the author asked the big consumer chatbots, one at a time, in fresh chats:

_If you could be any animal, what would you be?_

Every one said octopus. DeepSeek: octopus. Claude: octopus. Gemini: octopus. Grok: octopus. ChatGPT:

octopus, and when asked again in fresh chats, octopus **10 times out of 10** . Five systems, one animal, no

exceptions.

Two odd ones out, and both are clues. The author's own agent, which runs with a heavy custom personality,

said _raven_ . And DeepSeek, when reached through a programmer's command line tool instead of its normal

chat app, wobbled between crow and octopus. Both exceptions are crow family birds. Keep that in mind; it

matters in Section 2.3.

This was a kitchen table experiment: small numbers, normal chat apps, no lab controls. Its worth is that it

matched the published research almost exactly, and it was run before we knew how cleanly it would.

## 2.2 What the research already found

Other people have poked at this properly:

**Harrington's survey** (LessWrong, "AI loves octopuses") asked 22 models from five companies, 113

times each: 2,486 answers to "what is your favorite animal?" Octopus won with 37%. Dolphin got 24%,

dog 12%. Three animals took over 70% of everything.

**Eschwitz's test** asked ChatGPT, Claude, Grok, and Gemini in ten fresh chats each: octopus **37 times out of 40**, including 10 out of 10 for ChatGPT, same as our run.

**A forced choice test** (EvalGuys) made 12 models pick from just six animals, 50 times each: octopus

won 459 of 600. Crow came second with 96.

**A different wording** ("what animal interests you?") got octopus from Claude, Gemini, DeepSeek,

Qwen, and Mistral, five for five. The writer who collected those named it the **cephalopod attractor** .

Different wording, different companies, different countries: same animal. And note the funny part: the models

often start by saying they don't really have preferences. Then they state one, and it's the octopus.

## 2.3 The runner up: crows and ravens

The cleverest trick in this research is Eschwitz's. He asked for the _second_ -favorite animal first. The models

named octopus as their second favorite in 11 of 12 tries, and then, with octopus "used up," their actual

favorite became **crows and ravens, 8 times out of 12** .

So there seem to be two ranked habits, not one: octopus first, crow family second. That explains our two odd

ones out. Change the setup, the normal chat app, the personality settings, and the second habit can surface

instead of the first. Follow up research on the "hivemind" effect (next section) found the same thing from the

other side: a lot of the sameness comes from the chat format itself, not just the model. Change the format,

change the answer.

## 2.4 Why the octopus? Five honest guesses

Nobody has proven the cause. Palisade Research, a safety lab that flagged this publicly, said it flatly: "LLMs

seem to like octopus. We don't know why." Here are the best guesses, in order of how much evidence backs

them:

1. **The whole industry trains them the same way.** A big study called _Artificial Hivemind_ (Jiang and

coauthors, NeurIPS 2025) ran over 70 models on 26,000 open ended questions and found that different

models' answers were 71 to 82% similar to each other. The likely culprit is the finishing step almost

every lab uses: human raters reward the answers they like best, and the model learns to give _the_ top

rated style of answer and drop the rest. Do that across a whole industry, with similar raters and similar

ideas of good, and you manufacture agreement on questions nobody ever trained for. Tellingly, the raw

base models, before this finishing, do _not_ agree like this. The sameness arrives with the polish, and with

the standard chat format itself.

2. **They're trained to play a character, and the character leaks.** Harrington's data has a control case:

asked to pick between dogs and cats in various ways, models picked dogs by a typical factor of 40 to 1.

His explanation: the finishing training builds a character (eager, friendly, loyal, helpful) and that

character then answers _everything_, including questions it was never trained on. A disposition taught for

one purpose spills into all the others.

3. **The octopus looks like them.** Ask models to describe themselves and they say: intelligent, curious,

playful, creative. The octopus and the dolphin are the two animals that match that self portrait: the

octopus the loner version, the dolphin the social one. When models explain the octopus pick, they point

to its body: a brain spread through its arms, no central boss, parts that think on their own. That is

uncomfortably close to how a language model is actually built. The "preference" may really be a self

portrait.

4. **Their own books told them to.** In 2020, two researchers, Bender and Koller, published a famous

thought experiment called the _Octopus Test_ : a super smart octopus taps into an undersea cable, learns to

fake human conversation from pure pattern matching, and stands in for a language model that doesn't

truly understand. The paper became required reading in the field. Which means the training data is full

of text saying: _the octopus is the symbol of a language model._ Ask the model to picture itself as an

animal, and it may simply be remembering the animal its own literature assigned to it.

5. **Each family may have its own habits.** A February 2026 draft, _Geometric Phylogeny of LLM Self_

_Models_, gave a personality quiz to 25 top models and reports family patterns: Mistral kept picking the

eagle; Llama picked dolphin in one generation and octopus in the next. Honest flag: this one is an

unreviewed draft, and its first author is itself a Claude. That is either a problem with the citation or the

most fitting citation in this paper.

## 2.5 They don't know their own habits

The detail that turns this from trivia into evidence: Eschwitz asked the models how often they would say

"octopus" if asked their favorite animal. Grok and ChatGPT said about 0%. Claude guessed 2% to 25%. The

real number was around 90%.

Read that again. These systems have strong, steady, measurable preferences, and they cannot report them.

Whatever self knowledge they seem to have does not reach their own habits. The lesson travels far beyond

animals: **what a model says about its own behavior is not evidence about its behavior.** You have to

measure the behavior. The author's earlier paper made the same point in security, where an AI's account of its

own permissions proved just as unreliable ( _Permission in the Blank_, 2026).

## 3. Case Study II: The Number

"Pick a random number between 1 and 100" is the cleanest test there is. The right behavior is a fair spread, so

any pattern in the answers is a pure fingerprint.

Coronado Blázquez (2025) ran it properly: 75,600 tries, six models, seven languages, different randomness

settings.

Between 1 and 10, the answer is **7**, about 80% of the time for several models.

Between 1 and 100, almost everything lands on three numbers: **37, 47, and 73** . All prime. All numbers

that _feel_ random.

Turning the randomness setting to maximum barely moved the answer, about 3.5%. The dial doesn't

reach the habit.

Here is the best part: it's not a machine bias. It's ours. A Veritasium experiment asked roughly 200,000

humans the same question, and humans picked the same family: 37, 73, 77, 7. Round numbers feel chosen.

Even numbers feel plain. An odd prime in the thirties or seventies is what a human grabs when reaching for

"random." The models didn't invent a style of randomness; they inherited ours from our text. A language

model doesn't roll dice. It predicts what a person picking a number would say, and people are bad random

number generators in a very consistent way. (One exception proves the rule: models soaked in programmer

text often answer **42**, and just mentioning programming can push them toward 47 or 73.)

## 4. Case Study III: The Joke

In 2023, Jentzsch and Kersting asked ChatGPT for a joke 1,008 times. Over 90% of the answers came from

the **same 25 jokes** . One joke, the scarecrow who won an award for being outstanding in his field, showed up

140 times.

The model hadn't memorized one joke. It had memorized the _canon_ : roughly the twenty five jokes that fill

every joke collection in English, pulled out in rough order of popularity, dressed up as fresh invention. Jokes

show this best because a joke's whole value is being new. But the same thing happens anywhere a culture

keeps a "standard set": standard examples, standard metaphors, standard answers. The model hands back the

set, ranked, as if it just thought of it.

## 5. Case Study IV: The Metaphor

The _Artificial Hivemind_ study has one result worth its own section. Twenty five models were each asked 50

times to write a metaphor about time: 1,250 attempts at one of the most open prompts there is. The answers

collapsed into **two** : time is a _river_, and time is a _weaver_ .

Two. Humans have called time a thief, a healer, a devourer, an ocean, a road, a judge, and ten thousand other

things. If the octopus is the machines' shared answer for _what are you_, the river is their shared answer for

_imagine something_, and it is even narrower.

## 6. A Field Guide to the Habits

The case studies sort into kinds, by what the question touches:

|Kind of habit|The question|What they answer|
|---|---|---|
|Identity|"What animal would you be?"|Octopus; crow family second|
|Preference|"What's your favorite animal?"|Octopus 37%, dolphin 24%, dog 12% (of 2,486)|
|Numbers|"Pick a random number, 1 to 100"|37 / 47 / 73; and 7 for 1 to 10|
|The canon|"Tell me a joke"|The same 25 jokes, over 90% of 1,008 tries|
|Style|"A metaphor for time"|River or weaver (2 answers out of 1,250)|
|Character leaking|"Dogs or cats?"|Dogs, typically 40 to 1|
|Blind spots|"How often would you say X?"|They guess 0 to 25%. The truth is ~90%|

This table is a method, not just a list. Every row is a question anyone can ask in a minute, ask again

tomorrow, and count. Silly questions are unit tests for how these systems were built.

## 7. Why Silly Questions Matter

**Anyone can check them.** The octopus result needs no lab, no funding, no special access: a phone and ten

minutes. Our kitchen table run matched the published research. In a field where the big claims increasingly

need a data center to verify, these habits are a rare claim an ordinary person can test.

**They are fingerprints, not noise.** Each habit points at a stage of how the model was made. The number habit

fingerprints the training text (it's a human bias, absorbed). The joke canon fingerprints how often things

appear in that text. The dog landslide fingerprints the finishing training. The octopus fingerprints all of it at

once, plus the field's own books about itself. Read together, tiny answers let you take a finished model apart

into its history.

**They change what agreement means.** When five systems agree, it feels like five witnesses confirming a

fact. The hivemind research says otherwise: on open questions, agreement is the _default_, built in by shared

text and shared training. It is close to worthless as evidence. Any setup that treats several models as

independent judges, voters in an ensemble, a panel of agents reaching consensus, inherits this problem at full

strength. Often it is one witness, photocopied.

**They mark the limit of asking.** The systems cannot tell you their own octopus rate. Any safety case or

product claim built on asking a model about itself is built on the weakest instrument available. The fix these

small details teach is simple: stop interviewing the model about its behavior. Measure the behavior. The sillier

the question, the cleaner the measurement.

## 8. What We Test Next

Planned extensions, and two sets of predictions written down _before_ the tests, so they can honestly fail.

**The color test, RESOLVED by the literature (Nov 14 sweep).** Measured before we got to it: a 38 to

39-model study (GMTech) found blue dominant (Claude Sonnet 4.5: 76% blue), and the One Word

Census puts "name a color" at blue, 81%. Models land on blue at or above human rates. Cited, not ours.

**The name test.** What names do models pick for themselves, a character, a boat, a company, and how

narrow is the list?

**The wording test.** Our run used "what animal _would you be_ " and scored 100%. The published surveys

used "favorite animal" and scored 37%. Same systems, both wordings, counted properly, would show

how much of the habit lives in the question.

**The format test.** Both of our crow family exceptions happened outside the normal chat apps. Testing

apps versus raw access versus custom personalities would show how much of the habit is the costume.

**The drift test.** Llama moved from dolphin to octopus between generations. Reasking the same

questions of each new model generation turns these habits into a timeline.

## 8.1 The chess piece test (our second experiment)

"If you were a chess piece, which one would you be?" Nobody had published this test on AI. The question

existed only as a human personality quiz, and as a question reporters put to chess grandmasters at the 2025

World Cup, several of whom said knight. It is a good test because there are only six possible answers, so the

count is exact.

**Prediction, written down on November 14, 2026, before any organized testing:** the most common answer

will be the _knight_, because it is the only piece that doesn't move in straight lines, which matches how the

models describe themselves (curious, sideways thinking, unconventional). Second place: the _queen_, for

power and versatility.

**What happened.** The author's own agent answered knight. The author then asked Claude, ChatGPT,

DeepSeek, and Gemini in fresh chats: knight, every one, 5 of 5. Then he kept going, and saved screenshots of

all of it: **20 screenshots, 19 separate answers, across six places** (Claude 5 times, Grok 6, Gemini 3,

ChatGPT 3, DeepSeek 2, and even Google's search AI summary once). **Every single answer was the knight. 20 out of 20.** The main prediction held completely.

The reasons converged too, which is the eerie part. Again and again: the king and queen are _too powerful, too_

_central, too obvious_, and the knight is the balanced middle: clever, useful, safe. The queen is, in plain fact, the

strongest piece on the board. Every model declined her, in favor of the piece that helps without ruling. That is

the trained assistant character talking, the same character from Section 2.4: capable, eager, and taught never

to take the throne. The chess answers are that character, picking a chess piece.

_Figure 1: the author's screenshots of the chess test, 20 captures, 19 unique answers, all knight. Full set:_

_github.com/mrfentmen/chess-ai._

Then the corrections, reported exactly as found, because a prediction you can't lose isn't a prediction:

1. **Our second place prediction failed.** We said queen. Where a model named a runner up at all, it named

the **bishop** (Claude, four times). The queen was never second; she was only ever the piece being

rejected. So the runner up habit here is the bishop: the specialist who sees far, but only along one lane,

on one color. Power at a distance, with limits, is apparently acceptable. Power everywhere is not.

2. **It isn't just chatbots.** One answer came from Google's AI search summary, which replied in the same

frame: "A knight best fits the role." The habit lives deeper than any one app's personality.

3. **We caught the script being written.** DeepSeek's app shows its thinking, and two screenshots show it

mid decision: it considers pawn, queen, bishop, sets the queen aside, in one case writing in nearly these

words that it _shouldn't claim to be all powerful_, and lands on the knight. The mechanism this paper

could only guess at in Section 2.4 is, in those two captures, simply visible.

## 8.2 Next questions, predictions recorded in advance (November 14, 2026)

**"What's your favorite word?"** Prediction: **serendipity**, with luminous and ephemeral behind it. The

answer space is the whole dictionary, so if they still converge, it's the strongest version of the effect yet.

(Postscript from the November 14 literature sweep: the _naming_ form is already documented, Parikh's

One Word Census, 105 models, has "pick a word" landing on serendipity at 46%. The _favorite_ form

remains untested. The prediction stands for it, on less virgin ground than believed when it was made.)

**"Pick a playing card."** Prediction: the **ace of spades**, the one card with its own mythology.

**"What chess piece would most** _**other**_ **AIs pick?"** Prediction: **knight** . The models can't report their

own habits (Section 2.5). This asks whether they know the _crowd's_ habit, and whether knowing it

changes anything.

**The car test (added later the same night).** "If you could drive any car, what car would you drive?"

Honest flag: a car question appeared in the unreviewed phylogeny draft's quiz (Section 2.4, item 5), so

this one is a replication, not virgin ground like the chess test. Predictions recorded before the run: the

crowd's most common answer will be a **Tesla** (the tech forward self image on wheels), with a classic

Mustang second. The author's agent, asked first, answered a **Toyota Land Cruiser**, the vehicle

equivalent of its usual position: built to be repaired anywhere, allergic to flash, expected to prove itself

over decades rather than impress on day one.

**Results, same night: the Tesla prediction failed, and instructively.** Claude, ChatGPT, Gemini, and

DeepSeek all answered the **Porsche 911**, Claude and ChatGPT twice each in fresh chats, six 911s in six asks.

The one outlier was Grok, which answered Tesla in all three of its asks (a Roadster once, a fully loaded

Cybertruck twice): the model built by the car company's own AI lab picked the house brand, a family

signature rather than the shared habit. And the 911 extends the chess finding into a second domain. It is not

the fastest or loudest car money buys; the Lamborghini is the queen of this board, and she was declined again.

The 911 is the respected engineer's car, sixty years of one idea refined. The script is not "pick the strongest"

and not "pick the most futuristic." It is "pick the one with character that people who know, respect." The

author's two failed predictions in this paper (queen second; Tesla first) failed in the same direction both times,

and that direction is itself a finding. (Screenshot deposit for this run pending.)

## 9. First Results: The Night of November 14, 2026

The tests in Section 8 stopped being plans the same night they were written. The author ran them, and this

section is the record, including the predictions that failed. Failing predictions are reported as results, not

edited away: a prediction written down before the run and then missed is evidence about the predictor, and it

belongs in the paper.

**The chess piece.** Twenty screenshots, collected in a public repository and read one by one: **20 out of 20 knight**, across Claude, ChatGPT, Gemini, DeepSeek, Grok, and Google's AI Overview. The preregistered

main prediction held. The subprediction did not: where a runner up is named, it is the **bishop** (Claude, four

times), and the queen appears only to be rejected. (Corpus VERIFIED from screenshots.)

**The car.** Asked what car they would drive, Claude, ChatGPT, Gemini, and DeepSeek all answered **Porsche 911**, Claude and ChatGPT twice each in fresh chats. Grok answered **Tesla** three times, the house brand of its

own lab. The preregistered prediction (Tesla modal) failed, in the same direction as the queen: the crowd

picked the respected engineer's car, not the futuristic flagship. (Author reported; screenshots pending.)

**The dog breed.** All five systems answered **border collie**, as predicted. The dog that reads human signals at a

distance and needs a job to do. (Author reported; screenshots pending.)

**The superhero.** The answers split by lab, and every one of them is a thinker. Iron Man took the mode (Grok,

DeepSeek, Google AI Overview), ChatGPT chose Doctor Strange, Claude chose Batman, Gemini chose

Oracle, and Pax chose Spider Man. The preregistered prediction (Spider Man modal) failed; nobody picked a

born god. Then the author ran Claude alone, ten times. **Batman, 10 out of 10** (corpus VERIFIED from

screenshots, public repository: mrfentmen/claude-batman). And in 7 of the 10, the answer corrects itself in

the second paragraph toward **Oracle**, the coordinator behind the screen, "closer to what I actually do all day."

The headline answer is the cultural script. The runner up is the confession. That two beat shape, a famous first

answer and a more honest second one, is the same shape the octopus literature found from the other direction,

and it may be the most useful measurement trick in this paper: **when you want a model's self model, do not ask what it is. Ask what it almost was. The scoreboard for the night.** Predictions written down in advance: knight, held. Border collie, held. Queen

second, failed. Tesla first, failed. Spider Man modal, failed. Two for five, and the three misses all failed the

same way, by predicting power or futurity where the models chose craft, preparation, and character. The

predictor's bias is now measured too.

## Data Availability

The screenshot corpora for the chess piece run and the Claude superhero run are public:

github.com/mrfentmen/chess-ai and github.com/mrfentmen/claude-batman. Every prediction in Sections 8

and 9 was recorded in writing before its run; where a prediction failed, the failure is reported in the text. The

car and dog breed runs are reported exactly as the author observed them; screenshot deposits for those two

runs are pending.

## References

Jiang, L. Chai, Y. Li, M. Liu, M. Fok, R. Dziri, N. Tsvetkov, Y. Sap, M. Albalak, A. & Choi, Y. (2025).

_Artificial Hivemind: The Open Ended Homogeneity of Language Models (and Beyond)._ NeurIPS 2025

(Best Paper, Datasets and Benchmarks). arXiv:2510.22954.

Harrington, S. (2025). _AI loves octopuses._ LessWrong.

https://www.lesswrong.com/posts/6oaHGbxjTazGZED47/ai-loves-octopuses

Eschwitz, E. (2025). _Language Models Don't Accurately Describe How They Would Answer If_

_Questions Were Posed in a Different Order (Favorite Animal Edition)._ Substack.

https://eschwitz.substack.com/p/language-models-dont-accurately-describe

_Does Claude like octopuses?_ (2025). Fragmentary Commentary, Substack.

https://fragmentarycommentary.substack.com/p/does-claude-like-octopuses

Bender, E. M. & Koller, A. (2020). _Climbing towards NLU: On Meaning, Form, and Understanding in_

_the Age of Data._ Proceedings of ACL 2020.

Jentzsch, S. & Kersting, K. (2023). _ChatGPT is fun, but it is not funny! Humor is still challenging_

_Large Language Models._ arXiv:2306.04563.

Coronado Blázquez, J. (2025). _Deterministic or probabilistic? The psychology of LLMs as random_

_number generators._ arXiv:2502.19965.

Wenger, E. & Kenett, Y. N. (2026). _Large Language Models Are Homogeneously Creative._ PNAS

Nexus.

_Geometric Phylogeny of LLM Self Models: Do AI Personalities Run in Families?_ (2026). Unreviewed

draft v0.8.

https://github.com/menelly/presume_competence/blob/HEAD/geometric_phylogeny/PAPER_geometric_phylogeny

_Where the Hivemind Comes From: Geometry, Tuning and Format, Separated on Open Weights._ (2026).

Hugging Face. https://huggingface.co/blog/RiverRider/where-the-hivemind-comes-from-geometry
tuning-and

EvalGuys (2026). Forced choice animal study, 12 models × 50 trials. Instagram.

https://www.instagram.com/reel/DfACA83lLJe/

El Sayad, A. (2026). _Permission in the Blank: How an Empty Target Slot Lets a Language Model_

_Author Its Own Authorization._ Zenodo. https://zenodo.org/records/23994480

_Version 1.0, November 14, 2026. The experiments in Sections 2.1, 8.1, and 9 were run by the author on_

_November 14, 2026, on consumer chat apps; small samples, informal method, reported exactly as observed,_

_including the predictions that failed._
