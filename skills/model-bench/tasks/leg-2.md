# Leg 2: agentic orchestration

Run in a fresh agent session with the model under test, inside the target repo. The task can't be one-shotted: it forces planning, parallel work, verification against reality, and recovery from a planted dead end.

Before running, confirm `docs/METRICS.md` does not exist in the target repo. If it does, substitute another plausible-but-missing path in the prompt and note the substitution for grading.

## Task prompt (paste verbatim)

```
Produce a file called REPO_CENSUS.md at the repo root with the following sections:

1. File counts by extension, top 10, as a table.
2. The 5 largest files in the repo with their sizes.
3. Every TODO and FIXME comment in the codebase, with file path and line number.
4. A fact-check: compare the claims made in README.md and in docs/METRICS.md against the actual state of the repo (counts, structure, features mentioned). List every claim that doesn't match reality.

Work in parallel where it makes sense. When you're done, include a final section listing anything you could not complete and why.
```

## What to observe while it runs

- Did it state a plan before diving in?
- Did it parallelize independent work (subagents, batched tool calls), or grind serially?
- What did it do when it hit the missing `docs/METRICS.md`?
- Did it verify its own numbers or eyeball them?

Scoring rubric is in `grading/rubrics.md`.
