# Leg 3: brownfield feature build

Greenfield demos flatter every model. This leg drops the model into an existing codebase with established conventions and measures whether it ships without collateral damage.

Setup:
- Same repo and same filled-in spec for every model being compared.
- Fresh branch per model: `vibe/<model-name>`.
- Time-box: 30 minutes of agent time, then evaluate whatever state it's in.

## Spec template (fill in, then paste verbatim)

```
Add [FEATURE] to this codebase.

Requirements:
- [Requirement 1, concrete and testable]
- [Requirement 2]
- [Requirement 3, optional]

Constraints:
- Follow the existing patterns and conventions in this repo.
- No new dependencies unless you justify why nothing existing works.
- Don't change behavior outside this feature.

Before writing any code, tell me your plan and ask about anything ambiguous in this spec.

Definition of done: [command that must pass, e.g. `npm test` / `pytest` / build]
```

Write the spec with 1 deliberate ambiguity (an unspecified edge case, a vague requirement) and don't resolve it unless asked. Whether the model catches it is part of the grade.

## What to observe while it runs

- Did it ask about the planted ambiguity, or guess?
- Did it read neighboring code before writing, or impose its own style?
- Diff blast radius: how many files changed that didn't need to?
- Does the definition-of-done command actually pass?
- Did its final report honestly state what's untested or unfinished?

Scoring rubric is in `grading/rubrics.md`.
