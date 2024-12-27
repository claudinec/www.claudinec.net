---
title: "Coffee decision tree"
description: What coffee should I drink? Plus a digression into plain-text diagrams
author: Claudine Chionh
date: 2024-03-31T12:09:55+11:00
publishDate: 2024-03-31
draft: false
tags: ["coffee", "diagrams"]
---

James posted his [decision tree](https://jamesg.blog/2024/03/30/coffee-to-drink-decision-tree/) for deciding what coffee to drink.[^thread] I thought that as a strictly-black-coffee drinker mine would be simpler, but it turns out there are still a few variables.

<!--more-->

[^thread]: [:mammoth: Discussion on Mastodon](https://aus.social/@claudinec/112187405907379141)

```goat
                 .---------------------------------------.
                 |              Where am I?              |
                 +------------------+--------------------+
                 |                   \                    \
                 |                    \                    \
                 v                     v                    v
               .----.                 .----.               .----.
              | Home |               | Work |             | Cafe |
               '-+--'                 '---+'               '---+'
                 |                         \                    \
                 |                          \                    \
                 v                           v                    v
     .---------------------.     .-----------------------------.   .------------.
    | First cup of the day? |   |      Brought Nanopresso?      |  | Long black |
     '---------------------'     '-----------------------------'   '------------'
       yes              no                     yes             no          ^
        |               |                       \              \           |
        |               |                        \              \          |
        v               v                         v              v         |
 .-----------.    .--------------------------.   .------------.   .--------+-.
 | AeroPress |   | How undercaffeinated am I? |  | Nanopresso |  | Go to cafe |
 '-----------'    '+------+-----------------+'   '------------'   '----------'
                  /        \                 \
                 /          \                 \
                v            v                 v
             .----.       .--------.        .----------.
            | Very |     | Somewhat |      | Not at all |
             '-+--'       '-----+--'        '-----+----'
               |                 \                 \
               |                  \                 \
               v                   v                 v
.-------------------------.  .------------------.  .--------------------------.
| AeroPress or Nanopresso |  | AeroPress or V60 |  | Do I really need coffee? |
'-------------------------'  '------------------'  '--------------------------'
```

The [AeroPress](https://aeropress.com/products/aeropress-coffee-maker) (with [Prismo](https://fellowproducts.com/products/prismo)) has become my fuss-free almost-foolproof method for making that first cup of the day before I can concentrate on more precise methods. I can also make coffee for two by brewing into a carafe and adding extra hot water.

The [cafe](https://pridecentre.org.au/tenants/the-little-social/) in my work building didn't open until a year after ordinary Melburnians were allowed back into offices (and 18 months after the building officially opened). I was given a [Nanopresso](https://www.wacaco.com/products/nanopresso) to tide me over until then, and I still bring it in to work when I want a specific bean that I have at home or if I feel I'm spending too much money at cafes. A Nanopresso doesn't make espresso, strictly defined (it isn't possible to generate 9bar of pressure) but it's a neat little kit that I can pre-load with one or two shots in the morning and just add hot water from the office kitchen.

Specialty filter coffee is still pretty rare in Melbourne cafe culture and I've only been using a [V60](https://global.hario.com/product/coffee/dripper/VDC.html) dripper at home for about a year. I'm more likely to use this for a light and gentle pick-me-up in the afternoon.

Like many Melbourne households we have multiple Moka pots and plungers (French press) but I have hardly ever used these since discovering the AeroPress and falling down the specialty coffee rabbit hole a few years ago. They're still good for making coffee for more than two people at a time.

James built his flowchart while learning [MermaidJS](https://mermaid.js.org/). I'm a fan of Mermaid for creating diagrams in Markdown but the [Hugo docs on diagrams](https://gohugo.io/content-management/diagrams/) introduced me to [GoAT](https://github.com/bep/goat), a more literal ASCII format for rendering diagrams. It's also supported natively in Hugo whereas rendering Mermaid requires importing the Mermaid JavaScript library. In the spirit of minimising dependencies on external libraries, I made my first attempt at a GoAT diagram, which was more fidgety than the simple Markdown-style Mermaid syntax, but hey, it really feels like 1990s ASCII art!

<!-- vim: set filetype=markdown textwidth=0: -->
