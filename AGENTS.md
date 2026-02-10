# Repository Guidelines

## Project Structure & Module Organization
- `DCA-Planner.html` is the whole application (HTML structure, CSS theme system, and JavaScript calculation/export logic).
- `README.md` contains the short project description.
- There is no separate `src/`, `tests/`, or build pipeline yet. Keep related logic grouped by section in `DCA-Planner.html` (styles first, then markup, then scripts).
- If you add major features, prefer extracting code into clear folders such as `src/js/`, `src/css/`, and `tests/` while keeping `DCA-Planner.html` as the entry page.

## Build, Test, and Development Commands
- `python3 -m http.server 8000` - run a local static server from the repo root.
- Open `http://localhost:8000/DCA-Planner.html` - load the app for development and manual QA.
- `git status` - confirm only intended files changed before committing.

## Coding Style & Naming Conventions
- Use 2-space indentation across HTML, CSS, and JavaScript.
- JavaScript naming: `camelCase` for functions/variables (for example, `calculateAndRender`), `UPPER_SNAKE_CASE` for constants (for example, `TRADING_DAYS_PER_YEAR`).
- Keep user-facing copy consistent with existing Chinese labels unless a task explicitly requires localization changes.
- Reuse CSS custom properties (`--primary`, `--text-main`, etc.) and theme blocks (`[data-theme="light"]`, `[data-theme="dark"]`) instead of hardcoding colors in new rules.

## Testing Guidelines
- No automated test framework is configured; use manual regression checks for each change.
- Validate: positive/invalid amount input, calculation rendering, TXT download, theme toggle behavior, and mobile layout at `max-width: 640px`.
- For finance logic changes, verify sample outputs for 5/10/30-year rows and ensure units remain in `万元`.

## Commit & Pull Request Guidelines
- Keep commit subjects short, imperative, and capitalized (matching history style like `Initial commit`).
- Suggested pattern: `Verb concise change` (example: `Adjust plan card animation delay`).
- PRs should include: purpose, key UI/logic changes, manual test steps performed, and screenshots/GIFs for visual updates.

## Agent-Specific Instructions
- Unless explicitly instructed otherwise, always respond in Simplified Chinese (`简体中文`).
