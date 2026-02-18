# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

Personal blog/website for Genduk Ayu Pramesti (genduk.dev). Built with Astro, deployed to GitHub Pages.

## Commands

```sh
bun install              # install dependencies
bun dev                  # dev server at localhost:4321
bun build                # production build to ./dist/
bunx prettier --check .  # format check
bunx prettier --write .  # format fix
bunx eslint .            # lint
bunx astro check         # typecheck
pre-commit run --all-files  # run all pre-commit hooks
```

## Architecture

- **Astro 5** static site with MDX support, sitemap, and RSS
- Package manager: **bun** (bun.lock, not package-lock.json)
- Pre-commit hooks via **pre-commit** framework (Python): prettier, eslint, astro check
- CI: GitHub Actions deploys to GitHub Pages on push to main (runs lint/check/build)

### Content

- Blog posts live in `src/content/blog/` as `.md`/`.mdx` files
- Content schema defined in `src/content.config.ts` — frontmatter requires: `title`, `description`, `pubDate`; optional: `updatedDate`, `heroImage`
- Site constants (title, description) in `src/consts.ts`

### Layout

- Single layout: `src/layouts/BlogPost.astro` — used by blog posts and standalone pages (about, me)
- Components in `src/components/`: BaseHead, Header, Footer, HeaderLink, FormattedDate
- Pages: index (homepage with post list), blog/index, blog/[...slug], about, me (hidden), rss.xml

### Styling

- Custom CSS in `src/styles/global.css` — terminal-inspired design with CSS custom properties
- No CSS framework or preprocessor

## Conventions

- Use double quotes (prettier default)
- Respond in **Bahasa Indonesia Gaul** when communicating with the user
