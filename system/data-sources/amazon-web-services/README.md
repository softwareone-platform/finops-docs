# Amazon Web Services

This topic describes how to add your AWS data sources to the FinOps platform. FinOps for Cloud supports both AWS organizations and individual AWS standalone accounts.&#x20;

## AWS organization <a href="#aws-organizations" id="aws-organizations"></a>

Depending on the access to your management account and other member accounts, there are different ways to add AWS data sources to FinOps for Cloud.&#x20;

{% hint style="info" %}
If you connect the root account but don't connect the linked accounts, all expenses from the unconnected linked accounts are ignored, even if they exist in the data export file. To retrieve expenses from both linked and root accounts, connect all AWS accounts (not just the root). FinOps for Cloud ignores data from unconnected linked accounts.
{% endhint %}

### With access to the management account <a href="#with-access-to-the-management-account" id="with-access-to-the-management-account"></a>

If you have access to create a Cost and Usage Report (CUR) and Identity and Access Management (IAM) users in your management account, follow these steps:

{% stepper %}
{% step %}
#### Add your management account <a href="#add-your-management-account" id="add-your-management-account"></a>

To add your management account:

1. [Create a Cost and Usage Report in AWS](create-a-cost-and-usage-report.md).
2. [Create the `FinOpsForCloudBillingImport` ](configure-aws-access.md#create-a-policy-for-billing-imports)[IAM policy](configure-aws-access.md#create-a-policy-for-billing-imports).
3. [Create the `FinOpsForCloudResourceDiscovery` IAM policy](configure-aws-access.md#creating-a-policy-for-resource-discovery).
4. [Create the `FinOpsForCloudUser` IAM user](configure-aws-access.md#create-a-user-for-finops-for-cloud).
5. [Create an access key for the `FinOpsForCloudUser` IAM user](configure-aws-access.md#create-an-access-key-for-finops-for-cloud).
6. [Add the management account to your FinOps for Cloud data sources as an AWS Root account.](../)&#x20;
{% endstep %}

{% step %}
#### Add your member accounts to FinOps for Cloud <a href="#add-your-member-accounts" id="add-your-member-accounts"></a>

To add your member accounts:

1. [Create the `FinOpsForCloudResourceDiscovery` IAM policy](configure-aws-access.md#creating-a-policy-for-resource-discovery).
2. [Create the `FinOpsForCloudUser` IAM user](configure-aws-access.md#create-a-user-for-finops-for-cloud).
3. [Create an access key for the `FinOpsForCloudUser` IAM user](configure-aws-access.md#create-an-access-key-for-finops-for-cloud).
4. [Add the member account to your FinOps for Cloud data sources as an AWS-linked account. ](../)
5. Repeat steps 1 - 4 for each member account you want to add.
{% endstep %}
{% endstepper %}

When the member accounts are added, FinOps for Cloud automatically identifies the management account and uses the imported cost and usage data from that account.

### Without access to the management account <a href="#without-access-to-the-management-account" id="without-access-to-the-management-account"></a>

If you don't have access to your management account, you can create individual CURs in each member account and add them to FinOps for Cloud as if they were AWS Root Accounts.

To add your member account to FinOps as an **AWS Root** account:

1. [Create a Cost and Usage report in AWS.](create-a-cost-and-usage-report.md)
2. [Create the `FinOpsForCloudBillingImport` IAM policy](configure-aws-access.md#create-a-policy-for-billing-imports).
3. [Create the `FinOpsForCloudResourceDiscovery` IAM policy](configure-aws-access.md#creating-a-policy-for-resource-discovery).
4. [Create the `FinOpsForCloudUser` IAM user](configure-aws-access.md#create-a-user-for-finops-for-cloud).
5. [Create an access key for the `FinOpsForCloudUser` IAM user](configure-aws-access.md#create-an-access-key-for-finops-for-cloud).
6. [Add the member account to your FinOps for Cloud data sources as an AWS Root account](../).

## AWS standalone accounts <a href="#aws-standalone-accounts" id="aws-standalone-accounts"></a>

To add a standalone AWS account:

1. [Create a Cost and Usage report in AWS.](create-a-cost-and-usage-report.md)
2. [Create the `FinOpsForCloudBillingImport` IAM policy](configure-aws-access.md#create-a-policy-for-billing-imports).
3. [Create the `FinOpsForCloudResourceDiscovery` IAM policy](configure-aws-access.md#creating-a-policy-for-resource-discovery).
4. [Create the `FinOpsForCloudUser` IAM user](configure-aws-access.md#create-a-user-for-finops-for-cloud).
5. [Create an access key for the `FinOpsForCloudUser` IAM user](configure-aws-access.md#create-an-access-key-for-finops-for-cloud).
6. [Add the standalone account to your FinOps for Cloud data sources as an AWS Root account.](../)
