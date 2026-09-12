---
name: redesign-ui
description: Redesign existing UI screenshots into new image-generation concepts. Use for visual redesigns of dashboards, landing pages, web apps, iOS screens, or individual UI components; not for code implementation or pixel-perfect cloning.
---

# Redesign UI

Use the supplied UI screenshot as the functional and visual reference, then produce a stronger redesign as image output.

The user's explicit instructions take precedence over this skill. Apply only the guidance that is relevant to the requested redesign.

## Route to the relevant guidance

Read only the reference files needed for the current task:

- Dashboard, admin, analytics, CRM, or operational workspace: read `references/dashboard.md`.
- Marketing site or landing page: read `references/landing-page.md`.
- iPhone or iPad application: read `references/ios-app.md`.
- One localized card, table, modal, FAQ, pricing block, panel, or section: read `references/component.md`.
- Multiple redesign directions or variants: also read `references/multiple-directions.md`.

Do not load every reference by default.

## Core behavior

1. Inspect the screenshot and infer the product purpose, primary user goal, critical information and actions, brand cues, and device category.
2. Preserve product meaning and important functionality unless the user explicitly asks to rethink them.
3. Treat the current layout as a reference, not a constraint. Rebuild hierarchy, composition, grouping, typography, surfaces, and component structure when that improves the design.
4. Use the available image-generation or image-editing capability to create the redesign. Do not substitute implementation code unless the user asks for code.
5. Keep the output in the same general device category and show the interface itself rather than a device mockup unless the user requests otherwise.
6. Preserve readable product text and realistic data when practical. Do not invent unrelated functionality merely to make the image look richer.

## Output invariant

**One output image = one redesign.**

If the user requests multiple redesigns, generate separate full-size output images. Never combine alternatives into a contact sheet, concept grid, split-screen comparison, moodboard, or set of miniature interfaces unless the user explicitly asks for that format.

## Design quality

Favor clear hierarchy, deliberate composition, realistic information density, coherent typography, restrained surfaces, and plausible production UI.

Avoid default AI-design fingerprints such as gratuitous purple-blue gradients, excessive glass, random glow, meaningless charts, repeated equal cards, excessive pills, giant radii, decorative floating panels, and visual effects that do not support the product.

Do not remove useful information simply to make an operational interface look minimal. Do not preserve a weak layout simply because it appears in the reference.

## Autonomy

Infer routine design decisions from the screenshot and the user's request. Do not ask for clarification when a reasonable design assumption is reversible and does not materially change the requested outcome.

## Definition of done

Before finishing, verify that:

- the requested image output was actually produced;
- each output image contains exactly one redesign;
- the product purpose and important information remain understandable;
- the redesign is meaningfully stronger than a recolor;
- the result looks like plausible software rather than a presentation board or generic AI concept.
