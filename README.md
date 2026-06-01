# DEV_DOJO

A self-directed software-development curriculum driven by ChatGPT/Codex. The syllabus content under `src/data/roadmaps/` is taken **read-only** from [roadmap.sh](https://github.com/kamranahmedse/developer-roadmap); the tutor layer lives at the repo root. The upstream Astro website build has been stripped — this repo is purpose-built for tutor sessions, not for running the roadmap.sh site.

## What's in here

| File / dir | Role |
|---|---|
| [AGENTS.md](AGENTS.md) | Auto-loaded by Codex at session start. Tells the tutor how to orient, the lesson workflow, and the teaching style. |
| [progress.md](progress.md) | Single source of truth for what you've completed, in progress, and next. Updated by the tutor as you work. |
| [curriculum-index.md](curriculum-index.md) | The 13-phase full-stack map. Each topic links to its dedicated deep-dive roadmap under `src/data/roadmaps/`. |
| [lessons/](lessons/) | One folder per topic gets created here as you go. |

## Setup

1. **Open this repo:**
   ```bash
   cd /srv/jackson-server/repos/DEV_DOJO
   ```
2. **Open ChatGPT/Codex** in that folder. It will read `AGENTS.md` automatically.
3. **Say:** *"start HTML"* — or whichever topic you want to begin with. The tutor will create `lessons/01-html/` and walk you through it.

## How it works

When you start a topic, the tutor creates `lessons/<phase-N>-<topic>/` containing:

- `lesson.md` — teaching walkthrough (What / How / Why / Where / How-to-use)
- `example/` — hands-on code you build together
- `understanding-check.md` — questions you answer; gaps loop back to the lesson
- `quick-reference.md` — one-page cheatsheet for future lookback

After every topic transition, the tutor updates `progress.md`. So when you come back days later and open a fresh session, the tutor reads `progress.md`, greets you with *"You're on Phase X, topic Y. Ready to continue?"* and picks up where you left off.

## Ecosystem fit

DEV_DOJO is the learning workspace for software-development practice in the wider repo ecosystem. CONTROL_PLANE owns governance and routing. DEV_DOJO can reference `TECH_LIBRARY` for technical source material, `WORK_FACTORY` for bounded build patterns, and `DATA_STORE` as a pointer-only runtime asset concept when lessons need that context.

## Switching curricula

This fork is configured for the **full-stack** roadmap. To target a different roadmap (e.g. AI Engineer, DevOps, Frontend-only), edit `curriculum-index.md` to point at the corresponding directory under `src/data/roadmaps/<other-roadmap>/`. The 87 available roadmaps are listed in that source directory.

## Credit

Curriculum structure and source content from [roadmap.sh](https://roadmap.sh) ([github.com/kamranahmedse/developer-roadmap](https://github.com/kamranahmedse/developer-roadmap)), used under their license (see [license](license)). Tutor layer added in this fork.
