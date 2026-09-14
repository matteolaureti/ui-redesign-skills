# Skill architecture

## Goal

Keep discovery cheap and precise while preserving strong art direction.

The skill uses progressive disclosure, but it does not make the universal design guidance shallow. Every redesign loads a shared design brain first, then only the domain guidance that changes the current task.

## Structure

```text
skills/redesign-ui/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── design-principles.md
    ├── dashboard.md
    ├── landing-page.md
    ├── ios-app.md
    ├── component.md
    └── multiple-directions.md
```

## Why a single routed skill?

GPT-6 Astra follows contextual instructions very closely. Current OpenAI guidance favors precise skill discovery and progressive disclosure for skills that support multiple workflows.

A previous version of this repository exposed separate core, dashboard, landing-page, iOS, component, and direction-explorer skills. That required the agent to discover and combine several overlapping descriptions.

The current architecture exposes one trigger: visual UI redesign from screenshots. After `redesign-ui` triggers, its root document routes internally.

This reduces:

- competing descriptions in discovery context;
- duplicated rules;
- accidental loading of irrelevant guidance;
- dependence on the agent selecting several skills in the correct combination.

## Two-stage guidance loading

### Stage 1 — Universal design brain

Every redesign loads:

```text
references/design-principles.md
```

This preserves the strong, opinionated art direction needed for image generation: typography, hierarchy, layout, surfaces, component choices, realism, brand handling, accessibility, and anti-AI-slop review.

### Stage 2 — Conditional domain guidance

Only the relevant additional references are loaded:

- dashboard/admin/analytics → `dashboard.md`;
- landing/marketing → `landing-page.md`;
- iOS/iPadOS → `ios-app.md`;
- localized component → `component.md`;
- multiple concepts → additionally `multiple-directions.md`.

The agent should not bulk-load unrelated domain references.

## Why the universal design brain matters

Progressive disclosure should reduce irrelevant context, not remove useful expertise.

A very small generic root can leave an image model free to fall back to common generated-UI patterns. `design-principles.md` restores concrete design judgment while keeping discovery simple and domain references modular.

The intended model is:

```text
one installable skill
+ strong universal design judgment
+ conditional domain expertise
```

## Degrees of freedom

The skill constrains outcomes that materially matter — product meaning, scope, image composition, realism, and one-redesign-per-image — while leaving actual visual problem-solving relatively high freedom.

It avoids prescribing one house style or forcing every product through the same layout recipe.

## Trigger boundary

The skill is for generating visual redesign concepts from UI screenshots.

It should not govern ordinary code implementation, pixel-perfect screenshot cloning, or unrelated image editing. This keeps an image-design skill from influencing normal frontend coding tasks merely because a screenshot is present.

## Output invariant

> **ONE OUTPUT IMAGE = ONE REDESIGN.**

Multiple concepts are multiple outputs unless a combined comparison format is explicitly requested.
