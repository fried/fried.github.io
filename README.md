# jasonfried.info

Personal website built with [Zola](https://www.getzola.org/), hosted on GitHub Pages.

## Quick Start

```bash
# Install Zola (macOS)
brew install zola

# Run locally
cd jasonfried.info
zola serve
# Open http://127.0.0.1:1111
```

## Project Structure

```
jasonfried.info/
├── config.toml              # Site configuration
├── content/
│   ├── _index.md            # Home page (unused — uses templates/index.html)
│   ├── resume.md            # Resume page → /resume/
│   ├── blog/
│   │   ├── _index.md        # Blog section config
│   │   └── my-post.md       # Individual posts → /blog/my-post/
│   └── stories/
│       ├── _index.md        # Stories section config
│       └── story-name/
│           ├── _index.md    # Story intro & config
│           ├── chapter-1.md # Chapter pages
│           └── chapter-2.md
├── sass/
│   └── style.scss           # All styles
├── templates/
│   ├── base.html            # Layout wrapper
│   ├── index.html           # Home page
│   ├── section.html         # Blog listing
│   ├── page.html            # Single post / resume
│   ├── stories.html         # Stories overview
│   ├── story.html           # Single story (chapter list)
│   └── chapter.html         # Single chapter
└── .github/
    └── workflows/
        └── deploy.yml       # GitHub Actions → GitHub Pages
```

## Adding Content

### New Blog Post

Create a file in `content/blog/`:

```markdown
+++
title = "My New Post"
date = 2025-04-01
description = "A short summary for the listing page."
+++

Your content here. Standard Markdown.
```

### New Story

1. Create a directory in `content/stories/`:

```
content/stories/my-story/
├── _index.md
├── chapter-1.md
├── chapter-2.md
```

2. Set up `_index.md`:

```markdown
+++
title = "My Story Title"
template = "story.html"
sort_by = "weight"
page_template = "chapter.html"
description = "What the story is about."
+++

Optional intro text shown on the story page.
```

3. Add chapters with `weight` to control order:

```markdown
+++
title = "Chapter 1: The Beginning"
weight = 1
description = "Optional chapter subtitle."
template = "chapter.html"
+++

Chapter content here.
```

### Update Resume

Edit `content/resume.md` directly. It uses standard Markdown wrapped in a `<div class="resume">` for styling.

## Deployment

Push to `main` and GitHub Actions handles the rest:

1. Zola builds the site
2. Output uploads as a GitHub Pages artifact
3. Deploys to your custom domain

### First-Time Setup

1. Create a GitHub repo (e.g., `jasonfried/jasonfried.github.io` or `jasonfried/jasonfried.info`)
2. Push this project to `main`
3. In repo Settings → Pages:
   - Source: **GitHub Actions**
4. Add custom domain `jasonfried.info`:
   - In repo Settings → Pages → Custom domain
   - Add a CNAME record with your DNS provider pointing `jasonfried.info` to `<username>.github.io`
   - Optionally add a `static/CNAME` file containing `jasonfried.info`

## Dark Mode

The site respects your system preference and includes a toggle button (☀️/🌙) in the navigation. The preference is saved in localStorage.

## Local Development

```bash
zola serve        # Dev server with hot reload at :1111
zola build        # Build to ./public/
zola check        # Validate internal links
```
