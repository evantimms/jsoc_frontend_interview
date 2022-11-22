# JSOC Frontend Interview

You are working on the latest and greatest JSOC application, Transparency. Transparency collects information on recent malicious attacks on our systems. You have been hired to implement a feature which sorts the Transparency dataset based on the attacks priority - either as low, medium, or high.

This feature will query the attacks database (simplified as a JSON file) based on the following criteria and dynamically update the list of attacks in the UI.

See `priorities.png` for a breakdown.

## Part 1

#### The ask is the following:

1. Update the Transparency UI by adding a row of selectable buttons for each of the priorities. Each button should be a different color, and be displayed in a way a user can understand the feature.
2. When a user clicks a button, Transparency should update the list of attacks being shown to only those that have the priority.
3. Add a clear button to remove a users current query and show the original attack list again.

Notes:

- Attacks can match more than one priority. If an attack has multiple priorities, they should show up for all the appropriate priorities.
- The general design is up to you, it does not need to be super fancy but should be intuitively understood by our users.

## Part 2

The user base loves the new priority feature, congratulations! However, we are getting feedback that there needs to be an easier way to look for attacks. The next feature we are planning is to add some basic search functionality which allows a user to search for a job via the impact level, or the threat actor.

#### The ask is the following:

1. Add a search components to the UI above the attack list. The component should be a text box where the user can only enter alphanumeric characeters.
2. Add a dropdown with the selections Low, Medium and High. The user may only select one at a time. When a user selects an item, it should show the attacks that correspond to an asset impact of low, medium, or high.

Notes:

- We can repurpose our clear button from part one to clear the search filters in part two.
- A user can use the filters from part one in combination with the filters in part two.
