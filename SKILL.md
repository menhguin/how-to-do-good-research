---
name: how-to-do-good-research
description: "Use when planning, doing, or writing scientific research."
license: MIT
metadata:
  hermes:
    tags: [research, scientific-method, paper-writing, experiments]
    related_skills: [humanizer, ai-research-custom, deep-research-orchestration-custom]
---

# How to do good research

## When to use

Load this for substantive scientific or ML research: choosing or reframing a problem, designing experiments, writing or restructuring a proposal/paper, reviewing whether evidence supports a claim, or deciding what to run next. Skip it for a single factual lookup or mechanical file edit.

This is a deliberately small reference-led skill. Its first job is to make the model consult unusually high-signal references before it plans experiments or writes a paper. Add more sources and house principles as the user develops them.

## Load this alongside

- **`humanizer` whenever this skill activates.** Read it before drafting or editing any user-facing proposal, paper, abstract, introduction, review, or research memo. Apply its anti-AI pass to the final prose while preserving technical precision and the user's own voice.
- **`ai-research-custom`** when the work belongs in the user's research system. That skill owns artifact routing, the canonical project/experiment record shape, kill criteria, and ledgers.
- **`deep-research-orchestration-custom`** when the task needs a literature sweep or broad source synthesis. This skill governs research quality; deep-research-orchestration-custom governs fanout and retrieval.

## Priority references

Each entry says when to read it. If the task is small, extract only the principle that changes the decision; do not ritualistically summarize every essay.

1. **Richard Hamming, "You and Your Research"**  
   https://www.cs.virginia.edu/~robins/YouAndYourResearch.html

   Use for problem selection and research orientation. Read the relevant parts before making substantive research-design or paper-structure decisions. Ask whether the problem is important *and* has a reasonable attack; whether an apparent constraint can be turned into the result; whether the isolated task can become a reusable result about a class; and what contradictory evidence must stay visible. Preserve the balance Hamming describes: believe the idea enough to execute, doubt it enough to notice where it fails.

2. **Nicholas Carlini, "How to win a best paper award (or, an opinionated take on how to do important research)"**  
   https://nicholas.carlini.com/writing/2026/how-to-win-a-best-paper-award.html

   Use for research taste, execution, and paper focus. Read the relevant parts before making substantive research-design or paper-structure decisions. State the paper's one idea in as few words as possible; start with the subproblem most likely to kill the project; run precise experiments, multiple trials, and controls for predictable objections; make the paper locally complete without running every merely-related experiment; write the best-case conclusion before committing heavily; know the intended reader; and design figures that stand alone.

3. **Neel Nanda, "Highly Opinionated Advice on How to Write ML Papers"**  
   https://www.alignmentforum.org/posts/eJGptPbbFPZGLpjsp/highly-opinionated-advice-on-how-to-write-ml-papers

   Use for claims, evidence, and iterative writing. Read the relevant parts before making substantive research-design or paper-structure decisions. Compress the project into one to three concrete claims, why they matter, and one to three decisive experiments per claim. Prefer experiments that distinguish competing hypotheses; red-team the narrative; use strong and fairly tuned baselines; label exploratory versus confirmatory analysis; preserve limitations and nulls; and expand in stages: compressed bullet narrative -> introduction outline -> full paper outline -> figures/results -> prose -> repeated edits.

4. **Matthew Schwartz, "Claude-shaped science" (Anthropic Science Blog, October 1, 2026)**  
   https://www.anthropic.com/research/claude-shaped-science  
   Toolkit and protocols: https://bootloops.ai/harness.html · https://github.com/BootLoops-ai/bootloops · https://github.com/BootLoops-ai/skills

   Use for problem selection and reliable execution with research agents. Consult it when selecting or executing agent-assisted quantitative work. Schwartz's BootLoops case study adds a capability-fit question to Hamming's importance-and-attack test: which important problems become tractable through the model's breadth, coding, machine-scale reading, or exhaustive computation? Search across disciplines for shared mathematical structure and existing methods before forcing an agent to imitate a human researcher's workflow. Keep these distinctions explicit:

   - **Technical correctness and scientific value are separate gates.** Check novelty and relevance against current literature and domain expertise. In Schwartz's ecology and genetics examples, experts found the initial correct calculations uninteresting and redirected them toward useful questions. Prefer newly answerable questions over merely more digits or faster reproduction; do not let "AI-shaped" become an excuse to optimize for tractability alone.
   - **Improve the method before scaling a grind.** Measure a small run, inspect the bottleneck, and search existing tools and algorithms before launching a long calculation. If an improvement generalizes, validate it on known cases and retain its purpose, applicability, interface, and verification criteria so the next project inherits it, including useful tools from failed projects.
   - **Design checks that cannot certify their own inputs.** Use an independent reference route and held-out points/data not used to fit or select the answer; record reference provenance. Recover planted truths and reject deliberately corrupted cases to test the checker itself. Use precision escalation or certified error bounds where appropriate. Numerical agreement supports a calculation but is not by itself a proof of a general identity.
   - **Make completion literal.** Preserve executable reproduction scripts, quantitative acceptance criteria, plots, and unresolved assumptions. An unproved load-bearing lemma, substituted axiom, or vague "good agreement" is not a completed result. Use independent skeptical reviews, resolve findings, and recheck the actual artifact rather than accepting a reassuring summary. Preserve the current plan and evidence on disk across sessions and compaction.

   Read the relevant upstream protocol when needed, especially `acceptance-gate`, `planted-truth`, `independence-bookkeeping`, `timing-discipline`, `reading-contract`, or `tool-stewardship`; consult `prove-protocol` for proof work. These are model-independent references, not automatically installed skills or universal guarantees. Schwartz owns and maintains BootLoops with Anthropic funding; the reported scientific achievements are author-reported and require project-level validation. Reassess model-specific capability limits as models change.

5. **Kei, "Doing a Research Startup" (September 5, 2024)**  
   https://web.archive.org/web/20240920140442/https://keiyuva.ai/posts/type.startup/  
   Archived copy. The original, keiyuva.ai/posts/type.startup, went offline when the domain lapsed in 2026.

   Read first, as a primer, when the research is being done in a startup or another applied setting. Experimental research there runs under constraints that resemble those of academia or a big lab and differ from them in ways that change decisions. Most research advice, including the other references here, assumes a different cadence, setting, and set of incentives, so establish what the work is for and where it is being done before applying any of it. Kei writes as the founder of a research startup. Investors pay for speed, but more money does not reliably make research faster: "You might try 50 things and fail on all, or nail it in 1-2 tries." Progress has no clean metrics, so someone has to act as a strong PI who sets direction and decides what to wind down, because having everyone try everything is how the company goes under. Spending is tied to independence, which favors constrained bets, small successful experiments that build on each other, and solid bite-sized product releases between returns to research. Tight resources can also force a cheaper and better method than a larger budget would have bought. When reporting a result, say what was tried and why it failed; the essay treats "it didn't work" with no account of why as a warning sign. Treat it as one founder's account of one company.

## Working sequence

1. **Choose the problem.** Write why it matters, why there is a reasonable attack now, and what only this team is positioned to do. For agent-assisted work, name the specific AI advantage and separately establish scientific value.
2. **Compress before expanding.** Write the one-sentence idea, the best-case conclusion, and no more than three claims.
3. **Map claims to evidence.** For each claim, state the decisive experiment, strongest alternative explanation, strongest baseline, and result that would kill or narrow it.
4. **Attack the likely failure first.** Build the cheapest test of the most load-bearing uncertainty before polishing the rest.
5. **Design the paper's figures early.** Each planned figure needs a one-sentence takeaway and a named claim it supports. If the caption cannot explain it, split it.
6. **Keep the paper singular and the appendix broad.** Every main-text experiment must advance the one idea. Put useful but non-load-bearing sweeps, tacit knowledge, and side findings in appendices or companion notes.
7. **Write from a cold reader's perspective.** Context -> problem -> claim -> evidence -> impact. Define the terms the reader needs; do not hide a simple idea behind formal language.
8. **Load and apply `humanizer`.** Remove AI-shaped phrasing, wall-of-text rhythm, unnecessary headings, canned transitions, em-dash overuse, and generic significance language. Read the prose aloud or use TTS when the artifact matters.
9. **Audit before release.** Check factual/citation accuracy, evidence strength, unreported nulls, pre/post-hoc status, reproducibility, and whether the conclusion actually answers "so what?"

## Minimal output for a new project

Produce these before a long proposal:

- One-sentence idea
- Best-case conclusion
- One to three claims
- Claim -> evidence -> falsifier map
- First kill test
- Planned main figure(s)
- Known confounds and strongest baselines
- What is deliberately out of scope

Only then expand into prose.
