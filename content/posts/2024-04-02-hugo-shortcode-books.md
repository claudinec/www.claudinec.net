---
# vim: set spell linebreak textwidth=0:
title: "A custom Hugo shortcode for books"
description:
author: Claudine Chionh
date: 2024-04-02T16:23:09+11:00
publishDate:
draft: false
tags: [hugo, books, reading, indieweb, ausglamr]
---

I've broken out of my lockdown-era reading slump (a topic for another blog post) and wanted to return to tracking and sharing my reading online (tracking and sharing my reading is one of the reasons I went back to library school in the first place). I have accounts on both [LibraryThing](https://en.wikipedia.org/wiki/LibraryThing) and [Goodreads](https://en.wikipedia.org/wiki/Goodreads) and used to find good recommendations on both sites, but Amazon bought Goodreads and LibraryThing, while still independent and nerd-friendly, is after all another [silo](https://indieweb.org/silo) where I am not in full control of the data I submit.

I went looking for an IndieWeb/fediverse-friendly solution and, as usual, I started getting into the weeds and trying to over-engineer the issue. Should I find a friendly neighbourhood [BookWyrm](https://joinbookwyrm.com/) instance or even run my own?[^sysadmin] In terms of social interaction, I'm pulling back from the oversharing encouraged by data-hungry corporations -- I want to share the books I'm reading and see what other people are reading, but I don't need to publicly track how many pages I read every day or comment on other people's highlights or marginalia.

[^sysadmin]: Of course not! I stopped working in tech partly so I wouldn't have to constantly worry about maintaining and securing a server.

I realised that all I wanted for now was a single **Reading** page here to track the books I've read since the start of the year. Still in that over-engineering mindset, I thought I'd need to use something like Hugo data files and templates to represent structured book data, but really all I needed was a [custom shortcode](https://gohugo.io/templates/shortcode-templates/)[^shortcode] to mark up author, title, and date of publication. I use the `book` shortcode on my [**Reading**](/reading) page to enforce a consistent formatting style on each listed book. If I want to change the format or add more metadata later, I only need to change the shortcode to apply the new style to all content using the shortcode. You can see how this works in the source code for the [shortcode](https://github.com/claudinec/www.claudinec.net/blob/f9fa12901f37ef608cf922eda27fb2b581723bc4/layouts/shortcodes/book.html) and the [Reading page](https://github.com/claudinec/www.claudinec.net/blob/f9fa12901f37ef608cf922eda27fb2b581723bc4/content/reading/index.md?plain=1).

[^shortcode]: A [shortcode](https://gohugo.io/content-management/shortcodes/) is a kind of micro-template also found in content management systems like WordPress.

