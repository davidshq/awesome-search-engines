## Terminology

### Concepts
- Atomic Updates - "An approach to updating only one or more fields of a document, instead of reindexing the entire document."
- Boolean operators - "control the inclusion or exclusion of keywords in a query by using operators such as AND, OR, and NOT."
- Clustering (of Results) - "groups search results by similarities discovered when a search is executed, rather than when content is indexed."
    - "It can reveal unexpected commonalities among search results"
- Document - "A group of fields and their values. Documents are the basic unit of data in a collection."
    - "basic unit of information is a document, which is a set of data that describes something."
- Facet / Faceting - "The arrangement of search results into categories based on indexed terms."
    - Facet Constraint - A specific facet value within a category that further constrains the results.
- Field - "The content to be indexed/searched along with metadata defining how the content should be processed by Solr."
    - "documents are composed of fields, which are more specific pieces of information."
    - Fields can be of different types - e.g. text, number.
- Index - where Solr stores all of the data.
    - Indexing - adding data to Solr.
- Inverse Document Frequency (IDF) - "A measure of the general importance of a term. It is calculated as the number of total Documents divided by the nuber of Documents that a  particular word occurs in the collection."
- Inverted Index - "A way of creating a searchable index that lists every word and the documents that contain those words, similar to an index in the back of a book which lists words and the pages on which they can be found."
- Metadata - "Literally, data about data. Metadata is information about a document, such as its title, author, or location."
- Natural Language Query - "A search that is entered as a user would normally speak or write".
- Precision - "the percentage of documents in the returned results that are relevant."
- Query - asking a question of the data using Solr.
    - Query Parser - "processes the terms entered by a user."
- Recall - "the percentage of relevant results returned out of all relevant results in the system."
    - "The ability of a search engine to retrieve all of the possible matches to a user’s query."
- Relevance - "the degree to which a query response satisfies a user who is searching for information."
    - "The appropriateness of a document to the search conducted by the user."
- Stopwords - "Generally, words that have little meaning to a user’s search but which may have been entered as part of a natural language query."
    - "Stopwords are generally very small pronouns, conjunctions and prepositions (such as, "the", "with", or "and")"
- Syonyms - "Synonyms generally are terms which are near to each other in meaning and may substitute for one another. In a search engine implementation, synonyms may be abbreviations as well as words, or terms that are not consistently hyphenated."
- Term Frequency - "The number of times a word occurs in a given document."
- Wildcard - "A wildcard allows a substitution of one or more letters of a word to account for possible variations in spelling or tenses."
- Zookeeper - "The system used by SolrCloud to keep track of configuration files and node names for a cluster. A ZooKeeper cluster is used as the central configuration store for the cluster, a coordinator for operations requiring distributed synchronization, and the system of record for cluster topology."

### Infrastructure
- Cluster - "a set of Solr nodes operating in coordination with each other via ZooKeeper, and managed as a unit."
- Collection - "one or more Documents grouped together in a single logical index using a single configuration and Schema."
    - A similar concept is Cores in single-node installations and user-managed clusters.
- Core - "An individual Solr instance (represents a logical index). Multiple cores can run on a single node."
    - Compare to Collection above.
- Ensemble - "A ZooKeeper term to indicate multiple ZooKeeper instances running simultaneously and in coordination with each other for fault tolerance."
- Leader - "A single Replica for each Shard that takes charge of coordinating index updates (document additions or deletions) to other replicas in the same shard."
    - "This is a transient responsibility assigned to a node via an election, if the current Shard Leader goes down, a new node will automatically be elected to take its place."
- Node - "A JVM instance running Solr. Also known as a Solr server."
- [Operator](https://solr.apache.org/operator/) - "[B]uilt to reliably manage Apache Solr on Kubernetes."
- Overseer - "A single node in SolrCloud that is responsible for processing and coordinating actions involving the entire cluster. It keeps track of the state of existing nodes, collections, shards, and replicas, and assigns new replicas to nodes."
    - "This is a transient responsibility assigned to a node via an election, if the current Overseer goes down, a new node will be automatically elected to take its place."
- Replica - "A Core that acts as a physical copy of a Shard."
- Replication - "A method of copying a leader index from one server to one or more 'follower' or 'child' servers."
- SolrCloud - "Umbrella term for a suite of functionality in Solr which allows managing a Cluster of Solr Nodes for scalability, fault tolerance, and high availability."

### Other
- Common Query Parameters - Parameters that are "accepted by all query parsers."
- Distributed Search - "queries are processed across more than one Shard."
- Field Analysis - "tells Solr what to do with incoming data when building an index."
    - "A more accurate name for this process would be processing or even digestion, but the official name is analysis."
- Filter
    - Filter Query - "a filter query runs a query against the entire index and caches the results...the strategic use of filter queries can improve search performance."
        - Operates on data already existing in the index.
    - Analysis Filter - Operates on data being ingested.
- MoreLikeThis - "enables users to submit new queries that focus on particular terms returned in an earlier query."
- `maxDoc` - The number of documents in the index including those which have been logically but not physically deleted.
- `numDocs` - The "number of searchable documents in the index."
    - Some files may contain multiple documents, e.g. XML, JSON, or CSV. In this case the `numDocs` will be greater than the number of files indexed.
- Request Handler (RequestHandler) - receives and processes requests.
    - "Logic and configuration parameters that tell Solr how to handle incoming "requests", whether the requests are to return search results, to index documents, or to handle other custom situations."
- SearchComponent - "ogic and configuration parameters used by request handlers to process query requests."
    - "Examples of search components include faceting, highlighting, and "more like this" functionality."
- Response Writer - "manages the final presentation of the query response."
    - Solr is bundled with both XML and JSON response writers.
- SolrConfig (solrconfig.xml) - "The Apache Solr configuration file. Defines indexing options, RequestHandlers, highlighting, spellchecking and various other configurations."
      - The file, solrconfig.xml, is located in the Solr home conf directory."
- `solr.home` - "the location under the main Solr installatiomn where Solr's collections and their `conf` and `data` directories are stored."
- Solr Schema (managed-sechame.xml or schema.xml) - Defines how Solr builds indexes from data sent to it.
    - Stores information about the fields and data types.
- Shard - "In SolrCloud, a logical partition of a single Collection."
    - "Every shard consists of at least one physical replica".

    # Bibliography / Resources
    - See Bibliography section of the main [Apache Solr document](../apache-solr.md).