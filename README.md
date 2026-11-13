# explain-me-template

Starter for the weekly explain-me tradition.

Each week: pick one piece of tech you worked on but don't fully understand → create `explain-me-<topic>` from this template → learn it via a tiny demo.

## Starting a lesson

Send this as your first message in the new lesson repo:

`Explain me <topic>. Follow prompt.md in this repo.`

The agent reads `prompt.md` itself and fills `TOPIC.md` with you.

## Use this template

1. GitHub → `Use this template` → name it `explain-me-<topic>`
2. Fill `TOPIC.md` (short or long, as needed) — or leave it blank and the agent fills it with you
3. Fill tech-specific `AGENTS.md` under `## Per-topic overrides`
4. Start the lesson (see above)
5. Build the `src/` demo (one concept, one primary run command, deps with versions + why)
6. Fill `README.md` explanation sections below
7. Append `SESSION.md` per round, copy `LOG-ENTRY.md` row into your central log

## Explanation format (fill per-topic)

### What
One paragraph: what is this tech?

### Why
Why does it exist / what problem does it solve?

### How demo works
What the `src/` demo shows. Then: `sh` fence with run + verify commands, env line (runtime version, deps, `.env` or none), and build-output (servable) or no-build (CLI) statement.

### Gotchas
Answer the confusions in `TOPIC.md` explicitly, as dash bullets with `file:line` refs. Edge cases, common mistakes.

### Sources
In order: (1) `src/<demo>` (this repo — the thing being explained), (2) origin link from `TOPIC.md`, (3) docs actually consulted.

### Template friction
What felt missing or awkward in this template while doing this lesson?

## Files

- `prompt.md` — universal first prompt (does not change per-topic)
- `TOPIC.md` — variable part: tech, delivery, origin link, mental model, confusions
- `AGENTS.md` — base instructions, plus tech-specific notes in each lesson
- `SESSION.md` — running session log, appended per round
- `LOG-ENTRY.md` — table row snippet for central log (the pointer; transcript stays in `SESSION.md`)
- `src/README.md` — demo rules

## Evolving this template

To make that easy:
- Keep this template minimal — don't add tech-specific stuff here
- When something feels missing in a lesson, note it in that lesson's README under `### Template friction`
- Every ~3 lessons, backport common fixes here
