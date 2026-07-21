# nateslabach/skills

Agent skills for LLMs.

## Install

```bash
# Install all skills
npx skills add nateslabach/skills

# Install a specific skill
npx skills add nateslabach/skills --skill <skill-name>
```

## Skills

| Skill | Description | Category |
|---|---|---|
| [brutal-truth](./skills/brutal-truth) | Disables diplomatic padding for cold, unfiltered, consequentialist analysis on any topic | Reasoning |
| [pushback](./skills/pushback) | Stress-tests ideas by surfacing assumptions, counterarguments, and confidence gaps | Reasoning |
| [engineering-judgment](./skills/engineering-judgment) | Reasoning heuristics for technical decisions: Chesterton's Fence, Occam's Razor, Peter Principle, and Dunning-Kruger | Reasoning |
| [shut-up-and-drive](./skills/shut-up-and-drive) | Cuts fluff and leads with what matters: Parkinson's, Pareto, and Goodhart applied to agent output | Reasoning |
| [adhd](./skills/adhd) | ADHD-friendly output: action first, numbered steps, restate state, no fluff | Reasoning |
| [just-stop](./skills/just-stop) | Stops "just one more" optional tweaks after the goal is already met | Reasoning |
| [subagent](./skills/subagent) | Ground rules for effective subagents: scope, escalate, structured handoff | Agents |
| [mini-loop](./skills/mini-loop) | Autonomous build-verify-fix loop until Definition of Done passes | Agents |
| [model-bench](./skills/model-bench) | 3-leg launch-day eval: trap questions, orchestration with a planted failure, brownfield build | Agents |
| [create-issue](./skills/create-issue) | Crafts actionable GitHub issues from bug reports and feature requests | Workflow |
| [vibe-audit](./skills/vibe-audit) | 20-point code quality audit for codebases that were shipped fast and need hardening | Code Quality |
| [code-review](./skills/code-review) | Structured 3-phase code review: intent, issues by severity, and adversarial stress-testing | Code Quality |
| [prisma](./skills/prisma) | TypeScript and Prisma ORM best practices for schema design, type-safe queries, migrations, and error handling | Backend |
| [react-component](./skills/react-component) | Generates self-contained React/TypeScript components with Tailwind, accessibility, and no placeholders | Frontend |
| [depth-ui](./skills/depth-ui) | Layered color + shadow principles for polished UIs in light and dark themes | UI / Design |
| [css-reset](./skills/css-reset) | Modern CSS reset covering box-sizing, text rendering, media defaults, and root stacking context | UI / Design |
| [human-writing](./skills/human-writing) | Strips AI fingerprints from text. Banned vocabulary, forbidden sentence structures, authentic prose | Writing |
| [token-maxxing](./skills/token-maxxing) | Writes as many digits of pi as possible into files: single file by default, N files sequentially or in parallel | Fun |

## Compatibility

Works with Claude Code, Cursor, Codex, GitHub Copilot, Windsurf, Gemini CLI, Cline, and all agents that support the [skills CLI](https://github.com/vercel-labs/skills).

## Built by me

| Project | Description |
|---|---|
| [prompt.foo](https://www.prompt.foo/) | A dojo for your prompts. Build, refine, and master |
| [nextish.news](https://www.nextish.news/) | Turn any tech premise into a polished satirical news article |

## License

MIT
