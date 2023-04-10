# OpenSearch
- https://opensearch.org/
- An open source fork of Elasticsearch started by Amazon.

## Some Basics
- Built on Apache Lucene
- Node - A server that contains data and responds to search queries.
- Cluster - A group of nodes that work together to store and search data.
- Index - A collection of documents.
    - Mapping - Collection of fields that documents in an index.
    - Settings - Configurations for an index.
- Shard - A portion of an index.
    - Shards are split evenly across the nodes in a cluster.
    - Each shard is a full Lucene index.
    - Rule of Thumb: Shards should be 10-50 GB each.
- Primary Shard - The node is responsible for the shard.
- Replica Shard - The node acts as a backup and can take some of the read load off the primary shard.- REST API - Allows one to interact with OpenSearch using HTTP requests.