---
description: >-
  Configuring access to your Azure subscriptions for FinOps for Cloud requires
  the creation of an App Registration and assigning the Reader role in each
  subscription.
---

# Configure Azure Access

## Configure Azure for FinOps for Cloud

FinOps for Cloud requires an app registration to connect to your Azure subscriptions.

As you create your app registration, make a note of the following:

* Application (client) ID
* Directory (tenant) ID
* Client secret

Additionally, if you plan to add individual Azure subscriptions rather than the tenant itself, make a note of each Subscription ID to be added.

### Create the app registration

More information about creating app registrations can be found here: [https://learn.microsoft.com/en-us/entra/identity-platform/quickstart-register-app](https://learn.microsoft.com/en-us/entra/identity-platform/quickstart-register-app)

To create the app registration, follow these steps:

1. Sign in to the Azure Portal with a user that has enough permissions to create an app registration.
2. Browse to **Entra ID** > **App registrations** and select **New registration**.
3. Provide a name for the application. We recommend `FinOpsForCloud` .
4. Under **Supported account types**, select **Accounts in this organizational directory only**.
5. Select **Register** to complete the app registration.

On the app registration **Overview** page, make a note of:

1. The **Application (client) ID**.
2. The **Directory (tenant) ID**.

### Create a client secret

More information about creating a client secret can be found here: [https://learn.microsoft.com/en-us/entra/identity-platform/how-to-add-credentials?tabs=client-secret](https://learn.microsoft.com/en-us/entra/identity-platform/how-to-add-credentials?tabs=client-secret)

1. On the `FinOpsForCloud` app registration **Overview** page, expand the **Manage** menu on the left and click **Certificates & secrets**.
2. Select **New client secret** and add a description for your secret.
3. Select an expiration for the secret. SoftwareOne recommends setting an expiration value of less than 12 months.
4. Select **Add**.

Make a note of the client secret **Value** for use in FinOps for Cloud. This secret value is _never displayed again_ after you leave this page.

### Find your subscription IDs

If you intend to add individual Azure subscriptions to FinOps for Cloud rather than a tenant, follow these steps to make a note of your subscription IDs.

1. In the top search field of the Azure Portal, search for **Subscriptions**.
2. For each subscription you wish to add to FinOps for Cloud, make a note of the ID in the **Subscription ID** column.

### Assign the Reader Role

When adding either individual Azure subscriptions or an Azure tenant to FinOps for Cloud, the Reader role in each subscription must be assigned to the app registration.

{% hint style="warning" %}
You must have **Owner** or **User Access Administrator** permissions on the subscription to assign roles.
{% endhint %}

1. In the top search field of the Azure Portal, search for **Subscriptions**.
2. For each subscription you wish to add to FinOps for Cloud, add the **Reader** role as follows:
   1. Select the specific subscription, then click on **Access control (IAM)** in the left menu.
   2. Click **+ Add** and select **Add role assignment**.
   3. On the **Role** tab, search for and select the **Reader** role.
   4. On the **Members** tab, set "Assign access to" to **User, group, or service principal**.
   5. Click **+ Select members**, search for `FinOpsForCloud`, and select it.
   6. Click **Review + assign** to finalize.

### Next steps

When you have completed these steps, you are ready to [add-your-azure-subscriptions-to-finops-for-cloud.md](add-your-azure-subscriptions-to-finops-for-cloud.md "mention").
