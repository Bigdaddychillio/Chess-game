# The Chess Room

A polished chess game built with React. Features multiple AI difficulty levels,
ELO ratings, achievements, post-game review, coordinate training, time controls,
drag-to-move, custom themes, and ambient music.

## Local development

```bash
npm install
npm run dev
```

Then open the URL printed in your terminal (usually http://localhost:5173).

## Build for production

```bash
npm run build
```

The deployable site is produced in the `dist/` folder. You can preview the
production build with:

```bash
npm run preview
```

## Deployment

### Vercel (recommended, free)

1. Push this folder to a GitHub repo.
2. Go to https://vercel.com and click "Import Project".
3. Select your repo. Vercel will auto-detect Vite and deploy it.
4. You get a live URL in about 60 seconds. Every git push auto-redeploys.

### Netlify (also free)

1. Push this folder to a GitHub repo.
2. Go to https://app.netlify.com, click "Add new site" → "Import from Git".
3. Select your repo. For build command use `npm run build`, and for publish
   directory use `dist`.
4. Click deploy. You get a live URL.

### GitHub Pages

1. Push this folder to a GitHub repo.
2. In the repo settings, enable GitHub Pages on the `gh-pages` branch.
3. Run `npm run build` locally, then push the `dist/` folder contents to the
   `gh-pages` branch.
4. Your site will be live at `https://<username>.github.io/<repo>`.

### Upload anywhere (any static host)

Run `npm run build`, then upload everything in `dist/` to any static host —
Cloudflare Pages, Firebase Hosting, S3+CloudFront, or even a plain file server.

## Project structure

- `src/chess.jsx` — the full game (engine, UI, audio, everything)
- `src/main.jsx` — React entry point
- `src/storage-shim.js` — localStorage shim providing the `window.storage` API
  the game uses for saving profiles, preferences, and stats
- `src/index.css` — Tailwind + body reset
- `index.html` — loads Google Fonts and mounts the React app

## Data storage

Profiles, game stats, rating, achievements, and preferences are all saved to
the browser's `localStorage` — they persist on the same device/browser but do
not sync across devices. Clearing your browser data will reset everything.
