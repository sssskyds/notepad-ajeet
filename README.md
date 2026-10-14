<div align="center">

# ⚡ NovaPad — Browser Notepad

**A powerful, zero-install code & text editor that runs entirely in your browser.**
No backend. No dependencies to install. Just open and type.

[![Made with ❤ by Ajeet](https://img.shields.io/badge/Made%20with%20%E2%9D%A4%20by-Ajeet%20Kumar%20Sharma-blueviolet?style=flat-square)](https://github.com/sssskyds)
[![HTML](https://img.shields.io/badge/Built%20with-HTML%2FJS%2FCSS-orange?style=flat-square&logo=html5)](#)
[![License: MIT](https://img.shields.io/badge/License-MIT-green?style=flat-square)](LICENSE)
[![Zero Install](https://img.shields.io/badge/Install-Zero-success?style=flat-square)](#)
[![Version](https://img.shields.io/badge/Version-2.2.1-blue?style=flat-square)](#)

[🚀 **Live Demo**](https://sssskyds.github.io/notepad-ajeet/) &nbsp;·&nbsp;
[📥 **Download**](https://github.com/sssskyds/notepad-ajeet/raw/main/index.html) &nbsp;·&nbsp;
[🐛 **Report Bug**](https://github.com/sssskyds/notepad-ajeet/issues)

</div>

---

## ✨ Features

### 🗂 Multi-Tab Editing
- Open as many files as you need — each in its own tab
- Unsaved tabs show a dot indicator
- Drag tabs to reorder · double-click to rename · middle-click / × to close
- New tab: `Ctrl+Alt+N` (browser reserves `Ctrl+T` / `Ctrl+W`, so NovaPad does not use them)

### 🎨 Syntax Highlighting
Built-in lightweight highlighter — no CodeMirror, no CDN. Zero dependencies.

| Language | Extensions |
|---|---|
| Plain text | `.txt`, `.log`, `.csv` |
| Markdown | `.md`, `.markdown` |
| JavaScript | `.js`, `.mjs`, `.ts`, `.jsx` |
| HTML | `.html`, `.htm` |
| CSS | `.css` |
| Python | `.py` |
| JSON | `.json` |
| SQL | `.sql` |
| Shell | `.sh`, `.bash`, `.zsh`, `.bat`, `.cmd`, `.ps1` |
| C / C++ / Java (shared C-like highlighting) | `.c`, `.h`, `.cpp`, `.cc`, `.hpp`, `.java`, `.cs` |
| XML | `.xml`, `.svg` |

> Note: C, C++ and Java share one C-like highlighter. Batch (`.bat` / `.cmd`) is highlighted as Shell.

### 💾 Auto-Save & Session Restore
- Auto-saves to **localStorage** (key `novapad.v2`) after the last keystroke — delay configurable: Instant / 1 s (default) / 3 s in Settings
- On restart, restores **all tabs, content, saved state, language, cursor position, and settings**
- Real files: open / edit / save via File System Access API (Chrome/Edge) or download fallback. Drag & drop files to open (8 MB max per file).
- ⚠️ File links do **not** survive a reload (browser security). After reload, use `Ctrl+S` to re-link a file. Large files (>1 MB) may exceed localStorage — NovaPad warns if auto-save fails.
- Legacy `.ajs` session files (v1 format) can be **opened** to restore a session, but NovaPad no longer auto-saves to `.ajs`.

### 🔍 Find & Replace
- `Ctrl+F` to open inline search bar
- Match case (`Aa`), whole word (`W`), regex (`.*`) toggles
- Match counter (e.g. `3 of 12`)
- **Enter / Shift+Enter** to jump next/previous
- Replace single occurrence or **Replace All**

### ⚙ Editor Power Features
| Feature | Shortcut |
|---|---|
| Save | `Ctrl+S` |
| Download as… | `Ctrl+Shift+S` |
| Open file(s) | `Ctrl+O` |
| New tab | `Ctrl+Alt+N` |
| Find & Replace | `Ctrl+F` |
| Find + focus Replace | `Ctrl+H` |
| Go to line | `Ctrl+G` |
| Duplicate line | `Ctrl+D` |
| Delete line | `Ctrl+Shift+K` |
| Move line up / down | `Alt+↑` / `Alt+↓` |
| Toggle comment | `Ctrl+/` |
| Markdown preview | `Ctrl+Shift+M` |
| Command palette | `Ctrl+K` |
| Zen mode | `F10` |
| Increase / decrease font | `Ctrl+=` / `Ctrl+-` |
| Indent | `Tab` |
| Unindent | `Shift+Tab` |

- **Active line highlight** — subtle highlight on cursor's line
- **Auto-close brackets** — `{`, `[`, `(`, quotes
- **Auto-indent** on Enter (keeps current line indent; splits `{}` pairs)
- **Line tools** — sort A→Z / Z→A, remove duplicates, reverse, join, trim trailing spaces, remove empty lines
- **Case** — UPPERCASE / lowercase / Title Case / Sentence case (requires a selection)
- **Convert** — Format / minify JSON (selection or whole doc), Base64 encode/decode, URL encode/decode (selection required)
- **Copy All**, **Clear document**, **Insert date & time**
- **Multi-cursor & column editing** — `Ctrl+Click` to add a cursor, `Alt+drag` / `Ctrl+Shift+drag` for column selection, `Ctrl+Alt+↑/↓` to add cursor above/below. Type, Backspace, or paste once to edit every cursor.
- **Markdown preview** — live preview + Export as HTML, with LaTeX math (`$...$`, `$$...$$`, `\(...\)`, `\[...\]`) and live Mermaid diagrams (fenced ```mermaid blocks)
- **Tools** — Dictation (speech to text), Read aloud, Print / PDF, Document statistics

> Not in v2: code folding, minimap, and auto-complete were in the old CodeMirror build and were removed in the custom-editor rewrite. They are not in v2.2.1.

### 🎨 Themes & Appearance
- **System** (follows OS) · **Light** · **Dark** · **Sepia** · **Nord**
- Theme button cycles through all five, including System. Settings also lets you pick directly.
- Editor font: Monospace / Sans serif / Serif (system font stacks — no webfont download)
- Font size: 12–22 px in Settings (`Ctrl+=` / `Ctrl+-` adjusts 10–28 px)
- Line height, tab size (2 / 4 / 8), word wrap, line numbers, highlight active line, spell check

### 📊 Status Bar
Shows: `Line/Col` · `Selection` (chars + words, when selected) · `Words` · `Chars` · `~min reading time` · `Stats` · `Language`.
Total lines, paragraphs, sentences, unique words, and average word length live in **Document statistics** (Stats button / Command palette).

---

## 🚀 Getting Started

### Option 1 — Just download and open
```bash
# Download the file
wget https://github.com/sssskyds/notepad-ajeet/raw/main/index.html

# Open in browser
start index.html   # Windows
open index.html    # macOS
xdg-open index.html # Linux
```

### Option 2 — Clone the repo
```bash
git clone https://github.com/sssskyds/notepad-ajeet.git
cd notepad-ajeet
start index.html
```

> ✅ **No server required.** The entire app is a single self-contained HTML file. Open `index.html` directly, or serve it via GitHub Pages.

---

## 🛠 Tech Stack

| Component | Technology |
|---|---|
| Editor engine | Custom `<textarea>` + highlight overlay + built-in tokenizer (no CodeMirror) |
| UI fonts | System stacks: `ui-monospace / SF Mono / Menlo / Consolas` (code) + system UI sans |
| Session storage | `localStorage` only + File System Access API for real files |
| Zero dependencies | Pure HTML/CSS/JavaScript — no build step. LaTeX math renders offline (built-in converter). Mermaid diagrams load the Mermaid library from CDN (jsDelivr) only when a ```mermaid block is previewed or exported; with no internet, the diagram source is shown instead. |

---

## 📁 File Structure

```
notepad-ajeet/
├── index.html   ← The entire app (single file, v2.2.1)
├── README.md
└── LICENSE
```

---

## 📜 Changelog

- **v2.2.1 (2026-10-14)** — `<br>` now renders as a line break in Markdown preview (bare `<br>`, `<br/>`, `<br />`, any case; works in paragraphs, table cells, headings, list items). All other HTML stays escaped, and `<br>` inside code / fenced blocks stays literal.
- **v2.2.0 (2026-10-14)** — LaTeX math in Markdown preview (offline built-in converter: `$...$`, `$$...$$`, `\(...\)`, `\[...\]`, fractions, roots, Greek letters, sub/superscripts, matrices; `$` inside code stays literal; unknown commands degrade to plain text; math content is HTML-escaped so it cannot inject markup) + live Mermaid diagrams from fenced ```mermaid blocks (library loaded from CDN on first use, `securityLevel: strict`, syntax errors fall back to the diagram source with an error note, offline falls back to a code block). Exported HTML carries the math styles and loads Mermaid only when the document contains a diagram.
- **v2.1.0 (2026-10-13)** — Fix release: Markdown-preview XSS via image `alt` (attributes now escaped), theme cycle now includes System, cursor position saved/restored per tab + across reloads, case/Base64/URL tools now require a selection (no more whole-doc surprise), close-tab always confirms unsaved tabs, JSON has no comment syntax (toggle-comment no longer inserts `//`), `.bat` / `.cmd` / `.ps1` map to Shell highlighting, `.ajs` session files can be opened to restore, file-link loss on reload is surfaced, large-file auto-save warning, early-theme script (no light flash), download anchor fixed for Firefox, README rewritten to match the actual app, placeholder `notepad-ajeet.html` removed.
- **v2.0 (2026-07-23)** — Rewrite: dropped CodeMirror, custom tokenizer + highlight overlay, multi-cursor / column select, markdown preview, themes Light/Dark/Sepia/Nord + System, `index.html` rename.
- **v2.0 / v1 (2026-05-22)** — Initial release: CodeMirror 5 build with minimap, folding, `.ajs` auto-save, IndexedDB handle storage.

---

## 📜 License

MIT © [Ajeet Kumar Sharma](https://github.com/sssskyds)

---

<div align="center">
  <sub>Built with ❤ by Ajeet · Pune, India</sub>
</div>
