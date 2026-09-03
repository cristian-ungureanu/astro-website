---
layout: ../../layouts/ProjectPage.astro
title: "Variante Loto"
subtitle: "A statistics-driven Loto 6/49 newsletter and website, built as two connected Astro/Node projects."
poster: "/images/varianteloto.jpg"
imageAlt: "Variante Loto homepage with a headline about statistics-based number variants and a cluster of decorative lottery balls"
---

*Built with [Claude Code](https://claude.com/claude-code), Anthropic's AI coding agent — I directed the architecture, reviewed every change, and made the product decisions; Claude wrote and tested the code.*

### What it is

[VarianteLoto.ro](https://varianteloto.ro) analyses the full public history of Romanian Loto 6/49 draws and turns it into four suggested number variants, sent by email twice a week (Thursday and Sunday, the subscriber's choice) alongside the current jackpot and prize values. The site itself carries the always-on part: full-history statistics (hottest/coldest numbers, overdue numbers, most frequent pairs), the latest draws, and a subscribe form with a double opt-in flow and zero database.

### Tech stack

- Two separate repos: a **data + email pipeline** (Node scripts run on a GitHub Actions cron, twice a week) and the **Astro 7** site itself, deployed to **Cloudflare Workers**
- **Resend** for transactional email and audience segments; subscribers pick Thursday, Sunday, or both, and each gets routed to the matching Resend segment via a signed, stateless confirmation link (HMAC over email + preference + expiry — no database, no sessions)
- An architecture pivot mid-project: fetching loto.ro from inside a Cloudflare Worker turned out to be silently blocked at the network level (reproduced in production, `wrangler dev`, and even build-time prerendering) — the scraper moved out entirely into a plain Node script run by a normal GitHub Actions runner, writing a static JSON file the site imports at build time
- **node:test** and **Vitest** unit tests for the pure logic on both sides (variant generation, pairing/frequency analysis, token signing/verification) — deliberately excluding anything that hits a real network
- An optional, translated daily horoscope snippet in the email, sourced from a free API and machine-translated via a free translation API, added and swapped out a couple of times after early providers turned out to be paywalled or rate-limited from CI IP ranges

### What it set out to achieve

- Suggestions that come from real historical frequency and pairing data, not `Math.random()` — the homepage copy makes that distinction explicit
- A 100/100/100/100 Lighthouse score across every page, including a cookie-consent-gated Google Analytics setup that still gets detected as installed (Google's own installation checker only looks for a tag that's present unconditionally, which pushed the consent implementation from "load nothing until accepted" to Google's official Consent Mode pattern)
- Subscription and delivery that stay correct under edge cases most toy versions skip: no duplicate confirmation emails for an already-subscribed address, no repeated numbers across the four variants in a single email, incremental re-scraping instead of re-fetching decades of history on every run

The repos are private (subscriber data involved) — [see the live site](https://varianteloto.ro) instead.
