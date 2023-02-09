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
