# Vernacular Web

> The exuberant, handmade visual language of early personal websites.

- **Classification:** Retrospective web aesthetic
- **Atlas entry:** [Vernacular Web on NameThatUI](https://namethatui.com/styles/vernacular-web)
- **Research status:** Initial synthesis; verify source links and platform guidance before production use.

## Overview

The exuberant, handmade visual language of early personal websites. Treat this as a visual language with defining signals, not as a rigid component library. Preserve the product's information architecture, behavior, and accessibility while applying the style.

## Defining visual signals

- Tiled wallpaper backgrounds and small repeating textures.
- Animated GIF ornaments, sparkles, badges, and construction signs.
- Guestbooks, visitor counters, webrings, and prev/next badges.
- Centered single-column layouts and default system fonts.
- Rainbow rules, blinking accents, and playful personal content.

## Design system guidance

### Color
Highly variable, often bright, clashing, and personal rather than governed by a strict palette.

### Surfaces and materials
Patterned backgrounds, visible borders, image buttons, and simple HTML-era structures.

### Geometry
Simple boxes, tables, centered columns, and image-based decoration.

### Typography
System serif, sans-serif, or playful display fonts; expressive emphasis is common.

### Motion
Animated GIFs and marquees are historically characteristic; use sparingly in modern implementations.

## Implementation starting point

The following CSS is a starting point, not a complete theme. Adapt tokens, contrast, states, and responsive behavior to the host product.

```css
.vernacular-page {\n  font-family: Georgia, 'Times New Roman', serif;\n  color: #111;\n  background-color: #d8e9ff;\n  background-image: radial-gradient(#fff 1px, transparent 1px);\n  background-size: 18px 18px;\n  text-align: center;\n}\n.vernacular-box { border: 3px ridge #777; padding: 1rem; background: #fff7c7; }
```

## Avoid style drift

- Turning the look into polished retro branding and losing its handmade character.
- Using autoplay audio or motion without user control.
- Confusing vernacular decoration with deliberately raw brutalism.

## Closest look-alikes

Web Brutalism foregrounds raw structure and defaults. Vernacular Web foregrounds personal expression, decorative abundance, and early-web conventions.

## Accessibility and responsive behavior

Do not use flashing content. Provide pause controls for animation, avoid autoplay audio, preserve readable contrast, and ensure responsive behavior despite intentionally old-web styling.

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

- NameThatUI style entry: [Vernacular Web](https://namethatui.com/styles/vernacular-web)
- https://www.w3.org/WAI/WCAG22/Understanding/three-flashes-or-below-threshold.html

Source notes: This file is an independently written implementation guide informed by the linked material. It is not a reproduction of the source page. Verify current platform APIs and licensing before shipping.
