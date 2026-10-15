---
layout: ../../layouts/ProjectPage.astro
title: "Neve"
subtitle: "A fast, AMP-ready WordPress theme with 200,000+ active installs, built as part of the Themeisle team."
poster: "/images/neve.jpg"
imageAlt: "Neve theme homepage demo with a bold hero headline and product mockups"
---

### What it is

[Neve](https://themeisle.com/themes/neve/) is a free, lightweight WordPress theme by Themeisle, built for speed and compatibility with every major page builder (Elementor, Gutenberg, Beaver Builder). I worked on it as part of the Themeisle/Codeinwp team for about five years (2018–2023), shipping features and maintaining the codebase across 400+ merged pull requests on the main repo. It's rated 4.7/5 from over 1,000 reviews on WordPress.org and has 200,000+ active installs.

### Tech stack

- **PHP** for theme templates and the `WP_Customize_Control` layer behind Neve's live Customizer options (menu icons, payment icons, popovers, typography, and more)
- **JavaScript/React** for the admin dashboard and onboarding flow, including the Starter Templates plugin (Templates Patterns Collection) used to import full demo sites, and in-dashboard feature-usage tracking
- **Cypress** end-to-end tests covering onboarding and starter-site import
- Close coordination with the companion **Otter Blocks** (Gutenberg blocks) and **neve-fse** (Full Site Editing) plugins in the same organization

### What it set out to achieve

- Keep a theme running on 200k+ live WordPress sites fast, accessible, and compatible as WordPress itself kept shipping new editor and Customizer APIs underneath it
- Cut the distance between "new WordPress install" and a finished site, through the Starter Templates onboarding flow
- Maintain backwards compatibility for a large existing install base while still shipping new features and page-builder integrations

[See the repo on GitHub](https://github.com/Codeinwp/neve), or [my merged pull requests](https://github.com/Codeinwp/neve/pulls?q=is%3Apr+author%3Acristian-ungureanu+is%3Amerged).
