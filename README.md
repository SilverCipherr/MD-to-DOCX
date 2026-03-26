# MD2DOCX — Precision Markdown Conversion

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![GitHub Stars](https://img.shields.io/github/stars/SilverCipherr/MD-to-DOCX?style=social)](https://github.com/SilverCipherr/MD-to-DOCX)

**MD2DOCX** is a modern, browser-based tool for converting Markdown documents to Microsoft Word (.docx) format with high fidelity. No server required — everything runs locally in your browser.

![MD2DOCX Preview](https://via.placeholder.com/800x400/0a0a0a/d4af37?text=MD2DOCX+Preview)

## Features

### Core Conversion
- **Full Markdown Support** — Headers, lists, code blocks, tables, blockquotes, and more
- **DOCX Export** — Generates standards-compliant Word documents
- **Equation Support** — LaTeX math rendering with KaTeX integration
- **Syntax Highlighting** — Code blocks with language-specific highlighting

### Customization Options
- **Document Title** — Set custom titles for generated documents
- **Table of Contents** — Auto-generate navigable ToCs
- **Syntax Highlighting** — Toggle code block styling
- **Style Presets** — Multiple formatting themes for output

### User Experience
- **Drag & Drop** — Drop `.md` or `.docx` files directly
- **Live Preview** — See your Markdown rendered in real-time
- **Dark Theme** — Eye-friendly dark interface with gold accents
- **No Uploads** — All processing happens locally in your browser

##  Quick Start

### Option 1: Open Directly
Simply open [`index.html`](index.html) in any modern web browser. No build step, no dependencies, no server.

### Option 2: Local Server
```bash
# Using Python
python -m http.server 8000

# Using Node.js
npx serve .

# Using PHP
php -S localhost:8000
```
Then visit `http://localhost:8000`

##  Usage

### Converting Markdown to DOCX

1. **Enter Markdown** — Type or paste your Markdown content in the left panel
2. **Configure Options** — Set title, enable ToC, adjust styling as needed
3. **Preview** — See live rendered preview on the right
4. **Export** — Click "Generate DOCX" to download your Word document

### Working with Files

- **Load a .md file** — Click the upload area or drag & drop
- **Load a .docx file** — Import existing Word documents for editing
- **Export** — Download your creation as a `.docx` file

### Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| `Ctrl/Cmd + Enter` | Generate DOCX |
| `Ctrl/Cmd + S` | Save current document |
| `Ctrl/Cmd + O` | Open file |

##  Technology Stack

| Category | Technology |
|----------|------------|
| Core | Vanilla JavaScript (ES6+) |
| Document | [docx.js](https://docx.js.org/) |
| Math Rendering | [KaTeX](https://katex.org/) |
| Archive Handling | [JSZip](https://stuk.github.io/jszip/) |
| Fonts | Syne, Space Mono (Google Fonts) |

##  Project Structure

```
├── index.html          # Main application (all-in-one)
└── README.md           # This file

```

##  Configuration Options

### Document Settings
| Option | Default | Description |
|--------|---------|-------------|
| Title | Empty | Document title (metadata) |
| Generate ToC | Off | Include table of contents |
| Syntax Highlighting | On | Style code blocks |

### Style Presets
Choose from multiple visual themes for your exported document.

##  Design Philosophy

MD2DOCX prioritizes:
- **Privacy** — No data leaves your browser
- **Simplicity** — One file, zero dependencies to install
- **Precision** — Accurate conversion that respects Markdown semantics
- **Speed** — Instant preview and export

##  Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing`)
5. Open a Pull Request

##  License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

##  Acknowledgments

- [docx.js](https://docx.js.org/) — For the excellent DOCX generation library
- [KaTeX](https://katex.org/) — For fast math typesetting
- [Google Fonts](https://fonts.google.com/) — For beautiful typography

---

**Made with precision for those who care about their documents.**

**-Prottay**
