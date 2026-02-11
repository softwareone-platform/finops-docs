---
description: >-
  Learn how you can add your Azure data sources to the FinOps for Cloud
  platform. FinOps for Cloud supports both Azure tenants and individual Azure
  subscriptions.
---

# Microsoft Azure

## Configuring your Azure data sources

### Add an Azure tenant

Adding an Azure tenant requires the creation of an app registration and the assignment of the Reader role to each Azure subscription.

To do this, follow these steps:

{% stepper %}
{% step %}
**Configure Azure Access**

1. Create the app registration
2. Create a client secret
3. Assign the Reader role
{% endstep %}

{% step %}
**Add your tenant to FinOps for Cloud**

1. Add your Azure tenant to FinOps for Cloud
2. \[Optional] Reimport historical billing data
{% endstep %}
{% endstepper %}

### Add individual Azure subscriptions

Adding individual Azure subscriptions requires the creation of an app registration and the assignment of the Reader role to each Azure subscription.

To do this, follow these steps:

{% stepper %}
{% step %}
**Configure Azure Access**

1. Create the app registration
2. Create a client secret
3. Find your Azure subscription IDs
4. Assign the Reader role
{% endstep %}

{% step %}
**Add your tenant to FinOps for Cloud**

1. Add your Azure subscriptions to FinOps for Cloud
2. \[Optional] Reimport historical billing data
{% endstep %}
{% endstepper %}

## Important

{% hint style="warning" %}
Adding the same Azure subscription by adding it under a tenant and also adding it individually will cause problems when importing billing data.
{% endhint %}
