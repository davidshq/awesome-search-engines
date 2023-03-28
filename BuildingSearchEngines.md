# Building Search Engines

## Table of Contents
- [Open Source Search Engines](OpenSourceSearchEngines.md)
- Open Source Web Crawlers
    - Apache Nutch
    - StormCrawler
    - CoCrawler
    - Norconex Web Crawler
    - PulsarR
    - Heritrix
- Common Crawl
    - General
    - Tooling
- Wikimedia Search
- Books on Search and Information Retrieval
- Research on Search and Information Retrieval
- Footnotes

## Open Source Search Engines
- I've broken this section out into it's own page, see [Open Source Search Engines](OpenSourceSearchEngines.md).

## Open Source Web Crawlers

### Apache Nutch
- https://nutch.apache.org/
- Probably the best known and most utilized open source web crawler.
- [Nutch Tutorial](https://cwiki.apache.org/confluence/display/NUTCH/NutchTutorial) - The official tutorial for getting started with Nutch.

### StormCrawler
- http://stormcrawler.net/index.html
- [GitHub Repo](https://github.com/DigitalPebble/storm-crawler)
- Open source web crawler built on Apache Storm.

### CoCrawler
- https://github.com/cocrawler/cocrawler
- Authored by Greg Lindahl (Blekko) in Python, pre-release.

### Norconex Web Crawler
- https://opensource.norconex.com/crawlers/web/
- [GitHub Repo](https://github.com/Norconex/collector-http)
- Open source Java web crawler.

### PulsarR
- https://github.com/platonai/pulsarr
- Open source web crawler written in Kotlin.

### Heritrix
- https://heritrix.readthedocs.io/en/latest/
- [GitHub Repo](https://github.com/internetarchive/heritrix3)
- Open source web crawler written in Java by the Internet Archive.

### Comparisons
- Rody. [Comparison of Open Source Web Crawlers for Data Mining and Web Scraping: Pros & Cons](https://outsourceit.today/comparison-open-source-web-crawlers/). outsourceit.today, 10/2022.
    - Covers Scrapy, Heritrix, Nutch, and PySpider.


## Common Crawl
Common Crawl is a non-profit organization that maintains a large index of the web that is updated on a bi-monthly basis and freely available.

### General
- Official Site: https://commoncrawl.org/
- GitHub Repositories: https://github.com/commoncrawl - A few of the repositories are listed below, but there are many more.
    - [Common Crawl WARC Examples](https://github.com/commoncrawl/cc-warc-examples) - "This repository contains both wrappers for processing WARC files in Hadoop MapReduce jobs and also Hadoop examples to get you started."
    - [Jupyter Notebooks to Analyze Common Crawl Data](https://github.com/commoncrawl/cc-notebooks) - This includes several different notebooks, some may be especially interested in [running a notebook on AWS EMR](https://github.com/commoncrawl/cc-notebooks/blob/main/cc-emr-notebook/cluster_setup.md).
    - [Common Crawl PySpark Examples](https://github.com/commoncrawl/cc-pyspark) - "This project provides examples [of] how to process the Common Crawl dataset with Apache Spark and Python".
    - [Common Crawl Index Server](https://github.com/commoncrawl/cc-index-server) - "This project is a deployment of the pywb web archive replay and index server to provide an index query mechanism for datasets provided by Common Crawl".

### Tooling
- [cdx_toolkit](https://github.com/cocrawler/cdx_toolkit) - "a set of tools for working with CDX indices of web crawls and archives, including those at CommonCrawl and the Internet Archive's Wayback Machine."

## Wikimedia Search
- https://www.mediawiki.org/wiki/Wikimedia_Search_Platform
- https://www.mediawiki.org/wiki/User:TJones_(WMF)/Notes

## Covers Search Related Topics
- [Algolia's Blog](https://algolia.com/)

## Books on Search and Information Retrieval
- Please see the [Books on Search and Information Retrieval](/research/books-research.md) page for information on various books published regarding search/IR.

## Research on Search and Information Retrieval
- Please see the [Research on Search and Information Retrieval](/research/research-main.md) pages for information on studies, journal articles, etc. regarding search/IR.

## Footnotes
[^controversy]: The fork was started following controversial licensing changes by Elasticsearch. For more on the history of this controversy see Graham Gillen's [Elasticsearch vs OpenSearch series](https://pureinsights.com/blog/2021/elasticsearch-vs-opensearch-user-point-of-view-part-1-of-3/). For a brief evaluation of OpenSearch's progress see Matt Asay's [One year of OpenSearch: Grading AWS’ open source effort](https://www.techrepublic.com/article/opensearch-grading-aws-open-source/).
[^typesense]: Some interesting functionality includes tunable ranking, sorting, faceting & filtering, grouping & distinct, federated search, and curation. It doesn't appear to be in web scale usage but they've expressed interest in benchmarking larger datasets so I submmited an [issue requesting CommonCrawl be benchmarked](https://github.com/typesense/typesense/issues/933).
[^opensemanticsearch]: It isn't meant for web search particularly but it offers a number of features which could be useful in a search engine - e.g. exploratory search as well as collaborative annotation and tagging.
[^mwmbl]: The project has some similarities with what I'm looking to do with [Phoebe](https://github.com/davidshq/next-search/). It is open source, a non-profit, and the code is written in Python.