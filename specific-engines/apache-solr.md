# Apache Solr
- Introduction
- My Notes
- Related Projects
    - General
    - Discovery and/or UI
    - Language Integrations
        - .NET, Clojure, Go, JS, Java, PHP, Python, Ruby, Scala
    - Application/Framework Integrations
    - Utilities
    - Vector Search
    - Projects Using Solr
- Discussion
- Solr as a Service Options
- Consulting Companies Working with Solr
- Interesting But Old
- Bibliography/Resources

## Introduction
Apache Solr is a search engine built on top of Apache Lucene (a Java library, also used in Elasticsearch). Solr receives queries via HTTP requests and provides responses in JSON by default (but can also output XML, CSV, etc.).

## My Notes
These are largely pulled from Solr's documentation, consider them cliff notes / cheat sheets.
- [Basic Solr Tutorial](./solr/basic-tutorial.md)
- [Basic Solr Admin UI Tutorial](./solr/basic-admin-ui-tutorial.md)
- [Basic SolrCloud Tutorial](./solr/basic-solrcloud-tutorial.md)
- [Basic Indexing Your Own Data Tutorial](./solr/basic-indexing-your-own-data.md)
- [Solr Development](./solr/solr-development.md)
- [Solr Terminology](./solr/solr-terminology.md)
- [Solr Notes Unorganized](./solr/solr-notes.md)

## Related Projects

### General
- [Solr Plugin Directory](https://solr.cool/) - A directory of plugins/extensions available for Solr including query parsers, analyzers, response writers, search components, document transformers, and utilities.

### Discovery and/or UI
- [Blacklight](https://projectblacklight.org/) - Stars: 731 - Updated: 4/2023 - Checked: 5/2023
    - A Ruby on Rails open source frontend for querying and discovery of results from Solr.
    - [Penn State University](https://github.com/psu-libraries/psulib_blacklight)
    - [Stanford University](https://github.com/sul-dlss/exhibits)
    - [Temple University](https://github.com/tulibraries/funcake-solr)
- [AJAX Solr](https://github.com/evolvingweb/ajax-solr) - Stars: 654 - Updated: 10/2021 - Checked: 4/2023 - JS library for building UI's for Solr.
- [SolrDora](https://github.com/hectorcorrea/solrdora) - Stars: 6 - Updated: 1/2023 - Checked: 5/2023*
    - Provides a UI for browsing a Solr collection.
- [YASA (Yet Another Solr Admin)](https://github.com/yasa-org/yasa) - Stars: 47 - Updated: 4/2023 - Checked: 5/2023
    - A web-based UI for administering Solr written with Vue in TypeScript.

### Language Integrations

#### .NET
- [SolrNet](https://github.com/SolrNet/SolrNet) - Stars: 913 - Updated: 5/2023 - Checked: 5/2023

#### Go
- [Solr Go](https://github.com/stevenferrer/solr-go) - Stars: 36 - Updated: 3/2023 - Checked: 5/2023
- [go-solr](https://github.com/vanng822/go-solr) - Stars: 67 - Updated: 9/2022 - Checked: 5/2023

#### JS
- [solr-client for Node.js](https://github.com/lbdremy/solr-node-client) - Stars: 456 - Updated: 3/2022 - Checked: 5/2023


#### JVM (includes Java, Clojure, Scala, etc.)
- [flux](https://github.com/mwmitchell/flux) - Stars: 35 - Updated: 7/2022 - Checked: 5/2023
    - "A Clojure based Solr client."
- [solrs](https://github.com/inoio/solrs) - Stars: 103 - Updated: 4/2023 - Checked: 5/2023
    - "An async, non-blocking solr client for java/scala, providing a query interface like SolrJ"
- [solr-scala-client](https://github.com/takezoe/solr-scala-client) - Stars: 91 - Updated: 9/2022 - Checked: 5/2023

#### PHP
- [Solarium](https://github.com/solariumphp/solarium) - Stars: 911 - Updated: 5/2023 - Checked: 5/2023

#### Python
- [solrcloudpy](https://github.com/solrcloudpy/solrcloudpy) - Stars: 37 - Updated: 2/2021 - Checked: 5/2023

#### Ruby
- [rsolr](https://github.com/rsolr/rsolr) - Stars: 416 - Updated: 2/2022 - Checked: 5/2023
- [solrb](https://github.com/machinio/solrb) - Stars: 38 - Updated: 9/2022 - Checked: 5/2023

### Application/Framework Integrations
- [Dokku Solr](https://github.com/dokku/dokku-solr) - Stars: 13 - Updated: 5/2023 - Checked: 5/2023
- [Ibexa DXP Solr Integration](https://github.com/ibexa/solr) - Stars: 2 - Updated: 5/2023 - Checked: 5/2023
- [Kafka Connect Solr](https://github.com/jcustenborder/kafka-connect-solr) - Stars: 37 - Updated: 9/2021 - Checked: 5/2023
- [Solr Lando Plugin](https://github.com/lando/solr) - Stars: 0 - Updated: 5/2023 - Checked: 5/2023
- [collective.solr for Plone CMS](https://github.com/collective/collective.solr) - Stars: 19 - Updated: 5/2023 - Checked: 5/2023
- [Solr Search for NodeBB](https://github.com/julianlam/nodebb-plugin-solr) - Stars: 22 - Updated: 1/2023 - Checked: 5/2023
- [TYPO3-Find](https://github.com/subugoe/typo3-find) - Starts: 17 - Updated: 9/2022 - Checked: 5/2023
    - For providing a UI using TYPO3 to a given Solr instance.
- [TYPO3-Solr](https://github.com/TYPO3-Solr/ext-solr) - Stars: 126 - Updated: 5/2023 - Checked: 5/2023
    - For searching the contents of a TYPO3 CMS instance.
- [Solr Engine for Laravel Scout](https://github.com/pxslip/laravel-scout-solr) - Stars: 17 - Updated: 5/2023 - Checked: 5/2023

### Projects Using Solr
- [Fulcrum (Heliotrope)](https://github.com/mlibrary/heliotrope) - Stars: 41 - Updated: 5/2023 - Checked: 5/2023
    - "a Samvera-based digital publishing platform built by the University of Michigan Library"
- [MontySolr](https://github.com/adsabs/montysolr) - Stars: 50 - Updated: 12/2022 - Checked: 5/2023
    - "the search engine behind Astrophysics Data System (ADS 2.0)"
- [National Information Exchange Model (NIEM) Movement](https://github.com/NIEM/movement-solr) - Stars: 3 - Updated: 2/2023

### Utilities
- [Data Import Handler](https://github.com/SearchScale/dataimporthandler) - Stars: 51 - Updated: 4/2023 - Checked: 5/2023
    - Assists in importing records from databases into Solr.
- [RequestSanitizer](https://github.com/cominvent/request-sanitizer-component) - Stars: 4 - Updated: 12/2022 - Checked: 5/2023
    - Sanitizes request parameter input.

### Vector Search
- [BERT Solr Search](https://github.com/DmitryKey/bert-solr-search) - Stars: 134 - Updated: 6/2022 - Checked: 3/2023 - Allows one to search with BERT vectors in Solr, also compatible with Elasticsearch/OpenSearch.
    - Has associated articles explaining the process that was used to build the solution.

## Discussion
- [Official Solr Users Mailing List](https://lists.apache.org/list.html?users@solr.apache.org)

## Solr as a Service Options
- [OpenSolr](https://opensolr.com/)
    - 30-day free trial
    - Pricing starts at €10/mo.

## Companies Working with Solr
- 

## Interesting But Old
- [Elsevier Labs' Solr Dictionary Annotator](https://github.com/elsevierlabs-os/soda) - 2/2020.
- [OpenSextant's  Solr Text Tagger](https://github.com/OpenSextant/SolrTextTagger) - 7/2020.
- [Solr Recommender](https://github.com/pferrel/solr-recommender) - 6/2016.
- [solr-movielens-recommender](https://github.com/o19s/solr-movielens-recommender) - 10/2016.
- [solr-resource-recommender](https://github.com/lacic/solr-resource-recommender) - 12/2014.

## Bibliography / Resources
- [Apache Solr](https://solr.apache.org/)
    - Solr Reference Guide
        - Getting Started
            - [Introduction to Solr](https://solr.apache.org/guide/solr/latest/getting-started/introduction.html)
            - Solr Concepts
                - [Documents, Fields, and Schema Design](https://solr.apache.org/guide/solr/latest/getting-started/documents-fields-schema-design.html)
                - [Solr Indexing](https://solr.apache.org/guide/solr/latest/getting-started/solr-indexing.html)
                - [Searching in Solr](https://solr.apache.org/guide/solr/latest/getting-started/searching-in-solr.html)
                - [Relevance](https://solr.apache.org/guide/solr/latest/getting-started/relevance.html)
                - [Solr Glossary](https://solr.apache.org/guide/solr/latest/getting-started/solr-glossary.html)
        - [Solr Tutorials](https://solr.apache.org/guide/solr/latest/getting-started/solr-tutorial.html)
        