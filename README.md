## Feature Requests:

#### Feature 1

For each attack item, show the remaining metrics that are not shown in the item already (this would be attack_type and threat_actor).

#### Feature 2

We wish to add a new metric, priority. This metric will have a value of low, medium, or high. The priority is assigned to an attack based on the following table of ratings:

| Rating                              | Low   | Medium | High                    |
| :---------------------------------- | :---- | :----- | :---------------------- |
| Country Code (country_code)         | CA    | US     | Other (BR, RU, AU, etc) |
| Asset Impact (asset_impact)         | low   | medium | high                    |
| Clients Affected (clients_affected) | False | False  | True                    |

Each of the above metrics has a rating associated with it (low, medium, high). For example, country_code can have the ratings of Low (when it is equal to CA), Medium (=US), or high (when it is any other country code).

Show the attack priority (Low, Medium, High) for each attack item in the list. The attack priority should be given the same value as the highest rating from each of the above metrics. This can be added as a row much like how the other metrics are shown in the list item.

Hint: Pay attention to the metric clients_affected. It has the same value for medium and low. Think about how the final priority is assigned if another metric has a medium rating, but clients_affected is False.

Example:

An attack has the following metrics:
{
"country_code": "CA",
"asset_impact": "low",
"clients_affected": True
}
-> Priority: High

{
"country_code": "US",
"asset_impact: "medium",
"clients_affected: False
}
-> Priority: Medium

{
"country_code": "CA",
"asset_impact: "low",
"clients_affected: False
}
-> Priority: Low

#### Feature 3

We wish to add some basic filtering to the attack list.

- We want to have row of selectable buttons for each of the priorities. Each button should be a different color, and be displayed in a way a user can understand the feature.
- When a user clicks one of the filter buttons, Transparency should update the list of attacks being shown to only those that have the priority assigned to the button.
- There should also be a clear button that removes any filtering and shows the entire attack list again.

#### Follow Up Questions

1. How could you make improvements to the UI/UX to handle potentially 100s of attacks?
2. What can you do to your code to make it more maintanable and readable to other developers?
3. Explain how you would design the application if the datasource was an API endpoint instead of a JSON file?
