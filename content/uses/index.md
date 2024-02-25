---
title: What I use
draft: false
date: 2024-02-24
publishDate: 2024-02-25
---

Lists of things I use daily/frequently. Longer explanations may come later.

## Hardware

General principles: Unix-like servers, personal devices from the Appleverse. This is where I've landed after learning programming and system administration in Unix environments and later working with history professors and web designers who care about things looking nice. I work in a bring-your-own-device environment, so I only occasionally have to use Windows.

- everyday devices: MacBook Air, iPhone, Apple Watch, iPad Pro
- home servers: Mac Mini, Raspberry Pi
- hosted elsewhere: [NearlyFreeSpeech](https://www.nearlyfreespeech.net/) shared hosting for DIY enthusiasts, which allows me to tinker with my static website without the overkill of a cloud VPS

## Software

- programming and, for want of a better term, "personal devops"
    - [Tailscale](https://tailscale.com/) connects all my devices in a VPN
    - most code and config is kept in git repositories which live in [Gitolite](https://gitolite.com/gitolite/index.html) at home and, in some cases, also on GitHub
    - after decades in bash and many years in zsh, I've been using [fish](https://fishshell.com/) as my primary shell since mid-2023
    - [tmux](https://github.com/tmux/tmux/wiki) plays nicely with both iTerm2 (macOS) and Secure Shellfish (iOS)
    - [Vim](https://www.vim.org/) is my default text editor; I periodically try to live with Emacs as my default (mainly because of [Org Mode](https://orgmode.org/)) but 25 years of `vi` muscle memory is hard to resist
    - [dotfiles](https://dotfiles.github.io/) are managed by [chezmoi](https://chezmoi.io/) (still in the process of migrating from [dotbot](https://github.com/anishathalye/dotbot))
    - [Python](https://www.python.org/) is my go-to scripting language for most tasks that don't interact with the web
    - plain [JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript) for working with web data and APIs, and with iOS automation utilities
    - [Hugo](https://gohugo.io/) static site generator
- macOS
    - dev tools: [Homebrew](https://brew.sh/), [iTerm2](https://iterm2.com/), [MacVim](https://macvim.org/), [Visual Studio Code](https://code.visualstudio.com/)
    - personal automation: [Shortcuts](https://support.apple.com/en-au/guide/shortcuts-mac/welcome/mac), [Keyboard Maestro](https://www.keyboardmaestro.com/main/), [Bunch](https://bunchapp.co/), [Drafts](https://getdrafts.com/)
    - Microsoft Office to collaborate with work colleagues
- iOS/iPadOS
    - automation superpowers: [Shortcuts](https://support.apple.com/en-au/guide/shortcuts/welcome/ios), [Pushcut](https://pushcut.io/), [Scriptable](https://scriptable.app/), [Drafts](https://getdrafts.com/)
    - dev tools: [Textastic](https://www.textasticapp.com/), [Runestone](https://runestone.app/), [Working Copy](https://workingcopy.app/), [Secure Shellfish](https://secureshellfish.app/), [a-Shell](https://holzschu.github.io/a-Shell_iOS/)
- fun/downtime (iOS/macOS)
    - [NetNewsWire](https://netnewswire.com/) [feed](https://aboutfeeds.com/) reader (self-curated chronological feeds[^feedrant])
    - [Overcast](https://overcast.fm/) podcast player
    - [Triode](https://triode.app/) internet radio
    - [Ivory](https://tapbots.com/ivory/) Mastodon client

[^feedrant]: [A micro-rant about the changing definition of online "feeds" :mammoth:](https://aus.social/@claudinec/111793840021907927)
