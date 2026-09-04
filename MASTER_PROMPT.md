# scupstatefoundation.org — Emergent Master Build Prompt

## Live Site Reference

**Live site:** https://scupstatefoundation.org
**Reference for:** full_reference

Copy guidance: Preserve copy that works, improve what doesn't.

## Answer Provenance — read this before treating anything below as a decision

⚠️ **The other 3 answers are DEFAULTS.** Nobody chose them. They are a starting point to confirm, never a decision already made, and where one of them contradicts something the client did say, **the client wins**:

`q19`, `q20`, `q21`

---


> ⚠️ **BUILD MODE: EXACT REBUILD**
>
> This is a pixel-faithful reconstruction of an existing site — **not a redesign**.
> Every layout decision, section order, color choice, and typographic detail in this
> document reflects the live site as it exists today.
>
> **Do NOT:**
> - Modernize, simplify, or "improve" the layout
> - Reorder or remove sections
> - Substitute fonts, colors, or spacing
> - Add features or sections not present on the live site
>
> **Do:**
> - Match the screenshots as closely as possible — treat them as the build spec
> - Preserve the section rhythm (dark/light alternation, full-bleed photos, etc.)
> - Replicate the exact component hierarchy described in "Page Structure" below
>
> Reference the live site at https://scupstatefoundation.org to fill in any gaps.

**Generated:** September 1, 2026
**Source:** https://scupstatefoundation.org (wordpress 7.1)
**Extraction:** 42 pages, 21 screenshots, 413 assets (39.4MB)

---

## ⭐ Implementation Notes

## Recurring Visual Motifs

**Photo backgrounds** — 1 sections use full-bleed photography as backgrounds. Typically overlaid with a semi-transparent color layer for text legibility.

## Page Structure Pattern

**Dark-dominant layout** — Most sections (1 of 1) use dark backgrounds. This is a brand aesthetic choice, not an accessibility issue.

## Implementation Notes for Emergent

- Load **Oswald** as the display/heading font. Verify it's self-hosted or confirmed Google Fonts — check downloads/ in emergent-package.
- Load **-apple-system** for body copy and UI elements.
- Apply heading style utilities: `uppercase` to heading classes globally.

---


---

## Project Brief

*(describe the desired feeling — trustworthy, premium, exciting, etc.)*

**Design standard:** Every page must feel **luxury and premium** — polished, intentional, unhurried.
This is not a template site. Photography is the hero. Whitespace is earned. Details matter.
If something looks generic or SaaS-y, it's wrong.

---

## 🎨 Creative Direction

> ⚠️ **This section must be completed by Roy/team before handing to Emergent.**
> The extractor captures what it can — the rest is human creative direction.

### Soul Statement
> *(Not captured — Roy, add one sentence here: when someone lands on this site, what should they feel in the first 5 seconds?)*

### Aesthetic Language
*(Specific words and phrases the team uses to describe this brand's feeling — not what it does, but what it feels like)*

*(Roy/Trey — add 3-5 evocative phrases here before build starts. Example: 'Sunday afternoon kitchen light, neighbors not strangers, earned trust, warm and unhurried')*

### Color Rationale
*(Why each confirmed color — the emotion it carries, not just its role. Fill in before handing to Emergent.)*

| Hex | Role | Why this color |
|-----|------|----------------|
| `#85b559` | Brand color | *(add emotional rationale)* |
| `#001e53` | Brand color | *(add emotional rationale)* |
| `#334155` | Brand color | *(add emotional rationale)* |
| `#666666` | Brand color | *(add emotional rationale)* |
| `#ffffff` | Brand color | *(add emotional rationale)* |
| `#000000` | Brand color | *(add emotional rationale)* |

### Typography Rationale
*(Why each font — what personality it projects for this brand. Fill in before handing to Emergent.)*

- **Gilroy Semibold** (Heading) — *(add rationale)*
- **Gilroy Regular** (Body) — *(add rationale)*

### Physical Object Reference
*(If this site were a physical object, what would it be? This locks the layout direction. Example: 'a community cookbook' or 'a civic pamphlet' or 'a coffee table book')*

*(Roy/Trey — fill in before build starts)*

### Homepage Directions

Build **3 homepage directions** — distinct visual approaches using the same brand, content, and fonts. Client selects one to develop fully.

> ⚠︎ **This count is a generator default, not a decision anyone made** (no bound answer and no questionnaire answer). If the client has said a number, bind it.

**Each direction needs:** concept name · layout metaphor · emotional hook · hero treatment · color weighting

**Direction 1:** *(Roy/Trey — name it and describe it)*

**Direction 2:** *(Roy/Trey — name it and describe it)*

**Direction 3:** *(Roy/Trey — name it and describe it)*

---

## Target Audience

*(describe the ideal buyer — age, lifestyle, motivation, what they're leaving behind)*

---

## #1 Conversion Goal

***(primary CTA — schedule a tour, call, buy, etc.)***

This CTA should appear in the hero, in the nav, and at the bottom of every core page.

---

## Current Site — Keep vs. Fix

**What works:**
*(what to preserve from the current site)*

**What to fix:**
*(biggest problems to solve)*

---

## Design System

### Brand Colors

| Hex | Token | Usage |
|-----|-------|-------|
| `#ffffff` | `--color-white` | White — text on dark, light section backgrounds |
| `#000000` | `--color-black` | Black — text on white |
| `#85b559` | `--color-neutral-1` | Neutral |
| `#001e53` | `--color-neutral-2` | Neutral |
| `#334155` | `--color-neutral-3` | Neutral |
| `#666666` | `--color-neutral-4` | Neutral |
| `#cccccc` | `--color-neutral-7` | Neutral |

⚠️ Verify palette with client before finalizing.

⚠️ **Artifact colors detected** (in CSS but not visible in screenshots — likely plugin/admin defaults): `#4b3fe1`, `#07b787`, `#7ed500`, `#21759b`, `#4d68ff`. Do NOT use these in the rebuild.

🔍 **Review manually** (borderline — may be small UI elements): `#046bd2`, `#ff6900`, `#0693e3`.

**Avoid** any colors not in this table — verify any additions with client.

**Critical color roles — do not swap these:**
- **CTA buttons, nav bar, dark panels** → `--color-primary` (the darkest brand color)
- **Nature accents, secondary highlights only** → `--color-green` (lighter green — NOT for buttons or primary UI)
- When in doubt: darker = more premium. Default to `--color-primary`.

**CSS custom properties** — define these once in your global stylesheet:

```css
:root {
  --color-white: #ffffff;  /* White — text on dark, light section backgrounds */
  --color-black: #000000;  /* Black — text on white */
  --color-neutral-1: #85b559;  /* Neutral */
  --color-neutral-2: #001e53;  /* Neutral */
  --color-neutral-3: #334155;  /* Neutral */
  --color-neutral-4: #666666;  /* Neutral */
  --color-neutral-7: #cccccc;  /* Neutral */
}
```

_Use these tokens everywhere — never hardcode hex values in components._

### Typography

⚠️ Verify font choices with client.

#### Font Roles
| Role | Font |
|------|------|
| **Headings (H1–H6)** | `Gilroy Semibold` |
| **Body copy / paragraphs** | `Gilroy Regular` |



#### Font Loading

Load brand fonts via `@font-face` in `app/globals.css` from local files downloaded from Drive or committed under `downloads/fonts/`. Source URLs are extraction evidence only; do not hotlink live-site or CDN font URLs in runtime code.

```css
/* Font sources detected during extraction. Prefer local files from public/assets/fonts/ or downloads/fonts/ when available. */
@font-face {
  font-family: 'Gilroy';
  src: url('https://scupstatefoundation.org/wp-content/uploads/2025/07/Gilroy-Regular.ttf') format('truetype');
  font-weight: 400;
  font-style: normal;
  font-display: swap;
}
@font-face {
  font-family: 'Gilroy';
  src: url('https://scupstatefoundation.org/wp-content/uploads/2025/07/Gilroy-Medium.ttf') format('truetype');
  font-weight: 500;
  font-style: normal;
  font-display: swap;
}
@font-face {
  font-family: 'Gilroy';
  src: url('https://scupstatefoundation.org/wp-content/uploads/2025/07/Gilroy-SemiBold.ttf') format('truetype');
  font-weight: 600;
  font-style: normal;
  font-display: swap;
}
@font-face {
  font-family: 'Gilroy';
  src: url('https://scupstatefoundation.org/wp-content/uploads/2025/07/Gilroy-Bold.ttf') format('truetype');
  font-weight: 700;
  font-style: normal;
  font-display: swap;
}
@font-face {
  font-family: 'Nunito';
  src: url('http://demo.webenixsolutions.com/Upstate-Education/wp-content/uploads/elementor/google-fonts/fonts/nunito-xrxx3i6li01bkofimnaors71ca.woff2') format('woff2');
  font-weight: 200;
  font-style: italic;
  font-display: swap;
}
@font-face {
  font-family: 'Nunito';
  src: url('http://demo.webenixsolutions.com/Upstate-Education/wp-content/uploads/elementor/google-fonts/fonts/nunito-xrxx3i6li01bkofimnaors71ca.woff2') format('woff2');
  font-weight: 300;
  font-style: italic;
  font-display: swap;
}
@font-face {
  font-family: 'Nunito';
  src: url('http://demo.webenixsolutions.com/Upstate-Education/wp-content/uploads/elementor/google-fonts/fonts/nunito-xrxx3i6li01bkofimnaors71ca.woff2') format('woff2');
  font-weight: 400;
  font-style: italic;
  font-display: swap;
}
@font-face {
  font-family: 'Nunito';
  src: url('http://demo.webenixsolutions.com/Upstate-Education/wp-content/uploads/elementor/google-fonts/fonts/nunito-xrxx3i6li01bkofimnaors71ca.woff2') format('woff2');
  font-weight: 500;
  font-style: italic;
  font-display: swap;
}
@font-face {
  font-family: 'Nunito';
  src: url('http://demo.webenixsolutions.com/Upstate-Education/wp-content/uploads/elementor/google-fonts/fonts/nunito-xrxx3i6li01bkofimnaors71ca.woff2') format('woff2');
  font-weight: 600;
  font-style: italic;
  font-display: swap;
}
@font-face {
  font-family: 'Nunito';
  src: url('http://demo.webenixsolutions.com/Upstate-Education/wp-content/uploads/elementor/google-fonts/fonts/nunito-xrxx3i6li01bkofimnaors71ca.woff2') format('woff2');
  font-weight: 700;
  font-style: italic;
  font-display: swap;
}
@font-face {
  font-family: 'Nunito';
  src: url('http://demo.webenixsolutions.com/Upstate-Education/wp-content/uploads/elementor/google-fonts/fonts/nunito-xrxx3i6li01bkofimnaors71ca.woff2') format('woff2');
  font-weight: 800;
  font-style: italic;
  font-display: swap;
}
@font-face {
  font-family: 'Nunito';
  src: url('http://demo.webenixsolutions.com/Upstate-Education/wp-content/uploads/elementor/google-fonts/fonts/nunito-xrxx3i6li01bkofimnaors71ca.woff2') format('woff2');
  font-weight: 900;
  font-style: italic;
  font-display: swap;
}
@font-face {
  font-family: 'Titillium Web';
  src: url('http://demo.webenixsolutions.com/Upstate-Education/wp-content/uploads/elementor/google-fonts/fonts/titilliumweb-napfcztiaohvxomyor9n_e7fdmbewi1db5yciwm.woff2') format('woff2');
  font-weight: 200;
  font-style: italic;
  font-display: swap;
}
@font-face {
  font-family: 'Titillium Web';
  src: url('http://demo.webenixsolutions.com/Upstate-Education/wp-content/uploads/elementor/google-fonts/fonts/titilliumweb-napfcztiaohvxomyor9n_e7fdmbepi5db5yciwm.woff2') format('woff2');
  font-weight: 300;
  font-style: italic;
  font-display: swap;
}
@font-face {
  font-family: 'Titillium Web';
  src: url('http://demo.webenixsolutions.com/Upstate-Education/wp-content/uploads/elementor/google-fonts/fonts/titilliumweb-napacztiaohvxomyor9n_e7fdmbwaaxwxr0.woff2') format('woff2');
  font-weight: 400;
  font-style: italic;
  font-display: swap;
}
@font-face {
  font-family: 'Titillium Web';
  src: url('http://demo.webenixsolutions.com/Upstate-Education/wp-content/uploads/elementor/google-fonts/fonts/titilliumweb-napfcztiaohvxomyor9n_e7fdmbe0ihdb5yciwm.woff2') format('woff2');
  font-weight: 600;
  font-style: italic;
  font-display: swap;
}
@font-face {
  font-family: 'Titillium Web';
  src: url('http://demo.webenixsolutions.com/Upstate-Education/wp-content/uploads/elementor/google-fonts/fonts/titilliumweb-napfcztiaohvxomyor9n_e7fdmbetildb5yciwm.woff2') format('woff2');
  font-weight: 700;
  font-style: italic;
  font-display: swap;
}
@font-face {
  font-family: 'Titillium Web';
  src: url('http://demo.webenixsolutions.com/Upstate-Education/wp-content/uploads/elementor/google-fonts/fonts/titilliumweb-napdcztiaohvxomyor9n_e7ffedbgivzy4sy.woff2') format('woff2');
  font-weight: 900;
  font-style: normal;
  font-display: swap;
}
@font-face {
  font-family: 'elementskit';
  src: url('../fonts/elementskit.woff?itek3h') format('woff');
  font-weight: 400;
  font-style: normal;
  font-display: swap;
}
@font-face {
  font-family: 'Questrial';
  src: url('https://fonts.gstatic.com/s/questrial/v19/QdVUSTchPBm7nuUeVf70sSFluW44JUcz.woff2') format('woff2');
  font-weight: 400;
  font-style: normal;
  font-display: swap;
}
@font-face {
  font-family: 'Montserrat';
  src: url('http://demo.webenixsolutions.com/Upstate-Education/wp-content/uploads/elementor/google-fonts/fonts/montserrat-jtuqjig1_i6t8kchkm459wxrxc7mw9c.woff2') format('woff2');
  font-weight: 100;
  font-style: italic;
  font-display: swap;
}
@font-face {
  font-family: 'Montserrat';
  src: url('http://demo.webenixsolutions.com/Upstate-Education/wp-content/uploads/elementor/google-fonts/fonts/montserrat-jtuqjig1_i6t8kchkm459wxrxc7mw9c.woff2') format('woff2');
  font-weight: 200;
  font-style: italic;
  font-display: swap;
}
@font-face {
  font-family: 'Montserrat';
  src: url('http://demo.webenixsolutions.com/Upstate-Education/wp-content/uploads/elementor/google-fonts/fonts/montserrat-jtuqjig1_i6t8kchkm459wxrxc7mw9c.woff2') format('woff2');
  font-weight: 300;
  font-style: italic;
  font-display: swap;
}
@font-face {
  font-family: 'Montserrat';
  src: url('http://demo.webenixsolutions.com/Upstate-Education/wp-content/uploads/elementor/google-fonts/fonts/montserrat-jtuqjig1_i6t8kchkm459wxrxc7mw9c.woff2') format('woff2');
  font-weight: 400;
  font-style: italic;
  font-display: swap;
}
@font-face {
  font-family: 'Montserrat';
  src: url('http://demo.webenixsolutions.com/Upstate-Education/wp-content/uploads/elementor/google-fonts/fonts/montserrat-jtuqjig1_i6t8kchkm459wxrxc7mw9c.woff2') format('woff2');
  font-weight: 500;
  font-style: italic;
  font-display: swap;
}
@font-face {
  font-family: 'Montserrat';
  src: url('http://demo.webenixsolutions.com/Upstate-Education/wp-content/uploads/elementor/google-fonts/fonts/montserrat-jtuqjig1_i6t8kchkm459wxrxc7mw9c.woff2') format('woff2');
  font-weight: 600;
  font-style: italic;
  font-display: swap;
}
@font-face {
  font-family: 'Montserrat';
  src: url('http://demo.webenixsolutions.com/Upstate-Education/wp-content/uploads/elementor/google-fonts/fonts/montserrat-jtuqjig1_i6t8kchkm459wxrxc7mw9c.woff2') format('woff2');
  font-weight: 700;
  font-style: italic;
  font-display: swap;
}
@font-face {
  font-family: 'Montserrat';
  src: url('http://demo.webenixsolutions.com/Upstate-Education/wp-content/uploads/elementor/google-fonts/fonts/montserrat-jtuqjig1_i6t8kchkm459wxrxc7mw9c.woff2') format('woff2');
  font-weight: 800;
  font-style: italic;
  font-display: swap;
}
@font-face {
  font-family: 'Montserrat';
  src: url('http://demo.webenixsolutions.com/Upstate-Education/wp-content/uploads/elementor/google-fonts/fonts/montserrat-jtuqjig1_i6t8kchkm459wxrxc7mw9c.woff2') format('woff2');
  font-weight: 900;
  font-style: italic;
  font-display: swap;
}
@font-face {
  font-family: 'Oswald';
  src: url('http://demo.webenixsolutions.com/Upstate-Education/wp-content/uploads/elementor/google-fonts/fonts/oswald-tk3iwkuhhaijg752fd8ghe4.woff2') format('woff2');
  font-weight: 200;
  font-style: normal;
  font-display: swap;
}
@font-face {
  font-family: 'Oswald';
  src: url('http://demo.webenixsolutions.com/Upstate-Education/wp-content/uploads/elementor/google-fonts/fonts/oswald-tk3iwkuhhaijg752fd8ghe4.woff2') format('woff2');
  font-weight: 300;
  font-style: normal;
  font-display: swap;
}
@font-face {
  font-family: 'Oswald';
  src: url('http://demo.webenixsolutions.com/Upstate-Education/wp-content/uploads/elementor/google-fonts/fonts/oswald-tk3iwkuhhaijg752fd8ghe4.woff2') format('woff2');
  font-weight: 400;
  font-style: normal;
  font-display: swap;
}
@font-face {
  font-family: 'Oswald';
  src: url('http://demo.webenixsolutions.com/Upstate-Education/wp-content/uploads/elementor/google-fonts/fonts/oswald-tk3iwkuhhaijg752fd8ghe4.woff2') format('woff2');
  font-weight: 500;
  font-style: normal;
  font-display: swap;
}
@font-face {
  font-family: 'Oswald';
  src: url('http://demo.webenixsolutions.com/Upstate-Education/wp-content/uploads/elementor/google-fonts/fonts/oswald-tk3iwkuhhaijg752fd8ghe4.woff2') format('woff2');
  font-weight: 600;
  font-style: normal;
  font-display: swap;
}
@font-face {
  font-family: 'Oswald';
  src: url('http://demo.webenixsolutions.com/Upstate-Education/wp-content/uploads/elementor/google-fonts/fonts/oswald-tk3iwkuhhaijg752fd8ghe4.woff2') format('woff2');
  font-weight: 700;
  font-style: normal;
  font-display: swap;
}
@font-face {
  font-family: 'Roboto Slab';
  src: url('http://demo.webenixsolutions.com/Upstate-Education/wp-content/uploads/elementor/google-fonts/fonts/robotoslab-bngmuxzytxpivibgjjsb6ufa5qw54a.woff2') format('woff2');
  font-weight: 100;
  font-style: normal;
  font-display: swap;
}
@font-face {
  font-family: 'Roboto Slab';
  src: url('http://demo.webenixsolutions.com/Upstate-Education/wp-content/uploads/elementor/google-fonts/fonts/robotoslab-bngmuxzytxpivibgjjsb6ufa5qw54a.woff2') format('woff2');
  font-weight: 200;
  font-style: normal;
  font-display: swap;
}
@font-face {
  font-family: 'Roboto Slab';
  src: url('http://demo.webenixsolutions.com/Upstate-Education/wp-content/uploads/elementor/google-fonts/fonts/robotoslab-bngmuxzytxpivibgjjsb6ufa5qw54a.woff2') format('woff2');
  font-weight: 300;
  font-style: normal;
  font-display: swap;
}
@font-face {
  font-family: 'Roboto Slab';
  src: url('http://demo.webenixsolutions.com/Upstate-Education/wp-content/uploads/elementor/google-fonts/fonts/robotoslab-bngmuxzytxpivibgjjsb6ufa5qw54a.woff2') format('woff2');
  font-weight: 400;
  font-style: normal;
  font-display: swap;
}
@font-face {
  font-family: 'Roboto Slab';
  src: url('http://demo.webenixsolutions.com/Upstate-Education/wp-content/uploads/elementor/google-fonts/fonts/robotoslab-bngmuxzytxpivibgjjsb6ufa5qw54a.woff2') format('woff2');
  font-weight: 500;
  font-style: normal;
  font-display: swap;
}
@font-face {
  font-family: 'Roboto Slab';
  src: url('http://demo.webenixsolutions.com/Upstate-Education/wp-content/uploads/elementor/google-fonts/fonts/robotoslab-bngmuxzytxpivibgjjsb6ufa5qw54a.woff2') format('woff2');
  font-weight: 600;
  font-style: normal;
  font-display: swap;
}
@font-face {
  font-family: 'Roboto Slab';
  src: url('http://demo.webenixsolutions.com/Upstate-Education/wp-content/uploads/elementor/google-fonts/fonts/robotoslab-bngmuxzytxpivibgjjsb6ufa5qw54a.woff2') format('woff2');
  font-weight: 700;
  font-style: normal;
  font-display: swap;
}
@font-face {
  font-family: 'Roboto Slab';
  src: url('http://demo.webenixsolutions.com/Upstate-Education/wp-content/uploads/elementor/google-fonts/fonts/robotoslab-bngmuxzytxpivibgjjsb6ufa5qw54a.woff2') format('woff2');
  font-weight: 800;
  font-style: normal;
  font-display: swap;
}
@font-face {
  font-family: 'Roboto Slab';
  src: url('http://demo.webenixsolutions.com/Upstate-Education/wp-content/uploads/elementor/google-fonts/fonts/robotoslab-bngmuxzytxpivibgjjsb6ufa5qw54a.woff2') format('woff2');
  font-weight: 900;
  font-style: normal;
  font-display: swap;
}
@font-face {
  font-family: 'Poppins';
  src: url('https://fonts.gstatic.com/s/poppins/v24/pxiAyp8kv8JHgFVrJJLmE0tDMPKhSkFEkm8.woff2') format('woff2');
  font-weight: 100;
  font-style: italic;
  font-display: swap;
}
@font-face {
  font-family: 'Poppins';
  src: url('https://fonts.gstatic.com/s/poppins/v24/pxiDyp8kv8JHgFVrJJLmv1pVFteOYktMqlap.woff2') format('woff2');
  font-weight: 200;
  font-style: italic;
  font-display: swap;
}
@font-face {
  font-family: 'Poppins';
  src: url('https://fonts.gstatic.com/s/poppins/v24/pxiDyp8kv8JHgFVrJJLm21lVFteOYktMqlap.woff2') format('woff2');
  font-weight: 300;
  font-style: italic;
  font-display: swap;
}
@font-face {
  font-family: 'Poppins';
  src: url('https://fonts.gstatic.com/s/poppins/v24/pxiGyp8kv8JHgFVrJJLucXtAOvWDSHFF.woff2') format('woff2');
  font-weight: 400;
  font-style: italic;
  font-display: swap;
}
@font-face {
  font-family: 'Poppins';
  src: url('https://fonts.gstatic.com/s/poppins/v24/pxiDyp8kv8JHgFVrJJLmg1hVFteOYktMqlap.woff2') format('woff2');
  font-weight: 500;
  font-style: italic;
  font-display: swap;
}
@font-face {
  font-family: 'Poppins';
  src: url('https://fonts.gstatic.com/s/poppins/v24/pxiDyp8kv8JHgFVrJJLmr19VFteOYktMqlap.woff2') format('woff2');
  font-weight: 600;
  font-style: italic;
  font-display: swap;
}
@font-face {
  font-family: 'Poppins';
  src: url('https://fonts.gstatic.com/s/poppins/v24/pxiDyp8kv8JHgFVrJJLmy15VFteOYktMqlap.woff2') format('woff2');
  font-weight: 700;
  font-style: italic;
  font-display: swap;
}
@font-face {
  font-family: 'Poppins';
  src: url('https://fonts.gstatic.com/s/poppins/v24/pxiDyp8kv8JHgFVrJJLm111VFteOYktMqlap.woff2') format('woff2');
  font-weight: 800;
  font-style: italic;
  font-display: swap;
}
@font-face {
  font-family: 'Poppins';
  src: url('https://fonts.gstatic.com/s/poppins/v24/pxiDyp8kv8JHgFVrJJLm81xVFteOYktMqlap.woff2') format('woff2');
  font-weight: 900;
  font-style: italic;
  font-display: swap;
}
@font-face {
  font-family: 'Roboto';
  src: url('http://demo.webenixsolutions.com/Upstate-Education/wp-content/uploads/elementor/google-fonts/fonts/roboto-kfo5cnqeu92fr1mu53zec9_vu3r1gihoszmkc3kawzu.woff2') format('woff2');
  font-weight: 100;
  font-style: italic;
  font-display: swap;
}
@font-face {
  font-family: 'Roboto';
  src: url('http://demo.webenixsolutions.com/Upstate-Education/wp-content/uploads/elementor/google-fonts/fonts/roboto-kfo5cnqeu92fr1mu53zec9_vu3r1gihoszmkc3kawzu.woff2') format('woff2');
  font-weight: 200;
  font-style: italic;
  font-display: swap;
}
@font-face {
  font-family: 'Roboto';
  src: url('http://demo.webenixsolutions.com/Upstate-Education/wp-content/uploads/elementor/google-fonts/fonts/roboto-kfo5cnqeu92fr1mu53zec9_vu3r1gihoszmkc3kawzu.woff2') format('woff2');
  font-weight: 300;
  font-style: italic;
  font-display: swap;
}
@font-face {
  font-family: 'Roboto';
  src: url('http://demo.webenixsolutions.com/Upstate-Education/wp-content/uploads/elementor/google-fonts/fonts/roboto-kfo5cnqeu92fr1mu53zec9_vu3r1gihoszmkc3kawzu.woff2') format('woff2');
  font-weight: 400;
  font-style: italic;
  font-display: swap;
}
@font-face {
  font-family: 'Roboto';
  src: url('http://demo.webenixsolutions.com/Upstate-Education/wp-content/uploads/elementor/google-fonts/fonts/roboto-kfo5cnqeu92fr1mu53zec9_vu3r1gihoszmkc3kawzu.woff2') format('woff2');
  font-weight: 500;
  font-style: italic;
  font-display: swap;
}
@font-face {
  font-family: 'Roboto';
  src: url('http://demo.webenixsolutions.com/Upstate-Education/wp-content/uploads/elementor/google-fonts/fonts/roboto-kfo5cnqeu92fr1mu53zec9_vu3r1gihoszmkc3kawzu.woff2') format('woff2');
  font-weight: 600;
  font-style: italic;
  font-display: swap;
}
@font-face {
  font-family: 'Roboto';
  src: url('http://demo.webenixsolutions.com/Upstate-Education/wp-content/uploads/elementor/google-fonts/fonts/roboto-kfo5cnqeu92fr1mu53zec9_vu3r1gihoszmkc3kawzu.woff2') format('woff2');
  font-weight: 700;
  font-style: italic;
  font-display: swap;
}
@font-face {
  font-family: 'Roboto';
  src: url('http://demo.webenixsolutions.com/Upstate-Education/wp-content/uploads/elementor/google-fonts/fonts/roboto-kfo5cnqeu92fr1mu53zec9_vu3r1gihoszmkc3kawzu.woff2') format('woff2');
  font-weight: 800;
  font-style: italic;
  font-display: swap;
}
@font-face {
  font-family: 'Roboto';
  src: url('http://demo.webenixsolutions.com/Upstate-Education/wp-content/uploads/elementor/google-fonts/fonts/roboto-kfo5cnqeu92fr1mu53zec9_vu3r1gihoszmkc3kawzu.woff2') format('woff2');
  font-weight: 900;
  font-style: italic;
  font-display: swap;
}
@font-face {
  font-family: 'Oswald';
  src: url('https://fonts.gstatic.com/s/oswald/v57/TK3iWkUHHAIjg752FD8Gl-1PK62t.woff2') format('woff2');
  font-weight: 200 700;
  font-style: normal;
  font-display: swap;
}
@font-face {
  font-family: 'Nunito';
  src: url('https://fonts.gstatic.com/s/nunito/v32/XRXX3I6Li01BKofIMNaORs7nczIHNHI.woff2') format('woff2');
  font-weight: 200 1000;
  font-style: italic;
  font-display: swap;
}
```

**⚠️ Critical:** Never silently substitute a system font for any brand font. Commercial fonts (flagged above) must be flagged to the client before building.

### Layout
- Mobile-first responsive
- Full-bleed imagery where appropriate
- Primary CTA prominent on every page

**Responsive breakpoints:**
- `766px` — layout collapses (multi-col → single-col)
- `600px` — mobile — reduced typography, stacked layout

_Match these breakpoints in Tailwind config or CSS media queries. Do not use arbitrary breakpoints._

---



## Site Architecture

### Current Navigation (4 items)
  1. Home → https://scupstatefoundation.org/
  2. About → https://scupstatefoundation.org/about/
  3. Our Initiatives → https://scupstatefoundation.org/our-initiatives/
  4. Impact Stories → https://scupstatefoundation.org/impact-story/

### Current Pages (42 total)
  - Share Your Treasure → /share-your-treasure/
  - Share Your Talent → /share-your-talent/
  - Share Your Time → /share-your-time/
  - East End Elementary School → /east-end-elementary-school/
  - Forest Acres Elementary School → /forest-acres-elementary-school/
  - Hagood Elementary School → /hagood-elementary-school/
  - Liberty Elementary School → /liberty-elementary-school/
  - Liberty Primary School → /liberty-primary-school/
  - McKissick Academy of Science and Technology → /mckissick-academy-of-science-and-technology/
  - Dacusville Elementary School → /dacusville-elementary-school/
  - Pickens Elementary School → /pickens-elementary-school/
  - Crosswell Elementary School → /crosswell-elementary-school/
  - Six Mile Elementary School → /six-mile-elementary-school/
  - West End Elementary School → /west-end-elementary-school/
  - Clemson Elementary School → /clemson-elementary-school/
  - Central Academy for the Arts → /central-academy-for-the-arts/
  - Ambler Elementary School → /ambler-elementary-school/
  - Pickens Middle School → /pickens-middle-school/
  - Liberty Middle School → /liberty-middle-school/
  - Gettys Middle School → /gettys-middle-school/
  ... and 22 more (see content/pages/_index.json)

### Custom Content Types
  - elementskit-template: 2 items

---

## Content Map

_All page copy is in the repo. Read the referenced file for each page — strip HTML/shortcodes, preserve the text._

| Page | Source File | Key Copy Note |
|------|-------------|---------------|
| **Home** | `extraction/content/pages/home-sections.json` (section-structured) | 1 sections: content |
| **About** | `extraction/content/pages/about-sections.json` (section-structured) | 1 sections: content |
| **Adult Learning Center** | `extraction/content/pages/adult-learning-center-sections.json` (section-structured) | 1 sections: content |
| **Ambler Elementary School** | `extraction/content/pages/ambler-elementary-school-sections.json` (section-structured) | 1 sections: content |
| **Cart** | `extraction/content/pages/cart.json` → `content_html` (strip HTML) | [woocommerce_cart] |
| **Central Academy for the Arts** | `extraction/content/pages/central-academy-for-the-arts-sections.json` (section-structured) | 1 sections: content |
| **Checkout** | `extraction/content/pages/checkout.json` → `content_html` (strip HTML) | [woocommerce_checkout] |
| **Clemson Elementary School** | `extraction/content/pages/clemson-elementary-school-sections.json` (section-structured) | 1 sections: content |
| **Crosswell Elementary School** | `extraction/content/pages/crosswell-elementary-school-sections.json` (section-structured) | 1 sections: content |
| **Dacusville Elementary School** | `extraction/content/pages/dacusville-elementary-school-sections.json` (section-structured) | 1 sections: content |
| **Dacusville Middle School** | `extraction/content/pages/dacusville-middle-school-sections.json` (section-structured) | 1 sections: content |
| **Daniel High** | `extraction/content/pages/daniel-high-sections.json` (section-structured) | 1 sections: content |
| **Donation Confirmation** | `extraction/content/pages/donation-confirmation.json` → `content_html` (strip HTML) | [give_receipt] |
| **Donation Failed** | `extraction/content/pages/donation-failed-sections.json` (section-structured) | 1 sections: content |
| **Donor Dashboard** | `extraction/content/pages/donor-dashboard.json` → `content_html` (strip HTML) | [give_donor_dashboard] |
| **Easley High School** | `extraction/content/pages/easley-high-school-sections.json` (section-structured) | 1 sections: content |
| **East End Elementary School** | `extraction/content/pages/east-end-elementary-school-sections.json` (section-structured) | 1 sections: content |
| **Edwards Middle School** | `extraction/content/pages/edwards-middle-school-sections.json` (section-structured) | 1 sections: content |
| **Forest Acres Elementary School** | `extraction/content/pages/forest-acres-elementary-school-sections.json` (section-structured) | 1 sections: content |
| **Gettys Middle School** | `extraction/content/pages/gettys-middle-school-sections.json` (section-structured) | 1 sections: content |
| **Hagood Elementary School** | `extraction/content/pages/hagood-elementary-school-sections.json` (section-structured) | 1 sections: content |
| **Impact Stories** | `extraction/content/pages/impact-story-sections.json` (section-structured) | 1 sections: content |
| **Liberty Elementary School** | `extraction/content/pages/liberty-elementary-school-sections.json` (section-structured) | 1 sections: content |
| **Liberty High** | `extraction/content/pages/liberty-high-sections.json` (section-structured) | 1 sections: content |
| **Liberty Middle School** | `extraction/content/pages/liberty-middle-school-sections.json` (section-structured) | 1 sections: content |
| **Liberty Primary School** | `extraction/content/pages/liberty-primary-school-sections.json` (section-structured) | 1 sections: content |
| **McKissick Academy of Science and Technology** | `extraction/content/pages/mckissick-academy-of-science-and-technology-sections.json` (section-structured) | 1 sections: content |
| **My account** | `extraction/content/pages/my-account.json` → `content_html` (strip HTML) | [woocommerce_my_account] |
| **Our Initiatives** | `extraction/content/pages/our-initiatives-sections.json` (section-structured) | 1 sections: content |
| **Pickens County Career and Technology Center** | `extraction/content/pages/pickens-county-career-and-technology-center-sections.json` (section-structured) | 1 sections: content |
| **Pickens County Virtual Academy + 360 Academy** | `extraction/content/pages/pickens-county-virtual-academy-360-academy-sections.json` (section-structured) | 1 sections: content |
| **Pickens Elementary School** | `extraction/content/pages/pickens-elementary-school-sections.json` (section-structured) | 1 sections: content |
| **Pickens High School** | `extraction/content/pages/pickens-high-school-sections.json` (section-structured) | 1 sections: content |
| **Pickens Middle School** | `extraction/content/pages/pickens-middle-school-sections.json` (section-structured) | 1 sections: content |
| **Project Go Alternative School** | `extraction/content/pages/project-go-alternative-school-sections.json` (section-structured) | 1 sections: content |
| **Sample Page** | `extraction/content/pages/sample-page-sections.json` (section-structured) | 1 sections: content |
| **Share Your Talent** | `extraction/content/pages/share-your-talent-sections.json` (section-structured) | 1 sections: content |
| **Share Your Time** | `extraction/content/pages/share-your-time-sections.json` (section-structured) | 1 sections: content |
| **Share Your Treasure** | `extraction/content/pages/share-your-treasure-sections.json` (section-structured) | 1 sections: content |
| **Shop** | `extraction/content/pages/shop.json` → `content_html` (strip HTML) | *(page builder content — see screenshots)* |
| **Six Mile Elementary School** | `extraction/content/pages/six-mile-elementary-school-sections.json` (section-structured) | 1 sections: content |
| **West End Elementary School** | `extraction/content/pages/west-end-elementary-school-sections.json` (section-structured) | 1 sections: content |

**Content rules:**
- Strip all HTML tags and shortcode markup (`[fusion_*]`, `[vc_*]`, etc.)
- Preserve the exact text — do not paraphrase or rewrite
- Images referenced in content are in `downloads/images/` — see `structure/image-map.json`

**`*-sections.json` file schema** (used by all section-structured pages):
```json
{ "page": "slug", "section_count": 6, "sections": [
  {
    "type": "hero | content | cta | gallery | faq | form | map",
    "headline": "H1 or H2 text",
    "subheadline": "supporting text or null",
    "body": "paragraph copy or null",
    "list_items": ["bullet 1", "bullet 2"],
    "ctas": [{ "label": "Button Text", "url": "/link/" }],
    "bg_image": "filename.jpg or null",
    "bg_image_url": "https://... or null",
    "bg_color": "#hex or null"
  }
]}
```
Use `structure/image-assignments.json` to map images to their section and page role.

---

## Technical Stack

| Layer | Decision |
|-------|----------|
| CMS | Migrate all content into the new codebase as flat files. No CMS backend. |
| Hosting | Vercel. |

**Framework:** Next.js (App Router) or Astro — static-first
**Styling:** Tailwind CSS

### Forms & CRM
*(no forms detected — confirm with client)*

**Who updates post-launch:** Take Part team. Developer access.

---

## Architecture

### Stack

| Layer | Technology |
|-------|-----------|
| Framework | Next.js (App Router) or equivalent — use latest stable |
| Styling | Tailwind CSS |
| Database | Supabase (Postgres) |
| Auth | Supabase Auth *(if needed — see below)* |
| Storage | Vercel `/public/images/` — `next/image` for all images |
| Hosting | Vercel |
| Forms | Next.js API route → Supabase `leads` table |

### Content Strategy — Static vs. Dynamic

**Static (hardcoded or MDX — no DB needed):**
- Core marketing pages: Home, Our Story, Explore the Area, FAQ, Contact

**Dynamic (Supabase tables):**

| Table | Purpose | Update Frequency |
|-------|---------|-----------------|
| `dashboards` | Dynamic content detected from /donor-dashboard/ page | medium |
| `shops` | Dynamic content detected from /shop/ page | medium |

### Auth

**Supabase Auth required.**
Reason: Page /my account/ suggests member/login functionality
- Public visitors: anonymous (read-only Supabase queries)
- Admin/editor: email+password via Supabase Auth
- Protect `/admin/*` routes with Next.js middleware

### Media & Images

**Strategy:** All images are static marketing assets — commit to `/public/images/` and use `next/image` with local paths

**Always use `next/image`** — never raw `<img>` tags.
- Enables automatic optimization, lazy loading, and WebP conversion
- Set `sizes` prop on full-width hero images
- Local static images: `import heroImg from '@/public/images/hero.jpg'`

### Next.js App Router — Server vs. Client Components

Follow this pattern strictly — wrong choices kill SEO or break interactivity:

| Component type | Directive | Examples |
|---------------|-----------|----------|
| Page layouts, static content, data fetching | *(none — Server by default)* | `page.tsx`, nav, footer, hero |
| Interactive UI | `'use client'` | Forms, accordions, modals, carousels |
| Supabase queries | Server Component (via `createServerClient`) | Listings page, FAQ page |
| Auth state, user context | `'use client'` | Header user menu, protected routes |

**Rule of thumb:** Start Server. Add `'use client'` only when you need `useState`, `useEffect`, or browser events.

### Environment Variables (`.env.local`)

```
NEXT_PUBLIC_SUPABASE_URL=https://your-project.supabase.co
NEXT_PUBLIC_SUPABASE_ANON_KEY=your-anon-key
SUPABASE_SERVICE_ROLE_KEY=your-service-role-key  # server-side only
```
Add all three to Vercel project settings under Environment Variables.


---

## Brand Tokens — Tailwind Config

Brand color and font values — apply using whatever config format
the installed version of Tailwind requires:

```js
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: [
    './app/**/*.{js,ts,jsx,tsx,mdx}',
    './components/**/*.{js,ts,jsx,tsx,mdx}',
  ],
  theme: {
    extend: {
      colors: {
        'neutral_1': '#85b559',
        'neutral_2': '#001e53',
        'neutral_3': '#334155',
        'neutral_4': '#666666',
        'white': '#ffffff',
        'black': '#000000',
        'neutral_7': '#cccccc',
      },
      fontFamily: {
        'heading': ['Gilroy Semibold', 'sans-serif'],
        'sans': ['Gilroy Regular', 'sans-serif'],
      },
    },
  },
  plugins: [],
}

```

---

## Header Scripts to Migrate

Copy the following into the new site's `<head>` exactly as-is. Do not omit any of these — missing a pixel breaks client analytics.

**External tracking scripts:**
- `https://www.googletagmanager.com/gtag/js?id=GT-K828KR5B`

**Inline tracking (GTM / GA4 / Pixel):**
- window.dataLayer = window.dataLayer || [];function gtag(){dataLayer.push(argumen

**Full head block for reference:** `structure/head-code.html`

---

## Integrations to Preserve

  - Google Analytics / GTM
  - GoHighLevel — preserve/configure the existing lead and contact flows.
  - Givebutter — preserve/configure donation CTAs and donation flow.
  - Newsletter signup — an existing newsletter system is present, but its platform is unidentified; inspect the live form/embed and preserve the current signup behavior once identified.

---

## Assets

⚠️ **Bulk media lives in Google Drive, not this repo.** Download the Drive asset folder linked in `DRIVE_ASSETS.md` into the rebuilt project under `public/assets/` before writing runtime image, font, document, video, or audio references.
**Brand fonts** should load from local files in `public/assets/fonts/` or committed `downloads/fonts/`, never from live-site/CDN URLs.
**Commercial fonts** (e.g. Interstate) require a separate license — see Font Loading section.

All original image source URLs are also in `extraction/structure/image-map.json` as evidence and retrieval hints only.

**Key images and original source URLs for identification only:**
| Filename | Usage | Source URL |
|----------|-------|------------|
| `copy-of-dsc02630-1.png` | home hero/bg | `https://scupstatefoundation.org/wp-content/uploads/2025/10/Copy-of-DSC02630-1.png` |

| Path | Contents |
|------|----------|
| `DRIVE_ASSETS.md` | Verified Google Drive asset folder and builder asset rules |
| `media-drive-manifest.json` | Asset-only Drive upload inventory |
| `extraction/downloads/images/` | 413 images in the Drive asset folder; copy to `public/assets/` before use |
| `extraction/downloads/fonts/` | Font files in Drive and/or committed repo files; load locally |
| `extraction/downloads/logos/` | Logo variations — see usage guide below |
| `extraction/screenshots/` | 21 full-page screenshots (desktop/tablet/mobile) |
| `extraction/design/design-tokens.json` | Colors, fonts, spacing (JS-rendered) |
| `extraction/design/image-analysis.json` | Image descriptions, categories, section assignments |
| `extraction/content/pages/` | 42 page content files — `*.json` raw, `*-clean.txt` plain text, `*-sections.json` section-structured |
| `extraction/structure/navigation.json` | 4-item primary nav |
| `extraction/structure/image-map.json` | Original source URLs for evidence only; do not use these as runtime `src` paths |
| `extraction/structure/image-assignments.json` | Image → page + section mapping (use this to place images in rebuild) |

**Runtime asset rule:** all runtime `src`, `href`, CSS `url()`, and `@font-face src` references must point to local project assets such as `public/assets/<filename>`. Do not reference Google Drive URLs, live `9panel.net` URLs, WordPress CDN URLs, or extracted CDN URLs directly in code.
| `extraction/content/custom/elementskit-template/` | 2 items |


**Logo usage:**
- `extraction/downloads/logos/adult_learning_center_logo.png` → general use — check against nav background color
- `extraction/downloads/logos/central_academy_of_the_arts_logo.png` → general use — check against nav background color
- `extraction/downloads/logos/crosswell_elementary_school_logo.png` → general use — check against nav background color
- `extraction/downloads/logos/ctc-png-logo-1.png` → general use — check against nav background color
- `extraction/downloads/logos/dacusville-el-logo.png` → general use — check against nav background color
- `extraction/downloads/logos/dacusville_middle_school_logo.png` → general use — check against nav background color
- `extraction/downloads/logos/daniel-high-school-logo.png` → general use — check against nav background color
- `extraction/downloads/logos/easley_hs_logo.png` → general use — check against nav background color
- `extraction/downloads/logos/east_end_elementary_school_logo.png` → general use — check against nav background color
- `extraction/downloads/logos/forest_acres_elementary_school_logo.png` → general use — check against nav background color
- `extraction/downloads/logos/hagood_elementary_logo.png` → general use — check against nav background color
- `extraction/downloads/logos/horizontal-logo_full-color.png` → nav on white/light background
- `extraction/downloads/logos/horizontal-logo_full-color_web-use-white.png` → nav on dark background, footer, dark overlays
- `extraction/downloads/logos/layer-51-2.png` → general use — check against nav background color
- `extraction/downloads/logos/liberty-middle-logo.png` → general use — check against nav background color
- `extraction/downloads/logos/liberty_elementary_school_logo.png` → general use — check against nav background color
- `extraction/downloads/logos/liberty_high_school_logo.png` → general use — check against nav background color
- `extraction/downloads/logos/liberty_primary_school_logo.png` → general use — check against nav background color
- `extraction/downloads/logos/mckissick-logo.png` → general use — check against nav background color
- `extraction/downloads/logos/new-gms-logo.png` → general use — check against nav background color
- `extraction/downloads/logos/pickens_county_virtual_academy_logo.png` → general use — check against nav background color
- `extraction/downloads/logos/pickens_elementary_logo-scaled.png` → general use — check against nav background color
- `extraction/downloads/logos/pickens_high_school_logo.png` → general use — check against nav background color
- `extraction/downloads/logos/pickens_middle_school_logo.png` → general use — check against nav background color
- `extraction/downloads/logos/project_go_alternative_program_logo.png` → general use — check against nav background color
- `extraction/downloads/logos/r.c._edwards_middle_school_logo.png` → general use — check against nav background color
- `extraction/downloads/logos/six_mile_elementary_school_logo.png` → general use — check against nav background color
- `extraction/downloads/logos/west-end-logo.png` → general use — check against nav background color

---

## 📸 Reference Screenshots — Match These

_These are the ground truth for this exact rebuild. Each page you build should match its screenshot._

- **Home** → `screenshots/page--home--desktop.png`
- **Home Tablet** → `screenshots/page--home--tablet.png`
- **About** → `screenshots/page--about--desktop.png`
- **About Tablet** → `screenshots/page--about--tablet.png`
- **Impact Story** → `screenshots/page--impact-story--desktop.png`
- **Impact Story Tablet** → `screenshots/page--impact-story--tablet.png`
- **Our Initiatives** → `screenshots/page--our-initiatives--desktop.png`
- **Our Initiatives Tablet** → `screenshots/page--our-initiatives--tablet.png`
- **Scupstatefoundation.org** → `screenshots/page--scupstatefoundation.org--desktop.png`
- **Scupstatefoundation.org Tablet** → `screenshots/page--scupstatefoundation.org--tablet.png`
- **Post Childcare For Teachers** → `screenshots/post--childcare-for-teachers--desktop.png`
- **Post Childcare For Teachers Tablet** → `screenshots/post--childcare-for-teachers--tablet.png`

---

## Build Notes

**Out-of-nav pages:**
rebuild all

**Contact details (display in header/footer):**
Phone: 864-397-3500; Email: connect@scUpstateFoundation.org


---

## Definition of Done

- [ ] All core pages live and styled — screenshots confirmed to match
- [ ] Mobile responsive — 375px, 768px, 1280px
- [ ] Primary CTA in hero, nav, and bottom of every core page
- [ ] Forms connected to CRM
- [ ] Custom fonts loading correctly
- [ ] Integrations installed (see list above)
- [ ] Images lazy-loaded, no layout shift
- [ ] Lighthouse ≥ 85 mobile

