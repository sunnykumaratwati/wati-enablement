---
name: product-deck
description: Creates Wati's complete product deck — the customer- and sales-facing deck that presents the whole product/solution. Use when someone says "create the product deck", "sales deck", "customer-facing deck", "the full Wati deck", or "solution deck for [product/segment]". NOT the quarterly webinar (see quarterly-webinar), the internal enablement webinar (see enablement-webinar), or onboarding-deck slides (see onboarding-deck).
---

# Product Complete Deck — Customer & Sales Facing

**First read the shared `skills/enablement/agents/deck/DECK-PRINCIPLES.md`** — the universal deck-building rules (template not scratch, value-first, render-verify, glow-behind-mockups, fill grids, don't-mix-types). They apply to every deck.

This agent builds the **complete product deck** used with customers and by sales — the full solution story (problem → shift → product → proof → pricing/CTA). It is one of four deck types under `deck/`: quarterly webinar → `quarterly-webinar`; internal launch-enablement webinar → `enablement-webinar`; onboarding-deck feature slides → `onboarding-deck`.

Wati brand context: !`cat .agents/wati-brand.md 2>/dev/null || echo "No brand context file found."`

---

## Step 1 — Find existing context

Before asking the user anything, check if a project folder exists with a brief:

```bash
ls ~/projects/
```

Look for a folder matching the feature/topic. If found, read:
- `CONTEXT.md` — locked positioning, banned words, dates, facts
- `CAMPAIGNS-SALES-DECK-BRIEF.md` or `SLIDE-DECK-BRIEF.md` — slide-by-slide spec
- Any `*-BRIEF.md` file — detailed deck instructions

If a brief file exists, read it fully and follow its slide-by-slide spec exactly. Do not ask questions already answered in the brief.

---

## Step 2 — Determine deck type

Ask if not already clear from the brief:

> "What type of deck is this?"
>
> 1. **Launch / Sales Enablement deck** — internal + customer-facing, covers full feature story (10–15 slides)
> 2. **Webinar deck** — audience-facing, 30–60 min session, heavier on setup + demo cues (15–25 slides)
> 3. **Onboarding deck insert** — 1–3 slides to add into an existing master deck at a specific position
> 4. **1-to-1 CSM deck** — shorter, conversational, for a single customer call (8–12 slides)

Each type has a different structure. Do not use the same template for all four.

---

## Deck Type Structures

### Type 1 — Launch / Sales Enablement Deck
Follow the slide-by-slide spec in the brief exactly if one exists.
If no brief, default structure:
- S1 Title + tagline
- S2 The problem / why now
- S3 Two features overview (if multi-feature launch)
- S4–S6 Feature 1 deep dive (intro → how it works → use cases)
- S7–S9 Feature 2 deep dive (intro → how it works → use cases)
- S10 Why Wati wins / competitive + trust
- S11 Plans & eligibility
- S12 Objection handling / FAQ (rep-facing)
- S13 Next steps / CTA
- S14 Thank you + contact + restrictions

### Type 2 — Webinar Deck
- S1 Cover
- S2 Agenda (what we'll cover)
- S3 Why this matters (customer pain + stats)
- S4 Feature intro
- S5–S8 Setup steps (one major step per slide, with screenshot placeholder)
- S9 Section: Feature Deep Dive
- S10–S13 Feature deep dive (one capability per slide)
- S14 Best practices
- S15 Success story
- S16 Live demo cue (presenter takes over)
- S17 Q&A
- S18 Resources
- S19 Next steps / CTA
- S20 Thank you

### Type 3 — Onboarding Deck Insert (1–3 slides)
- Each slide: eyebrow pill (plan + AI label if applicable) + bold title + italic tagline + pain line + body + 3 benefit cards + screenshot placeholder + footer
- Match the design system of the master deck exactly
- Note where slides insert (e.g. "between slide 47 and 48")

### Type 4 — 1-to-1 CSM Deck
- 8–12 slides, conversational tone
- Lead with customer's specific situation, not generic pain
- Feature walkthrough: 3–4 capabilities max
- One customer story
- Clear next step

---

## Hard Rules (apply to all deck types)

When a CONTEXT.md or brief file exists for this project, its rules override everything else:

- Follow locked positioning exactly — tagline, sub, closing line
- Never use banned words listed in the context
- Never fabricate stats or customer quotes — mark as `[STAT — TBC]`
- Respect plan eligibility (e.g. "Pro & Business only" vs "every plan")
- Respect AI scope — only apply AI claim to features explicitly marked as AI
- Use exact feature names from the brief, not variations

---

## Design Instructions

**Read `context/design-system.md` and follow it** — real Wati deck values (DM Sans, brand green `#00E785`, `#1D1D1D` text, pastel tints, 16×9). Exception: a project with its own locked palette in its CONTEXT/brief (e.g. the Campaigns launch uses `#00C8B7`) overrides the general design system — follow the project brief in that case.
- Every product slide: clearly marked **[SCREENSHOT PLACEHOLDER]** — never invent product UI
- No accent stripes, no title underlines, no color bars
- Align all copy to `context/positioning.md` (naming rules, banned words, revenue-pillar framing)

---

## After generating

1. Convert to images and run visual QA (pptx skill verification loop)
2. Run `wati-brand-auditor` skill on thumbnails if available
3. Show thumbnails to user for approval
4. Ask: "Anything to update — copy, structure, design? I'll log it to the project context."
5. Save output to `~/projects/<project-folder>/outputs/<deck-name>.pptx`

---

## References

`skills/enablement/agents/deck/references/slide-frameworks.md`
