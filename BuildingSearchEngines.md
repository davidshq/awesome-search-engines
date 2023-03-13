# Building Search Engines

## Table of Contents
- Open Source Search Engines
    - Apache Lucene
    - Apache Solr
    - Elasticsearch
    - OpenSearch
    - Gigablast
    - meilisearch
    - Typesense
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
- Footnotes

## Open Source Search Engines

### Apache Lucene
- https://lucene.apache.org/
- The open source Java library that powers Apache Solr and Elasticsearch, among many other search projects.

### Apache Solr
- https://solr.apache.org/
- [Blacklight](https://projectblacklight.org/) - A Ruby on Rails open source frontend for querying and discovery of results from Solr.

### Elasticsearch
- https://elastic.co/
- Used by Wikipedia

### OpenSearch
- https://opensearch.org/
- An open source fork of Elasticsearch started by Amazon.[^controversy]

### Gigablast
- https://gigablast.com/
- [GitHub Repo](https://github.com/gigablast/open-source-search-engine)
- Founded in 2000 by Matt Wells as a closed source search engine it was later open sourceed. It is written in C++, is distributed, and includes both the engine and a crawler.

### meilisearch
- https://www.meilisearch.com/
- [GitHub Repo](https://github.com/meilisearch/meilisearch)
- An open source search engine written in Rust.

### Typesense
- https://typesense.org/
- [GitHub Repo](https://github.com/typesense/typesense)
- An open source Algolia alternative written in C/C++.[^typesense]

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

## Footnotes
[^controversy]: The fork was started following controversial licensing changes by Elasticsearch. For more on the history of this controversy see Graham Gillen's [Elasticsearch vs OpenSearch series](https://pureinsights.com/blog/2021/elasticsearch-vs-opensearch-user-point-of-view-part-1-of-3/). For a brief evaluation of OpenSearch's progress see Matt Asay's [One year of OpenSearch: Grading AWS’ open source effort](https://www.techrepublic.com/article/opensearch-grading-aws-open-source/).
[^typesense]: Some interesting functionality includes tunable ranking, sorting, faceting & filtering, grouping & distinct, federated search, and curation. It doesn't appear to be in web scale usage but they've expressed interest in benchmarking larger datasets so I submmited an [issue requesting CommonCrawl be benchmarked](https://github.com/typesense/typesense/issues/933).