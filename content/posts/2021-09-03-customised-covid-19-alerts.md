---
title: Customised Covid-19 alerts
description: Moderating my anxiety with customised Covid-19 alerts
slug: customised-covid-19-alerts
draft: false
date: 2021-09-03
lastmod: 2021-09-03
images:
  - /images/2021-09-03-pushcut-exposure-alert.jpg
  - /images/2021-09-02-pushcut-whattimedan.jpg
tags:
  - covid-19
  - ios
  - javascript
  - python
  - raspberrypi
---

{{< archive-disclaimer >}}

Since my [last post](/posts/victorian-covid-19-exposure-site-highlighter/), the number of {{< archive-robustlink text="Victorian Covid-19 exposure sites" originalurl="https://www.coronavirus.vic.gov.au/exposure-sites" versionurl="https://web.archive.org/web/20210902233457/https://www.coronavirus.vic.gov.au/exposure-sites" versiondate="2021-09-02" >}} has climbed to over 1000. It isn't healthy for me to park myself on that page and constantly refresh it, or to constantly watch Twitter for case updates and press conferences. I've built a couple more small tools to send me alerts when they're relevant, so I don't need to have those browser tabs of doom open all the time. (That doesn't mean I don't sometimes spend hours on Twitter anyway, but at least I know I can tear myself away without missing important alerts.) Building tools to tune the cacophony of information has also done a little to focus and calm my mind in this distressing period.

This is a system that works for me. It might not suit your needs or your technology setup, but if you want to build your own Covid-19 alert system, this might give you some ideas.

I use the following Free tools:

- [JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
- [Python](https://www.python.org/)
- {{< archive-robustlink text="Victorian Government Covid-19 exposure site data" originalurl="https://discover.data.vic.gov.au/dataset/all-victorian-sars-cov-2-covid-19-current-exposure-sites" versionurl="https://web.archive.org/web/20210627233551/https://discover.data.vic.gov.au/dataset/all-victorian-sars-cov-2-covid-19-current-exposure-sites" versiondate="2021-06-28" >}}
- [Violentmonkey](https://violentmonkey.github.io/) userscript manager

and these non-Free ones:

- [Due](https://www.dueapp.com/) for iOS (nagging reminders)
- [Pushcut](https://www.pushcut.io/) for iOS (customisable notifications accessible via webhooks)
- [Shortcuts](https://support.apple.com/en-au/guide/shortcuts/welcome/ios) for iOS
- [Zapier](https://zapier.com/)

## Victorian Covid-19 press briefings

![Pushcut notification -- tweet from @WhatTimeDan](/images/2021-09-02-pushcut-whattimedan.jpg)

{{< archive-robustlink text="@WhatTimeDan" originalurl="https://twitter.com/WhatTimeDan" versionurl="https://web.archive.org/web/20201026014012/https://twitter.com/WhatTimeDan" versiondate="2020-10-25" >}} is a Twitter account that does a good job of finding and announcing the time of each day's Victorian Government press briefing. I use Zapier, Pushcut, and Due to create a reminder for the press briefing. {{< archive-robustlink text="Zapier" originalurl="https://zapier.com/apps/twitter/integrations" versionurl="https://web.archive.org/web/20210813110837/https://zapier.com/apps/twitter/integrations" versiondate="2021-08-13" >}} monitors the @WhatTimeDan account and, when they tweet, sends a notification to Pushcut on my iOS devices. I configured the corresponding Pushcut notification to offer a choice of two actions: to create a timed reminder, or (because @WhatTimeDan tweets more than just the press briefing times) to open the tweet to see its context.

The timed reminder action runs an iOS shortcut that takes the text of the tweet and sends it to Due, which intelligently reads the time of day from the given text and schedules a persistent reminder when the press briefing is supposed to start.

## Personalising the table of exposure sites

![Pushcut notification -- nearby exposure site](/images/2021-09-03-pushcut-exposure-alert.jpg)

The table of exposure sites is overwhelming. I previously [posted](/posts/victorian-covid-19-exposure-site-highlighter) about my browser script that adds colour highlights to selected suburbs in the table. This still requires actually visiting the table.

There are tools and bots (including {{< archive-robustlink text="@exposuresitebot" originalurl="https://twitter.com/exposuresitebot" versionurl="https://web.archive.org/web/20210927041243/https://twitter.com/exposuresitebot" versiondate="2021-09-27" >}} and {{< archive-deadlink text="@covid19nearmeau" originalurl="https://twitter.com/covid19nearmeau" >}}) that tweet *all* exposure sites as they are added to the table. Again, I wanted to be notified only of the suburbs that are relevant to my friends, family, and myself. [This Python script](https://github.com/claudinec/vic-exposure-site-alert) queries the exposure site data for chosen suburbs and sends an alert for each new exposure site to Pushcut. I run this script on a Raspberry Pi via `cron` at regular intervals -- every half hour seems reasonable for me at the moment, as I don't get notified unless an exposure has been added in a suburb of interest. I have also just added the ability to customise alerts for selected train, tram, and bus routes.
