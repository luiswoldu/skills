---
name: design-foundation
description: Create a polished HTML design foundation from seed colors, a typeface, and references. Use to explore and present typography, palettes, and semantic color roles before building a reusable design system.
---

# Design foundation

Create a browser-viewable design foundation with two sections: a typography specimen and a color-and-semantics board. The page itself should demonstrate the proposed visual language through live type, real color swatches, and a carefully composed layout. Accept rough inputs: raw hex codes, a font, references, or screenshots. Inspect supplied references before designing.

## Delivery

Default to a self-contained HTML file with embedded CSS and only the JavaScript that improves the review experience. It should open directly in a browser without a build step. Use semantic HTML and responsive CSS for the layout; keep text selectable and specimens editable in source.

Bundle any needed font or image files alongside the HTML using relative paths, or embed them when practical. Prefer supplied font files; disclose any external font dependency. If the chosen typeface is unavailable, identify the fallback as a proposal rather than presenting it as the original font.

An existing app framework or another browser-rendered format is appropriate when it materially improves the result or fits the user's project. Deliver its editable source, a working preview, and any minimal run instructions. A design-tool document or account is not required.

## References

Use the bundled screenshots as **layout references**, not as project specifications:

- [Type specimen reference](attachments/type-specimen-reference.png): large live type samples, arranged by hierarchy, with each style's size and intended use directly beneath it. The two-column layout separates display and supporting text.
- [Semantic color reference](attachments/semantic-color-reference.png): grouped use cases, swatches and exact hex values, light/dark rows where relevant, and a side-by-side mapping from human-readable roles to reusable semantic names.

The screenshots' product names, exact type sizes, colors, token names, and status marks are examples. Derive those details from the current project's brief and visual exploration.

## Work

- Treat supplied colors and font as inputs. Clearly distinguish them from any derived colors or proposed substitutions.
- Make a typography specimen in the spirit of the first reference. Render every proposed style as live text in the chosen typeface. Show its size, weight, line height, letter spacing, and intended use close to the sample. Make the hierarchy scannable at a glance. Start with only the styles the project needs; add desktop/mobile variants only when their behavior differs. Labels must match the CSS actually rendered, including responsive changes.
- Make a color and semantics board in the spirit of the second reference. Group colors by use, show swatches and exact values, and map each proposed use to a semantic name. Show light/dark modes only if the project has both; mark unconfirmed mappings as proposals. Include small contextual samples where they help assess foreground/background pairings or recognizable states.
- Compose the page with deliberate hierarchy, generous whitespace, aligned annotations, and legible supporting text. Use the references' information structure while adapting the layout to the project and viewport. Keep the specimens and swatches central; use concise notes to explain decisions and tradeoffs.
- Define proposed colors and type styles in a consistent set of CSS custom properties or equivalent structured data. Keep rendered samples and displayed values synchronized. Keep presentation-only styling distinct from proposed project tokens. Avoid spacing-token systems and reusable component specifications unless requested.
- Add interactions only when they improve critique, such as switching an existing light/dark theme or editing specimen text. Keep the essential information visible without interaction, and make any controls keyboard-accessible.

## Check

Open the deliverable in a browser and inspect it at wide and narrow widths. Verify that fonts load, samples match their labels, annotations remain readable, and nothing clips or overlaps. Exercise any interactions and check that the delivered file and its relative assets work together. If browser inspection is unavailable, state that limitation.

Check contrast for the actual foreground/background pairings being proposed. Report measured ratios when making accessibility claims; identify unresolved pairings rather than implying every swatch combination is suitable.

## Handoff

Provide the HTML file or source bundle, open its preview when available, and summarize the direction: seed inputs, proposed palette and roles, type hierarchy, and unresolved choices. Keep names and values precise enough for downstream implementation directly from the artifact.

Treat the foundation as a proposal. Continue into a reusable library or production integration when the user requests that workflow, using their chosen implementation target. Request a choice only when competing directions cannot be resolved from the brief.
