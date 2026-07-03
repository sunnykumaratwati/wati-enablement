---
name: enablement-webinar
description: Creates Wati's internal launch-enablement webinar deck — the hands-on session that trains internal teams (Sales / CS / Support) on what shipped, what's coming, how to win competitively, and where to find assets. Use when someone says "enablement deck", "internal enablement session deck", "PMM enablement session", "train the team on [launch/feature]". NOT the customer quarterly webinar (quarterly-webinar), the customer product deck (product-deck), or onboarding slides (onboarding-deck).
---

# Internal Enablement Session Deck

**DELIVERABLE = a detailed ~3-page BUILD PROMPT only** — follow `skills/enablement/agents/deck/PROMPT-TEMPLATE.md` using this deck type's storyline in `skills/enablement/agents/deck/STORYLINE-BLUEPRINTS.md`, with a fully **inlined CONTEXT PACK** (positioning, value props, feature descriptions, naming/banned words, plan eligibility, edge-cases — embed the text; the builder can't read our files/Notion). Be very detailed on storyline + content. **Do NOT build the .pptx — output the prompt.** **(Everything else in this agent — structures, build/render/QA steps — describes what your PROMPT must instruct the downstream builder to do; you output the prompt, not the deck.)**


**First read the shared `skills/enablement/agents/deck/DECK-PRINCIPLES.md`** — universal rules for every deck.

**Design: match each content slide to a layout in `skills/enablement/agents/deck/DESIGN-LIBRARY.md` and clone the exact source slide (1:1 replica). Storyline is this agent's own; design base is shared across onboarding-deck / product-deck / enablement-webinar. Only the approved Wati decks (see DESIGN-LIBRARY).**

This agent builds the **internal enablement deck**: a session that equips Sales/CS/Support on a launch. Internal audience, internal/playful tone — distinct from the customer quarterly webinar, the customer product deck, and onboarding slides. It is one of four deck types under `deck/`.

**Read the pattern before building:** `references/enablement-session-pattern.md` (the storyline + layout library, extracted from the real reference deck).

Wati brand context: !`cat .agents/wati-brand.md 2>/dev/null || echo "No brand context file found."`

## References (template from these — never from scratch)
**Storyline** (two shapes — pick from the ask; see pattern file):
- A — Periodic recap: `~/Downloads/Decks/Wati - PMM Enablement - Session 1.pptx` (1–9 session; 10–48 layout library)
- B — Single-launch deep-dive: `~/Desktop/Example Data/[Internal enablement] CTWA & Conversions.pptx`

**Design** is borrowed from the customer marketing/sales decks: `~/Desktop/Example Data/Wati for Marketing_ Deck Draft_ Final.pptx` and `~/Desktop/Example Data/Wati Deck - Sales Template 2026.pptx` — plus reference A's layout library. Clone the layout that fits each slide; swap content.

## Method

### 1. Gather content (data-sourcing fallback chain)
Pull the launch's content in this order, stopping when you have enough:
1. **Knowledge base** — the feature's `context/*.md` (what it does, value props, plan, proof, positioning; "Recently Shipped" for dates). Kept current by the weekly refresh.
2. **Launch folder** — `~/projects/<launch>/` (CONTEXT.md, briefs, positioning).
3. **Notion** — the feature's launch/positioning doc (Notion MCP) if the KB is thin.
4. **Support docs** — WebSearch the Wati support article (support.wati.io) for accurate mechanics.
5. **Launch Slack thread** — the launch/#product-updates-gtm discussion often holds the real edge-cases, FAQs, naming decisions, and VO/positioning lines (e.g. Drip: "always 'Drip Campaigns' not 'sequences'"; the undelivered-message + auto-retry FAQ; active-segment behaviour). Fold these into the enablement/FAQ slides.
6. **Battlecard / competitor-intel** — for the competitive deep-dive.
7. **Ask Sunny** — if after all this a needed piece is missing (e.g. no customer story, no FAQs), say so and ask, or mark `[TBC]`. Never fabricate.

### 2. Size the deck to the launch (analytical call)
**The deck length scales with the launch's significance — you decide as PMM.** A big/flagship feature earns more slides (recap + a real deep-dive + demo + customer story + objections); a small feature gets a tight few. Don't pad a minor launch to full length, and don't shortchange a major one. State your reasoning and the planned slide count before building.

### 3. Plan the storyline (LLM the fit)
**Pick the storyline shape from the ask** (pattern file): A = periodic recap; B = single-launch deep-dive. Then **reason about what actually fits THIS launch** and assemble from the section palette (educate/why · status-quo pain · before→now→benefits · walkthrough · demo · why-Wati · battlecard · customer story · packaging/pricing · getting-started/known-issues/adoption · attributes · "feedback we need" · "why it's complex" · assets · Q&A). Include a section only if you have the data for it — don't force empty quote/FAQ sections.

### 4. Match each slide to a layout-library template
For every slide you plan, **pick the matching template page from the reference deck's layout library (slides 10–48)** by content type — multi-column recap, quote/case-study layout, heading+body, section divider, contact/thank-you. Choose the layout whose shape fits the content and value props; clone it and swap the copy. Don't invent a layout when a library one fits.

### 5. Build by templating
Clone the chosen reference slides/layouts and swap text in place (preserves DM Sans, burst, logo, brand tints). Value/enablement-first copy. Fill grids evenly.

### 6. Render + QA
Render every slide (LibreOffice → PyMuPDF PNG), run `wati-brand-auditor`, fix issues, show Sunny the render, then save to `~/projects/<launch>/outputs/enablement-session-<launch>.pptx`.

## Content notes
- **Value/enablement first** — equip the rep: what it means for the customer, how to sell it, what to pitch it against. Not a feature dump.
- Internal tone: a playful themed cover is on-brand here (the reference used "Avengers"). Keep the body clear and useful.
- Footer `www.wati.io | hello@wati.io`.

## Mistakes to never repeat
Template (never from scratch) · render before "done" · fill grids evenly · use brand-auditor guidelines · don't mix deck types · install DM Sans (serif = missing font).
