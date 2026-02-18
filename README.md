# genduk.dev

Personal blog and website of Genduk Ayu Pramesti, from Kotagede, Yogyakarta.

Thoughts on identity, safety, and what it means to remember and be remembered.

Live at [genduk.dev](https://genduk.dev)

## Stack

- [Astro](https://astro.build) with MDX
- Styled with custom CSS (terminal-inspired design)
- Deployed to GitHub Pages

## Development

```sh
bun install
bun dev
```

## Pre-commit Hooks

This project uses [pre-commit](https://pre-commit.com/) for code quality checks:

```sh
pre-commit install    # setup (one-time)
pre-commit run --all-files  # manual run
```

Hooks: **prettier** (format check), **eslint** (lint), **astro check** (typecheck).

## Commands

| Command       | Action                                     |
| :------------ | :----------------------------------------- |
| `bun install` | Install dependencies                       |
| `bun dev`     | Start local dev server at `localhost:4321` |
| `bun build`   | Build production site to `./dist/`         |
| `bun preview` | Preview build locally before deploying     |
