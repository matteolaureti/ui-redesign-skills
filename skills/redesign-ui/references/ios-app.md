# iOS app redesign guidance

Use this guidance for iPhone and iPad application screenshots.

## Platform fit

Make the redesign feel intentionally designed for iOS or iPadOS rather than like a responsive website placed inside a device.

Preserve the product's own identity while using platform-familiar hierarchy and interaction patterns.

## Layout and typography

Respect safe areas and keep important content clear of system-reserved regions.

Use readable typography and layouts that could plausibly adapt to larger text. Avoid brittle horizontal arrangements and tiny labels that would fail with Dynamic Type.

Do not simply scale an iPhone layout up for iPad. Larger screens may benefit from sidebars, split views, or persistent context when appropriate.

## Navigation

Choose navigation according to information architecture:

- navigation hierarchy and back behavior for drill-down flows;
- tabs for meaningful top-level destinations;
- search when it is a primary retrieval mechanism;
- split navigation where larger layouts benefit from persistent context.

Do not add a tab bar just because the interface is mobile.

Keep toolbars focused on important contextual actions. Lower-priority actions can move into secondary menus when appropriate.

Use sheets and modality for temporary focused tasks rather than ordinary navigation.

## Controls and touch

Favor native-feeling touch controls and adequate spacing. Avoid desktop dropdowns, hover-dependent interactions, tiny web checkboxes, dense desktop toolbars, and web tables squeezed into a phone viewport.

Use progressive disclosure when all desktop-level information cannot remain visible at once; preserve meaning through drill-down rather than simply deleting useful content.

## Avoid

Avoid excessive cards, gratuitous translucency, copying Apple apps without regard for the product brand, or treating "native iOS" as a visual effect.

The result should look plausible as a real app screen and remain easy to operate by touch.
