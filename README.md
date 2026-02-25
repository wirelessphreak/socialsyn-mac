# ⬡ SocialSync

> Cross-post photos to Mastodon, Pixelfed, Bluesky, and Threads — all from one beautiful desktop app.

![Build DMG](https://github.com/yourusername/socialsync/actions/workflows/build-dmg.yml/badge.svg)
![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python&logoColor=white)
![PyQt6](https://img.shields.io/badge/UI-PyQt6-green?logo=qt&logoColor=white)
![Platform](https://img.shields.io/badge/Platform-macOS%20%7C%20Linux-lightgrey?logo=apple&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-purple)

---

## ⬇️ Download

### macOS (MacBook Air / Pro / Mac mini)
👉 Go to [**Releases**](https://github.com/yourusername/socialsync/releases/latest) and download **SocialSync.dmg**

1. Open the DMG
2. Drag **SocialSync** into your **Applications** folder
3. Double-click to launch

> **First launch:** if macOS says "unidentified developer", right-click the app → **Open** → **Open** to bypass Gatekeeper.

### Linux (Ubuntu)
```bash
git clone https://github.com/yourusername/socialsync.git
cd socialsync
pip3 install -r requirements.txt
python3 socialsync.py
```

---

## ✨ Features

- 🖼️ **Image upload** — click to select PNG, JPG, GIF, or WebP
- ✍️ **Caption editor** with per-platform character counters
- 👁️ **Live post preview** — see exactly how your post will look before sending
- ♿ **Alt text** support for screen reader accessibility
- ✅ **Selective posting** — choose which accounts receive each post
- 📊 **Real-time progress** — per-account status while posting
- 👤 **Multiple accounts** — add multiple Mastodon/Pixelfed instances
- 🔒 **Local credential storage** — tokens never leave your machine
- 🌙 **Modern dark UI** — looks great on macOS and Linux

---

## 📦 Supported Platforms

| Platform | Auth | Char Limit |
|----------|------|-----------|
| 🐘 Mastodon | Access Token | 500 |
| 📸 Pixelfed | Access Token | 2,200 |
| 🦋 Bluesky | App Password | 300 |
| @ Threads | Graph API Token | 500 |

---

## 🔑 Getting API Credentials

See the full guide → **[docs/CREDENTIALS.md](docs/CREDENTIALS.md)**

| Platform | What you need |
|----------|--------------|
| 🐘 Mastodon | Settings → Development → New Application → Access Token |
| 📸 Pixelfed | Settings → Applications → New Application → Access Token |
| 🦋 Bluesky | Settings → Privacy → App Passwords → New App Password |
| @ Threads | Meta Developer Console → Graph API Token |

---

## 🤖 Automated DMG Builds

Every time you publish a **GitHub Release**, the DMG is built automatically on a real macOS GitHub runner and attached to the release. No Mac needed to distribute!

**To publish a new release:**
1. Go to your repo → **Releases** → **Draft a new release**
2. Create a tag like `v1.0.0`
3. Click **Publish release**
4. GitHub builds the DMG and attaches it automatically (~5 minutes)

You can also grab test builds from any push: **Actions → Build macOS DMG → Artifacts**

---

## 🔧 Building from Source

### macOS
```bash
pip3 install PyQt6 requests Pillow pyinstaller
pyinstaller --windowed --name "SocialSync" socialsync.py
# App appears in dist/SocialSync.app
```

### Linux
```bash
pip3 install -r requirements.txt --break-system-packages
python3 socialsync.py
```

---

## 🔒 Privacy & Security

- Credentials stored locally — never sent to any server other than the social platforms directly
- No telemetry, no analytics
- To revoke access, delete the token from each platform's settings page

---

## 🤝 Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) — PRs welcome!

## 📄 License

MIT — see [LICENSE](LICENSE)
