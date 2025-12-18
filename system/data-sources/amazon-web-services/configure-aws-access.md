# Configure AWS Access

## AWS IAM Policies <a href="#aws-iam-policies" id="aws-iam-policies"></a>

FinOps for Cloud requires two policies, depending on the type of account being onboarded:

* **Billing import access policy** - This policy allows FinOps for Cloud to read cost and usage data from the configured S3 bucket. This policy is only required when you are onboarding an account that contains a cost and usage report.
* **Resource discovery access policy** - This policy allows FinOps for Cloud to discover new and changed resources in your AWS account more often than AWS updates the cost and usage reports. This allows FinOps for Cloud to show information about your spend that is more up-to-date than what is contained in the cost and usage report.

### Creating a policy for billing imports <a href="#create-a-policy-for-billing-imports" id="create-a-policy-for-billing-imports"></a>

The billing import access policy is only required for accounts with cost and usage reports configured for FinOps for Cloud.

A suggested name for the policy is `FinOpsForCloudBillingImport`.

{% hint style="warning" %}
In the following policy, be sure to replace `<bucket_name>` with a valid name of your S3 bucket.
{% endhint %}

{% code lineNumbers="true" %}
```json
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "FinOpsForCloudGetBillingFiles",
            "Effect": "Allow",
            "Action": [
                "s3:GetObject"
            ],
            "Resource": "arn:aws:s3:::<bucket_name>/*"
        },
        {
            "Sid": "FinOpsForCloudManageBillingBucket",
            "Effect": "Allow",
            "Action": [
                "s3:GetBucketLocation",
                "s3:ListBucket",
                "s3:PutBucketPolicy",
                "s3:PutObject"

            ],
            "Resource": "arn:aws:s3:::<bucket_name>"
        }
    ]
}
```
{% endcode %}

### Creating a policy for resource discovery

The resource discovery access policy is required for all accounts.

A suggested name for the policy is `FinOpsForCloudResourceDiscovery`.

{% code lineNumbers="true" %}
```json
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "FinOpsforCloudGetResources",
            "Effect": "Allow",
            "Action": [
                "bcm-data-exports:GetExport",
                "bcm-data-exports:ListExports"
                "cloudwatch:GetMetricStatistics",
                "cur:DescribeReportDefinitions",
                "ec2:Describe",
                "elasticloadbalancing:Describe",
                "iam:GetAccessKeyLastUsed",
                "iam:GetLoginProfile",
                "iam:ListAccessKeys",
                "iam:ListUsers",
                "s3:GetAnalyticsConfiguration",
                "s3:GetBucketAcl",
                "s3:GetBucketLocation",
                "s3:GetBucketPolicy",
                "s3:GetBucketPolicyStatus",
                "s3:GetBucketPublicAccessBlock",
                "s3:GetBucketTagging",
                "s3:GetIntelligentTieringConfiguration",
                "s3:GetLifecycleConfiguration",
                "s3:GetMetricsConfiguration",
                "s3:GetObject",
                "s3:ListAllMyBuckets",
                "s3:ListBucket",
            ],
            "Resource": "*"
        }
    ]
}
```
{% endcode %}

## AWS IAM User <a href="#aws-iam-user" id="aws-iam-user"></a>

### Creating a new IAM user <a href="#create-a-user-for-finops-for-cloud" id="create-a-user-for-finops-for-cloud"></a>

To create a new IAM user for FinOps for Cloud, see [Create an IAM user in your AWS account](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_users_create.html) in the AWS IAM User Guide.

When creating the user, use the following settings:

1. For **User name**, enter `FinOpsForCloudUser`.
2. In **Provide user access to the AWS Management Console**, select **No**.
3. Under **Set permissions**, select **Attach policies directly**.
   1. `FinOpsForCloudResourceDiscovery` (always required)
   2. `FinOpsForCloudBillingImport` (required only for accounts with cost and usage reports buckets)

### Creating an access key for FinOps for Cloud <a href="#create-an-access-key-for-finops-for-cloud" id="create-an-access-key-for-finops-for-cloud"></a>

To create an access key for FinOps for Cloud, see [Create an access key for an IAM user](https://docs.aws.amazon.com/IAM/latest/UserGuide/access-keys-admin-managed.html#admin-create-access-key) in the AWS IAM User Guide.

When creating the access key, choose **Third-party service** as your use case.

{% hint style="warning" %}
Be sure to store your access key and secret access key securely. This is your only chance to view or download the newly created access key, as it cannot be recovered later.
{% endhint %}
