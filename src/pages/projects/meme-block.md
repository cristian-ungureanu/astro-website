---
layout: ../../layouts/ProjectPage.astro
title: "Meme Block"
subtitle: "A React-powered Gutenberg block for adding memes to WordPress posts, built during a hackathon."
---

### What it is

Meme Block is a Gutenberg block that lets WordPress users drop a meme generator straight into a post: pick a template, add top/bottom text, and the block renders the finished image inline. Built during an internal hackathon, it was voted the most interesting project of the event and later published on the WordPress.org plugin repository.

### Tech stack

- **React** via `@wordpress/element`, registered as a custom **Gutenberg block**
- `@wordpress/components` for the block's editor controls (template picker, text inputs)
- Canvas-based image composition to render the meme text onto the chosen template
- Packaged and published as a standalone plugin on **WordPress.org**

### What it set out to achieve

- Prove out a fun, self-contained Gutenberg block end-to-end within a hackathon's time limit
- Keep the editing experience simple: pick a template, type your captions, see the result immediately
- Ship something real: get it through WordPress.org plugin review and out to actual users
