# Migrate from Legacy CUR to CUR 2.0

If you connected an AWS data source using the Legacy CUR export schema and want to migrate to CUR 2.0, you will need to create a new CUR 2.0 report and then update the AWS data source within FinOps for Cloud.&#x20;

{% hint style="info" %}
You can create a new S3 bucket for the CUR 2.0 report or use your existing legacy CUR S3 bucket.

If you use your existing S3 bucket, you must specify a report prefix that is different from the one used for the legacy CUR report.
{% endhint %}

## Migrating from Legacy CUR to CUR 2.0

{% stepper %}
{% step %}
**Create a new CUR 2.0 report**

In the AWS Console, create an export of CUR 2.0 with its new schema.

See [Creating reports](https://docs.aws.amazon.com/cur/latest/userguide/cur-create.html) in the AWS Data Exports User Guide for the necessary steps.&#x20;

When creating the report, use the recommended settings in [Create Cost and Usage Reports](create-cost-and-usage-reports.md).&#x20;
{% endstep %}

{% step %}
**Update your existing data source in FinOps for Cloud**

When the report is ready, use the following steps to update your existing AWS data source in FinOps for Cloud:

1. Select the existing AWS data source on the **Data sources** page in FinOps for Cloud. The page with detailed information opens.
2. Select **Update credentials** to update the data source's credentials.
3. In **Update AWS cloud credentials**, do the following:
   1. Enable **Update data export parameters** to update the billing bucket information.
   2. Select **Standard data export (CUR 2.0)**
      1. If you used the same S3 bucket as your legacy CUR reports, update the **Export name** and **Export path prefix**.
      2. If you created a new S3 bucket for your CUR 2.0 reports, update the **Export name**, **S3 bucket name**, and **Export path prefix**.
   3. Select **Save** and wait for a new export to import.

<div data-with-frame="true"><figure><img src="../../../.gitbook/assets/image (1) (1).png" alt=""><figcaption><p>Migrate to CUR 2.0 and update the credentials.</p></figcaption></figure></div>
{% endstep %}
{% endstepper %}
