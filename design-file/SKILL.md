---
name: design-file
description: Turn an established Figma design library into a project-ready global.css or design-system.md draft, then obtain human review before adding or replacing the repository file. Use when a design system must be available to a coding agent in a repository.
---

# Design file

Create a repository-facing representation of the established design library. First inspect the project's framework, existing styles, and documentation. Choose `global.css` when the project consumes CSS variables directly; choose `design-system.md` when the main need is guidance for an agent or the project has no CSS integration. Use both only when each has a distinct purpose or the user asks.

## Draft

- Reproduce the Figma definitions faithfully: semantic color roles, text styles, radii, and shadows. Preserve exact final values and names, and include the Figma source link and update date.
- For CSS, expose stable custom properties and reusable type classes or clear usage guidance that fits the existing codebase. Integrate with existing naming and cascade conventions rather than adding a second competing system.
- For Markdown, explain token intent, type hierarchy, radius and shadow usage, and any meaningful accessibility or responsive behavior. Keep it concise enough for an agent to consult during implementation.
- Do not introduce spacing tokens or a generic component specification unless requested.
- Check that names and values match the Figma library and that the proposed file fits the repository. Show a readable diff or draft before committing the change to the repository.

## Human review gate

The founder wants to approve the repository-facing file. Prepare the complete draft and explain any choices that differ from Figma, then request approval before adding or replacing the repository file. If the user has already explicitly approved this exact draft or explicitly authorized writing the file in the current request, proceed without asking again. After approval, write the file, verify its contents, and report its path.
