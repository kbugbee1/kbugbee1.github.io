# Writing and publishing workflow

This journal has two kinds of writing: **Essays** for substantial perspectives,
and **Reading & Reflections** for shorter observations and reading notes.
The workflow is: **create a draft → revise → preview → review → publish**.
No substantive article is supplied by the templates.

## Before you start: drafts are public

This repository is public. Files in `_drafts`, branches, pull requests, and Git
history can be read by others. Jekyll leaving a draft off the website does **not**
make it private. Keep nonpublic work outside this repository. Do not commit
credentials, personal information, restricted information, or material awaiting
release authorization. Removing a committed file does not erase its history.

## 1. Create a draft (GitHub website)

1. Start from the latest `main` and create a new branch, for example
   `writing/short-title`, using GitHub's branch selector.
2. Open `_templates/essay.md` or `_templates/reading-reflection.md`. Copy its text.
3. Choose **Add file → Create new file** and name it `_drafts/short-title.md`.
   Paste the template. Use a short lowercase filename with hyphens.
4. Replace the title, description, and example date. Keep `layout: post` and
   exactly one category: `[essays]` or `[reflections]`.
5. Keep `published: false`. Save your draft to the new branch, not `main`.

The metadata between the two `---` lines is called *front matter*. Keep its
indentation, brackets, and quotation marks. Quote titles and descriptions,
especially if they contain colons. Do not change the original template files
when writing an article.

## 2. Revise

Edit the draft and save revisions on its branch. The description appears in
listings and the article header. Start article sections with `##`; the page
layout supplies the article title. Use descriptive link text and image alt text.
Put images safe for public release in `assets/images/` with suitable credits.
For an internal link, follow this example so Jekyll handles the site path:

```liquid
[About]({{ '/about/' | relative_url }})
```

For an essay, `featured: false` gives it a regular card. To nominate a prominent
essay, use `featured: true` and a numeric `featured_order: 1`. If several essays
are nominated, the lowest number wins and the others remain in the smaller-card
grid. Give nominated essays distinct numbers. Unfeatured essays and reading notes
appear newest first.

Reading notes may have a `references` list. Uncomment the template's example and
replace every placeholder. Each entry needs `title`; `url` is optional and must
start with `https://` to become a link. References appear in the reading journal
and at the end of the article. Omit the list if no references are needed.

## 3. Preview without publishing

GitHub's Markdown **Preview** tab checks the text, headings, and ordinary links.
It does not show the complete website design or render Jekyll-specific links.
For a visual review, ask your coding assistant:

> Preview my draft on its branch with Jekyll. Show desktop and mobile screenshots,
> check its category and links, and do not publish or merge anything.

The assistant should use a separate local output directory. Screenshots containing
draft text are also shareable material: only preview material safe to share.
Normal builds exclude `_drafts` and articles marked `published: false`.

### Commands for a coding assistant or local development

Use the existing isolated checkout; no additional worktree is needed. In this
prepared cloud environment, activate Ruby first:

```bash
cd /workspace/kbugbee1.github.io
source /workspace/.onboarding/env.sh
```

Run Jekyll with `ruby /workspace/.onboarding/ruby/usr/bin/jekyll` in this environment
(or `jekyll` on a computer with Jekyll installed). A draft preview explicitly
requires **both** flags because templates keep `published: false`:

```bash
jekyll serve --drafts --unpublished --destination /tmp/journal-draft-preview --disable-disk-cache --host 127.0.0.1
```

These flags can reveal *all* drafts and unpublished posts, including the old
sample welcome post. Review only the intended article. Do not use these flags
for a publication build, commit the output, or deploy the preview directory.
Keep any cloud preview internal and provide screenshots rather than localhost
links. Stop the preview server when finished. To verify normal publication:

```bash
jekyll build --destination /tmp/journal-publication-check --disable-disk-cache
```

Check the generated homepage, `/writing/`, `/about/`, `/publications/`, `/cv/`,
feed, and article pages. Verify drafts and the sample welcome post are absent.
Compare the article at desktop and phone widths. A successful build alone does
not establish that references, facts, or release permissions are correct.

## 4. Prepare an approved draft for publication

Do this only after the writing and release review below is complete:

1. On the article branch, open the draft in GitHub's editor. Rename its path from
   `_drafts/short-title.md` to `_posts/YYYY-MM-DD-short-title.md`, replacing the
   date with the intended publication date. This moves the file; do not leave a
   duplicate in `_drafts`.
2. Set `date` to match the filename and change `published: false` to
   `published: true`. Remove all template prompts and example source links.
3. Check category, description, and any featured settings. Build again without
   draft/unpublished flags and verify the article appears in the correct section.
4. Open a pull request into `main`. Include a short description, preview images,
   verification results, and any sources or release decisions needing attention.
   Use a **draft pull request** while review is incomplete.
5. Review the final changes and approve them before merging. Merging into the
   configured GitHub Pages publishing branch (`main`) triggers publication;
   creating or pushing the feature branch does not publish it to the site.
6. After the approved merge, check GitHub **Actions** for successful Pages
   deployment, then check the public homepage, Writing page, article, and links.
   Do not assume a merge means deployment succeeded.

A future publication date normally keeps an article off the site until a build
after that date. GitHub Pages does not guarantee a scheduled rebuild: use an
intentional publication build/merge when ready. Do not use dates as a privacy
control.

Existing article URLs use `/writing/YYYY/MM/DD/short-title/`. Once published,
keep the filename slug and date unchanged, and leave the configured permalink
alone. Editing the displayed title or text does not require changing the URL.

## Publication checklist

- [ ] **Factual accuracy:** verify names, dates, numerical claims, and quotations;
      distinguish evidence, uncertainty, interpretation, and personal opinion.
- [ ] **Sources:** open original sources; confirm authors, titles, dates, DOI/URLs,
      quoted context, and that each cited source supports the related claim.
- [ ] **Metadata:** check title, plain-text description, matching filename/date,
      correct category, intended featured priority, and explicit publication status.
- [ ] **Formatting:** remove template prompts; check headings, lists, quotations,
      images, captions, alt text, and long content at phone and desktop widths.
- [ ] **Links:** test internal links, article links, reference URLs, and asset paths;
      check that existing published URLs have not changed.
- [ ] **Public release:** confirm the text and attachments are safe for public
      sharing; check permissions/licenses and attribution, personal information,
      affiliation wording, and any applicable organizational review requirements.
      Preserve the site's personal-capacity disclaimer.
- [ ] **Build and review:** normal Jekyll build passes; intended article appears in
      its section; other drafts, templates, workflow notes, and the welcome sample
      are absent from generated output. Review the pull request before merging.
- [ ] **After publication:** Pages deployment succeeds and public pages work.

Templates and documentation are editorial tools only. They do not create a
publication schedule, change existing writing, or automatically approve or
publish drafts.
