# OpenSearch Python

## OpenSearch Python (opensearch-py) Client
This section provides a brief overview of some portions of the OpenSearch Python client. See the [official documentation](https://opensearch-project.github.io/opensearch-py/index.html) for details.

## OpenSearch Client
- `OpenSearch()`
- `bulk()`
- `count()`
- `create()` - A document in the index.
- `create_pit()` - Creates point in time context.
- `delete()` - Remove a document from the index.
- `delete_all_pits()`
- `delete_by_query()` - Delete documents that match a specific query.
- `delete_pit()` - Deletes one or more pits.
- `delete_script()`
- `exists()` - Whether a document exists in an index.
- `exists_source()`
- `explain()` - Why specific documents matched or did not match a query.
- `field_caps()`
- `get()` - Retrieve a document.
- `get_all_pits()`
- `get_script()`
- `get_script_context()`
- `get_script_languages()`
- `get_source()`
- `index()` - Creates or updates a document in an index.
- `info()` - Returns info about cluster.
- `mget()` - Retrieve multiple documents.
- `msearch()` - Multiple search operations in a single request.
- `msearch_template()`
- `mtermvectors()` - Retrieve multiple term vectors in a single request.
- `ping()` - Check if the cluster is up.
- `put_script()` - Create or update a script.
- `rank_eval()`  - Evaluate the quality of ranked search results over a set of typical search queries.
- `reindex()` - Reindex documents from one index to another.
- `render_search_template()` - Use the Mustache language to pre-render a search definition.
- `scripts_painless_execute()`
- `scroll()` - Allows to retrieve a large number of results from a single search request.
- `search()` - Search for documents in one or more indices.
- `search_shards()` - Returns info about the indices and shards a request would be executed against.
- `search_template()`
- `termvectors()` - Retrieve information and statistics about terms in the fields of a particular document.
- `update()` - Update a document.
- `update_by_query()` - Update documents that match a specific query.

### Http Client
- `delete()`, `get()`, `head()`, `post()`, `put()`

### Compact and aligned text (CAT) Client
- `aliases()`
- `all_pit_segments()`
- `allocation()` - How many shards are allocated to each data node and how much disk they are using.
- `cluster_manager()` - Info about cluster manager node.
- `count()`
- `fielddata()` - How much heap memory is being used by fielddate on each data node.
- `health()`
- `help()` - Regarding the CAT APIs
- `indices()` - Info about indices.
- `nodeatrs()` - Info about custom node attributes.
- `nodes()` - Info about nodes.
- `pending_tasks()` - Info about pending tasks.
- `pit_segments()`
- `recovery()` - Info about shard recoveries.
- `plugins()`
- `recovery()`
- `repositories()`
- `segment_replication()`
- `segments()`
- `shards()`
- `snapshots()`
- `tasks()`
- `templates()`
- `thread_pool()`

### Cluster Client
- `allocation_explain()`
- `delete_component_template()`
- `delete_weighted_routing()`
- `exists_component_template()`
- `get_component_template()`
- `get_settings()` - Of a cluster
- `get_weighted_routing()`
- `health()`
- `pending_tasks()`
- `put_component_template()`
- `put_settings()`
- `put_weighted_routing()`
- `remote_info()`
- `reroute()` - Manually change allocation of individual shards in the cluster.
- `state()` - Comprehensive info about state of cluster.
- `stats()` - High-level overview of cluster stats.

### Dangling Indices Client
- https://opensearch-project.github.io/opensearch-py/api-ref/clients/dangling_indices_client.html

### Ingest Client
- `delete_pipeline()`
- `get_pipeline()`
- `processor_grok()` - Returns a list of the built-in patterns.
- `put_pipeline()`
- `simulate()` - Simulate a pipeline with example docs.

### Indices Client
- `add_block()`
- `analyze()`
- `clear_cache()`
- `clone()`
- `close()`
- `create()`
- `create_data_stream()`
- `data_streams_stats()`
- `delete()`
- `delete_alias()`
- `delete_data_stream()`
- `delete_template()`
- `exists()` - Whether a particular index exists
- `exists_alias()`
- `exists_template()`
- `flush()`
- `forcemerge()` - Of one or more indices
- `get()` - Returns info about one or more indices
- `get_alias()`
- `get_data_stream()`
- `get_field_mapping()` - Returns mapping for one or more fields
- `get_mapping()` - Returns mapping for one or more indices
- `get_settings()` - Returns settings for one or more indices
- `get_template()`
- `open()` - Opens an index
- `put_alias()` - Creates or updates an alias
- `put_mapping()` - Updates the index mappings
- `put_settings()`
- `put_template()`
- `recovery()` - Info about shard recoveries
- `refresh()`
- `resolve_index()` - Resolves info about any matching indices, aliases, data streams.
- `rollover()` - Updates an alias to point to a new index when old index is too large/old.
- `segments()` - Low-level info about Lucene segments in one or more indices
- `shard_stores()`
- `shrink()` - Shrinks an existing index into a new index with fewer primary shards
- `simulate_template()`
- `split()` - Splits an existing index into a new index with more primary shards
- `stats()`
- `update_aliases()`
- `validate_query()` - For validating a potentially expensive query without executing it.

### Nodes Client
- `hot_threads()`
- `info()`
- `reload_secure_settings()`
- `stats()`
- `usage()` - Low-level info about REST actions usage

### Remote Client

### Security Client
- `change_password()` - For current user
- `create_action_group()` - Create or replace
- `create_role()`  - Create or replace
- `create_role_mapping()` - Create or replace
- `create_tenant()` - Create or replace
- `create_user()` - Create or replace
- `delete_action_group()`
- `delete_distinguished_names()`
- `delete_role()`
- `delete_role_mapping()`
- `delete_tenant()`
- `delete_user()`
- `flush_cache()` - Flushes the Security plugin user, authentication, and authorization caches.
- `get_account_details()` - For current user
- `get_action_group()`
- `get_action_groups()`
- `get_audit_configuration()`
- `get_certificates()`
- `get_configuration()`
- `get_distinguished_names()`
- `get_role()`
- `get_role_mapping()`
- `get_role_mappings()`
- `get_roles()`
- `get_tenant()`
- `get_tenants()`
- `get_user()`
- `get_users()`
- `health()`
- `patch_action_group()` - Updates individual attributes of an action group
- `patch_action_groups()`
- `patch_audit_configuration()`
- `patch_configuration()`
- `patch_distinguished_names()`
- `patch_role()`
- `patch_role_mapping()`
- `patch_role_mappings()`
- `patch_roles()`
- `patch_tenant()`
- `patch_tenants()`
- `patch_user()`
- `patch_users()`
- `reload_http_certificates()`
- `reload_transport_certificates()`
- `update_audit_configuration()`
- `update_configuration()`
- `update_distinguished_names()`

### Snapshot Client
- `cleanup_repository()` - Removes stale data
- `clone()` - Clones indices from one snapshot to another in the same repository
- `create()` - Creates a snapshot in the repository
- `create_repository()` - Creates a repository
- `delete()` - Deletes a snapshot
- `delete_repository()` - Deletes a repository
- `get()` - Returns info about a snapshot
- `get_repository()` - Returns info about a repository
- `restore()` - Restores a snapshot
- `status()` - Returns info about the status of a snapshot
- `verify_repository()` - Verifies that a repository is working correctly

### Tasks Client
- `cancel()`
- `get()` - Return info about a task
- `list()` - Return info about all tasks

### Features Client
- `get_features()` - List of features which can be included in snapshots using the feature_states field when creating a snapshot

### Exceptions
- `AuthenticationException` - 401
- `AuthorizationException` - 403
- `ConflictError` - 409
- `ConnectionError`
- `ConnectionTimeout`
- `ImproperlyConfigured`
- `NotFoundError` - 404
- `RequestError` - 400
- `SerializationError`
- `SSLError`
- `TransportError`

### Helpers
- `aggs.Agg()`
    - `to_dict()`
- `analysis.Analyzer()`
- `document.Document()`
    - `delete()`
    - `exists()`
    - `get()`
    - `init()` - Create an index and populate the mappings
    - `mget()`
    - `save()` - Create or overwrite a document
    - `search()`
    - `to_dict()`
    - `update()`
- `faceted_search.FacetedSearch()`
    - `add_filter()`
    - `aggregate()`
    - `build_search()` - Construct the search object
    - `execute()` - Execute the search and return response
    - `filter()` - Add a `post_filter` that narrows results based on facet filters
    - `highlight()` - For all the fields
    - `query()`
    - `search()` - Returns the base Search object to which the facets are added
    - `sort()`
- `field.Field()`
    - `to_dict()`
- `function.ScoreFunction()`
    - `to_dict()`
- `index.Index()`
    - `aliases()` - Add to the index definition
    - `analyze()`
    - `analyzer()`
    - `clear_cache()`
    - `clone()`
    - `close()`
    - `create()`
    - `delete()`
    - `delete_alias()`
    - `document()` - Associates a Document subclass with an index.
    - `exists()`
    - `exists_alias()`
    - `flush()`
    - `forcemerge()`
    - `get()`
    - `get_alias()`
    - `get_field_mapping()` - For a specific field
    - `get_mapping()` - For a specific type
    - `get_settings()`
    - `get_upgrade()` - How much of index is upgraded
    - `mapping()` - Associate a mapping with index
    - `open()`
    - `put_alias()`
    - `put_mapping()`
    - `put_settings()`
    - `recovery()`
    - `refresh()`
    - `save()` - Sync the index definition with opensearch, create index if it doesn't exist, update settings/mappings if it does
    - `search()`
    - `segments()`
    - `settings()` - Add settings
    - `shard_stores()`
    - `shrink()`
    - `stats()`
    - `updateByQuery()`
    - `upgrade()`
    - `validate_query()`
- `Mapping`
- `Query`
- `search.Search()`
    - `__getitem__(n)` - slicing Search instance for pagination
    - `__iter__()` - over the hits
    - `_clone()` - Clone of current search request, performs shallow copy of underlying objects.
        - Used internally by most state modifying APIs.
    - `collapse()`
    - `count()` - Number of matching hits
    - `delete()` - Delegates to `delete_by_query()`
    - `execute()` - Executes the search, returns an instance of Response wrapping all the data.
    - `from_dict()` - Constructs a new Search instance from a raw dict
    - `highlight()` - For some fields
    - `highlight_options()` - Set global options for current request
    - `response_class(cls)` - Override default wrapper used for the response
    - `scan()` - Returns a generator that will iterate over all the documents matching the query.
    - `script_field()` - Define script field to be calculated on hits
    - `sort()`
    - `source()` - Control how the `_source_` field is returned.
    - `suggest()` - Add a suggestions request to the search
    - `to_dict()`
    - `update_from_dict()` - Apply options from a serialized body to the current instance.
        - Modifies object in place.
        - Used mostly by from_dict.
- `update_by_query.UpdateByQuery()`
    - `_clone()` - Clone of current search request, performs shallow copy of underlying objects.
    - `execute()` - Executes the update, returns an instance of Response wrapping all the data.
    - `from_dict()` - Constructs a new UpdateByQuery instance from a raw dict
    - `response_class(cls)` - Override default wrapper used for the response
    - `script()` - Define update action to take
        - Only accepts a single script
    - `to_dict()`
    - `update_from_dict()` - Apply options from a serialized body to the current instance.
        - Modifies object in place.
        - Used mostly by from_dict.
- `wrappers.Range()`

## Plugins

### Alerting Plugin

### Index Management Plugin

### Serializer

### Transport