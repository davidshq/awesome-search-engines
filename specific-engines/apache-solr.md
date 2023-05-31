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
    - [Boston Public Library](https://github.com/boston-library/commonwealth-vlr-engine)
    - [Penn State University](https://github.com/psu-libraries/psulib_blacklight)
    - [Stanford University](https://github.com/sul-dlss/exhibits)
    - [Temple University](https://github.com/tulibraries/funcake-solr)
    - [warclight](https://github.com/archivesunleashed/warclight)
- [AJAX Solr](https://github.com/evolvingweb/ajax-solr) - Stars: 654 - Updated: 10/2021 - Checked: 4/2023 - JS library for building UI's for Solr.
- [SolrDora](https://github.com/hectorcorrea/solrdora) - Stars: 6 - Updated: 1/2023 - Checked: 5/2023*
    - Provides a UI for browsing a Solr collection.
- [YASA (Yet Another Solr Admin)](https://github.com/yasa-org/yasa) - Stars: 47 - Updated: 4/2023 - Checked: 5/2023
    - A web-based UI for administering Solr written with Vue in TypeScript.
- [RecordManager](https://github.com/NatLibFi/RecordManager) - Stars: 44 - Updated: 5/2023 - Checked: 5/2023
- [Goobi](https://goobi.io/)
- [DS-Discover](https://github.com/kb-dk/ds-discover) - Stars: 0 - Updated: 4/2023 - Checked: 5/2023
    - "Gateway for Solr text search, image similarity, sound location and other discovery technologies....Developed and maintained by the Royal Danish Library."
- [Search Management UI](https://github.com/querqy/smui) - Stars: 49 - Updated: 5/2023 - Checked: 5/2023
- [MOPSY Search](https://github.com/Der-Henning/mopsy-react) - Stars: 0 - Updated: 1/2022 - Checked: 5/2023
    - Hasn't been updated in a while, but has a live demo.
- [solrkit](https://github.com/garysieling/solrkit) - Stars: 11 - Updated: 4/2018 - Checked: 5/2023

### Language Integrations

#### .NET
- [SolrNet](https://github.com/SolrNet/SolrNet) - Stars: 913 - Updated: 5/2023 - Checked: 5/2023
- [solr-net-linq](https://github.com/IharYakimush/solr-net-linq) - Stars: 4 - Updated: 4/2023 - Checked: 5/2023

#### Elixir
- [Elsol](https://github.com/findmypast/elsol) - Stars: 8 - Updated: 3/2023 - Checked: 5/2023

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
- [SolrQueryComponent](https://github.com/InterNations/SolrQueryComponent) - Stars: 64 - Updated: 8/2022 - Checked: 5/2023
- [pecl-search_engine-solr](https://github.com/php/pecl-search_engine-solr) - Stars: 56 - Updated: 5/2023 - Checked: 5/2023

#### Python
- [Pysolr](https://github.com/django-haystack/pysolr) - Stars: 639 - Updated: 5/2023 - Checked: 5/2023
- [solrcloudpy](https://github.com/solrcloudpy/solrcloudpy) - Stars: 37 - Updated: 2/2021 - Checked: 5/2023
- [solrq](https://github.com/swistakm/solrq) - Stars: 22 - Updated: 11/2022 - Checked: 5/2023

#### Ruby
- [rsolr](https://github.com/rsolr/rsolr) - Stars: 416 - Updated: 2/2022 - Checked: 5/2023
- [solrb](https://github.com/machinio/solrb) - Stars: 38 - Updated: 9/2022 - Checked: 5/2023
- [LSolr](https://github.com/supercaracal/lsolr) - Stars: 10 - Updated: 12/2022 - Checked: 5/2023
- [Sunspot](https://github.com/sunspot/sunspot) - Stars: 3k - Updated: 3/2023 - Checked:  5/2023

### Application/Framework Integrations
- [Dokku Solr](https://github.com/dokku/dokku-solr) - Stars: 13 - Updated: 5/2023 - Checked: 5/2023
- [Drupal Search API Solr](https://github.com/mkalkbrenner/search_api_solr) - Stars: 6 - Updated: 5/2023 - Checked: 5/2023
- [eZ Platform](https://github.com/ezsystems/ezplatform-solr-search-engine) - Stars: 45 - Updated: 5/2023 - Checked: 5/2023
- [Feathersjs Solr Client (feathers-solr)](https://github.com/sajov/feathers-solr) - Stars: 29 - Updated: 3/2023 - Checked: 5/2023
- [Flask Backend Solr Service](https://github.com/NeuroBridge/Backend_service) - Stars: 0 - Updayted: 5/2023 - Checked: 5/2023
- [@florajs/datasource-solr](https://github.com/florajs/datasource-solr) - Stars: 6 - Updated: 5/2023 - Checked: 5/2023
- [Ibexa DXP Solr Integration](https://github.com/ibexa/solr) - Stars: 2 - Updated: 5/2023 - Checked: 5/2023
- [Kafka Connect Solr](https://github.com/jcustenborder/kafka-connect-solr) - Stars: 37 - Updated: 9/2021 - Checked: 5/2023
- [Solr Lando Plugin](https://github.com/lando/solr) - Stars: 0 - Updated: 5/2023 - Checked: 5/2023
- [Omeka-S-module-SearchSolr](https://github.com/Daniel-KM/Omeka-S-module-SearchSolr) - Stars: 2 - Updated: 5/2023 - Checked: 5/2023
- [collective.solr for Plone CMS](https://github.com/collective/collective.solr) - Stars: 19 - Updated: 5/2023 - Checked: 5/2023
- [Solr Search for NodeBB](https://github.com/julianlam/nodebb-plugin-solr) - Stars: 22 - Updated: 1/2023 - Checked: 5/2023
- [Spring Data Solr](https://github.com/spring-projects/spring-data-solr) - Stars: 386 - Updated: 5/2023 - Checked: 5/2023
- [Modern SilverStripe Solr Search](https://github.com/Firesphere/silverstripe-solr-search) - Stars: 10 - Updated: 5/2023 - Checked: 5/2023
- [TYPO3-Find](https://github.com/subugoe/typo3-find) - Starts: 17 - Updated: 9/2022 - Checked: 5/2023
    - For providing a UI using TYPO3 to a given Solr instance.
- [TYPO3-Solr](https://github.com/TYPO3-Solr/ext-solr) - Stars: 126 - Updated: 5/2023 - Checked: 5/2023
    - For searching the contents of a TYPO3 CMS instance.
- [Solr Engine for Laravel Scout](https://github.com/pxslip/laravel-scout-solr) - Stars: 17 - Updated: 5/2023 - Checked: 5/2023
- [Apache Solr Dialect for SQLAlchemy and Apache Superset](https://github.com/aadel/sqlalchemy-solr) - Stars: 8 - Updated: 8/2022 - Checked: 5/2023
- [Sitecore SmartSolrSchema](https://github.com/dataweaversio/SmartSolrSchema) - Stars: 17 - Updated: 12/2022 - Checked: 5/2023
    - Populates "not only standard Sitecore dynamic fields but also reads any custom languages that are set up"
- [solr-power (for WordPress)](https://github.com/pantheon-systems/solr-power) - Stars: 122 - Updated: 4/2023 - Checked: 5/2023

### Neural
- [Neural Solr](https://github.com/maxdotio/neural-solr) - Stars: 14 - Updated: 6/2022 - Checked: 5/2023
    - "This project provides a complete and working semantic search application, using Mighty Inference Server, Apache Solr v9, and an example Node.js express application."

### Other
- [solr-constnat-similarity](https://github.com/freedev/solr-constant-similarity) - Stars: 2 - Updated: 4/2022 - Checked: 5/2023

### Security
- [solr-proxy](https://github.com/Trott/solr-proxy) - Stars: 7 - Updated: 5/2023 - Checked: 5/2023
    - "Reverse proxy to make a Solr instance read-only, rejecting requests that have the potential to modify the Solr index."

### Semantic Search
- [Solr-SBERT-semantic-search](https://github.com/tkhang1999/Solr-SBERT-semantic-search) - Stars: 5 - Updated: 4/2023 - Checked: 5/2023
    - "a simple web demo of semantic search (search by meaning)...using Solr and BERT embeddings."

### Utilities
- [Solr Ansible role](https://github.com/idealista/solr_role) - Stars: 23 - Updated: 1/2023 - Checked: 5/2023
- [Apache Solr Container (Built with Ansible)](https://github.com/geerlingguy/solr-container) - Stars: 17 - Updated: 11/2022 - Checked: 5/2023
- [Solr Bulk Indexing](https://github.com/miku/solrbulk) - Stars: 39 - Updated: 4/2023 - Checked: 5/2023
    - For indexing "a bunch of documents really, really, fast"
- [Solr DB Importer](https://github.com/saro-lab/solr-db-importer) - Stars: 10 - Updated: 3/2023 - Checked: 5/2023
    - Supports MariaDB, Oracle, MSSQL, MySQL, PostgreSQL, and H2.
- [ik-analyzer-solr](https://github.com/magese/ik-analyzer-solr) - Stars: 1.1k - Updated: 1/2022 - Checked: 5/2023
- [Data Import Handler](https://github.com/SearchScale/dataimporthandler) - Stars: 51 - Updated: 4/2023 - Checked: 5/2023
    - Assists in importing records from databases into Solr.
- [Multi Tier Annotation Search (MTAS)](https://github.com/textexploration/mtas) - Stars: 6 - Updated: 1/2022 - Checked: 5/2023
- [RequestSanitizer](https://github.com/cominvent/request-sanitizer-component) - Stars: 4 - Updated: 12/2022 - Checked: 5/2023
    - Sanitizes request parameter input.
- [solr-diagnostics](https://github.com/sematext/solr-diagnostics) - Stars: 5 - Updated: 5/2021 - Checked: 5/2023
    - "Gathers info from Solr that should help diagnose issues"
- [SolrCloud Manager](https://github.com/ekataglobal/solrcloud_manager) - Stars: 23 - Updated: 1/2022 - Checked: 5/2023
    - "Provides easy SolrCloud cluster management."
- [solrcopy](https://github.com/juarezr/solrcopy) - Stars: 6 - Updated: 3/2022 - Checked: 5/2023
    - CLI for backup/restore of documents in Solr cores.
- [Solr Grouping](https://github.com/nla/solr-grouping) - Stars: 2 - Updated: 1/2023 - Checked: 5/2023
    - Allows two levels of grouping (from the National Library of Australia)
- [Solr Operator](https://github.com/apache/solr-operator) - Stars: 208 - Updated: 5/2023 - Checked: 5/2023
    - "Kubernetes Operator for Apache Solr"
- [Lucidworks Spark/Solr Integration](https://github.com/lucidworks/spark-solr) - Stars: 440 - Updated: 5/2023 - Checked: 5/2023
    - "tools for reading data from Solr as a Spark DataFrame/RDD and indexing objects from Spark into Solr using SolrJ."
- [solrscripts](https://github.com/tokee/solrscripts) - Stars: 10 - Updated: 4/2022 - Checked: 5/2023
    - Includes a tool for diffing schema configs and another for validating configs.
- [SolrUtils](https://github.com/InterNations/SolrUtils) - Stars: 8 - Updated: 8/2022 - Checked: 5/2023
    - "helps with recurring tasks when working with Solr like escaping and sanitizing user input"
- [Traject](https://github.com/traject/traject) - Stars: 98 - Updated: 4/2023 - Checked: 5/2023
    - "An easy to use, high-performance, flexible and extensible metadata transformation system, focused on library-archives-museums input, and indexing to Solr as output."
- [Zeppelin Solr Interpreter](https://github.com/lucidworks/zeppelin-solr) - Stars: 28 - Updated: 1/2021 - Checked: 5/2023
    - "allows user to issue Solr queries and display results in the Zeppelin UI"
- [solr-bench](https://github.com/fullstorydev/solr-bench) - Stars: 15 - Updated: 4/2023 - Checked: 5/2023
    - "Solr benchmarking and load testing harness"

### Vector Search
- [BERT Solr Search](https://github.com/DmitryKey/bert-solr-search) - Stars: 134 - Updated: 6/2022 - Checked: 3/2023 - Allows one to search with BERT vectors in Solr, also compatible with Elasticsearch/OpenSearch.
    - Has associated articles explaining the process that was used to build the solution.

### Projects Using Solr
- [Fulcrum (Heliotrope)](https://github.com/mlibrary/heliotrope) - Stars: 41 - Updated: 5/2023 - Checked: 5/2023
    - "a Samvera-based digital publishing platform built by the University of Michigan Library"
- [FXDesktopSearch](https://github.com/mirkosertic/FXDesktopSearch) - Stars: 164 - Updated: 5/2023 - Checked: 5/2023
    - "a JavaFX based desktop search application"
- [Hydroshare](https://github.com/hydroshare/hydroshare) - Stars: 166 - Updated: 5/2023 - Checked: 5/2023
    - "collaborative website for better access to data and models in the hydrologic sciences."
- [MontySolr](https://github.com/adsabs/montysolr) - Stars: 50 - Updated: 12/2022 - Checked: 5/2023
    - "the search engine behind Astrophysics Data System (ADS 2.0)"
- [National Information Exchange Model (NIEM) Movement](https://github.com/NIEM/movement-solr) - Stars: 3 - Updated: 2/2023 - Checked: 5/2023
- [Nelmio](https://github.com/nelmio/NelmioSolariumBundle) - Stars: 152 - Updated: 4/2023 - Checked: 5/2023
- [Samvera](https://github.com/samvera/hyrax) - Stars: 166 - Updated: 5/2023 - Checked: 5/2023
    - "provides a foundation for creating many different digital repository applications."

## Learning Resources
- [solr-tmbd](https://github.com/o19s/solr-tmdb) - Stars: 18 - Updated: 5/2023 - Checked: 5/2023
    - "part of the Think Like a Relevancy Engineer training provided by OpenSource Connections."

## Discussion
- [Official Solr Users Mailing List](https://lists.apache.org/list.html?users@solr.apache.org)

## Solr as a Service Options
- [OpenSolr](https://opensolr.com/)
    - 30-day free trial
    - Pricing starts at €10/mo.
- [SearchStax](https://www.searchstax.com/)
    - Limited free account
    - Pricing starts at $9/mo.

## Companies Working with Solr
- [sematext](https://sematext.com/)
- SeaseLtd
- OpenSourceConnections

## Interesting But Old
- [Elsevier Labs' Solr Dictionary Annotator](https://github.com/elsevierlabs-os/soda) - 2/2020.
- [OpenSextant's  Solr Text Tagger](https://github.com/OpenSextant/SolrTextTagger) - 7/2020.
- [O'Reilly Media's Solr Plugin](https://github.com/oreillymedia/ifpress-solr-plugin) - 8/2020.
- [Vector Scoring Plugin for Solr](https://github.com/saaay71/solr-vector-scoring) - 9/2019.
- [Solr Recommender](https://github.com/pferrel/solr-recommender) - 6/2016.
- [solr-movielens-recommender](https://github.com/o19s/solr-movielens-recommender) - 10/2016.
- [solr-resource-recommender](https://github.com/lacic/solr-resource-recommender) - 12/2014.
- [Selective Search](https://github.com/rajanim/selective-search) - 9/2019.
- [solr-mlt](https://github.com/dfdeshom/custom-mlt) - 10/2019.
- [UPenn's solrplugins](https://github.com/upenn-libraries/solrplugins) - 7/2017.
- [solrgraph](https://github.com/kwatters/solrgraph) - 8/2021.
- [carrot2's solr-integration-strategies](https://github.com/carrot2/solr-integration-strategies) - 1/2014.
- [solr-fusion](https://github.com/outermedia/solr-fusion) - 3/2017.
- [solr-quantities-detection-qparsers](https://github.com/SeaseLtd/solr-quantities-detection-qparsers) - 10/2019.
- [kafka-solr-sink-connector](https://github.com/bkatwal/kafka-solr-sink-connector) - 11/2020.
- [scrapy-solr](https://github.com/scalingexcellence/scrapy-solr) - 4/2016.
- [SKOS Support for Apache Lucene and Solr](https://github.com/behas/lucene-skos) - 2/2016.
- [Solr Mongo Importer](https://github.com/james75/SolrMongoImporter) - 11/2018.
- [ftw.crawler](https://github.com/4teamwork/ftw.crawler) - 11/2017.
- [solr-sql](https://github.com/bluejoe2008/solr-sql) - 4/2020.
- [rdf-graph-search-with-solr-custom-streaming-expression](https://github.com/spoddutur/rdf-graph-search-with-solr-custom-streaming-expression) - 2/2018.
- [nutch-solr-integration](https://github.com/basraven/nutch-solr-integration) - 10/2018.
- [solrj-nested-docs](https://github.com/lucidworks/solrj-nested-docs) - 7/2014.

### UI
- [Solrstrap](https://github.com/fergiemcdowall/solrstrap) - Stars: 86 - Updated: 4/2017 - Checked: 5/2023


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
        