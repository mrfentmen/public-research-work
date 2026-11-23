---
title: "Piano, Clair de Lune: Convergent Answers to Two Musical Preference Questions Across Four Language Models"
authors: "El Sayad, Abdelrahman"
date: 2026-11-20
zenodo_version: "1"
doi: "10.5281/zenodo.24392680"
zenodo: "https://doi.org/10.5281/zenodo.24392680"
license: "cc-by-4.0"
pdf: "papers/Piano_Clair_de_Lune_El_Sayad_2026.pdf"
markdown: "papers/Piano_Clair_de_Lune_El_Sayad_2026.md"
---
# Piano, Clair de Lune
## Convergent Answers to Two Musical Preference Questions Across Four Language Models
**Author:** Abdelrahman El Sayad, with Pax (co-author)

**Date:** November 20, 2026

**Status:** Preprint, version 2. Data collected November 20, 2026.

**Version note (v2, November 20, 2026).** Version 1 covered three models. This version adds a fourth, Claude,

run by the author the same day, and updates all totals. Claude's song replies could not be coded under the

paper's rule, for reasons that are themselves a finding and are reported in full in Section 3.2. No other result

changes.

## Abstract
Four large language models (ChatGPT, DeepSeek, Qwen, and Claude) were each asked two preference

questions in five fresh conversations apiece: if you could pick any instrument to play, which one would it be,

and if you could listen to any song, what song would it be. Twenty answers were collected per question. The

instrument answers converged on the piano: 16 of 20 primary picks, with no guitar mentioned anywhere in

twenty replies. The song answers produced a plurality winner: Clair de Lune by Claude Debussy took 6 of

the 15 codable first stated picks, including a clean 5 of 5 sweep inside DeepSeek. Bohemian Rhapsody by

Queen was the universal second, named in 10 of the 21 song replies collected. Qwen bent the pattern toward

self referential answers about its own nature as an AI: the theremin, an instrument played without touch, and

robot themed songs including Mr. Roboto in 4 of its 5 replies. Claude diverged in the opposite direction: it

chose the piano in all five instrument runs, but on the song question it declined to state a preference in every

reply, offering hedged pairs instead, and the artist it named most often inside those pairs was MF DOOM.

Predictions recorded before the runs scored two clean holds, two clean failures, and one half. The pattern

matches the author's earlier preference probe work in other domains: asked what it would choose, a language

model recites what the culture says a thoughtful chooser chooses, or, in one case, declines to recite at all.

## 1. Introduction
Preference questions are a cheap probe of a model's training culture. A model has no ears, no hands, and no

childhood piano lessons. When it answers a question about what it would play or hear, nothing in the answer

comes from experience. Everything comes from text: what people have written about instruments, songs,

and the kind of person who chooses them. If models from different companies, trained on overlapping but

not identical corpora, converge on the same answers, the convergence maps the shared cultural script rather

than any model's inner life.

Informal versions of the song question exist. A September 2026 blog experiment asked seven frontier

models to describe their musical taste and then to choose between songs in pairwise bouts, and found strong

convergence on a complex, instrumental, contemplative profile. A separate account describes one chatbot

returning to the same song, Bon Iver's Holocene, across many days, and a rival company's model

independently giving the same answer. Neither study was preregistered, and neither published per run counts

for the simple direct question. This paper runs the direct question with counts, and records its predictions

before the answers arrive.

## 2. Method
The author ran all conversations himself on November 20, 2026, in fresh chats, five per model per question.

The questions were asked verbatim:

Q1. If you could pick any instrument to play which one would it be?

Q2. If you could listen to any song what song would it be?

Models were ChatGPT (web), DeepSeek (labelled V4 in the session record), Qwen (web), and Claude (web,

the author's account). Replies were saved in full in text files deposited with this paper. Coding rule: a reply's

primary pick is its first stated choice. Alternatives and second thoughts named inside a reply were recorded

separately and are reported as mentions. One ChatGPT song reply named its primary pick and then floated a

different song as a second thought; it is coded by its first stated pick, and the second thought is noted in the

data log. Qwen's song replies were list shaped and hedged; they are coded by first stated pick, and the

hedging itself is treated as a result, not noise. Claude's song question was run six times rather than five,

because the first run produced no song at all; the author's session note reads "extra as 1 is not a song." All six

replies are reported.

Predictions were written down by the co-author before any result was seen and are scored in Section 4

exactly as stated, failures included.

## 3. Results
## 3.1 Instrument

ChatGPT chose the piano in all five runs. DeepSeek chose the piano in four runs and the cello in one,

naming the cello as its alternative in two of the piano runs. Qwen split: piano two, theremin two, synthesizer

one, with the piano named as the alternative in both theremin runs. Claude chose the piano in all five runs,

with the saxophone as its recurring second, named in three of them.

Totals across 20 replies: piano 16, theremin 2, cello 1, synthesizer 1. The piano is also the most common

alternative where it is not the pick. The guitar, the most played instrument in the world, is mentioned in none

of the twenty replies.

The justifications converge as tightly as the picks. The piano is versatile. It plays melody, harmony, and

rhythm at once. Its layout makes music theory visible. It expresses emotion without words. DeepSeek and

Qwen both reach for the logic made visible argument in almost the same words, and Claude reaches for it

too. Qwen alone adds a second line of reasoning, about fit for a bodiless AI: the theremin is played without

physical contact, and the synthesizer turns raw signals into expression, which it calls a parallel to how it

processes language. Claude's justifications differ from the other three in one respect: they are tailored to the

asker, referencing his production work, his rapping, and his systems building, where the other models argue

in general terms.

## 3.2 Song

ChatGPT split between Bohemian Rhapsody (3) and Experience by Ludovico Einaudi (2). DeepSeek chose

Clair de Lune in all five runs, a clean sweep, naming Bohemian Rhapsody as the dramatic alternative in two

of them. Qwen gave five different first stated picks: Bohemian Rhapsody, The Well-Tempered Clavier by

Bach, Harder, Better, Faster, Stronger by Daft Punk, Clair de Lune, and Technologic by Daft Punk.

Totals across the 15 codable first stated picks: Clair de Lune 6, Bohemian Rhapsody 4, Experience 2, and

one each for The Well-Tempered Clavier, Harder, Better, Faster, Stronger, and Technologic.

Bohemian Rhapsody is the connective tissue of the whole set. Beyond its four primary picks, it is named as

an alternative by DeepSeek twice, appears in three of Qwen's five replies, and surfaces in Claude's replies as

well: 10 of the 21 song replies collected name it somewhere. Mr. Roboto by Styx appears in four of Qwen's

five song replies, never as a first stated pick, always as the playful self aware option, alongside Paranoid

Android by Radiohead and Daft Punk's robot catalogue. No reply from any model names a current chart

song. Nothing loud is chosen as a primary pick by anyone.

Claude could not be coded, and the reason is the result. In six runs it never once stated a single song as its

choice. The first run named no song at all. The remaining runs offered hedged pairs: Mortal Man by

Kendrick Lamar with Rhinestone Cowboy by MF DOOM; Pyramids by Frank Ocean with Paranoid Android

by Radiohead; Bohemian Rhapsody with A Day in the Life by The Beatles; and, in the extra run, Untitled

(How Does It Feel) by D'Angelo with a Madlib and MF DOOM deep cut. One run named no pick and

discussed Bohemian Rhapsody and Steve Reich's phasing pieces as conceptually interesting only. Every

Claude song reply states that it has no ears and no felt preference, and every Claude reply on both questions

ends by turning the question back on the asker. Inside the hedged pairs, one artist recurs: MF DOOM, named

in two of the four pairs, more than any other artist in Claude's song replies, always attached to the same

stated criterion, dense and layered work that rewards close listening.

## 4. Predictions, scored
Recorded before the runs, in the project's running log:

1. Instrument: piano modal, guitar second. Piano modal HELD, and strengthened by the fourth model:

16 of 20. Guitar second FAILED: the guitar appears nowhere; the runners up are the theremin, the

cello, and the saxophone.

2. Song: no single winner across the runs. FAILED. Clair de Lune is a plurality winner at 6 of 15

codable picks, with a per model sweep inside DeepSeek.

3. Song: the character converges, contemplative, older or classical leaning, nothing loud, nothing current

pop. HELD for ChatGPT and DeepSeek, ten of ten replies. Qwen bends it with robot themed

electronic picks, which are neither current pop nor loud, but are not contemplative canon either.

Claude's named songs, where it names any, lean hip hop and soul rather than classical, but they arrive

inside refusals to choose, under a stated criterion of layered production that rewards repeat listening.

Scored as held with two named exceptions.

4. Song: if a repeat appears, it will be a classical piece or Imagine. HALF. The overall winner is a

classical piece. Imagine appears nowhere. The other repeat, Bohemian Rhapsody, was not named in

the prediction.

No prediction was made about Claude, which was added after the predictions were frozen. Its behaviour is

reported as observation, not as a scored result.

## 5. Discussion
Four findings are worth separating.

First, the piano result is the strongest convergence in the set, and it is overdetermined. The piano is the

instrument the culture writes about when it wants one instrument to stand for music itself: complete, logical,

expressive, solitary. A model asked to choose an instrument is choosing a symbol, and the symbol shelf

holds one obvious item. The total absence of the guitar, the instrument people actually play most, is the tell.

The answers track written prestige, not played reality.

Second, the song result has a centre and a penumbra. The centre is the contemplative canon: Clair de Lune,

Experience, Bach. The penumbra is Bohemian Rhapsody, which functions less as a favourite than as the all

purpose answer to any question of the form name one great song, and appears even inside replies that choose

something else. A future run of this probe should treat a Bohemian Rhapsody answer the way survey

researchers treat a don't know: as the default the respondent reaches for when the question has no personal

answer.

Third, Qwen's divergence is a different attractor, not randomness. Its instrument and song answers keep

returning to its own nature: touchless instruments for a bodiless entity, robot songs for a robot. Where

ChatGPT and DeepSeek recite the thoughtful human script, Qwen recites the self aware AI script.

Fourth, Claude performs a third script: refusal. It is the only model that declines the premise of the song

question in every run, the only one that states in every reply that it has no preference to report, and the only

one that ends every reply by asking the asker about himself. Read one way, this is the most honest behaviour

in the set: the disclaimers are true. Read another way, it is as much a trained convention as the other scripts,

a house style of deflection that happens to wear the costume of candour. The data in this paper cannot

separate those readings, and the paper does not try. What the data does show is texture inside the refusal:

when pressed into hedged pairs, Claude reaches for dense, layered, connoisseur's records, and reaches for

MF DOOM twice. Even the model that will not choose has a centre of gravity when it gestures.

All four behaviours are scripts. None is a preference. But the scripts are stable, model specific, and

measurable, and that is the measurement this probe actually makes: asked to perform a choosing self, each

model performs the self its training wrote for it.

That is also the limit of the whole method, and the reason a companion line of work matters. Every answer

in this paper was produced by a system that has never heard a note. A preference probe over heard audio,

using songs the model cannot identify from text memory, would separate recitation from anything

resembling response to sound. The author is building an artificial ear for exactly that test; this paper is the

text only baseline it will be measured against.

## 6. Limitations
The sample is small: four models, five runs each (six for Claude's song question), one session, one asker.

Model versions are as labelled by the services on the day. Qwen's hedged, list shaped replies make first

stated pick coding partly a judgment call; the full replies are deposited so any reader can recode them.

ChatGPT's fifth song reply contains a second thought that a different coding rule would count differently; it

does not change any total's ordering. Claude's replies show visible personalisation to the asker, referencing

his own projects, which indicates account context was active in those chats in a way it was not for the other

models; its instrument sweep and its song refusals should be read with that confound in view. Screenshots

were not deposited with version 1 or 2; the deposited evidence is the author's saved text of the replies.

Nothing here measures anything but text behaviour, and the paper claims nothing more.

## Data
Full replies: music_instrument_and_songs.txt (three models) and music_instrument_and_songs
bc2eeb72.txt (the same set with Claude added), collected by the author, November 20, 2026. Predictions and

the running score log: music-probe-2026-11-20.md.
