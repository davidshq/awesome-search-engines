# Building Search Engines

## Table of Contents
- Open Source Search Engines
    - Apache Lucene
        - Lucene++
    - Apache Solr
        - Other Projects
        - Open Semantic Search
            - Subprojects
    - Elasticsearch
    - OpenSearch
    - Gigablast
    - YaCy
    - Vald
    - Weaviate
    - MWMBL
    - Alexandria
    - Wiby
    - OpenSearchServer
- Meta Search
    - MetaGer
- Not Web Scale
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

#### Lucene++
- https://github.com/luceneplusplus/LucenePlusPlus
- An open source C++ port of Lucene.

### Apache Solr
- https://solr.apache.org/

#### Other Projects
- [Blacklight](https://projectblacklight.org/) - A Ruby on Rails open source frontend for querying and discovery of results from Solr.
- [AJAX Solr](https://github.com/evolvingweb/ajax-solr) - JS library for building UI's for Solr. No updates since 10/2021 as of 3/2023.

### Open Semantic Search
- https://opensemanticsearch.org/
- Under the hood one is running Apache Solr, but there are some significant changes that make listing Open Semantic Search separately worthwile.[^opensemanticsearch]

#### Subprojects
- [Solr PHP UI](https://opensemanticsearch.org/solr-php-ui/) - A frontend for Open Semantic Search.
    - [GitHub Repo](https://github.com/opensemanticsearch/solr-php-ui)

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

### YaCy
- https://yacy.net/
- [GitHub Repo](https://github.com/yacy/yacy_search_server)
- An open source, distributed, P2P search engine built in Java with a focus on user privacy and decentralization. It's been around for a long time and continues to be actively developed. Includes a crawler.

### Vald
- https://vald.vdaas.org/
- [GitHub Repo](https://github.com/vdaas/vald)
- An open source, distributed vector search engine built using Go, utilized by Yahoo Japan.

### Weaviate
- https://weaviate.io/
- [GitHub Repo](https://github.com/weaviate/weaviate)
- Open source vector search engine written in Go.
- [Semantic Search through Wikipedia with Weaviate](https://github.com/weaviate/semantic-search-through-wikipedia-with-weaviate)

### MWMBL
- https://mwmbl.org/
- [GitHub Repo](https://github.com/mwmbl/mwmbl)
- Open source, non-profit search engine written in Python.[^mwmbl]

### Alexandria
- https://www.alexandria.org/
- [GitHub Repo](https://www.alexandria.org/)
- Open source search engine that uses CommonCrawl and is written in C++.

### Wiby
- https://wiby.me/
- [GitHub Repo](https://github.com/wibyweb/wiby)
- Open source search engine written in PHP, C, and Go.

### OpenSearchServer
- https://www.opensearchserver.com/
- [GitHub Repo](https://github.com/jaeksoft/opensearchserver)
- Open source search engine written in Java, includes bundled crawler.
- Note: No updates since 8/2021 as of 3/2023.

### Metasearch

#### Metager
- https://metager.org/
- [Git Repo](https://gitlab.metager.de/open-source/MetaGer)
- Open source metasearch engine run by a nonprofit.

### Not Web Scale

#### meilisearch
- https://www.meilisearch.com/
- [GitHub Repo](https://github.com/meilisearch/meilisearch)
- An open source search engine written in Rust.

#### Typesense
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

## Covers Search Related Topics
- [Algolia's Blog](https://algolia.com/)

## Books on Search and Information Retrieval
- NOTE: There are currently 36 books in Springer's the Inforamtion Retrieval Series, not all are listed below.
- NOTE: If you are interested in volumes published by Pearson, Manning, Apress, Packt, O'Reilly, Chapman Hall/CRC, Morgan Kaufmann, or Addison-Wesley, you may want to consider a subscription to [O'Reilly Learning](https://oreilly.com/learning) which includes access to a number of volumes from these publishers (check if your specific volumes are included).

### General Audience
- Dirk Lewandowski. Understanding Search Engines. Springer, 3/2023. 307 pp. $45-$60 USD.
- Alexander Halavais. Search Engine Society. Digital Media and Society, 11/2017. 240 pp.
- Ian H. Witten, Marco Gori, Teresa Numerico. Web Dragons: Inside the Myths of Search Engine Technology. Morgan Kaufmann, 7/2010.

#### Ethics
- Rosie Graham. Investigating Google's Search Engine: Ethics, Algorithms, and the Machines Built to Read Us. Bloomsbury Academic, 1/2023. 256 pp.
- Safiya Umoja Noble. Algorithms of Oppression: How Search Engines Reinforce Racism. NYU Press, 2/2018. 248 pp.

### Core
- W. Bruce Croft, Donald Metzler, Trevor Strohman. Search Engines: Information Retrieval in Practice. Pearson, 2/2009. 552 pp. $30+ USD.
    - Available for free from the [University of Massachusetts](https://ciir.cs.umass.edu/irbook/).
- Christopher D. Manning, Hinrich Schütze, Prabhakar Raghavan. Introduction to Information Retrieval. Cambridge University Press, 7/2008.  506 pp. Price: $26-$54 USD.
    - Available for free from [Stanford](https://nlp.stanford.edu/IR-book/information-retrieval-book.html).

### User Perspective
- Karen Markey. Online Searching: A Guide to Finding Quality Information Efficiently and Effectively. Rowman & Littlefield Publishers, 3rd edition. 2/2023. 294 pp. $55-$58 USD.
    - Focused on the user experience of searching, not building, but may be helpful, especially for those new to the field as it addresses some terminology and usability concerns.
- Duncan O. Case. Looking for Information: A Survey of Research on Information Seeking, Needs, and Behavior, 4th edition. Emerald Publishing Limited, 4/2016. 528 pp. $71 - $85 USD.
- Stefan Buttcher, Charles L. A. Clarke, Gordon V. Cormack. Information Retrieval: Implementing and Evaluating Search Engines. The MIT Press, 2/2016. 632 pp. $30-$42 USD.
    - Significant portions of the 2010 edition of this book are [available for free from the official site](https://plg.uwaterloo.ca/~ir/ir/book/). There are 16 chapters in that edition with 7 available for free.

### Practical
- Tommaso Teofili. Deep Learning for Search. Manning Publications, 6/2019. 328 pp.
- John Berryman, Doug Turnbull. Relevant Search: With applications for Solr and Elasticsearch. Manning Publications, 6/2016. 360 pp.
- Martin White. Enterprise Search, 2nd edition. O'Reilly Media, 10/2015. 310 pp.

#### Lucene
- Atri Sharma. Practical Lucene 8: Uncover the Search Capabilities of Your Application. Apress, 10/2020. 114 pp.
- Edwood Ng, Vineeth Mohan. Lucene 4 Cookbook. Packt Publishing, 6/2015. 220 pp.
- Michael McCandless, Erik Hatcher, Otis Gospodnetic. Lucene in Action, 2nd edition. Manning Publications, 7/2010. 475 pp.

#### Solr
- Dikshant Shahi. Apache Solr: A Practical Approach to Enterprise Search. Apress, 12/2015. 328 pp.
- Trey Grainger, Timothy Potter. Solr in Action. Manning Publications, 3/2014. 664 pp.

#### Elasticsearch
- Note: Some of these volumes address to more or less extent the Elastic / ELK Stack, this is about IR but more on a monitoring, logging side than web search.
- Alberto Paro. Elasticsearch 8.x Cookbook, 5th edition. Packt Publishing, 5/2022. 750 pp.
- Asjad Athick, Shay Banon. Getting Started with Elastic Stack 8.0. Packt Publishing, 3/2022. 474 pp.
- Wai Tak Wong. Advanced Elasticsearch 7.0. Packt Publishing, 8/2019. 560 pp.
- Pranav Shukla, Sharath Kumar M N. Learning Elastic Stack 7.0, 2nd edition. 5/2019. 474 pp.
- Abhishek Andhavarapu. Learning Elasticsearch. Packt Publishing, 6/2017. 404 pp.
- Bharvi Dixit. Mastering Elasticsearch 5.x, 3rd edition. 2/2017. 428 pp.
- Bharvi Dixit. Elasticsearch Essentials. Packt Publishing, 1/2016. 240 pp.
- Rafał Kuć, Marek Rogoziński. Mastering Elasticsearch, 2nd edition. Packt Publishing, 2/2015. 434 pp.
- Clinton Gormley, Zachary Tong. Elasticsearch: The Definitive Guide. O'Reilly Media, 1/2015. 724 pp.
- Rafał Kuć, Marek Rogoziński. Elasticsearch Server, 3rd edition. Packt Publishing, 2/2016. 556 pp.

#### Spark
- Alex Thomas. Natural Language Processing with Spark NLP. O'Reilly Media, 6/2020. 364 pp.

#### Sphinx
- Andrew Aksyonoff. Introduction to Search with Sphinx. O'Reilly Media, 4/2011. 148 pp.

### Information Architecture
- Louis Rosenfeld, Peter Morville, Jorge Arango. Information Architecture: For the Web and Beyond, 4th edition. O'Reilly, 9/2015. 483 pp. $37-$51 USD.

### Collaborative
- Chirag Shah. Social Information Seeking: Leveraging the Wisdom of the Crowd. Springer, 7/2017. 204 pp. $24-$25 USD.
- Chirag Shah. Collaborative Information Seeking: The Art and Science of Making the Whole Greater Than the Sum of All. Springer, 8/2014. 206 pp. $26-$98 USD.

### Other
- Anuradha D. Thakare, Shilpa Laddha, Ambika Pawar. Hybrid Intelligent Systems for Information Retrieval. Chapman Hall/CRC, 11/2022. 252 pp. $144 USD.
- Jiawei Han, Jian Pei, Hanghang Tong. Data Mining: Concepts and Techniques, 4th edition. Morgan Kaufmann, 7/2022. 752 pp. $57-122 USD.
- Yi Chang, Hongbo Deng (editors). Query Understanding for Search Engines. Springer, 12/2021. 236 pp. $110-$150 USD.
- Krisztian Balog. Entity-Oriented Search. Springer, 10/2018. 370 pp. $0 (ebook) - $57 USD.
    - Available for free for Amazon Kindle as well as at https://eos-book.org/.
- ChengXiang Zhai and Sean Massung. Text Data Management and Analysis: A Practical Introduction to Information Retrieval and Text Mining. ACM Books, 6/2016. 532 pp. Price: $40-$80 USD.
- Gerald Kowalski. Information Retrieval Systems: Theory and Implementation. Springer, 3/2013. 300 pp. $25-$147 USD.
- Tyler Tate, Tony Russell-Rose. Designing the Search Experience: The Information Architecture of Discovery. Morgan Kaufmann, 1/2013. 320 pp. $5-$28 USD.
- Giovanni Maria Sacco, Yannis Tzitzikas (editors). Dynamic Taxonomies and Faceted Search: Theory, Practice, and Experience. Springer, 3/2012. 357 pp. $32-$120 USD.
- Amy N. Langville, Carl D. Meyer. Google's PageRank and Beyond: The Science of Search Engine Rankings. Princeton University Presss, 2/2012. 240 pp. $10-$30 USD.
- Marcia J. Bates. Understanding Information Retrieval Systems: Management, Types, and Standards. Auerbach Publications, 12/2011. 752 pp. $51-$159 USD.
- Tie-Yan Liu. Learning to Rank for Information Retrieval. Springer, 4/2011. 302 pp. $45-$125 USD.
- Ricardo Baeza-Yates, Berthier Ribeiro-Neto. Modern Information Retrieval: The Concepts and Technology Behind Search, 2nd edition. Addison-Wesley Professional, 2/2011. 913 pp. $35-$53 USD.
    - Chapters 1 and 10 are available for free at: https://people.ischool.berkeley.edu/~hearst/irbook/, Chapters 1-2, 11, and 15 are available here: https://www.baeza.cl/mir2ed/contents.php.html.
- Peter Morville, Jeffery Callender. Search Patterns: Design for Discovery. O'Reilly, 2/2010. 192 pp. $9-$28 USD.
- Bo Long, Yi Chang. Relevance Ranking for Vertical Search Engines. Morgan Kaufmann, 1/2014. 264 pp.

### Older
- Michael W. Berry, Murray Browne. Understanding Search Engines: Modeling and Text Retrieval, 2nd edition. Society for Industrial and Applied Mathematics, 5/2005. 184 pp. $38-$53 USD.
- David A. Grossman, Ophir Frieder. Information Retrieval: Algorithms and Heuristics. Springer, 10/2004. 352 pp. $17-$164 USD.
- Gerhard Weikum, Gottfried Vossen. Transactional Information Systems: Theory, Algorithms, and the Practice of Concurrency Control and Recovery. Morgan Kaufmann, 6/2001. 872 pp. $62-$100 USD.
- Richard K. Belew. Finding Out About: A Cognitive Perspective on Search Engine Technology and the WWW. Cambridge University Press, 1/2001. 384 pp.
- Ian H. Witten, Alistair Moffat, Timothy C. Bell. Managing Gigabytes: Compressing and Indexing Documents and Images, 2nd edition. Morgan Kaufmann, 5/1999. 560 pp.  $19-$82 USD.
- Karen Sparck Jones, Peter Willett (editors). Readings in Information Retrieval. Morgan Kaufmann, 7/1997. 587 pp. $16 USD.
- William Frakes, Ricardo Baeza-Yates (editors). Information Retrieval: Data Structures & Algorithms. Pearson College Divison, 1/1992. 464 pp. $4-$55 USD.

## Footnotes
[^controversy]: The fork was started following controversial licensing changes by Elasticsearch. For more on the history of this controversy see Graham Gillen's [Elasticsearch vs OpenSearch series](https://pureinsights.com/blog/2021/elasticsearch-vs-opensearch-user-point-of-view-part-1-of-3/). For a brief evaluation of OpenSearch's progress see Matt Asay's [One year of OpenSearch: Grading AWS’ open source effort](https://www.techrepublic.com/article/opensearch-grading-aws-open-source/).
[^typesense]: Some interesting functionality includes tunable ranking, sorting, faceting & filtering, grouping & distinct, federated search, and curation. It doesn't appear to be in web scale usage but they've expressed interest in benchmarking larger datasets so I submmited an [issue requesting CommonCrawl be benchmarked](https://github.com/typesense/typesense/issues/933).
[^opensemanticsearch]: It isn't meant for web search particularly but it offers a number of features which could be useful in a search engine - e.g. exploratory search as well as collaborative annotation and tagging.
[^mwmbl]: The project has some similarities with what I'm looking to do with [Phoebe](https://github.com/davidshq/next-search/). It is open source, a non-profit, and the code is written in Python.