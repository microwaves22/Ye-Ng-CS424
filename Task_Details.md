<!-- # for main headers, ** for bold text, - or * for bullet points, and | for tables
![Description of image](path/to/image.png) -->

# Task #1: Observation and data collection plan

## Primary Dataset
- Add path to CSV file
- ![Link to Google Sheets](https://docs.google.com/spreadsheets/d/1kPfpt8VzsofgehPeB3OIRECaAapwIVqHasqaJXrZmyE/edit?usp=sharing)

## Description of What is Desired to Observe and Why
- Our group desires to observe the University of Illinois-Chicago's (UIC) Computer Design and Learning Resource Center (CDLRC). We want to observe the enviornment of different selected locations of study spots around the building across multiple times and days.
- Just like many Computer Science (CS) students at UIC, we study in the CDLRC frequently and are curious as to what constitutes optimal study spots in that building, meaning that the enviornment can support the productivity of our academics and work.

## Four Initial Domain Questions
- Around a certain time, where are the most available spaces to study in the CDRLC?
- Which spaces in the CDRLC provide the studying quality I want?
- What ammenities are near these study locations in the CDRLC?
- Which study spaces best fit different study activites in the CDRLC?

## Proposed Data Collection Process

An observation is constituted as having data for all of the attributes that are described in the data dictionary below. We want to take into
account those observations because enviornmental factors and what different spaces have to offer are inherent factors that cause people to
subconciously decide where they want to study. Admittedly, our list of attributes is very granular because it's not feasible for us to fully
anticipate or know how the actual data collection experience will go and what our findings will be, so we want to cover as many attributes as
we can per observation for now. We will make adjustments based on the outcomes later, if necessary.

Since our focus is on the CDRLC, all of the locations that we will visit will be in this building only. We've also identified 14 locations
to collect data, and these locations are a mix of main or prominent study areas and smaller study spots that are in different corners of the
building. We plan on collecting data at every hour of the weekday (Monday to Friday) starting from 9 AM and ending at 6 PM, which are the most
common times that students are in the building. The plan is to collect data across five days. Repeating observations by visiting many locations
for each hour of the timeframe we described will ensure that our data captures meaningful variation about each study spot rather than a single
snapshot. For instance, the situation of study spots on Monday at 12 PM would most likely be different than the situation on Friday at 5 PM.

In terms of dividing the work of data collection, our group of two members will split the work based on our schedule availability at different
hours of the day. This ensures that at least one person is available to collect data at a particular time. Something else we've considered is the
difficulty of having one person collect data at, for instance, 9 AM every day because the contraints of our schedules don't allow
for that. One member might be available at 9 AM on Tuesday's and Thursday's only, so the other person would fill in for the other three days since
they're available at that time on those days. Despite these circumstances, the group addressed them by collectively discussing our data collection
methodology to ensure we're all on the same page and to minimize as much inconsistencies and human error as possible. Some ways we ensure that our
data collection process is the same is that we both use the same weather app and noise level recording app, we both record noise levels for exactly
30 seconds and focus on recording the mean or average decibel value, and we have discussed how to count open vs. occupied seats or what constitutes
particular chair or table types.

Our collection process might introduce bias based on what we determine to be a group of students that are together, our personal definitions of tables
or chairs, the tables and chairs getting moved around, and possibly miscounting people due to the natural movement of people leaving and entering an
area or people standing instead of sitting.

## Initial Data Dictionary
| Attribute                           | Type         | Description                                                   | Example                   |
| :--- | :--- | :--- | :--- |
| `date`                              | Temporal     | Date of observation                                           | 9/17/2026                 |
| `time`                              | Temporal     | Time of observation                                           | 13:00                     |
| `location`                          | Categorical  | Location of the study area                                    | 2nd Floor CS Study Lounge |
| `weather_condition`                 | Categorical  | Description of the outside weather                            | Sunny                     |
| `weather_temperature`               | Quantitative | Degree in Fahrenheit                                          | 75                        |
| `noise_level`                       | Quantitative | Average noise level in decibels across the span of 30 seconds | 81.2                      |
| `occupancy`                         | Quantitative | Total number of occupants at a location                       | 15                        |
| `single-person_tables`              | Quantitative | Number of fully open tables for 1                             | 6                         |
| `two-person_tables`                 | Quantitative | Number of fully open tables for 2                             | 3                         |
| `tables_for_multiple_people`        | Quantitative | Number of fully open tables for 3+ people                     | 5                         |
| `nook_chair_availability`           | Quantitative | Number of open nook seats                                     | 4                         |
| `regular_plastic_chair_availability`| Quantitative | Number of open regular pastlic seats                          | 8                         |
| `tall_plastic_chair_availability`   | Quantitative | Number of open tall plastic seats                             | 3                         |
| `sofa_spot_availability`            | Quantitative | Number of empty soft seats                                    | 1                         |
| `outlets`                           | Quantitative | Number of outlets at a location                               | 4                         |
| `window_access`                     | Categorical  | Is there access to direct sunlight?                           | Yes                       |
| `number_of_single-person_tables`    | Quantitative | Number of tables for 1 at a location                          | 5                         |
| `number_of_two-person_tables`       | Quantitative | Number of tables for 2 at a location                          | 4                         |
| `number_of_multiple_people_tables`  | Qunatitative | Number of tables for 3+ people at a location                  | 4                         |
| `number_of_nook_chairs`             | Quantitative | Number of nook seats at a location                            | 7                         |
| `number_of_regular_plastic_chairs`  | Quantitative | Number of regular plastic chairs at a location                | 4                         |
| `number_of_tall_plastic_chairs`     | Quantitative | Number of tall plastic chairs at a location                   | 8                         |
| `number_of_sofa_spots`              | Quantitative | Number of sofa spots at a location                            | 2                         |                                      


# Task 2: Pilot and data collection

## Pilot Collection & Key Findings
On September 17, 2026 at 11:00 AM, our team conducted a pilot collection at the University of Illinois-Chicago (UIC) Computer Design Research and Learning Center (CDRLC)

## Collection Protocol & Timing
To test workload and feasibility of the collection, the team split up and each collected data across the different floors:
- Elizabeth: Covered all designated study spots on Floors 1 and 2 (time: ~20 minutes)  
  > *note: due to class time conflict Elizabeth did not cover all study spots*
- Michelle: Covered all designated study spots on Floors 1-5 (time: ~30 minutes) and tested a subset excluding Floors 3 and 5 (times: ~15 minutes)

At first, we recorded data using Google Sheets with a separate key mapping `Location ID` to `Location Description` (e.g., `11` for `Area in front of stairs`)

## Pilot Observations & Issues Found
- Location ID Issue: Needing to cross-reference `Location ID` numbers with the `Location Descriptions` caused extra unnecessary mental load and slowed down the collection process. 
- Enclosed Study Rooms: Initially, we planned to include the study rooms on the second floor that can be booked. However, because these spaces are enclosed, pre-booking is required, and there are multiple study rooms, recording occupancy and noise levels inside them did not align with our focus on open/shared study spaces.
- Office Hour Study Spaces: Initially, we also planned to factor in all of the Office Hour areas on the second floor. Due to time constraints and the notion that these areas are specifically meant for students in those courses at specific tables, we decided they did not align with our focus on general open/shared study spaces.
- Movable Furniture: Students frequently moved chairs between nearby tables. Trying to track exact counts per table was chaotic and created confusion when a chair was moved from one nearby study area to another.
- Seating Types: We initially wanted to track detailed chair/table variations (e.g., 1-person tables, nook chairs, tall plastic chairs, ADA accessibility, sofa spots). However, capturing these granular seating types proved overly complex, time-consuming, and difficult to standardize across collectors.

## Revisions & Professor Consultation

Following our pilot, we scheduled a meeting with our professor to discuss issues that arose, how to simplify our attributes without losing data, and more. 

During our meeting, our professor provided key feedback to guide our strategy:
- Increase Data Points: 30 observations isn't enough to capture meaningful variation. We need to collect across more days or more times throughout the day to notice if there’s any signal or pattern across the span of 1-2 days.
- Simplify Attributes: Restrict the total amount of attributes so collecting frequent observations over time is feasible. Our professor recommended using the simplest approach possible—don't worry about people moving between rooms or furniture moving around.
- Summarize Metrics: Summarize attributes after occupancy down to 2-3 essential, less granular attributes: count number of people, count the number of open seats, and count the number of outlets.

Based on our pilot findings and feedback from our professor, we made the following revisions:
- Removed study rooms and Office hour study areas: Excluded booked study rooms and course-specific office hour tables to focus strictly on open/shared spaces.
- Simplified seating and furniture: Stripped away complex chair types and table variations in favor of simpler counts: seat availability, people present, and outlet access.
- Made zones bigger by merging close study areas: Combined adjacent areas where furniture easily moves around into unified zones so individual chair shifts won't affect our counts.
- Replaced location ID system: Used direct location descriptions on the main collection sheet instead of forcing cross-referencing with a separate lookup key.
- Removed floors 3 and 5: Excluded these floors because they only consist of a single table with 2-3 seats next to the elevator, which did not provide useful data for our study.
- Expanded collection frequency: Scheduled data collection across multiple days and varying times of day to ensure we collect a higher volume of data points and detect meaningful patterns.

## Revised Data Dictionary (Post-Pilot)
| Attribute | Type | Description | Example |
| :--- | :--- | :--- | :--- |
| `date` | Temporal | Date of observation | 9/17/2026 |
| `time` | Temporal | Time of observation | 13:00 |
| `location` | Categorical | Specific study area within UIC CDRLC | 2nd Floor CS Study Lounge Collaborative |
| `weather_condition` | Categorical | Description of outside weather | Sunny |
| `weather_temperature` | Quantitative | Degree in Fahrenheit | 75 |
| `noise_level` | Quantitative | Average noise level in decibels across the span of 30 seconds | 81.2 |
| `occupancy` | Quantitative | Total number of occupants at a location | 25 |
| `open_seats` | Quantitative | Number of open seats at a location | 12 |

## Full Data Collection Strategy
- Collection Strategy: To increase data points as suggested by our professor, data will be collected over more days and more times throughout the day to notice if there's any signal or pattern across the span of 1-2 days.
- Dataset File:[File Path] (./Data/Pilot_Collection_Data.csv)

# Task 3: Data description and domain questions

## Dataset Overview & Collectin Process

Data was collected over a two-week period from September 21, 2026 to October 2, 2026 (Monday to Friday). The dataset collected caputres spatial and temporal variations in noise and seating occupancy across five selected areas of CDRLC. The areas include: the Sandella Cafe seating, 1st Floor CS Lounge, Fron of Stairs area, 2nd Floor CS Study Lounge (split into Collaborative and Quiet sections), and the 4th Floor Balcony. Sampling occurred daily across five fixed time slots (9:00 AM, 11:00 AM, 1:00 PM, 3:00 PM, and 5:00 PM). In total 50 observation windows and 300 individual area data points.

For every location and time slot, we recorded six attributes: Area Name, People Count, Open Seats Count, Average Noise Level (dB), Temperature (°F), and Weather Condition. Also a Notes section. Sound levels were caputured using 30-second average decibel readings with the Decibel X app, while ambient weather parameters were recorded from iPhone's weather app.

To ensure consistent sampling, we established observational rules: chairs occupied by belongings were marked as occupied unless the owner was actively seated nearby, circle blue couches were recorded at a capacity of one person per circle, and long blue couches were evaluated at two people per stitched seat segment.

## Limitations and Biases

Our dataset contains inherent sampling limitations and potential sources of bias:
- Decibel Measurements: Capturing sound over a 30-second window means that even a brief burst of loud noise (e.g., someone dropping something, door closing, laughing loudly) could slightly skew the mean reading compared to ambient continuous volume. 
  > *Note this was attempted to be lowered by restarting recording if the noise subjectively really ruined the data*
- Seating Assumptions: deciding whether unattended bags represented a temporarily open seat or a long-term open spot. This requires subjective judgment, but was attempted to limit based on obvious factors like an open laptop, or items on the table. (e.g., one person would typically not have 2 backpacks or 2 laptops)
- Temporal scope: Collection was constrained to weekdays between 9:00 AM to 5:00PM, our data reflects peak academic hours, but misses evning study habits and weekend activity.
  > *Note this was due to group members conflict with school schedules, work schedules, living off campus, etc*

## Abstraction & Process Reflection

Taking the dynamic physical spaces into rows and numeric values required compressing complex social environments into standardized attributes. Our dataset effectively captured quantitative trends for space usage, number of people, noise level, and outside weather.

Some qualitative nuances were lost in the abstraction:
- Noise Quality: devibel metric captures sound pressure level, but loses type of noise a room has. For example some rooms had a higher sound pressure level, but it was due to the loud HVAC in the room rather than human conversation.
- Seating Dynamics: Recording people count and open seats count fails to capture group dynamics like people working together or alone. It also fails to capture what types of seating are available. If a table with four chairs only has one person sitting compared to a table with four chairs and no one sitting.

Deciding how real-world observations became data points required creating a standard. For example, when individuals were standing we recorded them in people count and added in notes saying that they were standing so the open seats count baseline was not too affected. Also having set couch capacity based on stitching helped us have discrete numeric attributes.

## Refined Domain Questions

1. Does the 2nd Floor Quiet Area consistently maintain lower decibel levels than collaborative spaces during peak hours (11:00 AM – 1:00 PM)?
    - Original Quetion: Which spaces in the CDRLC provide the studying quality I want?
    - Why Changed: Quality is too subjective for visualization so narrowing it down to be more specific and measurable with decibel levels is helpful.
    - Reasoning: This question tests how spaces more limited to individual seating controls sound levels when student traffic is highest.
2. Refined Question: At what specific times during the day is seat scarcity most severe across all locations?
    - Original Question: Around a certain time, where are the most available spaces to study in the CDRLC?
    - Why Changed: With structured data and timestamps it is more easier to visualize precise hourly open seating.
    - Reasoning: This identifies peak times when there are many people in an area based on time and provides it for each area.
3. How do external temperature and weather conditions impact the availability of seating?
    - Original Quetion: What amenities are near these study locations in the CDRLC?
    - Why Changed: We did not count amenities, but we did factor in weather data.
    - Reasoning: This looks at how outdoor weather can affect seating by using temperature, weather condition, area, and the open seats count.
4. Is there a correlation between the number of people and the sound level, or are certain places typically louder?
    - Original Quetion: Which study spaces best fit different study activities in the CDRLC?
    - Why Changed: The student activity types and seating types were not tracked so this question is harder to answer.
    - Reasoning: This helps us determine if noise level is affected by the number of people or if the room is generally louder.

# Task 4: Task abstractions

# Task 5: Visualization sketches

# Task 6: Summarizing

# Task 7: Collaboration process


# IDK where this goes: photos
- notes converted with Canva fom heic to jpeg 
- hiding people's faces w/ Canva editing