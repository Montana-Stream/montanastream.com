# Montana Stream

A wireframe / clip-art style landing page with mountains, pine trees, and an animated river.

## Project structure

```
montana-stream/
├── index.html          ← landing page with the scene + "Coming Soon!"
├── videos.html         ← /videos
├── affiliates.html     ← /affiliates
├── about.html          ← /about
├── css/
│   └── style.css
├── js/
│   └── include.js      ← injects header & footer on every page
└── partials/
    ├── header.html     ← global header (Videos / Affiliates / About)
    └── footer.html     ← global footer (© Montana Stream, 2026 + socials)
```

## How the global header / footer works

Every page contains just two empty placeholders:

```html
<div id="site-header"></div>
...
<div id="site-footer"></div>
<script src="js/include.js"></script>
```

`js/include.js` runs on page load, fetches `partials/header.html` and `partials/footer.html`, and injects them into those placeholders. To change the header or footer everywhere, edit the partial — the change applies to every page automatically.

## Deploying to GitHub Pages

1. Create a new GitHub repository (e.g. `montana-stream`).
2. Upload all the files in this folder to the repo root, keeping the folder structure intact.
3. In your repo, go to **Settings → Pages**.
4. Under **Source**, select the `main` branch and `/ (root)` folder, then click **Save**.
5. Your site will be live at `https://<your-username>.github.io/montana-stream/` within a minute or two.

> **Note:** the partials are loaded via `fetch()`, so the site **must** be served over HTTP(S). It will work on GitHub Pages, Netlify, Vercel, or any local web server (e.g. `python3 -m http.server`). It will **not** work if you double-click `index.html` to open it from your file system, because browsers block `fetch()` on `file://` URLs.

## Local preview

```bash
cd montana-stream
python3 -m http.server 8000
# then open http://localhost:8000
```

## Customization quick-reference

| What | Where |
|---|---|
| Add a nav tab | `partials/header.html` |
| Change copyright year | `partials/footer.html` |
| Swap social icon links | `partials/footer.html` (the `href="#"` attributes) |
| Change colors | `:root` block at the top of `css/style.css` |
| Adjust river speed | `dur="6s"` on the `riverFlow` pattern in `index.html` |
