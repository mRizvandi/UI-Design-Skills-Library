# Claymorphism

> Puffy, soft 3D objects that resemble molded clay or soft plastic.

- **Classification:** Industry-coined trend
- **Atlas entry:** [Claymorphism on NameThatUI](https://namethatui.com/styles/claymorphism)
- **Research status:** Initial synthesis; verify source links and platform guidance before production use.

## Overview

Puffy, soft 3D objects that resemble molded clay or soft plastic. Treat this as a visual language with defining signals, not as a rigid component library. Preserve the product's information architecture, behavior, and accessibility while applying the style.

## Defining visual signals

- Rounded, inflated-looking forms with oversized corner radii.
- Soft inner highlights and shadows plus an outer floating shadow.
- Matte or gently satin surfaces rather than sharp glass reflections.
- Friendly, playful dimensional objects.
- Often colorful, pastel, or softly saturated surfaces.

## Design system guidance

### Color
Pastel or soft saturated colors with enough separation between adjacent objects.

### Surfaces and materials
Use layered inset and outer shadows to suggest volume. Avoid sharp specular chrome.

### Geometry
Pill shapes, circles, and generous rounded rectangles.

### Typography
Friendly sans-serif type; maintain contrast against soft surfaces.

### Motion
Small buoyant transitions can support the tactile metaphor; keep them subtle.

## Implementation starting point

The following CSS is a starting point, not a complete theme. Adapt tokens, contrast, states, and responsive behavior to the host product.

```css
.clay-card {\n  background: #f4b6c8;\n  border-radius: 28px;\n  box-shadow: 10px 12px 24px rgba(80, 55, 80, .16),\n              inset 7px 7px 14px rgba(255,255,255,.55),\n              inset -7px -7px 14px rgba(160,80,120,.12);\n}
```

## Avoid style drift

- Using only a drop shadow; the inner light/shadow treatment is important.
- Over-inflating every component until controls become unclear.
- Confusing clay with neumorphism: clay objects often have independent color and stronger object-like volume.

## Closest look-alikes

Neumorphism molds controls from a shared background surface with dual shadows. Claymorphism uses puffier, often independently colored objects with layered inner and outer shading.

## Accessibility and responsive behavior

Do not rely on shadow depth alone for interactive state. Maintain clear focus rings and adequate contrast; avoid excessive motion or parallax.

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

- NameThatUI style entry: [Claymorphism](https://namethatui.com/styles/claymorphism)
- https://www.nngroup.com/articles/

Source notes: This file is an independently written implementation guide informed by the linked material. It is not a reproduction of the source page. Verify current platform APIs and licensing before shipping.
