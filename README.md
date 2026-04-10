# ⚡ Orinex

> A modern AI-powered code editor for desktop and mobile, built for speed, privacy, and real-world workflows.

> Update 2026-04-10: Added Runtime + Upgrade Intelligence panel, refreshed custom icon pipeline (including installer bitmap overrides), and unified Graph 3D controls into a single responsive mini-bar.

[![Build Status](https://img.shields.io/github/actions/workflow/status/ManoharPadul/Orinex/test-and-build.yml?branch=main&style=for-the-badge&logo=github&label=Build)](https://github.com/ManoharPadul/Orinex/actions)
[![Tests](https://img.shields.io/github/actions/workflow/status/ManoharPadul/Orinex/test-and-build.yml?branch=main&style=for-the-badge&logo=jest&label=Tests)](https://github.com/ManoharPadul/Orinex/actions)
![Version](https://img.shields.io/badge/version-1.1.0-0ea5e9?style=for-the-badge)
![License](https://img.shields.io/badge/license-MIT-22c55e?style=for-the-badge)
![Platforms](https://img.shields.io/badge/platform-Windows%20%7C%20macOS%20%7C%20Linux%20%7C%20iOS%20%7C%20Android-1d4ed8?style=for-the-badge)
![Electron](https://img.shields.io/badge/Electron-41-47848F?style=for-the-badge&logo=electron)

![Orinex App Icon](assets/branding/icon-512.png)

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

### 🤖 AI-Powered Features

- 🤖 **Multi-AI support**
	Claude, OpenAI, Gemini, Mistral, Groq, Cohere, Together, GitHub Models, and Ollama (local LLM).

- ✨ **Inline AI Completions**
	Context-aware code suggestions with configurable triggers, caching, and multi-provider support.

- 🧠 **RAG Codebase Chat**
	Index your project and ask questions about your codebase with semantic search and SQLite-backed embeddings.

- 📝 **AI Code Review**
	Automated code review with issue detection, one-click fixes, backup/restore, and ignore patterns.

- 📚 **AI Documentation Generator**
	Auto-generate JSDoc, TSDoc, PyDoc, Rustdoc, and more from your code with style customization.

- 🧪 **AI Test Generator**
	Generate comprehensive unit tests (Jest, Pytest, Rust test, etc.) with edge cases and mocks.

- 💡 **AI Code Explainer**
	Get clear explanations of code at beginner, intermediate, or expert level.

- ✏️ **AI Rename Suggestions**
	Get 5 better name suggestions for variables, functions, and classes based on usage context.

- 🔧 **AI Refactoring**
	Refactor code for cleaner, more maintainable structure while preserving functionality.

- 📐 **AI Type Annotations**
	Add TypeScript-style type annotations to untyped code automatically.

- 🌐 **Local LLM + web refresh**
	Ollama chats can optionally pull fresh web snippets (DuckDuckGo/Wikipedia) into the prompt while keeping generation local.

- 🧭 **Idea-to-app build planner**
	Turn a product idea into a practical build plan with install checklists, platform strategy, architecture support matrix (arm64/x64/x86), packaging outputs, and CI guidance.

- 🔄 **Smart AI provider continuity**
	When a provider hits quota/rate limits, Orinex can switch to another configured provider and continue the same request.

- 💾 **Persistent AI preferences**
	Save provider and model choices (including Ollama/GitHub models) and keep them after restart.

- 🧪 **One-click AI self-test**
	Run an in-app pass/fail validation for provider routing, model availability, connectivity, and prompt round-trip checks.

- 💬 **Chat History**
	Save, search, pin, and export AI conversations with full-text search and statistics.

- 🧭 **Unified AI provider system**
	All 10 providers (Claude, OpenAI, Gemini, Mistral, Groq, Cohere, Together, GitHub Models, GitHub Copilot, Ollama) routed through a single `AIRouter` class. Each provider has its own isolated handler module in `src/modules/ai/providers/`.

- 🎯 **Complexity-based model routing**
	Requests are automatically scored (simple / moderate / complex / expert) and routed to the right model tier. When only Ollama is configured, model selection uses parameter-count heuristics (7B → small, 13B → medium, 34B+ → large).

- 📁 **Project folder selection before file generation**
	Before any AI agent creates files, the app shows a modal to create a new folder or select an existing one. All generated files are written there. Recent folders are saved to `recentProjectFolders` in the store (max 10).

### 🛠️ Developer Tools

- � **Git Log Visual Graph**
	View commit history with branch visualization, cherry-pick, revert, reset, and full commit details with diffs.

- 📦 **Stash Management**
	Save, pop, apply, drop stashes with diff preview and one-click operations.

- 🤖 **AI Commit Message Generator**
	Generate commit messages from staged changes using AI with streaming output.

- 🔍 **Monaco Diff Viewer**
	View side-by-side diffs for commits, stashes, branch comparisons, and working directory changes.

- 🧠 **Runtime + Upgrade Intelligence**
	Analyze runtime and dependency health, generate targeted fix previews, apply selected changes through interactive diff review, and rollback safely using snapshots.

- 🧪 **Interactive Diff Workspace**
	Review generated changes line-by-line with selectable apply before writing files.

- 📊 **Performance Monitor**
	Real-time memory and CPU tracking with tab memory estimates, garbage collection, and warning thresholds.

- �🔍 **Multi-file Search & Replace**
	Project-wide find/replace with regex support, file filters, streaming progress, and backup/restore.

- 🐛 **Integrated Debugger**
	Full debugging support via Debug Adapter Protocol (DAP) for Node.js, Python, and more with breakpoints, step controls, variable inspection, and watch expressions.

- 📋 **TODO/Issue Tracker**
	Scan codebase for TODO, FIXME, HACK, BUG comments with AI-powered fix suggestions.

- 🌐 **LSP Integration**
	Language Server Protocol support for TypeScript, Python, Rust, Go, PHP, HTML/CSS, JSON, YAML with autocomplete, hover, go-to-definition, references, and formatting.

- 📦 **Package Manager UI**
	Unified interface for npm/yarn/pnpm, pip, cargo, and go modules with install, uninstall, update, search, outdated check, and security audit.

- 📁 **Project Templates**
	10+ built-in templates (Node.js, Express, React+Vite, Python, Flask, Rust, Go, Electron, TypeScript Library, HTML/CSS/JS) plus custom template creation and AI-powered customization.

- 🔖 **File Bookmarks**
	Bookmark lines with labels and colors, navigate between bookmarks, import/export, and search.

- 💾 **Workspace Profiles**
	Save and restore complete workspace configurations including open files, cursor positions, layout, settings, and breakpoints.

- ⌨️ **Custom Keybindings**
	Full keyboard shortcut customization with VS Code import, conflict detection, and search.

### 🖥️ Platform Support

- 🖥️ **Desktop apps for all major platforms**
	Native packaging for Windows, macOS, and Linux.

- 📱 **iPhone and Android support**
	Dedicated mobile client powered by Capacitor and Monaco.

- 🐍 **Python execution on mobile**
	Run Python directly in-app via Pyodide.

- 📦 **Offline Python runtime on mobile**
	Pyodide runtime is bundled locally, so first run does not require internet.

### 🧰 Editor Features

- 🧠 **Session continuity**
	Restore last project, open tabs, and active file.

- 🎨 **UI modes + premium variants**
	Switch between Solid and Glass UI modes, with premium variants including Dark Glass, Light Glass, Neon, and Minimal.

- 🪟 **Tahoe-style glass polish**
	Layered blur/saturation/tint/highlight/noise system with tuned dark-glass readability and built-in noise comparison controls.

- 🧩 **Extensions and cloud sync**
	Built-in extension loading and GitHub-backed cloud sync for settings/session snapshots.

- 🗂️ **Project language auto-detection**
	Detects the dominant project language on folder open; unsupported extensions are clearly marked as support-coming-soon.

- 🧰 **Productivity-first editor UX**
	Real-time panel resizing, integrated terminal, themes, and VS Code-style shortcuts.

- 🕸️ **Responsive graph controls**
	Graph 2D/3D controls are unified in one mini-bar with 3D-only focus actions (Exit Focus + Depth 1/2/3) and overlap-safe positioning in sidebar layouts.

---

## 🗂️ Supported File Types

- 🧾 **Text, code, and data files open directly in editor**
	`txt`, `md`, `json`, `yaml`, `yml`, `xml`, `csv`, `sql`, `py`, `js`, `ts`, `tsx`, `jsx`, `php`, `html`, `css`, `java`, `c`, `cpp`, `go`, `rs`, `sh`, `bash`, `r`, `swift`, `kt`, `env`, `toml`.

- 🖼️ **Image preview in-app**
	`jpg`, `jpeg`, `png`, `gif`, `webp`, `bmp`, `svg`.

- 📄 **PDF preview in-app**
	`pdf`.

- 📘 **Document preview in-app (with external-open fallback)**
	`docx`, `odt`, `pages` render live preview in Orinex when extractable; `doc` uses best-effort text extraction.

- 📦 **Archive extraction in-app**
	`zip`, `rar`, `7z` via right-click **Extract Archive** or preview panel **Extract Archive** button.

Notes:
- CSV files are treated as editable plain text files.
- Document preview may differ from original formatting; use **Open Externally** for full-fidelity layout.
- Archive extraction uses bundled `7zip-bin` runtime.

---

## 🆕 Recent Upgrades

### v1.9.2 — Runtime Intelligence + Icon Source Workflow (Apr 10, 2026)

- 🧠 **Runtime + Upgrade Intelligence panel added** in the sidebar with Analyze, summary chips, upgrade plan steps, issue list, and rollback snapshots.
- 🧩 **Interactive diff-first fix flow** for runtime issues: generate fix preview, select exact lines, then apply only approved changes.
- 🛟 **Snapshot-based rollback support** wired to runtime fix applications for safer recovery.
- 🖼️ **Custom icon source directory workflow expanded**:
	- `scripts/generate-icons.js` now auto-detects `my app icons/` by default,
	- supports `--source-dir` / `-d` for explicit icon source folders,
	- writes refreshed desktop assets (`assets/icon.ico`, `assets/icon.icns`, `assets/orinex.icns`, `build/icon.*`) and Linux icon sizes.
- 📦 **NSIS bitmap override support added**:
	- `scripts/generate-nsis-bitmaps.js` now copies `installerSidebar.bmp`, `uninstallerSidebar.bmp`, and `installerHeader.bmp` from the source icon folder when present,
	- otherwise falls back to deterministic generated bitmaps.
- 🕸️ **Graph tab UX cleanup**:
	- removed duplicate 3D toolbar behavior,
	- consolidated controls into the mini-bar,
	- improved sidebar spacing so mini-map and mini-bar remain visible.

### v1.9.1 — Cross-Theme Menu Readability & Contrast Hardening (Apr 8, 2026)

- 🎯 **Dedicated menu tokens added** in `src/styles/tokens.css`:
	- `--menu-bg`, `--menu-text`, `--menu-hover-bg`, `--menu-hover-text`,
	- `--menu-active-bg`, `--menu-active-text`, `--menu-border`, `--menu-disabled-text`.
- 🌗 **Theme-safe menu token mapping expanded**:
	- explicit light-theme menu values,
	- non-light fallback mapping (`[data-theme]:not([data-theme="light"])`) so dark and custom themes inherit contrast-safe menu colors.
- 🧭 **All menu states now token-driven** across menubar and dropdown items:
	- default, hover, active/open, separator, and shortcut text styles.
- 👁️ **Disabled readability improved**:
	- removed opacity-based dimming for disabled menu entries,
	- disabled labels, shortcuts, and submenu arrows now use `--menu-disabled-text` with `opacity: 1`.
- 🖼️ **Menu icon visibility tuned**:
	- menu icons use `filter: none`, balanced base opacity, and stronger visibility on hover/active.
- ✅ **Static verification complete**:
	- CSS diagnostics clean,
	- menu styling rules now reference menu variables instead of hardcoded colors.

### v1.9.0 — Reusable Wizard Engine + Launch Readiness Validation (Apr 8, 2026)

- 🧩 **Reusable wizard engine added** at `src/ui/wizard/wizard.js` with:
	- one-question-per-step modal flow,
	- conditional branching,
	- strict required/custom validation,
	- persistent resume via `localStorage` (`storageKey`),
	- keyboard controls (`Enter`, `Shift+Enter`, `Escape`, `ArrowLeft`),
	- typo normalization (`reactjas` -> `React.js`, `nodejs` -> `Node.js`).
- 🎨 **Dedicated wizard styles added** at `src/ui/wizard/wizard.css` with 80vh modal cap, scroll-safe body, responsive mobile layout, and dark-theme-compatible variables.
- 🧭 **Project Setup Wizard command integrated**:
	- command id: `ai.projectSetupWizard`,
	- AI menu entry + quick action button,
	- structured completion output persisted in `window.lastProjectSetupWizardOutput`.
- 🌿 **Branch-specific setup paths added** for:
	- `React.js` (`react_state`),
	- `Node.js` (`node_runtime`),
	- `PHP` (`php_runtime`).
- 🛡️ **Wizard runtime safety hardening**:
	- added explicit error logging fallback: `console.error("[Wizard Error]", error)`,
	- added non-text focus safety to prevent invalid selection-range crashes on radio controls.

#### Validation executed

- ✅ Functional integrity
	- branch flows validated (React / Node.js / PHP),
	- back/next stability under rapid clicking,
	- persistence and resume after close/reload,
	- required + invalid input blocking,
	- clean completion payload checks (no `undefined` in included keys).
- ✅ UI/UX sanity (automated + static checks)
	- progress indicator correctness,
	- keyboard interaction behavior,
	- modal lifecycle cleanup (no leaked overlay nodes),
	- responsive and overflow-safe CSS rules present.
- ✅ Performance and stability checks
	- open-time smoke test (fast modal initialization),
	- repeated open/destroy lifecycle check,
	- no crashes during high-frequency navigation actions.
- ✅ Packaging / runtime checks
	- `npm run prepare:mac:entitlements` passed,
	- `npm run pack` completed (Windows dir package output),
	- Electron native load check passed: `better-sqlite3:ok`,
	- icon assets validated (`assets/icon.ico` multi-frame + `assets/icon.icns` present).

#### Test commands used

```bash
npm test -- tests/wizard-engine.test.js --runInBand
npm test -- tests/app-router.test.js tests/wizard-engine.test.js --runInBand
npm run prepare:mac:entitlements
npm run pack
```

#### Launch gate decision

- 🚦 **Status: HOLD (recommended before public launch)**
- Reason: automated gates are green, but final visual icon verification on real target environments (Windows taskbar + macOS dock) should still be confirmed manually before declaring full release readiness.

### v1.8.0 — Production Icon Pipeline Refresh

- 🎨 **Icon redesign completed** — refreshed Orinex icon with higher contrast and stronger small-size legibility while preserving brand identity.
- 🪟 **Windows ICO corrected for all critical UI slots** — `build/icon.ico` now includes `16, 20, 24, 32, 40, 48, 64, 128, 256` frames for taskbar, search, explorer, and installer rendering.
- 🍎 **macOS glass icon pipeline added** — packaging now uses `build/icon.icns` generated from a dedicated glass-style render pass for dock/app icon quality.
- 🔧 **Small-size manual optimization** — 16–32 uses simplified high-contrast glyph layers to avoid blur/noise from raw downscaling.
- 📦 **Installer icon wiring hardened** — electron-builder now explicitly uses `build/icon.ico` for `win.icon`, `nsis.installerIcon`, `nsis.uninstallerIcon`, and `nsis.installerHeaderIcon`.
- 🖼️ **Branding PNG deliverables added** — generated `assets/branding/icon-256.png`, `assets/branding/icon-512.png`, `assets/branding/icon-1024.png` (also mirrored to `build/branding/`).
- ✅ **Verified output** — fresh Windows setup executables produced in `dist/` with updated icon resources.

### v1.7.0 — Context Menu & AI Input UX Fixes

- 🖱️ **Duplicate right-click menus removed in editor and explorer** — the secondary native context menu path now skips zones already handled by Orinex custom menus, so only one menu appears.
- 🧭 **Context menus are mutually exclusive** — opening explorer, editor, or breakpoint context menu now auto-hides the others to prevent stacked menus.
- ✂️ **Editor right-click copy/cut/paste hardened** — custom menu actions now preserve selection range and use clipboard API with fallback behavior.
- 📎 **AI panel drag-drop upgraded** — dropping multiple files (including images) into the AI prompt area now attaches them in one flow.
- ✅ **Validation status** — full suite passing after changes (`35/35` suites, `335/335` tests).

### v1.6.0 — Premium UI Modes, Glass Polish & Icon Quality

- 🎛️ **UI Mode system added** — appearance now supports persistent `Solid` and `Glass` modes across startup, settings, and project restore.
- 🌈 **Premium theme variants expanded** — added and wired `dark-glass`, `light-glass`, `neon`, and `minimal` variants on top of base themes.
- 🪟 **Tahoe glass refinement completed** — layered blur/saturation/tint/highlight/noise now applies to scoped glass surfaces with renderer-safe fallback behavior.
- 🧪 **Glass noise debug workflow added** — new runtime `GLASS_DEBUG` toggle + in-settings Noise On/Off comparison cards for visual QA.
- 🖼️ **Homepage logo updated to PNG** — replaced old SVG homepage mark with a PNG logo at the same rendered dimensions.
- 🧊 **Dark-glass contrast corrected** — deepened dark-glass tokens so the UI reads as true dark glass instead of flat gray.
- 🧱 **New texture asset added** — introduced `assets/noise.png` as a 128x128 tiled grain texture for glass surfaces.
- 🧰 **Desktop icon quality improved** — Windows now uses a multi-size ICO (`build/icon.ico`) and macOS packaging uses `build/icon.icns` with runtime fallback at `assets/orinex.icns`.
- ✅ **Validation status** — full suite passing after changes (`35/35` suites, `335/335` tests).

### v1.5.0 — Cross-Platform Compatibility

- ⌨️ **Fixed `Toggle Terminal` accelerator on macOS** — changed `Ctrl+\`` to `CmdOrCtrl+\`` in `menu.js` so the shortcut works correctly on both macOS (`Cmd+\``) and Windows/Linux (`Ctrl+\``).
- 🐧 **Fixed file watcher on Linux** — chokidar now sets `usePolling: true` (with `interval: 100`) when running on Linux, preventing missed file-system events in environments where `inotify` is unavailable (WSL, Docker, some VMs).
- ✅ **All other platform paths verified correct** — Python runtime already uses `py -3` on Windows and `python3`/`python` on Unix; Unix shell selection already checks `$SHELL` → zsh → bash → sh; temp scripts use `.cmd` on Windows and inline `-lc` on Unix (no `chmod` needed); all file paths use `path.join()` throughout.

### v1.4.0 — Theme-Aware Modals (All 17 Themes)

- 🎨 **`.ai-error-reason` hardcoded color fixed** — replaced `color: #f47474` (invisible on light themes) with `color: var(--red)`, which maps to a readable bright red on dark themes (`#f44747`) and a darker accessible red on light themes (`#cd3131`).
- 🏷️ **Semantic badge colors now use CSS variables** — `.badge--create`, `.badge--modify`, `.badge--delete` backgrounds and text colors now use `color-mix(in srgb, var(--green/accent/red) 18%, transparent)` and the theme's own color variables, ensuring readable contrast in all 17 themes including light, solarized, catppuccin-latte, and dainty.
- 🟢 **Diff indicators use theme variables** — `.diff-add` and `.diff-remove` now use `var(--green)` and `var(--red)` instead of hardcoded `#22c55e`/`#ef4444`, adapting correctly to both dark and light themes.
- ✅ **Chat history & code apply dialogs confirmed theme-safe** — both modals already use only CSS variables (`--bg`, `--bg2`, `--bg3`, `--border`, `--text`, `--muted`, `--accent`) and work correctly across all 17 themes without changes.

### v1.3.0 — Fixed Resizable Panels & Toggle Sidebar / AI Panel

- 🔧 **Fixed Toggle Sidebar & Toggle AI Panel** — root cause was that `startSidebarResize` / `startResize` write an inline `style.width`, which has higher CSS specificity than a class rule. The toggle functions now explicitly set `style.width = '0'` when collapsing (overriding any resize-applied inline style) and restore the saved inline width when expanding. Both states are fully persisted to `localStorage`.
- 💾 **Sidebar visibility now persists** — `toggleSidebar()` writes `orinex-sidebar-visible` to `localStorage`; `restorePanelLayout()` reads it on startup and re-collapses the sidebar if needed (with correct inline style).
- 🔒 **`restorePanelLayout` collapse fix** — when AI panel is restored as collapsed (`orinex-ai-panel-visible = 0`), the function now also sets `style.width = '0'` so the inline width saved from a previous resize session doesn't prevent the panel from hiding on next launch.
- ↔️ **Resize handles confirmed correct** — `#sidebar-resizer`, `#resizer`, and `#terminal-resizer` with `startSidebarResize`, `startResize`, and `startTerminalResize` all verified working; `#app.is-resizing` removes transitions during drag so resize is always smooth.

### v1.2.0 — AI Retry with Provider Switching & Bug Fixes

- ♻️ **AI retry with provider switching** — when any AI request fails, the error bubble shows a **Retry** bar with provider and model dropdowns. Pick any configured provider and click Retry to resend the exact same prompt — no re-typing required. Non-retryable errors (invalid key, forbidden, context too long) show an **Open AI Settings** button instead.
- 🔎 **Smart error classification** — errors are classified into human-readable categories (`INVALID_KEY`, `QUOTA_EXCEEDED`, `NETWORK_ERROR`, `SERVER_ERROR`, `MODEL_NOT_FOUND`, `CONTEXT_TOO_LONG`) with actionable hints for each.
- 🔢 **Retry count badge** — each re-attempt increments a visible "Retry N" badge on the error bubble so you can track how many providers have been tried.
- 🎨 **Theme-aware error UI** — error bubbles and retry bars use CSS variables (`--bg2`, `--border`, `--accent`, `--muted`) and work correctly with all 17 themes.
- 🐛 **Fixed `tabs.map is not a function`** — `updatePerfMetrics` now converts the `tabs` plain-object to an array with `Object.values()` before iterating, fixing a crash in the Performance Monitor panel.
- ✅ **202/202 tests passing** after all changes.

### v1.4.0 — AI Context Menu, Terminal AI & Chat History

- 🖱️ **Editor AI Context Menu** — right-click anywhere in the editor to instantly trigger AI actions: Explain Code, Fix Errors, Refactor, Add Comments, Write Tests, Optimize. Works on selection or the full file.
- 🖥️ **Terminal AI Error Detection** — MutationObserver watches terminal output in real time; when an error pattern is detected, a smart banner appears offering "Ask AI" and "Fix with AI" one-click actions.
- 📚 **Chat History Browser** — new clock-icon button in the AI panel header opens a searchable modal listing all saved conversations. Load, delete, and search past chats. Backed by the existing `chat-history:*` IPC layer.
- ⌨️ **AI Commands in Command Palette** — `Ctrl+K` now includes 8 new AI entries: Explain Code, Fix Errors, Refactor, Add Comments, Write Tests, Optimize, Chat History, and Open Memory/Identity.
- ✅ **202/202 tests passing** after all changes.

### v1.3.0 — Unified AI System & Project Folder Manager

- 🤖 **Unified AI subsystem** (`src/modules/ai/`) with `AIRouter`, `ai-providers.js`, `ai-complexity.js`, `ai-attachments.js`, and 10 individual provider handler modules in `providers/`.
- 📡 **`ipc-ai-unified.js`** — new IPC module registering `ai:get-providers`, `ai:refresh-providers`, `ai:chat`, `ai:process-attachment`, `ai:calculate-complexity`.
- 🎯 **Complexity-based routing** — four levels (simple/moderate/complex/expert) used to pick the best provider or model tier automatically.
- 🦙 **Ollama-only intelligent routing** — when Ollama is the sole provider, bins available models by parameter count and selects appropriate tier per request.
- 📁 **Project Folder Manager** (`src/modules/ai/project-folder.js`) — modal-based folder selection before any AI file generation; recent folders persisted to store.
- 🖥️ **Provider status UI** — live model tag, provider icons, and contextual setup prompts for Ollama, GitHub Models, and Groq added to `editor.html`.
- ✅ **202/202 tests passing** after all changes.

### v1.2.0 — Git Workflow & Performance Tools

- 📜 **Git Log Visual Graph** with branch visualization, commit details, and file-level diffs.
- 🍒 **Cherry-pick, Revert, Reset** operations with conflict detection and resolution support.
- 📦 **Stash Management** with save, pop, apply, drop, and diff preview.
- 🤖 **AI Commit Message Generator** with streaming output and multi-provider support.
- 🔍 **Monaco Diff Viewer** for viewing commit diffs, stash diffs, branch comparisons, and working directory changes.
- 📊 **Performance Monitor** with real-time memory/CPU tracking, tab memory estimates, and garbage collection.
- 🔔 **Memory Warning System** with configurable thresholds and status bar indicator.

### v1.1.0 — Developer Tools & AI Enhancements

- 🔍 **Multi-file Search & Replace** with regex support, file filters, streaming progress, and backup/restore.
- 🐛 **Integrated Debugger** via DAP for Node.js, Python with breakpoints, step controls, variables, and watch expressions.
- 📚 **AI Documentation Generator** for JSDoc, TSDoc, PyDoc, Rustdoc with customizable styles.
- 🧪 **AI Test Generator** with Jest, Pytest, Rust test support including edge cases and mocks.
- 💡 **AI Code Explainer** with beginner/intermediate/expert level explanations.
- ✏️ **AI Rename Suggestions** with 5 better name options based on context.
- 🔧 **AI Refactoring** for cleaner, more maintainable code.
- 📐 **AI Type Annotations** to add types to untyped code.
- 🌐 **LSP Integration** for TypeScript, Python, Rust, Go, PHP, HTML/CSS, JSON, YAML.
- 📦 **Package Manager UI** for npm/yarn/pnpm, pip, cargo, and go with search, audit, and updates.
- 📁 **Project Templates** with 10+ built-in templates and custom template creation.
- 🔖 **File Bookmarks** with labels, colors, navigation, and import/export.
- 💾 **Workspace Profiles** to save/restore open files, layout, settings, and breakpoints.
- ⌨️ **Custom Keybindings** with VS Code import, conflict detection, and search.
- ✨ **Inline AI Completions** with context-aware suggestions and multi-provider support.
- 🧠 **RAG Codebase Chat** to index and query your codebase with semantic search.
- 📝 **AI Code Review** with issue detection, one-click fixes, and backup/restore.
- 💬 **Chat History** with save, search, pin, export, and statistics.
- 📋 **TODO/Issue Tracker** to scan for TODO/FIXME/HACK/BUG with AI fix suggestions.

### Previous Updates

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
- 🧠 Added Node.js and React (JSX) language support in editor/run flows.
- 🔎 Added project-level language detection with unsupported-language notice.
- 🗂️ Added broad file-type support including CSV/XML/SQL text workflows.
- 📘 Added live document preview extraction for DOCX/ODT/PAGES with DOC best-effort text preview.
- 📦 Added in-app archive extraction for ZIP/RAR/7Z.
- 🧭 Added AI Idea-to-App planner (quick action + command palette + menu).
- 🧩 Added extension manager and command execution hooks.
- ☁️ Added GitHub-based cloud sync (push/pull).
- 🧭 Added runtime GitHub model discovery from your account token instead of static-only model lists.
- 🛟 Added unknown GitHub model auto-recovery (refresh catalog + retry with valid fallback model).
- 🔐 Added GitHub OAuth Client ID validation (prevents callback-URL/client-ID mixups).
- 🧪 Added one-click AI self-test button with in-app/terminal pass-fail report output.
- 🔄 Added in-app update checker in About (shows current version, latest release, and changelog preview/copy).
- 🐍 Added Python runtime auto-detection for Run Code (supports python3/python/py -3) to avoid macOS ENOENT errors.
- 🩺 Added About-page Python diagnostics button to show detected runtime and platform context.
- 🧾 Added About-page update UX improvements: last-checked timestamp, release asset quick-links, and skip-version action.
- ⬇️ Added packaged-app updater flow with check/download/install + progress reporting.
- 🛡️ Added Project Agent onboarding plus host-enforced allowlisted command runner (lint/test/format/pytest) with per-provider toggles, confirmation prompts (session lock), project-root restriction, execution timeouts, and in-app command audit log.
- 🧷 Added AI code-apply confirmation modes (always/big/never) with per-change backups + one-click rollback, and made the web search toggle sticky across sessions.
- 🧪 Added release-channel control (stable/beta) and persisted skipped-version update preference.

Detailed release history: see [CHANGELOG.md](CHANGELOG.md).

---

## 📥 Downloads

### Pre-built binaries

| Platform | File | Architecture |
|----------|------|-------------|
| Windows Setup | `Orinex-1.1.0-Windows-x64.exe` | x64 |
| Windows Setup (multi-arch) | `Orinex-1.1.0-Windows.exe` | x64 + ia32 |
| Windows Setup (ia32) | `Orinex-1.1.0-Windows-ia32.exe` | ia32 |
| Windows ZIP | `Orinex-1.1.0-Windows-x64.zip` | x64 |
| macOS | `Orinex-1.1.0-macOS-universal.dmg` | Intel + Apple Silicon |
| Linux (portable) | `Orinex-1.1.0-Linux-x64.tar.gz` | x64 |
| Linux | `Orinex-1.1.0-Linux-x64.AppImage` | x64 |
| Linux | `Orinex-1.1.0-Linux-x64.deb` | x64 |
| Linux | `Orinex-1.1.0-Linux-x64.rpm` | x64 |

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

### Run tests

```bash
# Run all tests
npm test

# Run tests in watch mode
npm run test:watch

# Run tests with coverage report
npm run test:coverage
```

### Environment Configuration

Copy `.env.example` to `.env` and fill in your API keys:

```bash
cp .env.example .env
```

See `.env.example` for all available configuration options.

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

### Custom icon pipeline (new)

Use this when you update brand assets and installer visuals.

1. Put icon PNGs in `my app icons/` using names like `64x64.png`, `128x128.png`, `256x256.png`, `512x512.png`, `1024x1024.png`.
2. Optional installer overrides: add `installerSidebar.bmp`, `uninstallerSidebar.bmp`, and `installerHeader.bmp` to the same folder.
3. Generate all app + installer icon assets:

```bash
npm run icons:generate
```

Outputs include:
- `assets/icon.ico`, `assets/icon.png`, `assets/icon.icns`, `assets/orinex.icns`
- `assets/app-icons/linux/<size>x<size>.png`
- `build/icon.ico`, `build/icon.png`, `build/icon.icns`
- `build/installerSidebar.bmp`, `build/uninstallerSidebar.bmp`, `build/installerHeader.bmp`

Use a different source folder if needed:

```bash
node scripts/generate-icons.js --source-dir "path/to/icons"
node scripts/generate-nsis-bitmaps.js --source-dir "path/to/icons"
```

### Installation recommendation

- For distribution on Windows, use the Setup executable from `dist/`:
	- `dist/Orinex-1.1.0-Windows-x64.exe` (recommended)
- Portable/dev validation executable is available at:
	- `dist/win-unpacked/Orinex.exe`

### Linux note for Windows users

- AppImage packaging requires Linux tooling (`mksquashfs`).
- On plain Windows, use `npm run build:linux:x64:portable` for uploadable Linux `.tar.gz`.
- For AppImage, `.deb`, and `.rpm`, use GitHub Actions or a Linux host.

---

## ☁️ Build For Upload (Recommended)

This repository includes CI workflow: `.github/workflows/build-desktop.yml`.

1. Push your code to GitHub.
2. Open the Actions tab.
3. Run Build Desktop Artifacts (manual) or push a tag like `v1.1.0`.
4. Download artifacts: `orinex-windows-x64` and `orinex-linux-x64`.
5. Upload artifacts to your GitHub Release.

Automatic changelog and release notes workflow:

- `.github/workflows/release-changelog.yml` runs on tag pushes (`v*`).
- It generates release notes from commit history between tags.
- It opens a changelog PR and updates GitHub Release body for the pushed tag.

## 🍎 Signed macOS builds

### CI (recommended)

- Workflow: Actions → **Build macOS Signed Artifacts** ([.github/workflows/build-macos-signed.yml](.github/workflows/build-macos-signed.yml)).
- Triggers: manual run or tag push like `v1.1.0`.
- Required GitHub repo secrets:
	- `MACOS_CERTIFICATE_P12_BASE64` — base64 of Developer ID Application `.p12`.
	- `MACOS_CERTIFICATE_PASSWORD` — password for the `.p12` file.
	- `MACOS_CERTIFICATE_NAME` — optional identity override (matches certificate name).
	- `APPLE_ID` — Apple ID used for notarization.
	- `APPLE_APP_SPECIFIC_PASSWORD` — app-specific password for that Apple ID.
	- `APPLE_TEAM_ID` — 10-character Team ID.
- Outputs: signed and notarized `.dmg` + `.zip` uploaded as `orinex-macos-signed` artifacts.

### Local signed build (macOS host)

- Import the same Developer ID certificate into your login keychain or set env vars.
- Run a signed build: `npm run build:mac:signed:universal` (or `:x64` / `:arm64`).
- Required env vars: `CSC_LINK`, `CSC_KEY_PASSWORD`, `APPLE_ID`, `APPLE_APP_SPECIFIC_PASSWORD`, `APPLE_TEAM_ID` (optional `CSC_NAME`).

Create base64 for `MACOS_CERTIFICATE_P12_BASE64` from a `.p12` on macOS:

```bash
base64 -i developer-id.p12 | pbcopy
```

## 🔄 App Updates Across Systems

When you publish a new GitHub Release, all desktop users (Windows/macOS/Linux) can check and update using the same flow:

1. Open **Settings → About**.
2. Click **Check for Updates**.
3. Review latest version and changelog.
4. Click **Open Latest Release** to download your platform build.
5. Optional: click **Skip This Version** to mute repeat prompts for the same latest version.

For troubleshooting local runtime issues:

1. Open **Settings → About**.
2. Click **Python Diagnostics**.
3. Verify detected command (`python3`, `python`, or `py -3`).

If Python is not detected, install Python 3 and/or set `ORINEX_PYTHON_BIN`.

Notes:
- Orinex currently uses GitHub Releases as the cross-platform update source.
- Keep release tags aligned with `package.json` version (for example `v1.1.0`) so version checks are accurate.
- Changelog text shown in app comes from the release notes body on GitHub.
- Auto-download/install updater actions are enabled in packaged builds and disabled in dev mode (`npm start`).
- Release channel can be switched between `stable` and `beta` in About settings.

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

### GitHub Models model selection behavior

- Orinex fetches available GitHub Models dynamically from your authenticated account.
- If a previously selected model is no longer available, Orinex refreshes the catalog and retries with a valid fallback model.
- Static model entries are used only as fallback defaults when live discovery is unavailable.

### GitHub OAuth sign-in (recommended)

Orinex supports Device Flow OAuth sign-in for GitHub Models, so users can connect with a button instead of manually pasting token values.

1. Create a GitHub OAuth App and copy the Client ID.
2. In Orinex AI settings, select GitHub Models.
3. Paste your GitHub OAuth Client ID.
4. Click Sign in with GitHub and complete the browser verification code prompt.
5. Orinex stores the returned token locally and uses it for GitHub Models requests.

Important:
- In Orinex, enter only the OAuth Client ID (`Iv1...`) in the GitHub OAuth field.
- Do not paste callback URL into the Client ID field.

### AI self-test (recommended for local LLM users)

Use **Run AI Self-Test** from AI settings to automatically validate:

1. Provider switch to Ollama
2. Local model list discovery
3. Active model selection
4. Connectivity probe
5. Prompt round-trip probe

Web search for Ollama (optional)
- Enable “Internet refresh” in the chat toolbar when provider = Ollama.
- Only the search query is sent to DuckDuckGo/Wikipedia; generation stays on your machine.

The test prints a pass/fail report in both AI chat output and terminal logs.

### Local LLM agent mode (roadmap)

To let Ollama act more like a coding agent, we plan to expose guarded tools:
- Read-only context: list files, read file ranges, show git diff, and surface failing test logs.
- Safe edits: apply validated patches/diffs with user confirmation and path whitelists.
- Command runner: allowlisted tasks (lint, test, format) with timeouts and streamed logs.
- Prompt schema: structured tool-calls for read/patch/command so the model can request actions explicitly.
- Guardrails: size limits, no writes to node_modules/build outputs, and user approval before any change.

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
| `Ctrl/Cmd + W` | Close file |
| `Ctrl/Cmd + K` | Ask AI |
| `Ctrl/Cmd + ,` | Open settings |
| `Ctrl/Cmd + B` | Toggle sidebar |
| `Ctrl/Cmd + Shift + A` | Toggle AI panel |
| `Ctrl + Backtick` | Toggle terminal |
| `Ctrl/Cmd + F` | Find |
| `Ctrl/Cmd + H` | Find and Replace |
| `Ctrl/Cmd + Shift + F` | Find in Files |
| `Ctrl/Cmd + G` | Go to Line |
| `Ctrl/Cmd + P` | Go to File |
| `Ctrl/Cmd + Shift + O` | Go to Symbol |
| `Ctrl/Cmd + /` | Toggle Comment |
| `Ctrl/Cmd + Shift + D` | Duplicate Line |
| `Ctrl/Cmd + Shift + K` | Delete Line |
| `Alt + Up` | Move Line Up |
| `Alt + Down` | Move Line Down |
| `F5` | Start Debugging |
| `Shift + F5` | Stop Debugging |
| `F9` | Toggle Breakpoint |
| `F10` | Step Over |
| `F11` | Step Into / Fullscreen |
| `Shift + F11` | Step Out |
| `F12` | Go to Definition |
| `Shift + F12` | Find References |
| `Ctrl/Cmd + Space` | AI Suggest |
| `Ctrl/Cmd + Shift + E` | Explain Code |
| `Ctrl/Cmd + Shift + R` | AI Refactor |
| `Ctrl/Cmd + Shift + G` | Generate Docs |
| `Ctrl/Cmd + Shift + H` | Git History Panel |
| `Ctrl/Cmd + Alt + K` | Toggle Bookmark |
| `Ctrl/Cmd + Alt + N` | Next Bookmark |
| `Ctrl/Cmd + Alt + P` | Previous Bookmark |

> 💡 All keybindings are fully customizable via **Settings → Keybindings**. You can also import keybindings from VS Code.

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
│   ├── main.js              # Entry point (modular)
│   ├── preload.js           # Electron preload script
│   ├── editor.html          # Editor UI
│   ├── hardware.js          # Hardware detection
│   ├── core/                # Runtime intelligence analyzers/planner/executor/runtime
│   ├── main/                # Dependency extractor + embedding engine + main-process graph IPC
│   ├── renderer/app/        # App UI logic (graph visualizer, interactive diff workspace, runtime panel)
│   └── modules/             # Modular IPC handlers
│       ├── constants.js     # Shared constants
│       ├── store.js         # Electron-store wrapper
│       ├── utils.js         # Utility functions
│       ├── window.js        # Window management
│       ├── menu.js          # App menu
│       ├── ipc-files.js     # File system handlers
│       ├── ipc-editor.js    # Editor state handlers
│       ├── ipc-terminal.js  # Terminal/code runners
│       ├── ipc-ai.js        # AI provider handlers
│       ├── ipc-runtime-intelligence.js # Runtime analysis/fix/apply/rollback handlers
│       ├── ai-key-store.js  # Provider key presence + key-management helpers
│       ├── ipc-ai-inline.js # Inline AI completions
│       ├── ipc-ai-review.js # AI code review
│       ├── ipc-ai-tools.js  # AI docs/tests/explain/rename
│       ├── ipc-ai-unified.js # Unified AI chat + provider routing (NEW)
│       ├── ipc-rag.js       # RAG codebase chat
│       ├── ipc-chat-history.js # Chat history persistence
│       ├── ipc-todo.js      # TODO/issue tracker
│       ├── ipc-debugger.js  # DAP debugger integration
│       ├── ipc-search.js    # Multi-file search & replace
│       ├── ipc-lsp.js       # Language Server Protocol
│       ├── ipc-packages.js  # Package manager (npm/pip/cargo/go)
│       ├── ipc-templates.js # Project templates
│       ├── ipc-keybindings.js # Custom keybindings
│       ├── ipc-bookmarks.js # File bookmarks
│       ├── ipc-profiles.js  # Workspace profiles
│       ├── ipc-updater.js   # Auto-updater handlers
│       ├── ipc-archive.js   # Archive extraction
│       ├── ipc-github.js    # Git operations + AI commit messages
│       ├── ipc-git-log.js   # Git log, cherry-pick, revert, stash
│       ├── ipc-diff.js      # Diff viewer for Monaco
│       ├── ipc-performance.js # Performance monitoring
│       ├── ipc-memory.js    # Session persistence
│       ├── ipc-shell.js     # Shell utilities
│       └── ai/              # Unified AI subsystem (NEW)
│           ├── ai-router.js         # AIRouter class — provider + model selection logic
│           ├── ai-providers.js      # PROVIDERS metadata, detectProviders(), DEFAULT_MODELS, SINGLE_PROVIDER_MODELS
│           ├── ai-complexity.js     # calculateComplexity(), getComplexityLevel()
│           ├── ai-attachments.js    # processAttachment(), formatAttachmentsForPrompt()
│           ├── project-folder.js    # ProjectFolderManager + registerProjectFolderHandlers()
│           └── providers/           # One module per AI provider, each exports chat()
│               ├── claude.js
│               ├── cohere.js
│               ├── copilot.js
│               ├── gemini.js
│               ├── github-models.js
│               ├── groq.js
│               ├── mistral.js
│               ├── ollama.js
│               ├── openai.js
│               └── together.js
├── tests/                   # Jest test suite
│   ├── hardware.test.js
│   ├── utils.test.js
│   ├── constants.test.js
│   ├── ipc-ai.test.js
│   ├── ipc-archive.test.js
│   ├── ipc-updater.test.js
│   ├── ipc-git-log.test.js
│   ├── ipc-diff.test.js
│   └── ipc-performance.test.js
├── mobile-web/              # Mobile PWA
│   ├── index.html
│   ├── app.js
│   ├── styles.css
│   ├── vendor/
│   │   ├── monaco/          # Bundled Monaco editor
│   │   └── pyodide/         # Bundled Python runtime
│   └── manifest.webmanifest
├── scripts/
│   ├── generate-icons.js
│   ├── generate-nsis-bitmaps.js
│   ├── preload-monaco.js
│   └── preload-pyodide.js
├── assets/
│   ├── icon.png
│   ├── icon.ico
│   ├── orinex.icns
│   ├── noise.png
│   └── orinex-logo.svg
├── .github/
│   └── workflows/
│       ├── test-and-build.yml   # CI: Test + Build
│       └── release.yml          # CD: Auto-release
├── capacitor.config.json
├── jest.config.js
├── .env.example
├── package.json
└── README.md
```

---

## 🏛️ Architecture

```
┌─────────────────────────────────────────────────────────────────┐
│                      Orinex Desktop App                          │
├─────────────────────────────────────────────────────────────────┤
│  ┌─────────────────────────────────────────────────────────────┐│
│  │                    Renderer Process                          ││
│  │  ┌──────────────┐  ┌──────────────┐  ┌────────────────────┐ ││
│  │  │ Monaco Editor│  │  AI Panel    │  │ Integrated Terminal│ ││
│  │  └──────────────┘  └──────────────┘  └────────────────────┘ ││
│  │           │                │                    │            ││
│  │           └────────────────┼────────────────────┘            ││
│  │                            ▼                                 ││
│  │              ┌─────────────────────────┐                     ││
│  │              │    preload.js (IPC)     │                     ││
│  │              └─────────────────────────┘                     ││
│  └─────────────────────────────────────────────────────────────┘│
│                               │                                  │
│                      contextBridge                               │
│                               ▼                                  │
│  ┌─────────────────────────────────────────────────────────────┐│
│  │                     Main Process                             ││
│  │                                                              ││
│  │  ┌────────────┐  ┌────────────┐  ┌────────────────────────┐ ││
│  │  │  main.js   │──│ipc-*.js    │──│  External Services     │ ││
│  │  │ (entry)    │  │ modules    │  │  • AI APIs (Cloud)     │ ││
│  │  └────────────┘  └────────────┘  │  • Ollama (Local)      │ ││
│  │                                  │  • GitHub API          │ ││
│  │  ┌────────────┐  ┌────────────┐  │  • File System         │ ││
│  │  │ store.js   │  │hardware.js │  │  • Child Processes     │ ││
│  │  │ (persist)  │  │ (detect)   │  └────────────────────────┘ ││
│  │  └────────────┘  └────────────┘                             ││
│  └─────────────────────────────────────────────────────────────┘│
└─────────────────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────────────────┐
│                      Orinex Mobile App                           │
├─────────────────────────────────────────────────────────────────┤
│  ┌─────────────────────────────────────────────────────────────┐│
│  │                      WebView                                 ││
│  │  ┌──────────────┐  ┌──────────────┐  ┌────────────────────┐ ││
│  │  │ Monaco Editor│  │   Pyodide    │  │    Service Worker  │ ││
│  │  │  (bundled)   │  │  (Python)    │  │   (offline cache)  │ ││
│  │  └──────────────┘  └──────────────┘  └────────────────────┘ ││
│  └─────────────────────────────────────────────────────────────┘│
│                               │                                  │
│                      Capacitor Bridge                            │
│                               ▼                                  │
│  ┌─────────────────────────────────────────────────────────────┐│
│  │              Native Layer (iOS/Android)                      ││
│  │         • File System  • Storage  • Camera (future)         ││
│  └─────────────────────────────────────────────────────────────┘│
└─────────────────────────────────────────────────────────────────┘
```

---

## � AI System — Technical Reference

This section documents the unified AI subsystem (`v1.3.0+`). It is written for developers and AI assistants who need to understand the codebase well enough to extend or debug it.

---

### Module map

```
src/modules/
├── ipc-ai.js              # Legacy handlers: ai:get-settings, ai:save-settings,
│                          #   ollama-generate, ollama-list-models, github-models-*,
│                          #   github-device-auth, web-search-context
├── ipc-ai-inline.js       # ai:inline-complete, ai:inline-cancel, ai:inline-*
├── ipc-ai-review.js       # AI code review IPC
├── ipc-ai-tools.js        # AI docs / tests / explain / rename
├── ipc-ai-unified.js      # ai:chat, ai:get-providers, ai:refresh-providers,
│                          #   ai:process-attachment, ai:calculate-complexity
└── ai/
    ├── ai-router.js        # AIRouter class — all provider/model selection logic
    ├── ai-providers.js     # PROVIDERS map, detectProviders(), DEFAULT_MODELS,
    │                       #   SINGLE_PROVIDER_MODELS (per-provider model tiers)
    ├── ai-complexity.js    # calculateComplexity(text), getComplexityLevel(score)
    ├── ai-attachments.js   # processAttachment(), formatAttachmentsForPrompt()
    ├── project-folder.js   # ProjectFolderManager + registerProjectFolderHandlers()
    └── providers/          # Each exports: async chat(request, store, win)
        ├── claude.js       #   → { text, model, provider }
        ├── cohere.js
        ├── copilot.js
        ├── gemini.js
        ├── github-models.js
        ├── groq.js
        ├── mistral.js
        ├── ollama.js
        ├── openai.js
        └── together.js
```

---

### IPC channels — Unified AI

| Channel | Type | Payload | Returns |
|---|---|---|---|
| `ai:get-providers` | invoke | — | Array of `{ id, name, available, models, hasKey }` |
| `ai:refresh-providers` | invoke | — | Same as above (forces cache refresh) |
| `ai:chat` | invoke | `{ prompt, model?, provider?, history?, attachments?, webContext?, stream? }` | `{ text, model, provider }` |
| `ai:process-attachment` | invoke | `{ filePath }` | `{ content, mimeType, name, size }` |
| `ai:calculate-complexity` | invoke | `{ prompt }` | `{ score, level, suggestedRouting }` |

These channels are registered by `registerUnifiedAIHandlers(ipcMain, win, store)` in `ipc-ai-unified.js`. A singleton `AIRouter` instance is created on first call and reused.

---

### AIRouter — routing decision order

```
Request arrives at ai:chat
│
├─ request.provider set explicitly?
│   └─ YES → use that provider directly
│
└─ NO → check store.get('aiAutoSwitch')
    ├─ false → use store.get('aiProvider') + store.get('aiModel') as-is
    │
    └─ true  → score prompt with calculateComplexity()
                │
                ├─ Multiple providers available?
                │   └─ Iterate PROVIDER_PRIORITY, pick first available
                │      whose tier supports the complexity level
                │
                ├─ Single provider available?
                │   └─ Look up SINGLE_PROVIDER_MODELS[provider][level]
                │      to pick the best model within that provider
                │
                └─ Ollama only?
                    └─ categorizeOllamaModels(modelList)
                       → bins by param count (7b→small, 13b→medium, 34b+→large)
                       → selectOllamaModelByComplexity(bins, level)
```

**Complexity levels** (from `ai-complexity.js`):

| Level | Score | Typical requests |
|---|---|---|
| `simple` | 0–3 | Single-line answers, explain a variable |
| `moderate` | 4–6 | Write a function, explain a concept |
| `complex` | 7–8 | Multi-file refactors, architecture questions |
| `expert` | 9–10 | System design, multi-step agent tasks |

**Provider priority order** (`PROVIDER_PRIORITY` in `ai-router.js`):
`ollama` → `github` → `github-copilot` → `openai` → `claude` → `gemini` → `mistral` → `groq` → `cohere` → `together`

---

### Provider handler interface

Every file in `src/modules/ai/providers/` must export:

```js
/**
 * @param {{ prompt: string, model: string, history: Array, attachments: Array,
 *           webContext: string, stream: boolean }} request
 * @param {import('electron-store')} store
 * @param {Electron.BrowserWindow} win
 * @returns {Promise<{ text: string, model: string, provider: string }>}
 */
async function chat(request, store, win) { ... }

module.exports = { chat };
```

Provider-specific keys read from store:

| Provider | Store key for API key |
|---|---|
| claude | `anthropicKey` |
| openai | `openaiKey` |
| gemini | `geminiKey` |
| mistral | `mistralKey` |
| groq | `groqKey` |
| cohere | `cohereKey` |
| together | `togetherKey` |
| github / github-copilot | `githubToken` |
| ollama | `ollamaUrl` (default `http://localhost:11434`) |

---

### Project Folder system

`src/modules/ai/project-folder.js` — ensures AI agents always write files to a user-chosen location. Registered via `registerProjectFolderHandlers(ipcMain, win, store)` called from `main.js`.

#### IPC channels

| Channel | Type | Description |
|---|---|---|
| `project-folder:prompt` | **push** main→renderer | Triggers the modal in `editor.html`; sent via `win.webContents.send()` |
| `project-folder:response` | **send** renderer→main | Carries the user's result; received by `ipcMain.once()` inside `promptForProjectFolder()` |
| `project-folder:select-existing` | invoke | Native directory picker; returns `{ path }` or `{ canceled: true }` |
| `project-folder:create` | invoke `{ parentPath, folderName }` | Sanitises name, calls `fs.mkdir({ recursive: true })`; returns `{ path }` |
| `project-folder:browse-parent` | invoke | Native directory picker for parent folder selection |
| `project-folder:get-recent` | invoke | Returns `store.get('recentProjectFolders')` — array of `{ path, name, lastUsed }`, max 10 |
| `project-folder:get-default-location` | invoke | Returns first accessible path from: `~/Projects`, `~/Documents/Projects`, `~/Code`, `~/Development`, `~/Documents` |
| `project-folder:get-current` | invoke | Returns `manager.currentProjectPath` |
| `project-folder:set-current` | invoke `{ path }` | Sets current path + prepends to recent list |

#### Renderer API (`window.electronAPI.projectFolder` in `preload.js`)

```js
projectFolder.prompt(options)                         // triggers modal
projectFolder.selectExisting()                        // native open dialog
projectFolder.create({ parentPath, folderName })      // mkdir
projectFolder.browseParent()                          // native open dialog (parent)
projectFolder.getRecent()                             // recent folders array
projectFolder.getDefaultLocation()                    // best default path
projectFolder.getCurrent()                            // active project path
projectFolder.setCurrent(path)                        // set + add to recent
projectFolder.respond(result)                         // internal: send answer to main
projectFolder.onPrompt(callback)                      // register listener for push
projectFolder.removePromptListener()                  // remove listener
```

#### Modal flow (sequence diagram)

```
main process                     renderer (editor.html)
─────────────────────────────────────────────────────────
promptForProjectFolder(options)
  │
  ├─ win.webContents.send('project-folder:prompt', options)
  │                                │
  │                                ├─ onPrompt(cb) fires
  │                                ├─ showProjectFolderModal(options) — async
  │                                ├─ user picks create/existing + confirms
  │                                ├─ pfConfirm() creates folder or uses existing
  │                                ├─ openFolderByPath(path)   ← existing global fn
  │                                └─ projectFolder.respond({ success, path })
  │                                         │
  │                                         └─ ipcRenderer.send('project-folder:response', result)
  │
  ├─ ipcMain.once('project-folder:response') resolves
  └─ returns { success: true, path } or { canceled: true }
```

**Important**: `ipcMain.once` is used (not `on`) so the listener is consumed after one response. If the modal is closed without responding, the promise will hang until the renderer calls `respond()` or the app is restarted.

**Folder name sanitisation**: `/[<>:"/\\|?*\x00-\x1f]/g` → `_`

**Store key**: `recentProjectFolders` (array, max 10, newest first)

---

### editor.html — key globals added in v1.3.0

| Symbol | Type | Purpose |
|---|---|---|
| `showProjectFolderModal(options)` | `async function` | Displays the `#project-folder-modal` overlay; returns a Promise |
| `pfToggle(type)` | function | Switches between `create` / `existing` radio UI |
| `pfUpdatePreview()` | function | Updates the full-path preview string in the modal |
| `pfBrowseParent()` | async function | Opens native dialog to pick parent for new folder |
| `pfSelectExisting()` | async function | Opens native dialog to pick existing folder |
| `pfConfirm()` | async function | Validates choice, creates folder if needed, resolves Promise |
| `pfCancel()` | function | Closes modal, resolves `{ canceled: true }` |
| `updateAIStatus(provider, model)` | function | Updates the `.ai-model-tag` chip in the toolbar |
| `setupProviderSwitchedListener()` | function | Listens for `ai:provider-switched` IPC event from main |
| `showOllamaSetupPrompt()` | function | Contextual modal guiding Ollama install + first model pull |
| `showNoProviderPrompt()` | function | Modal shown when no provider is configured |

---

### Debugging common problems

| Symptom | Where to look | What to check / fix |
|---|---|---|
| `ai:chat` throws or returns empty | `ipc-ai-unified.js`, `ai-router.js` | Call `ai:get-providers` first. Verify at least one provider has `available: true` and `hasKey: true`. Check `store.get('aiProvider')` and `store.get('aiKey')` / provider-specific key. |
| Ollama routes to wrong model | `ai-router.js` `categorizeOllamaModels()` | Models are bucketed by size suffix in their name (`7b`→small, `13b`→medium, `34b`/`70b`→large). A model with no numeric suffix falls into `medium`. Run `ollama list` to verify model names. |
| Project folder modal never appears | `editor.html`, `preload.js` | Check `window.electronAPI.projectFolder.onPrompt` is registered (added right after `setAboutUpdateUiStatus` in editor.html). Check `win.webContents.send('project-folder:prompt', ...)` is being called from `project-folder.js`. |
| `project-folder:response` never resolves | `project-folder.js` `promptForProjectFolder()` | The renderer must call `projectFolder.respond(result)` — this is a `send` not `invoke`. If the app hot-reloads mid-modal, the `once` listener is gone; reopen the modal to get a new one. |
| Provider availability shows all `false` | `ai-providers.js` `detectProviders()` | `detectProviders()` reads store keys synchronously. Ensure keys are saved with `ai:save-settings`. For Ollama, it also pings the `ollamaUrl`; if Ollama isn't running, Ollama will show unavailable. |
| Tests fail after adding a new IPC handler | `tests/ipc-ai.test.js` | Jest mocks `ipcMain.handle`. New handlers must not call `store.set` at registration time. Verify the handler is added inside `registerXxxHandlers()` and not at module load. |
| AI status tag not updating in toolbar | `editor.html` `updateAIStatus()` | Check `setupProviderSwitchedListener()` is called on DOMContentLoaded. The main process must emit `ai:provider-switched` with `{ provider, model }` after routing. |
| `SINGLE_PROVIDER_MODELS` returns undefined | `ai-providers.js` | The map covers 9 providers × 4 tiers. Add your new provider with all four keys: `simple`, `moderate`, `complex`, `expert`. |

---

## �🤝 Contributing

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
# orinex-source
