# Web Archiving Introduction

## Introduction
Search engines depend on indexes which are built by crawling and caching the content of the web. While for search engines this caching can be temporary (before the relevant data is extracted into an index) it overlaps significantly with web archiving and using open crawl data often involves working with web archiving formats and tooling.

In this document we'll be particularly interested in discussing the file formats utilized in modern web archiving.

## Origins
The [ARC](https://archive.org/web/researcher/ArcFileFormat.php) format was created by the [Internet Archive](https://archive.org/) for use with it's Wayback Machine. It's success is WARC, released in a "finalized" form in 2009, this format (and subsequent revisions) continues to be the mainstay of web archiving.

## WARC Format
- [Official Standard Specifications for WARC 1.1](https://iipc.github.io/warc-specifications/specifications/warc-format/warc-1.1/)
- Karl-Rainer Blumenthal. [The stack: An introduction to the WARC file](https://ait.blog.archive.org/post/the-stack-warc-file/). Archive.org, 4/2021.
    - A great introductory article to WARC including it's history, purpose, and implementation.
- [Wikipedia on Web ARChive](https://en.wikipedia.org/wiki/Web_ARChive)

A WARC file contains WARC records which are composed of eight pieces, six of which are actually utilized currently:
- warcinfo - information about the request, "good provenance information" as Blumenthal puts it.
- request - The HTTP request made by the archiving tool to the website that results in the response received.
- response - The response received from the website (including file contents).
- revisit - A record that has been previously archived and hasn't changed in subsequent visit.
- resource - May include screenshots, videos of the page.
- conversion - Conversion of older data into a current format (e.g. as an image standard is deprecated this might contain a replacement image in a new format).
- continuation - Allows one to reference another WARC record that contains the remainder of the record.
- metadata - Various metadata depending on the archiving source.

They can be opened with a text editor (although many WARC files are quite large and may require a special editor with large file support).

## WAT Format
Includes data extracted from the WARC format using JSON. Includes metadata, request, and response as well as the links extracted from the page.

## WET Format
Includes data extracted from a WARC in plaintext.

## Bibliography/Resources
- Archive.org
    - Note that the Internet Archive maintains a [general blog](https://blog.archive.org/) but for those interested in more technical aspects of the Archive, see the [Archive-It blog](https://ait.blog.archive.org/), which also covers general Archive-It news along with some technical posts.
        - [A New Wayback: Improving Web Archive Replay](https://ait.blog.archive.org/post/archive-it-wayback-release/). 9/2021.
        - Karl-Rainer Blumenthal. [The stack: A guide to A/V web archiving with youtube-dl](https://ait.blog.archive.org/post/the-stack-youtube-dl-guide/). 1/2021.
        - Karl-Rainer Blumenthal. [The stack: High fidelity web collecting at scale with Brozzler](https://ait.blog.archive.org/post/the-stack-brozzler/). 11/2020.
        - Molly Bragg, Kristine Hanna, et al. [Web Archiving Lifecycle Model](https://ait.blog.archive.org/learn-more/publications/web-archiving-life-cycle-model/). 3/2013.
- CommonCrawl.org
    - Stephen Merity. [Navigating the WARC file format](https://commoncrawl.org/2014/04/navigating-the-warc-file-format/). 4/2014.
        - Brief introduction to the WARC format, but perhaps more importantly (as the info seems less readibly available around the web), discusses the WET and WAT formats.