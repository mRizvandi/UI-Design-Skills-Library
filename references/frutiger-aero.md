# Frutiger Aero

> Optimistic eco-tech: glossy interfaces, blue skies, water, greenery, and luminous bubbles.

- **Classification:** Retrospective digital aesthetic
- **Atlas entry:** [Frutiger Aero on NameThatUI](https://namethatui.com/styles/frutiger-aero)
- **Research status:** Initial synthesis; verify source links and platform guidance before production use.

## Overview

Optimistic eco-tech: glossy interfaces, blue skies, water, greenery, and luminous bubbles. Treat this as a visual language with defining signals, not as a rigid component library. Preserve the product's information architecture, behavior, and accessibility while applying the style.

## Defining visual signals

- Nature fused with technology: sky, water, grass, leaves, fish, and bubbles.
- Glossy glass and aqua surfaces with curved specular highlights.
- Luminous cyan-blue and fresh grass-green palette.
- Friendly humanist sans-serif typography.
- Bokeh, sun rays, and diagonal sheen.

## Design system guidance

### Color
Bright sky blue, cyan, aqua, white, and fresh green; warm light rather than dark cyber tones.

### Surfaces and materials
Glossy, translucent, light-filled surfaces rather than matte frosted glass.

### Geometry
Rounded organic shapes, bubbles, droplets, and smooth panels.

### Typography
Friendly humanist sans-serif; prioritize clarity over techno styling.

### Motion
Gentle floating, ripple, or light movement can support the ambient world.

## Implementation starting point

The following CSS is a starting point, not a complete theme. Adapt tokens, contrast, states, and responsive behavior to the host product.

```css
.aero-panel {\n  background: linear-gradient(145deg, rgba(255,255,255,.82), rgba(185,239,255,.42));\n  border: 1px solid rgba(255,255,255,.9);\n  border-radius: 24px;\n  box-shadow: inset 0 2px 8px rgba(255,255,255,.8), 0 12px 28px rgba(20,120,150,.18);\n}
```

## Avoid style drift

- Mirror chrome, wireframes, and techno type that shift toward Y2K.
- Dark, dystopian palettes.
- Using generic stock nature photos without coherent art direction.

## Closest look-alikes

Y2K is synthetic chrome-and-gel futurism. Frutiger Aero blends glossy technology with optimistic natural imagery and blue-green color.

## Accessibility and responsive behavior

Nature photography and bright highlights can produce unpredictable contrast. Place text on stable surfaces or scrims; respect reduced motion.

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

- NameThatUI style entry: [Frutiger Aero](https://namethatui.com/styles/frutiger-aero)
- https://aesthetics.fandom.com/wiki/Frutiger_Aero

Source notes: This file is an independently written implementation guide informed by the linked material. It is not a reproduction of the source page. Verify current platform APIs and licensing before shipping.
