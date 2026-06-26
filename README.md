# alimezar.github.io

Personal site and security research blog for Ali Sherif. Built with Jekyll, hosted
on GitHub Pages, dark/terminal theme, zero JavaScript.

## Structure

```
_config.yml            site config, nav, stats
index.html             home / landing
research.html          /research/ writeup index
about.md               /about/
cves.md                /cves/   (renders _data/cves.yml)
hall-of-fame.md        /hall-of-fame/ (renders _data/hof.yml)
404.html               not-found page
_posts/                writeups (one Markdown file per post)
_layouts/              default, page, post
_includes/             head, header, footer
_data/                 cves.yml, hof.yml  (edit these to update lists)
assets/css/style.css   the whole theme + syntax highlighting
assets/img/            diagrams (SVG)
assets/favicon.svg
```

## Run it locally (optional)

GitHub Pages builds the site for you on every push to `main`. To preview locally:

```bash
bundle install
bundle exec jekyll serve --livereload
# open http://127.0.0.1:4000
```

## Add a writeup

1. Create `_posts/YYYY-MM-DD-some-slug.md`.
2. Use this front matter (severity drives the colored badge):

```yaml
---
title: "Title"
subtitle: "One line hook."
date: 2026-06-22
severity: High        # Critical | High | Medium | Low
status: Fixed         # Fixed | Disclosed | Reserved
vuln_class: "Out-of-bounds R/W"
vendor: "Vendor"
product: "Component"
tags: [memory-safety, parser]
references:
  - label: "Advisory"
    url: "https://..."
---
```

3. Write Markdown. Fenced code blocks get syntax highlighting. Drop images/diagrams
   in `assets/img/` and reference them with
   `{% raw %}{{ '/assets/img/file.svg' | relative_url }}{% endraw %}`.

## Update CVEs / Hall of Fame

Edit `_data/cves.yml` and `_data/hof.yml`. No HTML needed, the pages render the lists.

## House style

No em dashes anywhere. Use commas, colons, or parentheses.
