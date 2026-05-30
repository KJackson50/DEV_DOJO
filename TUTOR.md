# Full-Stack Tutor (this fork)

This is a fork of [roadmap.sh](https://github.com/kamranahmedse/developer-roadmap) configured to be driven by an LLM tutor (Claude Code, Cursor, etc.). The upstream roadmap content under `src/data/roadmaps/` is used **read-only** as the syllabus; the tutor layer lives at the repo root.

## What's added on top of upstream

| File / dir | Role |
|---|---|
| [CLAUDE.md](CLAUDE.md) | Auto-loaded by Claude Code at session start. Tells the tutor how to orient, the lesson workflow, and the teaching style. |
| [progress.md](progress.md) | Single source of truth for what you've completed, in progress, and next. Updated by the tutor as you work. |
| [curriculum-index.md](curriculum-index.md) | The 13-phase full-stack map. Each topic links to its dedicated deep-dive roadmap under `src/data/roadmaps/`. |
| [lessons/](lessons/) | One folder per topic gets created here as you go. |

## Setup

1. **Clone this fork:**
   ```bash
   git clone https://github.com/donroy26/developer-roadmap.git
   cd developer-roadmap
   ```
2. **Open Claude Code** (or your LLM tool of choice) in that folder. It will read `CLAUDE.md` automatically.
3. **Say:** *"start HTML"* — or whichever topic you want to begin with. The tutor will create `lessons/01-html/` and walk you through it.

## How it works

When you start a topic, the tutor creates `lessons/<phase-N>-<topic>/` containing:

- `lesson.md` — teaching walkthrough (What / How / Why / Where / How-to-use)
- `example/` — hands-on code you build together
- `understanding-check.md` — questions you answer; gaps loop back to the lesson
- `quick-reference.md` — one-page cheatsheet for future lookback

After every topic transition, the tutor updates `progress.md`. So when you come back days later and open a fresh session, the tutor reads `progress.md`, greets you with *"You're on Phase X, topic Y. Ready to continue?"* and picks up where you left off.

## Using with other LLMs

`CLAUDE.md` is named for Claude Code, but the file itself is plain markdown. For other tools (Cursor, ChatGPT, Gemini, etc.), either:
- Rename it to whatever your tool auto-loads (e.g. `.cursorrules`), or
- Paste its contents into the system prompt / project instructions of your tool.

## Switching curricula

This fork is configured for the **full-stack** roadmap. To target a different roadmap (e.g. AI Engineer, DevOps, Frontend-only), edit `curriculum-index.md` to point at the corresponding directory under `src/data/roadmaps/<other-roadmap>/`. The 87 available roadmaps are listed in that source directory.

## Credit

Curriculum structure and source content from [roadmap.sh](https://roadmap.sh) ([github.com/kamranahmedse/developer-roadmap](https://github.com/kamranahmedse/developer-roadmap)). Tutor layer added in this fork. Original upstream README is at [readme.md](readme.md).
