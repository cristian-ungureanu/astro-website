---
layout: ../../layouts/ProjectPage.astro
title: "Customizer Repeater"
subtitle: "A repeatable-field control for the WordPress Customizer, among the first of its kind."
---

### What it is

The WordPress Customizer ships with simple controls — text, color, image — but no built-in way to manage a *list* of repeatable items, like a set of slides or social links. Customizer Repeater adds that missing control, letting theme and plugin authors add, remove, and reorder groups of fields directly inside the live Customizer preview.

### Tech stack

- **PHP** for the `WP_Customize_Control` subclass and server-side rendering
- **JavaScript** (Underscore.js templates, as used natively by the Customizer) for the add/remove/reorder UI
- Integrates with the existing **WordPress Customizer API** — no extra admin screens or database tables

### What it set out to achieve

- Fill a real gap in the Customizer API at a time when no other public control did this
- Keep the control self-contained and easy to drop into any theme or plugin
- Get it in front of the WordPress community early — it went on to be well received and reused by other developers

[See it on GitHub](https://github.com/cristian-ungureanu).
