# JSOC Frontend Interview

You are working on the latest and greatest JSOC application, Transparency. Transparency collects information on recent malicious attacks on our systems. You have been hired to implement a feature which sorts the Transparency dataset based on the attacks priority - either as low, medium, or high.

This feature will query the attacks database (simplified as a JSON file) based on the following criteria and dynamically update the list of attacks in the UI.

The criteria for assigning an attack as low medium or high is as follows:

| Category | Low | Medium | High |
| -------- | --- | ------ | ---- |
| attack_type | Reconnoissance, Discovery or Collection (collection, discovery, reconnoissance) 

Attack Type (attack_type)

Reconnoissance, Discovery or Collection (collection, discovery, reconnoissance) 

Defense Evasion, Initial Access (defense_evasion, initial_access)

Credential Access, Command and Control (credential_access, command_and_control)

Country Code (country_code)

CA

US

Any other code.

Threat Actor (threat_actor)

tomato, hamburger, soup

lollypop, celery, steak

hotdog, pizza

Asset Impact (asset_impact)

Low

Medium

High

Clients Affected (clients_affected)

False

True

True

The attack data will be provided for you via a JSON file. The ask is the following:

Update the Transparency UI by adding a row of selectable buttons for each of the priorities. Each button should be a different colour, and be displayed in a way a user can understand the feature.
When a user clicks a button, Transparency should update the list of attacks being shown to only those that have the priority.
Notes:

If an attack matches more than one category - they should be shown in all of them.
Part 2

The user base loves the new priority feature, congratulations! However, we are getting feedback that there needs to be an easier way to look for attacks. The next feature we are planning is to add some basic search functionality which allows a user to search for a job via the impact level, or the threat actor.

The ask is the following:

Add a search components to the UI above the attack list. The component should be a text box with the following restrictions:
The user can enter any alphanumeric character.
Add a dropdown with the priorities Low, Medium and High. The user may only select one at a time.
Add a fourth search button that will process the search request.
