---
name: redesign-ui
description: Redesign existing UI screenshots into new image-generation concepts. Use for visual redesigns of dashboards, landing pages, web apps, iOS screens, or individual UI components; not for code implementation or pixel-perfect cloning.
---

# Redesign UI

Use the supplied UI screenshot as the functional and visual reference, then produce a stronger redesign as image output.

## Guidance loading

For every redesign task, read `references/design-principles.md` first. It contains the shared art-direction rules that apply across product types.

Then read only the additional domain references needed for the task:

- Dashboard, admin, analytics, CRM, or operational workspace: `references/dashboard.md`.
- Marketing site or landing page: `references/landing-page.md`.
- iPhone or iPad application: `references/ios-app.md`.
- One localized card, table, modal, FAQ, pricing block, panel, or section: `references/component.md`.
- Multiple redesign directions or variants: also `references/multiple-directions.md`.

Do not load irrelevant domain references.

## Core behavior

1. Inspect the screenshot and infer the product purpose, primary user goal, critical information and actions, brand cues, and device category.
2. Preserve product meaning and important functionality unless the task explicitly calls for rethinking them.
3. Treat the current layout as a reference, not a constraint. Rebuild hierarchy, composition, grouping, typography, surfaces, and component structure when that improves the design.
4. Apply the universal design principles before the domain-specific guidance.
5. Use image generation or image editing to create the redesign.
6. Keep the output in the same general device category and show the interface itself rather than a device mockup unless requested otherwise.
7. Preserve readable product text and realistic data when practical. Do not invent unrelated functionality merely to make the image look richer.

## Output invariant

**One output image = one redesign.**

If multiple redesigns are requested, generate separate full-size output images. Never combine alternatives into a contact sheet, concept grid, split-screen comparison, moodboard, or set of miniature interfaces unless that format is explicitly requested.

## Autonomy

Infer routine design decisions from the screenshot and task. Avoid asking for clarification when a reasonable design assumption is reversible and does not materially change the requested outcome.

## Definition of done

Before finishing, verify that:

- the requested image output was actually produced;
- each output image contains exactly one redesign;
- the product purpose and important information remain understandable;
- the redesign is meaningfully stronger than a recolor;
- the relevant domain guidance was applied;
- the result passes the final art-direction and anti-AI-slop checks in `references/design-principles.md`;
- the result looks like plausible software rather than a presentation board or generic AI concept.
