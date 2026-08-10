# MD2DOCX — Precision Markdown Conversion

<div align="center">

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![GitHub Stars](https://img.shields.io/github/stars/SilverCipherr/MD-to-DOCX?style=social)](https://github.com/SilverCipherr/MD-to-DOCX)

[![Deployed on Vercel](https://img.shields.io/badge/Deployed%20on-Vercel-black?style=for-the-badge&logo=vercel)](https://md-2-docx.vercel.app)

**Transform Markdown into production-ready documents — entirely in your browser.**  
No server. No uploads. No friction.

[**✦ Try it Live →**](https://md-2-docx.vercel.app)

</div>

---

## ✦ What's New — PDF Export

> **v2.5 introduces direct Markdown → PDF conversion.** No intermediate tools, no server round-trips — your PDF is generated entirely client-side in milliseconds.

The new **output format switcher** lets you choose between DOCX and PDF before converting:

| Feature                       | DOCX        | PDF                  |
| -------------------------------| -------------| ----------------------|
| Output format                 | `.docx`     | `.pdf` (universal)   |
| Template styles               | ✓ 4 presets | — (branded layout)   |
| Page numbers                  | ✓           | ✓                    |
| Page breaks on H1             | ✓           | ✓                    |
| Headings H1–H6                | ✓           | ✓ with size scaling  |
| Bold / Italic / Strikethrough | ✓           | ✓                    |
| Inline code                   | ✓           | ✓ Courier font       |
| Fenced code blocks            | ✓           | ✓ with accent bar    |
| Blockquotes                   | ✓           | ✓ with gold left bar |
| Tables                        | ✓           | ✓ with cell wrapping |
| Bullet & ordered lists        | ✓           | ✓                    |
| KaTeX math                    | ✓ OMML      | placeholder          |
| Hyperlinks                    | ✓           | ✓ underlined         |
| Privacy                       | 100% local  | 100% local           |

### PDF Layout Highlights

- **Branded page header** — every page carries the MD2DOCX wordmark and generation date
- **Gold accent system** — H1 underlines, code block left bars, and bullet dots use the signature gold colour
- **Smart cell wrapping** — table cells word-wrap within their column; row height adjusts automatically
- **Page numbers** — centred footer with `current / total` format on every page

---

## ✦ What's Fixed — DOCX MS Word Compatibility

> **v2.5.1 resolves DOCX file corruption errors in Microsoft Word.**

Previously, the generated DOCX files were missing specific XML namespaces (`w14`, `w15`) and extended properties (`app.xml`) required by modern versions of Microsoft Word (2010, 2013, Office 365). 

- **100% Native MS Word Support** — The DOCX generation engine has been updated to strictly adhere to the `officeDocument` schema, ensuring files open flawlessly in Microsoft Word without triggering the "file is corrupt and cannot be opened" or "recovery" prompts.

---

## Features

### Core Conversion

- **Dual Output Formats** — Export to `.docx` (Microsoft Word) **or** `.pdf` with one click
- **Full Markdown Parsing** — Headings H1–H6, bold, italic, strikethrough, inline code, links
- **Code Blocks** — Fenced blocks with monospace rendering and language label support
- **Tables** — Full GFM table support with header styling and alternating row shading
- **Lists** — Bullet and ordered lists with up to 5 nesting levels
- **Blockquotes** — Rendered with a styled left-border accent
- **Math Equations** — LaTeX rendering via KaTeX (DOCX: full OMML; PDF: placeholder)
- **Horizontal Rules** — Rendered as a styled divider

### DOCX Customisation

- **4 Style Templates** — Academic, Technical, Corporate, Legal
- **Page Breaks** — Auto-insert page breaks before every H1
- **Code Formatting Toggle** — Enable/disable monospace code block styling
- **Blockquote Toggle** — Enable/disable blockquote styling
- **Custom Filename** — Set the output filename before downloading

### User Experience

- **Drag & Drop** — Drop `.md` or `.txt` files directly onto the upload zone
- **Markdown Editor** — Built-in textarea editor with live character/word/section metrics
- **System Log** — Real-time conversion log with progress bar
- **Dark Theme** — Precision dark UI with gold accents and noise texture
- **Zero Dependencies** — One HTML file; all libraries loaded from CDN

---

## Quick Start

### Option 1: Open Directly

```bash
# Clone the repository
git clone https://github.com/SilverCipherr/MD-to-DOCX.git
cd MD-to-DOCX

# Open in your browser — no build step needed
open index.html     # macOS
xdg-open index.html # Linux
start index.html    # Windows
```

### Option 2: Local Server

```bash
# Python
python -m http.server 8000

# Node.js
npx serve .

# PHP
php -S localhost:8000
```

Then visit `http://localhost:8000`

---

## Usage

### Converting to DOCX

1. **Load Markdown** — Drag & drop a `.md` file or type/paste directly in the editor
2. **Configure** — Set template style, toggles, and output filename in the Parameters panel
3. **Select DOCX** — The DOCX tab is active by default
4. **Convert** — Click **Convert to DOCX** (or press `Ctrl + Enter`)
5. **Download** — Click **↓ Download DOCX** when it appears

### Converting to PDF ✦ New

1. **Load Markdown** — Same as above
2. **Select PDF** — Click the **PDF** tab in the Output Format switcher
3. **Convert** — Click **Convert to PDF**
4. **Download** — Click **↓ Download PDF** when it appears

> The PDF tab shares the same page-break and code/blockquote toggles from the Parameters panel.

### Keyboard Shortcuts

| Shortcut | Action |
|---|---|
| `Ctrl + Enter` | Convert (active format) |

---

## Technology Stack

| Category | Technology |
| --- | --- |
| Core | Vanilla JavaScript (ES6+) |
| DOCX Generation | Custom pure-JS engine + [JSZip](https://stuk.github.io/jszip/) |
| PDF Generation | [jsPDF](https://github.com/parallax/jsPDF) 2.5 |
| Math Rendering | [KaTeX](https://katex.org/) + [mathml2omml](https://www.npmjs.com/package/mathml2omml) |
| Fonts | Syne, Space Mono (Google Fonts) |
| Hosting | [Vercel](https://vercel.com) |

---

## Project Structure

```
MD-to-DOCX/
├── index.html      # Complete application (self-contained)
├── favicon.png     # App icon
├── README.md       # This file
└── LICENSE         # MIT License
```

---

## Conversion Parameters

| Option | Applies To | Default | Description |
| --- | --- | --- | --- |
| Automatic Page Breaks | DOCX + PDF | Off | Insert page break before every H1 |
| Preserve Code Formatting | DOCX + PDF | On | Render fenced code blocks with monospace font |
| Render Blockquotes | DOCX + PDF | On | Style `>` quoted text with a left-border accent |
| Output Template | DOCX only | Academic | Visual theme for the Word document |
| Output Filename | DOCX + PDF | `document` | Base name for the downloaded file |

---

## Design Philosophy

- **Privacy first** — No data ever leaves your browser
- **Zero friction** — One file, no install, no login
- **Precision** — Conversion that faithfully respects Markdown semantics
- **Speed** — Instant in-browser generation; no server round-trip
- **Aesthetics** — A tool you enjoy using, not just tolerate

---

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -m 'Add your feature'`)
4. Push to the branch (`git push origin feature/your-feature`)
5. Open a Pull Request

---

## License

MIT — see [LICENSE](LICENSE) for details.

---

## Acknowledgments

- [jsPDF](https://github.com/parallax/jsPDF) — Client-side PDF generation
- [JSZip](https://stuk.github.io/jszip/) — ZIP/DOCX packaging
- [KaTeX](https://katex.org/) — Fast LaTeX math typesetting
- [mathml2omml](https://www.npmjs.com/package/mathml2omml) — MathML → OOXML math conversion
- [Google Fonts](https://fonts.google.com/) — Syne & Space Mono typography

---

<div align="center">

**Made with precision for those who care about their documents.**

*— Prottay*

</div>
