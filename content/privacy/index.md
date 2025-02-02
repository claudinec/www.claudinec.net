---
title: "Privacy"
description: Privacy here and elsewhere
author: Claudine Chionh
date: 2024-04-20T18:45:04+10:00
publishDate: 2025-02-02
lastmod: 2025-02-02
draft: false
tags: [privacy, analytics]
aliases: [privacy-policy]
---

## This website

### Analytics

This website is hosted on [NearlyFreeSpeech](https://www.nearlyfreespeech.net/), a shared hosting provider located in the United States.

I do web analytics the old-school way, [parsing log files directly on the web server](https://indieweb.org/website-analytics#Log_Analyzers). I don't use a third-party analytics service.[^ga] I log website visits and errors and do not currently delete old log entries. [Apache's Combined Log Format](https://httpd.apache.org/docs/2.4/logs.html#combined) for access logs records the following information for each page request:[^robots]

* your [IP address](https://en.wikipedia.org/wiki/IP_address)
* date and time of request
* path requested (the web address not including the domain)
* address of the website that referred you here, if applicable (the `Referer`)
* a `User-Agent` string, which may include your web browser, operating system, or device type[^user-agent]

I use [GoAccess](https://goaccess.io/) to generate reports[^cron] which are hosted in a private directory on my hosting account and are not publicly accessible. GoAccess parses the Apache access logs along with [MaxMind's GeoIP Country Database](https://www.maxmind.com/en/geoip-databases), which correlates IP addresses with location.

[^ga]: Including, but not limited to, Google Analytics, Fathom, Plausible, Umami, or any other external web analytics service I might not even know about.
[^robots]: This request data is also used with my [`robots.txt`]({{< ref "/posts/2024-04-21-robots.md" >}}) file to block nefarious AI web scrapers.
[^user-agent]: A request from Mastodon or another ActivityPub service will reveal the name of the ActivityPub server, but not individual usernames. Likewise, a request from an online feed reader such as NewsBlur or Feedbin will reveal the name of the service but not individual users.
[^cron]: My GoAccess reports are generated periodically from a `cron` job, not dynamically/in real time.

### Links, cookies, forms, and JavaScript

Any external links appearing on this website are cleaned of [tracking parameters](https://en.wikipedia.org/wiki/Query_string#Tracking). Following a link from here to another website will only send a [`Referer`](https://en.wikipedia.org/wiki/HTTP_referer) (sic) header to the external web server.

This website is built with the [Hugo](https://gohugo.io/) static site generator. I "publish" content by running a terminal command to update HTML files. Images, CSS, and JavaScript are located on the same server as the HTML. I have not modified Hugo's default [security policy](https://gohugo.io/about/security/#security-policy) to allow fetching external resources when building the site. I do not save any [cookies](https://en.wikipedia.org/wiki/HTTP_cookie) or host any interactive forms. No external JavaScript libraries are fetched dynamically.

JavaScript hosted on this website is included with the PaperMod theme and used for the following features:

- to detect your device's light/dark theme and to switch the website theme between light and dark
- to [search](https://www.claudinec.net/search/) within this website

You can view the source code for:

- [this website's content and configuration](https://git.sr.ht/~claudinec/www.claudinec.net)
- the [Hugo](https://github.com/gohugoio/hugo) static site generator
- the [PaperMod](https://github.com/adityatelange/hugo-PaperMod/) theme

### Webmentions

[Webmention](https://indieweb.org/Webmention) is a communication protocol favoured by many in the IndieWeb community for facilitating interactions between websites. Implementing automatic webmentions on a statically-generated site like this one is not straightforward.

I occasionally **send** webmentions manually when the author of a receiving website has indicated that this is their preferred interaction method.

I do not currently **receive** webmentions. My preferred methods for interaction/receiving comments about this site are email and Mastodon.

## Contacting me

[Hello]({{< ref "/hello" >}}) lists the ways you can contact me, with links to my online profiles.

As I have a very limited, superficial understanding of cryptography, I am not able to verify any claims about encryption or privacy of specific software or services.

Links to external privacy policies:

- [Aus.Social](https://aus.social/privacy-policy) (my Mastodon server)
- [Bluesky](https://bsky.social/about/support/privacy-policy)
- [Fastmail](https://www.fastmail.com/policies/privacy/)
- [Signal](https://signal.org/legal/#privacy-policy)

### Signal

[Signal](https://signal.org/)'s main selling point is its [end-to-end encryption](https://support.signal.org/hc/en-us/articles/360007320391-Is-it-private-Can-I-trust-it). I have not inspected the Signal source code to verify its claims.

The Signal link (appearing on the front page and at Hello) links to my [Signal profile](https://support.signal.org/hc/en-us/articles/360007459591-Signal-Profiles-and-Message-Requests), which will open in the Signal app if it is installed on your device, or on the Signal website otherwise. Unless you actively use this link to contact me through Signal, I won't know that you have followed this link or viewed my profile.

### Email

My email address is linked on every page. If you follow an "Email me about this page" link on a specific page, the subject line is pre-filled with the path to the page's source code. You are free to change this subject line.

My primary email provider is [Fastmail](https://www.fastmail.com/features/), an Australian company with email servers located in the United States. Both countries are part of the [Five Eyes](https://en.wikipedia.org/wiki/Five_Eyes) spy alliance. You can read Fastmail's FAQs on [Privacy](https://www.fastmail.com/features/privacy/) and [Security](https://www.fastmail.com/features/security/).

I have had PGP keys since the 1990s and can count on two hands the number of times I have used them in real-world (not testing) scenarios. I am convinced that email is fundamentally insecure and cannot be made more secure or private without radical changes to the behaviour of every single person in the world who uses email.[^pgp] Bottom line: the administrators of my and your email servers are probably not spending their valuable time snooping on our conversations, but as a rule, don't use email for highly sensitive communications.

[^pgp]: Further reading on the futility of email encryption: Matthew Green, [What’s the matter with PGP?](https://blog.cryptographyengineering.com/2014/08/13/whats-matter-with-pgp/) (2014); Fastmail, [Why we don't offer PGP](https://www.fastmail.com/blog/why-we-dont-offer-pgp/) (2016); Latacora, [Stop Using Encrypted Email](https://www.latacora.com/blog/2020/02/19/stop-using-encrypted/) (2020).

### Mastodon and Bluesky

I usually post my blog post links from here to Mastodon or Bluesky, depending on the intended audience.[^posse] Occasionally, if a Mastodon or Bluesky thread that I start gets substantial, I may copy or expand it into a blog post here.[^pesos] In both cases, blog posts here may link to Mastodon/Bluesky threads or summarise individual posts (crediting the author by their name, pseudonym, or profile handle), but I do not copy the *content* of anyone else's posts here without their permission.

[^posse]: [Publish on Own Site, Syndicate Elsewhere (POSSE)](https://indieweb.org/POSSE).
[^pesos]: [Publish Elsewhere, Syndicate to Own Site (PESOS)](https://indieweb.org/PESOS). I haven't *actually* syndicated anything from Bluesky yet as I don't really start conversations there.

Direct messages on social media are a convenient way for people to send one-to-one messages to each other. They are not end-to-end encrypted so the administrators of my or your ActivityPub server or Bluesky can view messages (but probably won't, unless required by law enforcement).

<!-- vim: set spell linebreak textwidth=0: -->
