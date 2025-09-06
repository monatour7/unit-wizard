# Unit Wizard — GH Pages

A blazing‑fast, privacy‑friendly **Unit & Currency Converter** that runs entirely in the browser. Ships as a single static page, perfect for **GitHub Pages**.

- ✅ No backend, no secrets
- ✅ Works offline (all unit converters)
- 🔁 Currency rates via public API (manual refresh for free users; auto for Pro)
- 🔒 Simple **Pro** unlock (client‑side) to enable batch convert & extended history

## Demo License (for testing)
```
UNIT-WIZARD-PRO-DEMO-2025
```

## Deploy to GitHub Pages
1. Create a new GitHub repo (public or private).
2. Download the release ZIP from your ChatGPT session and unzip.
3. Commit & push all files to the repo root.
4. In **Settings → Pages**, set:
   - **Source**: `Deploy from a branch`
   - **Branch**: `main` (or `master`), folder `/ (root)`
5. Save. Your site will be live at `https://<your-username>.github.io/<repo>/`.

> GH Pages tip: We include a `.nojekyll` file to ensure assets aren't altered by Jekyll.

## Customize Payment Link
Open `index.html` and search for `buyBtn`. Replace the placeholder Stripe link with your **Gumroad/LemonSqueezy/Stripe** payment link. After purchase, you can deliver the license key manually or add a serverless verification later.

## How Pro Unlock Works (client‑side)
- The "Unlock" button stores a boolean in `localStorage` when a valid key/email is provided.
- For demo: any string containing `@` (email‑like) or the exact demo key unlocks.
- For production: replace the check with your own logic or call a public serverless endpoint.

## PWA (Installable)
We ship a `manifest.webmanifest` and basic icons so users can "install" it like an app. For full offline caching of assets/data, you can add a Service Worker later.

## Dev Notes
- Styling: Tailwind via CDN (no build step).
- Currency API: `https://open.er-api.com/v6/latest/<BASE>` (no key). Data is cached in `localStorage`.
- No analytics/tracking.

## License
MIT © 2025 Mohammed Natour
