# Building Search Engines

## Table of Contents
- [Open Source Search Engines](OpenSourceSearchEngines.md)
- [Open Source Web Crawlers](WebCrawlers.md)
- Building Search Engines General Resources
- Common Crawl
    - General
    - Tooling
- Wikimedia Search
- Sites Covering Search Related Topics
- Tutorials
- [Books on Search and Information Retrieval](/research/books-research.md)
- [Research on Search and Information Retrieval](/research/research-main.md)

## Open Source Search Engines
- I've broken this section out into it's own page, see [Open Source Search Engines](OpenSourceSearchEngines.md).

## General Resources
- [The Open Guide to Search Engineering](https://github.com/open-guides/og-search-engineering)


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

## Sites Covering Search Related Topics
- [Algolia's Blog](https://algolia.com/)

## Tutorials

### For Beginners
- [Build Your Own Search Engine and Web Crawler in 5 Minutes with Node.js, MySQL, and Elasticsearch](https://coderdose.com/build-your-own-search-engine-and-web-crawler-in-5-minutes-with-node-js-mysql-and-elasticsearch/). Coderdose, 3/2023.
- [Web Search Engine: Design and implementation of a Web Search Engine Using Text Mining Techniques](https://www.codeproject.com/Articles/5319612/Web-Search-Engine). Code Project, 12/2021-3/2023.
    - Uses Python and a SQL back-end.