# OpenSearch
- Official Website: https://opensearch.org/
- Forums: https://forum.opensearch.org/
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

## Quickstart
1. You'll need Docker installed.
2. There are several settings OpenSearch recommends tweaking on the host machine. I'm holding off on tweaking these in a dev environment.
3. Download the Docker Compose config file: `curl -O https://raw.githubusercontent.com/opensearch-project/documentation-website/2.6/assets/examples/docker-compose.yml`
4. Start the cluster: `docker-compose up -d`
5. Query the API: `curl https://localhost:9200 -ku admin:admin`
    - `-k` (or `--insecure`) - Don't check host name (since it's using demo certs).
    - `-u` - Allows one to provide username and password (`admin:admin`).
6. Explore OpenSearch Dashboards: http://localhost:5601 (use same user/pass as above).
    - Click Explore on My Own.
    - Select tenant (Global or Private is fine).
7. Go to Management -> Dev Tools and perform a query (default query is to show all results)
    - Can paste queries in cURL format and they'll be converted to Console syntax.
    - Green triangle runs query.
    - Keyboard shortcuts are under Help.

## Configuring OpenSearch
- Most changes can be accomplished using the cluster settings API.
- A few changes need to be made by modifying `opensearch.yml` and restarting the cluster, prefer the API whenever possible.
    - Note: `opensearch.yml` applies settings to the local node, the API applies to all nodes in the cluster.
- One can also use environment variables when launching OpenSearch like so:
    `./opensearch -Ecluster.name=opensearch-cluster -Enode.name=opensearch-node1 -Ehttp.host=0.0.0.0 -Ediscovery.type=single-node`

### Using Cluster Settings API
- View current settings: `GET _cluster/settings?include_defaults=true`
- Non-default settings only: `GET _cluster/settings`
- The types of settings and precedence:
    1. Transient (cleared after restart)
    2. Persistent
    3. opensearch.yml
    4. Default
- To change settings specify the setting and whether it is persistent or transient:
```
PUT _cluster/settings
{
    "persistent": {
        "action.auto_create_index": "false"
    }
}
```
- Can also copy and paste from GET response and change the existing values:
```
PUT _cluster/settings
{
  "persistent": {
    "action": {
      "auto_create_index": false
    }
  }
}
```

### Using opensearch.yml
- Docker: `/usr/share/opensearch/config/opensearch.yml`
- Linux: `/etc/opensearch/opensearch.yml`
- Example Settings:
```
cluster.name: my-application
action.auto_create_index: true
compatibility.override_main_response_version: true
```
- To allow client app to connect to OpenSearch on a different domain:
```
- http.host:0.0.0.0
- http.port:9200
- http.cors.allow-origin:"http://localhost"
- http.cors.enabled:true
- http.cors.allow-headers:X-Requested-With,X-Auth-Token,Content-Type,Content-Length,Authorization
- http.cors.allow-credentials:true
```

## Plugins
- One can use the `opensearch-plugin` command to list, install, and remove plugins.
- If using OpenSearch in Docker, plugins must be managed by modifying the Docker image.

### List
- `bin/opensearch-plugin list`
- Or use CAT API: `GET _cat/plugins`

### Install
- By Name: `bin/opensearch-plugin install <plugin-name>`
- From Zip: `bin/opensearch-plugin install <zip-file>` (must use HTTP(S), for local fies use `file://`)
- Using Maven Coordinates: `bin/opensearch-plugin install <groupId>:<artifactId>:<version>`

### Remove
- `bin/opensearch-plugin remove <plugin-name>`

### Restart
- Restart the node after installing or removing a plugin.

### Batch Mode
- To skip confirmation prompts when installing plugins: `bin/opensearch-plugin install --batch <plugin-name>`

### Bundled Plugins
- Alerting - `opensearch-alerting`
- Anomaly Detection - `opensearch-anomaly-detection`
- Asynchronous Search - `opensearch-asynchronous-search`
- Cross Cluster Replication - `opensearch-cross-cluster-replication`
- Notifications - `notifications`
- Reports Scheduler - `opensearch-reports-scheduler`
- Geospatial - `opensearch-geospatial`
- Index Management - `opensearch-index-management`
- Job Scheduler - `opensearch-job-scheduler`
- k-NN - `opensearch-knn`
- ML Commons - `opensearch-ml`
- Neural Search - `neural-search`
- Observability - `opensearch-observability`
    - Notebooks (`opensearch-notebooks`) has been merged into Observability.
- Performance Analyzer - `opensearch-performance-analyzer`
    - Not available on Windows.
- Security - `opensearch-security`
- Security Analytics - `opensearch-security-analytics`
- SQL - `opensearch-sql`

### Additional Plugins
- These are available for install using `bin/opensearch-plugin install <plugin-name>`, additional ones are also available outside of OpenSearch's GitHub.
- `analysis-icu`
- `analysis-kuromoji`
- `analysis-nori`
- `analysis-phonetic`
- `analysis-smartcn`
- `analysis-stempel`
- `analysis-ukrainian`
- `discovery-azure-classic`
- `discovery-ec2`
- `discovery-gce`
- `ingest-attachment`
- `mapper-annotated-text`
- `mapper-murmur3`
- `mapper-size`
- `repository-azure`
- `repository-gcs`
- `repository-hdfs`
- `repository-s3`
- `store-smb`
- `transport-nio`

## Bibliography
- https://opensearch.org/docs/latest/about/
- https://opensearch.org/docs/latest/quickstart/
- https://opensearch.org/docs/latest/install-and-configure/configuration/
- https://opensearch.org/docs/latest/install-and-configure/plugins/