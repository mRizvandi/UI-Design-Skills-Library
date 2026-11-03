# Flat Design

> Two-dimensional rendering, solid fills, and minimal simulated depth.

- **Classification:** Established design movement
- **Atlas entry:** [Flat Design on NameThatUI](https://namethatui.com/styles/flat-design)
- **Research status:** Initial synthesis; verify source links and platform guidance before production use.

## Overview

Two-dimensional rendering, solid fills, and minimal simulated depth. Treat this as a visual language with defining signals, not as a rigid component library. Preserve the product's information architecture, behavior, and accessibility while applying the style.

## Defining visual signals

- Solid color fills without realistic gradients or material effects.
- Simple geometric shapes and restrained iconography.
- Clear typographic hierarchy and deliberate spacing.
- Minimal or absent drop shadows, bevels, and textures.
- Meaning conveyed through layout, color, and shape.

## Design system guidance

### Color
Use a deliberate, accessible palette with distinct semantic colors. Flat does not mean low contrast.

### Surfaces and materials
Opaque fills and simple borders; use elevation only when functionally necessary and visually restrained.

### Geometry
Simple geometry, consistent radii, and recognizable icon shapes.

### Typography
Readable sans-serif typography with clear scale and weight hierarchy.

### Motion
Use subtle transitions to clarify changes, not to simulate physical materials.

## Implementation starting point

The following CSS is a starting point, not a complete theme. Adapt tokens, contrast, states, and responsive behavior to the host product.

```css
.flat-card {\n  background: #ffffff;\n  border: 1px solid #e4e7ec;\n  border-radius: 8px;\n  box-shadow: none;\n}\n.flat-button {\n  background: #2457d6;\n  color: #fff;\n  border: 0;\n  border-radius: 6px;\n  padding: .7rem 1rem;\n}
```

## Avoid style drift

- Removing affordances along with decoration.
- Using color as the only status indicator.
- Equating flat design with minimalism; a flat screen can still be dense.
- Adding gradients, bevels, and heavy shadows that undermine the flat rendering.

## Closest look-alikes

Flat Design governs how elements are rendered. Minimalism governs how much content and how many elements are present.

## Accessibility and responsive behavior

Maintain WCAG contrast, visible focus states, semantic controls, and non-color status cues. Simplicity should not remove labels or discoverability.

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

- NameThatUI style entry: [Flat Design](https://namethatui.com/styles/flat-design)
- https://www.nngroup.com/articles/flat-design/

Source notes: This file is an independently written implementation guide informed by the linked material. It is not a reproduction of the source page. Verify current platform APIs and licensing before shipping.
