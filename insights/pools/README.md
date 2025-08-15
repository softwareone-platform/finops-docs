# Pools

The **Pools** page in FinOps for Cloud allows you to view and manage your organization’s resource pools, including their limits, expenses, and forecasts. You can also monitor resource usage, identify potential overspending, and optimize costs by visualizing current expenses and forecast.

All pools and sub-pools are organized in a hierarchical structure to help you navigate and manage them easily. The **Expenses** and **Forecast** columns provide insights into your current expenses and projected costs for each pool and sub-pool.&#x20;

You can also see the pool owner and perform actions, like adding new subpools, viewing the resource list, opening the pool in the cost explorer, and deleting the pool and its subpools.

## About Assignment Rules

Newly created resources are automatically distributed into pools based on assignment rules. If the resources have certain tags, they are immediately assigned to the appropriate pool upon first discovery. Resources that don't belong to any pool are assigned to the data source pool, which is created automatically when the data source is connected.

Assignment rules are evaluated according to priority. You can manually reapply these rules across the entire organization or within a specific pool. Additionally, you can manage assignment rules by editing them or adjusting their priority.&#x20;

To learn more, see the following links:

{% content-ref url="add-assignment-rules.md" %}
[add-assignment-rules.md](add-assignment-rules.md)
{% endcontent-ref %}

{% content-ref url="view-and-manage-assignment-rules.md" %}
[view-and-manage-assignment-rules.md](view-and-manage-assignment-rules.md)
{% endcontent-ref %}

{% content-ref url="re-apply-ruleset.md" %}
[re-apply-ruleset.md](re-apply-ruleset.md)
{% endcontent-ref %}

{% content-ref url="pool-constraint-policies.md" %}
[pool-constraint-policies.md](pool-constraint-policies.md)
{% endcontent-ref %}

{% content-ref url="view-pool-assignment-rules.md" %}
[view-pool-assignment-rules.md](view-pool-assignment-rules.md)
{% endcontent-ref %}

{% content-ref url="delete-a-pool.md" %}
[delete-a-pool.md](delete-a-pool.md)
{% endcontent-ref %}
