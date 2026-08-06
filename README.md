# rbi-mtm.github.io

Website of the Modelling and Theory of Materials Group, built with [Hugo](https://gohugo.io/).

## Setup

1. Install [Go](https://go.dev/doc/install) (needed by Hugo Modules).
2. Install [Hugo extended](https://gohugo.io/installation/) v0.164.0 or later.
3. Clone the repo:
   ```
   git clone git@github.com:rbi-mtm/rbi-mtm.github.io.git
   cd rbi-mtm.github.io
   ```

## Editing content

Most changes (adding people, news, publications, teaching entries) just mean adding or editing a Markdown file under `content/`. Copy an existing entry of the same type as a template.

### Adding a news post

Create `content/post/<date>-<slug>/index.md`, e.g. `content/post/26-01-15-new-paper/index.md`:

```markdown
---
title: We published a new paper!
date: 2026-01-15
---

_A one-sentence teaser shown on the news list._

<!--more-->

The rest of the post goes here.
```

### Adding a publication

Create `content/publication/<slug>/index.md`, e.g. `content/publication/lastname-2026-topic/index.md`. Authors are matched by profile folder name (e.g. `iloncaric`) when the person has a profile, otherwise just write their full name:

```markdown
---
title: Title of the paper
authors:
- Full Name
- iloncaric
date: '2026-01-15'
publication_types:
- article-journal
publication: '*Journal Name*'
doi: 'https://doi.org/xxxx'
---
```

### Editing a profile

Each person has a folder under `content/authors/<username>/_index.md`, e.g. `content/authors/iloncaric/_index.md`. Edit fields like `role`, `bio`, `social`, `user_groups`, or the bio text below the `---` frontmatter directly. To add a new person, copy an existing author folder (including their `avatar.*` image) and update the frontmatter.

## Preview locally

```
hugo server
```

Then open http://localhost:1313.

## Publishing

Just commit and push to `main` — a GitHub Action automatically builds the site and deploys it to GitHub Pages.
