# Universal first prompt

Agent instructions for explain-me lessons. The user starts the lesson with the first message documented in `README.md`. All variable context lives in `TOPIC.md`. Tech-specific agent instructions live in `AGENTS.md`.

---

Step 0 — resolve placeholders before explaining. If `TOPIC.md` is still blank template, take the topic from the user's message as the seed, ask targeted questions to fill Tech / Delivery / Origin / mental model / confusions, write `TOPIC.md`, then proceed. If any template comments (`<!-- ... -->`) are still present after that, stop and ask rather than guessing the tech.

Then read `TOPIC.md` and `AGENTS.md` in this repo.

Explain the topic in `TOPIC.md` for a competent engineer who is new to this language/stack. Assume general fluency (no hand-holding on basics); explain every stack-specific idiom, jargon term, and piece of implicit context on first use, with a familiar analogue where one exists.

Pick the elaboration formats that fit this tech best (don't force all of them):
- overall explanation
- usage examples
- code walkthrough
- interactive examples and graphs

Plus always: gotchas / edge cases — answer the confusions in `TOPIC.md` explicitly.

Then:
1. Build a minimal demo in `src/` following `src/README.md` (one concept, one primary run command, minimal deps with versions + why each is needed, env requirements recorded), plus the `Delivery` vehicle from `TOPIC.md` (default: static site).
2. Fill `README.md` sections following the conformance rules in `AGENTS.md`: What / Why / How demo works / Gotchas / Sources (+ Template friction).
3. Fill tech-specific notes in `AGENTS.md` under `## Per-topic overrides`.
4. Append the session to `SESSION.md` (one entry per prompt/response round).
5. Propose a 2-3 line human summary for `LOG-ENTRY.md`.
6. End by asking how the template can improve, and write it in `README.md` under `### Template friction`.

Keep explanations concrete and tied to the demo. Generated artifacts must be reproducible (generating script committed + documented, true source marked). Verify by execution before calling it done: build, serve + curl, typecheck — on a clean checkout, not just the dev server.
