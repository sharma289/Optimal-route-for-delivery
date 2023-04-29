# Find optimal route for delivery

Objective: To design and create algorithm for finding the optimal routes for 10 delivery agents to deliver parcels from a store to 100 different locations.

Approach:

1. Read the 'Location.txt' file that contains ID, Latitude and Longitude of all 100 delivery locations and create their separate list.

2. Convert the lists into a Pandas dataframe with column names 'ID', 'Latitude', and 'Longitude'. Use 'KMean' clustering technique of scikit-learn with 'n_clusters = Number of agents' to create 10 clusters.

3. Each agent will deliver the parcel to a single cluster. Now the next step is to find the order of delivery which means how an agent will decide which location he had to go first to minimize his distance travel.

4. Create a function to calculate distance from store location to delivery address location using Manhattan distance formula and store it into 'Distance' column in the dataframe.

5. Use a loop to arrange the order of delivery so that the address closest to the store will be delivered first, the second closest location, the third one, and so on.

6. Copy the ordering of location ID as a set and store it for all clusters into the 'output' list.

7. 'output' is the solution we need.

ANSWER = [[17, 15, 12, 13, 14, 16, 3, 8, 9, 11, 10, 7, 5, 6, 4, 2, 1, 18], [19, 20, 21], [23, 24, 22], [26, 25, 27, 28, 29], [31, 30], [32, 33], [34], [35, 38], [45, 46, 48, 47, 43, 42, 41, 40, 44, 39, 84, 37, 36], [100, 96, 99, 98, 87, 86, 97, 85, 92, 95, 93, 94, 90, 89, 88, 91, 83, 82, 79, 81, 80, 78, 77, 76, 75, 71, 69, 72, 73, 70, 66, 74, 62, 63, 64, 65, 60, 61, 57, 68, 67, 59, 56, 54, 53, 58, 52, 55, 50, 51, 49]]
