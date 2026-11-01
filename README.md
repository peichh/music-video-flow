# Music Video Flow

A reusable Codex skill for planning, generating, editing, and checking story-led music videos, lyric videos, and scene montages.

## Install with the Skills CLI

Requires Node.js 22.20 or later (see the [Skills CLI](https://github.com/vercel-labs/skills)).

Install globally for Codex:

```bash
npx skills add peichh/music-video-flow --skill music-video-flow -g -a codex
```

Install in the current project instead (omit `-g`):

```bash
npx skills add peichh/music-video-flow --skill music-video-flow -a codex
```

The installer is the community-maintained [Vercel Skills CLI](https://github.com/vercel-labs/skills). It supports Codex and discovers the skill folder in this repository.

## Install manually

Copy the `music-video-flow` folder into `~/.codex/skills/` (or `$CODEX_HOME/skills/`) and restart/reload Codex.

## Requirements and limits

The skill contains workflow instructions and references; it does not bundle Meta AI, Chrome, browser permissions, image/video generation, music, or any account access. Those tools and permissions must be available separately in the user's environment. Read `music-video-flow/SKILL.md` before use.

## Contents

- `music-video-flow/SKILL.md` — main workflow and first-use requirements
- `music-video-flow/references/scene-planning.md` — treatments, shot design, prompts, continuity
- `music-video-flow/references/edit-and-export.md` — frame review, trimming, transitions, export checks
