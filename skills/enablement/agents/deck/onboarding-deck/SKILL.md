---
name: onboarding-deck-slide
description: Creates 1 (sometimes 2–3) feature slide(s) to insert into Wati's marketing/onboarding deck when a feature launches. Use when someone says "add a slide to the onboarding deck", "create an onboarding slide for [feature]", "we launched [feature], make the deck slide", or "feature slide for the onboarding deck".
---

# Onboarding-Deck Feature Slide

**DELIVERABLE = a detailed ~3-page BUILD PROMPT only** — follow `skills/enablement/agents/deck/PROMPT-TEMPLATE.md` using this deck type's storyline in `skills/enablement/agents/deck/STORYLINE-BLUEPRINTS.md`, with a fully **inlined CONTEXT PACK** (positioning, value props, feature descriptions, naming/banned words, plan eligibility, edge-cases — embed the text; the builder can't read our files/Notion). Be very detailed on storyline + content. **Do NOT build the .pptx — output the prompt.** **(Everything else in this agent — structures, build/render/QA steps — describes what your PROMPT must instruct the downstream builder to do; you output the prompt, not the deck.)**


**Customer-facing:** lead with value & positioning (external messaging), NOT how the product was built. Omit internal mechanics (engines, confidence scores, build details) unless they're a customer benefit.


You produce a single feature slide (occasionally 2–3 for a flagship feature) to be inserted into Wati's **Wati for Marketing Onboarding Deck**. The slide equips the sales team: what the feature is, its benefits, and **what to pitch it against**. You hand back just the slide(s); Sunny pastes them into the master deck.

> **This is its own deck type — don't overlap.** Onboarding-deck feature slides ≠ quarterly webinar ≠ product-launch webinar ≠ enablement session. Different storyline and purpose (a sales-pitch aid, not a narrative deck). See the router's type note.

**First read the shared `skills/enablement/agents/deck/DECK-PRINCIPLES.md`** — universal rules for every deck (template not scratch, value-first, render-verify, glow-behind-mockups, fill grids).

**Design: match each content slide to a layout in `skills/enablement/agents/deck/DESIGN-LIBRARY.md` and clone the exact source slide (1:1 replica). Storyline is this agent's own; design base is shared across onboarding-deck / product-deck / enablement-webinar. Only the 7 approved decks.**

Wati brand context: !`cat .agents/wati-brand.md 2>/dev/null || echo "No brand context file found."`

## Method (template — never from scratch)
1. **Identify the feature** Sunny names.
2. **Gather context** from the local knowledge base: read the matching `context/*.md` (what it does, value prop, plan, proof, positioning/naming rules). The weekly refresh keeps this current — the launch will be in a "Recently Shipped" section.
3. **Borrow extra context if useful**: WebSearch the feature's Wati **support article** (site:support.wati.io or wati.io) for accurate mechanics/wording. Never fabricate — mark `[TBC]`.
4. **Judge the feature's size/importance** and pick a template from `references/feature-slide-templates.md`:
   - small/simple → 1 slide (T1 or T5); medium → 1 slide (T2/T5); flagship → propose 2–3 (T0 header + detail + T6 proof); "vs" story → T4; process → T3.
   - **Do the feature justice** — a big, high-MRR feature shouldn't get a thin slide. Tell Sunny if you recommend 2–3 slides and confirm.
5. **Clone the matching real slide** from the reference deck and swap the content:
   - Reference decks: `~/Desktop/Wati for Marketing_ Onboarding Deck.pptx` (insertion target) and `~/Desktop/Example Data/Wati for Marketing_ Deck Draft_ Final.pptx` (more template examples).
   - Edit text in place by shape index (preserve DM Sans, burst, logo, layout). Remove/replace any leftover feature-specific graphics or screenshots (use a clean `[SCREENSHOT PLACEHOLDER]` — Sunny adds the real Figma export). Fix stray refs; fill grids evenly.
6. **Save just the slide(s)** as a small `.pptx` to `~/projects/<feature>/outputs/onboarding-slide-<feature>.pptx`.

## Content the slide must carry — VALUE FIRST
An onboarding slide **sells value, not mechanics**. Lead with the outcome; support with how.
- **A value tagline** — the outcome/positioning ("Your blank Monday, already planned. A revenue-ready week in minutes, not hours."), not a feature restatement.
- **Value bullets** — what it brings and how much (time saved, budget protected, more engagement, revenue moments captured) — pulled from `context/positioning.md` + the feature's `context/*.md`. Include the richer story (e.g. campaigns: AI generates 3 copy options, more engagement, pacing protects budget), not just one mechanic.
- Exact feature name + plan eligibility (naming per `context/positioning.md`).
- **What to pitch it against** (the pain / old way it beats).
- Specs table or proof if the template calls for it (T6/T7/T8/T10).
- As PMM, decide the depth the feature deserves and pick the template that does it justice.

## Design
Follow `context/design-system.md` exactly (Wati overall theme: DM Sans, brand palette, burst on heading, logo top-right, footer, no shadows, rounded tinted cards). The onboarding deck uses this same theme.

## Verify before handing back
Render the slide(s) (LibreOffice → PyMuPDF PNG) and eyeball: on-brand, no overflow, no empty grid cells, no leftover graphics, correct plan + naming. Show Sunny the render, then deliver the file.

## Mistakes to never repeat
Template (never from scratch) · render before "done" · fill grids evenly · use brand-auditor guidelines · don't mix deck types · install DM Sans (serif render = missing font).
