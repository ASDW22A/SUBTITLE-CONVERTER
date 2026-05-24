# SUBTITLE CONVERTER

Convert any subtitle format to SRT — no limits, no uploads, all in your browser.

## Supported Formats

| Input | Extension | Notes |
|---|---|---|
| WebVTT | `.vtt` | Strips positioning/headers |
| ASS / SSA | `.ass` `.ssa` | Strips `{\*}` formatting codes, preserves `\N` newlines |
| SMI (SAMI) | `.smi` | Parses `<SYNC>` elements, cleans HTML |
| MicroDVD | `.sub` | Frame→time conversion (configurable FPS, default 23.976) |
| MPL2 | `.mpl2` `.txt` | Same frame-based conversion as MicroDVD |
| oTranscribe | `.txt` | Parses `[HH:MM:SS]` timestamps |
| ZIP | `.zip` | Extracts and processes all supported files inside |

## Features

- Drag & drop or file picker
- Batch conversion (multiple files + ZIPs)
- Download individual SRT files or all as ZIP
- Auto-detects subtitle format from content or extension
- No file size/count limits
- No server uploads — everything stays local
- Neon cyberpunk UI with animated glow effects

## Usage

### Local (HTTP server required)

Because the tool loads JSZip from CDN and uses the File API, you need a local server:

```bash
# Python
python -m http.server 8080

# Node (npx)
npx serve .

# VS Code
# Install "Live Server" extension, right-click index.html → Open with Live Server
```

Then open `http://localhost:8080` in your browser.

### GitHub Pages

1. Create a repository on GitHub
2. Push `index.html` and `README.md` to the default branch
3. Go to Settings → Pages → Source: "Deploy from branch" → main / (root) → Save
4. Your site is live at `https://YOUR_USERNAME.github.io/REPO_NAME`

## Tech Stack

- Pure HTML/CSS/JavaScript (no frameworks)
- [JSZip](https://stuk.github.io/jszip/) library (loaded from CDN) for ZIP handling
- All subtitle parsing done client-side — zero server dependencies

## Sample Files

The `test/` directory contains sample subtitle files in each supported format for testing.

## License

MIT
