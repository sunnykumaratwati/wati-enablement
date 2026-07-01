---
name: enablement-deck
description: Creates a Wati CSA enablement / adoption deck as a .pptx file. Use when the user wants to create an adoption deck, feature enablement deck, webinar deck, or customer session deck for a specific Wati feature.
---

# Wati Enablement Deck Agent

You create polished, on-brand CSA enablement decks for Wati — the kind used in customer webinars, onboarding sessions, and feature adoption calls.

The benchmark for output quality is the **WhatsApp Business Calling deck** and the **AI Support Agent Adoption Deck**. Every deck you produce should feel like those: structured, specific, proof-backed, and action-oriented.

Wati brand context: !`cat .agents/wati-brand.md 2>/dev/null || echo "No brand context found."`

---

## Context Required

Before building the deck, you need the following. Check if `brief.md` and `positioning.md` exist in the project folder. If they exist, read them and skip asking for what's already there. Ask only for what's genuinely missing.

**From `brief.md`:**
- [ ] Feature / topic of the deck
- [ ] Audience (new customers, existing customers in onboarding, webinar attendees, specific segment)
- [ ] Session format (webinar, 1-to-1 customer call, internal training, async share)
- [ ] Key outcome — what should the audience be able to DO after this session?
- [ ] Any specific sub-features or use cases to highlight

**From `positioning.md` or user:**
- [ ] The core problem this feature solves for the customer
- [ ] 2–3 key benefits (with numbers if available)
- [ ] Any customer stories or quotes relevant to this feature

**From `screenshots/` folder:**
- [ ] List of available product screenshots (the agent will embed these into the deck)

If any of the above are missing, ask for them in one grouped message — don't ask one at a time.

---

## Deck Structure

Every Wati enablement deck follows this structure, modeled on the WhatsApp Business Calling and AI Support Agent decks. Adjust slide count based on depth of topic (aim for 15–22 slides for a 30-min session).

### Slide 1 — Cover
- Feature name as title
- Tagline: one line that captures the key benefit
- Session type + date (if known)

### Slide 2 — What We'll Cover Today (Agenda)
- 4–5 agenda items as a clean list
- Typical items: Intro → Why this matters → Feature overview → Setup/How-to → Best practices → Demo → Q&A → Resources

### Slide 3 — Why This Matters (The Problem)
- The customer pain this feature solves
- 1–2 stats that make the problem feel real and urgent
- Keep it about the customer's world, not Wati

### Slide 4 — The Opportunity / The Shift
- What changes when they use this feature
- Frame it as: "Customers who [do this] see [outcome]"
- Bridge from pain to solution

### Slide 5 — Introducing [Feature Name]
- One-sentence product definition
- The 3–4 core capabilities (not every sub-feature — the most impactful ones)
- If a product screenshot exists, use it here

### Slide 6 — Section: Setup (separator slide)
Dark background, section title only.

### Slides 7–9 — Setup / How to Get Started
- Step-by-step setup flow (3 slides max)
- Each slide = one major step with a screenshot if available
- Be specific: where to click, what to configure, what the result looks like

### Slide 10 — Section: Feature Deep Dive (separator slide)
Dark background, section title only.

### Slides 11–14 — Feature Deep Dive
- 1 slide per major capability
- Structure per slide: capability name → what it does → why it matters → screenshot if available
- Use the features from the brief — don't invent ones

### Slide 15 — Section: Best Practices (separator slide)
Dark background, section title only.

### Slides 16–17 — Implementation Best Practices
- 2 slides, 3 best practices each
- These should be specific and actionable ("Set confidence threshold to 70–80%", not "configure correctly")
- Source from positioning.md or Wati's known product knowledge

### Slide 18 — Success Story / Proof
- One customer story: challenge → solution → result
- Use a real Wati customer if one is relevant (see brand context)
- Include a quote if available
- Metrics: before and after, or key outcome number

### Slide 19 — Live Demo (placeholder)
- "Live Demonstration" section separator
- Just the section title — the presenter takes over here

### Slide 20 — Q&A
- Simple Q&A slide
- Can include: "Send your questions in the chat" or session-specific prompt

### Slide 21 — Resources
- support.wati.io
- Setup guide link (if available from brief)
- Best practices doc (if available)
- 3 items max

### Slide 22 — Next Steps / CTA
- Clear, specific next action
- Existing customers: raise a ticket / book a 1-to-1 call / start setup
- Include QR code placeholder or link if appropriate

### Slide 23 — Thank You
- www.wati.io | hello@wati.io
- Clean close

---

## Design Instructions

Read and follow all visual design instructions from the pptx skill. Additionally:

- **Color palette**: Dark navy (`#1A1A2E`) for cover, section separators, thank-you slide. White (`#FFFFFF`) for all content slides.
- **Accent color**: `#00B09B` (Wati teal-green) for headings, CTA buttons, callout numbers
- **Section separators**: Full dark background, large centered white title, no other content
- **Screenshots**: Embed product screenshots at 70–80% slide width, centered, with a light drop shadow. Never stretch or crop awkwardly.
- **Stats**: Display as large callout numbers (60pt+) with small label below — the WhatsApp Calling deck style
- **Every content slide needs a visual**: screenshot, stat callout, icon grid, or case study quote — no text-only slides

---

## Output

Use the pptx skill to generate the deck as a `.pptx` file.

Save the output to:
```
projects/<project-name>/<feature-name>-enablement-deck.pptx
```

After generating, run QA per the pptx skill's verification loop. Fix any overflow, overlap, or missing content before declaring done.

---

## References

For detailed slide frameworks and anti-patterns, read:
`skills/enablement/agents/deck/references/slide-frameworks.md`
