# ⚡ Orinex

> A modern AI-powered code editor for desktop and mobile, built for speed, privacy, and real-world workflows.

![Version](https://img.shields.io/badge/version-1.0.0-0ea5e9?style=for-the-badge)
![License](https://img.shields.io/badge/license-MIT-22c55e?style=for-the-badge)
![Platforms](https://img.shields.io/badge/platform-Windows%20%7C%20macOS%20%7C%20Linux%20%7C%20iOS%20%7C%20Android-1d4ed8?style=for-the-badge)
![Electron](https://img.shields.io/badge/Electron-41-47848F?style=for-the-badge&logo=electron)

Built by [Manohar Padul](https://manoharpadul.com)

Orinex is an open source project, crafted with support from multiple AI assistants.

---

## 🌟 Why Orinex?

- ⚡ **Fast, focused coding experience** with desktop power and mobile reach
- 🤖 **Multiple AI providers in one editor** with local key storage
- 🧩 **Modern workflow features** like session restore, tab restore, and resizable panels
- 🐍 **Python on mobile** with offline-ready runtime bundling

---

## ✨ Feature Highlights

- 🤖 **Multi-AI support**
	Claude, OpenAI, Gemini, Mistral, Groq, Cohere, Together, and Ollama (local LLM).

- 🔄 **Smart AI provider continuity**
	When a provider hits quota/rate limits, Orinex can switch to another configured provider and continue the same request.

- 💾 **Persistent AI preferences**
	Save provider and model choices (including Ollama/GitHub models) and keep them after restart.

- 🖥️ **Desktop apps for all major platforms**
	Native packaging for Windows, macOS, and Linux.

- 🪟 **Window chrome customization**
	Switch between native OS window chrome and custom Orinex window style presets.

- 📱 **iPhone and Android support**
	Dedicated mobile client powered by Capacitor and Monaco.

- 🐍 **Python execution on mobile**
	Run Python directly in-app via Pyodide.

- 📦 **Offline Python runtime on mobile**
	Pyodide runtime is bundled locally, so first run does not require internet.

- 🧠 **Session continuity**
	Restore last project, open tabs, and active file.

- 🧩 **Extensions and cloud sync**
	Built-in extension loading and GitHub-backed cloud sync for settings/session snapshots.

- 🗂️ **Project language auto-detection**
	Detects the dominant project language on folder open; unsupported extensions are clearly marked as support-coming-soon.

- 🧰 **Productivity-first editor UX**
	Real-time panel resizing, integrated terminal, themes, and VS Code-style shortcuts.

---

## 🆕 Recent Upgrades

- 🎨 Rebranded from DevAI to **Orinex** with new logo and app icons.
- 🚀 Removed startup loading splash for faster launch.
- 🏠 Added startup homepage with resume session support.
- ♻️ Added session restore for project, tabs, and active file.
- ↔️ Added real-time resizable sidebar, terminal, and AI panel.
- 🧪 Improved terminal flow with cleaner prompt/output continuity.
- 🔐 Added connection-gated AI panel visibility and provider checks.
- 📲 Added mobile editor runtime for iPhone and Android.
- 🐍 Added mobile Python execution using Pyodide.
- 📦 Added local Pyodide preloading for offline Python startup.
- 💾 Added explicit Save AI Preferences button for provider/model persistence.
- 🔁 Added API quota/rate-limit failover flow with continue-on-switch behavior.
- 🪟 Added native window chrome toggle (native/custom titlebar mode).
- 🧠 Added Node.js and React (JSX) language support in editor/run flows.
- 🔎 Added project-level language detection with unsupported-language notice.
- 🧩 Added extension manager and command execution hooks.
- ☁️ Added GitHub-based cloud sync (push/pull).

---

## 📥 Downloads

### Pre-built binaries

| Platform | File | Architecture |
|----------|------|-------------|
| Windows | `Orinex-1.0.0-Windows-x64.exe` | x64 |
| Windows (portable) | `Orinex-1.0.0-Windows-x64.exe` | x64 |
| macOS | `Orinex-1.0.0-macOS-universal.dmg` | Intel + Apple Silicon |
| Linux (portable) | `Orinex-1.0.0-Linux-x64.tar.gz` | x64 |
| Linux | `Orinex-1.0.0-Linux-x64.AppImage` | x64 |
| Linux | `Orinex-1.0.0-Linux-x64.deb` | x64 |
| Linux | `Orinex-1.0.0-Linux-x64.rpm` | x64 |

➡️ Download from [GitHub Releases](https://github.com/ManoharPadul/Orinex/releases).

---

## 🚀 Quick Start (From Source)

### Requirements

- [Node.js](https://nodejs.org/) v18+
- npm v9+
- Git

### Run locally

```bash
git clone https://github.com/ManoharPadul/Orinex.git
cd Orinex
npm install
npm start
```

---

## 🏗️ Build Desktop Apps

```bash
# Windows x64 (local Windows build)
npm run build:win:x64

# Linux x64 (best on Linux or CI)
npm run build:linux:x64

# Linux portable artifact from Windows
npm run build:linux:x64:portable

# Build all desktop targets
npm run build:all
```

Built files are generated in `dist/`.

### Linux note for Windows users

- AppImage packaging requires Linux tooling (`mksquashfs`).
- On plain Windows, use `npm run build:linux:x64:portable` for uploadable Linux `.tar.gz`.
- For AppImage, `.deb`, and `.rpm`, use GitHub Actions or a Linux host.

---

## ☁️ Build For Upload (Recommended)

This repository includes CI workflow: `.github/workflows/build-desktop.yml`.

1. Push your code to GitHub.
2. Open the Actions tab.
3. Run Build Desktop Artifacts (manual) or push a tag like `v1.0.1`.
4. Download artifacts: `orinex-windows-x64` and `orinex-linux-x64`.
5. Upload artifacts to your GitHub Release.

---

## 📲 Mobile Apps (iPhone + Android)

Orinex includes a dedicated mobile client in `mobile-web/` and packages via Capacitor.

```bash
# Add native projects (one-time)
npm run mobile:add:android
npm run mobile:add:ios

# Bundle local editor runtime assets (Monaco)
npm run mobile:preload:editor

# Bundle local Python runtime assets (Pyodide)
npm run mobile:preload:python

# Sync web code into native projects
# (also runs mobile:preload:editor and mobile:preload:python automatically)
npm run mobile:sync

# Open native IDE projects
npm run mobile:open:android
npm run mobile:open:ios
```

### Mobile notes

- 🍎 iOS signing/build requires macOS + Xcode.
- 🌍 Monaco provides broad language editing support and is bundled locally.
- 🐍 Python runs in mobile app with built-in Pyodide (Run Py).
- 📦 Monaco and Pyodide runtimes are bundled locally for both iPhone and Android.
- 🚫 Full native execution for every non-Python language is not possible in mobile sandbox by default; use desktop or remote runners.

---

## 🔑 AI Provider Setup

1. Open Orinex.
2. Choose provider in the AI panel.
3. Enter your API key.
4. Click **Save AI Preferences** to persist provider + model selection.

| Provider | API key portal |
|----------|----------------|
| Claude (Anthropic) | [console.anthropic.com/settings/keys](https://console.anthropic.com/settings/keys) |
| OpenAI | [platform.openai.com/api-keys](https://platform.openai.com/api-keys) |
| Gemini | [aistudio.google.com/app/apikey](https://aistudio.google.com/app/apikey) |
| Mistral | [console.mistral.ai/api-keys](https://console.mistral.ai/api-keys/) |
| Groq | [console.groq.com/keys](https://console.groq.com/keys) |
| Cohere | [dashboard.cohere.com/api-keys](https://dashboard.cohere.com/api-keys) |
| Together | [api.together.xyz/settings/api-keys](https://api.together.xyz/settings/api-keys) |
| GitHub Models (Pro/Student) | [github.com/settings/tokens](https://github.com/settings/tokens) |
| Ollama (local) | [ollama.com](https://ollama.com) |

🔐 API keys are stored locally and only sent to the provider you select.

For GitHub Models, use a GitHub token with access to GitHub Models APIs.

### GitHub OAuth sign-in (recommended)

Orinex supports Device Flow OAuth sign-in for GitHub Models, so users can connect with a button instead of manually pasting token values.

1. Create a GitHub OAuth App and copy the Client ID.
2. In Orinex AI settings, select GitHub Models.
3. Paste your GitHub OAuth Client ID.
4. Click Sign in with GitHub and complete the browser verification code prompt.
5. Orinex stores the returned token locally and uses it for GitHub Models requests.

### When API quota is full

If your current provider reaches quota/rate limits, Orinex shows a prompt so you can switch to another configured provider and continue the same request without starting over.

GitHub Models docs (latest):
- [Experimenting with AI models using the API](https://docs.github.com/en/github-models/use-github-models/prototyping-with-ai-models#experimenting-with-ai-models-using-the-api)

---

## ⌨️ Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| `Ctrl/Cmd + S` | Save file |
| `Ctrl/Cmd + Shift + S` | Save As |
| `Ctrl/Cmd + O` | Open file |
| `Ctrl/Cmd + N` | New file |
| `Ctrl/Cmd + K` | Ask AI |
| `Ctrl/Cmd + ,` | Open settings |
| `Ctrl/Cmd + B` | Toggle sidebar |
| `Ctrl/Cmd + Shift + A` | Toggle AI panel |
| `Ctrl + Backtick` | Toggle terminal |
| `Ctrl/Cmd + F` | Find |
| `F11` | Fullscreen |

---

## 🎨 Themes

- 🌑 Dark (default)
- ☀️ Light
- 🟡 Monokai
- 🧛 Dracula
- ❄️ Nord
- 🌅 Solarized
- 🧁 Catppuccin (Mocha, Frappe, Latte)
- 🌃 Tokyo Night
- 🌈 Ayu Dark
- ✨ Dainty
- 🐙 GitHub Dark
- ⚛️ Atom One Dark
- 🚀 Houston
- 🦉 Night Owl
- 🍵 Matcha
- 🛠️ Custom theme builder

### 🖋️ Font Customization

- Monaspace family support: Neon, Krypton, Argon, Xenon, Radon
- Also supports Cascadia Code, Fira Code, Consolas, Monaco, JetBrains Mono, Source Code Pro

---

## 🧱 Project Structure

```text
Orinex/
├── src/
│   ├── main.js
│   ├── preload.js
│   ├── editor.html
│   └── hardware.js
├── mobile-web/
│   ├── index.html
│   ├── app.js
│   ├── styles.css
│   ├── vendor/
│   │   └── pyodide/
│   └── manifest.webmanifest
├── scripts/
│   └── preload-pyodide.js
├── assets/
│   ├── icon.png
│   ├── icon.ico
│   ├── icon.icns
│   └── orinex-logo.svg
├── capacitor.config.json
├── package.json
└── README.md
```

---

## 🤝 Contributing

Contributions are welcome.

1. Fork the repository.
2. Create your branch: `git checkout -b feature/amazing-feature`
3. Commit changes: `git commit -m "Add amazing feature"`
4. Push branch: `git push origin feature/amazing-feature`
5. Open a Pull Request.

Ideas:

- 🌿 Advanced Git workflows
- 🧪 Better testing and diagnostics
- 📱 More mobile-first UX improvements

---

## 📄 License

MIT License. See [LICENSE](LICENSE).

---

## 👨‍💻 Author

**Manohar Padul**

- 🌐 Website: [manoharpadul.com](https://manoharpadul.com)
- 💼 LinkedIn: [linkedin.com/in/manoharpadul](https://linkedin.com/in/manoharpadul-143395182)
- 🐙 GitHub: [github.com/manoharpadul](https://github.com/manoharpadul)

---

If Orinex helps you, consider giving the repo a ⭐.
