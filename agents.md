# Agents Guide (Quisharoo/colmquish)

This is my personal website. Use this guide to add features while keeping the same stack, look, and patterns.

## Architecture Overview
- Static site: `index.html` + `assets/css/styles.css` + a few small content files.
- Local preview: `npm run serve` (Python SimpleHTTPServer on http://localhost:8000).

## Languages & Tools
- HTML, CSS, vanilla JavaScript (no framework/build step).
- Node.js for the post generator; Python for local serving.
- No external backend or database.

## Design System & UI Patterns
- Typography: Google Fonts Inter (300/400/600).
- Layout: terminal-style top bar and command shortcuts.
- Icons: Lucide inline SVGs; keep size ~24px in header buttons.
- Colors: CSS custom properties in `assets/css/styles.css`; supports light/dark mode via `body.dark-mode`.
- Components: badges, file headers, diff blocks; keep spacing and sizes consistent.
- Keyboard: `i`/`t`/`b` for tab nav; `Cmd/Ctrl+K` to toggle command palette.

## Security Considerations
- External links should use `target="_blank" rel="noopener"` (already applied where rendered).
- No secrets/keys in repo; commit info uses public GitHub APIs client-side.

## Git Workflow
- Branch from `main`; small, focused PRs.
- Fast-forward merges only; open a PR for all changes.
- Commit style: `feat:`, `fix:`, `docs:` etc.; write clear messages.
- Before opening PR: preview locally, test dark mode + mobile, verify keyboard shortcuts still work.

## Coding Conventions
- Keep it simple (HTML/CSS/vanilla JS). Avoid adding frameworks or build tooling.
- Reuse existing CSS tokens and classes; match spacing, sizes, and icon style.
- Put images in `assets/images/`; follow `assets/images/README.md` for required icons (`favicon.png`, `apple-touch-icon.png`, `card.jpg`).
- Keep Markdown concise; prefer lists; maintain consistent tone.

## Common Tasks
- Local preview: `npm run serve` and visit http://localhost:8000.
- Styling tweaks: edit `assets/css/styles.css`; ensure dark mode parity.

## Minimal Directory Map
- `index.html` — app shell and terminal UI.
- `assets/css/styles.css` — design tokens + components + dark mode.
- `assets/images/` — icons/OG images (see README in folder).
- `README.md` — short bio.

## PR Checklist (for agents)
- [ ] Matches existing design (typography, spacing, icons)
- [ ] Light/dark mode verified
- [ ] Keyboard shortcuts unaffected
- [ ] Mobile layout OK
- [ ] No unsafe HTML/scripts in Markdown
- [ ] No new build/deps introduced without approval
