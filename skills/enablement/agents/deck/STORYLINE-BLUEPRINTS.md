# Storyline Blueprints — the 3 deck types (excl. quarterly webinar)

The design system is shared (see `DESIGN-LIBRARY.md`); the **storyline differs by type**. Each deck agent's deliverable is a **detailed ~3-page build prompt** (per `PROMPT-TEMPLATE.md`) using its blueprint below + an inlined CONTEXT PACK. **The agent does NOT build the deck — it produces the prompt only.**

The three differ in **audience, depth, and what they include vs omit**:

| | Onboarding-deck slide | Product deck | Enablement deck |
|---|---|---|---|
| Audience | Customers/sales (inside master deck) | Customers & prospects, sales | Internal Sales/CS/Support |
| Length | 1 slide (2–3 for flagship) | ~10–14 slides | ~12–16 slides |
| Voice | Value + "what to pitch against" | Value + proof + CTA | Enable the rep: how to sell + answer |
| Includes | plan, 1 screenshot | use cases, why-Wati, proof, plans, CTA | + FAQs/edge-cases, nuances-to-flag, how-to-pitch, feedback-we-need |
| Omits | narrative | internal mechanics/FAQs | nothing internal — this is the deep one |

---

## 1. ONBOARDING-DECK SLIDE (customer-facing, 1 slide)
A single high-density value slide inserted into the master marketing/onboarding deck at a named position. Not a narrative — one slide that sells the feature.
**Beats (one slide):** eyebrow pill (plan + AI if applicable) · **bold value headline** (outcome, not feature) · **3–4 value bullets** (what it brings, how much) · **what to pitch it against** (the pain/old way it beats) · plan · a LARGE product screenshot placeholder. For a flagship: split into 2–3 slides (what it is / how it works / proof).
**Prompt must specify:** the exact insertion slide #, the value headline, the bullets, the screenshot, the plan, the layout to clone (T7 value+specs+mockup, or text+mockup).

## 2. PRODUCT DECK (customer-facing, full)
The complete external solution story — move a customer from problem-aware to "I want this." Value-first; **omit internal mechanics** (engines, scores).
**Beats:**
1. Cover
2. The problem / why now (the customer's pain, framed in their world)
3. The shift (what changed / the new way)
4. Introducing [product/feature set] (one-line definition + the 3 things it does)
5–N. Per feature: **value + how it helps + demo** (text-left + LARGE product mockup)
- Use cases (by industry/persona)
- Why Wati (differentiators, first-to-ship, trust: 16,000+ businesses · 100+ countries · Meta Partner)
- Proof / customer story (real only; omit if none)
- Plans & pricing
- Next steps / CTA
- Thank you
**Prompt must specify:** the pain, the shift, per-feature value+demo, use cases, why-Wati, plans, CTA — all as actual copy.

## 3. ENABLEMENT DECK (internal, Sales/CS/Support)
Equip the team to sell and support the launch. Internal, enabling tone. This is the **deepest** — it keeps everything the customer decks omit.
**Beats:**
1. Cover (Launch Enablement · Internal · audience)
2. What's launching (features + plan pills; note separations)
3. Why this matters — **the customer pain reps hear**
4–N. Per feature: **how it works** (mechanics reps must know) → **how to pitch it / who it's for** (persona angles) → **demo**
- **FAQs & edge cases** (the real ones — what CS/Sales get asked)
- **Key nuances to flag** (plan gating, phased rollout, approval caveats, "don't promise X yet")
- Plans & eligibility
- **Feedback we need** (what to gather from customers)
- Q&A / close
**Prompt must specify:** the pain, per-feature mechanics + persona pitch angles, the actual FAQs/edge-cases, the nuances, plans, feedback asks — as actual copy.

---

## Rules for all three prompts
- **Deliverable = the detailed ~3-page prompt**, self-contained (inline CONTEXT PACK — the builder can't read our files/Notion).
- Pull context from `context/<category>.md` + `context/positioning.md` + the launch project + PRD/Notion, and **embed the text**.
- Design system + build method + 100% gate = paste from `DECK-PRINCIPLES.md` / `DESIGN-LIBRARY.md`.
- Real data only; respect naming/banned words; screenshots = clean placeholders.
