# Introduction
This is meant to be a cheatsheet-like condensation of [the official Solr tutorials](https://solr.apache.org/guide/solr/latest/getting-started/solr-tutorial.html). See the Bibliography/Resources section to links to the individual tutorials utilized.

In a few places I've included additional details I thought relevant but overall this cheatsheet leaves out a lot of material and you may want to read the original tutorials first and use this for later reference.

# Getting Solr
- [Download the latest Solr](https://solr.apache.org/downloads.html).
- Unzip the downloaded file: `tar -xzf solr-9.2.1.tgz`
- Enter the extracted folder: `cd solr-9.2.1`

# Launch Solr in SolrCloud Mode
- `bin/solr start -c`
- Add another Solr node to cluster: `bin/solr -c -z localhost:9983 -p 9984`
    - May need to increase open file limit to 65000.
    - May need to adjust available entropy.
- Open Admin UI: http://localhost:8983/

# Create a Collection
```
curl --request POST \
--url http://localhost:8983/api/collections \
--header 'Content-Type: application/json' \
--data '{
    "create": {
        "name": "techproducts",
        "numShards": 1,
        "replicationFactor": 1
    }
}'
```

# Define a Schema
```
curl --request POST \
  --url http://localhost:8983/api/collections/techproducts/schema \
  --header 'Content-Type: application/json' \
  --data '{
  "add-field": [
    {"name": "name", "type": "text_general", "multiValued": false},
    {"name": "cat", "type": "string", "multiValued": true},
    {"name": "manu", "type": "string"},
    {"name": "features", "type": "text_general", "multiValued": true},
    {"name": "weight", "type": "pfloat"},
    {"name": "price", "type": "pfloat"},
    {"name": "popularity", "type": "pint"},
    {"name": "inStock", "type": "boolean", "stored": true},
    {"name": "store", "type": "location"}
  ]
}'
```

# Index Some Documents
- Single Document:
```
curl --request POST \
--url 'http://localhost:8983/api/collections/techproducts/update' \
  --header 'Content-Type: application/json' \
  --data '  {
    "id" : "978-0641723445",
    "cat" : ["book","hardcover"],
    "name" : "The Lightning Thief",
    "author" : "Rick Riordan",
    "series_t" : "Percy Jackson and the Olympians",
    "sequence_i" : 1,
    "genre_s" : "fantasy",
    "inStock" : true,
    "price" : 12.50,
    "pages_i" : 384
  }'
```
- Multiple Documents:
```
curl --request POST \
  --url 'http://localhost:8983/api/collections/techproducts/update' \
  --header 'Content-Type: application/json' \
  --data '  [
  {
    "id" : "978-0641723445",
    "cat" : ["book","hardcover"],
    "name" : "The Lightning Thief",
    "author" : "Rick Riordan",
    "series_t" : "Percy Jackson and the Olympians",
    "sequence_i" : 1,
    "genre_s" : "fantasy",
    "inStock" : true,
    "price" : 12.50,
    "pages_i" : 384
  }
,
  {
    "id" : "978-1423103349",
    "cat" : ["book","paperback"],
    "name" : "The Sea of Monsters",
    "author" : "Rick Riordan",
    "series_t" : "Percy Jackson and the Olympians",
    "sequence_i" : 2,
    "genre_s" : "fantasy",
    "inStock" : true,
    "price" : 6.49,
    "pages_i" : 304
  }
]'
```
- A file containing the documents:
    - NOTE: This file does not exist, so this import will not work as-is.
```
curl -H "Content-Type: application/json" \
       -X POST \
       -d @example/products.json \
       --url 'http://localhost:8983/api/collections/techproducts/update?commit=true'
```

# Commit the Changes
- "After documents are indexed into a collection, they are not immediately available for searching. In order to have them searchable, a commit operation (also called refresh in other search engines like OpenSearch etc.) is needed. Commits can be scheduled at periodic intervals using auto-commits as follows."
- `curl -X POST -H 'Content-type: application/json' -d '{"set-property":{"updateHandler.autoCommit.maxTime":15000}}' http://localhost:8983/api/collections/techproducts/config`

# Make Some Queries
- `curl 'http://localhost:8983/solr/techproducts/select?q=name%3Alightning'`

# Reset Solr to Original State
- `bin/solr stop -all ; rm -Rf example/cloud`

# Start Solr in SolrCloud Mode
- `./bin/solr start -e cloud`
- Set how many Solr nodes `2`.
- Set the port for node1 to `8983`.
- Set the port for node2 to `7574`.
- The commands run by Solr are shown in the terminal and can be run in the future:
    - Start up node1: `bin/solr start -cloud -p 8983 -s "example/cloud/node1/solr"`
    - Start up node2: `bin/solr start -cloud -p 7574 -s "example/cloud/node2/solr" -z localhost:9983`
- Create a collection `techproducts`.
- Set the number of shards to `2`.
- Set the number of replicas per shard to `2`.
- Set the configuration to `sample_techproducts_configs`.

# Index the Techproducts Data
- `bin/post -c techproducts example/exampledocs/*`

# Use the Solr Admin UI to Query
- Open the Solr Admin UI in the browser: http://localhost:8983/
- On the left-hand side select the dropdown "Collection Selector" and choose "techproducts".
- A new menu opens on the left-hand side under the Collection Selector, click on Query.
- Click on Execute Query and you'll see the results of the query (ten documents in the collection).
- Note the URL above the results, this can be used with `curl` or similar to make the same query.
- Note that clicking on the URL above the results returns the raw response.
- The URL should look something like this: `http://localhost:8983/solr/techproducts/select?indent=true&q.op=OR&q=*%3A*&useParams=`
- The `q=` stands for query.
- The operator `*:*` means match all documents in the collection.
- This returns a parse error in curl, "Cannot parse ''*:*'':..."
    - If we use the html entity code for the colon, `%3A`, then it works.

# Returning Only Specific Fields in Response to a Query
- In the Query UI search for 'foundation'
- One can choose which fields are returned using the `fl` parameter, e.g.:
`curl "http://localhost:8983/solr/techproducts/select?q=foundation&fl=id"`

# Limit the Fields Searched for a Query
- We can also limit the fields searched using a field name and the desired search query, e.g.:
`curl "http://localhost:8983/solr/techproducts/select?q=cat:electronics"`

# Searching for a Phrase
- Enclose the phrase in double quotes, e.g.:
`curl "http://localhost:8983/solr/techproducts/select?q=\"CAS+latency\""`
- Note about that we had to escape the inner set of quotes with backslashes, this wouldn't be necessary in the Admin Query UI.

# Query on Exact Multiple Terms / Phrases
- By default Solr requires only one term to be present in a document for it to be included in the results. To require multiple terms or specific phrases you can use `+` before the terms, e.g.: `+electronics +music`:
`curl "http://localhost:8983/solr/techproducts/select?q=%2Belectronics%20%2Bmusic"`
- Can exclude specific terms / phrases using a `-`, for example:
`curl "http://localhost:8983/solr/techproducts/select?q=%2Belectronics+-music"`

# Create a New Collection
- `bin/solr create -c films -s 2 -rf 2`
    - Automatically utilizes the `_default` configset.
    - `-s` sets the number of shards for the collection.
    - `-rf` sets the number of replicas. 
- If we open the Solr Admin UI we can select the films collection from the Collection Selector dropdown as we selected the techproducts collection earlier.

# Working with the Schema API

## Creating the "names" Field
- `curl -X POST -H 'Content-type:application/json' --data-binary '{"add-field": {"name":"name", "type":"text_general", "multiValued":false, "stored":true}}' http://localhost:8983/solr/films/schema`
- This can also be accomplished with slightly less control using the Admin UI.

## Creating a "catchall" Copy Field
- A catchall field is created "defining a copy field that will take all the data from all fields and index it into a field named `_text_`."
- `curl -X POST -H 'Content-type:application/json' --data-binary '{"add-copy-field" : {"source":"*","dest":"_text_"}}' http://localhost:8983/solr/films/schema`
- This can also be accomplished through the Admin UI.

# Index the Film Data
- Import JSON: `bin/post -c films example/films/films.json`
- Or import XML: `bin/post -c films example/films/films.xml`
- Or import CSV: `bin/post -c films example/films/films.csv -params "f.genre.split=true&f.directed_by.split=true&f.genre.separator=|&f.directed_by.separator=|"`

# Query the Film Data
- Open the Admin UI and run Query, you should see 1100 results in the `numFound` field of the `response`, the first ten of which will be displayed.

# Using Faceting
- "Faceting allows the search results to be arranged into subsets (or buckets, or categories)..."
- Types of Faceting:
    - Field Values
    - Numeric and Date Ranges
    - Pivots (Decision Tree)
    - Arbitrary Query Faceting

## Field Facets
- In the Admin UI Query tab check the facet checkbox to see facet-related options appear.
- "To see facet counts from all documents (q=*:*): turn on faceting (facet=true), and specify the field to facet on via the facet.field parameter."
- If you want a list of facets but don't want any of the details of the results you can use `rows=0`.
- Example in curl: `curl "http://localhost:8983/solr/films/select?q=*:*&rows=0&facet=true&facet.field=genre_str"`
- One can use `facet.mincount` to only show facets with at least x documents in them.
- Example in curl: `curl "http://localhost:8983/solr/films/select?=&q=\*:*&facet.field=genre_str&facet.mincount=200&facet=on&rows=0"`

## Range Facets
- Admin UI does not support range facet options.
- curl:
```
curl 'http://localhost:8983/solr/films/select?q=*:*&rows=0'\
'&facet=true'\
'&facet.range=initial_release_date'\
'&facet.range.start=NOW/YEAR-25YEAR'\
'&facet.range.end=NOW'\
'&facet.range.gap=%2B1YEAR'
```
- The above returns all films and groups them by year starting 25 yrs ago and ending today.

## Pivot Facets
- `curl "http://localhost:8983/solr/films/select?q=\*:*&rows=0&facet=on&facet.pivot=genre_str,directed_by_str"`

## Remove Films Collection
- If desired the films collection can be removed using: `bin/solr delete -c films`


# Bibiography/Resources
- https://solr.apache.org/guide/solr/latest/getting-started/solr-tutorial.html
- https://solr.apache.org/guide/solr/latest/getting-started/tutorial-five-minutes.html
- https://solr.apache.org/guide/solr/latest/getting-started/tutorial-techproducts.html
- https://solr.apache.org/guide/solr/latest/getting-started/tutorial-films.html