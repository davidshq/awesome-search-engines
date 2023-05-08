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
- rokasramas' [fork of comcrawl](https://github.com/rokasramas/comcrawl) - Stars: 0 - Updated: 4/2020 - Checked: 5/2023 - Includes a fix that hasn't been applied to the [original comcrawl library](https://github.com/michaelharms/comcrawl/) that allows it to work.
- [getallurls](https://github.com/lc/gau) - Stars: 2.8k - Updated: 2/2023 - Checked: 5/2023 - Can fetch urls from Common Crawl as well as Open Threat Exchange, the Wayback Machine, and URLScan.
- [CommonCrawlDocumentDownload](https://github.com/centic9/CommonCrawlDocumentDownload) - Stars: 50 - Updated: 4/2023 - Checked: 5/2023 - Downloads documents by file/mime type from CC.
- [WARCannon](https://github.com/c6fc/warcannon) - Stars: 212 - Updated: 9/2022 - Checked: 5/2023 - Uses AWS to at scale search Common Crawl data with regex patterns.

## Other
- [NewsFetch](https://newsfetch.tech/) - Stars: 13 - Updated: 10/2022 - Checked: 5/2023 - Can fetch news articles from the Common Crawl API.
- [news-please](https://github.com/fhamborg/news-please) - Stars: 1.6k - Updated: 4/2023 - Checked: 5/2023 - Along with significant other functionality it can fetch articles from Common Crawl.
- [PWA Store](https://github.com/Tarasa24/PWA-Store) - Stars: 5 - Updated: 9/2022 - Checked: 5/2023 - Uses Common Crawl and EMR to find as many PWA apps on the web as possible.

## What Is?
- C4 Dataset - Text data extracted from Common Crawl.
    - https://github.com/shjwudp/c4-dataset-script
- [CDX](https://github.com/webrecorder/pywb/wiki/CDX-Index-Format) - Capture/Crawl inDeX - Standard index format for WARCs.

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
- Athul Jayson. [Extracting Data from Common Crawl Dataset](https://blog.qburst.com/2020/07/extracting-data-from-common-crawl-dataset/). qburst, 7/2020.
    - Also has an associated GitHub repository.
- Ryan Elkins. [Search the html across 25 billion websites for passive reconnaissance using common crawl](https://medium.com/@brevityinmotion/search-the-html-across-25-billion-websites-for-passive-reconnaissance-using-common-crawl-7fe109250b83). 7/2020.
    - While written from a security perspective it provides solid guidance to using AWS Athena with Common Crawl. It also utilizes Amazon SageMaker, S3, and AWS IAM. There is an associated repo.

### AWS EMR
- Basil Latif. [Measuring Internet Links: Accessing the Common Crawl Dataset Using EMR and Pyspark in AWS](https://basil-latif.medium.com/measuring-internet-links-accessing-the-common-crawl-dataset-using-emr-and-pyspark-in-aws-fcf5eb26afd9). 6/2020.
- [Common Crawl EMR Tutorial](https://github.com/haydenhw/commoncrawl-emr-tutorial) - Stars: 9 - Updated: 3/2021 - Checked: 5/2023 - "This guide walks you through submitting a Scala Spark application to EMR that queries 500k job urls from Common Crawl and saves the results to an S3 bucket in CSV format."

### AWS Lambda
- Chris Madden, Aaron Bawcom. [Analyzing Performance and Cost of Large-Scale Data Processing with AWS Lambda](https://aws.amazon.com/blogs/apn/analyzing-performance-and-cost-of-large-scale-data-processing-with-aws-lambda/). 6/2019.
    - Covers the high-level process with associated GitHub repository.
- Jader Dias. [One-click to download all the web pages you may want](https://medium.com/@jaderd/one-click-to-download-exactly-the-web-pages-you-may-want-no-matter-how-many-they-are-d4834265a0a3). 6/2022.
    - Builds on using Athena to get data from Common Crawl and AWS Lambda to download it.

### Snowflake
- Venkat Sekar. [Querying TB sized External Tables with Snowflake](https://medium.com/snowflake/querying-tb-sized-external-tables-with-snowflake-5ab14e807d3). 2/1/2022.


### Basic
- David Mackey. [Basic Information About CommonCrawl](common-crawl/basic-info-common-crawl.md). 5/2023.
- David Mackey. [How To Manually Access CommonCrawl](common-crawl/basic-manually-accessing-common-crawl.md). 5/2023.
- Chillar Anand. [Common Crawl On Laptop - Extracting Subset of Data](https://avilpage.com/2022/11/common-crawl-laptop-extract-subset.html). 11/2022.

### Other
- Colin Dellow. [S3 Throughput: Scans vs Indexes](https://code402.com/blog/s3-scans-vs-index/). 2/2020.
    - Is it fasters to scan entire WARC files and attempt to pull just the data required from each WARC file utilizing the index?