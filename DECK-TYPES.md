# Wati Deck Types

Inside **enablement → deck** there are **4 deck types**, each its own individually-trained agent under `skills/enablement/agents/deck/`. **They don't overlap** — different storyline, audience, and design. All four inherit `skills/enablement/agents/deck/DECK-PRINCIPLES.md`.

| # | Type | Agent | Purpose & audience | Status |
|---|------|-------|--------------------|--------|
| 1 | **Onboarding-deck slide** | `onboarding-deck` | 1–2 feature slides inserted into the Wati for Marketing onboarding deck. Sales aid: value props, positioning, what to pitch it against. Value-led; match the deck's feature-slide templates (T0–T11). | ✅ Trained |
| 2 | **Product deck** | `product-deck` | The complete customer- & sales-facing product deck — full solution story (problem → shift → product → proof → pricing/CTA). | ◻ Partially (has structure; template + train on a reference product deck) |
| 3 | **Enablement webinar** | `enablement-webinar` | Internal launch-enablement session — equips Sales/CS/Support: what shipped, what's coming, competitive battlecard, customer story, where assets live. Internal/playful tone. | ✅ Trained (ref: `~/Downloads/Decks/Wati - PMM Enablement - Session 1.pptx`) |
| 4 | **Quarterly webinar** | `quarterly-webinar` | External customers — the quarterly product-updates webinar (Wati Launch Day). Themes → per-feature PROBLEM/UPDATE/WIIFY → demos → roadmap. | ✅ Trained |

## Rules (see DECK-PRINCIPLES.md for the full set)
- Template from the matching reference deck — never from scratch.
- Content is **value-first** (outcome/positioning, then mechanics); pull from `context/*.md` (+ Granola / launch projects / a WebSearched support article); never fabricate.
- Match design exactly (`context/design-system.md`; source of truth = `wati-brand-auditor`): DM Sans, palette, burst, logo, soft glow behind mockups, fill grids evenly.
- Render + QA every slide before handing back.
- Each type is trained individually for its own outcome — never overlap.
