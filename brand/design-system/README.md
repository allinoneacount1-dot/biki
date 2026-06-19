# BIKI — Design System

> the tokens. the rules. the surface.

---

## Philosophy

the design system is **the breath of the brand**. tokens are not decoration — they are the grammar biki speaks in.

every value in this system is **restrained by intent**:
- one accent only. it is never decorative — it signals threshold.
- type carries hierarchy through **weight and tracking**, not size alone.
- spacing is **generous**. biki is patient. give it room.
- motion is **short and decisive**. no bounce, no spring, no playful curves.
- surfaces are **flat and quiet**. depth comes from restraint, not shadow.

the mark is monochrome by nature. so is the system.

---

## Structure

```
design-system/
├── README.md       ← you are here (philosophy + usage)
├── tokens.css      ← CSS custom properties (THE source of truth)
├── tokens.json     ← JSON export (build tools, frameworks)
└── swatches.svg    ← visual reference (palette + type + surface)
```

**rule:** if a value isn't defined here, it doesn't exist. don't invent new shades, new sizes, new easings. extend the scale by editing the source — never by adding one-offs in components.

---

## Token Map

### Color
| group | shades | use |
|-------|--------|-----|
| **ink** | 900 / 700 / mute | primary text on bone, ink surfaces |
| **bone** | primary / soft / mute | primary surface, secondary text on ink |
| **ochre** | primary / deep / soft | the one accent — sparing only, threshold moments |

semantic aliases (`surface-*`, `text-*`, `border-*`, `accent-*`) are defined in `tokens.css` for readability. always reference semantic names in components, never raw palette names.

### Typography
- **font-sans:** Inter (matches the wordmark)
- **font-mono:** JetBrains Mono
- **scale:** 10 steps (display-xl → mono)
- **weights:** regular / medium / semibold / bold — bold reserved for hero only

### Spacing
- **base unit:** 4px
- **scale:** 4 / 8 / 12 / 16 / 24 / 32 / 48 / 64 / 96 / 128 / 192
- the mark breathes in 1u units; the system breathes in these.

### Radii
- **default:** 0 (sharp, threshold-like)
- **radius-full:** 9999 (for circular elements that mirror the mark)
- **use radii rarely.** biki doesn't do rounded cards.

### Motion
- **durations:** 80 / 150 / 220 / 400 ms
- **easings:** `ease-out` (default) / `ease-in-out` (transforms only)
- **never:** bounce, spring, elastic, overshoot

### Grain
- **opacity:** 0.025 (2.5%)
- **use:** subtle texture on large flat surfaces — adds depth without noise
- **never:** as a focal element. grain is felt, not seen.

---

## How To Use

### In a plain HTML/CSS project
```html
<link rel="stylesheet" href="path/to/tokens.css">
<link rel="stylesheet" href="your-styles.css">
```
reference any token as `var(--token-name)` in your styles.

### In a framework (React/Vue/Svelte)
import `tokens.json` and resolve at build time, or include `tokens.css` once in your root stylesheet.

### In Figma / design tools
mirror the values manually. there's no Figma library yet — that's a later phase.

---

## Rules

1. **never invent new colors.** if you need a shade not in the palette, the design is wrong. adjust the scale, don't bypass it.
2. **never use weight > 600 outside hero display.** semibold (600) is the heaviest everyday weight.
3. **never use bounce/spring easing.** biki is patient, not playful.
4. **never apply grain to small surfaces.** only on full-bleed areas where the texture has room to breathe.
5. **always reference semantic tokens in components** (`var(--text-on-bone)`), not raw palette tokens (`var(--color-ink)`).

---

## When In Doubt

ask: *would this still feel deliberate?*

if the answer requires explanation, the design is wrong.
restraint is the design.