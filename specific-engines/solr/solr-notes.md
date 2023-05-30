## Goal
My memory isn't amazing so I tend to make concise notes that help me remember technologies. Much of this document will be a summarization of documentation for Apache Solr. On occasion it may also include information not in the source materials (or at least not in the same place), this is done to fill in gaps in my knowledge.

## Loading Data into Solr
- Can ingest data from many sources (XML, CSV, Microsoft Word, PDF, etc.)

### Common Ways to Load Data
- Using Solr Cell and Apache Tika, the latter is for ingesting binary files.
- Uploading XML files using HTTP requests.
- Creating a custom application that utilizes the Java Client API.
- Note: By default the `-e` option when starting Solr sets the `example` directory as base directory for the Solr instance.

## Searching with Solr
- A query is made to Solr and a *response handler* which calls a *query parser* "which interprets the terms and parameters of a query."

### Query Parsers
- "Different query parsers support different syntax."
    - Default: Standard Query Parser (aka "lucene" query parser).
    - Other Included Query Parsers:
        - DisMax Query Parser
        - Extended DisMax (eDisMax) Query Parser
- The Standard Query Parser is precise (but throws syntax errors when queries are incorrect) while the DisMax/eDisMax Query Parsers act similarly to web search engines.
    - eDisMax extends and improves on DisMax's functionality.

### Query Parser Input Types
- Queries can be made using:
    - strings (e.g. words, terms)
    - "parameters for fine-tuning the query"
    - "parameters for controlling the presentation of the query response"

## Bibliography / Resources
- See the main [Apache Solr](../apache-solr.md) document for a list of resources.