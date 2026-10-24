# Task 1: Revisit your data and questions
After reviewing our data and initial questions from Assignment 1, we refined some of our questions to better match
the attributes available in the dataset. We narrowed our broad question about distraction-free studying into a more 
specific exploration of the relationship between noise and available seating, expanded our popularity question to focus
on occupancy patterns across time and location, and replaced our weather-focused question with a comparison of high-traffic
and low-traffic study spaces. That being said, we're moving forward with the following questions:

- Which study spaces are the most reliable for finding available space?
- Are the quietest study spaces also the hardest spaces to find a seat?
- How do occupancy patterns vary across location, time of day, and day of week?
- How do high-traffic and low-traffic study spaces differ from one another?

Additionally, we collected more observations to expand our dataset.

# Task 2: Prepare the data
We used Pandas to prepare and transform our data. The first thing we did was combine the weather and study datasets using
the date and time attributes. Next, we derived several attributes that would support analysis, which are capacity (sum of occupancy and open seats), occupancy rate (normalized due to different study space sizes), availability rate (normalizaed due to different study space sizes), day of week (derived from date), and traffic level (high traffic vs. low traffic based on surrounding pedestrian activity). Afterwards, we checked the summary statistics for capacity to make sure there weren't any major inconsistencies. During this time, we noticed that the 1st Floor Study Lounge had an oddly high max capacity that deviated a lot from the mean, so we went back to our original Excel data to see if we missed something. We discovered that we mistyped a couple values, so we immeadiately went back to the csv file to fix that. Then, we filtered the observed times to only 9 AM, 11 AM, 1 PM, 3 PM, and 5 PM because some of the earlier observations we collected included times that were outside the scope of our finalized considerations. Lastly, we saved our transformations to a csv dataset of its own to use in upcoming analysis and visualizations.

# Task 3: Explore the data

# Task 4: Implement visualization alternatives

# Task 5: Interaction and multiple views

# Task 6: Iterate and refine

# Task 7: Current design
