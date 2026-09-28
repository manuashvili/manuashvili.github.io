# manuashvili.github.io

Personal site and blog of Mari Anuashvili, built with [Eleventy (11ty)](https://www.11ty.dev/) and deployed to GitHub Pages. Writing on product, operations, and building with AI.

Site theme adapted from [mrozanski.github.io](https://github.com/mrozanski/mrozanski.github.io) by Mariano Rozanski (MIT License).

## Run locally

```bash
npm install
npm run serve
```

The site runs at `http://localhost:8080/`.

## Build

```bash
npm run build
```

Output goes to `_site/`. Pushing to `main` builds and deploys automatically through GitHub Actions.

## Add a post

Create a `.md` file in `src/posts/`:

```yaml
---
layout: post.njk
title: "Post title"
excerpt: "One-line summary for post listings and link previews."
author: "Mari Anuashvili"
date: 2026-09-28
tags: [product-ops, ai]
---
```

Write the post in Markdown below the front matter.