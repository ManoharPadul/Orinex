# Orinex

> AI-native development workspace for real-world engineering workflows.

[![Build Status](https://img.shields.io/github/actions/workflow/status/ManoharPadul/Orinex/test-and-build.yml?branch=main&style=for-the-badge&logo=github&label=Build)](https://github.com/ManoharPadul/Orinex/actions)
[![Tests](https://img.shields.io/github/actions/workflow/status/ManoharPadul/Orinex/test-and-build.yml?branch=main&style=for-the-badge&logo=jest&label=Tests)](https://github.com/ManoharPadul/Orinex/actions)
![Version](https://img.shields.io/badge/version-1.0.1-0ea5e9?style=for-the-badge)
![License](https://img.shields.io/badge/license-MIT-22c55e?style=for-the-badge)
![Platforms](https://img.shields.io/badge/platform-Windows%20%7C%20macOS%20%7C%20Linux-1d4ed8?style=for-the-badge)
![Electron](https://img.shields.io/badge/Electron-41-47848F?style=for-the-badge&logo=electron)

<p align="center">
  <img src="/icon.png" alt="Orinex Icon" width="120" />
</p>

<p align="center">
  Built by <strong>Manohar Padul</strong><br />
  <a href="https://manoharpadul.com">manoharpadul.com</a>
</p>

---

# 📸 Screenshots

<img src="Screenshot1.png"/>
<img src="Screenshot2.png"/>
<img src="Screenshot3.png"/>


## Overview

Orinex is a desktop coding workspace with AI assistance, graph intelligence, runtime-aware project generation, safe patch previews, terminal workflows, Git tools, project memory, and local-model support in one app.

It is designed for real projects, not only small demos:

```text
Multi-provider AI routing
Local runtimes: Ollama, llama.cpp, MLX
Existing-project fix/add-feature workflows
Preview-first patch review
Graph + code-search context discovery
Real-world app generation with database/framework support
Cross-platform packaging for Windows, macOS, and Linux
```

---

## v1.0.1 Highlights

### AI and Local Runtime Support

- Unified AI provider routing for cloud and local providers.
- Ollama remains the easiest default local runtime.
- llama.cpp / llama-server support for GGUF models on Windows, macOS, and Linux.
- MLX server support for macOS Apple Silicon.
- Provider-specific health, self-test, and runtime error handling.
- No LM Studio dependency.
- Local runtime setup stays inside AI Settings instead of a blocking provider upsell modal.

### Project Generation

- Real-world project creation across static HTML, Node.js, Vite/React, Python, Flask, FastAPI, PHP, WordPress, Java, Go, C/C++, SQL, Lua, and more.
- Framework-aware generation for Laravel, Symfony, CakePHP, CodeIgniter, AdonisJS, Flask, FastAPI, WordPress, and Node/Express.
- Database-backed app planning for MySQL, PostgreSQL, MongoDB, SQLite, and framework migrations/schema files.
- Better dependency reconciliation for generated Node and AdonisJS projects.
- Safer manifest/config generation with compact output caps for small files.

### Existing Project Editing

- Preview-first existing-project edits.
- Apply Patch uses the exact reviewed patch and does not call the model again.
- Graph and code-search discovery can narrow context before generation.
- User-controlled graph modes: auto, on, off.
- User-controlled code-search discovery modes: auto, on, off.
- Explicit file paths keep highest priority.
- Read-only external references remain read-only.

### Graph Intelligence

- Dependency graph and function graph views.
- 2D and 3D graph modes with theme-aware rendering.
- Large-project graph guardrails and context budgeting.
- macOS graph indexing supports native SQLite rebuilds when copied from Windows paths.
- Graph-scoped edit context avoids sending huge full files to local models by default.

### Memory and Settings

- User memory, project memory, and global runtime-fix memory layers.
- Transparent Memory Inspector for what Orinex sends to the AI.
- Memory safety controls including private mode.
- Global theme/settings persistence.

### UI and Safety

- Glass and solid UI modes with theme-aware menus, dropdowns, graph colors, chat composer, and provider controls.
- Approval menu simplified to Ask for approval and Full access.
- Preview diff and apply behavior aligned across supported edit-capable stacks.
- Static HTML preview avoids unrelated localhost servers and falls back to exact file preview.
- No silent writes for normal existing-project edits.

### Validation

Recent validation included:

- Full Jest suite passing.
- llama.cpp Windows-hosted runtime validation.
- macOS MLX automated generation/edit validation.
- Real-world app and session test ladders.
- Public-ready edge cases for SSE dashboards, GraphQL CRUD, billing webhooks, Docker/MySQL apps, PHP CV/admin DB websites, WordPress booking plugins, Flask queues, and FastAPI OAuth/audit apps.

---

## Supported AI Providers

Cloud providers:

- OpenAI
- Claude / Anthropic
- Gemini
- Mistral
- Groq
- Cohere
- Together AI
- GitHub Models
- GitHub Copilot where configured

Local runtimes:

- Ollama
- llama.cpp / llama-server
- MLX server on macOS Apple Silicon

---

## Supported Project Types

- Static HTML/CSS/JavaScript websites
- Node.js / Express apps
- Vite / React apps
- AdonisJS apps
- Python scripts and CLIs
- Flask apps
- FastAPI apps
- PHP websites with HTML/CSS/JS and database support
- Laravel apps
- Symfony apps
- CakePHP apps
- CodeIgniter apps
- WordPress plugins and themes
- SQL schemas and migrations
- Java, Go, C/C++, Rust, Lua, Bash, JSON, YAML, Markdown, and other single-file outputs

---

## Download

Releases are published at:

[https://github.com/ManoharPadul/Orinex/releases](https://github.com/ManoharPadul/Orinex/releases)

Current local build artifacts:

- `Orinex Setup 1.0.1.exe`
- `Orinex-1.0.1-macOS-arm64.dmg`
- `Orinex-1.0.1-macOS-universal.dmg`
- `Orinex-1.0.1-macOS-x64.dmg`


Note: Windows SmartScreen may warn on unsigned or newly published builds. Use the official GitHub release artifact.

Note: public macOS distribution should be signed and notarized with Apple Developer ID credentials.

---

## Quick Start

1. Open Orinex.
2. Open a project folder.
3. Open Settings -> AI Providers.
4. Choose a provider or local runtime.
5. Run AI Self-Test.
6. Ask Orinex to explain, fix, add a feature, or create a project.
7. Review preview diffs before applying changes.

Recommended local setup:

```bash
# Ollama example
ollama pull qwen2.5-coder:14b
ollama run qwen2.5-coder:14b

# llama.cpp server example
llama-server -m /path/to/model.gguf --host 127.0.0.1 --port 8080 --ctx-size 32768

# MLX server example on macOS Apple Silicon
mlx_lm.server --host 127.0.0.1 --port 8081 --model mlx-community/Qwen2.5-Coder-14B-Instruct-4bit
```
---

## Security

- API key masking and isolated provider settings.
- Local runtimes do not require API keys.
- Terminal allowlist and command safety gates.
- Preview-first patch workflow.
- Reviewed-patch-only apply behavior.
- Private memory mode for projects that should not read/write memory.

---

## License

MIT License.

---

## Support

If Orinex helps you:

- Star the repository.
- Report issues.
- Suggest real-world workflows to test.
