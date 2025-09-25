# Data Sources

<details>

<summary>How do I add a data source?</summary>

Data sources can be added using the **Add** option on the Data Sources page. For more details, see [Add Data Sources](../../finops-for-cloud/getting-started/data-sources.md).

</details>

<details>

<summary>Are there any prerequisites to adding a data source?</summary>

Yes, adding a data source involves certain prerequisites depending on the type of source you want to add (Azure, AWS, or GCP). For specific details, see the following links:

* [Amazon Web Services](../../system/data-sources/amazon-web-services/)
* [Microsoft Azure](../../system/data-sources/microsoft-azure.md)
* [Google Cloud Platform](../../system/data-sources/google-cloud-platform.md)

</details>

<details>

<summary>What's the difference between terminating a FinOps for Cloud subscription vs disconnecting a data source?</summary>

If you choose to cancel your FinOps for Cloud subscription, you will no longer be able to sign in to FinOps for Cloud, and all of your data will be permanently deleted. For more details, see [Cancel Your FinOps Order](https://docs.platform.softwareone.com/extensions/finops-for-cloud/cancel-your-finops-order).&#x20;

Alternatively, if you remove a data source, only that specific data source will be affected. You’ll still have access to FinOps for Cloud and your other data sources. For removed data sources, you will be charged until the date of removal.

{% hint style="warning" %}
Removing a data source permanently deletes all historical data associated with it.
{% endhint %}

</details>

<details>

<summary>I have an Essentials agreement for Azure. Can I still add an AWS or GCP data source to FinOps for Cloud?</summary>

Yes, if you have an Essentials agreement for Azure, you can add your additional data sources, including AWS and GCP, to FinOps for Cloud.&#x20;

If your AWS account is covered under an AWS Essentials agreement, FinOps for Cloud is already included, so there’s no additional cost.&#x20;

For any other accounts not covered by an Essentials agreement, a standard 4% consumption fee might apply.

</details>

<details>

<summary>How do I onboard multiple subscriptions at once into FinOps for Cloud?</summary>

You can proceed with the tenant-level integration via data sources. However, you will still need to perform role assignment and grant the **Reader** role to each subscription.

To learn more, see [Microsoft Azure](../../system/data-sources/microsoft-azure.md).

</details>

<details>

<summary>How does the Billing Reimport option work? </summary>

The **Billing Reimport** option is available on the details page of a data source.

This feature allows you to manually reimport your billing data starting from a specific date into FinOps for Cloud. You can manually reimport data if:

* Your billing data has not been imported as expected.
* You have made configuration or permission-related changes that require reimporting data to reflect those updates.
* You need historical billing data from months that were not previously imported.

For details on how to perform a billing reimport, see [Reimport Billing](../../system/data-sources/manage-data-sources/reimport-billing.md).

</details>

<details>

<summary>How do I disconnect a data source?</summary>

The **Disconnect** option on the details page of a data source lets you disconnect and remove a data source from FinOps for Cloud.

To learn more, see [Disconnect Data Source](../../system/data-sources/manage-data-sources/disconnect-data-source.md).

</details>
