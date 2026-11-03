# Web Brutalism

> Expose the web page's raw structure and browser-default character instead of polishing it.

- **Classification:** Contested label
- **Atlas entry:** [Web Brutalism on NameThatUI](https://namethatui.com/styles/web-brutalism)
- **Research status:** Initial synthesis; verify source links and platform guidance before production use.

## Overview

Expose the web page's raw structure and browser-default character instead of polishing it. Treat this as a visual language with defining signals, not as a rigid component library. Preserve the product's information architecture, behavior, and accessibility while applying the style.

## Defining visual signals

- Browser-default or minimally styled typography and controls.
- Plain links, visible document structure, and straightforward flow.
- Little or no decorative rendering.
- A deliberately unpolished, direct, sometimes awkward composition.
- Content and structure are foregrounded over visual refinement.

## Design system guidance

### Color
Often defaults such as black text, white background, and conventional link colors; variation is possible.

### Surfaces and materials
Avoid ornamental layers, polished cards, gradients, and decorative shadows.

### Geometry
Use document flow and simple structural divisions rather than a component-heavy visual system.

### Typography
System defaults or intentionally plain type are part of the visual language.

### Motion
Usually minimal; avoid unnecessary animation.

## Implementation starting point

The following CSS is a starting point, not a complete theme. Adapt tokens, contrast, states, and responsive behavior to the host product.

```css
/* Intentionally minimal styling: preserve semantic HTML and native behavior. */\n.brutalist-document {\n  font: 16px/1.45 Georgia, serif;\n  color: #111;\n  background: #fff;\n  max-width: 72ch;\n  margin: 2rem auto;\n  padding: 1rem;\n}\n.brutalist-document a { color: #00e; text-decoration: underline; }
```

## Avoid style drift

- Adding thick graphic borders and hard offset shadows; that is closer to Neobrutalism.
- Mistaking broken usability for authenticity.
- Removing semantic HTML or accessibility.
- Using rawness without a clear content hierarchy.

## Closest look-alikes

Neobrutalism is deliberately stylized with thick black outlines, saturated blocks, and hard offset shadows. Web Brutalism often exposes browser-default structure instead of exaggerating decoration.

## Accessibility and responsive behavior

Raw appearance does not excuse poor semantics. Keep keyboard operation, meaningful headings, focus indicators, readable line length, and responsive reflow.

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

- NameThatUI style entry: [Web Brutalism](https://namethatui.com/styles/web-brutalism)
- https://www.nngroup.com/articles/brutalism-antidesign/

Source notes: This file is an independently written implementation guide informed by the linked material. It is not a reproduction of the source page. Verify current platform APIs and licensing before shipping.
