# devsheet

Minimal monospace Hugo theme for portfolios.

## Quick Start

```bash
hugo server
```

Open http://localhost:1313

## Creating Content

### New Blog Post

```bash
hugo new blog/YYYY-MM-DD-slug-title.md
```

Or manually create `content/blog/your-post.md`:

```yaml
---
title: "Your Post Title"
date: 2024-12-08
description: "Short description for lists"
github: "https://github.com/you/repo"  # optional
---

Your content here. Supports:

- **Markdown** formatting
- `inline code` and code blocks
- LaTeX math: $E = mc^2$ or block:

$$
\int_0^\infty e^{-x^2} dx = \frac{\sqrt{\pi}}{2}
$$
```

### New Project

Create `content/projects/project-name.md`:

```yaml
---
title: "project-name"
description: "One-line description"
date: 2024-12-08
github: "https://github.com/you/repo"  # optional
---

Project details here.
```

## Frontmatter Reference

| Field | Required | Description |
|-------|----------|-------------|
| `title` | Yes | Page title |
| `date` | Yes | YYYY-MM-DD, determines sort order |
| `description` | No | Shows in list views |
| `github` | No | Shows GitHub link in article header |

## Directory Structure

```
your-site/
├── content/
│   ├── blog/           # Blog posts
│   ├── projects/       # Project pages
│   └── about.md        # About page
├── static/
│   └── img/            # Images, GIFs
├── themes/devsheet/    # Theme files
└── hugo.toml           # Site config
```

## Adding Images

1. Put images in `static/img/`
2. Reference in markdown: `![alt text](/img/filename.png)`

Images in articles auto-scale to full content width.

## Configuration

Edit `hugo.toml`:

```toml
[params]
  author = "your name"
  description = "Site tagline"
  github = "https://github.com/you"
  linkedin = "https://linkedin.com/in/you"
  email = "you@example.com"
```

## Build for Production

```bash
hugo
```

Output goes to `public/`. Deploy that folder to your host.

## Theme Customization

- Colors: `themes/devsheet/assets/css/main.css` (CSS variables at top)
- Layouts: `themes/devsheet/layouts/`
- Icons: `themes/devsheet/layouts/partials/icon-*.html`

## Features

- Light/dark theme toggle (respects system preference)
- KaTeX for LaTeX math
- Syntax highlighting (Chroma)
- Full-width images in articles
- GitHub link in article headers
- Responsive design
