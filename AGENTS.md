# AGENTS.md

## Repository: wati-enablement

Internal skills repo for Wati's GTM and enablement team. Each skill in this repo helps create a specific type of enablement asset — decks, solution briefs, one-pagers, and more.

## Repository Structure

```
wati-enablement/
├── .agents/
│   └── wati-brand.md          # Wati brand context, narrative, messaging — auto-injected
├── skills/
│   └── enablement/
│       ├── SKILL.md            # Router — entry point for all enablement requests
│       └── agents/
│           ├── deck/
│           │   ├── SKILL.md    # CSA enablement deck agent
│           │   └── references/ # Slide frameworks, templates
│           └── solution-brief/
│               └── SKILL.md    # Coming soon
└── projects/
    └── _template/              # Copy this for each new project
        ├── brief.md            # Topic, audience, key messages
        ├── positioning.md      # Notion link or pasted positioning content
        └── screenshots/        # Drop Figma exports here
```

## How to Use

1. Copy `projects/_template/` and rename it to your project (e.g. `projects/whatsapp-calling/`)
2. Fill in `brief.md` and `positioning.md`
3. Drop Figma screenshots into `screenshots/`
4. Invoke the enablement skill: say **"create an enablement asset"** or **"/enablement"**
5. The router will ask what you want to create and guide you from there

## Available Agents

| Agent | Status | What it creates |
|-------|--------|-----------------|
| `deck` | ✅ Active | CSA enablement / adoption deck (.pptx) |
| `solution-brief` | 🔜 Coming soon | 1–2 page solution brief (.docx) |
| `one-pager` | 🔜 Coming soon | Single-page leave-behind (.pptx / .pdf) |

## Naming Conventions

- Project folders: `projects/kebab-case-name/`
- Screenshots: `feature-name-01.png`, `feature-name-02.png`
- Brief files: always named `brief.md` and `positioning.md`
