# src demo rules

- One concept only. If you need two concepts, make two repos.
- One primary run command (e.g. `npm run dev`, `python -m http.server`, `cargo run`). Secondary commands (build/preview/typecheck) are fine but one must be primary and servable. One serving story per lesson, not two.
- Prefer small, dependency-free tech. If dependencies exist, list them with versions and why each is needed. Record the exact run command and any env requirements (runtime, `.env` location and required vars).
- Demo must directly illustrate the confusion in `TOPIC.md`.
- Interactive webpages must be well-styled: Tailwind (or equivalent), syntax highlighting for all code blocks, light/dark toggle defaulting to system. Styling serves the concept — keep the demo itself visually quiet.
- Delivery vehicles: `static site` (default) is a styled write-up page following the webpage rules above; `interactive` adds try-it elements bound to the concept (sliders, toggles, live inputs); `cli` ships a command transcript + captured output instead of a page.
- Generated artifacts must be reproducible: if the demo embeds generated output (e.g. highlighted code), the generating script is committed and documented, with the true source clearly marked.
- Verify by execution before calling it done — on a clean checkout, not just the dev server. Pick your runtime's line as primary and record it in `## Run`: node (`npm run build` + serve/`preview` + `curl`, `tsc`), python (`python -m http.server` + `curl`, `compileall`), php (`php -l` + `php src/demo.php`), static (`npx serve` + `curl`).
- Document the run command in the per-lesson `README.md` under `How demo works`, and append a `## Run` section here with the exact commands + env setup.
- Credit the lineage: every lesson notes where it came from — the lesson repo and the template repo (`https://github.com/juaniquillo/explain-me-template`). A small footer works for webpages; a closing line in CLI output or a Sources link works for anything else. Quiet, same style as the output.
