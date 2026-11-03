# Neumorphism

> Soft controls appear pressed out of, or inset into, one continuous matte surface.

- **Classification:** Industry-coined trend
- **Atlas entry:** [Neumorphism on NameThatUI](https://namethatui.com/styles/neumorphism)
- **Research status:** Initial synthesis; verify source links and platform guidance before production use.

## Overview

Soft controls appear pressed out of, or inset into, one continuous matte surface. Treat this as a visual language with defining signals, not as a rigid component library. Preserve the product's information architecture, behavior, and accessibility while applying the style.

## Defining visual signals

- A largely monochrome, low-contrast surface.
- Raised elements use paired light and dark soft shadows.
- Inset controls reverse the shadow relationship.
- Surfaces share the same or closely related base color.
- Depth comes from shadow rather than borders or material texture.

## Design system guidance

### Color
Usually one muted background hue with lighter and darker shadow tones. Prioritize sufficient control-state contrast.

### Surfaces and materials
Matte, opaque surfaces; avoid glass transparency and strong material texture.

### Geometry
Rounded, pill-like controls and soft corners are common.

### Typography
Simple, high-contrast typography. Do not reduce text contrast to match the subtle surfaces.

### Motion
Small pressed-state transitions can reinforce physical feedback.

## Implementation starting point

The following CSS is a starting point, not a complete theme. Adapt tokens, contrast, states, and responsive behavior to the host product.

```css
.neu-surface {\n  background: #e6e9ef;\n  border-radius: 20px;\n  box-shadow: 8px 8px 18px rgba(163, 177, 198, .55),\n              -8px -8px 18px rgba(255, 255, 255, .9);\n}\n.neu-surface:active {\n  box-shadow: inset 5px 5px 10px rgba(163, 177, 198, .55),\n              inset -5px -5px 10px rgba(255, 255, 255, .9);\n}
```

## Avoid style drift

- Using the same shadow for raised and inset states.
- Relying on subtle shadows alone to communicate interactive state.
- Applying this to dense data-heavy screens without stronger grouping.
- Confusing it with skeuomorphism: neumorphism does not imitate named real-world materials.

## Closest look-alikes

Skeuomorphism uses recognizable materials, textures, and object metaphors. Neumorphism molds controls from a mostly uniform matte surface.

## Accessibility and responsive behavior

Soft shadow edges are not sufficient focus indicators. Add explicit keyboard focus rings and stronger selected/disabled states. Check text and icon contrast independently.

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

- NameThatUI style entry: [Neumorphism](https://namethatui.com/styles/neumorphism)
- https://www.nngroup.com/articles/neumorphism/

Source notes: This file is an independently written implementation guide informed by the linked material. It is not a reproduction of the source page. Verify current platform APIs and licensing before shipping.
