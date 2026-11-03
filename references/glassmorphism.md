# Glassmorphism

> Frosted translucent surfaces over a vivid, visible backdrop.

- **Classification:** Industry-coined trend
- **Atlas entry:** [Glassmorphism on NameThatUI](https://namethatui.com/styles/glassmorphism)
- **Research status:** Initial synthesis; verify source links and platform guidance before production use.

## Overview

Frosted translucent surfaces over a vivid, visible backdrop. Treat this as a visual language with defining signals, not as a rigid component library. Preserve the product's information architecture, behavior, and accessibility while applying the style.

## Defining visual signals

- Semi-transparent panels with a perceptible backdrop blur.
- A colorful gradient, photograph, or aurora remains visible through the surfaces.
- Thin, light, semi-transparent edges define the glass boundaries.
- Layered panels float with soft, wide shadows.
- Light or near-white text is common, but contrast must be engineered.

## Design system guidance

### Color
Let the backdrop provide much of the palette. Use translucent light or dark surfaces rather than assuming white glass is always correct.

### Surfaces and materials
Use translucent fills, backdrop-filter blur, subtle saturation, a fine light border, and restrained layered shadows.

### Geometry
Rounded rectangles are common; keep radii consistent across nested surfaces.

### Typography
Clear sans-serif typography with strong hierarchy. Avoid low-opacity body text.

### Motion
Keep transitions restrained; avoid blur-heavy animation on low-powered devices.

## Implementation starting point

The following CSS is a starting point, not a complete theme. Adapt tokens, contrast, states, and responsive behavior to the host product.

```css
.glass-panel {\n  background: rgba(255, 255, 255, 0.12);\n  -webkit-backdrop-filter: blur(16px) saturate(140%);\n  backdrop-filter: blur(16px) saturate(140%);\n  border: 1px solid rgba(255, 255, 255, 0.25);\n  border-radius: 16px;\n  box-shadow: 0 12px 32px rgba(0, 0, 0, 0.16);\n}\n@supports not (backdrop-filter: blur(1px)) {\n  .glass-panel { background: rgba(24, 30, 48, 0.94); }\n}
```

## Avoid style drift

- Using transparency without blur and calling it glass.
- Putting glass cards on a plain, lifeless background with no visible backdrop.
- Applying glass to every surface until hierarchy disappears.
- Confusing decorative glassmorphism with Apple's control-layer-focused Liquid Glass.

## Closest look-alikes

Liquid Glass reserves adaptive glass for floating controls above opaque content. Glassmorphism commonly treats content cards and panels themselves as frosted decorative surfaces.

## Accessibility and responsive behavior

Test contrast over the worst possible backdrop region, not a convenient screenshot. Provide near-opaque fallback for unsupported blur and prefers-reduced-transparency/OS transparency settings.

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

- NameThatUI style entry: [Glassmorphism](https://namethatui.com/styles/glassmorphism)
- https://www.nngroup.com/articles/glassmorphism/
- https://developer.apple.com/design/human-interface-guidelines/materials

Source notes: This file is an independently written implementation guide informed by the linked material. It is not a reproduction of the source page. Verify current platform APIs and licensing before shipping.
