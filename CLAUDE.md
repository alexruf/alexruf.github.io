# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

```bash
# Local development (hot-reload)
hugo server

# Production build (output to ./public/)
hugo --minify

# Update PaperMod theme
git submodule update --remote themes/PaperMod
```

## Deployment

Push to `source` branch triggers GitHub Actions (`.github/workflows/gh-pages.yml`), which builds with Hugo 0.159.0 extended and deploys to `master` branch via GitHub Pages. No manual deploy needed.

## Architecture

Personal blog built with Hugo + [PaperMod](https://github.com/adityatelange/hugo-PaperMod) theme (git submodule at `themes/PaperMod/`).

- **Config**: `hugo.toml` — base URL, menu items (Posts/Tags/About), social icons, privacy settings
- **Branches**: `source` = working branch, `master` = published site
- **Hugo Extended** is required (SCSS processing); version locked at 0.159.0 via `.tool-versions` (asdf)

## Content

```
content/
├── _index.md           # Homepage
├── about/index.md      # About page
└── posts/
    └── post-name/
        └── index.md    # Individual post (bundle style)
```

Front matter uses TOML (`+++` delimiters). Posts support `tags = ["tag1", "tag2"]`.

New post archetype (`archetypes/default.md`) sets `draft = true` by default.

## Customizations

- `layouts/shortcodes/social-icons.html` — custom shortcode rendering social links via a partial
- `static/CNAME` — custom domain (`alexruf.net`)
- Privacy settings in `hugo.toml`: analytics/Disqus disabled, YouTube uses privacy-enhanced mode
