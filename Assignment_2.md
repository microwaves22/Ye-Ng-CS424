# Task 1: Revisit your data and questions
After reviewing our data and initial questions from Assignment 1, we refined some of our questions to better match the attributes available in the dataset. We narrowed our broad question about distraction-free studying into a more specific exploration of the relationship between noise and available seating, expanded our popularity question to focus on occupancy patterns across time and location, and replaced our weather-focused question with a comparison of high-traffic and low-traffic study spaces. That being said, we're moving forward with the following questions:

- Which study spaces are the most reliable for finding available space?
- Are the quietest study spaces also the hardest spaces to find a seat?
- How do occupancy patterns vary across location, time of day, and day of week?
- How do high-traffic and low-traffic study spaces differ from one another?

Additionally, we collected more observations to expand our dataset.

# Task 2: Prepare the data
We used Pandas to prepare and transform our data in this [notebook](Notebooks/Task_2_Data_Prep.ipynb). The first thing we did was combine the weather and study datasets using the date and time attributes. Next, we derived several attributes that would support analysis, which are capacity (sum of occupancy and open seats), occupancy rate (normalized due to different study space sizes), availability rate (normalized due to different study space sizes), day of week (derived from date), and traffic level (high traffic vs. low traffic based on surrounding pedestrian activity). Afterwards, we checked the summary statistics for capacity to make sure there weren't any major inconsistencies. During this time, we noticed that the 1st Floor Study Lounge had an oddly high max capacity that deviated a lot from the mean, so we went back to our original Google Sheet data to see if we missed something. We discovered that we mistyped a couple values, so we immediately went back to the csv file to fix that. Then, we filtered the observed times to only 9 AM, 11 AM, 1 PM, 3 PM, and 5 PM because some of the earlier observations we collected included times that were outside the scope of our finalized considerations. Lastly, we saved our transformations to a [csv dataset](Data/transformed_study_data.csv) of its own to use in upcoming analysis and visualizations.

# Task 3: Explore the data
## Exploratory Visualization 1
This line graph compares time and occupancy rates across different study spaces. We wanted to explore our question, "How do occupancy patterns vary across location, time of day, and day of week?" The distribution can help identify whether there is a relationship between time and seat availability, as well as study space patterns.

During 13:00 most of the study spaces have their highest occupancy rate and then drop at 17:00. Also, the second Floor CS Study Lounge (Quiet) has its highest peak overall at 13:00 with being over 90% occupancy. The first Floor CS Study Lounge stays consisently at the bottom, showing the lowest average occupancy rates across every single time. A note, which could potentially contribute is that is has the most seat availability of all study spaces.

A general trend is seen with occupancy starting lower in the morning at 9:00, and then increasing quickly by early afternoon, and then decreasing quickly by 17:00.

## Exploratory Visualization 2
This scatterplot compares noise levels with seat availability rates across different study spaces. We wanted to explore our question, "Are the quietest study spaces also the hardest spaces to find a seat?" The distribution of points can help identify whether there is a relationship between noise level and seat availability, as well as if certain study spaces show different patterns. 

Some notices pertaining noise, in the second Floor CS Study Lounge (Quiet) is futher to the left, which supports generally lower noise levels ~(38dB - 50dB). Whereas in the first Floor Sandella Cafe and first Floor Lobby Area are futher to the right, closer to 69dB. This finding on the second Floor CS Study Lounge supports our finding in Visualization #1 in regards to time and occupancy.

Some notices pertaining seat availability, the second Floor CS Study Lounge and Sandella Cafe show low seat avability the most compared to other locations. A note, which potentially contributes to this is that they have less seats than the other study areas, but fourth Floor Study Lounge is an outlier in this.


# Task 4: Implement visualization alternatives

# Task 5: Interaction and multiple views

# Task 6: Iterate and refine

# Task 7: Current design
