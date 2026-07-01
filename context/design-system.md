# Wati Deck Design System Spec

Reverse-engineered from 5 production decks (2 quarterly webinar decks, the Wati AI webinar, WhatsApp Calling, and Wati for Marketing). Use these exact values to reproduce Wati's look and feel.

---

## 1. Slide dimensions

Two canvas sizes are in use. **Standardize new webinar/quarterly decks on 16:9 at 16.0 × 9.0 in** — that is the current quarterly format (Q4 '25).

| Deck | Size (in) | Notes |
|---|---|---|
| Q4 '25 Quarterly | **16.0 × 9.0** | Current standard, use this |
| Wati AI Webinar | 16.0 × 9.0 | Same standard |
| Q1 Astra Quarterly | 13.333 × 7.5 | Older 16:9 (10"-scale) — geometry values below are on this canvas |
| WhatsApp Calling | 10.0 × 5.625 | Compact 16:9 |
| Wati for Marketing | 10.0 × 5.625 | Compact 16:9 |

All decks are 16:9 aspect ratio. Geometry below notes which canvas each measurement came from; scale proportionally.

---

## 2. Color palette

The palette is **light, pastel-tinted, with one vivid brand green**. Backgrounds are white or soft pastel tint blocks; text is near-black; the green is the single saturated accent. Frequency counts confirm the true palette.

### Core
| Role | Hex | Notes |
|---|---|---|
| **Brand green (primary accent)** | `#00E785` | The signature vivid green. Used for accent fills, stat numbers, "WHAT'S IN IT FOR YOU" labels, dots, buttons. Darker variant `#009958` appears occasionally for green text on light bg. |
| **Near-black (primary text)** | `#1D1D1D` | Default title + body text color. Also used as dark-section background fill. |
| **Pure black** | `#000000` | Secondary text color (heavier decks). |
| **Off-black** | `#030303` | Occasional body text. |
| **White** | `#FFFFFF` | Background, and text on dark/green blocks. |
| **Muted grey (footer/caption text)** | `#828282` | Footer + page-number text. Lighter greys `#ADADAD`, `#666666`, `#3D3D3D` for secondary captions. |

### Pastel tint blocks (card / background fills)
These are the recurring soft category tints. Each has a lighter wash variant.
| Tint | Hex | Lighter wash |
|---|---|---|
| **Mint / green tint** (most common) | `#CAFDE8` | `#B3FFDF`, `#CCFFE9` |
| **Sky blue tint** | `#E3F5FF` / `#E4F8FF` | `#D2F4FF`, `#AAEAFF` |
| **Lavender / pink tint** | `#FDECFF` | — |
| **Cream / yellow tint** | `#FFF6DA` / `#FFFBE3` | — |

### Accent / category dot colors
Used for category dots, icon accents, eyebrow labels, small highlights:
| Accent | Hex |
|---|---|
| **Blue** | `#4FC3FF` (also `#64D8FF`) |
| **Pink / magenta** | `#F9B4FF` (also `#F6B8FD`) |
| **Yellow** | `#FFE96E` (also `#FFD966`) |
| **Green** | `#00E785` |

**Rule of thumb:** white or a single pastel tint as the slide background, `#1D1D1D` text, `#00E785` for the one thing you want to pop, and the blue/pink/yellow accents rotate to color-code categories or eyebrow labels.

---

## 3. Fonts

**Primary typeface: `DM Sans`** across all webinar/quarterly/product decks. Weight-named variants are used explicitly: `DM Sans Light`, `DM Sans Medium`, `DM Sans SemiBold`.

- The **Wati for Marketing** deck is the outlier — it uses **`Outfit`** (with `Outfit Light/Medium/SemiBold/ExtraBold`). Outfit is a close geometric-sans cousin of DM Sans. **For new decks default to DM Sans**; use Outfit only if matching that marketing lineage.
- Stray `Calibri` / `Helvetica Neue` appear a handful of times (accidental, not brand).

### Type scale (pt) — by role, from the 16:9 quarterly decks
| Role | Size (pt) | Weight | Color |
|---|---|---|---|
| Cover mega-title | **96** | Bold | `#1D1D1D` or white on dark |
| Cover subtitle | 36 | Regular/Medium | `#1D1D1D` |
| Section-divider number ("#1") | 96 | Bold | white/`#1D1D1D` |
| Slide title | **40** (16:9) / **28** (13.3" canvas) | Bold | `#1D1D1D` |
| Big stat number | 44.8–59 | Bold | `#00E785` or `#1D1D1D` |
| Section header / list heading | 18 | Bold/SemiBold | `#1D1D1D` |
| Body text | **16–18** (16:9) / **13** (13.3") | Regular | `#1D1D1D` |
| Eyebrow / category label | **11** | **Bold, ALL CAPS** | accent color (see below) |
| Caption / small body | 13–15.5 | Regular | grey/`#1D1D1D` |
| Footer + page number | **9** | Regular | `#828282` |

---

## 4. Layout geometry

(Measurements from Q1 Astra 13.333 × 7.5 canvas unless noted; scale ×1.2 for the 16.0 × 9.0 canvas.)

- **Left content margin:** ~0.87–0.97 in from left edge on 16:9; titles and body share this left rail. Card/indented content sits ~1.06–1.25 in.
- **Title position:** top-left, T ≈ 0.72 in (13.3" canvas) / T ≈ 0.43–0.87 in (16:9). Left-aligned, never centered on content slides.
- **Subtitle/deck:** sits directly under title, ~0.6 in below, at body size.
- **Footer treatment (KEY MOTIF):**
  - Bottom-left: `www.wati.io  |  pmm@wati.io` — **9 pt, `#828282`**, at L≈0.5, T≈7.05 (13.3") i.e. ~0.45 in above the bottom edge.
  - Bottom-right: **page number**, same 9 pt `#828282`, at far right (L≈12.33 on 13.3" canvas).
  - On the 16:9 quarterly deck the footer is instead a **"Plan Availability: …"** line, centered-ish, ~15.5 pt, near bottom (T≈8.35 on 9" canvas).
- **Two-column pattern:** left column starts ~1.25 in, right column ~7.1 in (13.3" canvas) — roughly a 50/50 split with a center gutter. Used for THE PROBLEM / THE UPDATE side-by-side.
- **Stat callout row:** three evenly spaced stat blocks; on 13.3" canvas at L≈1.32 / 4.92 / 8.51 (≈3.6 in pitch), each ~2.47 in wide. Big number (44.8 pt) stacked over a label (15.3 pt).
- **Cards/pills:** rounded auto-shapes filled with a pastel tint (`#CAFDE8` etc.) or `#1D1D1D` for dark pills; label text sits inside, bold. "Plan: All Plans" is a small dark/green pill with white 11 pt bold text.

---

## 5. Recurring slide archetypes

### A. Cover slide
- Full-bleed background: either **dark `#1D1D1D`** (Q1 Astra) or white/tint.
- Mega-title 96 pt bold, left-aligned, upper-third (T≈1.5 in).
- Secondary line 48–58 pt (e.g. "What's Cooking at Wati?").
- Bottom eyebrow strip: `Product Updates | Online | Apr 2026` at ~12–16 pt, using ` | ` pipe separators — a recurring Wati convention for cover metadata.

### B. Section divider slide (KEY MOTIF)
- Background = a full pastel tint block (e.g. `#CAFDE8`) OR dark `#1D1D1D`.
- **Giant "#1" number, 96 pt bold**, top-left.
- Section title 40 pt bold below it, then a 16 pt one-line descriptor.
- Footer still present.

### C. Content slide — "THE PROBLEM / THE UPDATE / WHAT'S IN IT FOR YOU" (signature layout)
- Title 28 pt (13.3") / 40 pt (16:9) bold `#1D1D1D`, top-left.
- **Eyebrow labels are ALL CAPS, 11 pt, bold, color-coded:**
  - `THE PROBLEM` → **blue `#4FC3FF`**
  - `THE UPDATE` → **blue `#4FC3FF`**
  - `WHAT'S IN IT FOR YOU` → **green `#00E785`**
- THE PROBLEM (left col) and THE UPDATE (right col) sit side-by-side ~1.85 in from top; body 13 pt regular under each.
- WHAT'S IN IT FOR YOU spans full width below (~4.15 in), body 14 pt **bold** `#1D1D1D`.
- A **plan pill** ("Plan: All Plans") 11 pt bold white on a filled pill near bottom.

### D. Stat / social-proof slide
- Title 26–28 pt bold.
- Row of big stats: number 59 pt bold (`#00E785` or dark), sub-label 13 pt underneath. E.g. "77% / 40% / 76%".
- Optional large supporting sentence (23 pt) below the stat row.

### E. Feature-benefit list slide
- Title 40 pt bold.
- Repeating pairs: **bold 18 pt heading** (e.g. "Instant Escalation") + **16 pt regular** description, stacked with ~1.2 in vertical rhythm.
- Each item often prefixed by a colored category dot (blue/pink/yellow/green accents).

### F. "Journey / loop" diagram slide
- Title 40 pt + 18 pt subtitle.
- Stage labels (Attract, Qualify, Engage, Convert, Retain, Intelligence) as 18 pt bold headings positioned around a circular/loop layout, each with a 18 pt description block.
- Closing 15.5 pt italic-tone summary line at the bottom.

### G. Demo slide
- Minimal: title `Demo: <Feature>` at 28/40 pt bold.
- Often a **dark `#1D1D1D` background** (Q1 Astra demo slides) with white title, or a plain slide holding a screenshot/embed.
- Plan-availability footer line present.

---

## 6. Quick build checklist

1. Canvas 16.0 × 9.0 in.
2. Font: DM Sans (Light/Medium/SemiBold as needed).
3. Text `#1D1D1D`; footers `#828282` at 9 pt.
4. One saturated accent: `#00E785`. Category coding via `#4FC3FF` (blue), `#F9B4FF` (pink), `#FFE96E` (yellow).
5. Backgrounds: white or a single pastel tint — mint `#CAFDE8`, sky `#E3F5FF`, lavender `#FDECFF`, cream `#FFF6DA`.
6. Titles 40 pt bold top-left; body 16–18 pt; eyebrows 11 pt ALL-CAPS bold in an accent color.
7. Footer: `www.wati.io  |  pmm@wati.io` bottom-left + page number bottom-right, both 9 pt `#828282` (quarterly decks may swap in a "Plan Availability:" line).
8. Section dividers: giant 96 pt "#N" on a tint or dark block.
9. Use the THE PROBLEM / THE UPDATE / WHAT'S IN IT FOR YOU three-block layout for feature updates.
