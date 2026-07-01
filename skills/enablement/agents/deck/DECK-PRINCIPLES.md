# Deck-Building Principles (shared by every deck agent)

Decks are **enablement assets**. Inside enablement → **deck** → four individually-trained deck-type agents, each under `skills/enablement/agents/deck/`:
1. **onboarding-deck** — 1–2 feature slides inserted into the marketing/onboarding deck
2. **product-deck** — the complete customer- & sales-facing product deck
3. **enablement-webinar** — the internal launch-enablement webinar deck
4. **quarterly-webinar** — the quarterly product-updates webinar (Wati Launch Day)

All four inherit the principles below (accumulated feedback; do not violate). Each is trained individually for its own storyline/design — never overlap them.

## 1. Design is the whole game — replicate a designed layout, never strip to plain text
**Order of work: (1) story → (2) content → (3) map each slide to a DESIGNED layout and fill it.**
- Clone a **polished, designed layout slide** and fill ITS placeholders (cards, icon grids, columns, quote blocks, tables) — keep every design element intact. **Never** reduce a designed slide to a bare title + paragraph, and never delete the design shapes. A plain title+body slide is a FAILED slide.
- **Design base / template library:** `~/Desktop/Example Data/Wati Deck - Sales Template 2026.pptx` — a full library of designed layouts (covers, section separators, icon grids, 3/4-point layouts, quote+highlights, image grids, funnels, comparison tables, next-steps, thank-you). Also `WhatsApp Business Calling.pptx`, `Wati for Marketing_ Deck Draft_ Final.pptx`.
- For each planned slide, pick the layout whose **shape matches the content** (2 items → 2-column; 3 benefits → 3-icon-grid; a quote → quote layout; specs → table) and fill the labelled placeholders. Match content to a designed layout — don't force content into a text box.
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

## 6. Verify by rendering — before "done"
Render every slide (LibreOffice → PyMuPDF PNG) and QA with fresh eyes (overflow, empty cells, leftover graphics, mislabeled pills, naming/plan). Run `wati-brand-auditor` on the output. Never declare done on un-rendered code.

## Render pipeline (this environment)
DM Sans installed in `~/Library/Fonts`; portable LibreOffice mounted at `/tmp/LOmount` (`soffice` at `/tmp/LOmount/LibreOffice.app/Contents/MacOS/soffice`); PyMuPDF (`fitz`) present. Pattern:
`soffice --headless --convert-to pdf --outdir . <deck>.pptx -env:UserInstallation=file:///tmp/louser` → `fitz` render pages to PNG at ~110–130 dpi.
