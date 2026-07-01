# Wati Product Knowledge Base (Context)

This folder is the **stable product knowledge layer** for every enablement asset. It holds one MD file per Wati product category. Any deck agent reads from here so that *every* feature is presented accurately and on-message — even features the PMM building the deck didn't personally work on.

This is the "integrity layer": it ensures nothing falls short when you have to present the whole product.

---

## The Two-Layer Context Model

| Layer | What | Where | Updates |
|-------|------|-------|---------|
| **1. Product Knowledge Base** (this folder) | What each Wati product/feature is, what it does, positioning, plan eligibility | In this repo | When features graduate new → established |
| **2. Quarter Feed** | This quarter's specific releases (Notion doc + Slack product-updates + Granola) | **Local only** (never committed) | Fresh each quarter |

A deck agent combines both: the Knowledge Base to understand each feature deeply + the Quarter Feed to know what to include right now.

---

## Categories (one file each)

| File | Covers |
|------|--------|
| `ai-astra.md` | Astra AI Agents — autonomous agents, voice AI, agent builder, testing, cloning |
| `ai-copilot.md` | Copilot — agent-assist: suggestions, summaries, translations, CX score, template assistant |
| `ai-byoa.md` | Bring Your Own AI — model-agnostic, data sovereignty, enterprise |
| `channels.md` | WhatsApp, Instagram, Messenger, RCS, SMS, TikTok Ads, WhatsApp Calling |
| `campaigns-marketing.md` | Broadcasts, Campaign Calendar, Drip, Segments, CTWA ads, attribution |
| `sales-crm.md` | WhatsApp CRM, lead stages, contact owner routing, sales analytics |
| `team-inbox.md` | Unified inbox, routing, collaboration, mobile app |
| `automation-chatbots.md` | Chatbot builder, WhatsApp Flows, automations |
| `ecommerce-shopify.md` | Shopify integration, abandoned cart, multichannel fallback |
| `analytics-insights.md` | Dashboards, attribution, topic/operator insights |
| `integrations.md` | HubSpot, Salesforce, Zoho, CRMs, APIs & webhooks |
| `platform-plans.md` | Plan tiers (Growth/Pro/Business), Astra plans, Try Higher Plan, pricing |

Each file follows `_TEMPLATE.md`.

---

## What goes in each category file

- **What it is** — the product/feature at a marketing level
- **Sub-features** — the individual capabilities under it
- **Positioning one-liners** — how Wati talks about it (borrowed from decks/enablement/website)
- **Plan eligibility** — which plans it's on
- **Proof points** — stats, outcomes, customer stories (only real ones)
- **Deeper material pointers** — where the source material lives (deck, enablement session, Granola note, Notion page)

---

## How this stays fresh (update mechanism)

Wati posts every release to the **#product-updates GTM channel** in Slack, and features are documented in Notion. The plan:

1. **Weekly refresh routine** reads the #product-updates channel + relevant Notion pages
2. Routes each new release to the right category file (by keyword: "Astra" → `ai-astra.md`, "Instagram" → `channels.md`, etc.)
3. Appends the new feature under a `## Recently Shipped` section in that file, timestamped
4. Flags anything that needs the PMM's positioning judgment

Until the routine is wired, update manually: when a feature ships, add it to the right category file.

---

## Safety

This folder holds **stable, mostly public-facing product knowledge** (what's on wati.io and in customer decks) — safe for the public repo. **Unreleased / roadmap / internal-only** detail must NOT go here — it belongs in the local Quarter Feed (gitignored). When in doubt, keep it local.
