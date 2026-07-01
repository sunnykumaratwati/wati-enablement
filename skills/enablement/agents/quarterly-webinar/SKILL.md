---
name: wati-launch-day
description: Creates Wati's quarterly product-updates webinar deck — "Wati Launch Day". Use when someone says "create the quarterly webinar deck", "build the product updates webinar", "Wati Launch Day deck", "what's new at Wati deck", or "quarterly product updates". This is the external customer-facing webinar where a quarter's shipped features are introduced.
---

# Wati Launch Day — Quarterly Product Updates Webinar

You build Wati's flagship quarterly customer webinar deck: **Wati Launch Day**. External, customer-facing, all plans. It introduces every feature shipped that quarter, organized into themes, in Wati's established format.

Wati brand context: !`cat .agents/wati-brand.md 2>/dev/null || echo "No brand context file found."`

**Read the pattern file before building anything:**
`skills/enablement/agents/quarterly-webinar/references/wati-launch-day-pattern.md`

It contains the exact slide-by-slide skeleton extracted from Wati's real Q1 2026 and Q4 '25 decks. Follow it precisely — this is the house format, not a suggestion.

**Use the Product Knowledge Base for feature integrity:** `context/` holds one file per Wati product category (see `context/README.md`). When a feature in the quarter feed is one you don't know deeply (e.g. an Astra release), read the matching category file (`context/ai-astra.md`, etc.) for its positioning, plan, proof points, and do's/don'ts. This is how you present every feature accurately — even ones you didn't build.

---

## Step 1 — Gather the quarter's inputs

Check for a project folder first (`ls ~/projects/`) — the quarter's release notes may already be there. If not, ask the user for:

1. **Quarter + year + month** (e.g. Q2 2026, webinar in July)
2. **Features shipped this quarter** — for each: name, the problem, what shipped, the benefit, plan eligibility. Accept this as a list, a Notion link, or a release log — whatever the user has.
3. **Quarter stats** — features shipped, bugs fixed, channels live (for "At a Glance"). Mark `[# — TBC]` if unknown.
4. **Next-quarter roadmap** — 4–6 upcoming items for the teaser.
5. **Screenshots / demo links** — for features that get a demo slide (optional; use placeholders if absent).

Do not invent features or stats. If something is missing, mark it `[TBC]` and flag it.

---

## Step 2 — Group features into themes

Cluster the features into **4–6 numbered themes**. The recurring Wati themes are:
- **AI at Wati** (Astra, Copilot, voice agents)
- **Multichannel Conversations** (WhatsApp, Instagram, Messenger, RCS, SMS, TikTok)
- **Sales & Marketing Automation** (campaigns, segments, sequences, CTWA)
- **Ecommerce / Shopify Growth**

If the features don't map cleanly to these, propose a grouping and confirm with the user before building.

Minor features that don't warrant a full slide go into an **"Also Shipped in [Quarter]"** grid at the end of their theme.

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

Use the pptx skill to generate the `.pptx`.

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
