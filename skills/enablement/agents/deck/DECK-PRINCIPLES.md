# Deck-Building Principles (shared by every deck agent)

Decks are **enablement assets**. Inside enablement → **deck** → four individually-trained deck-type agents, each under `skills/enablement/agents/deck/`:
1. **onboarding-deck** — 1–2 feature slides inserted into the marketing/onboarding deck
2. **product-deck** — the complete customer- & sales-facing product deck
3. **enablement-webinar** — the internal launch-enablement webinar deck
4. **quarterly-webinar** — the quarterly product-updates webinar (Wati Launch Day)

All four inherit the principles below (accumulated feedback; do not violate). Each is trained individually for its own storyline/design — never overlap them.

## 1. Template — never from scratch
Clone the matching real reference deck and swap text/content in place (preserves logo, burst, DM Sans, layout). Building slides from code loses all of it. See `context/design-system.md` (source of truth = the `wati-brand-auditor` brand guidelines).

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
