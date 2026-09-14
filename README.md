# UI Screenshot Redesign Skill

[![skills.sh compatible](https://img.shields.io/badge/skills.sh-compatible-111111)](https://skills.sh)

A single, opinionated Agent Skill for redesigning existing web apps, dashboards, SaaS interfaces, landing pages, websites, mobile apps, and individual UI components from screenshots with image-generation models.

> **One output image = one complete redesign.**

## Install

Install with skills.sh:

```bash
npx skills add matteolaureti/ui-redesign-skills
```

The repository exposes one installable skill:

```text
redesign-ui-from-screenshots
```

To update later:

```bash
npx skills update redesign-ui-from-screenshots
```

## Why this exists

Screenshot-based UI redesign often fails in predictable ways:

- the result is only a recolor of the original;
- multiple concepts are packed into one image;
- important functionality disappears for aesthetics;
- dashboards become generic AI/Dribbble concepts;
- mobile apps look like narrow websites;
- different requested alternatives reuse the same design language;
- layouts change, but the product still looks visually too close to the source.

This skill keeps the redesign logic in **one monolithic `SKILL.md`** so the image model receives the complete design judgment in one place: product analysis, visual audit, layout, typography, surfaces, components, anti-AI-slop rules, dashboard guidance, landing-page guidance, multi-direction rules, image fidelity, brand handling, accessibility, and final quality checks.

## Repository structure

```text
ui-redesign-skills/
├── README.md
├── INSTALL.md
├── LICENSE
├── CONTRIBUTING.md
├── docs/
│   └── references.md
├── examples/
│   └── prompts.md
└── skills/
    └── redesign-ui-from-screenshots/
        └── SKILL.md
```

## What the skill does

The screenshot is treated as a **functional, content, and product-context reference**, not as a layout that must be copied.

The skill can rethink:

- global composition;
- navigation architecture;
- hierarchy;
- grid and alignment;
- card structure;
- spacing;
- typography;
- surface treatment;
- density;
- component presentation;
- metrics, filters, tables and charts;
- visual language and supporting imagery.

At the same time, it preserves the product's purpose, important content, functionality, and recognizable identity unless the user explicitly asks for something more radical.

## Multiple redesigns

When several concepts are requested, every concept must be generated as a **separate full-size output image**.

For example, asking for 8 redesigns should produce:

```text
Image 1 → redesign A
Image 2 → redesign B
Image 3 → redesign C
...
Image 8 → redesign H
```

Never one image containing eight miniature concepts unless a comparison board is explicitly requested.

## Example prompt

Attach a dashboard screenshot and ask:

> Use $redesign-ui-from-screenshots to completely redesign this dashboard. Preserve its purpose and important functionality, but rethink the layout, hierarchy, navigation, typography, surfaces and visual language. Create 8 genuinely different redesigns as 8 separate full-size output images.

## Design philosophy

The skill is intentionally opinionated about recurring generated-UI problems: generic card grids, unnecessary pills, purple-blue AI gradients, excessive glass, weak typography, decorative analytics, fake futuristic styling, repeated layouts, and presentation-first concepts that do not feel like real software.

The goal is not merely to make the screenshot prettier. The goal is to make the same product communicate more clearly and feel plausibly shippable by a strong product-design team.

## References

See [docs/references.md](docs/references.md).

## License

MIT.
