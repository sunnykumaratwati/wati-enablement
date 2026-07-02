# Deck Build-Prompt Template

**A deck agent's deliverable is a BUILD PROMPT, not a finished deck.** After the storyline is signed off, the agent writes a self-contained prompt (save as `<project>/BUILD-PROMPT.md`) that any Claude Code session can run to generate the deck on Wati's design system. Fill every section below.

---

## `# BUILD PROMPT — <Deck Name>`

**1. Deck type & audience** — which of the 4 types, who it's for, the setting.

**2. Why this storyline** — 1–2 lines on the arc chosen for this deck type (internal enablement / product / onboarding) and what it must achieve.

**3. Storyline (approved) — beat by beat.** For each beat: `#. <beat name> — <what it accomplishes> — CONTENT: <the actual copy to place> — LAYOUT: <layout from DESIGN-LIBRARY> — CLONE: <source deck + slide #>`.

**4. Design system (non-negotiable)** — paste the pattern from `DESIGN-LIBRARY.md`: 10×5.625 canvas, one font per deck (DM Sans default; both installed), exact palette, burst on every content heading, logo + `www.wati.io | hello@wati.io` footer, tinted rounded cards / no shadows.

**5. Build method** — clone the real source slide (shapes/fills/fonts untouched) → replace ONLY text, run-by-run → fit copy to each placeholder (never overflow) → fill every slot (no empty box / no leftover Lorem/Icon/TYPE) → **screenshots = a clean labelled placeholder** (Sunny drops the export) → **normalize all runs to the deck's one font**. Feature slides use text-left + a LARGE product-mockup panel (like WhatsApp Calling S7), NOT tiny emoji in empty cards.

**6. Inputs & rules** — positioning + banned words (from `context/positioning.md` / launch CONTEXT), plan eligibility, real-data-only (mark `[STAT — TBC]`), screenshots to place, naming rules.

**7. 100% design gate** — render every slide (both fonts installed) → run `wati-brand-auditor` + per-slide check vs the source layout → fix until every slide scores 100% on font/palette/burst/logo/overflow/empty-slots/leftovers/alignment. Only ship at 100%.

**8. Output** — save to `<project>/outputs/<name>.pptx`; show rendered montage.

---
The prompt is the handoff. It must be complete enough that the builder never has to guess about design.
