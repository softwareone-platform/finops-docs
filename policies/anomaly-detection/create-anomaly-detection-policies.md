# Create Anomaly Detection Policies

Organization Managers can create new anomaly detection policies by defining the policy name and description, and the parameters under which anomalies will be identified.&#x20;

FinOps for Cloud supports two types of anomaly detection policies, including **Resource count** and **Expense**. To learn about these policy types, see [Anomaly Detection](./).

### Creating a new anomaly detection policy

To create a new anomaly detection policy:

1. Navigate to the **Anomaly detection** page, then select **Add**. The **Create anomaly detection policy** page opens.

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/create_anomaly_detection.png" alt=""><figcaption><p>The Create anomaly detection policy page in FinOps for Cloud.</p></figcaption></figure></div>

2. Enter a descriptive name for the policy and select the policy type:
   * Select **Resource count** if you want the daily resource count to not exceed the average amount over the last evaluation period, according to the threshold percentage.
   * Select **Expense** if you want FinOps for Cloud to detect when everyday expenses exceed the average sum for the last evaluation period above the threshold percentage.
3. Enter the evaluation period in days and define the threshold percentage.
4. (Optional) Select any filters to be used to trigger policy alerts. You can apply multiple filters. If applicable, select **Show more** to view all filter options.
5. Select **Save** to finish creating the new policy.

Once the policy has been created, FinOps for Cloud sends an email notification to the Organization Manager every time an anomaly is detected.
