---
layout: ../../layouts/ProjectPage.astro
title: "Orbit Fox"
subtitle: "A modular WordPress companion plugin with 100,000+ active installs, built as part of the Themeisle team."
poster: "/images/orbit-fox.jpg"
imageAlt: "Orbit Fox plugin dashboard showing the Mystock Import and Header Footer Scripts modules"
---

### What it is

[Orbit Fox](https://wordpress.org/plugins/themeisle-companion/) is Themeisle's free companion plugin: a grab-bag of features WordPress themes don't cover on their own (menu icons, SVG support, custom fonts, a cookie notice, page builder widgets, and more), each shipped as a module you can switch on or off individually so a site only loads what it actually uses. I worked on it alongside [Neve](/projects/neve/) as part of the Themeisle/Codeinwp team, between 2017 and 2023, with 100+ merged pull requests across the plugin and its page-builder integrations. It has 100,000+ active installs and 300+ reviews on WordPress.org.

### Tech stack

- **PHP** module system: each feature is a self-contained class the plugin can enable, disable, and settings-page for independently
- **JavaScript/React** for the admin modules dashboard and per-module settings UI
- Separate companion repos for the **Elementor** widgets module and the **content forms** module, kept decoupled from the core plugin's release cycle
- Deep integration with Themeisle's own themes, especially **Hestia**, keeping default section content and Customizer controls working as WordPress's own Customizer and selective-refresh APIs changed underneath them

### What I built

- **Header Footer Scripts**, a module I built from scratch, letting site owners drop tracking/analytics code into the header, footer, or body without editing theme files
- **Mystock Import**, pulling CC0 photos straight from [MyStock.photos](/projects/mystock-photos/), the stock-photo site I also built, directly into the WordPress media library in a couple of clicks
- Years of maintenance keeping the plugin working through PHP 8 deprecations, WordPress core Customizer changes, and page-builder (Elementor/Beaver Builder) compatibility breaks

### What it set out to achieve

- Keep a plugin running on 100k+ live sites modular, so enabling one feature never costs sites that don't use it
- Fill real gaps between what WordPress core and page builders offer out of the box and what site owners actually ask for
- Tie into Themeisle's own themes and other plugins (MyStock.photos among them) without becoming a single, tangled monolith
