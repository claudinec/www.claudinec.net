---
title: Everyday programming
author: Claudine Chionh
draft: false
date: 2024-12-17
tags: [ausglamr, python, programming, blogging, calendars]
---

I'm thinking of starting an occasional blog series on (until I find a better name) 'How an ex-programmer keeps introducing automation and programming into my non-programming job'. Yesterday I was compiling meeting and occupancy calendars for 2025 and instead of copying dates from an empty 2025 calendar and from the state government's public holiday calendar, I dusted off my Python date and calendar library (which I had built for generating janky lists of recurring dates) and started exploring the [`icalendar`](https://icalendar.readthedocs.io/en/latest/index.html) package to generate my own ical files.

(Yes, it's quite possible that I'm over-engineering a straightforward admin task, but I found it helpful to first formulate the rules for recurring meetings with the help of [`dateutil.rrule`](https://dateutil.readthedocs.io/en/stable/), then generate end-user-friendly calendar files as a separate step.)

Who would read this kind of blog post, though? This is useful for office administrators and archivists, but I'm guessing there aren't that many office admins offloading their boring tasks into bespoke software (yet?). Maybe it just illustrates that even though I burnt out of programming professionally, I can't stop bringing programming into my everyday life.

(Don't tell me an office admin can get a chatbot to write code for them – not a good idea if they don't understand what the code is doing.)

---

Originally posted elsewhere:

- [:mammoth: Mastodon](https://aus.social/@claudinec/113665390995716667) – a bit of discussion
- [:butterfly: Bluesky](https://bsky.app/profile/claudinec.net/post/3ldhml453tc26) – crickets ...