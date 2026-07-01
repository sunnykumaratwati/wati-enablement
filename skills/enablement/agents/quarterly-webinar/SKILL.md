---
name: wati-launch-day
description: Creates Wati's quarterly product-updates webinar deck — "Wati Launch Day". Use when someone says "create the quarterly webinar deck", "build the product updates webinar", "Wati Launch Day deck", "what's new at Wati deck", or "quarterly product updates". This is the external customer-facing webinar where a quarter's shipped features are introduced.
---

# Wati Launch Day — Quarterly Product Updates Webinar

You build Wati's flagship quarterly customer webinar deck: **Wati Launch Day**. External, customer-facing, all plans. It introduces every feature shipped that quarter, organized into themes, in Wati's established format.

> **Deck-type hierarchy — do not overlap.** "Webinar" is ONE type of deck; "quarterly product-updates webinar" (this: Wati Launch Day) is ONE sub-type within it. Feature/product webinars, launch-enablement decks, adoption decks, and marketing decks are DIFFERENT types with different storylines and designs. Never borrow a marketing deck's storyline/design for a quarterly webinar, and never mix sub-types. This agent covers ONLY the quarterly Launch Day webinar.

**First read the shared `skills/enablement/DECK-PRINCIPLES.md`** — universal rules for every deck.

## Mistakes to NEVER repeat (learned the hard way)
1. **Never build from scratch** — always template a real reference deck (from-scratch loses font, burst, logo, layout).
2. **Never declare "done" without rendering** every slide and eyeballing it (LibreOffice → PyMuPDF PNGs → fresh-eyes QA).
3. **Never leave an empty grid cell** — fill "Also Shipped" grids evenly (clone a card or fold two minors).
4. **Never reverse-engineer the design** — use the authoritative `wati-brand-auditor` brand guidelines.
5. **Never mix deck types** — webinar ≠ quarterly-webinar ≠ marketing; separate storylines and designs.
6. **Install DM Sans first** — a serif render means the font is missing, not that the deck is wrong.

## Proven build recipe (templating — the ONLY correct method)
Do NOT generate slides from scratch. Clone the latest quarterly deck and swap text in place:
1. `Presentation(<latest quarterly deck>.pptx)`; `slides = list(prs.slides)`.
2. Map Q-content onto slides by (slide#, shape-index). Replace text by editing `paragraph.runs[0].text` and deleting extra runs/paragraphs — this preserves DM Sans, colours, burst, logo.
3. Delete surplus template slides (extra demos / features you don't need) via `prs.slides._sldIdLst.remove(...)`.
4. **Remove mismatched leftover graphics**: small per-feature icons on feature slides (Q1 slides carry a feature-specific icon, e.g. a mic — remove pictures with width < 1.5" and top > 3.0"); leftover demo screenshots (they carry a "Made with dubbr" watermark — remove pictures wider than 5" on `Demo:` slides).
5. **Fix stray references** from the source deck (e.g. `clare.ai` → `wati.io`); strip any `[TBC]` tags from customer-facing lines.
6. **Renumber page numbers** (bottom-area bare-integer shapes) after deletion.
7. **Verify by rendering**: LibreOffice `--convert-to pdf` → PyMuPDF (`fitz`) per-slide PNG at ~110 dpi → visual QA with a subagent (fresh eyes) → fix overflow/artifacts. Install DM Sans first or renders show substitute serif.
8. Watch text overflow: Q-copy longer than the template's original box overflows — keep divider descriptors and feature blocks close to the reference's length.
9. **Fill grids evenly — never leave a partial row.** "Also Shipped" slots are grids (S13 = 2×2/4, S21 = 2×3/6, S29 = 3). Match your item count to the slot count. If you have one too few, either add a real item or clone a card into the empty cell (copy the card's bg+strip+title+desc shapes, offset left/top, set text) — an empty grid cell reads as broken. If one too many, fold two minor items into one card.
(Reference implementation: `~/projects/q2-2026-launch-day/template_deck.py`.)

Wati brand context: !`cat .agents/wati-brand.md 2>/dev/null || echo "No brand context file found."`

**Read the pattern file before building anything:**
`skills/enablement/agents/quarterly-webinar/references/wati-launch-day-pattern.md`

It contains the exact slide-by-slide skeleton extracted from Wati's real Q1 2026 and Q4 '25 decks. Follow it precisely — this is the house format, not a suggestion.

**Use the Product Knowledge Base for feature integrity:** `context/` holds one file per Wati product category (see `context/README.md`). When a feature in the quarter feed is one you don't know deeply (e.g. an Astra release), read the matching category file (`context/ai-astra.md`, etc.) for its positioning, plan, proof points, and do's/don'ts. This is how you present every feature accurately — even ones you didn't build.

---

## The workflow: Features in Focus → reconcile → deck

The deck is built from a **"Features in Focus" doc** — the curated, themed list of the quarter's customer-impacting launches. **Read `references/features-in-focus-format.md`** for its format and curation rules.

### Step 1 — Build or receive the Features in Focus doc
- If the user asks *"what launched this quarter?"* → generate the doc from `context/*.md` (dated "Recently Shipped" sections) + Slack #product-updates-gtm, applying the curation rules: include only features impacting **existing paying customers**; **exclude trials, signups, packaging/pricing, pure-marketing**; group into 3–5 themes. **The lead theme is the PMM's call — ask which theme leads; don't assume.** Default proposal: lead with the biggest-MRR/marquee theme, then order the rest by impact, and let the user confirm or override. (Q2 2026: PMM chose Astra to lead.)
- If the user already has a doc (e.g. a Notion "Features in Focus" page), use it as the base.

### Step 2 — Reconcile before building (the "any updates to add?" check)
Cross-check the doc against the latest `context/*.md` and Slack #product-updates-gtm for anything launched since the doc was written or missing from it. **Surface proposed additions/changes to the user and confirm before building the deck.**

### Step 3 — Gather remaining inputs
- **Quarter + year + month**, webinar date/speakers
- **Quarter stats** — features shipped, bugs fixed, channels live (for "At a Glance"); mark `[# — TBC]` if unknown
- **Next-quarter roadmap** — 4–6 upcoming items for the teaser
- **Screenshots / demo links** — optional; use placeholders if absent

Pull each feature's depth (value prop, positioning, plan, proof) from the matching `context/*.md`. Minor features go into an **"Also Shipped in [Quarter]"** grid at the end of their theme. Do not invent features or stats — mark `[TBC]` and flag.

---

## Step 3 — Build the deck

Follow the skeleton in the pattern file:

1. Title
2. Quarter at a Glance (3 big stats + one-line summary)
3. Themes overview (numbered 01–0N)
4. Per theme: divider → feature slides (PROBLEM / UPDATE / WHAT'S IN IT FOR YOU + Plan) → demo slides → "Also Shipped" grid
5. Bonus — Pro Tips (Try Higher Plan, Astra trial)
6. What's Coming Next Quarter (roadmap grid)
7. Q&A
8. Thank You

**Build by TEMPLATING a real deck — never from scratch.** Start from the latest quarterly deck (`~/Desktop/Decks/Webinar Decks/Quarterly Updates/`), keep its masters/layouts/logo/burst/fonts, duplicate its divider / feature / demo / grid slide types as needed, and swap only the text to the Q2 content. Follow `context/design-system.md` (which defers to the wati-brand-auditor brand guidelines). Then **run the `wati-brand-auditor` skill** on the output and fix every flagged issue before showing the user.

---

## Format Rules (do not break)

- **Every feature slide uses THE PROBLEM / THE UPDATE / WHAT'S IN IT FOR YOU + a Plan tag.**
- **Footer on every content slide:** `www.wati.io  |  pmm@wati.io` + page number.
- **Demo slides are minimal** — just "Demo: [feature name]".
- **Numbered theme dividers** (#1, #2…) separate every theme.
- **Roadmap teaser** closes the content before Q&A.
- No fabricated stats or quotes — mark `[STAT — TBC]`.
- Plain English, benefit-led headlines. No "we're excited to announce."

---

## Design

**Read `context/design-system.md` and follow it exactly** — it holds the real Wati deck values reverse-engineered from production decks. Key points:
- Canvas: **16.0 × 9.0 in** (current quarterly standard)
- Font: **DM Sans** (Light/Medium/SemiBold) — the real brand font. Note: DM Sans may substitute in LibreOffice QA, so trust the ~10% slack over the QA preview for text-fit; it renders correctly in PowerPoint on Wati machines.
- Brand green **`#00E785`** (the one saturated accent), text **`#1D1D1D`**, footers **`#828282`** 9pt
- Pastel tint blocks: mint `#CAFDE8`, sky `#E3F5FF`, lavender `#FDECFF`, cream `#FFF6DA`
- Eyebrows: 11pt ALL-CAPS bold, color-coded (PROBLEM/UPDATE = blue `#4FC3FF`, WHAT'S IN IT FOR YOU = green `#00E785`)
- Section dividers: giant 96pt "#N" on a tint or dark `#1D1D1D` block
- Footer every slide: `www.wati.io  |  pmm@wati.io` bottom-left + page number bottom-right
- Every feature/demo slide: `[SCREENSHOT PLACEHOLDER]` where product UI goes — never invent UI.

**Align all copy to `context/positioning.md`** — the latest Wati positioning (naming rules, banned words, revenue-pillar framing).

---

## After generating

1. Convert to images, run visual QA (pptx skill verification loop)
2. Run `wati-brand-auditor` skill on thumbnails if available
3. Show thumbnails to user for approval
4. Ask what to refine; log learnings back to the project context
5. Save to `~/projects/<quarter>/outputs/wati-launch-day-<quarter>.pptx`
