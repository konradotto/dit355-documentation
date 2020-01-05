# User stories: 

## US1. 
* As a city planner I want to get the request locations so that I know where to plan new busstops.
### Acceptance Criteria: 
1. Location should follow geographical-coordinate format.
1. Data should be in readable.
1. Data should be parsable.

## US2. 
* As a city planner I want to recieve destination plans so that I can plan routes for västtrafik.
### Acceptance Criteria:
4. Location should follow the geographical - coordinate format
5. Data should be in readable.
6. Data should be parsable.

## US3. 
* As Västtrafik I want to receive request information so that we can detect blind spots.
### Acceptance Criteria:
7. Blindspots are identified by requests in areas.
8. Blindspots are shown through dots.
9. Blindspots are clearly identified on the map.


## US4.
* As a city planner, I want to receive time details so that I can map time of the trips.
### Acceptance Criteria: 
10. Time data should be in local time.
11. Time data should include a date.
12. Time should be within reasonable range. 

## US 5.
* As Västtrafik I want to see a graphical representation so that we can analyze the travel patterns.
### Acceptance Criteria: 
13. The representation should be easy to understand.
14. Traveler behaviour should be easy to see.
15. Geographical representation should display locations through markers on the map.

## US 6.
* As Västtrafik I want to filter out the data received so that I can analyze a specific type of data.
### Acceptance Criteria: 
16. The data will be isolated from the JSON.
17. The data will be provided in the right format.
18. The data is readable.

## US 7.
* As a city planner, I want to be able to interact with the map so that I can focus on interesting places.
### Acceptance Criteria: 
19. The map should be zoomable.
20. The map should be able to move vertically.
21. The map should be able to move horizontally.
22. The map should be able to work with touch.

## US 8.
* As västtrafik, I want to be able to use the map in interactive mode so that I can analyze specific locations behaviors.
### Acceptance Criteria:
23. The map should show dots where requests are sent from.
24. The request points should contain information.
25. The map should be visually pleasing.

## US 9.
* As västtrafik I want the system to still be working even if one component malfunctions so that we dont have to reboot it every time it bugs.
### Acceptance Criteria:
26. The points on map shall remain when internet dies
27. the map should still be working if there is no net
28. the app should not erase every data if it crashes
 
## US 10.
* As a cityplanner I want the system to cluster requests so that I can see where most requests are sent in a overview.
### Acceptance Criteria:
29. The points on map shall be clustered
30. the clustering should group accurately

