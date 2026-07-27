<div align="center">

  <img src="https://raw.githubusercontent.com/sayan2302/OpenSpot/main/client/public/openspot.png" alt="OpenSpot Logo" width="128" />

  # 🎵 OpenSpot (`@supasayan/openspot`)

  **Cross-Platform High-Res Music Downloader, Player & Song Lore Platform**

  [![npm version](https://img.shields.io/npm/v/@supasayan/openspot.svg?style=for-the-badge&color=6366F1)](https://www.npmjs.com/package/@supasayan/openspot)
  [![npm downloads](https://img.shields.io/npm/dm/@supasayan/openspot.svg?style=for-the-badge&color=10B981)](https://www.npmjs.com/package/@supasayan/openspot)
  [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)
  [![Node Version](https://img.shields.io/badge/node-%3E%3D18.0.0-brightgreen.svg?style=for-the-badge)](https://nodejs.org)
  [![OS Support](https://img.shields.io/badge/platform-Windows%20%7C%20macOS%20%7C%20Linux-informational?style=for-the-badge)](#-cross-platform-support)

  ---

  ### ⚡ Instant 1-Command Launch (Zero Installation Required)

  Run directly from your terminal in seconds:

  ```bash
  npx @supasayan/openspot
  ```

  *Automatically launches your default browser at `http://127.0.0.1:3001` with zero setup!*

</div>

---

## 📖 Table of Contents
- [✨ Key Features](#-key-features)
- [🚀 Quick Start & Installation](#-quick-start--installation)
  - [Method 1: Instant NPX Execution (Recommended)](#method-1-instant-npx-execution-recommended)
  - [Method 2: Global CLI Installation](#method-2-global-cli-installation)
  - [Method 3: Local Clone & Development Setup](#method-3-local-clone--development-setup)
- [🖥️ Cross-Platform Support](#️-cross-platform-support)
- [⚙️ How It Works](#️-how-it-works)
- [🛠️ Troubleshooting & FAQ](#️-troubleshooting--faq)
- [🤝 Contributing](#-contributing)
- [💬 Support & Feedback](#-support--feedback)
- [📜 License](#-license)

---

## ✨ Key Features

| Feature | Description |
| :--- | :--- |
| **🚀 Zero-Config Setup** | Auto-detects, downloads, and configures native `yt-dlp` and `ffmpeg` binaries for your OS on first startup. |
| **🎧 High-Resolution Audio** | Export in **Lossless FLAC**, **M4A (AAC)**, **MP3**, or **OPUS** audio formats. |
| **🎤 Synced Karaoke Lyrics** | Real-time LRC timestamp synchronization with interactive vocal density curves and click-to-seek stanza navigation. |
| **💡 Behind-The-Song Lore** | Liquid glass drawer surfacing song origin stories, verified artist interview quotes, and chart achievements. |
| **🏷️ Automatic Tagging** | Embeds high-res album cover art, title, artist, album, release year, track index, and lyrics tags into audio files. |
| **🎶 Built-in Stream Player** | Stream tracks directly inside a sleek glassmorphic player with full queue and volume management before downloading. |
| **⚡ Bulk & Playlist Downloads** | Queue single tracks, top charts, or full playlists with real-time download progress and speed meters. |
| **📂 Native OS Picker** | Integrated 1-click folder selection and native file explorer opening (`explorer.exe` / `open` / `xdg-open`). |

---

## 🚀 Quick Start & Installation

### Method 1: Instant NPX Execution (Recommended)
No installation required! Run this single command in PowerShell, Terminal, or Command Prompt:

```bash
npx @supasayan/openspot
```
Your browser will open automatically to `http://127.0.0.1:3001`.

---

### Method 2: Global CLI Installation
Install globally on your machine to use `openspot` from any directory:

```bash
npm install -g @supasayan/openspot
```

Then run whenever you want music:
```bash
openspot
# OR
openspot-cli
```

---

### Method 3: Local Clone & Development Setup
Want to customize or contribute? Set up locally in minutes:

```bash
# 1. Clone the repository
git clone https://github.com/sayan2302/OpenSpot.git
cd OpenSpot

# 2. Install all dependencies for root, client, and server
npm run install-all

# 3. Start the development server (runs React client on :5173 and Express on :3001)
npm run dev
```

---

## 🖥️ Cross-Platform Support

OpenSpot natively adapts to your operating system:

| Operating System | Native Folder Picker | File Explorer Launch | Binary Resolutions |
| :--- | :---: | :---: | :--- |
| **Windows 10 / 11** | PowerShell `FolderBrowserDialog` | `explorer.exe` | Auto-fetches `ffmpeg.exe` & `yt-dlp.exe` |
| **macOS (Intel / Apple Silicon)** | `osascript` Finder Dialog | `open` | Auto-fetches `ffmpeg` & `yt-dlp` (macOS quarantine cleared) |
| **Linux (Ubuntu, Debian, Fedora, Arch)** | `zenity` / `kdialog` | `xdg-open` | Auto-fetches `ffmpeg` & `yt-dlp_linux` |

---

## ⚙️ How It Works

1. **System Health Check**: On launch, the backend checks for `ffmpeg` and `yt-dlp`. If missing, it securely downloads verified binaries to `~/.openspot/bin/`.
2. **Music API Proxy**: Queries tracks, albums, artists, and playlists via high-speed music inner-tube endpoints.
3. **Stream & Download Engine**: Rotates extractor clients (`android`, `web`, `tv`) to bypass rate limits and HTTP 403 Forbidden errors.
4. **Metadata & Artwork Tagging**: Uses `ffmpeg` to embed cover thumbnails and ID3/FLAC metadata tags into destination files.

---

## 🛠️ Troubleshooting & FAQ

<details>
<summary><strong>Q: Port 3001 is already in use on my machine. What happens?</strong></summary>
<br />
OpenSpot automatically scans for an open port starting at 3001 (e.g. 3002, 3003) and binds the local server and web browser to the first free port automatically.
</details>

<details>
<summary><strong>Q: Downloads fail or freeze on Linux / macOS. How do I fix this?</strong></summary>
<br />
If automated binary download is blocked by system policies, you can install native dependencies via your system package manager:
<ul>
  <li><strong>macOS</strong>: <code>brew install yt-dlp ffmpeg</code></li>
  <li><strong>Ubuntu / Debian</strong>: <code>sudo apt update && sudo apt install -y ffmpeg yt-dlp</code></li>
  <li><strong>Fedora</strong>: <code>sudo dnf install ffmpeg yt-dlp</code></li>
</ul>
</details>

---

## 🤝 Contributing

Contributions, feature suggestions, and bug reports are welcome!

1. Fork the Project Repository (`https://github.com/sayan2302/OpenSpot`)
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 💬 Support & Feedback

If you enjoy using OpenSpot or find it helpful:
- ⭐ **Star the Repository** on [GitHub](https://github.com/sayan2302/OpenSpot)
- 🐛 **Report Issues / Feature Requests**: [GitHub Issues](https://github.com/sayan2302/OpenSpot/issues)
- 📦 **NPM Package**: [@supasayan/openspot on npmjs.com](https://www.npmjs.com/package/@supasayan/openspot)

---

## 📜 License

Distributed under the **MIT License**. See `LICENSE` for more information.

<div align="center">
  <sub>Built with ❤️ by Sayan Pramanick</sub>
</div>
