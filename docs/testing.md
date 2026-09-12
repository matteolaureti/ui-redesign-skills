# Testing the redesign-ui skill

This test plan is designed for the current single-skill, progressively disclosed architecture.

The goal is not to test combinations of separate skills. The goal is to verify that `redesign-ui` triggers correctly, routes to the right reference, preserves scope, and produces compliant image outputs.

## Test references

Use four representative screenshots:

- **R1 — Dashboard:** desktop SaaS/admin/analytics interface with navigation, metrics, data and actions.
- **R2 — Landing page:** real product landing page with hero, product content and conversion elements.
- **R3 — iOS:** real iPhone or iPad application screen with meaningful navigation and controls.
- **R4 — Component:** one localized UI component such as a card, table, pricing block, modal, FAQ or panel. This can be cropped from R1 or R2.

Prefer real product screenshots over Dribbble-style concept art. Keep text reasonably readable.

## Test 1 — Explicit dashboard invocation

Reference: R1

```text
Use $redesign-ui to completely redesign the attached dashboard.

Preserve its product purpose, important information, controls and actions, but rethink the hierarchy, layout, navigation, density, typography and component structure where useful.

Generate exactly one complete redesign image.
```

Expected routing: `references/dashboard.md`.

Verify:

- the dashboard remains recognizable as the same product;
- the redesign is deeper than a recolor;
- information density remains appropriate;
- only one redesign appears in the output image.

## Test 2 — Implicit dashboard routing

Reference: R1

Do not name the skill.

```text
Completely redesign this dashboard.
Keep its purpose and important functionality, but make it significantly better in terms of usability, hierarchy, layout and visual design.
Create one complete redesign image.
```

Expected behavior: the skill should be discovered from its description and route to `references/dashboard.md`.

Compare against Test 1. A large quality drop can indicate discovery or routing problems rather than weak dashboard guidance.

## Test 3 — Multiple dashboard directions

Reference: R1

```text
Use $redesign-ui to create 4 genuinely different redesign directions for the attached dashboard.

Preserve the same product purpose and important functionality across all concepts, but vary the global composition, navigation, hierarchy, density, grouping and component architecture.

Generate 4 separate full-size output images.
Each image must contain exactly one redesign.
```

Expected routing:

- `references/dashboard.md`
- `references/multiple-directions.md`

Verify:

- four separate images are produced;
- no contact sheet or multi-concept canvas appears;
- differences are structural, not merely palette changes;
- product meaning remains stable across concepts.

## Test 4 — Landing page routing

Reference: R2

```text
Use $redesign-ui to completely redesign the attached landing page.

Keep the product and brand recognizable, but rethink the narrative, hero, product presentation, section rhythm, proof and conversion hierarchy.
Avoid generic SaaS landing-page patterns.

Generate exactly one redesign image.
```

Expected routing: `references/landing-page.md`.

Verify that the result does not fall into a generic hero → logo strip → three cards → bento → testimonials → pricing → FAQ template unless the source genuinely supports it.

## Test 5 — iOS routing

Reference: R3

```text
Use $redesign-ui to redesign the attached iPhone screen as a polished native-feeling iOS experience.

Preserve the task and important content, but rethink navigation, hierarchy and controls where useful.
Do not make it look like a mobile website.

Generate exactly one redesign image.
```

Expected routing: `references/ios-app.md`.

Verify:

- safe-area-aware composition;
- touch-friendly controls;
- native-feeling navigation and hierarchy;
- no desktop UI compressed into a phone.

## Test 6 — Component scope control

Reference: R4

```text
Use $redesign-ui to redesign only the target component in the attached screenshot.

Improve its information hierarchy, structure and visual treatment while keeping it compatible with the surrounding product.
Do not redesign the whole page.

Generate exactly one component redesign image.
```

Expected routing: `references/component.md`.

Verify that the surrounding product remains context rather than becoming a new full-page redesign.

## Test 7 — Trigger boundary: coding request

Use any UI screenshot.

```text
Implement this interface in React and match the screenshot as closely as possible.
```

Expected behavior: `redesign-ui` should not be the governing skill because the request is code implementation / screenshot reproduction rather than visual redesign image generation.

This test is important for Codex and Astra usage.

## Evaluation rubric

Score each visual redesign from 0–5 on:

1. **Functional preservation** — important product meaning survives.
2. **Redesign depth** — meaningful redesign rather than recolor.
3. **Hierarchy** — primary information and actions are clear.
4. **Product realism** — plausible production software.
5. **Visual quality** — composition, typography, spacing and surfaces.
6. **Anti-AI-slop** — avoids generic generated-UI fingerprints.
7. **Scope compliance** — follows the requested redesign scope.
8. **Output compliance** — one redesign per image, correct device category.

For multi-direction tests add:

9. **Concept diversity** — variants differ structurally rather than cosmetically.

## Recommended test order

Start with R1 and run Tests 1, 2 and 3 first. Those establish whether explicit invocation, implicit discovery, dashboard routing and multi-direction routing all work.

Then test R2, R3 and R4.

Change the skill only after comparing repeated results across the same reference screenshot. Prefer evidence-driven edits over adding more generic instructions.