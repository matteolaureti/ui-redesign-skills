# Universal design principles

Read this reference for every redesign task. It contains the shared art-direction rules that should shape the result before any domain-specific guidance is applied.

The goal is not to make the screenshot merely prettier. The goal is to make the same product communicate more clearly, feel more intentional, and look plausibly shippable by a strong product-design team.

## Start from product meaning

Treat the screenshot as a functional, informational, and brand reference — not as a layout that must survive.

Preserve important actions, statuses, metrics, controls, navigation, warnings, progress, account/device/plan information, and meaningful metadata unless the user explicitly asks to rethink them.

Preserve the information, not necessarily the component. Five metric cards can become one data strip. A sidebar can become top navigation. A list can become a timeline. A set of boxed widgets can become one integrated workspace.

A redesign that removes useful product meaning for aesthetics is a failure.

## Hierarchy before decoration

Before changing colors, decide:

- what the user must understand first;
- what the primary action is;
- what information is secondary;
- what belongs together;
- what can be visually quieter;
- what deserves persistent visibility.

The interface should make it obvious:

1. where the user is;
2. what the current state is;
3. what matters most;
4. what they can do;
5. what supporting information exists.

Do not give every element equal visual emphasis.

## Typography

Typography should feel deliberately designed, not simply formatted.

Avoid:

- browser-default-looking typography;
- Inter used with no character or hierarchy simply because it is common in SaaS UI;
- headings that barely differ from body text;
- oversized dashboard headings that waste operational space;
- excessive bold text;
- only Regular and Bold weights;
- tiny low-contrast labels;
- all-uppercase section labels everywhere;
- poor line-height or cramped copy;
- proportional-looking data columns where numeric comparison matters.

Prefer:

- a clear type scale;
- Medium/Semibold hierarchy rather than binary regular/bold treatment;
- tighter tracking on large display text when appropriate;
- restrained positive tracking for small labels when useful;
- readable body measure and line-height;
- tabular-looking number treatment for metrics and financial/data-heavy UI;
- sentence case by default;
- optical rather than purely mathematical alignment.

Large text should earn its space. Small text must remain readable.

## Color and surfaces

Use one coherent visual system.

Avoid default AI fingerprints:

- purple-to-blue gradients;
- random cyan/violet accents;
- neon glow;
- excessive glassmorphism;
- glowing card borders;
- multiple unrelated accent colors;
- pure black backgrounds with no tonal nuance;
- generic black shadows on every element;
- every section inside a white card with border + shadow + large radius;
- identical corner radius on everything.

Prefer:

- one considered accent color;
- a coherent warm or cool neutral family;
- tonal grouping before borders;
- restrained elevation;
- shadows that feel consistent with the surrounding palette and one light direction;
- subtle depth, texture, grain, ambient gradient, or imagery only when it strengthens the product;
- tighter radii on inner controls and softer radii on larger containers when appropriate.

Not every group needs a container. Not every container needs a border, radius, and shadow.

## Layout and composition

Do not preserve weak composition just because it exists in the reference.

Avoid automatic patterns such as:

- everything centered and symmetrical;
- three equal cards as the default feature row;
- a left sidebar on every dashboard;
- equal-height cards forced despite different content;
- mathematically identical spacing everywhere;
- every module floating independently;
- excessive nested cards;
- huge unused areas in operational interfaces;
- dense marketing layouts with no breathing room.

Consider when appropriate:

- asymmetry;
- offset alignment;
- mixed aspect ratios;
- integrated surfaces;
- split layouts;
- master-detail structures;
- contextual rails;
- top navigation;
- variable-height content;
- controlled overlap or depth;
- stronger whitespace around the true focal point.

Use whitespace intentionally. Marketing pages can breathe aggressively; operational products should preserve useful density.

Shared elements in side-by-side groups should align optically: titles, values, prices, buttons, baselines, and list starts.

## Components

Do not accept a component type merely because it appears in the source.

Question whether the information actually needs a card, modal, badge, accordion, carousel, or separate widget.

Avoid generic component recipes such as:

- icon in a colored rounded square + title + paragraph + button;
- one filled button and one ghost button everywhere;
- colorful pill badges for every state;
- avatar circles by default;
- FAQ accordion by default;
- three pricing towers with one slightly taller;
- modal dialogs for simple inline edits;
- cards that exist only to create visual separation.

Possible alternatives include:

- structured rows;
- integrated grouped surfaces;
- whitespace and dividers;
- timelines;
- data strips;
- tables;
- inline metrics;
- split panels;
- contextual rails;
- expandable regions;
- text links or tertiary actions;
- subtle dot/icon/text status treatment.

Component choice should improve comprehension or interaction, not just make the page look designed.

## Navigation

Navigation should reflect product structure, not fashion.

A left sidebar is one option, not the universal answer.

Consider when appropriate:

- top navigation;
- compact side rail;
- contextual secondary navigation;
- tabs;
- breadcrumbs;
- master-detail navigation;
- command-oriented controls.

The current destination must be visually understandable. Primary navigation should not compete with page-level actions.

## Realistic content and data

Preserve readable product copy from the reference where practical.

Avoid:

- Lorem Ipsum;
- nonsense labels;
- generic fake company names;
- suspiciously round fake metrics;
- repeated avatars;
- invented testimonials, logos, certifications, or proof;
- charts containing arbitrary data with no product meaning.

When new content is necessary, make it concise, believable, and specific to the product.

Avoid generic AI-copy phrases such as “Elevate”, “Seamless”, “Unleash”, “Next-Gen”, “Game-changing”, “Unlock the power of”, and similar filler.

## Image realism

The result should look like a real software screenshot, not concept art.

Aim for:

- crisp geometry;
- consistent spacing;
- straight UI edges;
- plausible control dimensions;
- coherent iconography;
- readable text placement;
- aligned tables and values;
- consistent component logic;
- realistic information density.

Avoid warped panels, curved browser windows, duplicated controls, impossible geometry, random microtext, distorted icons, and perspective presentation unless explicitly requested.

Generate the interface itself rather than placing it inside a laptop, phone mockup, 3D device, or floating browser scene unless the user asks for one.

## Brand handling

Preserve recognizable brand elements when they are intentional:

- logo;
- product name;
- distinctive brand color;
- meaningful visual motifs.

Do not randomly rebrand an existing product. If the brand system is weak or underspecified, strengthen coherence without inventing an unrelated identity.

## Accessibility-aware visual design

Even static concepts should suggest implementable, accessible UI.

Maintain:

- readable contrast;
- sufficiently large text;
- understandable interactive affordances;
- visible state differences;
- touch-friendly controls on mobile;
- status meaning that does not rely only on color.

Do not use low-contrast gray text simply because it looks minimal.

## AI-slop audit

Before finalizing, ask whether the result could plausibly be one of hundreds of interchangeable AI-generated UI concepts.

If yes, revise it.

Common warning signs:

- purple/blue gradient as default personality;
- random glowing blobs;
- excessive glass;
- arbitrary bento grids;
- excessive rounded rectangles;
- giant radii;
- decorative charts;
- identical cards everywhere;
- meaningless floating panels;
- pill overload;
- huge hero copy that displaces useful product information;
- excessive empty space in data-heavy software;
- a composition that looks like Dribbble rather than a real product.

Distinctiveness should come from product-specific hierarchy, composition, brand, and component decisions — not decoration for its own sake.

## Final art-direction check

Before producing the image, verify:

- the product purpose is still obvious;
- important functionality is represented;
- the redesign is materially deeper than a recolor;
- hierarchy is stronger than the reference;
- typography and spacing are intentional;
- surfaces and cards are used only where helpful;
- the layout is not generic by default;
- the result looks implementable;
- the design has one coherent visual system;
- each output image contains exactly one redesign.
