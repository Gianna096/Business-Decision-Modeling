# Business-Decision-Modeling

**Introduction and Data Prep**

Imagine that we are in charge of vaccine distribution in 20 towns for the State of Connecticut. We have a distribution center set up at the Connecticut State Capitol (41.76428988852701, -72.68249918399205) and We will deliver the COVID vaccines to CVS stores in the shortest amount of distance (so that none of the vaccines will spoil).

Here are the CVS locations in CT - https://www.cvs.com/store-locator/cvs-pharmacy-locations/Connecticut 

Go tabulate the CVS addressed into a spreadsheet (for example, West Hartford has 7 CVS locations, copy and paste the address field into an Excel spreadsheet - one row for each location, 7 rows total). Add a column in the spreadsheet for store number and address.

To do the distance calculation, we used Google Maps to get the lat/lon for each address. For each CVS location, add the lat/lon as separate columns (‘storeNumber’ ‘address’ ‘lat’, ‘lon’). 


**Traveling Salesman Problem (TSP, optimal routing for one vehicle)**

We used Google OR-Tools to perform the traveling salesman problem. Our depot location should be the State Capitol (41.76428988852701, -72.68249918399205) for ALL GROUP.

**Cost Matrix**
We used the ManhattanDistance() from sci-kit learn to create a cost matrix and we also used the distance callback from OR-Tools. Our distance was rounded to the nearest integer.

**Coding Scenarios**

We ran three different scenarios:
Scenario 1: Automatic (just accept all defaults)
Scenario 2: Try a different first solution strategy
https://developers.google.com/optimization/routing/routing_options#first_sol_options
Scenario 3: Try a different local search option
https://developers.google.com/optimization/routing/routing_options#local_search_options 
