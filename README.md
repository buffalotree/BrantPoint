# Brantpoint

Static website for Brantpoint, hosted on **GitHub Pages**.

- **Repo:** [buffalotree/BrantPoint](https://github.com/buffalotree/BrantPoint)
- **Live URL:** https://buffalotree.github.io/BrantPoint/

## How it's hosted

GitHub Pages is configured to **deploy from the `main` branch, root (`/`)**.
Every push to `main` republishes the site automatically (usually live within a minute).

A `.nojekyll` file is present so GitHub serves files exactly as-is (no Jekyll
processing) — this keeps folders/files that start with `_` working and speeds up builds.

## Project structure

```
.
├── index.html     # landing page (placeholder — to be replaced by the design)
├── 404.html       # custom not-found page
├── .nojekyll      # disable Jekyll processing
├── .gitignore
└── README.md
```

## Local development

It's plain static HTML — open `index.html` directly, or serve the folder:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploying a change

```bash
git add -A
git commit -m "Update site"
git push
```

## Custom domain (optional)

To use a custom domain (e.g. `brantpoint.com`):

1. Add a `CNAME` file at the repo root containing just the domain.
2. Point the domain's DNS at GitHub Pages (A/AAAA records for an apex domain,
   or a `CNAME` record `www -> buffalotree.github.io` for a subdomain).
3. Set the custom domain under the repo's **Settings → Pages**.
