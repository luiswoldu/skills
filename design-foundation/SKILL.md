---
name: design-foundation
description: Develop two boards in Figma from seed colors, a typeface, and references. Use for visual exploration before creating a reusable Figma library.
---

# Design foundation

Create two Figma boards that set the foundational design system choices and language for a project. Accept rough inputs: raw hex codes, a font, or a references and screenshots. Inspect supplied references before designing. 

Use the bundled screenshots as **layout references**, not as project specifications:

- [Type specimen reference](attachments/type-specimen-reference.png): large live type samples, arranged by hierarchy, with each style's size and intended use directly beneath it. The two-column layout separates display and supporting text.
- [Semantic color reference](attachments/semantic-color-reference.png): grouped use cases, swatches and exact hex values, light/dark rows where relevant, and a side-by-side mapping from human-readable roles to reusable semantic names.

The screenshots' product names, exact type sizes, colors, token names, and status marks are examples. Derive those details from the current project's brief and visual exploration.

## Work

- Treat supplied colors and font as inputs. Clearly distinguish them from any derived colors or proposed substitutions.
- Make a typography specimen frame in the spirit of the first reference. Render every proposed style in the actual typeface, show its size and intended use, and make the hierarchy scannable at a glance. Start with only the styles the project needs; add desktop/mobile variants only when their behavior differs.
- Make a color and semantics frame in the spirit of the second reference. Group colors by use, show swatches and exact values, and map each proposed use to a semantic name. Show light/dark modes only if the project has both; mark unconfirmed mappings as proposals.
- Label the important decisions and tradeoffs on the board. Make the board useful for critique, including legible contrast and recognizable states where relevant.
- Avoid spacing tokens and reusable component specifications unless the user later asks for them.

## Handoff

Provide the Figma board link and a short direction summary: seed inputs, proposed palette and roles, type hierarchy. Keep names and values precise enough for `design-library` to implement. If the user asks for the full workflow, continue to the library once the direction is clear; request a choice only when competing directions cannot be resolved from the brief.
