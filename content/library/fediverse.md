---
title: The Fediverse
draft: false
date: 2024-11-10
publishdate: 2024-11-17
lastmod: 2024-11-17
tags: [fediverse, mastodon]
ShowToc: true
---

## Introductions for complete newcomers

* [**Fedi.Tips**](https://fedi.tips/) – Comprehensive introductory guides to Mastodon and the wider Fediverse

* [**How the 'Fediverse' Works (and Why It Might Be the Future of Social Media)**](https://lifehacker.com/tech/what-is-the-fediverse-the-potential-future-of-social-media) – Lifehacker introductory article (October 2024)

## Types of service

Many current Fediverse services focus on replicating the experience of Big Tech services. Here's hoping that openness leads to more creative visions of what 'social media' can look like.

All of these services sit on top of the [ActivityPub](https://socialhub.activitypub.rocks/pub/guide-for-activitypub-users) protocol, which means that you can follow and interact with an account on another service from your own account. However, each type of service has different features so interactions across services (e.g. following a Bookwyrm reader from your Mastodon micro-blog) may be limited.

* :page_with_curl: Micro-blogging à la Twitter or Tumblr
  * [**Mastodon**](https://joinmastodon.org/) – The elephant in the room (sorry), the [most popular](https://fedidb.org/) Fediverse service, and commonly mistaken for the whole Fediverse. Notable forks include:
    * [**glitch-soc**](https://glitch-soc.github.io/docs/)
    * [**Hometown**](https://github.com/hometown-fork/hometown/wiki)
  * [**Misskey**](https://misskey-hub.net/en/)
    * [**Sharkey**](https://activitypub.software/TransFem-org/Sharkey/) – fork of Misskey
* :scroll: Long-form blogging
  * [**WriteFreely**](https://writefreely.org/)
* :speech_balloon: The 'Threadiverse' – link-sharing and discussions à la Reddit
  * [**Lemmy**](https://join-lemmy.org/)
  * [**kbin**](https://codeberg.org/Kbin/kbin-core)
    * [**Mbin**](https://joinmbin.org/) – fork of kbin, active development
* :books: Books – tracking collections and reading
  * [**Bookwyrm**](https://joinbookwyrm.com/)
* :camera: Photo blogging
  * [**Pixelfed**](https://pixelfed.org/)
* :video_camera: Video blogging
  * [**PeerTube**](https://joinpeertube.org/)

## Non-exhaustive lists of servers

Remember: **Federation** means you can interact with people on other servers without needing a separate account on each server. (Just like email!) And if you do find a friendly home, consider chipping in to help with the costs of operating a server.

### Micro-blogging

If you want to try Mastodon, I can't tell you which server is right for you, but I frequently follow or interact with members of the following servers so I think they're worth considering. Each server's **About** page has information about its ethos, rules/code of conduct, and prohibited content.

These arbitrary sub-headings of mine are not necessarily defining characteristics or rules for exclusion, just a very rough description of the kinds of people who tend to hang out on each server. There are also broader lists of general-interest and special-interest servers at [**Fedi.Garden**](https://fedi.garden/) (brought to you by Fedi.Tips) and [**Join Mastodon**](https://joinmastodon.org/servers).

Legend:

* :mammoth: Mastodon
* :house: Hometown
* :shark: Sharkey

#### Located in Australia or Aotearoa New Zealand

These all have admins and moderators living in the UTC+08:00 – UTC+12:00 timezones.

* :mammoth: [**Aus.Social**](https://aus.social/about) – :koala: my home server, hosted in Australia
* :house: [**ausglam.space**](https://ausglam.space/about) – Aussie GLAMR people
* :shark: [**Blåhaj Zone**](https://blahaj.zone/about) – trans and gender diverse people and allies, Australian admins and mods[^blåhaj]
* :mammoth: [**The Blower**](https://theblower.au/about)
* :question: [**Chinwag**](https://social.chinwag.org/about) – hosted in Australia
* :mammoth: [**Cloud Island**](https://cloudisland.nz/about) – paid membership, hosted in Aotearoa New Zealand

#### GLAMR or scholarly focus

* :house: [**ausglam.space**](https://ausglam.space/about) – Aussie GLAMR people
* :house: [**hcommons.social**](https://hcommons.social/about)

#### Tech focus

* :mammoth: [**Hachyderm**](https://hachyderm.io/about)
* :mammoth: [**IndieWeb.social**](https://indieweb.social/about)

#### Other

* :shark: [**Blåhaj Zone**](https://blahaj.zone/about) – trans and gender diverse people and allies, Australian admins and mods[^blåhaj]
* :mammoth: [**Wandering Shop**](https://wandering.shop/about) – science fiction and fantasy writers, fans, and fellow travellers

### Lemmy

* [**Beehaw**](https://beehaw.org/) – :bee: my home server, motivated by [safety and kindness](https://docs.beehaw.org/docs/core-principles/what-is-beehaw/)
* [**Blåhaj Lemmy**](https://lemmy.blahaj.zone/) – a safe place for trans and gender diverse people and allies, run by the operators of Blåhaj Zone[^blåhaj]

I used to spend a **lot** of time on Reddit – with its unified frontend to a wildly diverse range of discussion communities, it felt like a (Big Tech, corporate, centralised) descendant of [Usenet](https://en.wikipedia.org/wiki/Usenet) for the web. [Reddit's controversial changes to developer access in mid-2023](https://en.wikipedia.org/wiki/2023_Reddit_API_controversy) angered a lot of Reddit power-users – practically, because Reddit's default web interface is less appealing than the many alternative clients that were now being denied access; and philosophically, as this was a drastic reversal of Reddit's previous developer-friendly approach.

This unexpected change in Reddit's corporate attitude turned the spotlight on Lemmy and kbin, two Fediverse alternatives that were [unprepared for the sudden exodus from Reddit](https://join-lemmy.org/news/2023-06-17_-_Update_from_Lemmy_after_the_Reddit_blackout). This spotlight also revealed that the primary developers of Lemmy were [Marxist-Leninist, Chinese Communist Party apologists, and genocide denialists](https://beehaw.org/comment/318333). As Lemmy is a Fediverse service, anyone can run a Lemmy server with its own rules for content and behaviour, but the positions of the primary developers have not helped ease friction among various Lemmy communities. In addition, kbin, the main alternative to Lemmy, has only a single core developer who seems unable to handle the workload. (Since I last looked at kbin, a fork, Mbin, has emerged and is under active development.)

Like many others, I went looking for Reddit alternatives, but the [Reddit blackout protest](https://en.wikipedia.org/wiki/2023_Reddit_API_controversy#Subreddit_blackout) gave me time to re-evaluate my Reddit habits and realise that Reddit and its Fediverse equivalents had become (for me) spaces for window-shopping (I subscribed to too many subreddits for stationery collectors and specialty coffee enthusiasts) and watching argumentative people get into fights. While I think Beehaw and Blåhaj are examples of healthy Lemmy servers, I've gradually weaned myself off this particular kind of discussion space and don't spend much time on Lemmy now.

Whereas choosing a Twitter alternative (whether in the Fediverse or on one of its Big Tech competitors) depends a lot on finding the people/accounts you want to follow, choosing 'Threadiverse' (threaded discussion) alternatives is more focused on finding *communities*. Lemmy and similar servers are building their own communities, but following the Reddit exodus, many Reddit moderators moved their communities to various Fediverse servers, and [**sub.rehab**](https://sub.rehab/) provides a search interface to known Reddit alternatives. Again, in the Fediverse you may need only a single account to interact with any other account or community; however, if you follow a Threadiverse community from a non-Threadiverse account, you can't take advantage of many of the distinctive features of threaded discussion servers.

[^blåhaj]: Why **Blåhaj**? See Wikipedia: [LGBTQ symbols &sect; Blåhaj](https://en.wikipedia.org/wiki/LGBTQ_symbols#Bl%C3%A5haj) and [Blåhaj &sect; As a cultural phenomenon](https://en.wikipedia.org/wiki/Bl%C3%A5haj#As_a_cultural_phenomenon).
