# Microsoft Azure

FinOps for Cloud supports both Azure tenants and individual Azure subscriptions. This topic describes how you can add your Azure data sources to the FinOps for Cloud platform.&#x20;

### Prerequisites&#x20;

Before connecting Microsoft Azure to FinOps for Cloud, ensure:

* Azure subscriptions are active.
* Required permissions are assigned. See [Configure Azure Access](configure-azure-access.md) for the Azure roles and permissions required to connect Azure to FinOps for Cloud.
* Azure Cost Management is enabled and accessible for the subscriptions being onboarded.

FinOps for Cloud retrieves Azure cost and usage information through Azure Cost Management.&#x20;

If Azure Cost Management data is unavailable or access is restricted, cost and consumption data cannot be imported into the platform.

### Add an Azure tenant

Adding an Azure tenant requires creating an app registration and assigning the Reader role to each Azure subscription.

To add an Azure tenant:

{% stepper %}
{% step %}
**Configure Azure Access**

1. [Create the app registration](configure-azure-access.md#create-the-app-registration)
2. [Create a client secret](configure-azure-access.md#create-a-client-secret)
3. [Assign the Reader role](configure-azure-access.md#assign-the-reader-role)
{% endstep %}

{% step %}
**Add your tenant to FinOps for Cloud**

1. [Add your Azure tenant to FinOps for Cloud](add-your-azure-subscriptions-to-finops-for-cloud.md)
2. [\[Optional\] Reimport historical billing data](import-historical-data.md)
{% endstep %}
{% endstepper %}

### Add individual Azure subscriptions

Adding individual Azure subscriptions requires creating an app registration and assigning the Reader role to each Azure subscription.

To add individual Azure subscriptions:

{% stepper %}
{% step %}
**Configure Azure access**

1. [Create the app registration](configure-azure-access.md#create-the-app-registration)
2. [Create a client secret](configure-azure-access.md#create-a-client-secret)
3. [Find your Azure subscription IDs](configure-azure-access.md#find-your-subscription-ids)
4. [Assign the Reader role](configure-azure-access.md#assign-the-reader-role)
{% endstep %}

{% step %}
**Add your tenant to FinOps for Cloud**

1. [Add your Azure subscriptions to FinOps for Cloud](add-your-azure-subscriptions-to-finops-for-cloud.md)
2. [\[Optional\] Reimport historical billing data](import-historical-data.md)
{% endstep %}
{% endstepper %}

{% hint style="warning" %}
Adding the same Azure subscription under a tenant and individually can cause problems when importing billing data.
{% endhint %}
