# TOK Essay Council

A Claude skill that marks an IB Theory of Knowledge essay the way a moderation panel would. Five examiners each read the essay through one clause of the rubric, review each other's critiques anonymously, and a Chief Moderator turns all of it into a mark out of 10 with a ranked list of fixes.

It is built for IB Diploma students writing the TOK essay (1,600 words, one of the six prescribed titles) and for teachers who want a second reader before giving feedback.

## Install

**Claude app or claude.ai.** Download `tok-essay.zip` from the [latest release](../../releases/latest), then go to Settings, Capabilities, Skills and upload the zip. Skills need to be switched on for your account first.

**Claude Code.** Copy the skill folder into your skills directory:

```sh
git clone https://github.com/shorielol/tok-essay-council
mkdir -p ~/.claude/skills && cp -r tok-essay-council/tok-essay ~/.claude/skills/
```

Start a new session and type `/tok-essay`, or just ask it to mark your TOK essay.

## What happens when you run it

The skill asks for the exact prescribed title first. A paraphrased title can score zero, so it won't start without the real one. Then it offers three modes:

- `full` takes you from the title to a finished essay, stopping twice to get your own knowledge question, position and examples before anything is drafted.
- `moderate` starts from a draft you already have and goes straight to the council.
- `audit` is a single rubric check with no council, for when you want a quick read.

The five examiners are the Title Auditor (drift away from the question), the Knowledge-Question Analyst (paragraphs that slide into being a history or biology essay), the Evidence Examiner (hypothetical or decorative examples), the Counterpoint Advocate (counterclaims that get named but never weighed) and the Implications Examiner (conclusions that never say what follows). The last two exist because those are the two gaps that usually hold a decent essay at 7 or 8.

They are told to disagree. Inside a 1,600-word limit you can't add everything every examiner wants, so the Moderator's report rules on those trades instead of averaging them. It ends with one change that matters most.

## What it won't do

It won't write your essay for you and hand it over. The TOK essay comes with a signed declaration that the work is yours, so the skill stops at two checkpoints and waits for your own ideas before it drafts. Asking it to skip them gets a short explanation and an offer to run those steps quickly.

It also won't mark the TOK exhibition, an Extended Essay or an IA. Those have different rubrics.

The mark it gives is an estimate from a model reading against the published band descriptors, not an IB examiner's mark. It works best as a way to find what's holding a draft back. Run it again after each revision.

## How it works

The council structure is adapted from Andrej Karpathy's [LLM Council](https://github.com/karpathy/llm-council): parallel critiques, anonymous peer review with a shuffled A to E mapping, then a chair who writes the verdict. Here each advisor is tied to a specific rubric clause rather than a general thinking style. Everything else, including the prompt templates, the failure catalogue and a worked example, is in [`tok-essay/SKILL.md`](tok-essay/SKILL.md).

## Licence

MIT. See [LICENSE](LICENSE).
