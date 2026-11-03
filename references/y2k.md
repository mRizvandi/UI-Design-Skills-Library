# Y2K

> Turn-of-the-millennium digital futurism: chrome, gel, iridescence, and techno typography.

- **Classification:** Retrospective digital aesthetic
- **Atlas entry:** [Y2K on NameThatUI](https://namethatui.com/styles/y2k)
- **Research status:** Initial synthesis; verify source links and platform guidance before production use.

## Overview

Turn-of-the-millennium digital futurism: chrome, gel, iridescence, and techno typography. Treat this as a visual language with defining signals, not as a rigid component library. Preserve the product's information architecture, behavior, and accessibility while applying the style.

## Defining visual signals

- Liquid chrome, polished metal, and silver gradients.
- Glossy gel or translucent plastic buttons and blobs.
- Iridescent blue-silver with cyan/magenta shifts.
- Wide techno type, often outlined, italic, or metallic.
- Orbs, wireframes, lens flares, and pixel/cyber garnish.

## Design system guidance

### Color
Cool synthetic hues: silver, electric blue, cyan, violet, and holographic gradients.

### Surfaces and materials
Chrome and glossy plastic effects with strong specular highlights.

### Geometry
Orbs, bubbles, rounded capsules, sharp techno panels, and wireframe motifs.

### Typography
Extended techno display faces; pair with a highly readable text face.

### Motion
Shimmer, rotation, and animated gradients may be used sparingly.

## Implementation starting point

The following CSS is a starting point, not a complete theme. Adapt tokens, contrast, states, and responsive behavior to the host product.

```css
.y2k-panel {\n  background: linear-gradient(135deg, #f7fbff 0%, #9bb8d8 28%, #fff 48%, #6e8dbb 72%, #e8f7ff 100%);\n  border: 1px solid rgba(255,255,255,.85);\n  box-shadow: inset 0 1px 8px rgba(255,255,255,.9), 0 10px 28px rgba(25,45,90,.24);\n  border-radius: 22px;\n}
```

## Avoid style drift

- Nature-first imagery that moves the mood toward Frutiger Aero.
- Using decorative chrome behind dense text.
- Overusing scanlines and pixel effects until usability suffers.

## Closest look-alikes

Y2K leans synthetic, metallic, and cyber-futuristic. Frutiger Aero pairs glossy tech surfaces with optimistic nature imagery such as sky, water, grass, and bubbles.

## Accessibility and responsive behavior

Keep decorative chrome and animation away from essential text. Respect reduced motion and ensure display type remains legible at small sizes.

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

- NameThatUI style entry: [Y2K](https://namethatui.com/styles/y2k)
- https://aesthetics.fandom.com/wiki/Y2K

Source notes: This file is an independently written implementation guide informed by the linked material. It is not a reproduction of the source page. Verify current platform APIs and licensing before shipping.
