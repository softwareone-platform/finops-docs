# Add Data Sources

To start monitoring your cloud resources, you must connect your billing source to FinOps for Cloud. The supported data sources include Amazon Web Services, Google Cloud Platform, and Microsoft Azure.&#x20;

The onboarding process in FinOps requires you to meet certain prerequisites based on the data source you want to connect. These prerequisites can differ depending on the source.

Additionally, you might need to complete certain tasks on the cloud provider's side and some in FinOps for Cloud. For instance, if you are connecting an AWS source, you must create Cost and Usage Reports, configure policies in the AWS console, and then add your AWS account to FinOps.&#x20;

## Adding a data source

{% hint style="info" %}
Before adding a data source, make sure to go through the following links to understand the prerequisites and onboarding steps for supported data sources:&#x20;

* [Amazon Web Services](../../system/data-sources/amazon-web-services/)
* [Microsoft Azure](../../system/data-sources/microsoft-azure.md)
* [Google Cloud Platform](../../system/data-sources/google-cloud-platform.md)

Then, follow the steps in this section to add your data source to FinOps for Cloud.
{% endhint %}

To add a new data source:

1. On the **Data sources** page in FinOps for Cloud, select **Add**.

<figure><img src="../../.gitbook/assets/ffc_data_source (1).png" alt=""><figcaption><p>Data Sources page</p></figcaption></figure>

2. On the **Connect data source** page, do the following:
   1. Select the data source you want to add, for example, **AWS**, **Azure**, or **GCP**.&#x20;
   2. Select the connection type:
      1. **AWS** - Choose if you want to connect a root account or a linked account.
      2. **Azure** - Choose if you want to connect a tenant or a subscription.&#x20;
      3. **GCP** - Choose if you want to connect a tenant or a project. &#x20;
3. Enter the account credentials. The fields and options vary depending on the source you are connecting.
4. Select **Connect**.

When the data source is connected, the details and cloud expenses of the connected cloud account are displayed on the page.&#x20;

To view the resource details, select the resource name. You can then see all the properties and manage the data source, including renaming, updating credentials, and disconnecting.
