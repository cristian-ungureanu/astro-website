---
layout: ../../layouts/ProjectPage.astro
title: "MyStock.photos"
subtitle: "A WordPress site for browsing and importing CC0 stock photography."
poster: "/images/mystock-photos.jpg"
imageAlt: "MyStock.photos WordPress plugin interface showing a grid of stock photos"
---

### What it is

[MyStock.photos](https://mystock.themeisle.com/) is a WordPress site offering a large, searchable collection of CC0 (free-to-use) images. A custom gallery lets visitors browse and filter the collection, and a companion plugin lets WordPress users pull images from Flickr straight into their own media library.

### Tech stack

- **WordPress** as the content platform for the photo collection and site itself
- **Vue.js** powering the front-end image gallery: search, filtering, and lazy loading
- A companion **React** app, shipped as a WordPress plugin submodule, for browsing and importing photos, built on top of the [Free Stock Photos feature in Orbit Fox](https://docs.themeisle.com/orbit-fox/orbit-fox-documentation#5-free-stock-photos)
- **Flickr API** as the source for importable images

### What it set out to achieve

- Give visitors a fast, filterable gallery for finding CC0 images without leaving the browser
- Let WordPress users import photos directly into their media library in a couple of clicks, instead of downloading and re-uploading
- Keep the gallery and importer as two independently maintainable codebases sharing one platform
