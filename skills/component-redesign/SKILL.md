---
name: component-redesign
description: Redesigns a single UI component or localized interface section from a screenshot, such as a card, table, pricing block, FAQ, navigation element, modal, panel, form, widget, or dashboard module. Focuses on the target component without unnecessarily redesigning the surrounding product. Each output image must contain exactly one component redesign concept.
---

# Component Redesign

## Job to be done

Improve one specific component or localized section while respecting its surrounding product context.

This skill is for cases where the user does **not** want an entire page redesign.

## Mandatory output rule

**ONE OUTPUT IMAGE = ONE COMPONENT REDESIGN.**

If the user requests eight alternatives for one card, produce eight separate images.

Never create a grid containing all eight card alternatives unless explicitly requested.

## Workflow

### 1. Identify the exact target

Determine what is being redesigned:

- card;
- table;
- header;
- navigation;
- modal;
- FAQ;
- pricing module;
- settings panel;
- status widget;
- chart region;
- form;
- timeline;
- empty state;
- other section.

Do not expand the scope without reason.

### 2. Understand its job

Identify:

- what information it communicates;
- what action it enables;
- how often it is used;
- whether it is primary or supporting;
- what surrounding UI constrains it.

### 3. Preserve necessary context

Use enough surrounding context to make the redesign believable.

Do not generate an entirely new application around a small component.

If the reference shows the component inside a page, the output may show limited context, but visual attention should remain on the target.

### 4. Reconsider the component model

Do not assume the same component type must survive.

Examples:

- a card can become a structured row;
- an FAQ accordion can become categorized Q&A;
- a pricing card can become comparison-driven layout;
- a widget can become an inline summary;
- a modal can become an expandable section.

Preserve the job, not necessarily the original box.

### 5. Improve micro-hierarchy

Focus on:

- title/value relationship;
- metadata;
- status;
- action placement;
- label contrast;
- spacing;
- alignment;
- grouping;
- icon usefulness.

### 6. Match the surrounding design system

Unless the user asks for a new global direction, keep the component plausible within the existing product.

Do not introduce a radically unrelated palette or typography for one module.

### 7. Avoid component AI slop

Avoid:

- icon in colored square by default;
- excessive border/shadow/radius;
- unnecessary gradient;
- decorative mini-chart;
- multiple pills;
- giant empty padding;
- arbitrary glassmorphism.

## When exploring alternatives

Each separate output should change meaningful decisions, such as:

- information hierarchy;
- component architecture;
- action placement;
- density;
- visual emphasis;
- disclosure model.

Color-only changes are not distinct concepts.

## Final checks

- Did only the intended component meaningfully change?
- Is its purpose clearer?
- Are important actions easier to find?
- Does it fit the product context?
- Is the concept structurally meaningful rather than a recolor?
- Does the output contain exactly one redesign concept?
