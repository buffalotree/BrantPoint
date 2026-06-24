# Brant Point Courtyard

Website for **Brant Point Courtyard** — a timeshare resort of fourteen individually
appointed cottages set around a private garden courtyard at 15 Swain Street,
Nantucket, Massachusetts. Welcoming guests and owners for over 42 years.

Hosted on **GitHub Pages**.

- **Repo:** [buffalotree/BrantPoint](https://github.com/buffalotree/BrantPoint)
- **Live (staging):** https://buffalotree.github.io/BrantPoint/

## Pages

| File | Page |
|------|------|
| `index.html` / `Home.html` | Home — overview of the resort and its setting |
| `Cottage.html` | The fourteen cottages — layouts, features, photos |
| `Discover.html` | Discover Nantucket — local guide |
| `Gallery.html` | Photo gallery |
| `Sales.html` | Ownership / sales |
| `Contact.html` | Address, phone, email, enquiries |

`index.html` is a copy of `Home.html` so the root URL renders the homepage directly.
Internal links use relative `.html` filenames, so the site works both on the project
subpath above and on a custom domain. Photographs of the property load from the
existing `brantpointcourtyard.com` media library; all other imagery is embedded
in the pages.

## Source

These pages are a static export from a **Claude Design** project. The editable
source (`*.dc.html` components) lives in that design project, not in this repo —
re-export and replace the page files here to publish updates.

## How it's hosted

GitHub Pages deploys from the `main` branch, root (`/`). A `.nojekyll` file is
present so files are served exactly as-is. Every push to `main` republishes
(usually live within a minute).

## Deploying an update

```bash
git add -A
git commit -m "Update site"
git push
```

> Deploys require the **buffalotree** GitHub account: `gh auth switch --user buffalotree`
> before pushing, then switch back afterward if needed.

## Custom domain (brantpointcourtyard.com)

1. Add a `CNAME` file at the repo root containing the domain.
2. Point DNS at GitHub Pages (apex A/AAAA records, or `www` CNAME → `buffalotree.github.io`).
3. Set the custom domain under **Settings → Pages**.
4. Add back `robots.txt` and `sitemap.xml` from the export (they reference the production domain).
