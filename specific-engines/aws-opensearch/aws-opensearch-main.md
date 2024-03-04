# AWS OpenSearch Service

## Introduction
Amazon Web Services (AWS) used to offer a managed service called Amazon Elasticsearch Service (Amazon ES) that utilized the open source Elasticsearch engine. Elastic changed it's licensing in an attempt to prevent Amazon from using it's software without paying what Elastic saw as a reasonable price. AWS forked the last fully open source version of Elasticsearch and rebranded it as OpenSearch. OpenSearch itself is an open source search engine application that does not depend on AWS. AWS OpenSearch Service is a managed OpenSearch service. There is also a serverless offering available, but we will be focusing primarily on the managed offering at this point.

## Caveat
Both Elasticsearch and OpenSearch are powerful document search engines but much of the documentation on them focuses on their usage within DevOps and Security analytics contexts. We will not be covering these topics as indexes although we will address them as they apply to the proper configuration and maintenance of OpenSearch clusters.

## Resources
- [Amazon OpenSearch Service Documentation](https://docs.aws.amazon.com/opensearch-service/)
    - [Amazon OpenSearch Service Developer Guide](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/what-is.html)
        - [Searching data in Amazon OpenSearch Service](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/searching.html)
    - [Amazon OpenSearch Service API Operations](https://docs.aws.amazon.com/opensearch-service/latest/APIReference/API_Operations_Amazon_OpenSearch_Service.html)
    - [Amazon OpenSearch Service AWS CLI Command Reference](https://docs.aws.amazon.com/cli/latest/reference/opensearch/)
    - [Amazon OpenSearch Ingestion API Operations Documentation](https://docs.aws.amazon.com/opensearch-service/latest/APIReference/API_Operations_Amazon_OpenSearch_Ingestion.html)




## Ways to Search
- URI - Simple but limited in what functionality it can utilize.
- Request Body - Slightly more complex but able to utilize the full range of OpenSearch DSL.

## Boosting

## Search Result Highlighting

## Pagination
- Point in Time (PIT) - Runs the queries against the data as it was at a specific point in time. This is the preferred method.
- Using From and Size Parameters - Slightly less complicated but may not be as accurate as PIT.

## Packages (Dictionaries, Plugins)
- See [Custom packages for Amazon OpenSearch Service](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/custom-packages.html) and [Plugins by engine version in Amazon OpenSearch Service](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/supported-plugins.html)

Somewhat confusingly named, these are custom dictionary files and plugins that can improve the quality of results returned.

The plugins provided by Amazon for OpenSearch Service currently include analyzers for Japaneses, Chinese, Pinyin, and Korean as well as the more generally applicable Amazon Persoanlzied Ranking plugin ("re-ranks OpenSearch results based on each user's past behavior and preferences").

We can use a synonym token filter to add tokens and stop token filter to remove tokens when a specific token is found.

## SQL
- See [Querying your Amazon OpenSearch Service data with SQL](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/sql-support.html) and [SQL and PPL](https://opensearch.org/docs/latest/search-plugins/sql/index/)
- It is what it sounds like, you can use SQL instead of the JSON-based DSL to query your OpenSearch cluster.
- There is a SQL Workbench in OpenSearch Dashboards, a SQLI CLI is available, as well as a JDBC driver. There is also a read-only ODBC driver.

## k-NN search
- See [k-Nearest Neighbor (k-NN) search in Amazon OpenSearch Service](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/knn.html) and [k-NN search](https://opensearch.org/docs/latest/search-plugins/knn/index/).

## Cross-cluster search
- See [Cross-cluster search in Amazon OpenSearch Service](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/cross-cluster-search.html)
- Sometimes one may want to create multiple smaller domains rather than one large domain, this is helpful when the data will be used for different types of workloads and the clusters can be optimized to support that specific workload.

## Learning to Rank
- See [Learning to Rank for Amazon OpenSearch Service](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/learning-to-rank.html), [Elastic Learning to Rank Documentation](https://elasticsearch-learning-to-rank.readthedocs.io/en/latest/index.html)
- Uses machine learning and behavioral data to tune the relevance of search results.
- Based on the Elasticsearch LTR plugin which utilizes models from the XGBoost and Ranklib libraries for rescoring results.

## Asynchronous Search
- See [Asynchronous search in Amazon OpenSearch Service](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/asynchronous-search.html)
- "With asynchronous search for Amazon OpenSearch Service you can submit a search query that gets executed in the background, monitor the progress of the request, and retrieve results at a later stage. You can retrieve partial results as they become available before the search has completed. After the search finishes, save the results for later retrieval and analysis."

## Point in Time (PIT)
- See [Point in time in Amazon OpenSearch Service](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/pit.html)
- "The point in time (PIT) feature is a type of search that lets you run different queries against a dataset that's fixed in time. Typically, when you run the same query on the same index at different points in time, you receive different results because documents are constantly indexed, updated, and deleted. With PIT, you can query against a constant state of your dataset."

## Semantic Search
- See [Semantic search in Amazon OpenSearch Service](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/semantic-search.html)
- Allows one to perform semantic search using neural search or k-NN.
- DM: Explore this section further.
