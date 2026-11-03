# Windows Aero

> The Windows Vista/7 glass-window language: translucent frames, reflections, and luminous controls.

- **Classification:** Vendor design language
- **Atlas entry:** [Windows Aero on NameThatUI](https://namethatui.com/styles/windows-aero)
- **Research status:** Initial synthesis; verify source links and platform guidance before production use.

## Overview

The Windows Vista/7 glass-window language: translucent frames, reflections, and luminous controls. Treat this as a visual language with defining signals, not as a rigid component library. Preserve the product's information architecture, behavior, and accessibility while applying the style.

## Defining visual signals

- Transparent, blurred window frames that reveal the desktop behind.
- Specular sweeps and reflective highlights along frame edges.
- Glowing, hot-tracked controls and luminous accents.
- Layered desktop windows and a sense of spatial depth.
- Cool blue, charcoal, and glass-like neutrals.

## Design system guidance

### Color
Cool blue, silver, charcoal, and white highlights; desktop wallpaper contributes ambient color.

### Surfaces and materials
Translucent window chrome and blurred frame material, distinct from content surfaces.

### Geometry
Window frames, title bars, rounded corners, and clearly separated content panes.

### Typography
Compact system-style sans-serif typography with high legibility.

### Motion
Subtle window transitions and hover glows; avoid distracting effects.

## Implementation starting point

The following CSS is a starting point, not a complete theme. Adapt tokens, contrast, states, and responsive behavior to the host product.

```css
.aero-frame {\n  background: rgba(225, 242, 255, .48);\n  -webkit-backdrop-filter: blur(18px);\n  backdrop-filter: blur(18px);\n  border: 1px solid rgba(255,255,255,.7);\n  box-shadow: inset 0 1px rgba(255,255,255,.8), 0 12px 30px rgba(0,20,50,.22);\n}
```

## Avoid style drift

- Applying blur indiscriminately to content and controls.
- Confusing Aero's desktop window chrome with generic glassmorphism.
- Using glow as the only hover or focus signal.

## Closest look-alikes

Windows Aero is a specific desktop OS design language centered on translucent window frames. Glassmorphism generalizes frosted surfaces to arbitrary interface cards and panels.

## Accessibility and responsive behavior

Keep content surfaces opaque enough for reading. Provide fallbacks when backdrop blur is unavailable and visible focus indicators independent of glow.

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

- NameThatUI style entry: [Windows Aero](https://namethatui.com/styles/windows-aero)
- https://learn.microsoft.com/en-us/windows/apps/design/

Source notes: This file is an independently written implementation guide informed by the linked material. It is not a reproduction of the source page. Verify current platform APIs and licensing before shipping.
