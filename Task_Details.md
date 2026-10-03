<!-- # for main headers, ** for bold text, - or * for bullet points, and | for tables
![Description of image](path/to/image.png) -->

# Task #1: Observation and data collection plan
**Primary Dataset**
- Add path to CSV file
- Add link to Google Sheets

**Description of What is Desired to Observe and Why**
- Our group desires to observe the University of Illinois-Chicago's (UIC) Computer Design and Learning Resource Center (CDLRC). We want to observe the enviornment of different selected locations of study spots around the building across multiple times and days.
- Just like many Computer Science (CS) students at UIC, we study in the CDLRC frequently and are curious as to what constitutes optimal study spots in that building, meaning that the enviornment can support the productivity of our academics and work.

**Four Initial Domain Questions**
- Around a certain time, where are the most available spaces to study in the CDRLC?
- Which spaces in the CDRLC provide the studying quality I want?
- What ammenities are near these study locations in the CDRLC?
- Which study spaces best fit different study activites in the CDRLC?

**Proposed Data Collection Process**

An observation is constituted as having data for all of the following attributes: 
- Date
- Time
- Location
- Weather condition
- Weather temperature
- Noise level
- Occupancy
- Single-person tables
- Two-person tables
- Tables for 3+ people
- Nook chair availability
- Regular plastic chair availability
- Tall plastic chair availability
- Sofa spot availability
- Number of outlets
- Window access
- Number of single-person tables
- Number of two-person tables
- Number of tables for 3+ people
- Number of nook chairs
- Number of regular plastic chairs
- Number of tall plastic chairs
- Number of sofa spots

We want to take into account those observations because enviornmental factors and what different spaces have to offer are inherent
factors that cause people to subconciously decide where they want to study. Admittedly, our list of attributes is very granular because
we're not sure how the actual data collection experience will go and want to cover as many attributes as we can per observation. However,
we will make modifications based on the outcomes later, if necessary.

Since our focus is on the CDRLC, all of the locations that we will visit will be in this building only. We've also identified 14 locations
to collect data, and these locations are a mix of main or prominent study areas and smaller study spots that are in different corners of the
building. We plan on collecting data at every hour of the weekday (Monday to Friday) starting from 9 AM and ending at 6 PM. The plan is to do
this across five days. Repeating observations by visiting many locations for each hour of the timeframe we described will ensure that our data
captures meaningful variation rather than a single snapshot. 

In terms of dividing the work of data collection, our group of two members will split the work based on our schedule availability at different
hours of the day. This ensures that at least one person is available to collect data at a particular time. Something else we've considered is the
difficulty of having one person collect data at, for instance, 9 AM every day because the contraints of our schedules don't allow
for that. One member might be available at 9 AM on Tuesday's and Thursday's only, so the other person would fill in for the other three days since
they're available at that time on those days. Despite these circumstances, the group addressed them by collectively discussing our data collection
methodology to ensure we're all on the same page and to minimize as much inconsistencies and human error as possible. 

Our collection process might introduce bias based on what we determine to be a group of students that are together, our personal definitions of tables
or chairs, the tables and chairs getting moved around, and possibly miscounting people due to the natural movement of people leaving and entering an
area or people standing instead of sitting.

**Initial Data Dictionary**

# Task 2: Pilot and data collection

**Pilot Collection & Key Findings**
On September 17, 2026 at 11:00 AM, our team conducted a pilot collection at the University of Illinois-Chicago (UIC) Computer Design Research and Learning Center (CDRLC)

**Collection Protocol & Timing**
To test workload and feasibility of the collection, the team split up and each collected data across the different floors:
- Elizabeth: Covered all designated study spots on Floors 1 and 2 (time: ~20 minutes)  
  *note: due to class time conflict Elizabeth did not cover all study spots
- Michelle: Covered all designated study spots on Floors 1-5 (time: ~30 minutes) and tested a subset excluding Floors 3 and 5 (times: ~15 minutes)

At first, we recorded data using Google Sheets with a separate key mapping `Location ID` to `Location Description` (e.g., `11` for `Area in front of stairs`)

**Pilot Observations & Issues Found**
- Location ID Issue: Needing to cross-reference `Location ID` numbers with the `Location Descriptions` caused extra unnecessary mental load and slowed down the collection process. 
- Enclosed Study Rooms: Initially, we planned to include the study rooms on the second floor that can be booked. However, because these spaces are enclosed, pre-booking is required, and there are multiple study rooms, recording occupancy and noise levels inside them did not align with our focus on open/shared study spaces.
- Office Hour Study Spaces: Initially, we also planned to factor in all of the Office Hour areas on the second floor. Due to time constraints and the notion that these areas are specifically meant for students in those courses at specific tables, we decided they did not align with our focus on general open/shared study spaces.
- Movable Furniture: Students frequently moved chairs between nearby tables. Trying to track exact counts per table was chaotic and created confusion when a chair was moved from one nearby study area to another.
- Seating Types: We initially wanted to track detailed chair/table variations (e.g., 1-person tables, nook chairs, tall plastic chairs, ADA accessibility, sofa spots). However, capturing these granular seating types proved overly complex, time-consuming, and difficult to standardize across collectors.

**Revisions & Professor Consultation**

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

*Revised Data Dictionary (Post-Pilot)*
| Attribute | Type | Description |
| :--- | :--- | :--- |
| `Date` | Temporal | Date of observation |
| `Time` | Temporal | Time of observation |
| `Location` | Categorical | Specific study area within UIC CDRLC |
| `Weather Condition` | Categorical | Description of outside weather |
| `Weather Temperature` | Quantitative | Degree in Fahrenheit |
| `Noise Level` | Quantitative | Average noise level across the span of 30 seconds |
| `Occupancy` | Quantitative | Count number of people |
| `Open Seats` | Quantitative | Count the number of open seats |

**Full Data Collection Strategy**
- Collection Strategy: To increase data points as suggested by our professor, data will be collected over more days and more times throughout the day to notice if there's any signal or pattern across the span of 1-2 days.
- Dataset File: (./Data/Pilot_Collection_Data.csv)

# Task 3: Data description and domain questions

# Task 4: Task abstractions

# Task 5: Visualization sketches

# Task 6: Summarizing

# Task 7: Collaboration process