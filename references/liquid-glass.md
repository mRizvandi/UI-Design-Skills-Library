# Liquid Glass

> Apple's adaptive glass material belongs to the floating control layer, not the content itself.

- **Classification:** Vendor design language
- **Atlas entry:** [Liquid Glass on NameThatUI](https://namethatui.com/styles/liquid-glass)
- **Research status:** Initial synthesis; verify source links and platform guidance before production use.

## Overview

Apple's adaptive glass material belongs to the floating control layer, not the content itself. Treat this as a visual language with defining signals, not as a rigid component library. Preserve the product's information architecture, behavior, and accessibility while applying the style.

## Defining visual signals

- Glass is reserved for toolbars, tab bars, buttons, sliders, and floating controls.
- Lens-like highlights and refraction-inspired edges go beyond simple blur.
- Material adapts tint and appearance to changing content beneath it.
- Capsule forms and concentric corner radii are common.
- Underlying content remains opaque and legible.

## Design system guidance

### Color
Adaptive tint should respond to content and light/dark contexts; web approximations need explicit contrast safeguards.

### Surfaces and materials
On Apple platforms prefer native system APIs. On the web, approximate with blur, saturation, inner highlights, and carefully tested tint.

### Geometry
Capsules and concentric radii help controls sit optically within their containers.

### Typography
Keep text and symbols readable over every possible underlying content region.

### Motion
Morphing and fluid transitions may connect related controls; respect reduced-motion settings.

## Implementation starting point

The following CSS is a starting point, not a complete theme. Adapt tokens, contrast, states, and responsive behavior to the host product.

```css
.liquid-control {\n  background: rgba(255,255,255,.16);\n  -webkit-backdrop-filter: blur(14px) saturate(1.6);\n  backdrop-filter: blur(14px) saturate(1.6);\n  border: 1px solid rgba(255,255,255,.38);\n  border-radius: 999px;\n  box-shadow: inset 0 1px 1px rgba(255,255,255,.45), 0 8px 24px rgba(0,0,0,.14);\n}
```

## Avoid style drift

- Turning content cards into glass panels; that shifts toward Glassmorphism.
- Claiming CSS blur reproduces true optical refraction.
- Using an adaptive-looking surface without testing light and dark content behind it.

## Closest look-alikes

Glassmorphism is a decorative frosted treatment that may cover content cards. Liquid Glass is a functional, adaptive material reserved primarily for controls floating above content.

## Accessibility and responsive behavior

Native materials adapt automatically, but custom web imitations do not. Test worst-case backgrounds, preserve focus states, and honor reduced transparency and reduced motion.

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

- NameThatUI style entry: [Liquid Glass](https://namethatui.com/styles/liquid-glass)
- https://developer.apple.com/design/
- https://developer.apple.com/design/human-interface-guidelines/

Source notes: This file is an independently written implementation guide informed by the linked material. It is not a reproduction of the source page. Verify current platform APIs and licensing before shipping.
