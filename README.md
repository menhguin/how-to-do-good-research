# how-to-do-good-research

An agent skill that points the model to a short, curated set of research advice before it picks a problem, designs an experiment or writes a paper. It comes from the author's personal agent setup, where agents load it for research work. This is the file as it runs there.

## What it does

`SKILL.md` is short and built around its references. It doesn't restate them. Each entry links one piece of advice and says when to read it and what to take from it. Between them, the entries cover:

- choosing a problem worth working on
- research taste, execution and keeping a paper to one idea
- turning results into claims, evidence and a written paper
- doing research with AI agents, and checking what they produce
- doing research inside a startup, where the pace and incentives differ from academia or a big lab

After the references comes a working sequence, then a list of what to produce before writing a long proposal: the one-sentence idea, the best-case conclusion, up to three claims, a claim → evidence → falsifier map, and the first kill test.

The list is meant to grow. A new entry takes the same shape: a link, when to read it, and what to take from it.

## When it was written

This repo went public on 10 November 2026. The skill is older. Its commit history is imported from the private repos it lived in: author dates are the original ones, and commit dates are the day of the import.

| Date | Change |
|---|---|
| 6 Sep 2026 | First version, written during work on a research proposal, with three references. Their entries read the same today, apart from one sentence on when to read them, which moved into each entry from the section's intro on 10 Nov 2026. |
| 2 Oct 2026 | A fourth reference added, on research done with agents. |
| 21 Oct 2026 | A companion skill was renamed. |
| 10 Nov 2026 | Published: MIT license, `-custom` dropped from the skill's name, "the user" in place of the author's name, and this README. A fifth reference added the same day, on research inside a startup, and each entry now says when to read it. |

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

The skill names three other skills. [`humanizer`](https://github.com/blader/humanizer) is public: a skill for removing AI-sounding prose. `ai-research-custom` and `deep-research-orchestration-custom` are private. They handle project records and literature sweeps in the setup this came from. The skill works without them, so delete those two bullets or point them at your own equivalents.

MIT licensed.
