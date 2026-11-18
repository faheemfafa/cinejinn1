# OpenFlix on GitHub Pages

The OpenFlix app, hosted on GitHub Pages. It talks to your OpenFlix Apps Script (the Google Sheet with the
Sources, Index and Covers tabs), so everything stays shared with the family. Nothing personal is stored in this repo:
each device enters the web app link and family code once.

## One-time setup
1. **Apps Script**: paste the latest `Code.gs` into your sheet's script, then **Deploy → Manage deployments →
   Edit → New version** (Execute as **Me**, Who has access **Anyone**).
2. **Family code**: reload the spreadsheet, then **OpenFlix menu → Set family code** (8+ characters).
3. **GitHub**: create a **public** repository (e.g. `openflix`), upload these files
   (`index.html`, `manifest.webmanifest`, the three `.png` icons, this README) → **Commit**.
4. **Settings → Pages** → Source: **Deploy from a branch** → Branch **main**, folder **/ (root)** → **Save**.
   After a minute your app is at `https://<your-username>.github.io/openflix/`.
5. Open it, paste the Apps Script link (ends in **/exec**) and the family code → **Connect**.

## Install it like an app
- **iPhone/iPad (Safari)**: Share → **Add to Home Screen**. No Xcode, no 7-day limit.
- **Android (Chrome)**: ⋮ → **Install app** / **Add to Home screen**.
- **Mac/Windows (Chrome/Edge)**: the install icon in the address bar.

## Notes
- Watch history and My List are per device (as before); sources, index and covers come from the sheet.
- http:// videos still can't play inside the page (it's https). Use **Open with…**.
- Changing the family code signs every device out; use **Sources → Sign out of this device** to reconnect.
- After updating the Apps Script `Index.html`, run `python3 make-pages.py` to rebuild `index.html` here.
