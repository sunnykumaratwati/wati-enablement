# wati-enablement

Internal skills repository for Wati's GTM and CSA enablement team.

Use this repo to create enablement assets — decks, solution briefs, one-pagers — for any Wati feature launch or customer session.

## Quick Start

1. Copy `projects/_template/` → rename to your project (e.g. `projects/whatsapp-calling/`)
2. Fill in `brief.md` with topic, audience, session format, and key outcome
3. Add `positioning.md` — paste Notion link or key messaging
4. Drop Figma screenshots into `screenshots/`
5. In Claude Code, say: **"create an enablement asset"**

## Available Assets

| Asset | Status |
|-------|--------|
| Enablement Deck (.pptx) | ✅ Ready |
| Solution Brief | 🔜 Coming soon |
| One-Pager | 🔜 Coming soon |

## How It Works

The `/enablement` skill acts as a router. It reads your project brief, asks what you want to create, and hands off to the right agent. That agent checks what context it has and asks for anything missing before building.

## Adding to Claude Code

To use this repo as a skill source in Claude Code, add it as a plugin:

```
/plugin add sunnykumaratwati/wati-enablement
```
