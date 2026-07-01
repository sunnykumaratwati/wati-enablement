---
name: enablement-webinar
description: Creates Wati's internal launch-enablement webinar deck — the hands-on session that trains internal teams (Sales / CS / Support) on what shipped, what's coming, how to win competitively, and where to find assets. Use when someone says "enablement deck", "internal enablement session deck", "PMM enablement session", "train the team on [launch/feature]". NOT the customer quarterly webinar (quarterly-webinar), the customer product deck (product-deck), or onboarding slides (onboarding-deck).
---

# Internal Enablement Session Deck

**First read the shared `skills/enablement/agents/deck/DECK-PRINCIPLES.md`** — universal rules for every deck.

This agent builds the **internal enablement deck**: a session that equips Sales/CS/Support on a launch. Internal audience, internal/playful tone — distinct from the customer quarterly webinar, the customer product deck, and onboarding slides. It is one of four deck types under `deck/`.

**Read the pattern before building:** `references/enablement-session-pattern.md` (the storyline + layout library, extracted from the real reference deck).

Wati brand context: !`cat .agents/wati-brand.md 2>/dev/null || echo "No brand context file found."`

## Reference deck (template from this — never from scratch)
`~/Downloads/Decks/Wati - PMM Enablement - Session 1.pptx`
- Slides 1–9 = the real session (storyline). Slides 10–48 = a reusable **layout library** — clone the layout that fits each section and swap the content.

## Method
1. Read the pattern file + `DECK-PRINCIPLES.md`.
2. **Gather content** from `context/*.md` (what shipped / what's coming — kept current by the weekly refresh), the launch project (`~/projects/…`), the **battlecard / competitor-intel** for the competitive deep-dive, one real customer story, and where assets live. Borrow from Granola / a WebSearched support article when thin. Never fabricate — mark `[TBC]`.
3. **Follow the internal storyline** (pattern file): themed cover → what is this session → agenda → what we shipped → what's coming → competitive battlecard → customer story → where to find assets → Q&A → thank you. For a single-feature enablement, swap recap/roadmap for the feature (what it is, how to demo, plan, objections/FAQs, what to pitch against) — keep the internal arc.
4. **Build by templating** the reference deck: clone its slides / layout-library layouts and swap text in place (preserves DM Sans, burst, logo, brand tints). Fill grids evenly.
5. **Render + QA** every slide (LibreOffice → PyMuPDF PNG), run `wati-brand-auditor`, fix issues before showing Sunny.
6. Save to `~/projects/<launch>/outputs/enablement-session-<launch>.pptx`.

## Content notes
- **Value/enablement first** — equip the rep: what it means for the customer, how to sell it, what to pitch it against. Not a feature dump.
- Internal tone: a playful themed cover is on-brand here (the reference used "Avengers"). Keep the body clear and useful.
- Footer `www.wati.io | hello@wati.io`.

## Mistakes to never repeat
Template (never from scratch) · render before "done" · fill grids evenly · use brand-auditor guidelines · don't mix deck types · install DM Sans (serif = missing font).
