# JSOC Frontend Interview

You are working on the latest and greatest JSOC application, Transparency. Transparency collects information on recent malicious attacks on our systems. You have been hired to implement a number of new features for the application

## Feature Requests:

#### Feature 1

For each attack type, show the remaining metrics that are not shown in the list item already (this would be attack_type and threat_actor).

#### Feature 2

We wish to add a feature which sorts the Transparency dataset based on the attacks priority - either as low, medium, or high. The priority is assigned to an attack based on the following table:

| Category                            | Low   | Medium | High  |
| :---------------------------------- | :---- | :----- | :---- |
| country_code)                       | CA    | US     | Other |
| Asset Impact (asset_impact)         | Low   | Medium | High  |
| Clients Affected (clients_affected) | False | True   | True  |

Show the attack priority (Low, Medium, High) for each Attack list item. This can be added as a row much like how the other metrics are shown in the list item.

Notes:

- If an attack matches with more than one priority, the priority assigned to the attack should be the highest of all the priorities it matches. For example, if an attack has metrics matching low and high priorities, it should be assigned high.

#### Feature 3

We wish to add some basic filtering to the attack list.

- We want to have row of selectable buttons for each of the priorities. Each button should be a different color, and be displayed in a way a user can understand the feature.
- When a user clicks one of the filter buttons, Transparency should update the list of attacks being shown to only those that have the priority assigned to the button.
- There should also be a clear button that removes any filtering and shows the entire attack list again.

#### Follow Up Questions

1. How could you make improvements to the UI/UX to handle potentially 100s of attacks?
2. What can you do to your code to make it more maintanable and readable to other developers?
3. Explain how you would design the application if the datasource was an API endpoint instead of a JSON file?
