# FolderForge — Structure to ZIP

> **Paste a folder tree. Get a ZIP.** A zero-install, browser-based tool that converts any folder structure into a downloadable ZIP file — instantly.

---

## ✨ Features

- **Paste & Go** — Paste any folder tree (with `├──`, `└──`, `│` characters) and instantly generate a real ZIP
- **File Upload** — Drag & drop or upload a `.txt` file containing your folder structure
- **Live Preview** — See a visual tree preview update in real time as you type
- **Smart Parser** — Supports standard tree notation, depth-based indentation, inline comments, and trailing slashes for folders
- **Auto-named ZIP** — The downloaded ZIP is named after the root folder in your structure
- **Stats Bar** — Shows folder and file counts at a glance
- **Load Example** — One-click example to get started immediately
- **No Install Needed** — Runs entirely in the browser; no backend, no dependencies to install

---

## 🚀 Usage

### Option 1 — Live Site

Visit the hosted site and start using it immediately:

```
https://theshanbmr.github.io/folderforge/
```

### Option 2 — Run Locally

1. Clone the repository:
   ```bash
   git clone https://github.com/TheshanBMR/folderforge.git
   cd folderforge
   ```

2. Open `index.html` in any modern browser — that's it!

---

## 🖊️ Supported Input Format

FolderForge understands standard tree notation output (e.g., from the `tree` command). Use the **Load Sample** dropdown to try built-in examples.

---

### 📦 Sample 1 — Economy Bot (Python)

```
economy-system/
├── .env.example
├── .gitignore
├── requirements.txt
├── main.py
├── config.py
├── database/
│   ├── __init__.py
│   ├── models.py
│   ├── db.py
│   └── migrations/
├── services/
│   ├── __init__.py
│   ├── economy.py
│   ├── lottery.py
│   └── shop.py
├── cogs/
│   ├── __init__.py
│   └── economy.py
└── utils/
    ├── checks.py
    └── cooldowns.py
```

---

### ⚡ Sample 2 — Next.js Web App

```
nextjs-app/
├── .env.local
├── .gitignore
├── next.config.js
├── package.json
├── tailwind.config.js
├── tsconfig.json
├── public/
│   ├── favicon.ico
│   └── images/
├── src/
│   ├── app/
│   │   ├── layout.tsx
│   │   ├── page.tsx
│   │   ├── globals.css
│   │   ├── about/
│   │   │   └── page.tsx
│   │   └── api/
│   │       └── route.ts
│   ├── components/
│   │   ├── ui/
│   │   │   ├── Button.tsx
│   │   │   ├── Card.tsx
│   │   │   └── Modal.tsx
│   │   ├── layout/
│   │   │   ├── Header.tsx
│   │   │   ├── Footer.tsx
│   │   │   └── Sidebar.tsx
│   │   └── forms/
│   │       ├── LoginForm.tsx
│   │       └── ContactForm.tsx
│   ├── hooks/
│   │   ├── useAuth.ts
│   │   └── useFetch.ts
│   ├── lib/
│   │   ├── db.ts
│   │   └── utils.ts
│   ├── types/
│   │   └── index.ts
│   └── store/
│       └── index.ts
└── tests/
    ├── components/
    │   └── Button.test.tsx
    └── pages/
        └── home.test.tsx
```

---

**Format Rules:**
- Folders must end with `/`
- Use `├──`, `└──`, and `│` for tree structure (copy directly from `tree` command output)
- Lines starting with `#` are treated as comments and ignored
- Inline comments after names are supported: `main.py  # entry point`

---

## 🛠️ How It Works

1. **Parse** — The input is parsed line by line, extracting depth from tree characters and indentation
2. **Build Paths** — Full relative paths are constructed by tracking a depth-indexed path stack
3. **Preview** — The parsed structure is rendered as an animated visual tree
4. **ZIP** — [JSZip](https://stuk.github.io/jszip/) creates an in-memory ZIP with all folders and empty placeholder files
5. **Download** — The ZIP is streamed as a Blob and downloaded directly in the browser

---

## 📦 Tech Stack

| Technology | Purpose |
|---|---|
| Vanilla HTML / CSS / JS | Core application — zero frameworks |
| [JSZip v3.10.1](https://stuk.github.io/jszip/) | In-browser ZIP generation |
| [JetBrains Mono](https://fonts.google.com/specimen/JetBrains+Mono) | Monospace font |
| [Syne](https://fonts.google.com/specimen/Syne) | Display / heading font |
| Google Fonts CDN | Font delivery |

---

## 📁 Project Structure

```
folderforge/
├── index.html       # The entire application (single file)
└── README.md        # This file
└── icon.png         # Page Logo
```

---

## 🌐 Deployment

This is a single-file static site. It can be hosted on any static hosting platform:

| Platform | Steps |
|---|---|
| **GitHub Pages** | Push `index.html` → Settings → Pages → Deploy from `main` |
| **Netlify** | Drag & drop the folder on [netlify.com/drop](https://app.netlify.com/drop) |
| **Vercel** | `vercel --prod` in the project directory |
| **Any web server** | Copy `index.html` to your server's public directory |

---

## 📄 License

This project is licensed under the **MIT License**.

```
MIT License

Copyright (c) 2026 TheshanBMR

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

1. Fork the repository
2. Create your feature branch: `git checkout -b feature/my-feature`
3. Commit your changes: `git commit -m 'Add my feature'`
4. Push to the branch: `git push origin feature/my-feature`
5. Open a Pull Request

---

<p align="center">Made with AI by <a href="https://github.com/TheshanBMR">TheshanBMR</a></p>
