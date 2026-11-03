---
name: ui-design-styles
description: Apply, adapt, compare, or review one of 14 documented visual UI styles. Use when a user names a style, provides a style reference, requests a redesign in a visual style, or asks for a style comparison.
---

# UI Design Styles

Use this skill to implement a named visual style without damaging usability, accessibility, responsiveness, or the existing product behavior.

## Workflow

1. **Understand the request.** Identify the requested style, target pages/components, desired intensity, framework, and whether behavior must remain unchanged. If the style is not specified, ask one focused question or recommend options based on product context.
2. **Inspect the project.** Read existing components, tokens, CSS architecture, dependencies, and responsive conventions before editing. Do not replace the stack or introduce a UI framework without permission.
3. **Load the style reference.** Read the matching file under `references/`. Do not rely on memory or the short descriptions in this file alone.
4. **Resolve ambiguity.** If two styles are easily confused, use the comparison section in the reference. Examples: Glassmorphism vs Liquid Glass; Web Brutalism vs Neobrutalism; Flat Design vs Minimalism; Neumorphism vs Claymorphism; Y2K vs Frutiger Aero.
5. **Plan tokens and components.** Define reusable color, type, spacing, radius, border, shadow, surface, and motion tokens. Keep style-specific decisions centralized.
6. **Implement in scope.** Preserve routes, data flow, semantics, validation, keyboard behavior, and existing functionality. Change visual presentation unless the user explicitly asks for functional changes.
7. **Cover states.** Include default, hover, active, focus-visible, disabled, loading, empty, success, and error states where relevant.
8. **Validate.** Check responsive widths, contrast, keyboard navigation, reduced motion/transparency, fallback behavior, and console/build errors when tools are available.
9. **Summarize.** State what changed, the chosen visual signals, known limitations, and how it was checked.

## Available styles

Read exactly one primary reference for the selected style:

| Style | Reference |
|---|---|
| Glassmorphism | `references/glassmorphism.md` |
| Neumorphism | `references/neumorphism.md` |
| Skeuomorphism | `references/skeuomorphism.md` |
| Flat Design | `references/flat-design.md` |
| Minimalism | `references/minimalism.md` |
| Web Brutalism | `references/web-brutalism.md` |
| Neobrutalism | `references/neobrutalism.md` |
| Claymorphism | `references/claymorphism.md` |
| Liquid Glass | `references/liquid-glass.md` |
| Y2K | `references/y2k.md` |
| Frutiger Aero | `references/frutiger-aero.md` |
| Vernacular Web | `references/vernacular-web.md` |
| Aqua | `references/aqua.md` |
| Windows Aero | `references/windows-aero.md` |

**Note:** The NameThatUI atlas currently presents 14 entries; the list above intentionally contains those 14, including both Web Brutalism and Neobrutalism. Verify the live atlas before adding or removing entries.

## Operating modes

### Design from scratch
Create the requested screen using the selected style. Establish a coherent visual system before implementing individual components. Do not make every component equally decorative; preserve hierarchy.

### Transform an existing interface
Keep existing behavior, information architecture, routes, and data contracts. Change visual tokens and component presentation. Avoid unnecessary rewrites.

### Review an interface
Evaluate the implementation against the reference's defining signals, identify style drift, and separately report usability/accessibility problems. Do not equate stylistic fidelity with quality.

### Combine styles
Use one **primary** style and at most one **secondary influence** unless the user requests otherwise. State which elements belong to which influence. Never blend contradictory defining signals accidentally.

## Framework guidance

The references are framework-independent. Translate them into the project's existing stack:
- Plain HTML/CSS: semantic elements, custom properties, progressive enhancement.
- Bootstrap: use theme variables and scoped component overrides; avoid fighting the grid or duplicating Bootstrap utilities.
- Tailwind: encode stable values in the theme/config and compose reusable component classes.
- React/Vue/Angular: keep tokens separate from component logic.
- Blazor: preserve component parameters, event callbacks, forms, validation, and existing CSS isolation conventions.
- Flutter: map tokens to ThemeData and reusable widgets; use platform-native behavior where appropriate.

Do not claim that a CSS imitation exactly reproduces a native platform material or rendering engine.

## Non-negotiable quality rules

- Accessibility and readability outrank decorative fidelity.
- Never remove labels, focus indicators, semantics, or essential affordances to achieve a look.
- Respect `prefers-reduced-motion` and `prefers-reduced-transparency` where applicable.
- Provide fallbacks for expensive or unsupported effects such as `backdrop-filter`.
- Avoid unnecessary dependencies and large background assets.
- Keep contrast, responsive layout, and interaction states consistent.
- Do not copy source-site text or images wholesale; use original implementation and cite source references.

## Reference map

For the full design signals, CSS starting points, nearest-style comparisons, and accessibility notes, open the matching file in `references/`. The `README.md` contains the visual gallery and source links.
