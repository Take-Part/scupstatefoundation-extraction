# Design System Summary

_Synthesized by DesignAnalyzer — captures visual identity and design intent beyond raw token values. Use this alongside design-tokens.json and screenshots._

## Typography System

**Font pairing:** Display/headline text uses **Oswald** paired with **-apple-system** for body copy and UI text. This combination creates visual hierarchy — the display face carries the brand personality while the body font keeps content readable and clean.

**CTAs and buttons** use **Nunito**, adding a third typographic voice that makes calls to action visually distinct from both headings and body text.

**Heading scale:** H1: 60px, H2: 55px, H3: 23px.

**Heading style:** text-transform: uppercase — note these in Tailwind config.

## Color System

**Brand color palette:**
- `#fff` (mid-tone)
- `#85b559` (mid-tone)
- `#000` (mid-tone)
- `#87b55e` (mid-tone)
- `#999` (mid-tone)
- `#666` (mid-tone)

## Recurring Visual Motifs

**Photo backgrounds** — 1 sections use full-bleed photography as backgrounds. Typically overlaid with a semi-transparent color layer for text legibility.

## Page Structure Pattern

**Dark-dominant layout** — Most sections (1 of 1) use dark backgrounds. This is a brand aesthetic choice, not an accessibility issue.

## Color Usage in Context

| Background | Text Color | Role |
|-----------|-----------|------|
| `#001740` | `#334155` | body |

## Implementation Notes for Emergent

- Load **Oswald** as the display/heading font. Verify it's self-hosted or confirmed Google Fonts — check downloads/ in emergent-package.
- Load **-apple-system** for body copy and UI elements.
- Apply heading style utilities: `uppercase` to heading classes globally.
