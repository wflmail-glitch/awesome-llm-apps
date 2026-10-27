# 🎬 Lemo-Opuscar

Direct and produce a short film made entirely in code: canvas and WebGL pages rendered frame by frame, original scores and text-to-speech narration. No video generation, no stock footage. Pick one of 59 library styles (Ukiyo-e, Watercolor Brush, Satellite Briefing, Exploded Teardown, 1920s Newsreel, ...) or make your own.

Ported from [lemomo-ai/lemo-opuscar](https://github.com/lemomo-ai/lemo-opuscar) (upstream commit `413a6bd`) by Lemomo / LemoLab. [▶ Watch the gallery](https://lemomo-ai.github.io/lemo-opuscar/).

## How it works

This skill is a thin bootstrapper. On first use `scripts/setup.sh` downloads the style library (guides, render tools and every `STYLE.md`) as a sparse clone into `~/lemo-opuscar`, and the agent then follows the library's `AGENTS.md`, `DIRECTOR.md` and `TECHNIQUE.md`. Each film's project goes in the folder you started from.

```
lemo-opuscar/
├── SKILL.md          # Instructions for the agent
├── scripts/setup.sh  # Fetches/updates the library, installs packages, adds demo sources
└── LICENSE           # Upstream MIT licence
```

## Requirements

- Node 20+, ffmpeg and Python 3.11+ (or [uv](https://docs.astral.sh/uv/)); the agent installs the rest
- `git` and network access to github.com
- A film takes an agent about 30–60 minutes and a fair amount of tokens
- The styles are tuned for Claude Opus 5.5; other models may not reproduce them well

## Usage

Copy this folder into your agent's skills folder (for Claude Code: `~/.claude/skills/lemo-opuscar/`), or install the upstream plugin directly:

```sh
claude plugin marketplace add lemomo-ai/lemo-opuscar
claude plugin install lemo-opuscar@lemolab
```

Then ask, for example:

> Make a 45-second film in the **watercolor** style about the coffee farm my family runs. Warm female narrator.

Set `LEMO_OPUSCAR_HOME` to keep the library somewhere other than `~/lemo-opuscar`.

## Licence

Code and docs: MIT (see [LICENSE](LICENSE)). The upstream demo films and stills are CC BY 4.0; films you make with the library are yours. See the [upstream licence notes](https://github.com/lemomo-ai/lemo-opuscar#licence).
