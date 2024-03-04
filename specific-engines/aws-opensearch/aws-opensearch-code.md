# AWS OpenSearch - Writing Code

## Introduction

One of the stranger aspects of AWS' documentation on OpenSearch is it's relative lack of code samples. One would expect to find something comprehensive in the [Amazon OpenSearch Service Developer Guide's Sample Code](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/samplecode.html) section, but the section is extremely brief and only tangentially mentions Elasticsearch (not even OpenSeach) language clients. If you dig through [Using the AWS SDKs](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/configuration-samples.html) subsection there is some reference - but you have to dig for it (at least imho).

There is also a tutorial on [Creating a search application](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/search-example.html) but this is quite limited in scope and depends on a specific architecture (Amazon API Gateway <--> AWS Lambda <--> Amazon OpenSearch Service).

Ironically, nested under OpenSearch Serverless one can find some additional code (though beware that the serverless offering and managed offering have significant differences) in [Using the AWS SDKs to interact with Amazon OpenSearch Serverless](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/serverless-sdk.html) and [Ingesting data into collections](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/serverless-clients.html).

This section attempts to provide a gentler and more rounded conversation of writing code for AWS OpenSearch Service.

## Clients

One can perform operational tasks on an OpenSearch cluster using the AWS SDK in various languages but this does not provide an interface for querying the cluster.
- [Java AWS SDK: OpenSearch](https://sdk.amazonaws.com/java/api/latest/software/amazon/awssdk/services/opensearch/package-summary.html)
- [JavaScript AWS SDK: OpenSearch](https://docs.aws.amazon.com/AWSJavaScriptSDK/v3/latest/client/opensearch/)
- [Python AWS Boto3: OpenSearch](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/opensearch.html)

Instead one needs to use the [OpenSearch language-specific clients](https://opensearch.org/docs/latest/clients/) for this task. Currently these are available for Python, Java, JavaScript, Go, Ruby, PHP, .NET, and Rust.

