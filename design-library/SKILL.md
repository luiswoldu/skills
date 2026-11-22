---
name: design-library
description: Build or update a lean Figma design library from a selected visual direction, including semantic color variables, text styles, radius variables, and shadow styles. Use when the design direction is ready to become reusable design definitions.
---

# Design library

Translate the selected visual direction into reusable definitions in the project's Figma file or library. Inspect the existing file and library first; preserve useful names and avoid duplicate collections or styles.

## Build

- Define semantic color variables for roles the design actually uses, such as backgrounds, surfaces, text, borders, and actions. Give each role a clear name and value. Add modes only when the project calls for distinct themes or contexts.
- Keep seed or primitive colors separate from semantic roles when aliases make changes easier to manage. Do not create a large palette solely for completeness.
- Create **text styles** based on the chosen typeface, normally hero, headline, body, and any supporting style the designs need. Specify font family, size, weight, line height, and letter spacing. Keep the hierarchy simple and adjust it to the actual board.
- Create numeric radius variables for the recurring corner treatments. Create Figma effect styles for recurring shadows; shadows are styles, not ordinary scalar variables.
- Apply the definitions to representative elements on the board so their appearance and naming can be checked in context.
- Unless explicitly requested, do not add spacing tokens or a component library for these projects yet.

## Handoff

Provide the Figma library link.
