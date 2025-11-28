# Recommendations

The **Recommendations** page is designed to make you aware of the less apparent deficiencies of the infrastructure, like configuration flaws and security risks.&#x20;

To receive recommendations, it's essential to [add a data source](../../finops-for-cloud/getting-started/data-sources.md) to FinOps for Cloud. When a data source is added, FinOps for Cloud analyzes it to provide recommendations to help you optimize costs and improve resource security, performance, and availability.&#x20;

Currently, FinOps for Cloud performs a check every 3 hours.

<figure><img src="../../.gitbook/assets/recommendations.png" alt=""><figcaption><p>Recommendations in FinOps for Cloud.</p></figcaption></figure>

The **Recommendations** page displays a summary of each recommendation [across different categories](https://docs.finops.softwareone.com/insights/recommendations/recommendation-categories) and suggests actions to help you make informed decisions. The summary varies, depending on the condition. For instance, it might show AWS S3 duplicates found during the last check, checks that did not start or finish successfully, and so on.

Recommendations also contain one of the following symbols:

* A red symbol <img src="../../.gitbook/assets/ffc_icon_green.png" alt="" data-size="line"> indicates a critical situation, indicating that you must focus on the card and its information.
* A green symbol <img src="../../.gitbook/assets/ffc_icon.png" alt="" data-size="line"> indicates that there are no recommendations or your potential savings are zero.
* An orange symbol <img src="../../.gitbook/assets/icon_warning (1).png" alt="" data-size="line"> appears when certain items require attention, for instance, if there are inactive IAM users in your organization.

## Additional actions

On the **Recommendations** page, you can do the following:

* See your **possible monthly savings** that can be achieved if the recommended suggestions are implemented.
* See the **last check time**. This is the time when FinOps for Cloud last checked for an update.
* See the **next check time**. This is the time when the next recommendation check is due.
* Filter recommendations based on data source, category (**Savings**, **Security**, **Critical**, and **Non-empty**), and applicable services.&#x20;
* Customize the parameters for a recommendation, exclude pools, and pin or unpin recommendations. For more information, see [Customize Recommendations](customize-recommendations.md).
* Use the **Force check** option to run the data sources' evaluation sequence and initialize a force check. Only [Organization Managers](../../system/user-management/) can initialize a force check.
