<div align="center">

<img src="https://raw.githubusercontent.com/sssskyds/notepad-ajeet/main/assets/banner.svg" alt="NovaPad Banner" />

# ⚡ NovaPad — Browser Notepad

**A powerful, zero-install code & text editor that runs entirely in your browser.**  
No backend. No dependencies to install. Just open and type.

[![Made with ❤ by Ajeet](https://img.shields.io/badge/Made%20with%20%E2%9D%A4%20by-Ajeet%20Kumar%20Sharma-blueviolet?style=flat-square)](https://github.com/sssskyds)
[![HTML](https://img.shields.io/badge/Built%20with-HTML%2FJS%2FCSS-orange?style=flat-square&logo=html5)](#)
[![CodeMirror](https://img.shields.io/badge/Editor-CodeMirror%205-blue?style=flat-square)](#)
[![License: MIT](https://img.shields.io/badge/License-MIT-green?style=flat-square)](LICENSE)
[![Zero Install](https://img.shields.io/badge/Install-Zero-success?style=flat-square)](#)

[🚀 **Live Demo**](https://sssskyds.github.io/notepad-ajeet/NovaPad-BrowserNotepad.html) &nbsp;·&nbsp;
[📥 **Download**](https://github.com/sssskyds/notepad-ajeet/raw/main/NovaPad-BrowserNotepad.html) &nbsp;·&nbsp;
[🐛 **Report Bug**](https://github.com/sssskyds/notepad-ajeet/issues)

</div>

---

## ✨ Features

### 🗂 Multi-Tab Editing
- Open as many files as you need — each in its own tab
- Unsaved tabs show a **●** dot indicator
- `Ctrl+T` new tab · `Ctrl+W` close tab

### 🎨 Syntax Highlighting
Full syntax highlighting via **CodeMirror 5** for:

| Language | Extension |
|---|---|
| C | `.c` |
| C++ | `.cpp` |
| Java | `.java` |
| Python | `.py` |
| JavaScript | `.js` |
| HTML | `.html` |
| CSS | `.css` |
| Shell / Bash | `.sh` |
| JSON | `.json` |
| Batch | `.bat` |
| Markdown | `.md` |

### 💾 Auto-Save & Session Restore
- **Auto-saves every 2 seconds** after the last keystroke (debounced)
- **Periodic save every 30 seconds** in the background
- Session is saved to **localStorage** — survives browser restarts
- Optional **`.ajs` physical file** auto-save via File System Access API (Chrome/Edge)
- On every restart, NovaPad **restores all tabs, cursor positions, settings, and content** exactly where you left off
- `.ajs` is plain **JSON** — readable in any editor

### 🔍 Find & Replace
- `Ctrl+F` to open inline search bar
- Live **match highlighting** as you type
- Match counter (e.g. `5 matches`)
- **Enter / Shift+Enter** to jump next/previous
- Replace single occurrence or **Replace All**

### ⚙ Editor Power Features
| Feature | Shortcut |
|---|---|
| Save | `Ctrl+S` |
| Save As | `Ctrl+Shift+S` |
| Open file(s) | `Ctrl+O` |
| New tab | `Ctrl+T` |
| Close tab | `Ctrl+W` |
| Find & Replace | `Ctrl+F` |
| Duplicate line | `Ctrl+D` |
| Toggle comment | `Ctrl+/` |
| Auto-complete | `Ctrl+Space` |
| Indent | `Tab` |
| Unindent | `Shift+Tab` |

- **Code folding** — collapse `{}` blocks in the gutter
- **Active line highlight** — subtle highlight on cursor's line
- **Auto-close brackets** — `{`, `[`, `(`
- **Format / Re-indent** — smart auto-indent all lines
- **Sort lines** alphabetically
- **Copy All** — copies full editor content to clipboard
- **Word Wrap** toggle
- **Minimap** — scrollable code overview panel

### 🎨 Themes & Appearance
- 🌙 **Dracula** (dark) — default
- ☀ **Eclipse** (light)
- ◻ **Classic** (CodeMirror default)
- One-click **dark/light mode toggle** synced with system preference
- Font size selector: 12px → 20px
- Font: **JetBrains Mono** (code) + **Inter** (UI)

### 📊 Status Bar
Always shows: `Language` · `Line/Col` · `Selection chars` · `Word count` · `Char count` · `Total lines` · `Last save time`

---

## 🚀 Getting Started

### Option 1 — Just download and open
```bash
# Download the file
wget https://github.com/sssskyds/notepad-ajeet/raw/main/NovaPad-BrowserNotepad.html

# Open in browser
start NovaPad-BrowserNotepad.html   # Windows
open NovaPad-BrowserNotepad.html    # macOS
xdg-open NovaPad-BrowserNotepad.html # Linux
```

### Option 2 — Clone the repo
```bash
git clone https://github.com/sssskyds/notepad-ajeet.git
cd notepad-ajeet
start NovaPad-BrowserNotepad.html
```

> ✅ **No server required.** The entire app is a single self-contained HTML file.

---

## 💾 .ajs Auto-Save File

The `.ajs` session file is a plain JSON file that stores your entire NovaPad session:

```json
{
  "v": 2,
  "savedAt": "2026-04-06T12:00:00.000Z",
  "tabs": [
    {
      "name": "main.c",
      "content": "#include <stdio.h>\n...",
      "mode": "text/x-csrc",
      "cursor": { "line": 5, "ch": 0 }
    }
  ],
  "activeTabId": 1,
  "cfg": {
    "dark": true,
    "fontSize": "14",
    "theme": "dracula",
    "wrap": false
  }
}
```

**To enable physical `.ajs` file saving:**
1. Click the **⚡ Auto-Save** pill in the toolbar
2. A Save dialog opens — navigate to the **same folder as NovaPad** and save `notes.ajs`
3. From now on, every keystroke auto-saves to this file

> ⚠️ Physical `.ajs` file saving requires **Chrome or Edge** (File System Access API).  
> In Firefox, session saves and restores via localStorage — works perfectly.

---

## 🛠 Tech Stack

| Component | Technology |
|---|---|
| Editor engine | [CodeMirror 5](https://codemirror.net/) |
| UI fonts | [JetBrains Mono](https://fonts.google.com/specimen/JetBrains+Mono) + [Inter](https://fonts.google.com/specimen/Inter) |
| Session storage | `localStorage` + IndexedDB + File System Access API |
| Zero dependencies | Pure HTML/CSS/JavaScript |

---

## 📁 File Structure

```
notepad-ajeet/
├── NovaPad-BrowserNotepad.html   ← The entire app (single file)
├── README.md
└── LICENSE
```

---

## 📜 License

MIT © [Ajeet Kumar Sharma](https://github.com/sssskyds)

---

<div align="center">
  <sub>Built with ❤ by Ajeet · Pune, India</sub>
</div>
