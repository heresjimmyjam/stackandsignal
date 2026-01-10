# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Stack & Signal is a Hugo static site generator project for a personal portfolio and blog. The site showcases projects, blog posts, and a newsletter.

## Common Commands

```bash
# Local development with live reload
hugo server

# Build static site (outputs to /public)
hugo

# Create new content
hugo new posts/my-post.md
hugo new projects/my-project.md
```

Deployment is automatic via Netlify when pushing to the main branch.

## Architecture

### Theme System

The site uses a custom theme at `themes/stackandsignal/` with project-level overrides in the root `layouts/` directory.

**Layout hierarchy** (Hugo looks in this order):
1. `layouts/` (project root - overrides)
2. `themes/stackandsignal/layouts/` (theme defaults)

### Key Layout Files

- `themes/stackandsignal/layouts/_default/baseof.html` - Base template with header, footer, color bars
- `themes/stackandsignal/layouts/index.html` - Homepage with paginated posts and newsletter inserts
- `layouts/projects/*.html` - Standalone HTML/CSS/JS apps embedded in project pages

### Content Organization

Content uses TOML front matter:
```toml
+++
date = '2026-01-05'
draft = false
title = 'Post Title'
tags = ["tag1", "tag2"]
image = "/images/image.gif"
type = "link"  # optional: "link" or "quote" for special post types
+++
```

Post types supported on homepage:
- Regular posts (default)
- Links (`type = "link"`) - external URL posts with domain extraction
- Quotes (`type = "quote"`) - with `attribution` field

### Styling

Main stylesheet: `themes/stackandsignal/static/css/style.css`

CSS variables define the color system:
- `--bg-color`, `--text-color` - base colors
- `--color-coral`, `--color-gold`, `--color-teal`, `--color-lavender` - accent colors

### Interactive Projects

Projects like the coffee calculator (`layouts/projects/coffee-calculator.html`) are self-contained HTML/CSS/JS applications embedded directly in Hugo templates - no external dependencies.

### External Services

- **Buttondown** - Newsletter signup forms (API endpoint in newsletter templates)
- **Netlify** - Hosting and deployment (config in `netlify.toml`)
