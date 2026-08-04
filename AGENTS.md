# AGENTS.md

## Cursor Cloud specific instructions

This repository is a **static GitHub Pages portfolio** with no package manager, build step, or backend. All application code lives in `index.html` (inline CSS/JS) plus `cv.pdf`.

### Running locally

From the repo root:

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000. Any static file server works (`npx serve .` if Node is available).

### Lint / test / build

There is no configured linter, test runner, or build pipeline. Validation is manual: serve the site and verify in a browser.

### Services

| Service | Required | Notes |
|---------|----------|-------|
| Static HTTP server | Yes | Serves `index.html` and `cv.pdf` |
| Google Fonts CDN | No | Loaded from `fonts.googleapis.com`; site falls back to system fonts offline |

### Hello-world verification

1. Start the HTTP server (see above).
2. Load http://localhost:8000 — hero section and terminal animation should appear.
3. Press `Ctrl+K` (or `Cmd+K`) to open the command palette.
4. Use nav links or the palette to jump to sections (e.g. `#experience`).
5. Download or open `./cv.pdf` from the nav or command palette.

### Gotchas

- **No hot reload**: edit `index.html` and refresh the browser manually.
- **Port 8000**: if occupied, use another port (e.g. `python3 -m http.server 8080`).
- **Production deploy**: GitHub Pages serves the repo root; no build step required.
