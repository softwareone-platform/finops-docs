# Amazon Web Services

This topic describes how you can add your AWS data sources to the FinOps platform. FinOps for Cloud supports both AWS organizations and individual AWS standalone accounts.&#x20;

## AWS terminology

The following table contains the terminology that applies to AWS data sources.

<table><thead><tr><th width="190" valign="top">Term</th><th valign="top">Definition</th></tr></thead><tbody><tr><td valign="top">Management account</td><td valign="top"><p>A management account is an AWS account you use to create your AWS Organization. The owner of the management account is responsible for paying for all usage, data, and resources used by the accounts in the organization.</p><p></p><p>A management account is also called a root account, master account, billing account, or payer account.</p></td></tr><tr><td valign="top">Member account</td><td valign="top"><p>A member account is an AWS account, other than the management account, that is part of an AWS Organization. The management account is responsible for paying for all member accounts in the organization.</p><p></p><p>A member account is also referred to as a linked account, child account, usage account, or sub-account.</p></td></tr><tr><td valign="top">Standalone account</td><td valign="top"><p>A standalone account refers to an account that is not part of an AWS Organization. It stands on its own, without being linked to any other accounts for consolidated billing, management, or policy control.</p><p></p><p>A standalone account is also referred to as an individual account, non-organizational account, or unlinked account.</p></td></tr></tbody></table>

## FinOps for Cloud terminology <a href="#aws-organizations" id="aws-organizations"></a>

The following terminology is used in FinOps for Cloud when adding an AWS data source.

<table><thead><tr><th width="200" valign="top">Term</th><th valign="top">Usage</th></tr></thead><tbody><tr><td valign="top">Root</td><td valign="top"><p>Use this option when:</p><ol><li>Adding an AWS organization <a href="./#with-access-to-the-management-account">management account</a>.</li><li>Adding an AWS organization member account (<a href="./#without-access-to-the-management-account">when you don't have access to a management account</a>)</li><li>Adding an AWS <a href="./#aws-standalone-accounts">standalone account</a>.</li></ol></td></tr><tr><td valign="top">Linked</td><td valign="top">Use this option when adding an AWS organization member account, <a href="./#with-access-to-the-management-account">and the management account is already added</a>.</td></tr></tbody></table>

## Configuring your AWS accounts <a href="#aws-organizations" id="aws-organizations"></a>

### AWS organizations <a href="#aws-organizations" id="aws-organizations"></a>

Depending on the access to your management account and other member accounts, there are different ways to add AWS data sources to FinOps for Cloud.&#x20;

{% hint style="info" %}
If you connect the root account but don't connect the linked accounts, all expenses from the unconnected linked accounts are ignored, even if they exist in the data export file. To retrieve expenses from both linked and root accounts, connect all AWS accounts (not just the root). FinOps for Cloud ignores data from unconnected linked accounts.
{% endhint %}

#### With access to the management account <a href="#with-access-to-the-management-account" id="with-access-to-the-management-account"></a>

If you have access to create a Cost and Usage Report (CUR) and Identity and Access Management (IAM) users in your management account, follow these steps:

{% stepper %}
{% step %}
#### Add your management account <a href="#add-your-management-account" id="add-your-management-account"></a>

To add your management account:

1. [Create a Cost and Usage Report in AWS](create-cost-and-usage-reports.md).
2. [Create the `FinOpsForCloudBillingImport` ](configure-aws-access.md#create-a-policy-for-billing-imports)[IAM policy](configure-aws-access.md#create-a-policy-for-billing-imports).
3. [Create the `FinOpsForCloudResourceDiscovery` IAM policy](configure-aws-access.md#creating-a-policy-for-resource-discovery).
4. [Create the `FinOpsForCloudUser` IAM user](configure-aws-access.md#create-a-user-for-finops-for-cloud).
5. [Create an access key for the `FinOpsForCloudUser` IAM user](configure-aws-access.md#create-an-access-key-for-finops-for-cloud).
6. [Add the management account to your FinOps for Cloud data sources as an AWS **Root** account.](../../../finops-for-cloud/getting-started/data-sources.md)&#x20;
{% endstep %}

{% step %}
#### Add your member accounts to FinOps for Cloud <a href="#add-your-member-accounts" id="add-your-member-accounts"></a>

To add your member accounts:

1. [Create the `FinOpsForCloudResourceDiscovery` IAM policy](configure-aws-access.md#creating-a-policy-for-resource-discovery).
2. [Create the `FinOpsForCloudUser` IAM user](configure-aws-access.md#create-a-user-for-finops-for-cloud).
3. [Create an access key for the `FinOpsForCloudUser` IAM user](configure-aws-access.md#create-an-access-key-for-finops-for-cloud).
4. [Add the member account to your FinOps for Cloud data sources as an AWS **Linked** account. ](../../../finops-for-cloud/getting-started/data-sources.md)
5. Repeat steps 1 - 4 for each member account you want to add.
{% endstep %}
{% endstepper %}

When the member accounts are added, FinOps for Cloud automatically identifies the management account and uses the imported cost and usage data from that account.

#### Without access to the management account <a href="#without-access-to-the-management-account" id="without-access-to-the-management-account"></a>

If you don't have access to your management account, you can create individual CURs in each member account and add them to FinOps for Cloud as if they were AWS Root Accounts.

To add your member account to FinOps as an **AWS Root** account:

1. [Create a Cost and Usage report in AWS.](create-cost-and-usage-reports.md)
2. [Create the `FinOpsForCloudBillingImport` IAM policy](configure-aws-access.md#create-a-policy-for-billing-imports).
3. [Create the `FinOpsForCloudResourceDiscovery` IAM policy](configure-aws-access.md#creating-a-policy-for-resource-discovery).
4. [Create the `FinOpsForCloudUser` IAM user](configure-aws-access.md#create-a-user-for-finops-for-cloud).
5. [Create an access key for the `FinOpsForCloudUser` IAM user](configure-aws-access.md#create-an-access-key-for-finops-for-cloud).
6. [Add the member account to your FinOps for Cloud data sources as an AWS **Root** account](../../../finops-for-cloud/getting-started/data-sources.md).

### AWS standalone accounts <a href="#aws-standalone-accounts" id="aws-standalone-accounts"></a>

To add a standalone AWS account:

1. [Create a Cost and Usage report in AWS.](create-cost-and-usage-reports.md)
2. [Create the `FinOpsForCloudBillingImport` IAM policy](configure-aws-access.md#create-a-policy-for-billing-imports).
3. [Create the `FinOpsForCloudResourceDiscovery` IAM policy](configure-aws-access.md#creating-a-policy-for-resource-discovery).
4. [Create the `FinOpsForCloudUser` IAM user](configure-aws-access.md#create-a-user-for-finops-for-cloud).
5. [Create an access key for the `FinOpsForCloudUser` IAM user](configure-aws-access.md#create-an-access-key-for-finops-for-cloud).
6. [Add the standalone account to your FinOps for Cloud data sources as an AWS **Root** account.](../../../finops-for-cloud/getting-started/data-sources.md)
