# Neobrutalism

> A designed, graphic rawness: bold flat colors, thick ink-like outlines, and hard shadows.

- **Classification:** Industry-coined trend
- **Atlas entry:** [Neobrutalism on NameThatUI](https://namethatui.com/styles/neobrutalism)
- **Research status:** Initial synthesis; verify source links and platform guidance before production use.

## Overview

A designed, graphic rawness: bold flat colors, thick ink-like outlines, and hard shadows. Treat this as a visual language with defining signals, not as a rigid component library. Preserve the product's information architecture, behavior, and accessibility while applying the style.

## Defining visual signals

- Thick, high-contrast black outlines around cards and controls.
- Hard, offset shadows with zero or near-zero blur.
- Saturated flat color blocks on a light or neutral ground.
- Bold typography and deliberately graphic composition.
- Pressed states collapse or reduce the offset shadow.

## Design system guidance

### Color
High-saturation colors such as yellow, pink, lime, or cyan paired with black outlines. Keep text contrast strong.

### Surfaces and materials
Opaque, flat color blocks; avoid gradients, blur, and translucent surfaces.

### Geometry
Simple geometric shapes with consistent heavy borders.

### Typography
Bold display type and clear, often oversized labels.

### Motion
Pressed states can translate the control toward its shadow to simulate compression.

## Implementation starting point

The following CSS is a starting point, not a complete theme. Adapt tokens, contrast, states, and responsive behavior to the host product.

```css
.neo-card {\n  background: #ffe66d;\n  border: 3px solid #111;\n  box-shadow: 6px 6px 0 #111;\n  border-radius: 4px;\n}\n.neo-button:active { transform: translate(4px, 4px); box-shadow: 2px 2px 0 #111; }
```

## Avoid style drift

- Soft blurred shadows or gradients.
- Using thin low-contrast borders.
- Confusing designed graphic rawness with unstyled Web Brutalism.
- Making every element equally loud; preserve hierarchy.

## Closest look-alikes

Web Brutalism exposes raw browser/document styling. Neobrutalism exaggerates graphic styling through thick outlines, flat saturated fills, and hard shadows.

## Accessibility and responsive behavior

Ensure buttons remain recognizable and keyboard-focusable. Use non-color state cues and verify contrast for every saturated color combination.

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

- NameThatUI style entry: [Neobrutalism](https://namethatui.com/styles/neobrutalism)
- https://www.nngroup.com/articles/brutalism-antidesign/

Source notes: This file is an independently written implementation guide informed by the linked material. It is not a reproduction of the source page. Verify current platform APIs and licensing before shipping.
