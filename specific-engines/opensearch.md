# OpenSearch
- https://opensearch.org/
- An open source fork of Elasticsearch started by Amazon.

## Some Basics
- Built on Apache Lucene
- Node(s) - A server that contains data and responds to search queries.
- Cluster(s) - A group of nodes that work together to store and search data.
- Index / Indices - A collection of documents.
    - Mapping(s) - Collection of fields that documents in an index.
    - Setting(s) - Configurations for an index.
- Shard(s) - A portion of an index.
    - Shards are split evenly across the nodes in a cluster.
    - Each shard is a full Lucene index.
    - Rule of Thumb: Shards should be 10-50 GB each.
- Primary Shard - The node is responsible for the shard.
- Replica Shard - The node acts as a backup and can take some of the read load off the primary shard.- REST API - Allows one to interact with OpenSearch using HTTP requests.
- API - OpenSearch provides a REST API for interacting with the server.

```
// Add a JSON doc to index
PUT https://<host>:<port>/<index-name>/_doc/<document-id>
{
    "title": "The Wind Rises",
    "release_date": "2013-07-20"
}

// Search for a document
GET https://<host>:<port>/<index-name>/_search?q=wind

// Delete a document
DELETE https://<host>:<port>/<index-name>/_doc/<document-id>
```

## Bibliography
- https://opensearch.org/docs/latest/about/