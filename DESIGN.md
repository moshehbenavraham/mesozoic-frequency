# Design

## Style overview

A single-page brand experience called **Mesozoic Frequency**. The scene is a nocturnal natural-history archive after closing: blue-black air, pale fossil marks, scanner-light cyan, mineral amber, and a few volcanic rust details. It should feel immersive and art-directed, not like a classroom worksheet.

## Color system

Use OKLCH values only in CSS.

- Background: `oklch(0.105 0.018 218)` — deep blue-black museum dark.
- Surface: `oklch(0.165 0.023 218)` — raised basalt panels.
- Surface 2: `oklch(0.225 0.030 214)` — specimen wells and overlays.
- Ink: `oklch(0.930 0.018 205)` — readable fossil-white text.
- Muted: `oklch(0.730 0.040 205)` — cool secondary text.
- Primary: `oklch(0.720 0.090 200)` — scanner blue, anchored to the generated seed hue.
- Accent: `oklch(0.760 0.135 74)` — amber resin signal.
- Rust: `oklch(0.600 0.145 39)` — volcanic sediment and warning moments.
- Bone: `oklch(0.870 0.035 88)` — fossil drawings.

Strategy: drenched/committed hybrid. The page surface is dark and atmospheric; primary color appears as light/scanner interaction, not decoration.

## Typography

- Display: `Unbounded` for structural headings. Angular, fossil-plate/space-agency quality.
- Body: `Atkinson Hyperlegible` for clarity and accessibility.
- Mono/labels: `Chivo Mono` for era readouts and specimen metadata.

Avoid serif-editorial and generic Inter/Roboto styling.

## Components and layout

- Fixed top navigation as compact wayfinding, not a heavy app shell.
- Hero as a theatrical viewport with SVG fossil forms and layered strata.
- Interactive time dial with a large range input and live era readout.
- Specimen theater: one dominant illustrated specimen stage with selectable families, avoiding equal card-grid repetition.
- Field notes as dense but readable facts, staggered in asymmetric columns.
- Extinction section as a high-contrast impact vignette with restrained animation.

## Motion

Motion is primarily interaction-driven: cursor excavation light, timeline scrubbing, specimen swapping, hover scanner passes, and one-time reveal choreography. Respect `prefers-reduced-motion` by disabling transitions and auto-reveals.

## Responsive behavior

Hero and specimen layouts collapse into a single-column phone composition. Slider remains full-width with large touch target. Typography uses `clamp()` with conservative maxima to prevent overflow.
