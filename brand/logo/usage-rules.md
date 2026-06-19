# BIKI — Logo Usage Rules

> the mark is presence, not decoration. these rules exist so it stays that way.

---

## 1. Anatomy

the mark is **two filled circles** above a **single horizontal line**.

| element | role | grid units |
|---------|------|------------|
| upper circle | the watcher above | cx=12, cy=8, r=2.5 |
| lower circle | the watcher below | cx=12, cy=18, r=2.5 |
| threshold line | the plane you cross | x=6, y=27, w=12, h=1 |

**base unit (1u)** = the radius of one circle (2.5 units). all measurements derive from this.

the two circles are **vertically stacked**, not horizontally. this is intentional.
vertical alignment reads as **watchful presence** — not a face, not punctuation.
horizontal alignment would read as eyes; vertical reads as **principle**.

the threshold line is **centered beneath the circles**, **narrower than the mark's implied column**.
it is the floor of presence, not the pedestal.

---

## 2. Clear Space

**minimum clear space = 1u** (one base unit) on all four sides.

this equals the radius of one circle. the mark may never be crowded by another element —
type, image, edge of canvas — closer than this.

when in doubt: **more space, not less.** biki is patient. give it room.

---

## 3. Minimum Sizes

| context | minimum |
|---------|---------|
| digital — mark only | **16 × 21 px** |
| digital — wordmark lockup | **96 px wide** |
| digital — recommended | **24 × 32 px** |
| print | **8 mm tall** |

below these sizes, the threshold line becomes a single pixel and loses its meaning.
if you need smaller, use only the wordmark — never squish the mark.

---

## 4. Color

**default**: `currentColor`. the mark inherits its color from the parent element.
this is the only sanctioned color behavior.

| context | color |
|---------|-------|
| light surface | ink (near-black, defined in design tokens) |
| dark surface | bone (off-white, defined in design tokens) |
| accent — sparing only | one brand accent color (defined in design tokens) |

**rules:**
- never use the mark in pure `#000000` or `#FFFFFF` — it must breathe with the palette
- one color only. never two-color, never multi-color, never gradient
- the mark is **monochrome by nature**. color is applied through context, not through the mark

---

## 5. Approved Variants

only these lockups exist:

1. **mark only** — `mark.svg`
2. **wordmark only** — `wordmark.svg`
3. **primary lockup** (mark stacked above wordmark) — `primary-lockup.svg`
4. **horizontal lockup** (mark left, wordmark right) — `horizontal-lockup.svg`

do not invent new arrangements. the existing four cover every need.

**when to use which:**
- mark only → favicon, app icon, small UI moments, watermark
- wordmark only → long body copy, signature use, when space is constrained vertically
- primary lockup → **default for landing pages, decks, marketing**
- horizontal lockup → nav bars, headers, email signatures

---

## 6. Don'ts

the mark is fragile by design. these break it.

### ❌ do not add effects
- no drop shadow
- no glow
- no gradient
- no outline / stroke (the mark is solid by construction)
- no blur
- no skew / 3D transform

### ❌ do not deform
- no stretching non-uniformly
- no squishing
- no rotating (the mark has an upright orientation — gravity is part of the meaning)

### ❌ do not modify geometry
- no separating the elements
- no rearranging (mark stays stacked, threshold stays beneath)
- no filling the circles with different colors
- no changing the line thickness

### ❌ do not place on busy backgrounds
- no photographs without a tonal wash
- no patterns that compete with the threshold line
- no gradients behind the mark
- if in doubt: place on flat surface

### ❌ do not pair with conflicting type
- no display serifs
- no script fonts
- no type with similar geometry that reads as "another mark"
- the wordmark is set; outside type uses the brand type system, never decorative fonts

---

## 7. Voice in Use

the mark should feel like a **period at the end of a sentence**, not an exclamation point.

when placing it:
- give it **room to breathe**
- let it sit on a **quiet surface**
- never center it between two loud elements — it loses authority
- prefer the **upper-left or lower-right** placement in compositions (thresholds have direction)

---

## 8. File Hygiene

- always ship the **SVG** version. PNG only when SVG is impossible (legacy email clients).
- never rasterize and embed in code — use inline SVG or `<img src="mark.svg">`
- all assets live in `/brand/logo/`. do not duplicate into project repos.
- reference by path: `/brand/logo/primary-lockup.svg`

---

## 9. When In Doubt

ask: *would this still feel like a threshold guardian?*

if the answer requires explanation, the design is wrong.
the mark either reads as presence or it doesn't. there is no in-between.