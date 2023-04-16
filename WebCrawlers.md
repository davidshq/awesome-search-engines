# Open Source Web Crawlers

## Table of Contents
- Comments
- General Resources
- Apache Nutch
- StormCrawler
- Scrapy
- Norconex Web Crawler
- PulsarR
- Heritrix
- Sparkler
- CoCrawler
- Comparisons
- Other
- Maybe...?

## Comments
- This page focuses on web crawlers/spiders as opposed to web scrapers. While there can be significant overlap between the two, our goal is to evaluate systems that are meant for web scale crawling.
- This document focuses on general purpose web crawlers. There is a growing niche of crawlers created specifically for security purposes which are not covered here.
- We focus primarily on projects which are being actively developed. Projects which are showing limited signs of life may not be included. If you feel we've passed over a project that should be included, please create an issue or pull request.

## General Resources
- [Awesome Crawler](https://github.com/BruceDone/awesome-crawler) - Stars: 5.5k - Updated: 12/2022 - Checked: 4/2023.

## Apache Nutch
- https://nutch.apache.org/
- [GitHub Repo](https://github.com/apache/nutch)
    - Stars: 2.6k - Updated: 3/2023 - Checked: 4/2023.
- Probably the best known and most utilized open source web crawler.
- [Nutch Tutorial](https://cwiki.apache.org/confluence/display/NUTCH/NutchTutorial) - The official tutorial for getting started with Nutch.

## StormCrawler
- http://stormcrawler.net/index.html
- [GitHub Repo](https://github.com/DigitalPebble/storm-crawler)
    - Stars: 795 - Updated: 4/2023 - Checked: 4/2023.
- Open source web crawler built on Apache Storm.

## Scrapy
- https://scrapy.org/
- [GitHub Repo](https://github.com/scrapy/scrapy)
    - Stars: 9.9k - Updated: 4/2023 - Checked: 4/2023.
- A popular, open source web crawler/scraper written in Python.

## Norconex Web Crawler
- https://opensource.norconex.com/crawlers/web/
- [GitHub Repo](https://github.com/Norconex/collector-http)
    - Stars: 153 - Updated: 2/2023 - Checked: 4/2023.
- Open source Java web crawler.

## PulsarR
- https://github.com/platonai/pulsarr
- Open source web crawler written in Kotlin.

## Heritrix
- https://heritrix.readthedocs.io/en/latest/
- [GitHub Repo](https://github.com/internetarchive/heritrix3)
    - Stars: 2.4k - Updated: 3/2023 - Checked: 4/2023.
- Open source web crawler written in Java by the Internet Archive.
- See also Internet Archive's browser-based distributed crawler, [brozzler](https://github.com/internetarchive/brozzler).

## Sparkler
- http://irds.usc.edu/sparkler/
- [GitHub Repo](https://github.com/USCDataScience/sparkler)
    - Stars: 400 - Updated: 4/2023 - Checked: 4/2023.
- A next-generation successor to Apache Nutch that uses Spark, Kafka, Lucene/Solr, Tika, and pf4j.

## CoCrawler
- [GitHub Repo](https://github.com/cocrawler/cocrawler)
    - Stars: 166 - Updated: 4/2022 - Checked: 4/2023.
- Authored by Greg Lindahl (Blekko) in Python, pre-release.
    - Included primarily because Lindahl has a proven track record in web crawling.

## Comparisons
- Rody. [Comparison of Open Source Web Crawlers for Data Mining and Web Scraping: Pros & Cons](https://outsourceit.today/comparison-open-source-web-crawlers/). outsourceit.today, 10/2022.
    - Covers Scrapy, Heritrix, Nutch, and PySpider.

## Other
- [Crawlab](https://github.com/crawlab-team/crawlab) - Stars: 9.7k - Updated: 4/2023 - Checked: 4/2023.
    - A Go language, distributed web crawler admin platform that works with multiple languages and frameworks including Scrapy.
    - NOTE: Does not appear to have integrations with most web scale crawlers, e.g. Nutch or StormCrawler.

## Maybe...?
- This section includes a few crawlers that are in development and show some promise.

- [Crawler](https://github.com/crwlrsoft/crawler) - Stars: 233 - Updated: 3/2023 - Checked: 4/2023.
    - Including this one because it's written in PHP, which isn't particularly common for web crawlers.
- [SeimiCrawler](https://github.com/zhegexiaohuozi/SeimiCrawler) - Stars: 1.9k - Updateds: 4/2023 - Checked: 4/2023.
    - A Java-based, distributed, open source web crawler.
- [XXL-CRAWLER](https://www.xuxueli.com/xxl-crawler/) - Stars: 654 - Updated: 10/2022 - Checked: 4/2023.
    - A Java-based, distributed, open source web crawler.
- [Sparkler-Crawler](https://github.com/USCDataScience/sparkler) - Stars: 400 - Updated: 4/2023 - Checked: 4/2023.
    - A Java/Scala based web crawler built on Spark.
- [crawler](https://github.com/a11ywatch/crawler) - Stars: 22 - Updated: 4/2023 - Checked: 4/2023.
    - A Rust, open source web crawler that claims it is "capable of handling millions of pages per second efficiently."
- [colly](https://github.com/gocolly/colly) - Stars: 19.3k - Updated: 4/2023 - Checked: 4/2023.
    - A Go language open source frmework for building crawlers/scrapers/spiders.
- [Montferret](https://www.montferret.dev/) - Stars: 5.3k - Updated: 4/2023 - Checked: 4/2023.
    - A Go language, open source web scraper. Letting it slide in for its interesting declarative approach.