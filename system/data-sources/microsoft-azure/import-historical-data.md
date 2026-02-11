---
description: >-
  Microsoft stores up to 13 months of billing data. Follow these steps to import
  it.
---

# Import Historical Data

## Performing a billing reimport in FinOps

To perform a billing reimport in FinOps for Cloud:

1. Navigate to the **Data sources** page.
2. Select the Azure data source, then select **Billing reimport**.
3. In **Import from**, choose the start date of your historical billing data.
4. Select **Schedule import**.

Once the import process has been initiated, it might take several hours for the process to complete, depending on the amount of historical data.

{% hint style="info" %}
A billing reimport can only be started on individual Azure subscriptions. This functionality is not available to the parent tenant.
{% endhint %}
