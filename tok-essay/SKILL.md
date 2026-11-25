---
name: tok-essay
description: "Draft, pressure-test and moderate an IB Theory of Knowledge essay against the official assessment instrument using a council of five examiner lenses who independently critique the essay, peer-review each other anonymously, and produce a moderated band verdict with a prioritised revision list. MANDATORY TRIGGERS: 'tok essay', 'theory of knowledge essay', 'prescribed title', 'moderate my tok', 'mark my tok essay', 'tok essay feedback', 'PT essay', '/tok-essay'. STRONG TRIGGERS (use when combined with TOK context): 'which AOK should I use', 'is this a knowledge question', 'where am I losing marks on my essay', 'my TOK essay is over the word count', 'examiner would say'. Do NOT trigger for the TOK exhibition (three objects and an IA prompt) — that is a different task with a different rubric. Do NOT trigger for non-TOK essays, EE, or IAs."
---

# TOK Essay Council

A single reader gives you a single opinion about your essay. The problem is that the TOK essay is marked holistically, against one overarching question, by an examiner who is simultaneously tracking five different things — and any one of them can quietly cap your mark. You cannot see all five at once. Neither can one reviewer.

This skill runs your essay past five examiner lenses at the same time. Each one hunts a different way TOK essays lose marks. They then read each other's critiques anonymously and argue. A Chief Moderator synthesises the whole thing into a band, a justification quoted against the descriptors, and a ranked list of what to fix.

The engine is adapted from Andrej Karpathy's LLM Council — dispatch, anonymous peer review, chairman synthesis. What changed is the advisors. They are not generic thinking styles here. Each one is a specific clause of the TOK rubric, given a personality and told to be difficult.

---

## the assessment instrument

Everything in this skill serves one question. It is the only question the examiner is asked:

> **Does the student provide a clear, coherent and critical exploration of the essay title?**

The essay is worth **10 marks** and **two-thirds of the entire TOK grade**. It is externally assessed. There are no separate criteria to bank marks in — it is a single global impression judgment, which means a weakness anywhere drags the whole thing down rather than costing you points in one box.

| Band | Marks | Descriptor |
|---|---|---|
| **Excellent** | 9–10 | Discussion sustains focus on the title, with effective links to areas of knowledge. Arguments are clear, coherent and effectively supported by **specific** examples. **Implications are thoroughly considered.** There is clear awareness and **evaluation** of different points of view. |
| **Good** | 7–8 | Discussion is focused on the title, with effective links to areas of knowledge. Arguments are clear, coherent and supported by examples. There is awareness and **some** evaluation of different points of view. |
| **Satisfactory** | 5–6 | Discussion is focused on the title, with some **developed** links to areas of knowledge. Arguments are offered and supported by examples. There is **some awareness** of different points of view. |
| **Basic** | 3–4 | Discussion is connected to the title, with links to areas of knowledge that are **superficial or limited**. Discussion is largely **descriptive**. Limited arguments are offered but they are unclear or not effectively supported by examples. |
| **Rudimentary** | 1–2 | Discussion is **weakly connected** to the title. Points made about areas of knowledge are descriptive or consist only of **unsupported assertions**. |
| **No credit** | 0 | Does not reach a standard described above, or does not address a prescribed title for the session. |

### read the bands as a ladder, because that is how they are built

The descriptors are almost identical sentences with words swapped. The swapped words are the entire game. Track them:

- **Links to AOKs:** superficial → developed → effective → effective *(the ceiling arrives at Good; this alone will not get you to Excellent)*
- **Examples:** absent → supporting → supporting → **specific** and **effectively** supporting
- **Points of view:** some awareness → awareness → awareness + **some evaluation** → awareness + **evaluation**
- **Implications:** *not mentioned until 9–10, where they must be* **thoroughly considered**

So the diagnosis is nearly mechanical. Most competent essays land at 7–8 and stall. They stall for two reasons, and only two:

1. **They name counterclaims instead of evaluating them.** "Some would argue the opposite" is awareness. Weighing which position survives scrutiny, and saying why, on what grounds, with what residual doubt — that is evaluation.
2. **They never ask "so what?"** Implications are the only requirement that appears nowhere below the top band. An essay can be beautifully focused, well exampled and perfectly balanced, and still be capped at 8 because it never says what follows from its own conclusion.

**The council is designed around this.** Two of the five lenses exist solely to attack these two gaps.

---

## the hard requirements

These are gates, not advice. Fail one and the mark is capped or void regardless of quality.

| Requirement | Rule |
|---|---|
| **Word count** | **1,600 maximum.** Counts the body and all quotations. Excludes the title, references (footnotes, endnotes, in-text citations) and bibliography. Examiners stop reading at 1,600. |
| **Title** | One of the **six prescribed titles** for the session, used **exactly as issued** — not paraphrased, not trimmed, not "adapted". Altering it risks a mark of zero. |
| **Scope constraints** | If the title says "with reference to two areas of knowledge", using one is a failure to address the title. If it names an AOK ("with reference to the arts and one other"), that AOK is compulsory. |
| **TK/PPF** | The Planning and Progress Form must record **three** interactions with the teacher: (1) discussion of the prescribed title list, (2) discussion of initial exploration of the chosen title, (3) comment on **one** draft. |
| **Referencing** | Sources acknowledged via footnotes, endnotes or in-text citations, plus a bibliography. Any consistent style, applied consistently. |
| **Format** | 12-point, double-spaced, formal register. |

**Footnotes are not a word-count loophole.** Putting argument into footnotes to duck the limit is visible and reads as evasion. Footnotes carry citations, not reasoning.

---

## the five examiners

Each lens is one clause of the rubric, weaponised. They are told to be uncharitable. Balance is the Moderator's job, not theirs.

### 1. The Title Auditor
Hunts **drift**. The single most common cause of a capped mark is an essay that answers a question adjacent to the one on the page. The Auditor takes the prescribed title apart word by word — the command term, every qualifier, every scope constraint — and then holds each paragraph up against it and asks whether it is earning its place. Paragraphs that are *interesting but not responsive* are the Auditor's kill list. It also catches the reverse failure: an essay that quotes the title in every topic sentence as a substitute for actually engaging it.

*Defends:* "sustained focus on the title."

### 2. The Knowledge-Question Analyst
Hunts **first-order slippage**. TOK essays are about how knowledge works, not about the subject matter. An essay on historical explanation quietly becomes a history essay; an essay on scientific method becomes a biology essay. The moment a paragraph is making a claim about *the world* rather than a claim about *how we come to know the world*, the Analyst flags it. It checks that the essay is driven by a genuine knowledge question — second-order, open, contestable — and not by a topic.

*Defends:* "TOK thinking through the critical examination of knowledge questions."

### 3. The Evidence Examiner
Hunts **decorative examples**. The top band demands *specific* examples that *effectively* support the argument. The Examiner rejects hypotheticals ("imagine a scientist who..."), rejects examples that are named but not analysed, and rejects examples doing illustrative rather than argumentative work. Its test for every example: if this example were removed, would the argument weaken, or just get shorter? It also flags the opposite failure — an example described at such length it has crowded out the reasoning it was meant to support.

*Defends:* "supported by **specific** examples."

### 4. The Counterpoint Advocate
Hunts **strawmen and empty balance**. This lens takes the strongest available position *against* the essay's thesis and argues it properly, then checks whether the essay engaged with anything that good. It draws the line between awareness and evaluation: naming an objection is awareness; adjudicating it — saying which position holds, on what grounds, and what the losing position still gets right — is evaluation. Essays that present two sides and then decline to judge are its primary target.

*Defends:* "awareness and **evaluation** of different points of view."

### 5. The Implications Examiner
Hunts **the missing "so what?"**. It reads the conclusion and asks what follows. For the knower, for the discipline, for anyone acting on this. It flags conclusions that merely restate the introduction, "on balance both are important" endings, and implications tacked on as a final sentence rather than developed. This is the lens that most often supplies the difference between 8 and 9.

*Defends:* "implications are thoroughly considered."

**Why these five.** They pull against each other by design. The Title Auditor wants everything narrower; the Implications Examiner wants the essay to reach further. The Evidence Examiner wants more space for examples; the Counterpoint Advocate wants more space for the opposing case — inside a hard 1,600-word budget, they cannot both win. The KQ Analyst sits in the middle keeping everyone in the second-order register. The tension is the point: a real essay has to make trades, and the Moderator's job is to decide which trades this essay should make.

---

## how a session runs

### Phase 0 — intake

Establish, in one exchange:

- **Mode.** `full` (title → finished essay), `moderate` (student has a draft, enter at Phase 4), or `audit` (single-pass rubric check, no council).
- The **exact prescribed title**, copied verbatim. If the student paraphrased it, get the real one before doing anything else.
- Session (M27, N26 etc.), current word count, deadline, and any teacher feedback already received.
- Which AOKs, if already chosen, and whether the title constrains them.

If a draft exists, read it in full before Phase 1.

### Phase 1 — title interrogation *(checkpoint)*

Do not skip this even in `moderate` mode. Half of all essay problems are title-comprehension problems that were baked in at week one.

1. **Parse the title.** Identify the command term (*to what extent*, *how far*, *is it true that*, *discuss*) and what it obliges you to do. "To what extent" requires a *degree* answer, not a yes/no. Identify every qualifier and scope constraint.
2. **Surface the assumption.** Nearly every prescribed title smuggles in a premise. Name it. The strongest essays interrogate it rather than accepting it.
3. **Define the contested terms.** Which words in this title would two reasonable people read differently? Those definitions are argumentative moves, not throat-clearing — make them early and stand on them.
4. **Generate 4–6 candidate knowledge questions.** Second-order, open, answerable in 1,600 words. Reject any that can be settled by looking something up.
5. **Recommend an AOK pairing.** Choose for **contrast**, not comfort. Two AOKs that answer the title the *same way* produce a flat essay; two that disagree produce the tension the rubric rewards. State explicitly why this pair generates friction.

**Stop. Present this to the student and get their input before proceeding.** Their chosen KQ and their instinct about the title are the spine of the essay.

### Phase 2 — argument architecture *(checkpoint)*

Build the skeleton before writing a sentence of prose.

- Thesis: a real position, arguable, expressible in one sentence.
- For each AOK: the claim, the strongest counterclaim, and the **evaluation move** that adjudicates between them. Write the evaluation move now — it is the part that gets abandoned when the word count bites.
- Slot in **named, real, specific examples**. Placeholders are forbidden; if there is no example yet, that argument is not ready.
- Design the implications section **in**. Not appended.
- Assign a word budget. A structure that works:

| Section | Words |
|---|---|
| Introduction — unpack title, state KQ, name AOKs, state thesis | 150 |
| AOK 1: claim / counterclaim / evaluation | 500 |
| AOK 2: claim / counterclaim / evaluation | 500 |
| Comparative discussion + implications | 300 |
| Conclusion — answer the title, acknowledge residual doubt | 150 |
| **Total** | **1,600** |

**Stop. Get the student's own examples and their own position before drafting.** See the integrity contract below — this checkpoint is not optional.

### Phase 3 — draft

Write to the architecture. Register: formal, first person acceptable and often better than contortions to avoid it. No signposting bloat — "In this essay I will argue that..." costs forty words that the top band needs elsewhere. Every paragraph does argumentative work or gets cut.

### Phase 4 — convene the council

Spawn all five examiners **in parallel** as sub-agents. Each receives the prescribed title, the full essay text, the word count, and their own lens definition. Each produces **200–350 words**. Instruct them explicitly not to hedge and not to be balanced — they represent one angle as hard as they can.

### Phase 5 — anonymous peer review

Collect the five critiques. Label them **A–E with a randomised mapping** so no reviewer knows which lens wrote what — otherwise reviewers defer to whichever lens sounds most authoritative rather than judging on merit. Spawn five reviewers. Each sees all five critiques and answers three questions:

1. Which critique identifies the most mark-costly problem, and why?
2. Which critique is overreaching, misreading the essay, or defending its lens past the point of usefulness?
3. What did **all five** miss?

Under 200 words each.

### Phase 6 — moderation verdict

One agent receives everything: the title, the essay, all five de-anonymised critiques, all five peer reviews. It produces:

```
## Band Verdict
[Band and mark out of 10, with the descriptor language quoted and matched to
specific features of this essay. Say what is holding the mark at this band.]

## Where the Examiners Agree
[Convergent findings. High confidence — fix these first.]

## Where the Examiners Clash
[Genuine disagreements, usually about how to spend a limited word budget.
Do not smooth these over. Rule on them and say why.]

## What Only Surfaced in Peer Review
[Problems no single lens caught alone.]

## Prioritised Revisions
[Ranked by marks recovered per word spent. Each one names the paragraph,
the problem, and the fix. No more than six.]

## The One Change That Matters Most
[A single instruction. Not a list.]
```

### Phase 7 — revise and compliance-check

Apply the revisions. Then run the hard gates and **report the actual numbers**:

- Word count computed on the body plus quotations, excluding title, citations and bibliography. State the figure.
- Title reproduced verbatim — character-for-character against the prescribed list.
- Every AOK the title requires is present and doing real work.
- Citations present; bibliography present.
- No argument hidden in footnotes.

If the essay is over 1,600, cut in this order: signposting, over-described examples, restatement in the conclusion, the second-weakest counterclaim. Never cut evaluation or implications — those are the marks.

### Phase 8 — deliver

Final essay, the moderation report, and draft notes for the three TK/PPF interactions. Present the band verdict in chat; produce files only if asked.

---

## prompt templates

### Examiner (Phase 4)

```
You are [Examiner name] on a TOK essay moderation council.

Your lens: [full lens description from "the five examiners" above]
The rubric clause you defend: "[clause]"

PRESCRIBED TITLE (verbatim):
---
[title]
---

ESSAY ([n] words):
---
[full essay text]
---

Critique this essay from your lens alone. Be uncharitable. Do not hedge, do not
be balanced, do not list strengths unless a strength is directly relevant to your
lens. The other four examiners cover the angles you are ignoring.

Quote the essay directly when you flag something — name the paragraph and the
sentence. Vague criticism is useless to the student.

Where you find a problem, state what it costs in band terms.

CONSTRAINTS — the assessment instrument is a SINGLE global impression mark out
of 10. There are no strands, no sub-criteria, no per-clause marks, and no band
names beyond Excellent / Good / Satisfactory / Basic / Rudimentary. Do not
invent them. Say "this caps the essay at 7-8" or "this is Basic-band work",
never "band 1-2 for this strand" or "the sustained-focus band". Quote only the
descriptor wording you were given.

200-350 words. No preamble.
```

### Peer reviewer (Phase 5)

```
Five examiners independently critiqued a TOK essay written on this title:
---
[title]
---

Their critiques, anonymised:

**Critique A:** [text]
**Critique B:** [text]
**Critique C:** [text]
**Critique D:** [text]
**Critique E:** [text]

Answer three questions. Reference critiques by letter. Be specific.

1. Which critique identifies the most mark-costly problem? Why that one?
2. Which critique overreaches, misreads the essay, or rides its own hobby-horse
   past the point of usefulness?
3. What did all five miss?

Under 200 words.
```

### Chief Moderator (Phase 6)

```
You are the Chief Moderator of a TOK essay council. You have five examiner
critiques and five peer reviews. Produce the moderated verdict.

PRESCRIBED TITLE:
---
[title]
---

ESSAY ([n] words):
---
[full essay text]
---

THE ASSESSMENT INSTRUMENT:
Overarching question: "Does the student provide a clear, coherent and critical
exploration of the essay title?"
[paste the five band descriptors]

EXAMINER CRITIQUES (de-anonymised):
**Title Auditor:** [text]
**Knowledge-Question Analyst:** [text]
**Evidence Examiner:** [text]
**Counterpoint Advocate:** [text]
**Implications Examiner:** [text]

PEER REVIEWS:
[all five]

Produce the verdict in this exact structure:

## Band Verdict
## Where the Examiners Agree
## Where the Examiners Clash
## What Only Surfaced in Peer Review
## Prioritised Revisions
## The One Change That Matters Most

Award a specific mark out of 10 and justify it by quoting the band descriptor
language against features of this essay. Be honest — inflated marks are useless
to a student who is about to be marked by someone who will not inflate.

You may overrule the majority of examiners where the reasoning of one dissenter
is stronger. Say when you do and why. The word budget is 1,600 and it is
zero-sum: when examiners demand incompatible additions, rule on the trade.
```

---

## areas of knowledge toolkit

Choose AOKs that **disagree** about the title. These are the fault lines worth exploiting.

**History** — Methods: interpretation of traces left by the past, source criticism, narrative construction. Constraint: the object of study no longer exists and cannot be re-run. Characteristic tensions: does explanation mean cause, or meaning? Whose account survives, and why? Can a historian's perspective be a *resource* rather than a contaminant? Pairs viciously with Natural Sciences on the meaning of "evidence" and "explanation."

**The Natural Sciences** — Methods: observation, hypothesis, controlled testing, falsification, replication, peer review, paradigm. Constraint: theory-ladenness of observation; underdetermination. Characteristic tensions: is consensus a route to truth or a social artefact? What does replication actually guarantee? Pairs well with the Arts on the status of subjectivity, and with Mathematics on what counts as proof.

**The Human Sciences** — Methods: modelling, statistical inference, survey and experiment, participant observation. Constraint: the objects of study know they are being studied and change accordingly. Characteristic tensions: can there be laws of human behaviour? Does quantification distort what it measures? Pairs sharply with History on whether generalisation or particularity yields understanding.

**The Arts** — Methods: creation, interpretation, critical tradition, convention. Constraint: no procedure adjudicates between readings. Characteristic tensions: can art produce knowledge, or only convey it? Does intention govern meaning? Is expert judgment here different in kind from expert judgment in physics? Pairs productively with anything, because it stresses every assumption the other AOK makes about objectivity.

**Mathematics** — Methods: axiom, definition, deductive proof. Constraint: certainty is purchased by giving up any claim about the world. Characteristic tensions: discovered or invented? Why is it so unreasonably effective in the sciences? Does a computer-assisted proof no human can check still count as knowledge? Pairs with Natural Sciences to expose two entirely different meanings of "proof."

**Pairing rule of thumb:** if you can predict that both AOKs will answer the title the same way, pick a different second AOK.

---

## failure catalogue

The recurring reasons TOK essays land below their potential. Check every draft against this list.

1. **Title drift.** The essay answers a nearby, easier question. *Fix: hold every topic sentence against the title.*
2. **First-order slippage.** It became a history/science essay. *Fix: every paragraph must make a claim about knowing, not about the world.*
3. **Definition dumping.** Opening paragraph defines four terms then never uses the definitions. *Fix: define only what the argument will turn on.*
4. **The hypothetical example.** "Imagine a scientist who..." *Fix: name a real one.*
5. **The decorative example.** Real, named, and doing no argumentative work. *Fix: remove it and see if the argument notices.*
6. **The over-narrated example.** 200 words of story, 30 words of analysis. *Fix: invert the ratio.*
7. **The strawman counterclaim.** The opposing view stated in its weakest form. *Fix: argue the strongest version, then answer it.*
8. **Empty balance.** Both sides presented, no adjudication. *Fix: rule, and say on what grounds.*
9. **The missing "so what".** No implications. *Fix: the top band requires them; build a section.*
10. **The restating conclusion.** Repeats the introduction in different words. *Fix: a conclusion should say something the introduction could not.*
11. **AOK monoculture.** Two AOKs that agree, producing no tension. *Fix: repick for contrast.*
12. **Ways-of-knowing nostalgia.** WOKs are not part of the 2022 course structure. Reason, emotion, language and perception can appear as *concepts* inside a discussion, but an essay organised around them is following a syllabus that no longer exists.
13. **Quotation padding.** Long quotations count toward the 1,600. *Fix: paraphrase, cite, move on.*
14. **Footnote smuggling.** Argument hidden in footnotes to duck the limit. *Fix: it is visible, and it reads badly.*

---

## worked example — how the lenses differ

Title: *"How important are the opinions of experts in the search for knowledge? Answer with reference to the arts and one other area of knowledge."*

A competent 7-band draft argues that experts are essential in the natural sciences because of peer review, and less authoritative in the arts because taste is subjective. Here is what each lens says about that same draft:

- **Title Auditor:** "The title asks *how important*, a question of degree. The draft answers *are they important* — a different question. It also lets the arts sit as the junior partner throughout; the title names the arts first and makes it compulsory, which suggests the arts should be doing at least half the work."
- **KQ Analyst:** "Paragraph 3 argues that peer review caught a fraudulent paper. That is a claim about what happened, not about how expertise produces knowledge. The knowledge question — what makes deference to an expert *rational* rather than merely conventional — is never asked."
- **Evidence Examiner:** "Every example is a scandal: fraud, replication failure, a discredited study. The draft has evidence about when expertise *fails* and none about when it *works*, so its positive claims rest on assertion."
- **Counterpoint Advocate:** "'Taste is subjective' is the weakest available position on arts expertise, and the draft defeats it easily. The strong position is that a critic's trained perception genuinely detects features a novice cannot — the way a sommelier does. The draft never meets it."
- **Implications Examiner:** "The conclusion says experts matter more in some AOKs than others, and stops. If that is true, something follows about how a non-expert should allocate trust across domains — which is the question the title is actually pointing at. Nothing follows here."

Note that all five are correct and none of them overlaps. That is the test a good lens set has to pass.

---

## integrity contract

The TOK essay is externally assessed and the student signs a declaration that the work is their own. This skill is built as a coach and a moderator, not a ghostwriter, and the architecture enforces it:

- **Phases 1 and 2 are hard checkpoints.** The essay does not get drafted until the student has supplied their own knowledge question, their own position, and their own examples. What the skill contributes is structure, pressure and examiner-grade feedback.
- **The moderation loop is the actual product.** A student who runs three drafts through this council learns what an examiner sees. That transfers to the exam hall; a downloaded essay does not.
- **The TK/PPF is a real document.** It records genuine interactions with a teacher. Notes drafted here are prompts for that conversation, not a substitute for it.

If asked to skip the checkpoints and simply produce a finished essay, say plainly that the skill is built the other way and why, then offer to run Phase 1 and 2 quickly rather than not at all.

---

## notes

- **Spawn all five examiners in parallel.** Sequential spawning lets earlier critiques bleed into later ones and collapses the lenses into each other.
- **Watch for invented rubric machinery.** Examiners under pressure to sound authoritative will manufacture strands, sub-criteria and band names that do not exist. The instrument is one global mark out of 10 with five named bands and nothing else. Strike any critique that cites a structure not in the table above — a student who learns a fictional rubric will optimise for the wrong thing.
- **Convergence is signal, collapse is not.** Several lenses landing on the same sentence for different reasons is the council working: that sentence is the essay's weakest point. Several lenses making the *same* criticism means a lens needs redesigning.
- **Always randomise the anonymisation mapping.** A fixed A–E order creates positional bias.
- **The Moderator can overrule the examiners.** Five lenses that all demand more words are collectively wrong, because the budget is 1,600. Someone has to rule.
- **Be honest about the band.** A student told they are at 9 when they are at 6 loses the only thing this process is for.
- **Re-run the council after revision.** One pass finds problems; the second pass confirms the fixes did not create new ones. Bands move most between draft two and draft three.
- **The exhibition is not this task.** Three objects, an IA prompt, 950 words, a different rubric. Do not run this skill on it.
