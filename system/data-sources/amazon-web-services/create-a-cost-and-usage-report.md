# Create a Cost and Usage Report

You can create a new Cost and Usage Report (CUR) from the AWS console. For details, see [Creating reports](https://docs.aws.amazon.com/cur/latest/userguide/cur-create.html) in the AWS Data Exports User Guide.

When creating the report, use the following settings:

1. Under **Export details**, choose **Standard data export**.
2. For **Export name**, enter _billing-{your aws account number}_. Replace _{your aws account number}_ with a valid AWS account ID.
3. Under **Data table content settings**, select **CUR 2.0**.
4. For **Additional export content**, select **Include resource IDs**. Leave the **Split cost allocation data** checkbox clear.
5. For **Time granularity**, choose **Hourly**.
6. Under **Data export delivery options**, do the following:
   1. For **Compression type and file format**, select **Parquet - Parquet**.
   2. For **File versioning**, select **Overwrite existing data export file**.
7. Under **Data export storage settings**, enter the **S3 bucket name** as _billing-export-{your aws account number}_. Replace _{your aws account number}_ with a valid AWS account ID.
8. For **S3 path prefix**, enter _reports_ as your prefix.

The following image displays the recommended CUR settings:

<figure><img src="../../../.gitbook/assets/image.png" alt=""><figcaption><p>Cost and Usage Report settings</p></figcaption></figure>
