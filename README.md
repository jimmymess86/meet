# User Stores

## FEATURE 1: As a user, I would like to be able to filter events by city so that I can see the list of events
that take place in that city.

SCENARIO 1: WHEN USER HASN’T SEARCHED FOR A CITY, SHOW UPCOMING EVENTS FROM ALL CITIES.
Given: user hasn’t searched for any city
When: the user opens the app
Then: the user should see a list of all upcoming events

SCENARIO 2: USER SHOULD SEE A LIST OF SUGGESTIONS WHEN THEY SEARCH FOR A CITY.
Given: the main page is open
When: user starts typing in the city textbox
Then: the user should see a list of cities (suggestions) that match what they’ve typed

SCENARIO 3: USER CAN SELECT A CITY FROM THE SUGGESTED LIST.
Given: the user was typing “Berlin” in the city textbox
And the list of suggested cities is showing
When: the user selects a city (e.g., “Berlin, Germany”) from the list
Then: their city should be changed to that city (i.e., “Berlin, Germany”)
And the user should receive a list of upcoming events in that city

## FEATURE 2: As a user, I should be able to SHOW/HIDE AN EVENT’S DETAILS so that I can see specific details for a single event

Scenario 1: An event element is collapsed by default.
Given: a user is on the main page
When: nothing is clicked
Then: the event details will collapse

Scenario 2: User can expand an event to see its details.
Given: a user wants details of a single event
When: a user clicks the event
Then: the details of the event are opened

Scenario 3: User can collapse an event to hide its details.
Given: a user is finished reading event details
When: a user clicks the close button
Then: the event page is collapsed

## FEATURE 3: As a user I should be able to SPECIFY NUMBER OF EVENTS so that I can decide how many events to view at a single time
Scenario 1: When user hasn’t specified a number, 32 is the default number.
Given: User has not chosen a specific number of events to view
When: the user opens the page
Then: 32 events will be shown by default

Scenario 2: User can change the number of events they want to see.
Given: When a user wishes to see a specific number of events.
When: user clicks the menu
Then: the user will see the amount of events they prefer.

## FEATURE 4: As a user I should be able to USE THE APP WHEN OFFLINE so that I can access the information without an internet connection.
Scenario 1: Show cached data when there’s no internet connection.
Given: When a user has no internet connection
When: the user opens the app and has stored cached data
Then: the user will have access to the app's previous data

Scenario 2: Show error when user changes the settings (city, time range).
Given: The user is offline
When: the user tries to change information
Then: an error will be shown

## FEATURE 5: As a user I should be able to access DATA VISUALIZATION via charts, so I can quickly access events of interest
Scenario 1: Show a chart with the number of upcoming events in each city.
Given: user is on main the main page
When: When user wants to see upcoming events
Then: user will have access to chart data of all upcoming events in all cities.