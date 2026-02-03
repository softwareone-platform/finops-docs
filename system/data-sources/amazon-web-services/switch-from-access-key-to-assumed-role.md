---
description: >-
  Using an assumed role to connect your AWS account to FinOps for Cloud is the
  recommended approach. Follow this guide to switch your existing AWS accounts
  using an access key to use an assumed role.
---

# Switch from Access Key to Assumed Role

For more information on access keys vs assumed roles read our documentation here: [.](./ "mention").

{% hint style="warning" %}
Switching from an access key to an assumed role is permanent. After you make this change, you can’t switch back to using an access key for this data source.

If you later want to use an access key again, you’ll need to delete the data source and recreate it with access key credentials. This will delete all existing data for this data source and require a full reimport of the resource and billing data.

If you are changing an AWS organizations management account, this will also affect the billing data of any member account data sources linked to that management account.
{% endhint %}

## How to switch from using an access key to an assumed role

{% stepper %}
{% step %}
### Create a new IAM role

If you're currently using access keys, you may not have configured an IAM role with a trust policy. To do this, follow the instructions under **Creating a new IAM role** on this page: [#aws-iam-assumed-role](configure-aws-access.md#aws-iam-assumed-role "mention")
{% endstep %}

{% step %}
### Update your AWS data source in FinOps for Cloud

1. Navigate to **Data sources** in FinOps for Cloud
2. Click on the AWS data source you wish to change to an assumed role.
3. Click on **Update credentials** at the top right of the data source details screen.
4. Under the **Authentication** heading, toggle the authentication type to **Assumed role**.
5. Enter the name of your assumed role in the **Assumed Role Name** field.
6. Click **Save**.
{% endstep %}
{% endstepper %}

## What to expect after the change

Once you have switched from using an access key to an assumed role, the billing import and resource discovery for the account in question will continue uninterrupted.
