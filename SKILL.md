---
name: anti-ai-default-ui
description: Prohibit recurring generic AI-generated web and app design patterns when creating or editing an interface.
---

# Anti-AI Default UI

Use this skill when creating or editing a web or app interface. This is a strict prohibition list. Do not suggest alternative visual treatments, design directions, or compensating stylistic moves in this skill. If the user explicitly requests an exception, follow that request; otherwise, do not use any prohibited pattern.

## Prohibited visual defaults

- Blue-to-violet, purple-to-pink, warm beige, or dark gradient backgrounds used as generic atmosphere.
- Radial glows, blurred halos, ambient blobs, aurora effects, decorative mesh gradients, or glassmorphism.
- Creamy off-white backgrounds used only to signal “premium.”
- Near-black dark-mode backgrounds with low-opacity white borders as a default dark theme.
- Generic abstract 3D objects, floating spheres, or decorative AI imagery with no product meaning.
- Decorative gradients, blurs, textures, shadows, or glows added merely to make an empty interface look finished.
- Multiple pastel accent colors used only to decorate repeated UI elements.

## Prohibited hero and marketing templates

- Centered eyebrow pill → oversized headline → muted gray description → CTA hero structure.
- Fully rounded eyebrow pills, category pills, badge pills, and status pills used as default labels.
- Oversized centered marketing headlines with low-contrast gray subcopy.
- A filled primary button and outlined secondary button displayed with similar prominence.
- Two or more competing primary calls to action.
- Generic SaaS copy, interchangeable benefit claims, invented social proof, invented metrics, and placeholder testimonials.
- Product marketing sections whose headings and text could describe an unrelated SaaS product without changes.
- Decorative device mockups or product screenshots that do not depict real product content or states.

## Prohibited cards, borders, and containment

- Three-card, six-card, or repeated equal-card feature grids.
- Wrapping every feature, statistic, testimonial, price, FAQ, signup, or piece of content in a card.
- Repeating icon + title + description + link cards as a section template.
- Elevated rounded cards with faint borders and soft shadows as a default content container.
- Giving a card, feature tile, or panel a decorative border on only one edge.
- Left-only, right-only, top-only, or bottom-only accent borders applied to a card to fake distinction, editorial character, status, or priority.
- Colored edge accents, partial card borders, clipped card edges, inset card edges, or card-adjacent divider lines used as ornament.
- Uniform card surfaces, border weights, shadows, and containment regardless of content role.
- Using cards to replace information structure, content grouping, hierarchy, lists, tables, or actual interaction design.
- Placing a border around every section, subsection, control group, list row, statistic, sidebar, header, footer, and empty area.
- Nested boxes, double outlines, perimeter frames, stacked separators, or multiple concentric borders around the same region.
- Hairline borders used to make an otherwise empty region feel designed.
- Borders between elements that do not indicate a real grouping, ownership, state boundary, or interaction boundary.

## Prohibited geometry, spacing, and layout defaults

- Applying the same border radius to buttons, inputs, images, avatars, cards, sheets, modals, and panels.
- Uniformly large rounded corners as a style system.
- Perfectly even 8-point spacing and alignment applied without content-specific adjustment.
- Symmetrical two-column and three-column layouts chosen only because they are easy to generate.
- Repeating equal-width sections, equal-height blocks, equal visual weight, and identical padding across the page.
- Generic centered containers and repeated section spacing that produce an interchangeable landing-page rhythm.
- Full-page layouts built from stacked, detached floating rectangles.
- Decorative offset, overlap, asymmetry, broken grids, or editorial dividers added simply to avoid looking generic.

## Prohibited icon and component defaults

- Generic thin-stroke icon libraries used as the primary visual identity.
- Icons centered inside rounded squares with soft tinted backgrounds.
- A different colored icon tile for every feature without semantic meaning.
- Icons used as decoration where text, data, or content would communicate more clearly.
- Buttons, controls, inputs, menus, and surfaces that all share the same rounded, softly elevated appearance.
- Hover effects limited to a small lift, a larger shadow, a border-color shift, or a generic fade-and-slide animation.
- Decorative motion, staggered entrance animations, and page-wide reveal choreography.

## Prohibited game, HUD, and console drift

- Turning a non-game interface into a game board, arena, stage, field, cockpit, battle station, command center, or mission-control screen.
- Decorative rings, felt textures, table outlines, arena contours, player-position diagrams, chips, suits, shields, crosshairs, reticles, target marks, or scoreboards that are not required by the user’s actual task.
- Green, amber, red, cyan, or neon accent systems used as “game state” atmosphere rather than as necessary and accessible information.
- Glowing status lights, pulsing dots, LED indicators, online lamps, quality lights, readiness lamps, or animated signal marks without a concrete operational state.
- Mini progress bars, action meters, percentage tracks, XP-like meters, level bars, health-like bars, or colored gauges added when the value is not the user’s primary decision data.
- Color-coding every action, role, panel, row, or icon as if it were a game faction or ability.
- Decorative keyboard-shortcut keycaps, console labels, telemetry strips, system-readout chrome, or fake technical instrumentation.
- Dashboard chrome that turns ordinary labels into all-caps micro-headings, heavily tracked kickers, serial-number text, coordinate strings, or pseudo-military status language.
- Excessive status badges, colored dots, tiny labels, counters, counters-with-icons, and micro-metrics surrounding a simple task.
- Dense heads-up-display framing that competes with the primary content: permanent top bars, side rails, bottom strips, inset inspector panels, and boxed readouts all at once.
- Gamified hover, press, selection, completion, loading, or error effects that make ordinary software feel like an arcade interface.
- Decorative danger, success, warning, or achievement styling applied to neutral information.

## Prohibited hierarchy and content defaults

- Size hierarchy without an unambiguous attention hierarchy.
- Giving every heading, card, statistic, icon, button, and background accent similar visual prominence.
- Using color, contrast, or decoration to make all elements look equally important.
- Muted text, faint borders, or low-opacity controls that reduce readability or accessibility.
- Color as the only way to communicate status, selection, validation, urgency, or interaction.
- Styling before real copy, realistic content length, real data, empty states, loading states, error states, permission states, offline states, and narrow-screen behavior exist.
- Desktop layouts simply stacked on mobile without reconsidering hierarchy or content density.
- Layouts that fail with long Korean copy, localized text, larger text settings, or representative data.

## Prohibited workflow defaults

- Accepting the first generated layout and only changing its color, copy, radius, or imagery.
- Asking for “more modern,” “more premium,” “more polished,” or “more beautiful” without product-specific constraints.
- Using a generic design system, template, component set, or icon library as the visual identity of the product.
- Treating clean alignment, rounded cards, gradients, and component consistency as proof that a design is product-specific.
- Adding arbitrary novelty only to avoid looking AI-generated.

## Final guardrail

Before delivering an interface, remove every prohibited pattern above. Do not propose replacement styling in this skill. If removing a pattern leaves an unresolved product or hierarchy question, stop and ask the user for the missing product direction rather than inventing a new visual treatment.
