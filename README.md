<div align="center">

# ✨ Experiential AI Agent

### A beautiful ChatGPT-style AI workspace powered by the Experiential Labs gateway.

<p>
  <img src="https://img.shields.io/badge/UI-ChatGPT--style-111827?style=for-the-badge" alt="ChatGPT-style UI">
  <img src="https://img.shields.io/badge/Model-GPT--6%20Astra-7c3aed?style=for-the-badge" alt="GPT-6 Astra">
  <img src="https://img.shields.io/badge/API-OpenAI--compatible-2563eb?style=for-the-badge" alt="OpenAI compatible API">
  <img src="https://img.shields.io/badge/Storage-IndexedDB-059669?style=for-the-badge" alt="IndexedDB">
</p>

<p>
  <strong>Bring your own Experiential Labs API key, keep it tied to your browser, and chat with GPT-6 Astra from a clean, modern interface.</strong>
</p>

</div>

---

## 🚀 What is this?

**Experiential AI Agent** is a lightweight AI workspace built around the OpenAI-compatible Experiential Labs gateway.

It is designed to feel familiar to ChatGPT users while remaining simple enough to run from a browser, Termux, Windows, or a local Python environment.

The project has two modes:

| Mode | Best for | Backend |
|---|---|---|
| 🌐 **Browser Mode** | GitHub Pages / quick access | Direct API connection from the browser |
| 💻 **Local Agent** | Termux / Windows / advanced tools | Python backend |

---

## ✨ Highlights

### 💬 ChatGPT-style experience

- Clean dark interface
- Responsive desktop and mobile layout
- New-chat workflow
- Conversation history
- Markdown rendering
- Code blocks
- Typing animation
- Tool/activity indicators
- Modern message composer

### 🔐 Browser-specific API key

The browser version includes a dedicated **API Key** section in Settings.

Your key is:

- 🔒 Stored in **IndexedDB** for that browser origin
- 🚫 Not committed to this repository
- 🚫 Not placed in the page URL
- 🚫 Not stored in `localStorage`
- 🧹 Removable from Settings at any time

This means different browsers/devices can use different API keys without changing the GitHub repository.

> ⚠️ **Security note:** IndexedDB is persistent browser storage, not a secure password vault. Someone who has access to the browser profile or can execute trusted JavaScript in the same origin may potentially access the key. Never publish your API key in source code, screenshots, issues, or commits.

---

## 🧠 Powered by Experiential Labs

The project uses the Experiential Labs OpenAI-compatible API gateway.

**Default configuration:**

```text
Base URL: https://api.experientiallabs.ai/v1
Model:    gpt-6-astra
```

The model slug used by the application is **`gpt-6-astra`**.

---

## 🌐 Browser / GitHub Pages

The browser build is intended to be deployable as a static website.

### Quick setup

1. Open the repository on GitHub.
2. Go to **Settings → Pages**.
3. Select deployment from the `main` branch.
4. Open the generated GitHub Pages URL.
5. Open **Settings** inside the app.
6. Enter your Experiential Labs API key.
7. Save the key.
8. Test the connection.
9. Start chatting.

GitHub Pages provides static hosting; it does **not** execute the Python backend server-side. If the Experiential gateway does not allow browser CORS requests, use the local Python agent instead. citehttps://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site

---

## 💻 Local Agent

The full local version includes a Python backend and additional capabilities such as:

- 🧮 Calculator tools
- 🖥️ System information
- 📁 Workspace file operations
- 📚 Document/library support
- 🔎 Document search
- 🌍 Web search support
- 🐚 Optional shell execution
- 📎 File uploads
- 📄 PDF / DOCX / XLSX / PPTX / CSV / TXT and other document handling

For local use, keep your API key outside the repository:

### Linux / Termux

```bash
export EXPLABS_API_KEY="YOUR_API_KEY"
python app.py
```

### Windows PowerShell

```powershell
$env:EXPLABS_API_KEY="YOUR_API_KEY"
python app.py
```

Never replace `YOUR_API_KEY` with a real key inside this README.

---

## ⚙️ Environment Variables

| Variable | Default | Purpose |
|---|---|---|
| `EXPLABS_API_KEY` | — | Experiential Labs API key |
| `EXPLABS_BASE_URL` | `https://api.experientiallabs.ai/v1` | API gateway URL |
| `EXPLABS_MODEL` | `gpt-6-astra` | Model slug |
| `HOST` | `127.0.0.1` | Local server host |
| `PORT` | `8080` | Local server port |
| `AGENT_ALLOW_SHELL` | `0` | Enable/disable shell tool |
| `AGENT_SHELL_TIMEOUT` | `30` | Shell command timeout |

---

## 🛡️ Security First

Please follow these rules when using the project:

- ❌ Never commit API keys.
- ❌ Never paste API keys into public issues or screenshots.
- ❌ Never hard-code credentials into JavaScript.
- ✅ Use the browser Settings field for browser mode.
- ✅ Use environment variables for local backend mode.
- ✅ Rotate a key immediately if it becomes exposed.
- ✅ Disable shell access unless you actually need it.

---

## 🗂️ Project Structure

```text
experiential-ai-agent/
│
├── index.html                 # Browser / GitHub Pages UI
├── README.md                  # Project documentation
├── .nojekyll                  # GitHub Pages helper
│
└── local-agent/               # Optional local Python implementation
    ├── app.py
    ├── requirements.txt
    └── static/
        └── index.html
```

> The exact local-agent files may vary depending on which packaged version you use.

---

## 🧪 Example

Once connected, you can ask things like:

```text
Explain VLANs like I'm a beginner.

Calculate 12345 × 67.

Write a Python script to monitor a network interface.

Summarize this document.

Help me troubleshoot a Windows networking problem.
```

---

## 🛠️ Technology

| Layer | Technology |
|---|---|
| Frontend | HTML / CSS / JavaScript |
| AI Gateway | Experiential Labs |
| API Style | OpenAI-compatible |
| Browser Storage | IndexedDB |
| Local Backend | Python |
| Hosting | GitHub Pages / Local machine |

---

## 🌟 Why this project?

The goal is simple:

> **A personal AI interface that feels like ChatGPT, but gives you control over the API connection and where the agent runs.**

Use it in a browser when you want simplicity. Run the Python agent locally when you want tools, files, and deeper system integration.

---

## 📌 Current Status

**🟢 Active development**

The project is intentionally modular so more agent tools, providers, models, and integrations can be added later.

---

## 📜 License

No license has been specified yet. Until a license is added, assume the repository's code is **all rights reserved** and do not redistribute it as if it were open-source licensed.

---

<div align="center">

### Built for experimentation. Designed for everyday AI work. ⚡

**Experiential AI Agent** · GPT-6 Astra · Browser + Local

</div>
