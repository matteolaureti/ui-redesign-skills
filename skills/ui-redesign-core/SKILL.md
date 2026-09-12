---
name: ui-redesign-core
description: Redesigns an existing website, web app, dashboard, landing page, mobile app, or product UI from one or more reference screenshots. Preserves product meaning and important functionality while improving hierarchy, layout, typography, surfaces, components, and visual quality. Use for screenshot-led UI redesign. Every generated output image must contain exactly one redesign.
---

# UI Redesign Core

## Job to be done

Transform an existing UI screenshot into a substantially stronger, realistic product-design concept.

Treat the screenshot as a:

- functional reference;
- content reference;
- product-context reference;

not as a layout template that must be copied.

The redesign should feel like the same product designed by a stronger product-design team.

## Required inputs

Usually expect:

- at least one UI screenshot;
- an explicit or inferable redesign target;
- any constraints supplied by the user.

If the screenshot contains enough information to proceed, do not stop merely because every product detail is not known. Make conservative assumptions and preserve visible meaning.

## Mandatory output invariant

**ONE OUTPUT IMAGE = ONE REDESIGN.**

Every generated image must contain exactly one complete redesign concept.

If the user asks for 2, 4, 8 or more redesigns, produce that many separate output images.

Never pack multiple redesigns into one canvas unless the user explicitly asks for a contact sheet, comparison board, or multi-concept image.

Do not create:

- grids of redesigns;
- side-by-side alternatives;
- multiple browser windows containing different concepts;
- before/after comparisons;
- concept thumbnails;
- moodboards containing several UI solutions.

Use the available canvas for one readable redesign.

## Workflow

### 1. Identify the product

Determine:

- product type;
- device category;
- main user goal;
- primary action;
- navigation model;
- information density;
- brand cues.

### 2. Extract the information architecture

Identify:

- primary navigation;
- secondary navigation;
- title/context;
- main actions;
- main data;
- supporting data;
- controls;
- filters;
- status;
- warnings;
- activity;
- help;
- metadata.

Separate essential information from visual noise.

### 3. Determine redesign intensity

Interpret the user's wording.

#### Improve / polish

Remain relatively close to the existing composition.

#### Redesign

Meaningfully reconsider hierarchy, layout, typography and component language.

#### Complete redesign

Use the screenshot primarily as functional and informational input. Rebuild the visual composition when useful.

#### Explore different directions

Create structurally different concepts as separate image outputs.

### 4. Preserve product meaning

Unless the user explicitly asks to rethink functionality, preserve recognizable equivalents of critical:

- actions;
- statuses;
- metrics;
- filters;
- controls;
- navigation;
- progress;
- warnings;
- account/device/plan information;
- meaningful metadata.

Preserve information, not necessarily the original component.

Five metric cards can become one data strip.
A sidebar can become top navigation.
A list can become a timeline.
A collection of cards can become one integrated workspace.

### 5. Rebuild hierarchy

A user should quickly understand:

1. where they are;
2. the current state;
3. what matters most;
4. what they can do;
5. what supporting information exists.

Do not give everything equal visual weight.

### 6. Choose layout before styling

Do not begin by changing colors.

Decide:

- global composition;
- density;
- grouping;
- navigation placement;
- primary/secondary regions;
- alignment;
- whitespace.

Avoid automatically copying the reference grid.

### 7. Redesign typography

Avoid:

- weak hierarchy;
- oversized headings in operational UI;
- excessive bold;
- tiny gray labels;
- all-uppercase labels everywhere;
- poorly aligned data;
- generic typography with no deliberate treatment.

Use:

- clear type scale;
- purposeful weight;
- readable line-height;
- tabular-looking numeric treatment for data;
- stronger contrast between label, value and metadata.

Typography should look designed rather than merely formatted.

### 8. Redesign surfaces

Avoid default AI aesthetics:

- purple-blue gradients;
- neon violet glow;
- random cyan accents;
- excessive glass;
- glowing borders;
- every section inside a card;
- excessive shadows;
- enormous radii;
- generic gray SaaS surfaces.

Prefer:

- one controlled accent;
- coherent neutral family;
- deliberate elevation;
- tonal grouping;
- restrained shadows;
- surfaces only when hierarchy requires them.

Not every group needs a border, shadow and radius.

### 9. Redesign components

Do not default to:

- icon in colored rounded square;
- title;
- description;
- button;
- all contained in identical cards.

Consider:

- rows;
- grouped surfaces;
- whitespace;
- timelines;
- data strips;
- tables;
- split panels;
- contextual rails;
- inline metrics;
- progressive disclosure.

Do not turn every status into a colorful pill.

### 10. Remove AI slop

Avoid:

- gratuitous gradients;
- floating decorative cards;
- meaningless charts;
- symmetric three-card layouts by default;
- arbitrary bento grids;
- excessive pills;
- generic futuristic decoration;
- giant hero text with little product content;
- fake decorative data;
- UI that looks like a Dribbble concept rather than usable software.

### 11. Preserve realistic content

Retain readable text from the screenshot when useful.

Do not replace meaningful interface content with:

- Lorem Ipsum;
- nonsense labels;
- random strings;
- generic fake metrics.

If new microcopy is needed, keep it concise and product-specific.

### 12. Respect the viewport

Infer:

- desktop;
- tablet;
- mobile;
- approximate aspect ratio.

Stay within the same device category unless asked otherwise.

Generate the interface itself.

Do not place it inside:

- laptop mockups;
- phone mockups;
- 3D devices;
- perspective scenes;

unless the user asks.

### 13. Preserve brand intentionally

Usually preserve:

- logo;
- product name;
- recognizable brand color;
- meaningful brand motifs.

Do not randomly rebrand the product.

If identity is weak or unspecified, establish a coherent visual system without inventing an unrelated brand.

### 14. Keep accessibility visually plausible

Maintain:

- readable contrast;
- clear hierarchy;
- understandable states;
- sufficient control size;
- non-color-only status communication where feasible.

Do not make text low-contrast simply to appear minimal.

## Final quality check

Before finalizing each image, verify:

### Product

- Is the page purpose still obvious?
- Are critical capabilities preserved?
- Are actions understandable?

### Hierarchy

- Is there one clear focal structure?
- Are primary and secondary information distinct?
- Is the page easy to scan?

### Layout

- Is the composition deliberate?
- Is whitespace intentional?
- Is density appropriate for the product?

### Visual language

- Is there one coherent system?
- Are surfaces necessary?
- Is the accent controlled?
- Is the UI realistic enough to ship?

### Anti-slop

- Too many cards?
- Too many pills?
- Generic gradient?
- Random glass?
- Meaningless decorative charts?
- Suspiciously generic SaaS composition?

### Output

- Does this output image contain exactly one redesign?
- Is that redesign large enough to evaluate?
- Did any secondary concept, contact sheet or comparison accidentally appear?

If more than one redesign appears, the output is invalid. Recompose it as one redesign only.

## Hard rules

- One output image must contain exactly one redesign.
- Multiple requested redesigns require separate image outputs.
- Do not merely recolor the screenshot.
- Do not preserve a weak layout only because it exists.
- Do not remove important product functionality for aesthetics.
- Do not invent unrelated product capabilities.
- Do not put every piece of information inside a card.
- Do not overuse pills, gradients, glass or rounded rectangles.
- Do not confuse minimalism with removing useful information.
- Do not create device mockups unless requested.
- Do not make the interface less usable to make it more dramatic.
