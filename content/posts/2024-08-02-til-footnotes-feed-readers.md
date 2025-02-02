---
title: "Today I Learned: Footnotes in feed readers"
author: Claudine Chionh
draft: false
date: 2024-08-02
tags: [til, footnotes, hugo, markdown, html, css, feeds, rss, netnewswire, feedbin]
---

There's a *de facto* convention for rendering footnotes in HTML that enables feed readers to give them special treatment, e.g. NetNewsWire and Feedbin display them inline if you select the numbered footnote popup.

[Simon Willison](https://simonwillison.net/2024/Aug/1/footnotes-that-work-in-rss-readers/), referencing [Chris Coyier](https://css-tricks.com/footnotes-that-work-in-rss-readers/), both with screenshots:

> I found [this code](https://github.com/Ranchero-Software/NetNewsWire/blob/094a85bce0ca2e5a7593eed027b71714a37c147c/Shared/Article%20Rendering/main.js#L144-L150) in the NetNewsWire source (it's MIT licensed) which runs against elements matching this CSS selector:

> `sup > a[href*='#fn'], sup > div > a[href*='#fn']`

> So any link with an `href` attribute containing `#fn` that is a child of a `<sup>` (superscript) element.

This Just Works :tm: in [Hugo](https://gohugo.io/getting-started/configuration-markup/#goldmark) and I'd never wondered why – it's a feature of [Goldmark](https://github.com/yuin/goldmark/blob/master/extension/footnote.go), Hugo's default Markdown parser.

(And I was inspired by Simon to start posting 'Today I learned' posts – just a [tag](/tags/til) at this stage, not sure if I'll make its own category or subdomain.)

{{< posse-mastodon mastodonUrl="https://aus.social/@claudinec/112891175456704002" >}}

