# Minimalism

> Reduce what is on screen; use negative space and typography as primary composition tools.

- **Classification:** Established movement
- **Atlas entry:** [Minimalism on NameThatUI](https://namethatui.com/styles/minimalism)
- **Research status:** Initial synthesis; verify source links and platform guidance before production use.

## Overview

Reduce what is on screen; use negative space and typography as primary composition tools. Treat this as a visual language with defining signals, not as a rigid component library. Preserve the product's information architecture, behavior, and accessibility while applying the style.

## Defining visual signals

- Generous, intentional negative space.
- A restricted number of visible elements and competing actions.
- Limited or near-monochrome palette with a restrained accent.
- One or two dramatic typographic moments.
- Decoration is removed rather than merely restyled.

## Design system guidance

### Color
One or two dominant hues, often neutral plus one accent. Maintain contrast even with muted colors.

### Surfaces and materials
Rendering is flexible: flat fills, subtle shadows, or restrained depth can all work.

### Geometry
Simple, consistent shapes that support hierarchy.

### Typography
Typography carries much of the visual identity; use responsive display sizing and readable body measures.

### Motion
Minimal and purposeful; avoid motion that competes with the message.

## Implementation starting point

The following CSS is a starting point, not a complete theme. Adapt tokens, contrast, states, and responsive behavior to the host product.

```css
.minimal-layout {\n  width: min(100% - 2rem, 68rem);\n  margin-inline: auto;\n  padding-block: clamp(4rem, 14vh, 9rem);\n}\n.minimal-title {\n  max-width: 12ch;\n  font-size: clamp(2.75rem, 8vw, 6.5rem);\n  line-height: .98;\n  letter-spacing: -.045em;\n}
```

## Avoid style drift

- Hiding essential navigation or labels to make the page look sparse.
- Confusing minimalism with flat rendering.
- Leaving empty space without a hierarchy or purpose.
- Using tiny low-contrast text as a supposed minimalist treatment.

## Closest look-alikes

Flat design limits simulated depth in rendering; minimalism limits content, features, and visual competition. A UI can be flat but crowded.

## Accessibility and responsive behavior

Do not remove affordances or labels. Use responsive type scales and preserve at least 4.5:1 contrast for normal text.

Also verify:
- Layout reflows without horizontal scrolling at narrow viewport widths.
- Keyboard focus is visible and not clipped by overflow containers.
- Controls have semantic HTML, accessible names, and usable hit areas.
- Content remains understandable with motion, transparency, and decorative imagery disabled.
- Color is never the only carrier of meaning.

## Agent implementation checklist

1. Read the project before changing it; identify framework, design tokens, component conventions, and existing behavior.
2. Apply the defining signals above to the requested scope only.
3. Keep content hierarchy, navigation, validation, and interaction behavior intact.
4. Create reusable tokens and components rather than scattering one-off values.
5. Implement hover, active, disabled, focus-visible, loading, and error states.
6. Test desktop, tablet, and mobile widths.
7. Check contrast and reduced-motion/transparency fallbacks.
8. Report any visual compromises caused by framework or browser limitations.

## Sources

- NameThatUI style entry: [Minimalism](https://namethatui.com/styles/minimalism)
- https://www.nngroup.com/articles/characteristics-minimalism/

Source notes: This file is an independently written implementation guide informed by the linked material. It is not a reproduction of the source page. Verify current platform APIs and licensing before shipping.
