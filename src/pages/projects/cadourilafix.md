---
layout: ../../layouts/ProjectPage.astro
title: "CadouriLaFix"
subtitle: "A WordPress + React gift-recommendation flow powered by ChatGPT."
poster: "/images/cadourilafix.jpg"
imageAlt: "CadouriLaFix app screen asking about the gift recipient and budget"
---

### What it is

CadouriLaFix.ro helps people find gift ideas by asking a few short questions (the recipient's age and relationship to them, the occasion, and a budget) and returning a set of personalised suggestions. The step-by-step flow is a React component shipped as a WordPress plugin/Gutenberg block.

### Tech stack

- **React** via `@wordpress/element` and `@wordpress/components`, built as a WordPress plugin
- A small client-side state machine driving the question steps (age/sex → relationship/budget → occasion → results)
- A WordPress REST endpoint that forwards the collected answers to the **OpenAI API**, prompting it for a list of gift ideas
- A second endpoint that cross-checks each suggestion against **eMAG** search results to attach a real product link
- `adblock-detect-react` + cookies to fall back gracefully when ad blockers interfere with the outbound API calls
- Social sharing for the results screen

### What it set out to achieve

- Turn "I don't know what to get them" into a handful of concrete, shoppable ideas in under a minute
- Keep the question flow short: four steps, each with sensible defaults and back/forward navigation
- Offer a "search again" path when the first batch of suggestions misses the mark, without losing the answers already given

[See the source on GitHub](https://github.com/cristian-ungureanu/traveltribe-AI).
