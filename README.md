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

## License

MIT
