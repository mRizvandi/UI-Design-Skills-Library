# Skeuomorphism

> Interface elements imitate recognizable physical objects, materials, and mechanisms.

- **Classification:** Established design approach
- **Atlas entry:** [Skeuomorphism on NameThatUI](https://namethatui.com/styles/skeuomorphism)
- **Research status:** Initial synthesis; verify source links and platform guidance before production use.

## Overview

Interface elements imitate recognizable physical objects, materials, and mechanisms. Treat this as a visual language with defining signals, not as a rigid component library. Preserve the product's information architecture, behavior, and accessibility while applying the style.

## Defining visual signals

- Named physical materials such as leather, paper, linen, felt, or brushed metal.
- A consistent physical lighting model with highlights, bevels, and inset shadows.
- Real-object metaphors: notebook, bookshelf, dial, mixer, or calculator.
- Craft details such as stitching, grain, embossing, or rivets.
- Material-specific color and texture.

## Design system guidance

### Color
Derive colors from the represented material; avoid arbitrary gradients that contradict the material.

### Surfaces and materials
Use carefully optimized textures, material grain, gradients, and lighting. Keep textures subordinate to content.

### Geometry
Shapes often follow the physical object being represented.

### Typography
Typography may echo labels or printing on the physical object, while remaining legible.

### Motion
Use purposeful mechanical feedback only where it supports the metaphor.

## Implementation starting point

The following CSS is a starting point, not a complete theme. Adapt tokens, contrast, states, and responsive behavior to the host product.

```css
.skeuo-button {\n  background: linear-gradient(#fafafa, #cfd3d8);\n  border: 1px solid #8c929a;\n  border-radius: 8px;\n  box-shadow: inset 0 1px 0 rgba(255,255,255,.9),\n              0 2px 4px rgba(0,0,0,.28);\n  text-shadow: 0 1px rgba(255,255,255,.7);\n}
```

## Avoid style drift

- Decorative texture with no coherent material metaphor.
- Inconsistent light direction.
- Using bevels as the only indication of state.
- Confusing glossy plastic controls with a complete skeuomorphic metaphor.

## Closest look-alikes

Neumorphism removes named materials and uses soft dual shadows on a uniform surface. Skeuomorphism intentionally depicts a real material or object.

## Accessibility and responsive behavior

Texture must not reduce text contrast. Do not use physical appearance as the sole signal for action, state, or validation. Compress texture assets and provide reduced-motion behavior.

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

- NameThatUI style entry: [Skeuomorphism](https://namethatui.com/styles/skeuomorphism)
- https://www.nngroup.com/articles/skeuomorphism/

Source notes: This file is an independently written implementation guide informed by the linked material. It is not a reproduction of the source page. Verify current platform APIs and licensing before shipping.
