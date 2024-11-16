---
title: IndieWebbing from the couch
author: Claudine Chionh
draft: false
date: 2024-07-30
publishdate: 2024-07-30
lastmis: 2024-11-15
tags: [hugo, ios, indieweb, indieweb-carnival, tools, nearlyfreespeech]
---

I'm not going to pretend for a moment that building a personal website is easier than posting to a platform that someone else has already built. I know that updating content for a static site generator in a git repository from the command line introduces a whole lot of friction (and jargon) to the blogging/publishing process, when I could easily post elsewhere with a mobile app from the comfort of my couch or while commuting on a tram. But there are enough development and automation tools available for iOS that I can use my iPad or phone as a portable development lab. Here's how I write and publish away from a computer.

## Ingredients

- **Web host:** [NearlyFreeSpeech](https://www.nearlyfreespeech.net/)
- **Static site generator:** [Hugo](https://gohugo.io/)
- **Git repository host:** [Sourcehut](https://sourcehut.org/)[^githost]
- **iOS software**
  - **Git client:** [Working Copy](https://workingcopy.app/)
  - **Text editor:** [Textastic](https://www.textasticapp.com/)
  - **SSH client:** [Secure ShellFish](https://secureshellfish.app/)

[^githost]: My primary Git server is a Raspberry Pi running [Gitolite](https://gitolite.com/gitolite/index.html) and accessible only from my VPN. I use Sourcehut (and previously GitHub) to host repositories that I want to be able to reach from a third-party server like NearlyFreeSpeech.

## Method

To create a new post or page, I have a [Shortcut](https://support.apple.com/en-au/guide/shortcuts/welcome/ios) that creates a new file in Working Copy (optionally checking out a new Git branch), pre-filled with a template with Hugo metadata.

- **Write/edit** Markdown source in Textastic (or Working Copy for small changes)
- **Preview** Markdown output in the same text editor
- **Commit** changes in Working Copy and **push** to Sourcehut
- **Log in to web host** with Secure ShellFish
  - **Fetch and pull** changes from Sourcehut
  - **Build** the site with the [`hugo`](https://gohugo.io/commands/hugo/) command which is installed by default on NearlyFreeSpeech[^fish]

[^fish]: As I use [fish shell](https://fishshell.com/), I only need to start typing `hu` for the shell to [autosuggest](https://fishshell.com/docs/current/interactive.html#autosuggestions) `hugo` with command-line options from my command history.

Sure, it's not as streamlined as writing and publishing from a single app, but after no more than an hour's initial setup time I have an iOS blogging environment that replicates my computer setup.

*This post was written for the July 2024 [IndieWeb Carnival: Tools](https://jamesg.blog/2024/07/01/indieweb-carnival-tools/). Thanks James for hosting this month's Carnival. I really thought I was going to write about my favourite analogue writing tools and stationery for this Carnival, but somehow this post emerged instead.*
