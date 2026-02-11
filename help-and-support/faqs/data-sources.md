# Data Sources

<details>

<summary>How do I add a data source?</summary>

Data sources can be added using the **Add** option on the Data Sources page. For more details, see [Add Data Sources](../../finops-for-cloud/getting-started/data-sources.md).

</details>

<details>

<summary>Are there any prerequisites to adding a data source?</summary>

Yes, adding a data source involves certain prerequisites depending on the type of source you want to add (Azure, AWS, or GCP). For specific details, see the following links:

* [Amazon Web Services](../../system/data-sources/amazon-web-services/)
* [Microsoft Azure](../../system/data-sources/microsoft-azure/)
* [Google Cloud Platform](../../system/data-sources/google-cloud-platform.md)

</details>

<details>

<summary>I have connected my data source, but I can't view any cost or usage data.</summary>

This can occur due to a mismatch between the currency you selected when ordering the FinOps for Cloud subscription from the Marketplace and the currency used by your cloud provider for billing.

To avoid discrepancies, your organization currency must match the currency of the data source. Selecting a different currency may prevent the data source from being added or could result in no cost and usage data being displayed.

To resolve this issue, you must cancel your current agreement and create a new one with the correct currency. For more details, see the following links in the SoftwareOne Marketplace Platform documentation:

* [Order FinOps for Cloud from Marketplace](https://docs.platform.softwareone.com/extensions/finops-for-cloud/order-finops-for-cloud-from-marketplace)
* [Cancel Your FinOps for Cloud Order](https://docs.platform.softwareone.com/extensions/finops-for-cloud/cancel-your-finops-order)

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

To learn more, see [Microsoft Azure](../../system/data-sources/microsoft-azure/).

</details>

<details>

<summary>How does the Billing Reimport option work? </summary>

The **Billing Reimport** option is available on the details page of a data source.

Using this option, you can manually reimport your billing data starting from a specific date. Data can be reimported only if:

* Your billing data has not been imported previously as expected.
* You have made configuration or permission-related changes that require reimporting data to reflect those updates.
* You need historical billing data from months not previously imported.

For details on how to perform a billing reimport, see [Reimport Billing](../../system/data-sources/manage-data-sources/reimport-billing.md).

</details>

<details>

<summary>How do I disconnect a data source?</summary>

To remove a data source, use the **Disconnect** option on the details page of a data source you want to remove. To learn more, see [Disconnect Data Source](../../system/data-sources/manage-data-sources/disconnect-data-source.md).

</details>

