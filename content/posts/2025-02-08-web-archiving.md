---
title: Archiving websites with ArchiveBox and wget
summary: Brief usage notes on ArchiveBox and wget
author: Claudine Chionh
draft: false
date: 2025-02-08
tags: [safeguarding-research, digital-preservation, web-archiving, data-archiving, archivebox, wget]
---

I have been archiving copies of various websites that are in danger of disappearing or changing in the very near future. My two favourite tools for this are ArchiveBox and `wget`. These are just some brief usage notes for my own reference and possibly useful to others. To learn about urgent (early 2025) web- and data-archiving initiatives, visit the [Safeguarding Research forum](https://safeguarding-research.discourse.group/) or follow the `#SafeguardingResearch` and `#DataRescue` hashtags on the fediverse and Bluesky.

## Storage

I am saving archives to an external solid-state drive directly connected to a Mac Mini. Both `wget` and ArchiveBox can save directly to the external drive. This drive was formatted as APFS out of the box and I haven't reformatted it because I don't have enough free time to learn about other filesystems. I'm not very worried about the efficiency or reliability of APFS for casual archiving.

## ArchiveBox -- save individual pages or batches of links

[**ArchiveBox**](https://archivebox.io/) is a suite of Python tools, including command-line and web interfaces, which can save web pages and media in a variety of formats. You can feed it batches of URLs to be saved, or install the [Chrome/chromium extension](https://chromewebstore.google.com/detail/archivebox-exporter/habonpimjphpdnmcfkaockjnffodikoj) (which can be on a different machine from the one running ArchiveBox) and archive as you browse. It can be [installed](https://github.com/ArchiveBox/ArchiveBox/wiki/Quickstart) on macOS or any flavour of Linux or BSD, or even on Windows (using Docker or WSL).

## GNU Wget -- mirror whole websites

[**Wget**](https://www.gnu.org/software/wget/) is one of the output formats available in ArchiveBox and can also be run directly from the command line, with a wide range of [options](https://www.gnu.org/software/wget/manual/html_node/Invoking.html). Besides websites, `wget` can also mirror [FTP](https://en.wikipedia.org/wiki/File_Transfer_Protocol) directories. If you're using some flavour of Linux, BSD, or macOS, `wget` may already be installed, otherwise it can be installed from your package manager.

To mirror a website, I use these options:

```
wget --mirror --page-requisites <url>
```

The [`--mirror`](https://www.gnu.org/software/wget/manual/html_node/Very-Advanced-Usage.html#Very-Advanced-Usage-1) option tells `wget` to [recursively download](https://www.gnu.org/software/wget/manual/html_node/Recursive-Download.html) the starting URL, any links from that URL on the same (sub-)domain, and so on until it runs out of links on the same domain. [`--page-requisites`](https://www.gnu.org/software/wget/manual/html_node/Recursive-Retrieval-Options.html#index-page-requisites) tells it to also fetch any referenced images, media, and stylesheets alongside the HTML.

`wget` can also save [WARC files](https://archive-it.org/post/the-stack-warc-file/), a container file format that records the server traffic made while creating an archive. This option can also be enabled in ArchiveBox.