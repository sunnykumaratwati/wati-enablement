# Wati Deck Maker

Turns a launch into a **detailed, self-contained build prompt** that Claude Design runs to produce an on-brand Wati deck. The skill's job is the **prompt** (research + storyline + inlined context + design spec) — not building the .pptx itself.

## The 4 deck types (each its own agent, one shared design system)
| Agent | Deck | Audience |
|-------|------|----------|
| `onboarding-deck/` | 1–2 feature slides for the marketing/onboarding master deck | Customers/Sales |
| `product-deck/` | full customer- & sales-facing product deck | Customers/Sales |
| `enablement-webinar/` | internal launch-enablement session | Sales/CS/Support |
| `quarterly-webinar/` | quarterly product-updates webinar (Wati Launch Day) | Customers |

## The shared brain (read in this order)
1. **`DECK-PRINCIPLES.md`** — the rules every agent inherits: the **RESEARCH CHAIN** (PRD pain-points first → always WebSearch `support.wati.io` → Notion → KB → web), **DEPTH & calibration** (smart FAQs, separate distinct concepts, use-cases/personas/messaging, prep-for-launch + holistic close), **STORY-FIRST gate**, one design system, clone-not-scratch, fill-every-slot, ≤90 MB cap, render + 100% gate.
2. **`STORYLINE-BLUEPRINTS.md`** — the per-type storyline + what each includes/omits (their real differences).
3. **`DESIGN-LIBRARY.md`** — the ONE Wati design system (10×5.625, DM Sans/Outfit, palette, burst, footer) + the layout catalog (content-shape → clone source slide across the approved decks).
4. **`PROMPT-TEMPLATE.md`** — the exact shape of the deliverable, incl. the mandatory **inlined CONTEXT PACK** (builder can't read our files/Notion) and the ≤90 MB cap.

## The flow (every deck)
PRD pain-points → research (support docs / Notion / KB / web) → **story (gated)** → per-beat content → match each beat to a design-library layout + clone source → **inline everything into a ~3-page prompt** → hand to Claude Design → it clones layouts, fills, renders, passes the 100% gate (≤90 MB).

## Non-negotiables
- Each feature keeps its **own distinct pain** — never invent one unifying problem.
- Positioning/naming/banned-words per `context/*.md` + `context/positioning.md`, inlined.
- Real data only; screenshots = clean placeholders; design cloned from the approved Wati decks only.
