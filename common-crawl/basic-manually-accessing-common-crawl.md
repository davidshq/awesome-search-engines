# How To Manually Access CommonCrawl


## Introduction

I sometimes find it helpful to understand the intricacies of a process by performing it manually before attempting to automate it. This document outlines a manual process for retrieving data from CommonCrawl.

**NOTE**: There is a web search interface one can use and one can download the files over HTTP but both of these are quite slow. I'll only be covering how to accomplish the crawl using Amazon S3 (where the data is stored).

## Prerequisites

You'll need to have an AWS account, the AWS CLI installed, and programmatic access setup on your local system.

## Choose a Crawl

Crawls are organized by date. You can go to http://index.commoncrawl.org/ to view the list of available crawls.

For this example I'm using CC-MAIN-2023-14.

## Download the Index List

You can see the list of index files on the previously mentioned page. We'll grab the one for our selected crawl using the AWS CLI:
`aws s3 cp s3://commoncrawl/crawl-data/CC-MAIN-2023-14/cc-index.paths.gz .`

NOTE: The `.` in the above command is very important. The AWS CLI command is saying copy from the specified path on S3 to the specified path on the local system. The dot `.` will drop the file wherever you are running the command from. You can also specify a specific path instead of using `.`

## Opening the File

Extract the contents of the gzip file and the result should be a file called `cc-index.paths`. This can be opened with a regular text editor.

Scroll to the bottom and you'll find the path to get the `cluster.idx` file.

## Downloading the Cluster Index

In our case the path shown is `cc-index/collections/CC-MAIN-2023-14/indexes/cluster.idx`. Using the AWS CLI our command should look like:
`aws s3 cp s3://commoncrawl/cc-index/collections/CC-MAIN-2023-14/indexes/cluster.idx .`

This file is quite a bit larger (~150 MB) and may take a few minutes to download. 

## Opening the Cluster Index

There are a number of ways we could manipulate the file without opening it in a normal editor but for the moment lets do just that. A cross-platform program that can handle large files with a GUI is [klogg](https://klogg.filimonov.dev/).

You should see data that looks something like this:

```
0,1,184,137)/igplay 20230325212225	cdx-00000.gz	0	158603	1
10,124,97,161)/paito-warna-trinidad-tobago-afternoon 20230330213447	cdx-00000.gz	158603	187900	2
```

The above is two lines of data. Each contains the reversed domain of a site indexed by CommonCrawl (`0,1,184,137`, `10,124,97,161`) followed by the specific path that was indexed (e.g. `/igplay`, `/paito-warna-trinidad`...).

This can be a little confusing at first glance. Where are the domain names? Sometimes servers don't have a domain name and instead are accessed by IP, because when sorting a file numeric characters come before alpha characters the file starts off with all the IPs it has crawled.

Scroll down a bit in the file and you should start to see records that look like this:

```
com,homesandgardens)/gardens/how-to-split-irises 20230330183612	cdx-00077.gz	736773153	222043	311253
```

Note that whether the site is a domain or an IP it is reversed and separated by levels. If we reassemble the IPs/domains from the above examples we get:
```
137.184.1.0
161.97.124.10
homesandgardens.com
```

## Finding and Downloading the CDX We Need

If we are looking to access specific site data we need to figure out what CDX file serves as the index. In the case of the `homesandgardens.com` URL we can see that the CDX is `cdx-00077.gz`.

We'll use the AWS CLI to download this file:
```
aws s3 cp s3://commoncrawl/cc-index/collections/CC-MAIN-2023-14/indexes/cdx-00077.gz .
```

This file, again, is much larger than the previous files (closing in on 1 GB) so it may take some time to download. 

## Finding and Downloading the WARC We Need

Once downloaded we need to extract the contents from the gzip, which should be a plain text file called `cdx-00072`. Extracted this file will likely be several GB in size.

When we open the file (using `klogg` or something similar) we should see records that look like this:

```
com,homes-n-gardens)/adult-coloring-pages-garden 20230402111251 {"url": "https://homes-n-gardens.com/adult-coloring-pages-garden/", "mime": "text/html", "mime-detected": "text/html", "status": "200", "digest": "XJHZYZYMKOL62PIT56QEUFJT5MYNYVOT", "length": "3991", "offset": "343066379", "filename": "crawl-data/CC-MAIN-2023-14/segments/1679296950528.96/warc/CC-MAIN-20230402105054-20230402135054-00060.warc.gz", "charset": "UTF-8", "languages": "eng"}
```

NOTE: See Appendix A for a prettified version of the JSON above.

Note that we again have the reversed domain name at the beginning followed by the path to the specific file/document accessed and a little later we have `"filename":`. The filename specified here is the file we need to access to retrieve the data for the specific URL we are looking at. In this case it is:

```
"crawl-data/CC-MAIN-2023-14/segments/1679296950528.96/warc/CC-MAIN-20230402105054-20230402135054-00060.warc.gz"
```

We can get the WARC file using the AWS CLI:
```
aws s3 cp s3://commoncrawl/crawl-data/CC-MAIN-2023-14/segments/1679296950528.96/warc/CC-MAIN-20230402105054-20230402135054-00060.warc.gz .
```

This file is likely to clock in at over 1 GB in it's compressed form - so expect the download to take some time.

## Viewing the WARC

Once again we'll extract the file from it's gzip. We should end up with a file titled: `CC-MAIN-20230402105054-20230402135054-00060.warc`. We can open this file using klogg as well. Much of the file will be human readable but there will also be binary files that have been included (e.g. images) and these will appear as a long series of garbled characters.

# Appendix A: Prettified JSON CDX Record
```json
{
  "url": "https://homes-n-gardens.com/adult-coloring-pages-garden/",
  "mime": "text/html",
  "mime-detected": "text/html",
  "status": "200",
  "digest": "XJHZYZYMKOL62PIT56QEUFJT5MYNYVOT",
  "length": "3991",
  "offset": "343066379",
  "filename": "crawl-data/CC-MAIN-2023-14/segments/1679296950528.96/warc/CC-MAIN-20230402105054-20230402135054-00060.warc.gz",
  "charset": "UTF-8",
  "languages": "eng"
}
```


# Bibliography

- [StackOverflow: How to view huge txt files in Linux?](https://stackoverflow.com/questions/21246752/how-to-view-huge-txt-files-in-linux)
- Samuel Schaffhauser. [Using the Common Crawl as a Data Source](https://medium.com/@samuel.schaffhauser/using-the-common-crawl-as-a-data-source-693a41b3baa9). 6/2022.
- Chillar Anand. [Common Crawl On Laptop - Extracting Subset of Data](https://avilpage.com/2022/11/common-crawl-laptop-extract-subset.html). 11/2022.