---
description: >-
  Learn how you can add your AWS data sources to the FinOps platform. FinOps for
  Cloud supports both AWS organizations and individual AWS standalone accounts.
---

# Amazon Web Services

## Know your account types

FinOps for Cloud supports three account types as described in the following table:

{% hint style="warning" %}
If you want to add a member account in an AWS Organization to FinOps for Cloud, but you do not have access to the management account, follow the instructions for a [standalone account](./#aws-standalone-accounts).
{% endhint %}

<table><thead><tr><th width="179" valign="top">Term</th><th valign="top">Definition and use</th></tr></thead><tbody><tr><td valign="top">Management account</td><td valign="top"><p>A management account is an AWS account you use to create your AWS Organization. The owner of the management account is responsible for paying for all usage, data, and resources used by the accounts in the organization.</p><p></p><p>A management account is also called a root account, master account, billing account, or payer account.</p><p></p><p>In FinOps for Cloud, use this account type when adding an AWS Organization <a href="./#with-access-to-the-management-account">management account</a>.</p></td></tr><tr><td valign="top">Member account</td><td valign="top"><p>A member account is an AWS account, other than the management account, that is part of an AWS Organization. The management account is responsible for paying for all member accounts in the organization.</p><p></p><p>A member account is also referred to as a linked account, child account, usage account, or sub-account.</p><p></p><p>In FinOps for Cloud, use this account type when adding an AWS Organization member account, <a href="./#with-access-to-the-management-account">and the management account has already been added to FinOps for Cloud</a>.</p></td></tr><tr><td valign="top">Standalone account</td><td valign="top"><p>A standalone account refers to an account that is not part of an AWS Organization. It stands on its own, without being linked to any other accounts for consolidated billing, management, or policy control.</p><p></p><p>A standalone account is also referred to as an individual account, non-organizational account, or unlinked account.</p><p></p><p>In FinOps for Cloud, use this account type when:</p><ul><li>Adding <a href="./#aws-standalone-accounts">standalone AWS account</a> that is not part of an AWS Organization</li><li>Adding an AWS member account that is part of an AWS Organization, <a href="./#without-access-to-the-management-account">but access to the management account is not available</a>.</li></ul></td></tr></tbody></table>

## Assumed roles vs IAM user access keys <a href="#aws-organizations" id="aws-organizations"></a>

FinOps for Cloud supports adding data sources using two authentication methods:

* **Assumed role** - This is the recommended approach to adding AWS accounts to FinOps for Cloud. An IAM role is an identity that does not have its own permanent credentials (password or access keys). Instead, it defines permissions that a trusted entity (such as an AWS service, another AWS account, or an application running on an EC2 instance) can _assume_ to obtain temporary security credentials.
* **IAM user with access key** - Access keys are a set of permanent credentials consisting of an Access Key ID and a Secret Access Key. They are associated with a specific IAM User (or the root user, which is strongly discouraged) and are used for making programmatic API requests to AWS, typically from the AWS CLI, SDKs, or third-party applications. Read more about the security risks associated with this approach in the [AWS documentation](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_access-keys.html).

{% hint style="info" %}
SoftwareOne strongly recommends using assumed roles to configure your data sources.
{% endhint %}

## Configuring your AWS accounts <a href="#aws-organizations" id="aws-organizations"></a>

### AWS Organizations <a href="#aws-organizations" id="aws-organizations"></a>

Depending on the access to your management account and other member accounts, there are different ways to add AWS data sources to FinOps for Cloud.&#x20;

{% hint style="info" %}
If you add only a management account without connecting its member accounts, any expenses from those unconnected member accounts are ignored, even if they appear in the data export file.

To ensure expenses are captured for both management and member accounts, you must add all AWS accounts individually. FinOps for Cloud doesn't process data from unconnected member accounts.
{% endhint %}

#### With access to the management account <a href="#with-access-to-the-management-account" id="with-access-to-the-management-account"></a>

If you have access to create a Cost and Usage Report (CUR) and Identity and Access Management (IAM) roles or users in your management account, follow these steps:

{% stepper %}
{% step %}
#### Add your management account <a href="#add-your-management-account" id="add-your-management-account"></a>

To add your management account:

1. [Create a Cost and Usage Report in AWS](create-cost-and-usage-reports.md).
2. [Create the `FinOpsForCloudBillingImport` ](configure-aws-access.md#create-a-policy-for-billing-imports)[IAM role policy](https://docs.finops.softwareone.com/system/data-sources/amazon-web-services/configure-aws-access#create-a-policy-for-billing-imports).
3. [Create the `FinOpsForCloudResourceDiscovery` IAM role policy](https://docs.finops.softwareone.com/system/data-sources/amazon-web-services/configure-aws-access#create-a-policy-for-resource-discovery).
4. If you are using an assumed role (recommended):
   1. [Create the `FinOpsForCloudAccessRole` IAM role](https://docs.finops.softwareone.com/system/data-sources/amazon-web-services/configure-aws-access#creating-a-new-iam-role).
5. If you are using an IAM user with an access key:
   1. [Create the `FinOpsForCloudUser` IAM user](https://docs.finops.softwareone.com/system/data-sources/amazon-web-services/configure-aws-access#creating-a-new-iam-user).
   2. [Create an access key for the `FinOpsForCloudUser` IAM user](https://docs.finops.softwareone.com/system/data-sources/amazon-web-services/configure-aws-access#creating-an-access-key-for-finops-for-cloud).
6. [Add the management account data source to FinOps for Cloud.](https://docs.finops.softwareone.com/system/data-sources/amazon-web-services/add-your-aws-account-to-finops-for-cloud#adding-a-management-or-standalone-aws-account)&#x20;
{% endstep %}

{% step %}
#### Add your member accounts to FinOps for Cloud <a href="#add-your-member-accounts" id="add-your-member-accounts"></a>

{% hint style="info" %}
When adding a member account, and you have already added the management account, there is no need to create a cost and usage report or create the `FinOpsForCloudBillingImport` policy.
{% endhint %}

To add your member accounts:

1. [Create the `FinOpsForCloudResourceDiscovery` IAM policy](https://docs.finops.softwareone.com/system/data-sources/amazon-web-services/configure-aws-access#create-a-policy-for-resource-discovery).
2. If you are using an assumed role (recommended):
   1. [Create the `FinOpsForCloudAccessRole` IAM role](https://docs.finops.softwareone.com/system/data-sources/amazon-web-services/configure-aws-access#creating-a-new-iam-role).
3. If you are using an IAM user with an access key:
   1. [Create the `FinOpsForCloudUser` IAM user](https://docs.finops.softwareone.com/system/data-sources/amazon-web-services/configure-aws-access#creating-a-new-iam-user).
   2. [Create an access key for the `FinOpsForCloudUser` IAM user](https://docs.finops.softwareone.com/system/data-sources/amazon-web-services/configure-aws-access#creating-an-access-key-for-finops-for-cloud).
4. [Add the member account data source to FinOps for Cloud.](https://docs.finops.softwareone.com/system/data-sources/amazon-web-services/add-your-aws-account-to-finops-for-cloud#adding-a-member-aws-account)
5. Repeat steps 1 - 4 for each member account you want to add.
{% endstep %}
{% endstepper %}

{% hint style="success" %}
When the member accounts are added, FinOps for Cloud automatically identifies the management account and uses the imported cost and usage data from that account.
{% endhint %}

#### Without access to the management account <a href="#without-access-to-the-management-account" id="without-access-to-the-management-account"></a>

If you don't have access to your management account, you can create individual CURs in each member account and add them to FinOps for Cloud as if they were standalone accounts.

To add your member account to FinOps for Cloud, follow the steps below for [AWS standalone accounts](./#aws-standalone-accounts).

### AWS standalone accounts <a href="#aws-standalone-accounts" id="aws-standalone-accounts"></a>

To add a standalone AWS account:

1. [Create a Cost and Usage report in AWS.](create-cost-and-usage-reports.md)
2. [Create the `FinOpsForCloudBillingImport` IAM policy](https://docs.finops.softwareone.com/system/data-sources/amazon-web-services/configure-aws-access#create-a-policy-for-billing-imports).
3. [Create the `FinOpsForCloudResourceDiscovery` IAM policy](https://docs.finops.softwareone.com/system/data-sources/amazon-web-services/configure-aws-access#create-a-policy-for-resource-discovery).
4. If you are using an assumed role (recommended):
   1. [Create the `FinOpsForCloudAccessRole` IAM role](https://docs.finops.softwareone.com/system/data-sources/amazon-web-services/configure-aws-access#creating-a-new-iam-role).
5. If you are using an IAM user with an access key:
   1. [Create the `FinOpsForCloudUser` IAM user](https://docs.finops.softwareone.com/system/data-sources/amazon-web-services/configure-aws-access#creating-a-new-iam-user).
   2. [Create an access key for the `FinOpsForCloudUser` IAM user](https://docs.finops.softwareone.com/system/data-sources/amazon-web-services/configure-aws-access#creating-an-access-key-for-finops-for-cloud).
6. [Add the standalone account data source to FinOps for Cloud.](https://docs.finops.softwareone.com/system/data-sources/amazon-web-services/add-your-aws-account-to-finops-for-cloud#adding-a-management-or-standalone-aws-account)
