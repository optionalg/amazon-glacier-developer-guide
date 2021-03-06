# What Is Amazon Glacier?<a name="introduction"></a>

Welcome to the *Amazon Glacier Developer Guide*\. Amazon Glacier is a storage service optimized for infrequently used data, or "cold data\."

Amazon Glacier is an extremely low\-cost storage service that provides durable storage with security features for data archiving and backup\. With Amazon Glacier, customers can store their data cost effectively for months, years, or even decades\. Amazon Glacier enables customers to offload the administrative burdens of operating and scaling storage to AWS, so they don't have to worry about capacity planning, hardware provisioning, data replication, hardware failure detection and recovery, or time\-consuming hardware migrations\. For more service highlights and pricing information, go to the [Amazon Glacier detail page](https://aws.amazon.com/glacier)\. 

Amazon Glacier is a great storage choice when low storage cost is paramount, your data is rarely retrieved, and retrieval latency of several hours is acceptable\. If your application requires fast or frequent access to your data, consider using Amazon S3\. For more information, go to [Amazon Simple Storage Service \(Amazon S3\)](https://aws.amazon.com/s3/)\.


+ [Are You a First\-Time Amazon Glacier User?](#are-you-a-firsttime-glacier-user)
+ [Amazon Glacier Data Model](amazon-glacier-data-model.md)
+ [Supported Operations in Amazon Glacier](amazon-glacier-supported-operations.md)
+ [Accessing Amazon Glacier](amazon-glacier-accessing.md)

## Are You a First\-Time Amazon Glacier User?<a name="are-you-a-firsttime-glacier-user"></a>

If you are a first\-time user of Amazon Glacier, we recommend that you begin by reading the following sections:

+ **What is Amazon Glacier—**The rest of this section describes the underlying data model, the operations it supports, and the AWS SDKs that you can use to interact with the service\. 

+ **Getting Started—**The [Getting Started with Amazon Glacier](amazon-glacier-getting-started.md) section walks you through the process of creating a vault, uploading archives, creating jobs to download archives, retrieving the job output, and deleting archives\. 
**Important**  
Amazon Glacier provides a console, which you can use to create and delete vaults\. However, all other interactions with Amazon Glacier require that you use the AWS Command Line Interface \(AWS CLI\) or write code\. For example, to upload data, such as photos, videos, and other documents, you must either use the AWS CLI or write code to make requests, by using either the REST API directly or by using the AWS SDKs\. For more information about using Amazon Glacier with the AWS CLI, go to [AWS CLI Reference for Amazon Glacier](http://docs.aws.amazon.com/cli/latest/reference/glacier/index.html)\. To install the AWS CLI, go to [AWS Command Line Interface](http://aws.amazon.com/cli/)\.

Beyond the getting started section, you'll probably want to learn more about Amazon Glacier operations\. The following sections provide detailed information about working with Amazon Glacier using the REST API and the AWS Software Development Kits \(SDKs\) for Java and Microsoft \.NET: 

+ [Using the AWS SDKs with Amazon Glacier](using-aws-sdk.md)

  This section provides an overview of the AWS SDKs used in various code examples in this guide\. A review of this section will help when reading the following sections\. It includes an overview of the high\-level and the low\-level APIs that these SDKs offer, when to use them, and common steps for running the code examples provided in this guide\. 

+ [Working with Vaults in Amazon Glacier](working-with-vaults.md)

  This section provides details of various vault operations such as creating a vault, retrieving vault metadata, using jobs to retrieve vault inventory, and configuring vault notifications\. In addition to using the Amazon Glacier console, you can use the AWS SDKs for various vault operations\. This section describes the API and provides working samples using the AWS SDK for Java and \.NET\.

+ [Working with Archives in Amazon Glacier](working-with-archives.md)

  This section provides details of archive operations such as uploading an archive in a single request or using a multipart upload operation to upload large archives in parts\. The section also explains creating jobs to download archives asynchronously\. The section provides examples using the AWS SDK for Java and \.NET\.

+ [API Reference for Amazon Glacier](amazon-glacier-api.md)

  Amazon Glacier is a RESTful service\. This section describes the REST operations, including the syntax, and example requests and responses for all the operations\. Note that the AWS SDK libraries wrap this API, simplifying your programming tasks\. 

Amazon Simple Storage Service \(Amazon S3\) supports lifecycle configuration on a bucket that enables you to optionally transition objects to Amazon Glacier for archival purposes\. When you transition Amazon S3 objects to the Glacier storage class, Amazon S3 internally uses Amazon Glacier for durable storage at lower cost\. For more information about lifecycle configuration and transitioning objects to Amazon Glacier, go to [Object Lifecycle Management](http://docs.aws.amazon.com/AmazonS3/latest/dev/object-lifecycle-mgmt.html) and [Object Archival](http://docs.aws.amazon.com/AmazonS3/latest/dev/object-archival.html) in the *Amazon Simple Storage Service Developer Guide*\.