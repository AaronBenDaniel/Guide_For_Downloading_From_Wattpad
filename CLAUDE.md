# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

A Hugo static site using the PaperMod theme that provides platform-specific guides for downloading stories from Wattpad (branded as "Wattpad Downloading Guide"). Hosted on Netlify at https://wpd.abendaniel.top.

## Build & Development

The repo includes a vendored Hugo binary (`./hugo`, v0.122.0 extended). No system Hugo install is needed.

```bash
# Local dev server
./hugo server -D

# Production build (outputs to public/)
./hugo
```

Netlify builds use Hugo 0.122.0 as configured in `netlify.toml`.

## Content Structure

All guide pages live in `content/posts/` as Markdown files. The `weight` frontmatter field controls ordering on the home page (lower = higher). Platform guides: `getting-started.md`, `android.md`, `windows.md`, `macos.md`, `linux.md`, `ios.md`.

`content/search.md` exists solely to enable PaperMod's built-in search (requires JSON output in `hugo.yml`).

## Custom Shortcodes

Defined in `layouts/shortcodes/`:

- `linknewtab` — `{{</* linknewtab "URL" "text" */>}}` renders an `<a target="_blank">` link
- `linktotag` — links to a Hugo tag page
- `details` — collapsible `<details>/<summary>` block (inner content is markdownified)
- `rawhtml` — pass-through raw HTML
- `video` — HTML5 `<video>` embed from a URL
- `youtube` — responsive YouTube iframe embed by video ID

## Configuration

`hugo.yml` is the single config file. Key settings: dark theme default, PaperMod theme, search via Fuse.js, table of contents enabled and open by default.
