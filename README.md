# HA Light Console — Captain's Console

Bridge Command-style phone console for Home Assistant lights.

**Live (HA local, recommended):** `http://192.168.0.208:8123/local/captains_console.html`  
**Mirror (GitHub Pages):** `https://ejones35.github.io/HA-Light-Console/` — source mirror, see note below

### What it does
- Light picker: 5× Nanoleaf NL67 (Gryffindor / Hufflepuff / Study / Front Living / Back Living) + ALL
- **Red Alert** — pulsing red (255↔55, 1.1s)
- **Yellow Alert** — pulsing amber (255↔70, 1.1s) — updated 17 Sep
- **Clear Alert** — warm white 4000K 100%
- Lights Off + Test Flash
- Dark LCARS-ish BC styling, haptics, PWA-capable

### Setup (phone, same WiFi as HA)
1. Open the HA local URL above on your phone.
2. Scroll to **Connection** → paste a Home Assistant Long-Lived Access Token (HA → Profile → Long-Lived Access Tokens → Create) → **SAVE**.
3. Badge → **ONLINE**, pick lights, hit Red/Yellow/Clear.

Token stays in `localStorage` on that device only.

### GitHub Pages note
GitHub Pages serves over **https**, HA is **http** (`192.168.0.208:8123`). Browsers block mixed-content `https → http` fetches, so the GitHub Pages mirror will show the UI but **can't reach HA** until HA is exposed via https (e.g. Nabu Casa, reverse proxy, or HA with TLS). Use the **HA local URL** for actual control — the GitHub repo is the source/backup.

### Files
- `index.html` — single-file console (also deployed as `captains_console.html` in HA `config/www/`)

Built by Jarvis for Ethan, Sep 2026. For Ethan's phone — not Mike M.
