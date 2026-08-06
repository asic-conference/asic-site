# ASIC — Conference website

A static website for the **Annual Summer Interdisciplinary Conference (ASIC)**.
Plain HTML, CSS and a little JavaScript — no build step, no framework, no server.
Ready to publish with **GitHub Pages**.

## What's in here

```
.
├── index.html              ← master menu of all meetings (the home page)
├── 2026-conference/
│   └── index.html          ← the 2026 conference page (eight-tab layout)
├── .nojekyll               ← tells GitHub Pages to serve files as-is
├── README.md               ← this file
└── CONTRIBUTING.md         ← how co-organizers edit pages (written for non-developers)
```

Each conference year lives in its own folder named `YEAR-conference/` containing a
single `index.html`. More year pages will be added over time — each is a
self-contained folder you simply drop in.

## Publish to GitHub Pages

1. Create a new **public** GitHub repository.
2. Upload everything in this folder to the repository root. On github.com you can
   drag-and-drop: **Add file → Upload files** (upload the folders too).
3. In the repo, open **Settings → Pages**.
4. Under **Build and deployment → Source**, choose **Deploy from a branch**.
   Set the branch to **main** and the folder to **/ (root)**. Click **Save**.
5. Wait about a minute. The site goes live at
   `https://<username>.github.io/<repo>/`.

Every commit re-publishes the site automatically.

## Use your own domain (recommended: `asic.lewan.uk`)

To serve the site from lewan.uk instead of github.io — while leaving the existing
WordPress site untouched — use a subdomain:

1. In **Settings → Pages → Custom domain**, enter `asic.lewan.uk` and save.
   (GitHub creates a `CNAME` file in the repo for you.)
2. At the DNS provider that manages **lewan.uk**, add a **CNAME record**:
   host/name `asic` → value `<username>.github.io`.
3. Return to **Settings → Pages** and tick **Enforce HTTPS** once it becomes
   available (can take a little while after DNS propagates).

Resulting addresses:

- Master menu: `https://asic.lewan.uk/`
- A year page: `https://asic.lewan.uk/2026-conference/`

All internal links are **relative**, so the site works unchanged whether it's
served from the github.io project URL or from a custom domain — no edits needed.

## Notes

- The display font (Fraunces) loads from Google Fonts over the web.
- Each page is **fully self-contained** (its own CSS and JavaScript), so editing
  one page cannot break another.
- To edit a page or add a new year, see **CONTRIBUTING.md**.
- Nothing here is dynamic: the sign-up forms are Google Forms and registration is
  an external link, so there is no database or backend to maintain.
