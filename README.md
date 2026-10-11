# 🔗 LinkVault — Smart Shortener + Pastebin (MIT)

Free URL shortener & pastebin with a **smart protection layer**,
countdown interstitial with ads, and an earnings dashboard.
100% client-side except public third-party APIs.

## Features

- **Shorten:** global providers (is.gd → v.gd → cleanuri, auto-fallback)
  for worldwide links; **native vault links** (`#s=CODE`) with countdown
  ads, optional password, expiry. Auto-falls back to native if APIs blocked.
- **Protection scan:** every native link gets punycode/IP/`@`-trick/port/
  risky-TLD/subdomain/keyword/open-redirect/nested-shortener analysis with
  safe/suspicious/dangerous verdict + hash allowlist validation.
- **Pastebin:** local vault pastes (expiry, burn-after-read, `#p=` links)
  + global publish via **paste.rs** (worldwide link).
- **Earnings:** vault clicks counted locally, estimate = clicks × CPM/1000
  (CONFIG.cpm). Real revenue needs ad accounts + backend counting.

## Money

`CONFIG.ads` (AdSense/Carbon IDs) fills top + gate + footer slots;
empty = tasteful placeholder. Interstitial countdown (`CONFIG.waitSec`)
is the monetized surface — like major link shorteners.

## Honest limits

- Vault links/pastes live **in the visitor's browser** (localStorage).
  Global reach needs a backend (worker + KV). paste.rs covers global pastes.
- Short-API availability depends on third parties + CORS.
- Passwords stored plainly client-side = demo-grade; backend for real use.

## Contact

📧 baranavisat@gmail.com · 📞 +90 531 326 37 22 · WhatsApp

## Run / Deploy

```bash
cd linkvault
python3 -m http.server 8080
```
Static single file. GitHub Pages-ready from repo root.

## License

MIT.
