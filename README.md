# B&R Electrical — Emergency & Exit Lighting Audit (PWA)

This folder is a complete, ready-to-deploy Progressive Web App:

- `index.html` — the app itself
- `manifest.json` — makes it installable ("Add to Home screen" / "Install app")
- `sw.js` — service worker, caches the app so it works fully offline
- `icon-192.png`, `icon-512.png` — app icons

## To deploy with Claude Code

1. Unzip this folder somewhere on your computer.
2. Open a terminal in that folder (or open the folder in the Claude Code / Claude Desktop "Code" tab).
3. Paste this prompt to Claude Code:

   > I have a static PWA in this folder (index.html, manifest.json, sw.js, two icon
   > PNGs). Please deploy it to GitHub Pages (create a new repo if needed) so it
   > has a public HTTPS URL, then confirm the manifest and service worker are
   > being served correctly so it installs as a PWA on Android Chrome and iOS
   > Safari. Give me the final URL when done.

4. Once you have the URL, open it in Chrome on your phone — you should get a proper
   "Install app" prompt (not just a bookmark). After installing, it works fully
   offline and keeps your data between sessions.

## Notes

- Any static host works (GitHub Pages, Netlify, Vercel, Cloudflare Pages) — GitHub
  Pages is free and simple, which is why it's the default in the prompt above.
- All survey data and photos are stored in the browser's local storage on your
  device — nothing is uploaded anywhere. Keep using the same installed app icon
  (don't reinstall from scratch) to keep your data.
- If Claude Code asks whether to make the repo public or private — either works;
  public is simpler and free on GitHub Pages, private is fine too if your GitHub
  plan supports Pages on private repos.
