# Copilot Handoff — PixelPop-Content

**What:** Public content repo that PixelPop displays download on their own: Night Night songs and Storybook narration/pictures, indexed by `manifest.txt`.
**Location:** `~/dev/PixelPop Project/PixelPop-Content` · **GitHub:** rauls4/PixelPop-Content (public)
**Branch / HEAD:** `main` @ `a6538e4` (2026-10-07, before this doc).

## How to update
Edit `data/` in the firmware repo (rauls4/PixelPop) and run `tools/build_content_repo.py`, or edit here and regenerate `manifest.txt` with that script. Only add material you have the right to redistribute; this repo is public. Storybook narration is synthetic (OpenAI TTS); say so wherever presented. Large files use `.gitattributes`.

## Layout
- `nightnight/` — `*.mp3` + `tracks.txt`
- `storybook/<story>/` — six `NN-name.mp3` + `images/closeups/NN.jpg`
- `manifest.txt` — what boards fetch

## Standing rules for AI agents
- Keep this doc current after every meaningful change: branch, HEAD sha, state, next steps. Then commit and push.
- Never commit secrets: `.env`, `.dev.vars`, keystores (`*.jks`, `*.keystore`, `keystore.properties`), `local.properties`, signing certs (`*.p12`), API keys, login sessions.
- Never force-push, rewrite pushed history, or delete branches without Raul's explicit OK.
- Don't commit build output (`build/`, `Build/`, `DerivedData/`, `.gradle/`, `node_modules/`).
- Write "unknown" rather than guessing.
