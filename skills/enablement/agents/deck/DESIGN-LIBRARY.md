**Enablement decks: the canonical base is `BASE-DECK.md` (the recent 20×11.25 deck) — mirror it first.**

# Wati Deck Design System + Layout Library

All Wati decks are ONE design system (verified across 10 decks). Any slide I make must match this pattern. **I never design a slide — I clone the cleanest real instance of the layout I need and swap only the words.**

## THE PATTERN (invariants — enforce on every slide)
- **Canvas: 10 × 5.625 in** (16:9). Standard across 9/10 decks. (The AI Webinar deck is 16×9 — only clone from it if the target deck is also 16×9.)
- **Font: DM Sans *or* Outfit** — Wati uses both; near-identical geometric sans (both installed at `~/Library/Fonts`). **One font per deck.** Default **DM Sans** (brand guide). After cloning layouts from different source decks, **normalize every run to the deck's chosen font** so it's internally consistent.
- **Palette (only):** green `#00e785` · black text `#1d1d1d` · body grey `#505050` · footer grey `#828282` · white · tints `#cafde8` (green) `#e3f5ff` (blue) `#fdecff` (pink) `#fff6da` (yellow) · accents blue `#4fc3ff` / pink `#f9b4ff` / yellow `#ffe96e`.
- **Burst:** 3 fanned bars left of every content-slide heading.
- **Logo:** bottom-left or top-right per slide type. **Footer:** `www.wati.io  |  hello@wati.io` + page number.
- **Cards:** rounded corners, tinted fills, optional top accent strip, **no shadows**. Section dividers = solid brand-tint slide.
- Type scale + spacing per `wati-brand-auditor` brand guidelines (source of truth for invariants).

## The source decks (all share the pattern — clone the cleanest instance)
Sales Template 2026 (DM Sans, cleanest placeholders — best generic source) · Wati AI Webinar (DM Sans, 16×9) · Instagram Webinar (DM Sans) · WhatsApp Calling (DM Sans) · Marketing · CTWA Agency · Partner 2026 · Support Master · AI Adoption · AI ValueProp (these 6 = Outfit). All in `~/Desktop/Example Data/` (Partner in `~/Downloads/`).

## Layout index (content shape → clone the cleanest instance)
| Layout | Fits | Cleanest source(s) |
|--------|------|--------------------|
| Cover | title + tagline + date | Sales Template S1 · WA Calling S1 |
| Agenda / index | 3–5 agenda items | Sales Template S2 · Instagram S2 |
| Section divider | section title on tint | Sales Template S3–6 (4 colours) |
| Big-stat | 2–4 headline stats | WA Calling S2/S4 · Instagram S3 |
| 3/4-icon-grid | 3–4 capabilities (icon each) | Sales Template S11–14 · Marketing S14 · CTWA S5 |
| 3-col highlight | 3 points/use-cases | Sales Template S35–38 · Instagram S7 |
| 3-point + tag | 3 points w/ plan pill | Sales Template S42 · S52 |
| text+mockup (feature) ⭐ | one feature + screenshot | WA Calling S7–11 · Marketing S7–10 |
| comparison table | tiered / A-vs-B matrix | Sales Template S56 · AI ValueProp S10 |
| quote / case-study | customer + metrics + quote | Marketing S43–45 · WA Calling S15–16 |
| process / flow | a sequence / before→after | Marketing S6 · CTWA S34 |
| pillar engine (intro→demo→outcomes) | a feature told in 3 slides | Wati AI Webinar S10-11-12 (16×9 only) |
| next steps / CTA | closing actions | WA Calling S17 · Sales Template S58–61 |
| thank you | close + contact | Sales Template S62 |

## Clone-and-fit discipline (how a slide is made)
1. Duplicate the source slide (shapes/fills/fonts/graphics untouched).
2. Replace ONLY text, run-by-run (keep formatting).
3. **Fit copy to the placeholder** — shorten to its capacity; never overflow.
4. **Fill every placeholder** — no empty icon/box, no leftover Lorem/Icon/TYPE.
5. Add nothing, delete nothing in the design. **Screenshots = a clean labelled placeholder** (Sunny drops the export in).
6. **Normalize all text runs to the deck's one font.**

## 100% design gate (before Sunny sees it)
Render every slide (both fonts installed) → `wati-brand-auditor` + per-slide check vs the source layout → score font/palette/burst/logo/overflow/empty-slots/leftovers/alignment → fix until **every slide = 100%**. Ship only then.

## Process order
Story (gated, `DECK-PRINCIPLES.md` §0) → content → match layout → clone → fill → normalize font → gate.
