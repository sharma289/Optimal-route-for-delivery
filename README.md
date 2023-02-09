# Zorang-Recruitment-Project
Submitted by - Rajat Sharma

Roll no.: 21ME61R08

Objective: To design and create algorithm for finding the optimal routes for 10 delivery agents to deliver parcels from a store to 100 different locations.

Approach:

1. Read the 'Location.txt' file that contains ID, Latitude and Longitude of all 100 delivery locations and create their seperate list.

2. Convert the lists into a Pandas dataframe with column names 'ID', 'Latitude', and 'Longitude'.

3. Use KMean clustering technique with 'n_clusters = Number of agents' to create 10 clusters. Each agent will deliver parcel to a single cluster.

4. Now the next stem is to find the order of delivery which means how an agent will decide which location he had to go first to minimize his distance travel.

5. Create a function to calculate distance from store location to delivery address location using Manhattan distance formula and store it into 'Distance' column in the dataframe.

6. Use a loop arrange the order of delivery such that the address which is closest to the store will be delivered first then the second most closest location then the third one and so on.

7. Copy the ordering of location ID as a set and store it for all clusters into the 'output' list.

8. 'output' is our required solution.

ANSWER = [[32, 33], [49, 50, 51, 52, 53, 54, 55, 56, 57, 58, 59, 60, 61, 62, 63, 64, 65, 66, 67, 68, 69, 70, 71, 72, 73, 74, 75, 76, 77, 78, 79, 80, 81, 82, 83, 85, 86, 87, 88, 89, 90, 91, 92, 93, 94, 95, 96, 97, 98, 99, 100], [19, 20, 21], [30, 31], [25, 26, 27, 28, 29], [34], [22, 23, 24], [36, 37, 39, 40, 41, 42, 43, 44, 45, 46, 47, 48, 84], [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18], [35, 38]]
