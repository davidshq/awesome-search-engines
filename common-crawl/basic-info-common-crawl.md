# Basic Information About Common Crawl

## Introduction
Common Crawl is a non-profit organization (founded by Gil Elbaz) which for years has been crawling the web in a similar manner to major search engines such as Google and Bing. The data is then made available for [free and under a non-restrictive license](https://commoncrawl.org/terms-of-use/) for usage by anyone who desires to use it.

Common Crawl has been around for eons in internet years (since 2008) and has a number of well-known individuals on it's Board of Directors and Advisory Board.

Amazingly, the CC is currently primarily maintained by a single individual - Sebastian Nagel.

## That Said...
It does appear that CC has probably seen a decrease in funding over the years. The variety of voices on the blog has decreased markedly since ~2015, roughly when Lisa Green left her position as Director of Common Crawl (although she remains on the Board of Advisors) and more recently as crawls have become a bi-monthly event (formerly monthly). My sincere appreciation to Nagel who continues to carry the torch of an important project! I hope that funding and contributors will increase in the near future!

## Crawler
The web crawler (CCBot) is built on the famous open source Apach Nutch engine and utilizes Apache Hadoop.

## Data
The data is stored on Amazon Web Services' (AWS) S3 storage service. It can be accessed over HTTP (slow), using other AWS systems (e.g. EC2, Athena), and using the AWS CLI/SDK.

## Bibliography
- [Common Crawl](https://commoncrawl.org/)
    - [About](https://commoncrawl.org/about/)
        - [Our Team](https://commoncrawl.org/about/team/)
