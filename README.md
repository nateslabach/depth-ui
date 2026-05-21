# nateslabach/skills

Agent skills for AI coding assistants.

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
| [pushback](./skills/pushback) | Stress-tests ideas by surfacing assumptions, counterarguments, and confidence gaps | Reasoning |
| [engineering-judgment](./skills/engineering-judgment) | Reasoning heuristics for technical decisions — Chesterton's Fence, Occam's Razor, Peter Principle, and Dunning-Kruger | Reasoning |
| [response-discipline](./skills/response-discipline) | Cuts padding and leads with what matters — Parkinson's Law, Pareto, and Goodhart's Law applied to agent output | Reasoning |
| [vibe-audit](./skills/vibe-audit) | 20-point code quality audit for codebases that were shipped fast and need hardening | Code Quality |
| [code-review](./skills/code-review) | Structured 3-phase code review — intent, issues by severity, and adversarial stress-testing | Code Quality |
| [prisma](./skills/prisma) | TypeScript and Prisma ORM best practices for schema design, type-safe queries, migrations, and error handling | Backend |
| [react-component](./skills/react-component) | Generates self-contained React/TypeScript components with Tailwind, accessibility, and no placeholders | Frontend |
| [depth-ui](./skills/depth-ui) | Layered color + shadow principles for polished UIs in light and dark themes | UI / Design |
| [css-reset](./skills/css-reset) | Modern CSS reset covering box-sizing, text rendering, media defaults, and root stacking context | UI / Design |
| [human-writing](./skills/human-writing) | Strips AI fingerprints from text — banned vocabulary, forbidden sentence structures, authentic prose | Writing |
| [token-maxxing](./skills/token-maxxing) | Writes as many digits of pi as possible into files — single file by default, N files sequentially or in parallel | Fun |

## Compatibility

Works with Claude Code, Cursor, Codex, GitHub Copilot, Windsurf, Gemini CLI, Cline, and all agents that support the [skills CLI](https://github.com/vercel-labs/skills).

## Built by me

| Project | Description |
|---|---|
| [prompt.foo](https://www.prompt.foo/) | Prompt engineering training app — build, refine, and master prompts |
| [nextish.news](https://www.nextish.news/) | Turn any tech premise into a polished satirical news article |

## License

MIT
