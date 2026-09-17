# HA Light Console — Captain's Console

Bridge Command-style phone console for Home Assistant lights.

**Live (HA local, now https):** `https://192.168.0.208:8123/local/captains_console.html` — self-signed cert (accept once)  
**Mirror (GitHub Pages):** `https://ejones35.github.io/HA-Light-Console/` — now works, `https → https` (HA is https since 17 Sep)

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

### GitHub Pages note (fixed 17 Sep)
HA is now `https` (`https://192.168.0.208:8123` with self-signed cert at `config/ssl/cert.pem`), so **both versions are `https → https`** and no mixed-content block. 
- **HA local `https`** works offline on LAN after you accept the cert once (Safari → Show Details → Visit Website).
- **GitHub Pages `https`** needs internet to load the page itself, then fetches HA `https` on your LAN - works at home with internet.
- Away from home without internet: use HA local `https` bookmark (no GitHub needed). Tailscale away was scrapped per your order.

### Files
- `index.html` — single-file console (also deployed as `captains_console.html` in HA `config/www/`)

Built by Jarvis for Ethan, Sep 2026. For Ethan's phone — not Mike M.
