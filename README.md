# Impact Assessment Validation

A web frontend for loading and previewing Impact Assessment (IA) documents exported from TCS, preparing them for quality validation.

## Live site

The app is deployed from the `gh-pages` branch. Enable GitHub Pages once in repo **Settings → Pages → Build and deployment → Branch: `gh-pages` / `/ (root)`**.

Live URL: **https://leonvaughan-rgb.github.io/impact-assessment-validation/**

## Features

- **Drag & drop** or browse to load IA documents
- Supported formats: **JSON**, **Excel** (.xlsx/.xls), **Word** (.docx), **PDF**, **CSV**, **TXT**, **Markdown**
- **Structured view** for IA JSON documents (metadata, scope, risks, mitigations, sign-off)
- **Raw view** toggle for JSON inspection
- **Sample document** for quick testing

## Local development

Serve the folder with any static file server:

```bash
cd impact-assessment-validation
python3 -m http.server 8080
```

Open http://localhost:8080

## Project structure

```
impact-assessment-validation/
├── index.html              # Document loader frontend
├── package.json            # Static site marker for Vercel
├── vercel.json             # Vercel deployment config
├── samples/
│   └── ia_example.json     # Sample IA fixture
└── .nojekyll               # GitHub Pages static assets
```

## Next steps

- Wire validation agent to run quality checks on loaded documents
- Connect TCS API for live document fetch
- Export validation reports

## License

TBD
