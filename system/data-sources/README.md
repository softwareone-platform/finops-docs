# Data Sources

The **Data sources** page lets you add a new billing data source to your FinOps for Cloud account. The supported data sources include Amazon Web Services, Google Cloud Platform, and Microsoft Azure.

To add a new data source to your FinOps account:

1. Navigate to the **Data sources** page. Then, select **Add**.

<figure><img src="../../.gitbook/assets/ffc_data_source (1).png" alt=""><figcaption><p>Data Sources page</p></figcaption></figure>

2. On the **Connect data source** page, do the following:
   1. Select the data source you want to connect to FinOps, for example, **AWS**, **Azure**, or **GCP**.&#x20;
   2. Select the connection type:
      1. **AWS** - Choose if you want to connect a root account or a linked account. See [Amazon Web Services](amazon-web-services/) for details.
      2. **Azure** - Choose if you want to connect a tenant or a subscription. See [Microsoft Azure](microsoft-azure.md) for details.
      3. **GCP** - Choose if you want to connect a tenant or a project.  See [Google Cloud Platform](google-cloud-platform.md) for details.
3. Enter the account credentials. The fields and options vary depending on the source you are connecting.
4. Select **Connect**.

When the data source is connected, the details and cloud expenses of the connected cloud account are displayed on the page.&#x20;

To view the resource details, select the resource name. You can then see all the properties and manage the data source, including renaming, updating credentials, and disconnecting.
