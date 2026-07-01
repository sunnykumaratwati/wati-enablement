# Features in Focus — the curation doc (deck input)

Before a Wati Launch Day deck is built, the quarter's launches are curated into a **"Features in Focus"** doc. This is the bridge between raw launch data (Slack #product-updates-gtm + the `context/` knowledge base) and the deck. The deck is built FROM this doc.

Modeled on the real Q2 2026 doc ("Features in Focus for Q2 Webinar", Notion).

## What it is
A themed table of the quarter's features that **impact existing paying customers**, each with a plain "what it does for the customer" line, grouped into 3–5 themes with the biggest-impact theme leading.

## Curation rules (from the real Q2 doc)
- **Customer-webinar filter:** include only features that impact existing paying customers. **Exclude** trials, signups, packaging/pricing, and pure-marketing changes.
- **Astra leads the story** (or whatever the biggest-MRR / marquee theme is that quarter — see the theme-ordering rule in the pattern file).
- Group into themes, e.g. Q2 used: `🤖 Astra — what's new since launch` · `🚀 Smarter Campaigns` · `📣 Channels + Others` · `📊 Ads — Full-Funnel Analytics`.
- Each row: **Feature** | **What it does for the customer** (benefit-led, plain English, one or two sentences).
- Note webinar logistics at top: date, time, speakers, audience rule.

## Format
```
[Quarter] customer webinar — features released [window] that impact existing paying customers.
Webinar: [date · time · speakers]
Rule: Customer webinar. Excludes trials, signups, packaging, marketing. [Lead theme] leads the story.

| Feature | What it does for the customer |
|---------|-------------------------------|
| **THEME 1 HEADER** | |
| [feature] | [benefit line] |
| ... | |
| **THEME 2 HEADER** | |
| ... | |
```

## How the skill uses it
1. **Build or receive the doc.** If the user asks "what launched this quarter?", generate this doc from the `context/` knowledge base (Recently Shipped sections, dated) + Slack, applying the curation rules above. If the user already has a doc (like the Q2 Notion page), use it as the base.
2. **Reconcile before building the deck.** Cross-check the doc against the latest `context/` files and Slack #product-updates-gtm for anything launched since the doc was written or missing from it. Surface proposed additions to the user and confirm before building.
3. **Build the deck** from: this doc (what to include + themes) + `context/*.md` (depth: value props, positioning, proof, plan) + `context/design-system.md` (look) + the pattern file (structure).
