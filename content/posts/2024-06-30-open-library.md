---
title: Adding Open Library IDs to my Reading page
author: Claudine Chionh
draft: true
date: 2024-06-30
tags: [hugo, books, reading, open-library, internet-archive, indieweb, ausglamr]
---

I have updated the [`book` shortcode](/posts/2024-04-02-hugo-shortcode-books) used on my [Reading page](/reading) to link to the Internet Archive's [Open Library](https://openlibrary.org/help/faq/about), which provides crowd-sourced book metadata -- you can also look for these books in your local library! I've used the Open Library identifier for a [Work](https://openlibrary.org/about/lib) rather than a specific edition. I used the Open Library [API](https://openlibrary.org/dev/docs/api/books) to take the ISBN of a specific (physical or digital) book and return the Work ID; publishing and documenting that code might have to wait for another day.

