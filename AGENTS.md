# AGENTS.md

Base instructions for explain-me repos. See `README.md` and `src/README.md` for workflow.

Template itself has no run command. Each lesson must define one primary run command for its `src/` demo and document it in `README.md` under `How demo works` and in `src/README.md` under `## Run`.

Env vars: if a lesson introduces any, commit `.env.example` with a working placeholder and never commit `.env`; record the unset fallback and where production values live.

Decide small things in conversation; switch to formal planning only when the build shape changes (e.g. static → bundled → deploy).

Append `SESSION.md` per prompt/response round. Keep the one-row `LOG-ENTRY.md` summary separate — transcript and pointer stay separate.

Verify by execution before calling it done: build, serve + curl, typecheck — on a clean checkout, not just the dev server.

## README conformance (every lesson)

- Title: `# explain-me-<topic>` + 1-line topic description. Web lessons add `**Live demo:** <url>` under the title; CLI lessons omit it.
- Elaboration formats (pick fit, don't force all): overall explanation, usage examples, code walkthrough, interactive examples and graphs — plus mandatory gotchas.
- `How demo works`: `sh` fence with run + verify commands, env line (runtime version, deps, `.env` or none), build-output (servable) or no-build (CLI) statement.
- `Gotchas`: dash bullets with `file:line` refs answering the `TOPIC.md` confusions explicitly.
- `Sources` order: (1) `src/<demo>` (this repo), (2) origin link, (3) docs consulted.
- Audience: technical outsider. Never explain general programming; always explain stack-local context.

## Per-topic overrides

<!-- Fill per-lesson with stack-specific commands and explanation method. Example:
- Run: `npm run dev` (primary), `npm run build` + `npm run preview`, `npm run typecheck`
- Deps: `vite@7` (dev server + build), `tailwindcss@4` (demo styling) — why each is needed
- Env: `.env` location + required vars (e.g. `VITE_SITE_URL`), unset fallback, where production values live
- Delivery: static site (default) / interactive / cli — why this vehicle fits the concept
- Method for this tech: overall / usage examples / code walkthrough / interactive + graphs / gotchas
- Gitignore: append the lines your stack needs (e.g. Node: `node_modules/ dist/` / Python: `__pycache__/ .venv/`)
-->
