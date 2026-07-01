# Wati Deck Design System (Authoritative)

**Source of truth:** the `wati-brand-auditor` skill's `references/brand-guidelines.md`. That skill's guidelines win over any reverse-engineered values. Run `wati-brand-auditor` on every deck before it's final.

## Build method (non-negotiable)
**TEMPLATE from a real Wati deck — never build slides from scratch.** From-scratch loses the logo, the burst, embedded fonts, and layout fidelity. Start from a reference `.pptx`, duplicate its slide types, and swap the content.
- **Quarterly / Launch Day reference:** `~/Desktop/Decks/Webinar Decks/Quarterly Updates/Q1 Product Updates_ Wati X Astra.pptx` (or the latest quarterly deck)
- **Burst placement canonical reference:** `Wati for Marketing_ Onboarding Deck.pptx`
- Method: open the reference file, keep its masters/layouts/graphics, duplicate feature/divider/demo slides as needed, replace only the text. Delete leftover template slides at the end.

## Canvas
- **16:9 at 13.33" × 7.5"** (NOT 16×9 inches).

## Font
- **DM Sans** only (weights 300/400/500/600/700). Never Arial/Roboto/Inter/system. Install DM Sans if a machine lacks it — otherwise renders substitute serif.

## Colors (brand palette only — no off-palette)
| Role | Hex |
|------|-----|
| Green (primary accent/CTA) | `#00e785` |
| Blue (secondary) | `#4fc3ff` |
| Yellow (attention) | `#ffe96e` |
| Pink (decorative) | `#f9b4ff` |
| Light Green tint | `#cafde8` |
| Light Blue tint | `#e3f5ff` |
| Light Yellow tint | `#fff6da` |
| Light Pink tint | `#fdecff` |
| Black (text) | `#1d1d1d` |
| Body/description grey | `#505050` |
| Footer grey | `#828282` |
| White | `#ffffff` |
- Saturated colors = accents/CTAs/large stat values ONLY, never large backgrounds.
- **Never white text on bright brand colors** (fails contrast). Text on any tint/bright = `#1d1d1d`.
- **Accent rotates slide to slide** — never two consecutive slides with the same accent (Green → Blue → dark → Yellow → …).

## The Burst (core identity — on EVERY content-slide heading)
Three thin fanned bars immediately left of the heading. Each bar 0.069"W × 0.307"H:
- Left: x=0.820", rot −30.1° · Centre: x=1.018", rot 0° (0.061" higher) · Right: x=1.216", rot +30.1°
- All three same colour = the slide's accent (white on dark). Never mixed, never on cover/section-separator slides.

## Logo (on every slide)
- Cover: large (~1.9") top-left · Section separator: medium (~1.3") top-right · Content: small (~1.1") top-right · Thank You: large (~2.8") centred.
- `wati-logo-dark-bg` on dark, `wati-logo-white-bg` on light. **Logo assets live only inside real decks — another reason to template.**

## Slide types
- **Cover** — WHITE background; large logo top-left; two-line hero (black + green); thin vertical accent bar left of headline; subheading regular dark grey; event/date small light grey. (NOT dark background.)
- **Section separator** — tinted brand-colour background; giant 96pt bold section number in accent; 40pt bold black title; 16pt `#505050` descriptor; logo top-right. No burst.
- **Content** — white; logo top-right; burst + 28pt bold heading top-left (~y=0.82"); content below (~y=1.72"). Body `#505050`.
- **Thank You** — white; large centred logo; 58pt bold black headline; green italic 15pt tagline.

## Type scale (decks)
Section number 96pt bold accent · Cover hero number/year 72pt bold green · Cover headline 56pt bold · Slide heading (with burst) 28pt bold `#1d1d1d` · Section title 40pt bold · Card title 22pt bold · Stat number 38pt bold accent · Lead sentence 26pt bold · Card sub-label/tagline 13–15pt bold accent · Body 11–13pt regular `#505050` · Descriptor 16pt regular `#505050` · Footer 9–12pt `#828282`. Max 3 type sizes per slide. Biggest element = the key number/phrase.

## Cards & visual style
- Tinted card fills (never white-on-white), **rounded corners** (adj ≈12000–14000), **NO shadows**, **top accent strip** (~0.5" saturated) on cards. No thin dividers — use tinted panels/whitespace. Let content decide layout (2 ideas = 2 columns, one big idea = full slide).

## Footer
- `www.wati.io  |  hello@wati.io` bottom-left, 9pt, matched to bg. Page number bottom-right (except Thank You).
- Note: internal quarterly decks have used `pmm@wati.io`; brand standard for customer-facing is `hello@wati.io`. Confirm with PMM per deck.

## Feature-slide content format (Launch Day)
Keep the quarterly `THE PROBLEM / THE UPDATE / WHAT'S IN IT FOR YOU` + Plan structure, but rendered inside the real templated slide (burst, logo, tinted panels, accent rotation) — not a from-scratch layout.
