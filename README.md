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

## Writing page: essays and reading notes

The Writing page has two category-based sections. Add **one** of these categories
in a post's front matter: `categories: [essays]` for long-form writing, or
`categories: [reflections]` for reading notes. Only categorized posts appear on the Writing page. Existing post URLs retain the date-and-title
format configured in `_config.yml`; categories do not change that format.

Use this front matter with your own text (this is a template, not an article):

```yaml
---
layout: post
title: "Your essay title"
date: YYYY-MM-DD
categories: [essays]
description: "A short, plain-text description for the card and article header."
featured: true
featured_order: 1
---
```

One featured essay appears prominently above the smaller essay cards. Use `featured: true` and a unique
numeric `featured_order` on **every** featured essay; lower numbers appear first.
If several essays are marked featured, the lowest order wins; the others remain
in the regular grid. Remove both fields to stop featuring an essay. Other essays and all reflections
appear newest first. For a reading note use `categories: [reflections]` and omit
the featured fields. Without `description`, listings use a shortened excerpt.
Keep existing filenames and dates when categorizing existing posts to preserve
URLs. Use Markdown headings starting at `##` within articles; the layout supplies
the title. No JavaScript or additional Jekyll plugins are required.

Reading notes can optionally cite one or more works. References appear below the
description in the journal and below the article text. Supply a title and,
optionally, an HTTPS URL:

```yaml
references:
  - title: "Title and author of the paper or work"
    url: "https://example.org/paper"
  - title: "A print work without an online link"
```

The sample welcome post uses `published: false`, so normal Jekyll/GitHub Pages
builds omit it from the homepage, Writing page, feed, and generated post pages.
Do not use `--unpublished` for a publication build.

### Preview before publishing

In this prepared cloud environment:

```bash
cd /workspace/kbugbee1.github.io
source /workspace/.onboarding/env.sh
ruby /workspace/.onboarding/ruby/usr/bin/jekyll serve \
  --destination /workspace/.onboarding/site --disable-disk-cache \
  --host 127.0.0.1 --port 4000
```

The server rebuilds when you edit files. Use local HTTP requests to inspect
`/writing/` and post paths; the cloud onboarding UI does not provide a browser
preview link. A running server can be stopped with Ctrl+C.

On your own computer, with Jekyll 4.3 and `jekyll-feed` installed, check out
`feature/writing-stage-1` and run:

```bash
jekyll serve --destination /tmp/orbit-archive-preview --disable-disk-cache
```

Open the local server address printed by Jekyll and visit `/writing/`. Check both
wide and narrow browser widths. A production-style build can be checked with
`jekyll build --destination /tmp/orbit-archive-preview --disable-disk-cache`.
Previewing or building does not publish the site. Review the feature branch
before merging to the GitHub Pages publishing branch.
