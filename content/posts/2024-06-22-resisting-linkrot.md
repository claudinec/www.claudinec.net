---
title: Resisting linkrot
description: Web archiving starts at home
author: Claudine Chionh
draft: false
date: 2024-06-22
tags:
- linkrot
- web-archiving
- hugo
- ausglamr
---

I say I'm an archivist but I've been rather blasé about archiving my own web presence. I can't find an archive of my [GeoCities](https://indieweb.org/GeoCities) site and the Wayback Machine only has a single capture from [my university undergraduate page](https://web.archive.org/web/20020116164950/http://www.student.unimelb.edu.au/~claudine/reading.html) (I had already graduated a couple of years before that). But I started collecting my own domains around the early 2000s and the Wayback Machine is a reminder of [the many iterations of my personal website](https://web.archive.org/web/*/www.claudinec.net*),[^domains] the different hand-coded templates, CMSes, and static site generators that I used, and all the text that I published and abandoned over the years.

[^domains]: The Wayback collection for `claudinec.net` only goes back to 2010, but this is not my first or only domain.

I can recover some of this material from the Wayback Machine or from my own hoard of old laptops (if the hard drives haven't died). In theory, I agree with the World Wide Web Consortium that [Cool URIs/URLs don't change](https://www.w3.org/Provider/Style/URI). But does anyone care if *my* old URLs are broken? And what should I do with URLs that point to embarrassing content?

Having lived half my life on the internet, including the early, wild days of the web when only <del>spooks, nerds, and weirdos</del> early adopters were online and we had very different (or absent) notions of security, privacy, and anonymity, I face competing impulses to preserve everything I can, and to hide or disavow some of my past. Change and growth are signs of maturity, aren't they? Thankfully I haven't yet been called out for decades-old writing that I now regret. I'm not even sure if there is anything really incriminating or embarrassing out there. Rather, I've let URLs fall by the wayside because I didn't think my words were significant enough. But even setting aside that opportunity for therapy, I now work for an organisation that values collecting [ephemera](https://en.wikipedia.org/wiki/Ephemera) for the stories they tell of marginalised communities.

If I want to take a personal stand against [linkrot](https://en.wikipedia.org/wiki/Link_rot), it's easiest for me to start by working backwards from today. When I rebuilt this website in Hugo a few years ago, I kept a few earlier posts, and there are even more unpublished posts hiding in plain sight in git repositories. Just looking back over the last three years, there's one post about a code editor that is no longer maintained, and two posts about tools I built to track and filter COVID-19 exposure alerts. Inspired by Wikipedia's templates for [referencing dead or archived web pages](https://en.wikipedia.org/wiki/Template:Webarchive/doc), I have created Hugo shortcodes for dead links either with or without archived versions in the Wayback Machine or other web archive services,[^robustlinks] as well as for a disclaimer to add to the top of outdated posts. You can see these shortcodes used on these posts:

- [The IDEs of March -- Demonstrating Atom for PyLadies Melbourne](/posts/2019-03-18-ides-of-march)
- [Victorian Covid-19 exposure site highlighter](/posts/2021-08-27-victorian-covid-19-exposure-site-highlighter)
- [Customised Covid-19 alerts](/posts/2021-09-03-customised-covid-19-alerts)

[^robustlinks]: I have formatted the archived links as [Robust Links](https://robustlinks.mementoweb.org/about/), which capture both the original and archived URLs in machine-readable form.

The source code for the shortcodes are in this site's git repository on [sourcehut](https://git.sr.ht/~claudinec/www.claudinec.net/tree/main/item/layouts/shortcodes).
