# Harvard CV Builder

A self-contained, no-backend tool for building a **Harvard-style résumé/CV** — edit it like a document, drag sections to reorder, and export a clean PDF.

Written in plain **HTML + CSS + JavaScript** (no framework, no build step).

## Features

- **Docx-style live preview** — click any text in the résumé preview and type to edit it.
- **Form-based editor** on the left for structured fields (name, contact, jobs, education, skills…).
- **Drag & drop** sections in the editor to reorder them.
- **Section types:** Summary, Experience, Education, Projects, Skills (with groups), Certifications, Awards, Languages, and a free-form Custom section.
- **One-click PDF export** via the browser's print dialog (`Save as PDF`).
- **Save / Load** your CV as a `.json` file so you can keep multiple versions or move between computers.
- **Auto-saves** to your browser as you type.
- **Load sample** — one click fills in Muhammad Rutaab Ali's résumé as a starting template.
- Fully responsive; works on mobile.

## Use it

Just open `index.html` in any modern browser. No install or server required.

If you want to run it from a local server:

```bash
# Python 3
python3 -m http.server 8000
# then visit http://localhost:8000
```

### To deploy

It's a static site — drag the `cv-builder/` folder onto **Vercel**, **Netlify**, **GitHub Pages**, **Cloudflare Pages**, etc. No environment variables, no server.

## How to get the best PDF

1. Click **Download PDF**.
2. In the print dialog:
   - **Destination:** Save as PDF
   - **Margins:** None
   - **Background graphics:** off
3. Save.

The page is formatted to A4 and uses Helvetica/Arial, the classic Harvard résumé look.

## File layout

```
cv-builder/
├── index.html    # markup
├── styles.css    # styling + print/PDF rules
├── app.js        # state, editor, preview, drag & drop, JSON I/O
└── README.md
```

## Harvard-style conventions used

- Name centered at top, contact line below it.
- All-caps section headers with a solid rule underneath.
- Two-column item header: **Role / Title** on the left, **date** right-aligned.
- Organization/school name italicized on the second line.
- Bullets for achievements, not paragraphs.
- Single column, conservative typography, generous whitespace.

## Tips

- Start from the sample (**Load sample**) and just replace the text — it's faster than starting blank.
- In bullet fields, begin each line with `•` to keep the résumé looking tidy.
- Use the `.json` export like a save file; it contains every section and entry.
- All data stays in your browser — nothing is uploaded anywhere.
