# HTML Viewer Plus

An Obsidian plugin for previewing and embedding HTML/MHTML files directly in your vault.

[中文文档](assets/README_zh.md)

## Features

- **Embed preview** — Render HTML inline with `![[file.html]]`
- **Element targeting** — `![[file.html#elementId]]` shows only the specified element
- **Custom sizing** — `![[file.html|400]]` for width, `![[file.html|400x300]]` for width × height
- **Fullscreen / Open externally** — Fullscreen or open in system browser
- **Zoom** — Ctrl + scroll to zoom, adjustable step
- **In-page search** — Ctrl+F to search text within HTML, auto-switches tabs
- **Dark theme sync** — Follows Obsidian dark mode with custom CSS support
- **Hot refresh** — Auto-reload when HTML file changes
- **MHTML support** — Open .mht/.mhtml web archives directly
- **Right-click menu** — Right-click HTML to copy embed/link syntax
- **Scroll guard** — Click to activate scrolling, prevents accidental scroll

## Installation

### Manual

1. Download [main.js](main.js), [manifest.json](manifest.json), [styles.css](styles.css)
2. Create `.obsidian/plugins/html-viewer-plus/` in your vault
3. Copy the three files into that directory
4. Restart Obsidian, go to Settings → Community plugins, enable **HTML Viewer Plus**

### BRAT

Not yet on the community marketplace. Install via [BRAT](https://github.com/TfTHacker/obsidian42-brat):

1. Install the BRAT plugin
2. BRAT Settings → Add Beta Plugin → enter `kuaile1407/html-viewer-plus`
3. Enable the plugin

## Usage

### Embed in notes

```markdown
![[demo.html]]              default width and aspect ratio
![[demo.html|600]]          width 600px
![[demo.html|600x400]]      600px × 400px
![[demo.html#chart]]         show only id="chart" element
```

### Direct open

Click an HTML file in the file explorer to open it in a dedicated view with zoom, search, refresh, and open-externally controls.

### Toolbar

| Button | Embed mode | Direct open |
|--------|-----------|-------------|
| ⛶ | Fullscreen | — |
| ＋ / － | — | Zoom in/out |
| ↺ | — | Reset zoom |
| 🔍 | — | Search |
| ↻ | — | Refresh |
| ↗ | Open externally | Open externally |
| → | Locate in file | — |

### Right-click menu

Right-click on HTML content to see ancestor elements with IDs. Click to copy embed syntax to clipboard.

## Settings

| Option | Default | Description |
|--------|---------|-------------|
| Default width | 100% | Embed area default width |
| Aspect ratio | 4/3 | Supports `4/3`, `16:9`, `1.33` |
| Show toolbar | On | Action buttons on embed view |
| Enable zoom | On | Zoom in direct open mode |
| Zoom step | 0.1 | Zoom increment per scroll |
| Enable search | On | Search in direct open mode |
| Sync dark theme | On | Auto-inject dark CSS |
| Custom dark CSS | — | Appended after default dark styles |
| Custom background | Off | Force HTML body background color |
| Hot refresh | Off | Auto-reload on file change |
| MHTML support | On | Support .mht/.mhtml files |

## Supported formats

- HTML: `.html` `.htm` `.shtml` `.xht` `.xhtml`
- MHTML: `.mht` `.mhtml`

## Support the author

If this plugin helps you, consider buying me a coffee ☕

<img src="assets/支付宝.jpg" width="200"> <img src="assets/微信.jpg" width="200">

## License

[GPL-3.0](LICENSE)
