# Experiential AI Agent

ChatGPT-style browser UI for the Experiential Labs OpenAI-compatible gateway.

## GitHub Pages / Browser mode

The site uses the `gpt-6-astra` model by default and lets you enter an Experiential Labs API key in **Settings**. The key is stored in this browser's **IndexedDB**, not in the GitHub repository, URL, or localStorage. Each browser/device can have its own key.

**Security:** IndexedDB is browser storage, not a password vault. Anyone with access to the browser profile may potentially use the key. Use a limited/scoped key where possible and clear it when finished.

GitHub Pages hosts static HTML/CSS/JavaScript and does not run Python server-side. If the Experiential gateway blocks browser CORS requests, use the full Termux/Windows Python backend instead.

## Local agent

The full Termux/Windows agent includes the Python backend, document tools, calculator/system tools, optional shell tools, and library support. The packaged project created for this chat can be downloaded and run locally.

Never commit an actual API key to GitHub. Set `EXPLABS_API_KEY` as an environment variable for local backend use.
