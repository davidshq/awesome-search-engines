# SolrCloud Tutorial

- "SolrCloud is designed to provide a highly available, fault tolerant environment for distributing your indexed content and query requests across multiple servers."
- "It’s a system in which data is organized into multiple pieces, or shards, that can be hosted on multiple machines, with replicas providing redundancy for both scalability and fault tolerance, and a ZooKeeper server that helps manage the overall structure so that both indexing and search requests can be routed properly.
"

## Interactive Startup
- `bin/solr -e cloud`
- How many nodes? 2
- node1 port? 8983
- node2 port? 7574
- Solr starts the nodes and displays the command it used to start each node.
- The first node starts a ZooKeeper server on port 9983.
- name of collection? gettingstarted
- number of shards? 2
- replicas per shard? 2
- configuration? _default

## Check Status
- `bin/solr status`

## Log Files
- You can find log files in `example/cloud/node1/logs` and `example/cloud/node2/logs`.

## See Collection Deployed Across Cluster
- http://localhost:8983/solr/#/~cloud

## Basic Diagnostics
- `bin/solr healthcheck -c gettingstarted`
- "The healthcheck command gathers basic information about each replica in a collection, such as number of docs, current status (active, down, etc.), and address (where the replica lives in the cluster)."

## Stopping SolrCloud
- `bin/solr stop -all`

## Starting with -noprompt
- Use the defaults instead of interactive
- `bin/solr -e cloud -noprompt`

## Restarting Nodes
- `bin/solr restart -c -p 8983 -s example/cloud/node1/solr`
- `bin/solr restart -c -p 7574 -z localhost:9983 -s example/cloud/node2/solr`
- Note that in the first case we don't need to specify the ZooKeeper address because it is the same as the node but for the second case we need to tell the command where ZooKeeper is located.

## Adding a Node to a Cluster
- `mkdir solrHomeForNewNode`
- `cp AnExistingSolrHomePath solrHomeForNewNodePath`
- `bin/solr start -cloud -s solrHomeForNewNode/solr -p portNumber -z zooKeeperHostAndPort`
- Example:
- `mkdir -p example/cloud/node3/solr`
- `cp example/cloud/node1/solr/solr.xml example/cloud/node3/solr/solr.xml`
- `bin/solr start -cloud -s example/cloud/node3/solr -p 8987 -z localhost:9983`

## Bibliography / Resources
- https://solr.apache.org/guide/solr/latest/getting-started/tutorial-solrcloud.html