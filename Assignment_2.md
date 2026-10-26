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

This scatterplot compares noise levels with seat availability rates across different study spaces. We wanted to explore seat availability and noise level's relationship. We noticed that the Second Floor CS Study Lounge (Quiet) was farther to the left, with noise levels around 38-50dB. On the otherhand, the First Floor Sandella Cafe and First Floor Lobby Area were farther to the right, with noise levels closer to 69dB. Another finding is that the Second Floor CS Study Lounge and Sandella Cafe showed lower seat availability than most of the other locations. We also noticed that theses study spaces have fewer seats than some of the other study areas, although the Fourth Floor Study Lounge was an exception to this pattern.

## Exploratory Visualization 3
We wanted to explore occupancy rates and noise levels, and how they change or differ across study space's surrounding traffic. We created two box plots to explore how occupancy rates and noise levels differ between study spaces near high-traffic areas, such as cafes, elevators, entrances, and hallways, and study spaces near low-traffic areas, such as enclosed spaces. We noticed that high-traffic spaces have a higher median occupancy rate of around 55%, compared to 40% for low-traffic spaces. Noise levels were also slightly higher in high-traffic spaces, with a median of around 56dB compared to 54dB. We also noticed a few unusually low and high noirse measurements in the low-traffic group.

## Exploratory Visualization 4
We wanted to explore which specific study spaces offer the highest and lowest overall seat availability across all observation times. We created a horizontal bar chart ranking each study space by its average availability rate. We noticed that the 1st Floor CS Study Lounge had the highest average seat availability by a notable margin, reaching over 70%. In contrast, the 2nd Floor CS Study Lounge Quiet had the lowest availability at around 40%, closely followed by the 1st Floor Lobby Area at roughly 43%. The 4th Floor Study Lounge, 1st Floor Sandella Cafe, and 2nd Floor CS Study Lounge Collaborative formed a middle tier with average availability rates ranging between 50% and 60%.    

# Task 4: Implement Visualization Alternatives
## Visualization #1
![Task 4 Visualization 1](Visualizations_2/task4_vis1.png)
This heatmap approaches the question, "How do occupancy patterns vary across location, time of day, and day of week?" We used this approach because a heatmap allows us to compare average occupancy rates across different days of the week and time periods, and it is based off of a design created in Assignment 1. The attributes included in this visualization are time of day, day of week, and occupancy rate. The marks are the squares in the grid, and the visual channels include color intensity, with different shades of blue and green representing different occupancy rates. This approach makes it easier to identify general patterns across different times and days while providing an overview of occupancy rates throughout the week. For example, we can compare which times of day tend to have higher or lower occupancy rates and whether certain days show different patterns. However, the heatmap may hide differences between individual days because observations from the same day of the week are aggregated into average occupancy rates. It also does not represent individual study locations, but instead combines the data across all locations. This can make it harder to identify specific differences between study spaces or determine whether certain locations have different occupancy patterns. We wanted to use this visualization to get a general overview of occupancy patterns, but these limitations show that more detailed comparisons may be needed to understand the differences between individual locations and observations over time.

## Visualization #2
![Task 4 Visualization 2](Visualizations_2/task4_vis2.png)

This scatterplot addresses the question "Which study spaces are the most reliable for finding available space?" We used this approach because reliability can be determined by comparing average (mean) availability rates to availability variability (standard deviation), allowing us to view both availability and consistency across different locations. The dimensions of a scatterplot allow us to easily view those simultaneously. To elaborate, the most reliable locations would balance both high average availability and low availability variability. That being said, the attributes we used in this visualization are location, availability rate, average availability rate, and the standard deviation of availability rate. We used average availability rate to represent how often seats are typically available and standard deviation to measure how much availability fluctuates across observations. The marks we used are points, which represent locations in the CDRLC. The channels are position (x and y) and colors for each point. Furthermore, this scatterplot is an entirely new design that we didn't sketch in Assignment 1. We didn't want to implement our original sketch for this question because in that sketch, we used the sizes of circles to represent different availability rates on a spatial map, but it's harder to distinguish those visually.

 ## Visualization #3
![Task 4 Visualization 3](Visualizations_2/task4_vis3.png)

This visualization supports the question "Are the quietest study spaces also the hardest spaces to find a seat?" We used this approach to compare rankings of study spaces based on average noise level and average seat availability side-by-side. The data attributes that this visualization uses are location, average noise level, and average availability rate. The marks we used are bars, and the channels are length of the bars to represent average noise level or average availability rate and vertical positions to rank the study spaces by attributes. There are also two charts that are side-by-side to aid with making attribute comparisions. Although we initially considered creating a scatterplot visualization, we realized that we wanted a unique visualization that emphasized ranking and direct comparisions between study spaces. Therefore, creating ranked bar charts was the most straightforward way of accomplishing this. However, one thing we noticed is that this visualization involves aggregation, which is a source of uncertainty because we aren't able to see more detailed variation of the data over time or days. This is something we may potentially address in the upcoming tasks.

# Task 5: Interaction and Multiple Views
## Visualization #1
We believe this visualization could benefit from filtering, allowing users to focus on specific days or time periods. This would make it easier to examine occupancy patterns without having to view all the data at once. We also considered adding details-on-demand through hovering, which could display the exact average occupancy rate for a specific day and time. However, since the heatmap is intended to provide a general overview of occupancy patterns, keeping the visualization relatively simple would help users identify broader trends without unnecessary clutter.

## Visualization #2
We believe that this visualization would benefit from interaction, specifically details-on-demand. By simply looking at the scatterplot's points, it's generally not straightforward to determine exact values. To address this, we want to implement the ability to display additional information when a user hovers their cursor over a point. That information would include study spot location, average availability rate, availability variability, average occupancy rate, and traffic level. This interaction would also allow users to quickly inspect the data without the additional information cluttering the overall view of the data.

## Visualization #3
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
For our current design, we decided to move forward with the refined scatterplot and ranked bar charts from Task 6 to help answer our main questions about seat reliability and noise. The scatterplot plots average availability against how much that availability changes over time. It includes hover tooltips to show exact numbers and grid lines that break the chart into four reliability sections, making it easy to spot the most consistent study spots. Next to it, our ranked bar charts use side-by-side views to compare average noise levels and seat availability. We added hover details for exact values and used the same color for each study space across both charts so they are easy to match up. Compared to our original spatial map sketches from Assignment 1, these final designs focus more on clear, direct comparisons while keeping the charts easy to read. Going forward, we plan to test these visualizations with users to see if the four sections and colors make sense, get feedback on readability, and figure out if any final changes are needed so people can read the data without getting confused.