# JSOC Frontend Interview

You are working on the latest and greatest JSOC application, Transparency. Transparency collects information on recent malicious attacks on our systems. You have been hired to implement a feature which sorts the Transparency dataset based on the attacks priority - either as low, medium, or high.

This feature will query the attacks database (simplified as a JSON file) based on the following criteria and dynamically update the list of attacks in the UI.

| Category                            | Low                                   | Medium                          | High                                   |
| :---------------------------------- | :------------------------------------ | :------------------------------ | :------------------------------------- |
| Attack Type (attack_type)           | collection, discovery, reconnoissance | defense_evasion, initial_access | credential_access, command_and_control |
| country_code)                       | CA                                    | US                              | Other                                  |
| Asset Impact (asset_impact)         | Low                                   | Medium                          | High                                   |
| Clients Affected (clients_affected) | False                                 | True                            | True                                   |

#### The ask is the following:

1. Show the attack priority (Low, Medium, High) for each Attack list item. This can be added as a row much like how the other metrics are shown in the list item.
2. Update the Transparency UI by adding a row of selectable buttons for each of the priorities. Each button should be a different color, and be displayed in a way a user can understand the feature.
3. When a user clicks a button, Transparency should update the list of attacks being shown to only those that have the priority.
4. Add a clear button to remove a users current query and show the original attack list again.

Notes:

- Attacks can match more than one priority. If an attack has multiple priorities, they should show up for all the appropriate priorities.
- The general design is up to you, it does not need to be super fancy but should be intuitively understood by our users.
