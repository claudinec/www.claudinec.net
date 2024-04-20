---
# vim: set spell linebreak textwidth=0:
title: "Privacy"
description: This website's privacy policy
author: Claudine Chionh
date: 2024-04-20T18:45:04+10:00
publishDate:
lastmod:
draft: true
tags: []
---

## Analytics

This website is hosted on [NearlyFreeSpeech](https://www.nearlyfreespeech.net/), a shared hosting provider located in the United States.

I do web analytics the old-school way, parsing log files directly on the web server. I don't use Google Analytics or any other third-party analytics service.

I log website visits and errors and do not currently delete old log entries. Apache's Combined Log Format for access logs records the following information for each page request:

* your IP address
* date and time of request
* path requested (the web address not including the domain)
* address of the website that referred you here, if applicable
* a User-Agent string, which may include your web browser, operating system, and/or device type

I use GoAccess to generate reports which are hosted in a private directory on my hosting account and are not publicly accessible. GoAccess parses the Apache access logs along with MaxMind's country-level geolocation database, which correlates IP addresses with location.

robots.txt

...

Hugo, no external JavaScript.

To verify these claims, you can view the source code for this website's content and configuration on Sourcehut and GitHub; for the Hugo static site generator; and for the PaperMod theme.

## Interaction

