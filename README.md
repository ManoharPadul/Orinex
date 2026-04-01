<div align="center">

# ⚡ Orinex

### AI-Powered Code Editor — Built for Real Developers

[![Version](https://img.shields.io/badge/version-1.0.0-0ea5e9?style=for-the-badge)](https://github.com/ManoharPadul/Orinex/releases)
[![License](https://img.shields.io/badge/license-MIT-22c55e?style=for-the-badge)](LICENSE)
[![Electron](https://img.shields.io/badge/Electron-41-47848F?style=for-the-badge&logo=electron)](https://electronjs.org)
[![Platform](https://img.shields.io/badge/platform-Windows%20%7C%20macOS%20%7C%20Linux-1d4ed8?style=for-the-badge)](#-downloads)

**[⬇️ Download](#-downloads) · [✨ Features](#-features) · [🎨 Themes](#-themes) · [🔑 AI Setup](#-ai-provider-setup)**

Built by [Manohar Padul](https://manoharpadul.com)

</div>

---

## 🌟 What is Orinex?

Orinex is a modern, AI-powered desktop code editor built with Electron. It combines the power of multiple AI providers with a full-featured coding environment — giving you a VS Code-style editor with a built-in AI assistant, memory engine, and developer identity system all in one app.

---

## ✨ Features

### 🤖 AI Integration
- **9 AI Providers** — Claude, OpenAI, Gemini, Mistral, Groq, Cohere, Together, GitHub Models, Ollama (local LLM)
- **AI Chat Panel** — chat with AI about your code in a dedicated panel
- **Inline AI** — select any code, get instant fix, explain, or refactor suggestions
- **AI Autocomplete** — Copilot-style suggestions as you type
- **AI Code Review on Save** — automatic code review with score, issues, and suggestions every time you save
- **Chat with Codebase** — ask AI questions about your entire project
- **Smart AI Failover** — when one provider hits quota, automatically switches to the next configured provider
- **AI Chat History** — full conversation history per file, grouped by date with slide-in drawer
- **One-click AI Self-Test** — validate provider routing, model availability, and connectivity

### 🧠 Memory & Identity Engine
- **Living Developer Profile** — Orinex learns who you are: name, languages, frameworks, projects, goals
- **Smart Context Injection** — injects only relevant profile data per AI question (code questions get code context, career questions get goals context)
- **Passive Learning** — silently tracks what languages you use, how long you code, what errors you hit
- **Memory Inspector** — view and edit every memory field with full diff and version history
- **Memory Compression** — auto-compresses profile when it gets too large, keeps it lean
- **Undo Memory Changes** — full history with restore to any previous state
- **AI Memory Insights** — weekly AI-generated summary of your coding activity and progress
- **Memory Export** — export your profile as JSON or Markdown
- **Cloud Backup** — encrypted backup to GitHub Gist, restore on any machine
- **Onboarding Flow** — friendly 5-step setup on first launch to build your profile

### 🖥️ Editor
- **Monaco Editor** — the same engine that powers VS Code
- **Split Editor** — two panes side by side with independent files, cursors, and scrolls
- **Find & Replace** — in-file search with match highlighting, case sensitive, regex support
- **Project-Wide Search** — search across all files in your workspace (Ctrl+Shift+F)
- **Bracket Matching & Auto-close** — auto-insert closing brackets, wrap selections, highlight matching pairs
- **Word Wrap Toggle** — Alt+Z toggles line wrapping
- **Auto Save** — configurable auto save with 10s / 30s / 1min / 2min intervals
- **Line Number Breakpoints** — click line numbers to set visual breakpoints
- **Gutter Markers** — colored dots for breakpoints and code review issues
- **Minimap** — interactive minimap with click-to-scroll and viewport highlight
- **Code Folding, Indentation, Multi-cursor** — full VS Code-style editing

### 🗂️ File Management
- **File Tree Sidebar** — full project explorer with expand/collapse folders
- **Right-click Context Menu** — New File, New Folder, Rename, Delete, Open
- **Drag & Drop** — drag files from OS into editor to open them
- **Smart Tab Bar** — unsaved dot indicators, right-click tab menu, middle-click to close, overflow dropdown
- **Native File Watcher** — detects external file changes and prompts Reload / Keep / Diff
- **Multi-tab** — open many files simultaneously

### 🎛️ Productivity
- **Command Palette** — Ctrl+K / Cmd+K opens fuzzy-search command palette with all actions
- **Focus Mode** — F11 hides everything and centers the editor for distraction-free coding
- **Typewriter Mode** — current line stays vertically centered as you type
- **Snippet Library** — save and insert reusable code snippets with search, tags, and language filter
- **Advanced Pomodoro Timer** — fully customizable timer in status bar with work/break cycles, custom presets (Deep Work, Quick Sprint, Study Block, Gym Rest, and more)
- **System Tray** — app runs in system tray, hides to tray on close
- **Global Hotkey** — Ctrl+Shift+Space opens a mini AI input from anywhere on your system
- **Multi-Window** — open multiple independent Orinex windows
- **Live Collaboration Cursors** — see other users' cursors when Cloud Sync is active

### 💻 Terminal
- **Integrated Terminal** — full terminal inside the editor
- **Multiple Terminal Tabs** — open up to 8 terminals, switch between them instantly
- **Split Terminal** — two terminals side by side
- **Terminal Toolbar** — New, Split, Clear, Kill buttons

### 🔒 Security
- **Masked API Keys** — all tokens and API keys hidden as •••••• with eye toggle to reveal
- **Copy Protection** — right-click and Ctrl+C disabled on sensitive fields
- **Auto-Lock on Idle** — automatically locks screen after configurable idle timeout (1/5/10 min)
- **Screen Lock Button** — 🔒 button or Ctrl+L / Cmd+L instantly locks the app
- **Full-screen Lock Overlay** — dark overlay requiring click to unlock

### ☁️ Cloud & Sync
- **Cloud Sync** — Push/Pull settings, themes, AI preferences, and session state via GitHub Gist
- **Git Integration** — built-in Git status, diff, commit, push, pull inside the editor
- **Auto Updater** — checks GitHub Releases for updates, shows banner in status bar
- **Multi-Machine Sync** — same profile and settings across all your machines

### 🎨 Appearance
- **17 Built-in Themes** — Dark, Light, Monokai, Dracula, Nord, Solarized Dark, Catppuccin (Mocha/Frappe/Latte), Tokyo Night, Ayu Dark, Dainty, GitHub Dark, Atom One Dark, Houston, Night Owl, Matcha
- **Custom Theme Builder** — create your own theme with CSS variable editor
- **Font Customization** — Monaspace (Neon/Krypton/Argon/Xenon/Radon), Cascadia Code, Fira Code, JetBrains Mono, and more
- **Window Style** — switch between native OS titlebar and custom Orinex titlebar
- **Smooth Theme Transitions** — 200ms animated theme switching

### 📱 Mobile (iOS & Android)
- **Mobile Client** — dedicated mobile editor via Capacitor and Monaco
- **Python on Mobile** — run Python directly in-app via Pyodide
- **Offline Python** — Pyodide bundled locally, no internet needed for first run

### 🧩 Extensibility
- **Plugin/Extension System** — built-in extension manager and command execution hooks
- **Idea-to-App Planner** — turn a product idea into a full build plan with architecture and packaging guidance
- **Project Language Auto-detection** — detects dominant language on folder open

---

## 📥 Downloads

| Platform | File | Architecture |
|---|---|---|
| Windows | `Orinex-1.0.0-Windows-x64.exe` | x64 |
| macOS | `Orinex-1.0.0-macOS-universal.dmg` | Intel + Apple Silicon |
| Linux (AppImage) | `Orinex-1.0.0-Linux-x64.AppImage` | x64 |
| Linux (portable) | `Orinex-1.0.0-Linux-x64.tar.gz` | x64 |
| Linux (deb) | `Orinex-1.0.0-Linux-x64.deb` | x64 |

➡️ **[Download from GitHub Releases](https://github.com/ManoharPadul/Orinex/releases)**

---

## 🔑 AI Provider Setup

1. Open Orinex
2. Choose your AI provider in the AI panel
3. Enter your API key
4. Click **Save AI Preferences**

| Provider | Get API Key |
|---|---|
| Claude (Anthropic) | [console.anthropic.com](https://console.anthropic.com/settings/keys) |
| OpenAI | [platform.openai.com](https://platform.openai.com/api-keys) |
| Gemini | [aistudio.google.com](https://aistudio.google.com/app/apikey) |
| Mistral | [console.mistral.ai](https://console.mistral.ai/api-keys/) |
| Groq | [console.groq.com](https://console.groq.com/keys) |
| Cohere | [dashboard.cohere.com](https://dashboard.cohere.com/api-keys) |
| Together | [api.together.xyz](https://api.together.xyz/settings/api-keys) |
| GitHub Models | [github.com/settings/tokens](https://github.com/settings/tokens) |
| Ollama (local) | [ollama.com](https://ollama.com) |

🔐 API keys are stored locally on your machine only.

---

## ⌨️ Keyboard Shortcuts

| Shortcut | Action |
|---|---|
| `Ctrl/Cmd + S` | Save file |
| `Ctrl/Cmd + K` | Command Palette |
| `Ctrl/Cmd + F` | Find in file |
| `Ctrl/Cmd + H` | Find & Replace |
| `Ctrl/Cmd + Shift + F` | Search in all files |
| `Ctrl/Cmd + \` | Split Editor |
| `Ctrl/Cmd + Shift + S` | Toggle Snippet Library |
| `Ctrl/Cmd + L` | Lock screen |
| `Ctrl/Cmd + N` | New file |
| `Ctrl/Cmd + O` | Open file |
| `Ctrl/Cmd + B` | Toggle sidebar |
| `Ctrl/Cmd + Shift + A` | Toggle AI panel |
| `Ctrl + Backtick` | Toggle terminal |
| `Ctrl/Cmd + ,` | Open settings |
| `F11` | Focus Mode |
| `Alt + Z` | Toggle word wrap |
| `Ctrl/Cmd + Shift + Space` | Global AI quick input |

---

## 🎨 Themes

| Theme | Style |
|---|---|
| 🌑 Dark | Default dark |
| ☀️ Light | Clean white |
| 🟡 Monokai | Classic dark colorful |
| 🧛 Dracula | Purple-tinted dark |
| ❄️ Nord | Arctic blue-grey |
| 🌅 Solarized Dark | Warm dark tones |
| 🧁 Catppuccin Mocha | Soft dark pastel |
| 🧁 Catppuccin Frappe | Medium contrast pastel |
| 🧁 Catppuccin Latte | Light pastel |
| 🌃 Tokyo Night | Deep navy city lights |
| 🌈 Ayu Dark | Modern flat dark |
| ✨ Dainty | Minimal elegant |
| 🐙 GitHub Dark | GitHub's dark theme |
| ⚛️ Atom One Dark | Atom editor classic |
| 🚀 Houston | Astro's Houston theme |
| 🦉 Night Owl | Night Owl by Sarah Drasner |
| 🍵 Matcha | Green tea inspired |
| 🛠️ Custom | Build your own |

---

## 🗂️ Supported File Types

**Code:** `py`, `js`, `ts`, `tsx`, `jsx`, `html`, `css`, `java`, `c`, `cpp`, `go`, `rs`, `php`, `sh`, `r`, `swift`, `kt`

**Data:** `json`, `yaml`, `yml`, `xml`, `csv`, `sql`, `toml`, `env`

**Docs:** `md`, `txt`, `docx`, `odt`, `pdf`

**Images:** `jpg`, `png`, `gif`, `webp`, `svg`, `bmp`

**Archives:** `zip`, `rar`, `7z` (with in-app extraction)

---

## 📄 License

MIT License — see [LICENSE](LICENSE)

---

## 👨‍💻 Author

**Manohar Padul**

- 🌐 [manoharpadul.com](https://manoharpadul.com)
- 💼 [LinkedIn](https://linkedin.com/in/manoharpadul-143395182)
- 🐙 [GitHub](https://github.com/manoharpadul)

---

<div align="center">

If Orinex helps you, give it a ⭐ — it helps others find it!

</div>
