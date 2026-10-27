# 🌟 Pragnya AI Desktop Agent — Project Summary

> **A Secure, Autonomous AI Desktop Assistant for Windows**  https://adityasysnet.github.io/ai-desktop-agent-exe/
> Built with Python 3.12, PySide6 (Qt), Groq LLM API, and modern Human-in-the-Loop OS Tooling.

---

## 📌 Overview
**Pragnya** is an intelligent, privacy-first desktop agent designed to automate everyday OS tasks, analyze documents and visual screens, manage system hardware, and streamline workflows through conversational and shortcut-driven interactions.

---

## 🚀 Key Capabilities & Architecture

### 1. 🛠️ 51 Built-in System Tools
- **Filesystem Management:** Safe search, read, write, move, rename, delete, duplicate detection, and ZIP archiving.
- **Operating System Control:**
  - Enumerate visible open application windows.
  - Gracefully close or force-kill applications by Name or PID.
  - Master system volume level (0–100%) and mute toggle.
  - Dynamic desktop wallpaper changer.
  - Display sleep / screen timeout control (AC/DC).
  - Instant workstation lock (`LockWorkStation`).
  - Silent Recycle Bin purge.
  - Media controls (Play/Pause, Next, Previous, Stop).
- **Vision & Multimodal:**
  - Full-screen capture and instant visual analysis.
  - User image file inspection and OCR explanation.
- **Document Readers:** Native parsing for `.pdf`, `.docx`, `.xlsx`, and `.csv`.
- **System Telemetry:** Live battery monitoring, CPU/RAM utilization, and disk health.
- **Automation & Memory:**
  - Scheduled reminders and recurring timers.
  - Persistent SQLite-backed long-term memory (`save_memory`, `recall_memory`).
  - GUI automation (mouse moves, clicks, keyboard typing, hotkeys).
- **Extensibility:** Dynamic user plugin loader (`plugins/`).

---

### 2. 🎨 UI & Design (Claude.ai Aesthetic)
- **Compact Composer Input:** Sleek, rounded prompt card with file attachment support (`+`) and dynamic Groq model badges.
- **Dynamic Navigation Sidebar:**
  - **Date-wise Conversation Grouping:** `Today`, `Yesterday`, `Previous 7 Days`, and `Older`.
  - **Conversation Management:** Right-click context menu to **Rename**, **Pin to Top**, **Export to Markdown (`.md`)**, or **Move to Trash**.
  - **Trash & Archive Bin:** Soft delete with 1-click restore or permanent delete.
  - **Live Hardware Telemetry Widget:** Real-time CPU, RAM, and Battery mini-status display.
  - **Collapsible Sidebar:** Expand/collapse with `Ctrl+B`.
- **Global Quick Launcher:**
  - Lightweight spotlight-style bar toggled anywhere in Windows using `Ctrl+Shift+Space` or `Alt+Shift+Space`.
- **Voice System:**
  - Speech-to-Text input with offline Windows SAPI5 Text-to-Speech playback.

---

### 3. 🛡️ Security & Privacy
- **Human-in-the-Loop Approvals:** Destructive actions (file deletions, process kills, system locking) require explicit user confirmation.
- **Dynamic Path Policy:** Restricts operations to safe user directories (`Desktop`, `Documents`, `Downloads`, `Pictures`, and project workspace).
- **Per-User Isolation:** Chat histories and SQLite databases are stored in `%LOCALAPPDATA%\Pragnya\`, preventing data leaks across systems.
- **No Hardcoded Keys:** Users configure their own Groq API keys via the in-app Settings modal.

---

### 4. 📦 Deployment & Standalone Distribution
- **Standalone Build:** Packaged with PyInstaller into a self-contained Windows executable (`Pragnya.exe`).
- **Release ZIP:** `dist/Pragnya-v1.0.0-windows-x64.zip` (~73.7 MB), ready for zero-dependency execution on any Windows 10/11 machine.

---

## 🔮 Next Roadmap: "Pragnya Code"
- **Dual-Mode Switcher:** Top bar toggle between `💬 Pragnya Chat` and `💻 Pragnya Code`.
- **Integrated IDE:** Multi-tab code editor with syntax highlighting, line numbers, and project tree view.
- **AI Code Composer:** In-line bug fixing, code explanation, and automated unit-test generation.
- **Integrated Terminal Runner:** 1-click script execution with live stdout/stderr console.
