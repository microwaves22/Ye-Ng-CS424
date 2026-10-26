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
We wanted to explore how occupancy rates change throughout the day across different study spaces. We noticed that most study spaces had higher occupancy rates around 13:00 and lower rates by 17:00. The Second Floor CS Study Lounge (Quiet) had its highest occupancy at 13:00, reaching over 90%. On the otherhand, the First FLoor CS Study Lounge generally had lower occupancy rates than the other study spaces. We also noticed that occupancy rates were generally lower at 9:00, but then increased by late morning/early afternoon, and then decreased by 17:00.

## Exploratory Visualization 2
This scatterplot compares noise levels with seat availability rates across different study spaces. We wanted to explore our question, "Are the quietest study spaces also the hardest spaces to find a seat?" The distribution of points can help identify whether there is a relationship between noise level and seat availability, as well as if certain study spaces show different patterns. 

Some notices pertaining noise, in the second Floor CS Study Lounge (Quiet) is futher to the left, which supports generally lower noise levels ~(38dB - 50dB). Whereas in the first Floor Sandella Cafe and first Floor Lobby Area are futher to the right, closer to 69dB. This finding on the second Floor CS Study Lounge supports our finding in Visualization #1 in regards to time and occupancy.

Some notices pertaining seat availability, the second Floor CS Study Lounge and Sandella Cafe show low seat avability the most compared to other locations. A note, which potentially contributes to this is that they have less seats than the other study areas, but fourth Floor Study Lounge is an outlier in this.

## Exploratory Visualization 3
This box plot compares occupancy rate and traffic level with noise level and traffic level. We wanted to explore our question, "How do high-traffic and low-traffic study spaces differ from one another?" This allows us to compare occupancy rate and noise level on separate plots, but still allowing easy accessible comparison.

What was notices was that during high traffic periods the median occupancy rate is around 55% whereas low traffic periods drop to a median of around 40%. Also, the entire box for high traffic is shifted upward, which means that students typically are taking majority of the seats during this time. On the otherhand, low traffic periods see more lower occupancy.

Also during high traffic periods it is louder with the median noise level around 56, compared to a median of 53-54 during low traffic. There is a couple of outliers in the low traffic category where a few are around 38 and 41, which means it was even quieter.  

# Task 4: Implement Visualization Alternatives
## Visualization #1
![Task 4 Visualization 1](Visualizations_2/task4_vis1.png)

This heat map approaches the question, "How do occupancy patterns vary across location, time of day, and day of week?" This is based off of the sketch from assignment #1 of a heatmap. The heatmap shows an average occupancy rate across different 

Attempting to redo this for Curio
 - lost account; use username + password and said it was wrong
 - 502 error
 - offline twice within 10 minutes

## Visualization #2
![Task 4 Visualization 2](Visualizations_2/task4_vis2.png)

This scatterplot addresses the question "Which study spaces are the most reliable for finding available space?" We used this approach because reliability can be determined by comparing average (mean) availability rates to availability variability (standard deviation), allowing us to view both availability and consistency across different locations. The dimensions of a scatterplot allow us to easily view those simultaneously. To elaborate, the most reliable locations would balance both high average availability and low availability variability. That being said, the attributes we used in this visualization are location, availability rate, average availability rate, and the standard deviation of availability rate. We used average availability rate to represent how often seats are typically available and standard deviation to measure how much availability fluctuates across observations. The marks we used are points, which represent locations in the CDRLC. The channels are position (x and y) and colors for each point. Furthermore, this scatterplot is an entirely new design that we didn't sketch in Assignment 1. We didn't want to implement our original sketch for this question because in that sketch, we used the sizes of circles to represent different availability rates on a spatial map, but it's harder to distinguish those visually.

 ## Visualization #3
![Task 4 Visualization 3](Visualizations_2/task4_vis3.png)

This visualization supports the question "Are the quietest study spaces also the hardest spaces to find a seat?" We used this approach to compare rankings of study spaces based on average noise level and average seat availability side-by-side. The data attributes that this visualization uses are location, average noise level, and average availability rate. The marks we used are bars, and the channels are length of the bars to represent average noise level or average availability rate and vertical positions to rank the study spaces by attributes. There are also two charts that are side-by-side to aid with making attribute comparisions. Although we initially considered creating a scatterplot visualization, we realized that we wanted a unique visualization that emphasized ranking and direct comparisions between study spaces. Therefore, creating ranked bar charts was the most straightforward way of accomplishing this. However, one thing we noticed is that this visualization involves aggregation, which is a source of uncertainty because we aren't able to see more detailed variation of the data over time or days. This is something we may potentially address in the upcoming tasks.

# Task 5: Interaction and Multiple Views

## Visualization #1
[Visualization reference](Notebooks/Vis_1.ipynb)



## Visualization #2

[Visualization reference](Notebooks/Vis_2.ipynb)

We believe that this visualization would benefit from interaction, specifically details-on-demand. By simply looking at the scatterplot's points, it's generally not straightforward to determine exact values. To address this, we want to implement the ability to display additional information when a user hovers their cursor over a point. That information would include study spot location, average availability rate, availability variability, average occupancy rate, and traffic level. This interaction would also allow users to quickly inspect the data without the additional information cluttering the overall view of the data.

## Visualization #3

[Visualization reference](Notebooks/Vis_3.ipynb)

This visualization uses two coordinated views, which displays separate ranked bar charts for average noise level and average availability rate. The two charts show the same study spaces ordered by different criteria, allowing users to compare rankings side-by-side. This supports our task of determining whether quieter study spaces also tend to have lower seat availability. Furthermore, we also want to incorporate a details-on-demand through hovering. We want to move forward with this approach because we noticed how some of the bars have similar lengths, making it hard to determine exact values from visual inspection alone. Implementing this would look like users hovering over a bar and the exact average noise level or average availability rate getting displayed. This would help users make more precise value comparisons while maintaining a clean visualization look.

# Task 6: Iterate and Refine

## Visualization #2
![Task 6 Visualization 2](Visualizations_2/task_6_vis_2.png)

Note: You can access the refined visualization at [this notebook](Notebooks/Vis_2.ipynb)

Iteration 1: Details-on-Demand Interaction

A problem we noticed is that it was difficult to determine exact values from the original scatterplot. To address that, we added those values and extra information to each point to improve readability. We also made the visualization interactive, meaning that users can hover their cursor over each point to display the additional details. This helps reduce clutter while making the visualization more informative and supporting more precise comparisions between study locations.

Iteration 2: Reliability Quadrants

Another problem we discovered is that the visualization didn't clearly indicate which locations were more or less reliable. As a result, we added horizontal and vertical grid lines at the mean availability and mean variability values, creating four interpretation regions. We also included labels identifying the "Most Reliable" and "Least Reliable" regions. The overarching purpose of making those changes were to make it easier to identify study spaces with above-average availability and below-average availability, assisting users with interpreting reliability quickly and consistently.

## Visualization #3
![Task 6 Visualization 3](Visualizations_2/task_6_vis_3.png)

Note: You can access the refined visualization at [this notebook](Notebooks/Vis_3.ipynb)

Iteration 1: Details-on-Demand Interaction

A problem we observed is that many study spaces have similar bar lengths, making it difficult to determine exact values from looking at the bar lengths alone. We fixed this by making the bar charts interactive, allowing users to hover over each bar, which displays exact average noise level or availability rate for the selected study location. This allows users to make more precise comparisons between locations without adding more labels that could clutter the visualizations.

Iteration 2: Consistent Color Encoding Across Views

Another problem we discovered is that users had to repeatedly locate the same study space in both the noise ranking and availability ranking when making comparisons. We fixed this by adding another channel of color. To be more specific, we assigned a consistent color to each study space across both ranking charts. That way, the same location is represented by the same color in both views. This is helpful because it strengthens the relationship between the two views and makes it easier to compare how a study space ranks across noise level and availability.


# Task 7: Current Design
