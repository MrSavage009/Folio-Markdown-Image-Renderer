# Folio – Markdown Image Renderer

*Turn markdown into styled, publication‑ready image cards. Auto‑splits long content. Client‑side. No servers.*

---

## The Name

**Folio** is a leaf of a manuscript or book—a discrete, numbered page that holds written text. In scribal tradition, a folio is the fundamental unit of the physical archive: a bounded surface that preserves structure, enforces legibility, and demands careful composition.

This tool transforms your continuous markdown stream into a bound set of folios (image cards). It restores the discipline of the page to the fluidity of digital text—each card is a clean, styled surface ready for presentation, archive, or distribution.

---

## What It Does

**Folio** renders markdown as high‑quality JPEG images. Paste your text, choose a theme and styling mode, and export. If your content exceeds the defined height limit, it is automatically split across multiple pages (folios)—preserving headers, lists, tables, and structural context—so nothing is cropped or lost.

Everything runs in your browser. No uploads, no API keys, no server dependencies.

---

## Why You Would Use This

| Problem | Solution |
| :--- | :--- |
| Design tools (Canva, Photoshop) are slow and inconsistent. | One click from markdown to styled pages. |
| Long text gets cropped or truncated by image generators. | Auto‑splitting preserves all content across multiple cards. |
| Team members use different editors and formatting. | Single markdown source produces consistent, branded output. |
| Screenshots look unprofessional and lack typographic control. | Themed, colour‑coded renders with bracket semantics and math support. |
| Sharing raw LLM outputs (tables, code, nested lists) is messy. | Render AI‑generated markdown directly as structured visual assets. |

---

## Key Features

| Feature | Description |
| :--- | :--- |
| **Full markdown support** | Headers, lists, tables, blockquotes, code blocks, LaTeX math. |
| **7 colour themes** | Orange, Matrix, Cyber, Nord, Dracula, Solar, Crimson. |
| **5 semantic styling modes** | Standard, Alchemist (polarity), Codex (manuscript), Desert (warm/minimal), Legal (case‑file). |
| **Auto‑splitting** | Breaks content across multiple pages; preserves headers and list context. |
| **Bracket highlighting** | Distinguishes `[square]`, `{curly}`, `«guillemets»`, `‹chevrons›`. |
| **Linguistic root detection** | Auto‑highlights 3‑letter patterns (e.g., `q-r-a`) as semantic units. |
| **Math rendering** | Inline (`$...$`) and block (`$$...$$`) LaTeX via KaTeX. |
| **Adjustable dimensions** | Card width (400–1200px), max height (400–3000px). |
| **Resolution multiplier** | 1.0× to 3.4× for high‑DPI exports. |
| **Batch download** | One click to download all generated pages in sequence. |
| **Keyboard shortcut** | `Ctrl+Enter` / `Cmd+Enter` to render. |

---

## Markdown Support

| Element | Supported | Notes |
| :--- | :--- | :--- |
| Headers (`#` – `####`) | ✅ | Distinct styling for H1–H4. |
| Bullet lists (`-`, `*`) | ✅ | Nested lists supported. |
| Numbered lists (`1.`) | ✅ | Sequential numbering preserved across splits. |
| GFM Tables (`\|...\|`) | ✅ | Bordered cells, header background. |
| Code blocks (`` ``` ``) | ✅ | Monospace, background, line‑preserving. |
| Blockquotes (`>`) | ✅ | Left border, italic body, nested support. |
| Inline math (`$...$`) | ✅ | KaTeX rendering. |
| Display math (`$$...$$`) | ✅ | Block‑level equations. |
| `->` and `=>` | ✅ | Rendered as drift (`⟶`) and logic (`⟹`) vectors. |
| 3‑letter roots (e.g., `q-r-a`) | ✅ | Auto‑detected and wrapped as irreducible units. |

---

## How to Use

1. Open `index.html` in any modern browser (Chrome, Firefox, Edge, Safari).  
   *GitHub does not host HTML files as live pages—you must download and open the file locally.*
2. Paste your markdown text into the text area.
3. Select a **theme** and **semantic mode**.
4. Adjust card **width**, **max height**, and **resolution** using the sliders.
5. Click **Render Images** (or press `Ctrl+Enter` / `Cmd+Enter`).
6. Preview each card and download them individually, or click **Download All Images**.

---

## Configuration Options

| Control | Range / Options | Effect |
| :--- | :--- | :--- |
| **Card Width** | 400–1200 px | Horizontal canvas size; affects font scaling and layout density. |
| **Max Height** | 400–3000 px | Vertical threshold that triggers page splits. |
| **Resolution Multiplier** | 1.0× – 3.4× | Scales final image for high‑DPI export (e.g., 2.0× for retina). |
| **Full Artifacts / Cap Length** | Toggle | *Off* = aggressive splitting (word‑by‑word for long paragraphs). *On* = preserves larger blocks with less fragmentation. |

---

## Tech Stack

- **Marked** – Markdown parsing (GFM)
- **KaTeX** – Math rendering
- **html-to-image** – DOM‑to‑image conversion
- **Vanilla JavaScript** – no build tools, no frameworks

All dependencies are loaded from CDN. The entire application is a single HTML file.

---

## Quick Start

```bash
git clone https://github.com/MrSavage009/Folio.git
cd Folio
# Open index.html in your browser
```

Or simply download `index.html` and open it directly.

---

## File Structure

```
.
├── index.html          # Complete application (self‑contained)
└── README.md           # This file
```

---

## License

MIT – use it, modify it, distribute it. No restrictions.

---

## Author

**Wadoed Baykir** – Cognitive Systems Architect, AI Engineer.  
[GitHub](https://github.com/MrSavage009) · [LinkedIn](https://linkedin.com/in/wadoed-baykir)

---

**Questions, issues, or feature requests?** Open a GitHub issue or reach out directly.

---

This README is **fully compatible with GitHub's markdown renderer**. It uses standard GFM tables, code fences with language specifiers, and no raw HTML that could break formatting. Copy this content into your `README.md` file and commit it. The HTML file itself (`index.html`) will not render as a web page on GitHub (it will show the raw source), but that is expected—users must download it to run locally.

If you intend to provide a live demo, you can host the HTML file on GitHub Pages (see the guide in the repo settings). Then you can add a live demo link to the README. Let me know if you need instructions for that.
