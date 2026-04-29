# Digital Recruiter Content Engine

A Claude Cowork plugin that turns a recruiter or agency owner's real expertise — interviews, sales calls, voice memos, notes — into LinkedIn content that sounds like the operator, not AI.

## What it does

After a one-time onboarding, the plugin gives operators four modes:

- **Interview Mode** — Claude interviews the operator for 15-20 minutes to extract stories worth posting about.
- **Prep Mode** — Claude gives the operator 5-6 prompts to think about between interviews.
- **Creation Mode** — Operator pastes a transcript, Claude returns 16 LinkedIn posts following the Digital Recruiter SOP.
- **Newsletter Mode** — Operator pastes a transcript, Claude returns an 800+ word newsletter plus a LinkedIn promo post.

Creation Mode has three sub-modes for different operator workflows:

- **Standard** (default, ~12 approval gates, full visibility into every sub-phase)
- **Express** (~8 gates, sub-phases bundle, for trained operators with clean source)
- **Cowork** (2 gates default, async-friendly, for operators who want to step away from the screen during a run)

## What's inside

```
digital-recruiter-content-engine/
├── .claude-plugin/plugin.json
├── skills/content-engine/
│   ├── SKILL.md                        — system prompt, welcome, routing
│   └── references/
│       ├── Onboarding_SOP.md           — 5-phase onboarding (run once)
│       ├── Content_Creation_SOP.md     — the 16-post engine
│       ├── Interview_Mode_SOP.md       — conversational interview + Prep
│       ├── Newsletter_Mode_SOP.md      — long-form newsletter + LinkedIn promo
│       ├── Cowork_Mode_SOP.md          — autonomous async run with 2 checkpoints
│       ├── Memory_Log_Template.md      — cross-session memory format
│       └── Operating_Guide.md          — operator-facing reference
├── CONNECTORS.md
└── README.md
```

## How to install

In Claude Cowork, install this plugin once. Every new chat in Cowork will have the system prompt, SOPs, and routing logic loaded automatically. No per-chat upload step.

## How to use

Open a new chat. Say "Hi" or "Let's get started." On first run the plugin walks the operator through onboarding (5-10 minutes) and locks an ICP. After that, the operator picks a mode by name:

- "Start an interview"
- "Prep me"
- "Create content" + paste source
- "Create a newsletter" + paste source
- "Run in Cowork Mode" (in the Cowork desktop environment, for async runs)

At the end of every session, the plugin generates an updated `Client_Memory_Log.md` artifact. The operator downloads it and uploads it at the start of the next session — that's how the engine remembers prior posts and avoids repeating themes.

For the full operator-facing walkthrough, see `skills/content-engine/references/Operating_Guide.md`.

## Connectors

This plugin is instruction- and knowledge-only. It does not call any external services. One generic tool reference (`~~LinkedIn outreach tool`) appears in the closing Strategy Reminder; see `CONNECTORS.md` for the operator's options.

## Author

Mady Willcox

## Version

0.1.0
