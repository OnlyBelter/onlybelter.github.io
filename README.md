# Xin Xiong Personal Website

This repository contains the source for my personal academic website, built with Jekyll and deployed through GitHub Pages.

The site includes:

- a research-focused homepage,
- a homepage News panel fed by Jekyll posts,
- publications,
- CV,
- and a few secondary pages such as learning notes.

## Main Content

- Site-wide metadata: `_config.yml`
- Page content: `_pages/`
- Short news updates: `_posts/`
- Navigation: `_data/navigation.yml`
- Static files such as CV PDFs: `files/`
- Images: `images/`

## Homepage News panel

The homepage includes a lightweight `News` panel that renders the latest
posts tagged with `news`. This keeps the main self-introduction stable while
making it easy to publish short updates in a tweet-like format.

To add a news item:

1. Create a new Markdown file in `_posts/`.
2. Use a date-based filename such as
   `2026-09-06-qclaw-literature-tracking-system.md`.
3. Add the `news` tag in front matter.
4. Write a short paragraph and optional link.

Minimal template:

```md
---
title: "Short update title"
date: 2026-09-06
tags:
  - news
excerpt: "One short update with an optional [link](https://example.com)."
---

One short update with an optional [link](https://example.com).
```

The homepage currently shows the latest 3 `news` posts.

## Local Preview

This site uses the standard Jekyll workflow.

```bash
bundle install
bundle exec jekyll serve
```

Then open `http://localhost:4000`.

## Notes

- The site is based on the `academicpages` / `Minimal Mistakes` Jekyll ecosystem.
- Content and structure have been customized for personal academic use.
