---
layout: ../../layouts/ProjectPage.astro
title: "Movie DB"
subtitle: "A React + TMDB movie browser with search, genre filters, and a favourites list."
poster: "/images/movie-db.jpg"
imageAlt: "Movie DB app homepage with a movie poster backdrop, search bar, and genre filters"
---

### What it is

A single-page frontend for [The Movie Database (TMDB)](https://www.themoviedb.org/) API. Visitors can browse popular movies, search by title, filter by genre, page through results, and save favourites for later, all without an account, since the watchlist lives in the browser.

### Tech stack

- **React** with the **Context API** and a `useReducer` store for global state (query, pagination, categories, watchlist)
- **react-router-dom** for the Browse / Favorites views
- **TMDB API v3** for search, discovery, and poster images
- **localStorage** to persist the favourites list and filter preferences between visits
- **SCSS** for layout and theming, with responsive breakpoints for mobile, tablet, and desktop

### What it set out to achieve

- A fast, no-backend movie browser that feels native to the TMDB catalogue
- Debounced search with graceful error and loading states (skeleton cards while fetching)
- A favourites experience that works entirely client-side, including filtering and pagination over the saved list

[See the source on GitHub](https://github.com/cristian-ungureanu).
