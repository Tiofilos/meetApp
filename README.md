# meetApp
Feature 1: 
Filter Events by City
Scenario 1: When user hasn’t searched for a city, show upcoming events from all cities.
Scenario 2: User should see a list of suggestions when they search for a city.
Scenario 3: User can select a city from the suggested list.

As a user
I should be able to “filter events by city”
So that I can see the list of events that take place in that city

Given/When/Then:
Scenario 1: When user hasn’t searched for a city, show upcoming events from all cities.
Given user hasn’t searched for any city
When the user opens the app
Then the user should see a list of all upcoming events

Scenario 2: User should see a list of suggestions when they search for a city.
Given the main page is open
When user starts typing in the city textbox
Then the user should see a list of cities (suggestions) that match what they’ve typed

Scenario 3: User can select a city from the suggested list.
Given the user was typing “Berlin” in the city textbox
And the list of suggested cities is showing
When the user selects a city (e.g., “Berlin, Germany”) from the list
Then their city should be changed to that city (i.e., “Berlin, Germany”)
And the user should receive a list of upcoming events in that city


Feature 2: 
Show/hide an event's details
Scenario 1: An event element is collapsed by default
Scenario 2: User can expand an event to see its details
Scenario 3: User can collapse an event to hide its details

As a user
I should be able to “Show/hide an event's details”
So that I can read details about an event and hide it afterwards

Given/When/Then:
Scenario 1: An event element is collapsed by default
Given the user has'nt clicked on an event details
When the user doesn't click on the event details
Then the event element should remain hidden by default

Scenario 2: User can expand an event to see its details
Given the user clicks on an event element
When the element expands
Then the details of the event element should be displayed

Scenario 3: User can collapse an event to hide its details
Given the the details of an event element is showing  
When the user clicks on the event element again
Then the event element should collapse, hiding event details 

Feature 3: 
Specify number of events
Scenario 1: When user hasn’t specified a number, 32 is the default number
Scenario 2: User can change the number of events they want to see
As a user
I should be able to “specify the number of events”
So that I can change the number of events I want to see from the default number of 32 events

Given/When/Then:
Scenario 1: When user hasn’t specified a number, 32 is the default number
Given the user wants to search for certain numbers of events
When the user does'nt specify the number of events to be searched
Then 32 events should be displayed

Scenario 2: User can change the number of events they want to see
Given user sees a display of default 32 events
When user input the numbers of events the user wants to see
Then the numbers of events user input should be displayed


Feature 4: 
Use the app when offline
Scenario 1: Show cached data when there’s no internet connection
Scenario 2: Show error when user changes the settings (city, time range
As a user
I should be able to “use the app when offline”
So that I can access the cached data when there is no internet connection

Given/When/Then:
Scenario 1: Show cached data when there’s no internet connection
Given a user has no internet connection
When user accesses the app
Then cached data should be accessible

Scenario 2: Show error when user changes the settings (city, time range).
Given  user has no internet connection and has access to the cached data
When user changes the city and time range settings
Then an error message should be displayed


Feature 5: 
Data visualization
Scenario 1: Show a chart with the number of upcoming events in each city
As a user
I should be able to “visualise event data”
So that I can see a chart of the numbers of upcoming events in each city

Given/When/Then:
Scenario 1: Show a chart with the number of upcoming events in each city.
Given a user wants to know upcoming events
When a user clicks on upcoming events button
Then charts showing the numbers of upcoming events should be displayed