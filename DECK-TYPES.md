# Wati Deck Types

Wati makes distinct deck types. **Each has its own storyline, audience, and design — never overlap or reuse one type's template for another.** Route each request to the right agent.

| # | Type | Purpose & audience | Storyline / design | Agent | Status |
|---|------|-------------------|--------------------|-------|--------|
| 1 | **Quarterly product-updates webinar** ("Wati Launch Day") | External customers. Introduce everything shipped that quarter, grouped into themes. | Quarter-at-a-glance → numbered themes → per-feature PROBLEM/UPDATE/WIIFY → demos → roadmap → Q&A. Quarterly design (DM Sans, #00e785, burst). | `quarterly-webinar` | ✅ Built |
| 2 | **Onboarding-deck feature slide** | Sales team aid inside the Wati for Marketing onboarding deck. 1 slide (2–3 for a flagship) per launched feature: value props, what it adds, positioning, and **what to pitch it against**. | Match the onboarding deck's feature-slide templates (T0–T6). Wati for Marketing design, exact. | `onboarding-deck` | ✅ Built |
| 3 | **Product / feature webinar** | External customers, deep dive into ONE product (e.g. Instagram webinar). Explain the product in depth. | Narrative product walkthrough — problem → product → how it works → use cases → proof → CTA. Deeper than a quarterly slide. | *(planned)* | 🔜 Need reference deck (e.g. Instagram webinar) |
| 4 | **Launch-enablement session deck** | Internal (Sales/CS/Support). Hands-on build-along for a launch. | Enablement/training arc — what's launching, how to build/use it, plan eligibility, objections/FAQs. | *(planned)* | 🔜 |

## Rules
- Build every deck by **templating the matching reference deck** — never from scratch.
- Pull content from the local `context/*.md` knowledge base (kept current by the weekly refresh); borrow extra from Granola, the launch project repos, or a WebSearched Wati support article when the KB is thin. Never fabricate — mark `[TBC]`.
- Match design to the reference deck's real design (see `context/design-system.md`, source of truth = `wati-brand-auditor`).
- Render + QA every slide before handing back.
