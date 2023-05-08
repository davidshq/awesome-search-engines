# Common Crawl
Common Crawl is a non-profit organization that maintains a large index of the web that is updated on a bi-monthly basis and freely available.

## General
- Official Site: https://commoncrawl.org/
- Common Crawl Index Server: https://index.commoncrawl.org/
- GitHub Repositories: https://github.com/commoncrawl - A few of the repositories are listed below, but there are many more.
    - [Common Crawl WARC Examples](https://github.com/commoncrawl/cc-warc-examples) - "This repository contains both wrappers for processing WARC files in Hadoop MapReduce jobs and also Hadoop examples to get you started."
    - [Jupyter Notebooks to Analyze Common Crawl Data](https://github.com/commoncrawl/cc-notebooks) - This includes several different notebooks, some may be especially interested in [running a notebook on AWS EMR](https://github.com/commoncrawl/cc-notebooks/blob/main/cc-emr-notebook/cluster_setup.md).
    - [Common Crawl PySpark Examples](https://github.com/commoncrawl/cc-pyspark) - "This project provides examples [of] how to process the Common Crawl dataset with Apache Spark and Python".
    - [Common Crawl Index Server](https://github.com/commoncrawl/cc-index-server) - "This project is a deployment of the pywb web archive replay and index server to provide an index query mechanism for datasets provided by Common Crawl".

## Tooling
- [cdx_toolkit](https://github.com/cocrawler/cdx_toolkit) - Star: 127 - Updated: 3/2022 - Checked: 5/2023 - "a set of tools for working with CDX indices of web crawls and archives, including those at CommonCrawl and the Internet Archive's Wayback Machine."
- rokasramas' [fork of comcrawl] - Stars: 0 - Updated: 4/2020 - Checked: 5/2023 - Includes a fix that hasn't been applied to the original comcrawl library that allows it to work.

## What Is?
- C4 Dataset - Text data extracted from Common Crawl.
    - https://github.com/shjwudp/c4-dataset-script

## Tutorials

### General
- Edward Ross. [CommonCrawl Category](https://skeptric.com/#category=commoncrawl). skeptric.
    - Ross has published a number of well-written articles on Common Crawl. A great place to start if you are looking to go through the basics and beyond.
    - [Searching 100 Billion Webpages With Capture Index](https://skeptric.com/searching-100b-pages-cdx/). 6/2020.
        - Explains how to use the web interface (slow) as well as the CDX Toolkit, comcrawl, and directly in Python without using a custom CommonCrawl library. Unfortunately both comcrawl and the CDX Toolkit require some tweaks to get running.
    - [Read Commonm Crawl Parquet Metadata with Python](https://skeptric.com/reading-parquet-metadata/). 4/2022.
        - Covers reading Parquet metadata using PyArrow, fastparquet, manually (in Python), and using asyncio to speed things up.
- [CommonCrawl.org So you're ready to get started](https://commoncrawl.org/the-data/get-started/).
    - Covers a lot of ground, perhaps not the best for true beginners. Covers data locations, file formats (WARC, WAT, WET), indexes, as well as processing the files.
- [CommonCrawl.org Examples using Common Crawl Data](https://commoncrawl.org/the-data/examples/).
    - Unfortunately the vast majority of the examples available here are quite old.

### AWS Athena
- Sebastian Nagel. [Index to WARC Files and URLs in Columnar Format](https://commoncrawl.org/2018/03/index-to-warc-files-and-urls-in-columnar-format/). commoncrawl, 3/2018.
- Stanislas Girard. [Parse Petabytes of data from CommonCrawl in seconds](https://www.primates.dev/parse-petabytes-of-data-from-commoncrawl-in-seconds/). primates.dev, 1/2020.
    - Simple and straightforward, short, fairly basic, but good place to start.

### Basic
- David Mackey. [Basic Information About CommonCrawl](common-crawl/basic-info-common-crawl.md). 5/2023.
- David Mackey. [How To Manually Access CommonCrawl](common-crawl/basic-manually-accessing-common-crawl.md). 5/2023.