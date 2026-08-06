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

## Preview locally

```
hugo server
```

Then open http://localhost:1313.

## Publishing

Just commit and push to `main` — a GitHub Action automatically builds the site and deploys it to GitHub Pages.
