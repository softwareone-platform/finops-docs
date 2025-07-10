# How FinOps for Cloud Works

FinOps for Cloud supports three major cloud service providers, including Amazon Web Services (AWS), Google Cloud Platform (GCP), and Microsoft Azure.

To use FinOps, you only need to provide **read-only** access to your connected cloud account. This allows FinOps to view and retrieve data without making any changes. It also that FinOps does not interfere with any processes in your environment.

When the read-only access has been granted, the following data is used:&#x20;

* Billing information, including all details related to your cloud expenses.
* For actively discoverable types, the current state of resources is collected. This is essential for implementing constraints like Time to Live (TTL), expense limits, and recommendations.
* Monitoring data from the cloud is used to identify underutilized instances.

The following sections explain how FinOps for Cloud obtains these details for each of the supported cloud platforms.

## Amazon Web Services

For AWS accounts:

* The billing information is retrieved from the Data Exports located in a designated S3 bucket in the cloud. For details, see [GetObject](https://docs.aws.amazon.com/AmazonS3/latest/API/API_GetObject.html) in the AWS S3 API Reference Guide.
* [Amazon CloudWatch](https://docs.aws.amazon.com/cloudwatch/) is the source of monitoring data.&#x20;
* Resource discovery is done using the Discovery API. For reference, see the following pages in the Amazon EC2 API Reference:
  * [DescribeInstances](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_DescribeInstances.html) - Describes the specified instances or all instances.
  * [DescribeVolumes](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_DescribeVolumes.html) - Describes the specified EBS volumes or all of your EBS volumes.
  * [DescribeSnapshots](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_DescribeSnapshots.html) - Describes the specified EBS snapshots available to you or all of the EBS snapshots available to you.
  * [ListBuckets](https://docs.aws.amazon.com/AmazonS3/latest/API/API_ListBuckets.html) - Returns a list of all buckets owned by the authenticated sender of the request.

## Microsoft Azure

For Azure cloud accounts:

* The billing information is retrieved from the Billing API. For details, see [Usage Details - List](https://learn.microsoft.com/en-us/rest/api/consumption/usage-details/list?view=rest-consumption-2024-08-01\&tabs=HTTP) in the Microsoft documentation.
* Cloud's monitoring service is used as the source of all monitoring data.
* Resource discovery is done using the Discovery API. For reference, see the following pages in Microsoft documentation:
  * [Virtual Machines - List All](https://docs.microsoft.com/en-us/rest/api/compute/virtual-machines/list-all) - Lists all of the virtual machines in the specified subscription.
  * [Disks - List](https://docs.microsoft.com/en-us/rest/api/compute/disks/list) - Lists all the disks under a subscription.
  * [Snapshots - List](https://docs.microsoft.com/en-us/rest/api/compute/snapshots/list) - Lists snapshots under a subscription.
  * [Storage Accounts - List](https://docs.microsoft.com/en-us/rest/api/storagerp/storage-accounts/list) - Lists all the storage accounts available under the subscription.

## Google Cloud Platform

For Google Cloud accounts:

* The billing information is retrieved from the BigQuery Service.
* Cloud's monitoring service is used as the source of all monitoring data.
* Resource discovery is done using the Discovery API. For reference, see the following pages in Google Cloud documentation:
  * [Method: instances.list](https://cloud.google.com/compute/docs/reference/rest/v1/instances/list) - Retrieves the list of instances contained within the specified zone.
  * [Method: disks.list](https://cloud.google.com/compute/docs/reference/rest/v1/disks/list) - Retrieves a list of persistent disks contained within the specified zone.
  * [Method: snapshots.list](https://cloud.google.com/compute/docs/reference/rest/v1/snapshots/list) - Retrieves the list of Snapshot resources contained within the specified project.
  * [Buckets: list](https://cloud.google.com/storage/docs/json_api/v1/buckets/list) - Retrieves a list of buckets for a given project, ordered in the list lexicographically by name.
  * [Method: addresses.list](https://cloud.google.com/compute/docs/reference/rest/v1/addresses/list) - Retrieves a list of addresses contained within the specified region.
