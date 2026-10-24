# MarcLVR.github.io

Personal site and blog of Marc Pérez Bernús: Project Manager with an MSc in Data Science, focused on machine learning for risk, Agentic AI, Responsible AI and data governance.

**Live site:** https://marclvr.github.io

## What's here

| Page | What it is |
|---|---|
| [`index.html`](index.html) | Portfolio: about, capabilities, selected projects, writing, skills matrix, experience and contact |
| [`blog/index.html`](blog/index.html) | Blog index |
| [`blog/federated-learning/`](blog/federated-learning/index.html) | *Federated learning: training a model without collecting the data* |
| [`blog/mixture-of-experts/`](blog/mixture-of-experts/index.html) | *Mixture of Experts: huge models that only use a fraction of themselves* |

Each blog post can be read at two levels, **General** (visual, no maths) and **Technical** (formulas, algorithms, references), switched from the top bar. Posts include interactive diagrams, and every page supports light and dark themes.

## How it's built

- Plain static HTML, CSS and JavaScript. No framework, no build step, no dependencies to install.
- Each page is a single self-contained `index.html` with its own styles and scripts.
- External resources: Google Fonts, and [KaTeX](https://katex.org) from cdnjs for the maths in blog posts.
- Hosted on GitHub Pages from the `main` branch.

```
.
├── index.html                  # portfolio
├── README.md
└── blog/
    ├── index.html              # list of posts
    ├── federated-learning/
    │   └── index.html
    └── mixture-of-experts/
        └── index.html
```

## Run locally

Open `index.html` in a browser, or serve the folder so relative links behave exactly as on GitHub Pages:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Adding a blog post

1. Copy an existing post folder, e.g. `blog/mixture-of-experts/`, to `blog/<new-slug>/` and replace the content.
2. Update the `<title>`, `description`, and the `canonical` / `og:*` tags in the new page's `<head>` so link previews (LinkedIn, etc.) are correct.
3. In `blog/index.html`, copy one `<li>` block to the top of the list and change the link, date, title, summary and tags. Do the same in the **Writing** section of the main `index.html`.
4. Commit and push to `main`. GitHub Pages redeploys automatically.

## Licence and reuse

The code may be reused freely. The written content and diagrams are © Marc Pérez Bernús; please link back if you quote them.
