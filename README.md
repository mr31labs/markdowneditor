# Minimal Markdown Editor

An elegant, Apple-inspired Markdown editor with built-in AI writing tools, real-time previewing, and secure local file encryption. 

## Features

- **Apple-Inspired Design:** Soft typography, glassmorphism (`backdrop-filter`) UI elements, and a clean interface that supports both Light and Dark modes based on your system preferences.
- **View Toggles:** Easily switch between **Edit** (Markdown Only), **Split** (Side-by-side Editor & Preview), and **Preview** (Rendered Output Only) modes.
- **Floating Dock Toolbar:** Quick access to Markdown formatting shortcuts (Bold, Italic, Link, Code), AI tools, and Export options.
- **Multi-Provider AI Integration:** Highlight text and immediately Rewrite, Improve, Summarize, or Review it using the LLM of your choice (Gemini [Default], OpenAI, Claude, DeepSeek, or Perplexity).
- **Secure Encrypted Key Export:** For enhanced security, your AI provider API key is saved with AES encryption using `crypto-js`. Upon saving, you receive a downloaded `.enc` file protected by a password of your choice, so your key is never stored in plain text.
- **Exports:** Instantly save your markdown as a raw `.md` file, or render it exactly as it appears in the styled preview to a high-quality `.pdf` document.

## How to run

Simply open `minimal_md_editor.html` in your web browser! No local server or build pipeline is required.

## API Key Setup (Important)

In order to use the AI tools (the sparkles and magic wand icons in the dock), you **must provide your own API key** for your selected AI provider.

1. Click the **Settings Gear** icon in the bottom dock.
2. Select your provider (e.g., Gemini).
3. Paste your API key into the input field.
4. Click **Save & Encrypt**. You will be prompted to create a password.
5. A `.enc` file containing your encrypted key will be downloaded to your computer.

> **Note:** Do NOT commit your `.enc` files or raw API keys to GitHub. The repository includes a `.gitignore` to prevent uploading `.enc` files, but you should always keep your credentials secure.

If you return to the editor later, you can click **Choose .enc File**, select the file from your computer, and enter your password to instantly restore your API key.

## Dependencies (Loaded via CDN)
- [Lucide Icons](https://lucide.dev/) (UI Icons)
- [html2pdf.js](https://ekoopmans.github.io/html2pdf.js/) (PDF Exporting)
- [CryptoJS](https://cryptojs.gitbook.io/docs/) (AES encryption for API Key backup)
