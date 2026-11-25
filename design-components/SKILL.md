---
name: design-components
description: Creates main components and a rendered gallery of their permutations. Use when building components from an existing design foundation or supplied references, code, or a brief, and exploring their variations visually.
---

# Design Components

Build reusable components from either an existing design foundation or the user's supplied input. A completed foundation is optional, including while foundation work is in progress. Deliver programmatic component definitions and a rendered gallery of their permutations using those definitions.

## Choose the starting point

Inspect the supplied input and the project's existing tokens, styles, components, and implementation stack. Reuse established components where they already satisfy the need. Follow the user's chosen source and scope; do not require foundation work as a prerequisite.

### With an existing design foundation

- Read the project's `design-foundation.md` or equivalent foundation input when available. This is project input, not a bundled skill file or a website.
- Carry forward its typography, semantic colors, spacing, sizing, radii, elevation, iconography, motion, themes, and accessibility rules wherever specified. Bind component styles to those tokens rather than inventing parallel values.
- If the foundation is partial, use it for the decisions it covers and use the direct-input path below for the remaining component decisions. Keep proposed foundation additions explicit.

### From direct input

- Build from the supplied website, screenshots, design files, existing code, or written brief. Inspect the relevant component anatomy, typography, colors, spacing, sizing, states, and responsive behavior supported by that input.
- If no foundation is available or it is still being developed, proceed from that input. Do not ask for a foundation or create a full one unless the user requests it.
- Reuse applicable project tokens. For uncovered decisions, keep shared values in a small, clearly identified set of provisional component tokens or style constants so they can be mapped to a future foundation without changing the component API.
- Distinguish observed reference details from inferred behavior and provisional choices. Make minimal compatible assumptions for gaps; ask only when missing input would materially change the component direction or scope.

## Define the component families and permutations

Choose only the component families required by the product or requested scope. Establish each family's anatomy, purpose, default configuration, reusable API, and supported permutation axes before rendering it. Consider the axes that apply:

- **Hierarchy and intent:** primary, secondary, subtle, destructive, or other roles defined by the foundation or supplied input.
- **Size and density:** supported sizes, compact or comfortable spacing, and content-driven versus full-width behavior.
- **Interaction state:** default, hover, pressed, keyboard focus, disabled, loading, selected, checked, error, and success where meaningful.
- **Content and composition:** short and long labels, optional leading or trailing icons, icon-only use, supporting text, media, and nested content slots.
- **Context:** light or dark themes, narrow containers, wrapping, truncation, and responsive behavior where the foundation, supplied input, or product requires them.

Separate independent properties from states. Define valid combinations and precedence, such as whether loading disables activation and how focus appears with an error. Do not treat every possible combination as a separate hand-built component.

Show every supported value at least once and combine axes where the interaction could expose a design problem. Favor useful comparisons over an exhaustive Cartesian product. For example, a button gallery can show every hierarchy at its default size, every size in one hierarchy, the interaction states, and selected icon and long-label cases. Omit combinations that have no valid product meaning.

## File 1: Define the main components programmatically

Create the canonical implementation first, using the project's existing stack and conventions. For a new React artifact, `components.tsx` is a suitable default; use the equivalent in other stacks. In an existing project, update or reuse its component modules rather than duplicating them merely to fit a filename.

- Define reusable main components with explicit properties for supported variants, sizes, states, and content slots. Use sensible defaults and prevent contradictory combinations.
- Keep shared anatomy and styles in the main component so every permutation inherits changes from the same source. Reference established foundation tokens or the provisional component tokens defined from the input.
- Implement semantic elements, accessible names, keyboard behavior, visible focus, and disabled or loading behavior as applicable. Treat accessibility as part of the component contract.
- Define the valid gallery cases as structured configuration so their labels, properties, and rendered examples remain consistent.

## File 2: Show the permutations visually

Create a separate runnable preview, such as `components-preview.tsx`, a component gallery page, or stories in the project's existing component explorer. Import and render File 1's components; the visual reference must use the actual implementation.

- Open or render the gallery and show it to the user. A written inventory, code block, or list of variants alone does not satisfy this step.
- Arrange examples by component family. Show a clear default example, then labeled comparisons of variants, sizes, states, and selected combinations.
- Use consistent alignment, spacing, background, and scale to make differences easy to judge. Label each example with its relevant properties and state.
- Include realistic content and a small set of stress cases such as long labels, missing optional content, and narrow widths where applicable.
- Support real interaction so hover, focus, pressed, keyboard navigation, and loading behavior can be inspected. If persistent state specimens are useful, implement them through shared internal styling or the preview harness rather than adding fake state controls to the public component API.

Use the user's requested visual surface and any applicable tooling guidance. With no requested surface, use the project's preview environment or a local browser gallery. If no rendering tool is available, provide the runnable preview and state that visual verification remains incomplete.

## Inspect and refine like a designer

Review the rendered gallery, not just the source. Check visual hierarchy, optical alignment, typography, icon balance, spacing, contrast, focus visibility, and consistency with the chosen foundation or supplied input. Inspect content stress cases, applicable themes, and narrow layouts. Exercise the meaningful interaction paths and supported state combinations. Fix inconsistencies in the main definitions, regenerate their instances, and inspect again. Run the project's relevant existing checks when implementation changes warrant them. Claim only the checks and visual inspection actually completed.

## Handoff

Provide links to the canonical component definitions and the visual gallery. Briefly identify the component families and permutations covered, the input used, any assumptions or provisional tokens, any foundation gaps or proposed additions, and what was visually and behaviorally verified. The work is complete when the reusable components and their rendered permutations agree and the requested scope has been inspected.
