# Deck-Building Principles (shared by every deck agent)

Decks are **enablement assets**. Inside enablement → **deck** → four individually-trained deck-type agents, each under `skills/enablement/agents/deck/`:
1. **onboarding-deck** — 1–2 feature slides inserted into the marketing/onboarding deck
2. **product-deck** — the complete customer- & sales-facing product deck
3. **enablement-webinar** — the internal launch-enablement webinar deck
4. **quarterly-webinar** — the quarterly product-updates webinar (Wati Launch Day)

All four inherit the principles below (accumulated feedback; do not violate). Each is trained individually for its own storyline/design — never overlap them.

## RESEARCH CHAIN — before the story, gather DEEP context (mandatory, every deck)
A shallow deck = a failed deck. Before writing the storyline, gather real depth from ALL of:
1. **Feature Launch Doc** (the PMM's go-to brief — Google Sheet/PRD): why launching, feature description, key capabilities incl. HOW it works, launch tier/pricing, objectives, target geos, personas + pain + messaging, PMM launch activities. This is the base for every launch.
2. **PRD problem/pain-points FIRST** — read the PRD's 'why we're launching' + persona pain points before anything else. **Each feature solves its OWN distinct pain — do NOT invent one unifying problem** (e.g. don't blame 'the list view' for everything). Multi-feature launches (e.g. Campaign Calendar + AI Recommendations vs Drip) have separate pains that may only loosely relate via a common goal (save time / send more). Frame each feature's pain from the PRD, then research to deepen it.
3. **Support docs — ALWAYS WebSearch `support.wati.io` for the exact feature** + read it: step-by-step mechanics, settings, edge cases, and the REAL FAQs (auto-retry, static vs dynamic list, plan gating, how recs are generated). Non-negotiable — this is the core depth.
3. **Notion** launch hub / how-to / positioning / ICP / competition / emails.
4. **`context/<category>.md`** (KB) + the launch project folder.
5. **Web** for extra framing (e.g. what a great sales-enablement/feature-launch deck covers) — add sensible sections from your own product-marketer judgment.
Then INLINE all of it into the CONTEXT PACK (the builder can't read any of these).

## DEPTH & CALIBRATION (product-marketer brain)
- **Answer the questions people will actually ask.** Smart FAQs pulled from the support doc + PM briefing (not surface bullets). Reps must leave able to answer: does it work with auto-retry? static vs active list? how are recommendations made? plan gating?
- **Separate distinct concepts** and give each its own space — e.g. Campaign Calendar (the surface) vs AI Recommendations (incl. HOW they're generated) vs Drip. Missing 'how recs are made' is a failure.
- **Always include:** per-feature **use cases**, **personas + pain + messaging**, a **'how we're prepping for launch'** slide (PMM activities), and a closing **holistic** slide (e.g. everything Wati Campaigns now consists of).
- Calibration: impressive & complete, NOT a consulting wall of text and NOT 2 surface bullets. Empower the team — keep depth in the deck even if not all covered live.

## 0. STORY FIRST — hard gate (do not skip)
**Before any content or design, write the storyline and get Sunny's sign-off.** Save it as `STORYLINE.md` in the project: the narrative beats (what each beat accomplishes), not slides, not design. Present it and STOP. Only after approval do you write slide content, then match designs. Storyline differs per deck type (internal enablement vs product vs onboarding); it is always step one. Jumping to slides is the #1 failure — don't.

## One design system, many source decks
All Wati decks share **ONE design system** (verified across 10 decks — see `DESIGN-LIBRARY.md`): 10×5.625 canvas, DM Sans *or* Outfit (both installed; one font per deck; default DM Sans), fixed palette, the burst, tinted cards, footer. There is no single "template deck" — clone the **cleanest real instance** of the layout you need from any of the decks, then **normalize the deck to one font**. The shared invariants + the 100% gate guarantee consistency. (Storyline varies per deck type; design system is fixed.)

## 1. Design — clone a real designed layout, never strip to plain text
**Order of work: (1) story (gated) → (2) content → (3) match each slide to a DESIGNED layout in `DESIGN-LIBRARY.md`, clone the cleanest real instance, fill it, normalize the font.**
- Clone a **polished, designed layout slide** and fill ITS placeholders (cards, icon grids, columns, quote blocks, tables) — keep every design element intact. **Never** reduce a designed slide to a bare title + paragraph, and never delete the design shapes. A plain title+body slide is a FAILED slide.
- **Design source = the shared Wati design system**, catalogued in `DESIGN-LIBRARY.md` (layout → what content it fits → cleanest source deck + slide #). Clone only from the approved Wati decks; normalize the finished deck to one font.
- Building from code, or swapping only the title/body while removing the visuals, loses the design. Don't.

## 2. Match design exactly
DM Sans (install it — a serif render = missing font, not a broken deck). Brand palette only (`#00e785`, `#1d1d1d`, pastel tints). The **burst** on every content heading. Logo per slide type. No shadows; rounded tinted cards.

## 3. Design details not to miss
- **Soft circular glow behind mockups** — add a large light-tint OVAL behind each mockup/screenshot and **send it to back**. Not a flat rect.
- **Vary the accent/template per slide** so consecutive slides aren't identical.
- Keep left-column text clear of the right-column mockup/glow.
- **Fill grids evenly** — match item count to the template's slot count (clone a card or fold two minors). No empty grid cells / partial rows.

## 4. Content: VALUE first
Lead with the outcome/positioning (what it brings, how much value), then support with mechanics. Feature bullets alone = a failed slide. Pull value + positioning from `context/positioning.md` and the feature's `context/*.md`; borrow from Granola / launch projects / a WebSearched Wati support article when thin. Never fabricate — mark `[STAT — TBC]`. As PMM, judge how much depth a feature deserves and pick the template that does it justice.

## 5. Deck types don't overlap
Each type (quarterly webinar · onboarding-deck slide · product/feature webinar · launch-enablement session) has its own storyline + design. Never reuse one type's template for another, and never use a marketing deck as reference for a webinar. See `DECK-TYPES.md`.

## 5b. Fill the layout completely + fit the copy to it
- **Fill every icon placeholder.** No empty icon boxes or empty card bodies — a designed layout with blank slots looks unfinished. If no icon assets, use on-brand emoji icons (Wati internal decks do this: 📅 ✨ 🔁 💬 💸 🎯 📊). Fill empty tall-card bodies with a centred icon.
- **Fit copy to the placeholder, not the reverse.** If text overflows a pill/label/box (e.g. a narrow plan pill, a divider title, a column label), shorten the copy until it fits — don't let it spill or ghost. Match content length to the designed slot.

## 6. Verify by rendering — before "done"
Render every slide (LibreOffice → PyMuPDF PNG) and QA with fresh eyes (overflow, empty cells, leftover graphics, mislabeled pills, naming/plan). Run `wati-brand-auditor` on the output. Never declare done on un-rendered code.

## Render pipeline (this environment)
DM Sans installed in `~/Library/Fonts`; portable LibreOffice mounted at `/tmp/LOmount` (`soffice` at `/tmp/LOmount/LibreOffice.app/Contents/MacOS/soffice`); PyMuPDF (`fitz`) present. Pattern:
`soffice --headless --convert-to pdf --outdir . <deck>.pptx -env:UserInstallation=file:///tmp/louser` → `fitz` render pages to PNG at ~110–130 dpi.
