---
name: refresh-context
description: Weekly refresh of the Wati Product Knowledge Base. Reads (read-only) the Slack #product-updates-gtm channel, relevant Notion docs, and Granola meeting notes, then updates the local category MD files in context/. Use when someone says "refresh the context", "run the weekly refresh", "update the knowledge base", or it's fired on the Monday schedule.
---

# Refresh Context — Weekly Knowledge Base Update

You keep the Product Knowledge Base (`context/*.md`) current so enablement assets are built from fresh, real data — never hallucinated. Run this every Monday. End result: all 12 category files updated and re-dated.

## Absolute rules
- **READ-ONLY on all sources.** Never post, reply, react, comment, edit, or create anything in Slack, Notion, or Granola. You only read them.
- **Only write to local MD files** in `context/`. Never commit them (they're gitignored — that's intentional).
- **Never fabricate.** If a value prop or stat isn't in the source, mark `[STAT — TBC]` or leave it. Dates must be the real dates as posted.

## The 12 categories (process one at a time, in order)
ai-astra · ai-copilot · ai-byoa · channels · campaigns-marketing · sales-crm · team-inbox · automation-chatbots · ecommerce-shopify · analytics-insights · integrations · platform-plans

## Per-category procedure
For each category file, read its current `_Last updated_` date, then:

1. **Slack** — Search `#product-updates-gtm` (channel `C0987T0JECA`) for updates since the last-updated date, matching this category's keywords (e.g. ai-astra → "Astra", "voice agent", "AI agent"; channels → "Instagram", "RCS", "SMS", "TikTok", "WhatsApp Calling", "WebChat"). Load the Slack tools via ToolSearch. For each new launch capture: feature name, **exact launch date**, what it does, value/what's-in-it-for-the-user, plan.

2. **Notion** — Search for this category's feature launch docs / positioning pages updated since the last date (notion-search + notion-fetch). Pull positioning rationale, value props, ICP/cohorts, use cases, proof/data points, objections/FAQs.

3. **Granola** — Search meeting memory for recent sessions relevant to this category (enablement sessions, launch reviews). Pull anything that sharpens positioning, use cases, or objections. Load Granola tools via ToolSearch.

4. **Update the MD file** — merge new info into the right sections (follow `context/_TEMPLATE.md` structure): add new rows to Sub-Features, new dated items to Recently Shipped (newest first, no duplicates), enrich Value/ICP/Use Cases/Proof/Objections/Messaging Angles. Update the `_Last updated_` date and source line. Don't delete good existing content — only add/correct.

## After all 12
- Summarize what changed per category (one line each) for the user.
- Flag anything that needs the PMM's judgment (ambiguous positioning, unverified stats, features that don't fit a category).
- Do NOT git commit — the files stay local by design.

## Notes
- Interactively-authenticated connectors (Slack/Notion/Granola) must be live when this runs. If a source is unreachable, note it and continue with the others; don't block the whole refresh.
- Keep everything a deck/email/brief would need inside these files — the goal is that no asset-building ever has to go re-hunting the sources.
