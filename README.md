# BIKI

> the watchful threshold.

a brand and landing site for **biki** — a presence at the plane one crosses to enter.

---

## What is this

this repo contains the brand assets and the public landing page for biki. it's a brand-first site: the landing exists to anchor the identity, not to ship a product.

the site is intentionally restrained. one page. one voice. one mark.

---

## Structure

```
biki/
├── index.html              ← the landing page
├── styles.css              ← landing styles (uses brand tokens)
├── README.md               ← you are here
├── .gitignore
└── brand/
    ├── logo/               ← phase 2 — mark, wordmark, lockups, rules
    │   ├── mark.svg
    │   ├── wordmark.svg
    │   ├── primary-lockup.svg
    │   ├── horizontal-lockup.svg
    │   ├── construction.svg
    │   ├── clear-space.svg
    │   ├── min-sizes.svg
    │   ├── README.md
    │   └── usage-rules.md
    └── design-system/      ← phase 4 — design tokens
        ├── README.md
        ├── tokens.css      ← THE source of truth (CSS custom properties)
        ├── tokens.json     ← JSON export for build tools
        └── swatches.svg    ← visual reference (palette + type + surface)
```

---

## The four phases

| phase | scope | status |
|-------|-------|--------|
| 1 — lore | manifesto, origin, character bible | pending |
| 2 — logo | mark, wordmark, lockups, usage rules | **done** |
| 3 — landing | hero copy, hero structure, sections | **done** (this site) |
| 4 — design system | color, type, spacing, motion, grain tokens | **done** |

the landing (phase 3) sits on top of the design system (phase 4). no token, no surface.

---

## Design principles

- **the mark is monochrome by nature.** so is the system.
- **restraint is the design.** one accent only. it signals threshold, never decoration.
- **hierarchy comes from weight and tracking, not size alone.**
- **spacing is generous.** biki is patient.
- **motion is short and decisive.** no bounce, no spring.
- **surfaces are flat and quiet.** depth from restraint, not shadow.

see `brand/design-system/README.md` for the full philosophy.

---

## Local development

the site is a single static page. no build step.

```bash
# serve locally
python3 -m http.server 8000

# or with any other static server
npx serve .
```

open `http://localhost:8000`.

---

## Deploy

deploys via Vercel. any push to `main` triggers a production deploy.

`biki/` is the project root. Vercel auto-detects the static `index.html`.

---

## Voice

biki writes in lowercase. short sentences. declarative. no exclamations.

```
❌ "Welcome to BIKI!"
✅ "the watchful threshold."

❌ "We're building something amazing."
✅ "BIKI is being prepared."
```

the mark sits like a period at the end of a sentence. so does the copy.

---

## License

the mark and brand assets are © biki. all presence reserved.