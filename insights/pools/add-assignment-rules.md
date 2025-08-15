# Configure Assignment Rules

There are two ways to configure assignment rules in FinOps for Cloud. You can add them from the **Pools** or **Resources** pages.

When a new rule is added, it's always prioritized across the organization. It means that any discovered resources are first checked against the conditions of this new rule. If the resource doesn't meet the new rule's conditions, it's checked against the remaining rules in descending order until a matching rule is found.

## Configuring a new assignment rule

To configure a new assignment rule:

1. Navigate to the **Add automatic Resource Assignment Rule** page using one of the following steps:
   * Open the **Pools** page and select **Configure assignment rules**. Next, on the **Assignment rules** page, select **Add**.
   * Open the **Resources** page and select a resource. On the resource's details page, select **Add assignment rule**.
2. Under **Name**, enter a name for the rule.
3. Under **Conditions**, select all conditions that must be fulfilled for the rule to become applicable. The following conditions are available:

<table><thead><tr><th width="204">Type</th><th width="185">Key/Value</th><th>Description</th></tr></thead><tbody><tr><td>Name/ID starts with</td><td>string value</td><td>Matches resources where the name or ID begins with the specified value.</td></tr><tr><td>Name/ID ends with</td><td>string value</td><td>Matches resources where the name or ID ends with the specified value.</td></tr><tr><td>Name/ID is</td><td>string value</td><td>Matches resources with an exact name or ID match.</td></tr><tr><td>Name/ID contains</td><td>string value</td><td>Matches resources where the name or ID contains the specified substring.</td></tr><tr><td>Tag is</td><td>key-value pair</td><td>Matches resources with a tag that matches both the specified key and value.</td></tr><tr><td>Tag exists</td><td>key-value pair</td><td>Matches resources that have a tag with the specified key.</td></tr><tr><td>Tag value starts with</td><td>key-value pair</td><td>Matches resources with a tag value starting with the specified value for the given key.</td></tr><tr><td>Source is</td><td>selected row</td><td>Matches resources from a selected data source. Options are presented in a dropdown for selecting the source.</td></tr><tr><td>Resource type is</td><td>string value</td><td>Matches resources where the resource type contains the specified value.</td></tr><tr><td>Region is</td><td>string value</td><td>Matches resources where the region contains the specified value.</td></tr></tbody></table>

4. Add additional conditions as required.
5. Under **Assign to**, review the **Target pool** and **Owner**. By default, the matching resource is included in the selected target pool and assigned to an owner. You can change the values as relevant.
6. Select **Create** to finalize the rule.
