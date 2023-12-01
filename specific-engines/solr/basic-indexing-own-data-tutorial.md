# Indexing One's Own Data Tutorial

The content here is pulled from the official Solr Tutorials, [Exercise 3: Index Your Own Data](https://solr.apache.org/guide/solr/latest/getting-started/tutorial-diy.html).

These are essentially my notes on the course materials.

## Preparations
- What sort of data will I index?
- What do I need to prepare Solr for this data?
    - e.g., create fields, set up copy fields, determine analysis rules, etc.
- What kind of search options should the users have?
- How much testing is needed to ensure it is working correctly?

## Create Your Own Collection
- Make sure that Solr is running, e.g. `./bin/solr start`
- `./bin/solr create -c yourCollectionName -s 2 -rf 2`

## Indexing Ideas

### Local Files with bin/post
- If files are local, can handle JSON, XML, CSV, HTML, PDF, MS Office, plain text, and other formats.
- `./bin/post -c yourCollectionName ~/pathToYourData`

### SolrJ or Other Client APIs

### Documents Screen
- http://localhost:8983/solr/#/yourCollectionName/documents
- Paste in document or use Document Builder from Document Type to create a document field by field.

## Updating Data
- Documents with an identical `uniqueKey` value in the field `id` are updated rather than added in future indexing operations.


## Deleting Data
- "You can delete data by POSTing a delete command to the update URL and specifying the value of the document’s unique key field, or a query that matches multiple documents (be careful with that one!). We can use bin/post to delete documents also if we structure the request properly."
- Specific Document: `bin/post -c yourCollectionName -d "<delete><id>someUniqueId</id></delete>"`
- All Documents: `bin/post -c yourCollectionName -d "<delete><query>*:*</query></delete>"`


## Bibliography / Resources
- https://solr.apache.org/guide/solr/latest/getting-started/tutorial-diy.html