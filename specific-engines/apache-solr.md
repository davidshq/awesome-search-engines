# Apache Solr
- Introduction
- My Notes
- Related Projects
    - General
    - [Discovery and/or UI](./solr/solr-resources-ui.md)
    - [(Coding) Language Integrations](./solr/solr-resources-code.md)
    - [Application/Framework Integrations](./solr/solr-resources-app-framework-integrations.md)
    - [Utilities](./solr/solr-resources-utilities.md)
    - Vector Search
    - [Projects Using Solr](./solr/solr-resources-used-by.md)
- Discussion
- Solr as a Service Options
- Consulting Companies Working with Solr
- [Interesting But Old](./solr/solr-resources-interesting-old.md)
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

### Neural
- [Neural Solr](https://github.com/maxdotio/neural-solr) - Stars: 14 - Updated: 6/2022 - Checked: 5/2023
    - "This project provides a complete and working semantic search application, using Mighty Inference Server, Apache Solr v9, and an example Node.js express application."

### Other
- [solr-constant-similarity](https://github.com/freedev/solr-constant-similarity) - Stars: 2 - Updated: 4/2022 - Checked: 5/2023

### Plugins
- [sematext's Solr Redis Extensions](https://github.com/sematext/solr-redis) - Stars: 51 - Updated: 5/2022 - Checked: 5/2023.
    - "a ParserPlugin that provides a Solr query parser based on data stored in Redis."

### Security
- [solr-proxy](https://github.com/Trott/solr-proxy) - Stars: 7 - Updated: 5/2023 - Checked: 5/2023
    - "Reverse proxy to make a Solr instance read-only, rejecting requests that have the potential to modify the Solr index."

### Semantic Search
- [Solr-SBERT-semantic-search](https://github.com/tkhang1999/Solr-SBERT-semantic-search) - Stars: 5 - Updated: 4/2023 - Checked: 5/2023
    - "a simple web demo of semantic search (search by meaning)...using Solr and BERT embeddings."

### Vector Search
- [BERT Solr Search](https://github.com/DmitryKey/bert-solr-search) - Stars: 134 - Updated: 6/2022 - Checked: 3/2023 - Allows one to search with BERT vectors in Solr, also compatible with Elasticsearch/OpenSearch.
    - Has associated articles explaining the process that was used to build the solution.
- [Vector Search for E-commerce with Chorus](https://opensourceconnections.com/blog/2023/03/22/building-vector-search-in-chorus-a-technical-deep-dive/) - a blog from OpenSource Connections showing how to add vector features to a Solr-powered e-commerce platform

## Learning Resources
- [Solr for newbies workshop](https://github.com/hectorcorrea/solr-for-newbies) - Stars: 68 - Updated: 3/2023 - Checked: 5/2023.
- [solr-tmbd](https://github.com/o19s/solr-tmdb) - Stars: 18 - Updated: 5/2023 - Checked: 5/2023
    - "part of the Think Like a Relevancy Engineer training provided by OpenSource Connections."
- [OSC's pdf-discovery-demo](https://github.com/o19s/pdf-discovery-demo) - Stars: 25 - Updated: 4/2023 - Checked: 5/2023
    - "leverages the Solr Payload Component...and the Offset Highlighter Component...as well as pdf.js to make PDF documents searchable and have highlighting of matches with the text in context of the PDF."
- [Apache Lucene Solr Guide](https://github.com/mikeroyal/Apache-Lucene-Solr-Guide) - Stars: 7 - Updated: 10/2021 - Checked: 5/2023
- [Videos featuring Solr from OSC](https://www.youtube.com/playlist?list=PLCoJWKqBHERuLJgmR0PhiXmS3TUYjWatW) - a playlist of videos of talks featuring Solr

## Discussion
- [Official Solr Users Mailing List](https://lists.apache.org/list.html?users@solr.apache.org)

## Solr as a Service Options
- [OpenSolr](https://opensolr.com/)
    - 30-day free trial
    - Pricing starts at €10/mo.
- [SearchStax](https://www.searchstax.com/)
    - Limited free account
    - Pricing starts at $9/mo.
- [WebSolr](https://www.websolr.com/)
    - Standard from $59/mo with enterprise options

## Companies Working with Solr
- [sematext](https://sematext.com/)
- SeaseLtd
- [OpenSource Connections](https://www.opensourceconnections.com)


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
        
