# reMarkable Sync for Obsidian

Sync your reMarkable Paper Pro documents to your Obsidian vault as high-fidelity PDFs.

## Features

- **Direct Cloud Sync** - connects to reMarkable Cloud API
- **High-fidelity PDF rendering** - all 9 pen types with calibrated colors, widths, and opacity
- **Full color support** - 14 colors including shader and highlighter
- **Text rendering** - paragraph styles (headings, bold, bullets, checkboxes, numbered lists)
- **Layered drawing support** - preserves layer ordering
- **Extended pages** - vertically scrolled pages rendered correctly
- **Incremental sync** - only downloads changed documents
- **Auto-sync** - configurable sync interval
- **Annotated PDFs** - merges your annotations with the original PDF background

### Supported pen types

Ballpoint, Fineliner, Marker, Pencil, Mechanical Pencil, Calligraphy Pen, Paintbrush, Highlighter, Shader

## Installation

1. Create the folder `<vault>/.obsidian/plugins/remarkable-sync/`
2. Copy `main.js`, `manifest.json`, and `styles.css` into that folder
3. Open Obsidian Settings > Community Plugins > Enable "reMarkable Sync"
4. Go to the plugin settings and authenticate with your reMarkable account

**Note:** This is a desktop-only plugin (requires Obsidian desktop app).

## Authentication

1. Go to https://my.remarkable.com/device/desktop/connect to get a one-time code
2. Enter the code in the plugin settings (Obsidian Settings > reMarkable Sync)
3. Auth tokens are stored locally at `~/.remarkable-sync/token.json`

## Usage

- Click the tablet icon in the Obsidian ribbon to sync
- Or use the command palette: **reMarkable Sync: Sync now**
- Documents are saved as PDFs in your configured vault subfolder
- Enable auto-sync in settings for hands-free operation

## Configuration

| Setting | Default | Description |
|---------|---------|-------------|
| Sync folder | `reMarkable/` | Subfolder in your vault for synced documents |
| Auto-sync | Off | Sync automatically on a timer |
| Sync interval | 5 min | How often to auto-sync |

## License

Copyright (c) 2026 Tim Dommett

This project is licensed under the [GNU General Public License v3.0](LICENSE). You are free to use, modify, and distribute this software, but derivative works must also be open source under the same license.

### Third-party licenses

This project bundles the following MIT-licensed libraries:
- [pdf-lib](https://github.com/Hopding/pdf-lib) by Andrew Dillon
- [jszip](https://github.com/Stuk/jszip) by Stuart Knightley et al.

See [THIRD-PARTY-NOTICES](THIRD-PARTY-NOTICES) for full license texts.
