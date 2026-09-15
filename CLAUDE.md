# CLAUDE.md

YuniqueS Ltd's public site: AI products (Amnis, Voxtiva) plus e-commerce advisory. Hand-written static HTML — no framework, no bundler, no package.json, no build step. Each page is self-contained (inline `<style>`/`<script>`, `:root` custom properties per file); the only external dependency is the Google Fonts CDN link in `<head>`.

`index.html` is the live homepage. `a.html`, `b.html`, `c.html` are the three original design candidates (Studio Seal / Showreel / Catalogue) from the first exploration commit; `index.html` was later merged from A's structure and B's media wall. They are not linked from the live nav — keep them only as historical reference, don't treat them as pages to update alongside `index.html`.

`sabon/` is a separate static microsite (a different venture) with its own `index.html`, `plan/`, `market/`, `findings/`, and `assets/` — unrelated to the root site's content.

Deployed via GitHub Pages, legacy build, source = `main` branch root (no Actions workflow — Pages rebuilds automatically on push to `main`). `CNAME` pins the custom domain to `yuniques.com`. There is no staging: a push to `main` is live.

Preview locally with `python3 -m http.server` from the repo root and open `localhost:8000/index.html` (asset paths are root-relative, so serve the directory rather than opening the file directly).

Assets live under `assets/` (or `sabon/assets/` for the sabon microsite): images as `.jpg`/`.png`, icons as `.svg`, and each `.mp4` has a matching `<name>-poster.jpg` used as its poster frame — keep that pairing when adding new video assets.
