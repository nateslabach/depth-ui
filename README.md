# depth-ui

An agent skill for applying depth-driven layered color and shadow principles to produce polished, readable UIs in both light and dark themes.

## Install

```bash
npx skills add https://github.com/nateslabach/depth-ui --skill depth-ui
```

## What it does

Teaches your agent to improve UI quality by:

- Building a 3–4 layer color hierarchy (base → mid → top) using small OKLCH lightness deltas
- Composing two-part shadows: a soft inset top highlight + a darker outer bottom shadow
- Setting up token-based theming with light/dark parity
- Knowing when to elevate, when to sink, and when to leave things flat
- Maintaining WCAG AA contrast through layering changes

## When to use

- Reviewing or improving a UI component or page
- Setting up a design token system from scratch
- Making a flat or inconsistent UI feel more refined without a full redesign
- Auditing depth and shadow consistency across a design system

## Structure

```
depth-ui/
└── SKILL.md
```

## License

MIT
