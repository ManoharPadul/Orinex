# ⚡ Orinex

> AI-powered code editor for Windows, macOS, Linux, iPhone and Android — supporting Claude, OpenAI, Gemini, Mistral, Groq, Cohere, Together and Ollama

![Orinex](https://img.shields.io/badge/version-1.0.0-6366f1?style=for-the-badge)
![License](https://img.shields.io/badge/license-MIT-green?style=for-the-badge)
![Platform](https://img.shields.io/badge/platform-Windows%20%7C%20macOS%20%7C%20Linux%20%7C%20iOS%20%7C%20Android-blue?style=for-the-badge)
![Electron](https://img.shields.io/badge/Electron-28-47848F?style=for-the-badge&logo=electron)

Built by [Manohar Padul](https://manoharpadul.com)

Orinex is an open source project, built by Manohar Padul with support from 4-5 AI assistants.

---

## ✨ Features

- 🤖 **Multi-AI Support** — Claude (Anthropic), GPT-4 (OpenAI), Gemini (Google), Mistral, Groq
- 🎨 **6 Built-in Themes** — Dark, Light, Monokai, Dracula, Nord, Solarized + Custom theme builder
- 🖥️ **Native Desktop App** — Windows (.exe), macOS (.dmg), Linux (.AppImage / .deb / .rpm)
- 📱 **Mobile App Runtime** — iPhone and Android build path via Capacitor
- 🌍 **Broad Language Modes on Mobile** — Monaco language catalog (many programming and markup languages)
- 🐍 **Python on Mobile** — Run Python code directly on iPhone/Android using in-app Pyodide runtime
- 📦 **Offline Python Runtime on Mobile** — Pyodide is bundled locally (no first-run internet dependency)
- 📁 **File Explorer** — Open files and folders from your system
- ⌨️ **VSCode-like Shortcuts** — Ctrl+S, Ctrl+O, Ctrl+K, Ctrl+,, and more
- 🖱️ **OS Window Styles** — macOS traffic lights, Windows title bar, Linux minimal
- 🔒 **Local & Secure** — Your API keys stored locally, never sent anywhere except the AI provider
- 🌐 **Works Offline** — Editor works without internet; AI features need your API key

---

## 🆕 Recent Changes

- Rebranded from DevAI to **Orinex** with updated icons and branding.
- Removed startup loading splash for a faster direct launch.
- Added startup homepage with session resume support.
- Added session restore for last project, open tabs, and active file.
- Added real-time resizable sidebar, terminal, and AI panel.
- Improved built-in terminal flow (single-stream output with prompt continuity).
- Added connection-gated AI panel visibility with provider checks.
- Added mobile editor support for iPhone and Android via Capacitor.
- Added mobile Python execution using Pyodide.
- Added local Pyodide preloading so Python runtime works without first-run internet on iPhone/Android.

---

## 📦 Downloads

### Pre-built Binaries
| Platform | File | Architecture |
|----------|------|-------------|
| Windows | `Orinex-1.0.0-Windows-x64.exe` | x64 |
| Windows (portable) | `Orinex-1.0.0-Windows-x64.exe` | x64 |
| macOS | `Orinex-1.0.0-macOS-universal.dmg` | Intel + Apple Silicon |
| Linux | `Orinex-1.0.0-Linux-x64.AppImage` | x64 |
| Linux | `Orinex-1.0.0-Linux-x64.deb` | x64 |
| Linux | `Orinex-1.0.0-Linux-x64.rpm` | x64 |

> Download from the [Releases](https://github.com/ManoharPadul/Orinex/releases) page.

---

## 🚀 Getting Started (Build from Source)

### Prerequisites
- [Node.js](https://nodejs.org/) v18 or higher
- npm v9 or higher
- Git

### Installation

```bash
# Clone the repository
git clone https://github.com/ManoharPadul/Orinex.git
cd Orinex

# Install dependencies
npm install

# Run in development mode
npm start
```

### Building

```bash
# Build for Windows
npm run build:win

# Build for macOS (must be on macOS)
npm run build:mac

# Build for Linux
npm run build:linux

# Build for all platforms
npm run build:all
```

Built files will be in the `dist/` folder.

### Mobile Apps (iPhone and Android)

Orinex includes a dedicated mobile client in `mobile-web/` and can be packaged with Capacitor.

```bash
# Add native mobile projects (run once)
npm run mobile:add:android
npm run mobile:add:ios

# Preload local Python runtime assets (Pyodide)
npm run mobile:preload:python

# Sync web code into native shells
# (this command also runs mobile:preload:python automatically)
npm run mobile:sync

# Open Android Studio project
npm run mobile:open:android

# Open Xcode project (run on macOS)
npm run mobile:open:ios
```

Notes:
- iOS build/signing requires macOS + Xcode.
- Mobile supports broad editing language modes via Monaco.
- Python execution is supported on mobile via the built-in Pyodide runtime (Run Py).
- Pyodide runtime files are bundled locally into the app package for both iPhone and Android.
- No first-run internet connection is required to initialize Python runtime on mobile.
- Local execution of every non-Python language is not possible on mobile sandbox by default; use desktop runtime or remote/cloud runners for full execution workflows.

---

## 🔑 Setting Up AI Providers

1. Open Orinex
2. Click the provider selector in the AI panel (top right)
3. Enter your API key for the provider you want to use

| Provider | Get API Key |
|----------|------------|
| Claude (Anthropic) | [console.anthropic.com](https://console.anthropic.com) |
| OpenAI (GPT-4) | [platform.openai.com](https://platform.openai.com) |
| Google Gemini | [aistudio.google.com](https://aistudio.google.com) |
| Mistral | [console.mistral.ai](https://console.mistral.ai) |
| Groq | [console.groq.com](https://console.groq.com) |

Your API keys are stored **locally on your machine** using encrypted storage. They are never sent to anyone except the AI provider you choose.

---

## ⌨️ Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| `Ctrl/Cmd + S` | Save file |
| `Ctrl/Cmd + Shift + S` | Save As |
| `Ctrl/Cmd + O` | Open file |
| `Ctrl/Cmd + N` | New file |
| `Ctrl/Cmd + K` | Ask AI |
| `Ctrl/Cmd + ,` | Settings |
| `Ctrl/Cmd + B` | Toggle sidebar |
| `Ctrl/Cmd + Shift + A` | Toggle AI panel |
| `Ctrl + `` ` | Toggle terminal |
| `Ctrl/Cmd + F` | Find |
| `F11` | Fullscreen |

---

## 🎨 Themes

- **Dark** (default) — VS Code dark
- **Light** — Clean white
- **Monokai** — Classic Monokai
- **Dracula** — Purple dark
- **Nord** — Arctic cool
- **Solarized** — Solarized dark
- **Custom** — Build your own with color pickers

---

## 📁 Project Structure

```
Orinex/
├── src/
│   ├── main.js          # Electron main process
│   ├── preload.js       # Secure IPC bridge
│   ├── editor.html      # Main editor UI
│   └── splash.html      # Legacy splash template (startup splash removed)
├── mobile-web/
│   ├── index.html       # Mobile editor entry (Monaco)
│   ├── app.js           # Mobile logic
│   ├── styles.css       # Mobile styles
│   └── manifest.webmanifest
├── assets/
│   ├── icon.png         # Linux icon
│   ├── icon.ico         # Windows icon
│   ├── icon.icns        # macOS icon
│   └── orinex-logo.svg  # Orinex logo
├── capacitor.config.json
├── package.json         # App config & build settings
├── README.md
└── LICENSE
```

---

## 🤝 Contributing

Contributions are welcome! Please:

1. Fork the repo
2. Create a feature branch: `git checkout -b feature/amazing-feature`
3. Commit your changes: `git commit -m 'Add amazing feature'`
4. Push to the branch: `git push origin feature/amazing-feature`
5. Open a Pull Request

Ideas for contributions:
- Syntax highlighting with CodeMirror or Monaco Editor
- Git integration
- Extension/plugin system
- More AI providers
- Mobile app version
- Cloud sync

---

## 📄 License

MIT License — see [LICENSE](LICENSE) file.

---

## 👨‍💻 Author

**Manohar Padul**
- Website: [manoharpadul.com](https://manoharpadul.com)
- LinkedIn: [linkedin.com/in/manoharpadul](https://linkedin.com/in/manoharpadul-143395182)
- GitHub: [github.com/manoharpadul](https://github.com/manoharpadul)

---

*If you find this useful, please ⭐ star the repository!*
