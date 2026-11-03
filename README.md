# SFIS Learning Lab – Vercel Demo

Static single-page website. No build step or backend required.

## Deploy with Vercel Dashboard (fastest)
1. Create a GitHub repository, e.g. `sfis-learning-lab-demo`.
2. Upload `index.html`, `vercel.json`, and this README to the repository root.
3. In Vercel, choose **Add New → Project** and import the repository.
4. Framework Preset: **Other**.
5. Build Command: leave empty.
6. Output Directory: `.` (or leave the default if Vercel detects the static root).
7. Click **Deploy**.
8. Open the generated `*.vercel.app` URL and test the navigation, SQL Playground, and Interview Assessment.

## Deploy with Vercel CLI
From this directory:

```bash
npm i -g vercel
vercel
```

Follow the prompts. For production deployment:

```bash
vercel --prod
```

## Demo notes
- The site is static. SQL Playground uses sql.js from a CDN, so the first load needs internet access.
- AI Engineering Coach calls the configured API gateway directly from the browser. The API key is entered by the user at runtime and kept in tab memory by the current app; it is not embedded in this package.
- The public demo URL exposes the frontend and all client-side logic. Anyone can inspect it. Do not enter a valuable/private API key or production/company data. API gateway CORS must allow the Vercel domain for browser calls to work.
- Local progress uses browser localStorage and is per-browser/device.
