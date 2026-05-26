# Skill Conversion Guide

## Frontmatter

Every SKILL.md needs exactly two fields:

```yaml
---
name: kebab-case-name
description: One sentence — what it does and when to use it
---
```

Drop any Cursor-specific fields (title, globs, alwaysApply). Those don't carry over.

## Description formula

"[Action verb] + [what it teaches the agent] + [in what context]"

Good: "Layered color and shadow principles for readable UIs in light and dark themes"
Bad: "A reusable rule for making nice designs"

## Structure the body

Use this skeleton — not every section is required, but this order works:

```markdown
# Skill Name

One-line pitch: what the agent becomes capable of.

## Core Principles
The 3–6 opinionated rules that define this skill. Prose, not code.

## When to Use
Bullet list of trigger scenarios — helps the agent know when to activate.

## When NOT to Use (optional)
Prevents the agent from over-applying the skill.

## Implementation Guide
Concrete steps or checklist. Prose-first, code only when the pattern is non-obvious.

## Review Checklist (optional)
Questions the agent should ask itself after applying the skill.
```

## Code block rules

Before including any code block, pass this test:

1. Would the agent get this wrong without seeing this exact example? → Keep it
2. Is this standard syntax the model already knows? → Cut it
3. Is this a second example of the same pattern? → Cut it
4. Is this >15 lines? → Shorten it to the minimum that shows the pattern

One code block per concept, max. Never show the same idea in CSS + Tailwind + React + Svelte — pick the one that best illustrates the point.

## Token budget

Aim for 60–120 lines total. Under 80 is ideal. Every line competes with the agent's working memory for the actual task.

## Tone

Write like you're briefing a senior engineer, not teaching a beginner. State the rule, not the rationale. Skip "this is important because" — if it wasn't important it wouldn't be in the skill.

## Conversion checklist

- [ ] Frontmatter has `name` and `description` only
- [ ] No Cursor-specific fields (globs, alwaysApply, title)
- [ ] Under 120 lines
- [ ] Code blocks pass the "would the agent get this wrong?" test
- [ ] No duplicate examples across frameworks
- [ ] No sections that restate other sections (rationale, recap, summary)
- [ ] No generic advice the model already knows (run tests, check accessibility, use version control)
- [ ] Description is one specific sentence, not vague
- [ ] File is named SKILL.md and lives in skills/skill-name/