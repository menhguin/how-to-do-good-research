# how-to-do-good-research

An agent skill that sends the model to five pieces of research advice before it picks a problem, designs an experiment or writes a paper. It comes from Minh Nguyen's personal agent setup, where agents load it for research work. This is the file as it runs there.

## What it does

`SKILL.md` is short. It doesn't restate the essays. It says which one to read for which decision and what to take from it.

| Reference | Used for |
|---|---|
| Richard Hamming, [You and Your Research](https://www.cs.virginia.edu/~robins/YouAndYourResearch.html) | Choosing the problem: is it important, and is there a reasonable attack? |
| Nicholas Carlini, [How to win a best paper award](https://nicholas.carlini.com/writing/2026/how-to-win-a-best-paper-award.html) | Taste, execution and paper focus: one idea per paper, and test whatever is most likely to kill the project first |
| Neel Nanda, [Highly Opinionated Advice on How to Write ML Papers](https://www.alignmentforum.org/posts/eJGptPbbFPZGLpjsp/highly-opinionated-advice-on-how-to-write-ml-papers) | Claims and evidence: one to three claims, the experiments that decide them, red-teaming the narrative, writing in stages |
| Matthew Schwartz, [Claude-shaped science](https://www.anthropic.com/research/claude-shaped-science) and the [BootLoops](https://bootloops.ai/harness.html) protocols | Research done with agents: which problems suit a model, checks that can't certify their own inputs, what counts as finished |
| Kei, [Doing a Research Startup](https://web.archive.org/web/20240920140442/https://keiyuva.ai/posts/type.startup/) (archived copy) | Research inside a startup: how the cadence, money and incentives differ from academia or a big lab, and what that changes. Most research advice assumes the other setting, so the agent reads this first when the work is for a company |

After the references comes a nine-step working sequence, then a list of what to produce before writing a long proposal: the one-sentence idea, the best-case conclusion, up to three claims, a claim → evidence → falsifier map, and the first kill test.

## When it was written

This repo went public on 10 November 2026. The skill is older. Its commit history is imported from the private repos it lived in: author dates are the original ones, and commit dates are the day of the import.

| Date | Change |
|---|---|
| 6 Sep 2026 | First version, written during work on a research proposal, with three references: Hamming, Carlini and Nanda. Those three entries have not changed since. |
| 2 Oct 2026 | Schwartz's "Claude-shaped science" and BootLoops added as a fourth reference. |
| 21 Oct 2026 | A companion skill was renamed. |
| 10 Nov 2026 | Published: MIT license, `-custom` dropped from the skill's name, "the user" in place of the author's name, and this README. Kei's "Doing a Research Startup" added as a fifth reference the same day. |

The first version was written at about 01:04 Korea time on 6 September, which is 16:04 UTC on the 5th.

## Install

```bash
# Claude Code
git clone https://github.com/menhguin/how-to-do-good-research ~/.claude/skills/how-to-do-good-research

# Hermes
git clone https://github.com/menhguin/how-to-do-good-research ~/.hermes/skills/how-to-do-good-research
```

For any other agent, put the folder where it loads skills from, or give it the link and say "read SKILL.md before you plan this project".

## Companion skills it mentions

The skill names three other skills. [`humanizer`](https://github.com/blader/humanizer) is public: Siqi Chen's skill for removing AI-sounding prose. `ai-research-custom` and `deep-research-orchestration-custom` are private. They handle project records and literature sweeps in the setup this came from. The skill works without them, so delete those two bullets or point them at your own equivalents.

MIT licensed.
