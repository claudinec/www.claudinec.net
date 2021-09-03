---
title: Victorian Covid-19 exposure site highlighter
slug: victorian-covid-19-exposure-site-highlighter
description: Run a highlighter of doom over the suburbs near and dear to you
author: Claudine Chionh
date: '2021-08-27'
lastmod: '2021-08-27'
draft: false
images:
  - /images/2021-08-27-exposure-sites.png
tags:
  - covid-19
  - userscript
---

![table of exposure sites with rows highlighted in different background colours](/images/2021-08-27-exposure-sites.png)

At the time of writing, there are over 800 entries on the Victorian government's table of [public Covid-19 exposure sites](https://www.coronavirus.vic.gov.au/exposure-sites). The associated map isn't always up-to-date with the table, and even with the various sorting methods and the single-suburb filter, it can take a while to identify sites in the suburbs that you care about.

I have built a very rudimentary browser userscript that supplements this table by allowing you to identify multiple suburbs of interest and highlight the rows for these suburbs in background colours of your choice, differentiating between exposure tiers 1-3. This is my first userscript – and did I say it's very rudimentary? – but it makes it a bit easier to scan the last few pages of updates every few hours.

To run a userscript, you need Google Chrome or Firefox (or one of their derivatives) and a userscript manager such as [Violentmonkey](https://violentmonkey.github.io/), [Tampermonkey](https://www.tampermonkey.net/), or [Greasemonkey](https://www.greasespot.net/). You can [examine my code on GitHub](https://github.com/claudinec/cc-userscripts/blob/main/vic-exposure-site-highlighter.user.js) and [install the script from the 'raw' link](https://github.com/claudinec/cc-userscripts/raw/main/vic-exposure-site-highlighter.user.js).
