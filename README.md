# Concepts & Diagrams

A personal, visual knowledge base for concepts I am learning. Each concept lives in its own folder with an HTML explanation and an editable [draw.io](https://www.drawio.com/) diagram.

## Browse

- Open [`index.html`](index.html) for the catalog.
- See the starter example: [HTTP Request Lifecycle](concepts/http-request-lifecycle/index.html).
- GitHub Pages can turn the repository into a browsable website (setup below). This page is at [Github Page of Concepts & Diagrams](url)

```text
.
├── index.html
├── assets/
│   └── styles.css
├── concepts/
│   └── <concept-slug>/
│       ├── index.html
│       └── diagram.drawio
└── templates/
    ├── concept.html
    └── diagram.drawio
```

Use lowercase kebab-case folder names, such as `event-loop` or `zero-trust-networking`. Keeping the HTML page and its diagram together makes concepts easy to copy, move, and archive.

## Add a concept

1. Copy `templates/` to `concepts/<concept-slug>/`.
2. Rename nothing unless you want more than one diagram; `index.html` and `diagram.drawio` are the standard names.
3. Edit `diagram.drawio` at [app.diagrams.net](https://app.diagrams.net/) or with the draw.io desktop/VS Code extension.
4. Fill in the HTML placeholders and link the new page from the catalog in `index.html`.
5. Commit both files together so the explanation and source diagram stay in sync.

Optional exports (PNG, SVG, or PDF) can sit beside the source diagram. Always keep the `.drawio` file as the editable source of truth.

## Publish with GitHub Pages

1. Open this repository's **Settings → Pages**.
2. Under **Build and deployment**, choose **Deploy from a branch**.
3. Select the `main` branch and `/(root)` folder, then save.
4. After GitHub finishes publishing, browse the site at:
   `https://gh-user-001.github.io/Concepts-Diagrams/`

The included `.nojekyll` file tells GitHub Pages to serve this as a plain static HTML site.

## Preview locally

From the repository root, run:

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000`. A local server is preferable to opening files directly because it matches how the pages behave when hosted.
