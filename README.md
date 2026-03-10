# Minimal Markdown Editor

This repository contains a single-file solution (`minimal_md_editor.html`) that implements a lightweight Markdown editor with a live preview.

## How the solution works

The editor is intentionally minimal and dependency-free. Everything runs directly in the browser using plain HTML, CSS, and JavaScript.

### 1. Layout and UI
- The page uses a two-panel layout:
  - **Left panel:** a `<textarea>` where the user types Markdown.
  - **Right panel:** a preview container that displays rendered HTML.
- The layout is responsive and collapses to one column on smaller screens.

### 2. Live rendering pipeline
- JavaScript listens to the `input` event on the textarea.
- On each keystroke, the app:
  1. Reads the textarea value.
  2. Converts Markdown text into HTML via `markdownToHtml()`.
  3. Updates the preview (`preview.innerHTML`).

### 3. Markdown parsing strategy
- The parser is a small custom implementation that supports common Markdown features:
  - `#`, `##`, `###` headings
  - unordered lists (`- item`)
  - blockquotes (`> quote`)
  - fenced code blocks (```)
  - inline code (`` `code` ``)
  - bold (`**text**`), italic (`*text*`)
  - links (`[label](https://...)`)
- Security is handled with `escapeHtml()` before inline formatting is applied, reducing HTML injection risk.

## Run the project

No build step is needed.

1. Clone/download this repository.
2. Open `minimal_md_editor.html` in your browser.

## License

This project is available under the **MIT License**. See [LICENSE](./LICENSE) for full details.
