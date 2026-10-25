# Orbit & Archive — your GitHub Pages website

This is a light, editorial personal website with archival-inspired typography, a custom orbit illustration, and a subtle scientific-data-history aesthetic. It uses Jekyll, which GitHub Pages builds automatically. No command line is needed for everyday updates.

## Start here: publish your website

1. Download and unzip the ZIP file.
2. Sign in to [GitHub](https://github.com). Click **+** → **New repository**.
3. Name the repository **YOURUSERNAME.github.io** (replace YOURUSERNAME with your GitHub username). Choose **Public**, then create it. Do not add a starter README.
4. Upload **the contents** of this folder to the repository, not the outer folder itself. Preserve `_layouts`, `_posts`, and `assets` directories. If GitHub's web upload doesn't preserve folders, use [GitHub Desktop](https://desktop.github.com/) or create files with the path in their filename (e.g. `_layouts/default.html`).
5. Commit the upload. Go to **Settings → Pages**. Under **Build and deployment**, select **Deploy from a branch** → **main** → **/(root)** → **Save**.
6. Wait for deployment, then open **https://YOURUSERNAME.github.io**. If it does not appear, check the repository's **Actions** tab for build errors.

## Personalize the site

- `_config.yml`: change `title` to your name and update the description.
- `index.html`: edit the headline, introduction, and Recent activity section.
- `about.md`: replace the example biography. Keep the disclaimer and review its wording before publishing.
- `publications.md`: add your real talks and publications; delete placeholders.
- `cv.md`: add a summary or a PDF CV.
- `_layouts/default.html`: replace the generic GitHub and LinkedIn footer links with your profile links. Keep the disclaimer visible on every page.
- `assets/css/style.css`: the five colors at the start (`--paper`, `--surface`, `--ink`, `--accent`, `--gold`) control the palette.
- `assets/images/orbit-archive.svg`: a custom vector orbit diagram; no third-party image or license is needed.

## Write a new blog post (browser only)

1. Open `_posts` in your GitHub repository.
2. Click **Add file → Create new file**.
3. Name it `YYYY-MM-DD-short-title.md`, e.g. `2026-11-05-conference-reflections.md`.
4. Paste and edit:

```markdown
---
layout: post
title: "Reflections on Scientific Data"
date: 2026-11-05
---

This is my opening paragraph.

## A section heading

And this is another paragraph.
```

5. Click **Commit changes**. GitHub will automatically rebuild the site. The post appears on the homepage and the Writing archive.

The welcome post in `_posts` is a **sample**. Delete or rewrite it before you launch.

## Optional CV PDF

Upload a file to `assets/cv.pdf` and add `[Download my CV]({{ '/assets/cv.pdf' | relative_url }})` to `cv.md`.

## Personal capacity and publication caution

The disclaimer appears in the footer of **every page**, with an expanded section on the About page. It is suggested language, **not** a NASA-approved or legal-reviewed statement. Check applicable NASA ethics, communications, affiliation, and information-release guidance. Do not publish nonpublic, restricted, or otherwise unauthorized information. Do not imply agency endorsement.

## Troubleshooting

- If the site shows 404, check the repository name, Pages settings, and deployment status.
- If styling is missing, check the `assets/css/style.css` path.
- If posts do not appear, check the `_posts` folder, date format, and `layout: post` front matter.
- If links are wrong, ensure your repo is named `YOURUSERNAME.github.io` and `_config.yml` has `baseurl: ""`.
