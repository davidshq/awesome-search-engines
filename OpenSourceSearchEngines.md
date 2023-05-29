# Open Source Search Engines

## Table of Contents
- Apache Lucene
    - Lucene++
- Apache Solr
- Open Semantic Search
    - Subprojects
        - Solr PHP UI
- Elasticsearch
    - Other Projects
        - dejavu
        - Fess
        - Searchkit
- OpenSearch
    - Other Projects
- Gigablast
- [YaCy](/specific-engines/yacy.md)
    - Articles
- Vald
- Weaviate
- MWMBL
- Alexandria
- Wiby
- OpenSearchServer
- Metasearch
    - MetaGer
- Not Web Scale
    - meilisearch
    - Typesense
- Smaller Engines
    - Sonic
    - ZincSearch

## Apache Lucene
- https://lucene.apache.org/
- The open source Java library that powers Apache Solr and Elasticsearch, among many other search projects.

### Lucene++
- https://github.com/luceneplusplus/LucenePlusPlus
- An open source C++ port of Lucene.

## Apache Solr
- https://solr.apache.org/
- See also dedicated pages [on Solr](/specific-engines/apache-solr.md)

## Open Semantic Search
- https://opensemanticsearch.org/
- Under the hood one is running Apache Solr, but there are some significant changes that make listing Open Semantic Search separately worthwile.[^opensemanticsearch]

### Subprojects
- [Solr PHP UI](https://opensemanticsearch.org/solr-php-ui/) - A frontend for Open Semantic Search.
    - [GitHub Repo](https://github.com/opensemanticsearch/solr-php-ui)

## Elasticsearch
- https://elastic.co/
- Used by Wikipedia

### Other Projects
- [dejavu](https://github.com/appbaseio/dejavu) - Open source, JS web-based UI for Elasticsearch and OpenSearch.
- [Fess](https://fess.codelibs.org/) - Open source, enterprise search server with web crawler and GUI. Written in Java.
- [Searchkit](https://github.com/searchkit/searchkit) - Updated: 3/2023 - Checked: 3/2023 - Stars: 4.6k - Open source library for building search UI's with JS, React, Vue, Angular, etc. Written in TypeScript primarily.

## OpenSearch
- https://opensearch.org/
- An open source fork of Elasticsearch started by Amazon.[^controversy]

### Other Projects
- Please see Other Projects under Elasticsearch. Only projects that are for OpenSearch exclusively will be listed here.

## Gigablast
- https://gigablast.com/
- [GitHub Repo](https://github.com/gigablast/open-source-search-engine)
- Founded in 2000 by Matt Wells as a closed source search engine it was later open sourceed. It is written in C++, is distributed, and includes both the engine and a crawler.

## YaCy
- Please see the [dedicated page on YaCy](/specific-engines/yacy.md).

## Vald
- https://vald.vdaas.org/
- [GitHub Repo](https://github.com/vdaas/vald)
- An open source, distributed vector search engine built using Go, utilized by Yahoo Japan.

## Weaviate
- https://weaviate.io/
- [GitHub Repo](https://github.com/weaviate/weaviate)
- Open source vector search engine written in Go.
- [Semantic Search through Wikipedia with Weaviate](https://github.com/weaviate/semantic-search-through-wikipedia-with-weaviate)

## MWMBL
- https://mwmbl.org/
- [GitHub Repo](https://github.com/mwmbl/mwmbl)
- Open source, non-profit search engine written in Python.[^mwmbl]

## Alexandria
- https://www.alexandria.org/
- [GitHub Repo](https://www.alexandria.org/)
- Open source search engine that uses CommonCrawl and is written in C++.

## Wiby
- https://wiby.me/
- [GitHub Repo](https://github.com/wibyweb/wiby)
- [Installation and Setup Instructions](https://wiby.me/about/guide.html)
- Open source search engine written in PHP, C, and Go.

## OpenSearchServer
- https://www.opensearchserver.com/
- [GitHub Repo](https://github.com/jaeksoft/opensearchserver)
- Open source search engine written in Java, includes bundled crawler.
- Note: No updates since 8/2021 as of 3/2023.

## Metasearch

### MetaGer
- https://metager.org/
- [Git Repo](https://gitlab.metager.de/open-source/MetaGer)
- Open source metasearch engine run by a nonprofit.

## Not Web Scale

### meilisearch
- https://www.meilisearch.com/
- [GitHub Repo](https://github.com/meilisearch/meilisearch)
- An open source search engine written in Rust.

### Typesense
- https://typesense.org/
- [GitHub Repo](https://github.com/typesense/typesense)
- An open source Algolia alternative written in C/C++.[^typesense]

## Smaller Engines
- [Sonic](https://github.com/valeriansaliou/sonic) - Updated: 1/2023 - Checked: 3/2023 - Stars: 18k - A lightweight, speedy search backend written in Rust.
- [ZincSearch](https://github.com/zincsearch/zincsearch) - Updated: 3/2023 - Checked: 3/2023 - Stars: 14.7k - Lightweight alternative to Elasticsearch, written in Go. Includes a web UI.

## Footnotes
[^controversy]: The fork was started following controversial licensing changes by Elasticsearch. For more on the history of this controversy see Graham Gillen's [Elasticsearch vs OpenSearch series](https://pureinsights.com/blog/2021/elasticsearch-vs-opensearch-user-point-of-view-part-1-of-3/). For a brief evaluation of OpenSearch's progress see Matt Asay's [One year of OpenSearch: Grading AWS’ open source effort](https://www.techrepublic.com/article/opensearch-grading-aws-open-source/).
[^typesense]: Some interesting functionality includes tunable ranking, sorting, faceting & filtering, grouping & distinct, federated search, and curation. It doesn't appear to be in web scale usage but they've expressed interest in benchmarking larger datasets so I submmited an [issue requesting CommonCrawl be benchmarked](https://github.com/typesense/typesense/issues/933).
[^opensemanticsearch]: It isn't meant for web search particularly but it offers a number of features which could be useful in a search engine - e.g. exploratory search as well as collaborative annotation and tagging.
[^mwmbl]: The project has some similarities with what I'm looking to do with [Phoebe](https://github.com/davidshq/next-search/). It is open source, a non-profit, and the code is written in Python.