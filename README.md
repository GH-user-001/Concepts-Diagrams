# Concepts & Diagrams

A personal, visual knowledge base for concepts I am learning. Each concept lives in its own folder with an HTML explanation and an editable [draw.io](https://www.drawio.com/) diagram.

## Browse

- Open [`index.html`](index.html) for the catalog.
- See the starter example: [HTTP Request Lifecycle](concepts/http-request-lifecycle/index.html).
- GitHub Pages can turn the repository into a browsable website (setup below).

## Repository layout

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

## Preview locally

From the repository root, run:

```bash
python3 -m http.server 8000
```

Then open <http://localhost:8000>. A local server gives the same relative-link behavior as GitHub Pages.

## Publish with GitHub Pages

In the GitHub repository, open **Settings → Pages**, select **Deploy from a branch**, choose **main** and **/(root)**, then save. The site will be available at:

`https://gh-user-001.github.io/Concepts-Diagrams/`

## Writing checklist

- State the concept in one sentence.
- Explain why it matters and where it is used.
- Walk through the diagram in numbered steps.
- Capture assumptions, trade-offs, and common mistakes.
- Add sources and a “last reviewed” date.
- Prefer links between related concept pages over duplicating explanations.
