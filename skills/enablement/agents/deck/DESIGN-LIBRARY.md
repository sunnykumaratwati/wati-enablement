# Wati Deck Design Library

The **only** design source for Wati decks. To place a slide, you MATCH its content to a layout here, then **clone the exact source slide** (deck + slide #) and fill it — a literal replica, same shapes/fonts/colours. Do not invent layouts and do not use any deck not listed here.

## Method (per slide)
1. Write the storyline (differs per deck type).
2. Write the slide's content.
3. **Match** the content to a layout below (by shape of the content: 3 benefits → 3-point-icons; a metric → big-stat; a customer → quote/case-study; A vs B → comparison; a feature + screenshot → text+mockup…).
4. **Clone** the primary source slide for that layout and fill its placeholders. Fit copy to the placeholder (shorten to fit); fill every icon/card slot.
5. Render + QA each slide.

## Source decks (Example Data/)
1. `Wati Deck - Sales Template 2026.pptx` — the clean template library (Lorem placeholders; best for generic layouts)
2. `WhatsApp Business Calling.pptx`
3. `Wati for Marketing_ Deck Draft_ Final.pptx`
4. `Wati_ CTWA_ Agency Deck.pptx`
5. `Wati_Instagram_Webinar_Deck.pptx`
6. `AI Support Agent Adoption Deck.pptx`
7. `AI Support Agent Value Proposition & Use Cases .pptx`

All are 10 × 5.625 in, DM Sans, brand palette, burst on content headings, Wati logo bottom-right (or top per template).

---

## Standard intro/end slides (SAME across all deck types — don't re-match these)
| Slide | Primary clone | Alt |
|-------|---------------|-----|
| **Cover** | Sales Template S1 | WhatsApp Calling S1 |
| **Agenda / index** | Instagram Webinar S2 (2×3 numbered cards) | Sales Template S2 |
| **Section divider** | Sales Template S3–S6 (solid brand-tint + title chip) | WhatsApp Calling S6/14/18 (teal panel + rounded chip) |
| **Demo** | Sales Template S51 (QR + keyword) | any deck's full-bleed demo slide |
| **Next steps / CTA** | WhatsApp Calling S17 (Configure→Engage + button) | Instagram S23 (two CTA buttons) |
| **Resources** | AI Adoption S25 (linked list + button) | AI ValueProp S20 |
| **Q&A** | WhatsApp Calling S19 | Sales Template |
| **Thank you** | Sales Template S62 | AI ValueProp S24 |

---

## Middle-content layout catalog (match content → clone source)
| Layout | Fits (content shape) | Primary clone | Alternates | Fill notes |
|--------|----------------------|---------------|------------|-----------|
| **big-stat** | 3–4 headline metrics / proof numbers | Instagram S3 (eyebrow + 4 stat blocks + sources) | WhatsApp Calling S4 (3 tinted pill stats); Marketing S15 | Real stats only; big number + small label |
| **3-col-highlight** | 3 proof points or 3 use-cases/personas | WhatsApp Calling S2 (3 big % stats + intro) | Instagram S7 (3 vertical use-case cards); Sales Template S35–38 | Fill all 3 cols + icons |
| **3-point-icons** | 3 benefits/points, icon each | AI ValueProp S4 | CTWA S13; Instagram S6; Sales Template S42/S52 | icon + head + one line each |
| **4-icon-grid** | 4 capabilities/benefits/items | Marketing S14 (4 tiles + 2 big stats) | CTWA S5/S22; WhatsApp Calling S12; Instagram S20 (2×3); Sales Template S11 | fill every tile + icon; no empty cells |
| **text+mockup (feature detail)** ⭐ workhorse | one feature: value + product screenshot | WhatsApp Calling S7–S11 | Marketing S7–S10; AI Adoption S13–16; Sales Template | title + 3 bullets/value left, screenshot right; add soft glow behind mockup |
| **text+visual-grid** | feature with several sub-elements/use-cases | AI ValueProp S7 (diagonal accent + chat visual) | AI Adoption S10/18; Marketing S27/S32 | left copy, right visual grid |
| **two-column-comparison** | A vs B / with-vs-without / mode-vs-mode | WhatsApp Calling S5 (UIC vs BIC cards) | Marketing S39 (vs BSP/cPaaS); Instagram S21 (✗/✓) | two labeled cards, mirrored rows |
| **comparison-table** | feature/price matrix, 3+ columns | AI ValueProp S10 (teal header matrix) | Instagram S5 (What You Get/Miss); CTWA S26; Sales Template S56 | teal header row; ✓/✗ favouring Wati |
| **quote/case-study** ⭐ | one customer: result metrics + quote | Marketing S43–S45 (industry-tagged) | WhatsApp Calling S15/16; CTWA S17–19; AI ValueProp S22 (dark) | name + role + logo + metrics + pull quote; real only |
| **process/flow-diagram** | a sequence / before→after / tracking flow | Marketing S6 (numbered 1-2-3-4 band) | Instagram S13 (4 nodes + connectors); CTWA S34 (2-lane); Marketing S31 (CAPI) | numbered nodes + connectors |
| **bullets+image** | value bullets + a supporting photo/screenshot | AI Adoption S4 (checkmark bullets + screenshot) | AI ValueProp S2 (pain framing); WhatsApp Calling S13 | checkmark bullets left, image right |

⭐ = most-used. If two layouts fit, prefer the one whose source deck matches the asset's tone (webinar → Instagram/Calling; marketing → Marketing; support/AI → AI decks).

---

## Rules
- **Exact replica:** clone the source slide's shapes; only swap text/fill placeholders. Never rebuild a layout from scratch.
- **Only these 7 decks.** No external design references.
- **Storyline differs per deck type; design base is shared.** (onboarding-deck slide · product-deck · enablement-deck all draw from this library.)
- Fit copy to the placeholder; fill every slot; render + QA before done (see `DECK-PRINCIPLES.md`).
