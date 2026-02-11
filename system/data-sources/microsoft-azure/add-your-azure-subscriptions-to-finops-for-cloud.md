---
description: >-
  The final step in configuring your Azure subscriptions for FinOps for Cloud is
  to add the Azure data source(s).
---

# Add your Azure subscriptions to FinOps for Cloud

## Adding an individual Azure subscription to FinOps for Cloud

To add individual Azure subscriptions to FinOps for Cloud, follow these steps:

1. In FinOps for Cloud, navigate to **System** > **Data sources**.
2. Click **+ Add** and select **Azure**.
3. Under **Connection type**, select **Subscription**.
4. Enter the details record in the [configure-azure-access.md](configure-azure-access.md "mention") steps.
5. Repeat this process for each Azure subscription to be added.

## Adding an Azure tenant to FinOps for Cloud

To add an Azure tenant to FinOps for Cloud, follow these steps:

1. In FinOps for Cloud, navigate to **System** > **Data sources**.
2. Click **+ Add** and select **Azure**.
3. Under **Connection type**, select **Tenant**.
4. Enter the details record in the [configure-azure-access.md](configure-azure-access.md "mention") steps.
5. This step only needs to be performed once. FinOps for Cloud will automatically discover all configured Azure subscriptions in the tenant.

## Next steps

FinOps for Cloud will import billing data for the current and previous month. Microsoft stores up to 13 months of billing data. If you wish to import more historical data, follow the steps under [import-historical-data.md](import-historical-data.md "mention").
