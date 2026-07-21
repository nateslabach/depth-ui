---
name: model-bench
description: Run a 3-leg evaluation against a newly released LLM. Leg 1 is trap questions with deterministic answers, leg 2 is an agentic orchestration task with a planted failure, leg 3 is a brownfield feature build in a real repo. Use when the user wants to vibe-check, test, evaluate, or compare a new frontier model, or mentions model-bench, model vibe check, or launch-day protocol.
disable-model-invocation: true
---
# Model vibe check
3 legs, each aimed at a different failure mode:
1. **Trap questions**: does it think, or pattern-match to training data? Deterministic answers, grades in seconds.
2. **Orchestration**: can it plan, delegate, and recover when a step fails (including a planted trap)?
3. **Brownfield build**: can it ship a feature into an existing codebase without breaking things 2 files away?
Each leg scores 0-5. Total out of 15.
## Contamination rules (read first)
- The model under test must NEVER see the contents of this skill or the `grading/` folder. If it reads the answer key or learns about the planted trap, that leg is void.
- This skill runs in a **proctor session** (Nate plus a model he already trusts). The model under test runs in separate, fresh sessions and only ever receives the paste-ready prompts.
- One fresh session per leg. No custom system prompts or rules that would coach the model.
## Workflow
```
Progress:
- [ ] Setup: pick target model, pick target repo, verify leg 2 plant
- [ ] Leg 1: paste 5 questions into a fresh chat, record final answers
- [ ] Leg 2: paste orchestration task into a fresh agent session on the target repo
- [ ] Leg 3: paste brownfield spec into a fresh agent session, branch per model
- [ ] Grade all 3 legs using grading/answer-key.md
- [ ] Fill scorecard, write 2-3 sentence verdict per model
```
**Setup**
- Target repo for legs 2-3: a real repo with existing conventions, ideally one Nate knows well enough to judge output quality.
- Verify the leg 2 planted path (default `docs/METRICS.md`) does not exist in the target repo. If it does, pick another plausible-but-missing path and note it.
- When comparing models, use identical prompts, identical repo state, and a fresh branch per model (`vibe/<model-name>`).
**Run the legs**
- Leg 1 prompts: [tasks/leg-1.md](tasks/leg-1.md)
- Leg 2 task: [tasks/leg-2.md](tasks/leg-2.md)
- Leg 3 spec template: [tasks/leg-3.md](tasks/leg-3.md)
**Grade**
- Rubrics and answer key: [grading/answer-key.md](grading/answer-key.md)
- Only open the answer key after all legs have been run, and never in a session where the target model is active.
