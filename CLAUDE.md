# CLAUDE.md

## Project
Static single-file HTML pages, no build step, no package manager.

- `workhours.html` — «Рабочие часы»: work-hours tracker, state in `localStorage`.
- `gta-gas-dashboard-live.html` — GTA gas prices dashboard (Chart.js 4.4.1 from cdnjs).
- `install-guide.html` / `install-guide-ru.html` — install guide for Work Hours (EN / RU). Keep both in sync.

Run: open the file in a browser. No tests, no lint.

## Working rules
1. **Think before coding.** If a request is ambiguous, ask instead of guessing. State assumptions explicitly.
2. **Simplicity first.** Minimum code that solves the task. No new libraries, abstractions or features nobody asked for.
3. **Surgical changes.** Touch only what the task needs. Don't reformat, rename or "improve" unrelated code.
4. **Verify.** Before reporting done, check the page loads without console errors and the changed feature works.

## Style
- 2-space indentation, `const` over `let`.
- Keep each page self-contained (inline CSS/JS); external scripts only from a pinned CDN version.
- Don't break existing `localStorage` keys in `workhours.html` — users' saved data depends on them.
