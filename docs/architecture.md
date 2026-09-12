# Skill architecture

## Goal

Keep discovery cheap and precise, then load only the redesign guidance that changes the current task.

## Structure

```text
skills/redesign-ui/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── dashboard.md
    ├── landing-page.md
    ├── ios-app.md
    ├── component.md
    └── multiple-directions.md
```

## Why a single routed skill?

GPT-6 Astra follows contextual instructions very closely. Current OpenAI guidance recommends short, precise skill descriptions and progressive disclosure for skills that support multiple workflows.

A previous version of this repository exposed separate core, dashboard, landing-page, iOS, component, and direction-explorer skills. That required an agent to discover and combine overlapping skill descriptions.

The current architecture instead exposes one precise trigger: visual UI redesign from screenshots. After `redesign-ui` triggers, its root document acts as a small router.

This reduces:

- competing descriptions in always-on discovery context;
- duplicated rules;
- accidental loading of irrelevant guidance;
- dependence on the agent selecting several skills in the right combination.

## Progressive disclosure

`SKILL.md` contains only the invariants and routing logic needed for every redesign.

Domain-specific guidance lives one level deep in `references/` and is loaded conditionally:

- dashboard/admin/analytics → `dashboard.md`;
- landing/marketing → `landing-page.md`;
- iOS/iPadOS → `ios-app.md`;
- localized component → `component.md`;
- multiple concepts → additionally `multiple-directions.md`.

The agent should not bulk-load every reference.

## Degrees of freedom

The skill constrains outcomes that matter — product meaning, output format, scope, and one-redesign-per-image — while leaving visual problem-solving relatively high freedom.

It intentionally avoids a long design recipe. Astra can infer many intermediate design decisions from the screenshot and user request.

## User precedence

The user's explicit instructions override skill guidance. The skill should not block or reinterpret a clear user request merely because a default heuristic differs.

## Trigger boundary

The skill is for generating visual redesign concepts from UI screenshots.

It should not trigger for ordinary code implementation, pixel-perfect screenshot cloning, or unrelated image editing. This prevents a UI image-design skill from influencing normal coding tasks simply because they happen to involve frontend files.

## Output invariant

> **ONE OUTPUT IMAGE = ONE REDESIGN.**

Multiple concepts are multiple outputs unless the user explicitly requests a combined comparison format.
