# Aqua

> The glossy, candy-like Mac OS X interface language of the early 2000s.

- **Classification:** Vendor design language
- **Atlas entry:** [Aqua on NameThatUI](https://namethatui.com/styles/aqua)
- **Research status:** Initial synthesis; verify source links and platform guidance before production use.

## Overview

The glossy, candy-like Mac OS X interface language of the early 2000s. Treat this as a visual language with defining signals, not as a rigid component library. Preserve the product's information architecture, behavior, and accessibility while applying the style.

## Defining visual signals

- Candy-gel controls with glossy highlights.
- Pinstriped or subtly textured surfaces.
- Rounded, gumdrop-like window controls and buttons.
- Blue-forward, luminous interface surfaces.
- Strong specular highlights and polished gradients.

## Design system guidance

### Color
Aqua blues, whites, graphite, and occasional saturated accent colors.

### Surfaces and materials
Glossy gradients, highlights, subtle stripes, and polished translucent effects.

### Geometry
Rounded window controls, pill buttons, and soft rounded panels.

### Typography
Clean system sans-serif typography; keep labels crisp against glossy surfaces.

### Motion
Use subtle feedback for buttons and window-like controls.

## Implementation starting point

The following CSS is a starting point, not a complete theme. Adapt tokens, contrast, states, and responsive behavior to the host product.

```css
.aqua-button {\n  color: #12385c;\n  background: linear-gradient(#f8fdff 0%, #b9e5fa 42%, #5aa7d8 50%, #d9f3ff 100%);\n  border: 1px solid #4b91bd;\n  border-radius: 999px;\n  box-shadow: inset 0 1px 2px #fff, 0 2px 4px rgba(0,40,80,.25);\n}
```

## Avoid style drift

- Confusing Aqua with generic glassmorphism: Aqua emphasizes glossy gel controls and pinstripes.
- Overdoing reflections behind text.
- Using tiny controls that imitate legacy UI without modern touch targets.

## Closest look-alikes

Aqua is a specific classic macOS visual language with candy-like controls and pinstripes. Glassmorphism is a broader frosted-panel treatment.

## Accessibility and responsive behavior

Modernize target sizes and focus indicators. Gloss must not obscure labels or state. Avoid excessive animation and test contrast over highlights.

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

- NameThatUI style entry: [Aqua](https://namethatui.com/styles/aqua)
- https://developer.apple.com/design/human-interface-guidelines/

Source notes: This file is an independently written implementation guide informed by the linked material. It is not a reproduction of the source page. Verify current platform APIs and licensing before shipping.
