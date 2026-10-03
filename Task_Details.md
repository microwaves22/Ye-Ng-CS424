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

For the Pilot test we split and did them both so we could gauge how much time it took to collect data. We collected Time, we originally put it on Google sheets and had separate sheet with area and location ID, but from it we realized it was hard to remember the location id and the location. we collected noise level (min, mean, max), total number of people. We did the following areas 11	Area in front of stairs
ID  Location Description
12	Area in front of the lecture/conference rooms
13	Area in front of the Sandella cafe
14	CS Study Lounge Area
15	Area right of elevator
21	CS Study Lounge Quiet Area
22	CS Study Lounge Collaborative Area
23	Area right of elevator
24	Booked study rooms
31	Area right of elevator
41	Study lounge
42	Area right of elevator
43	Area between professor offices
51	Area right of elevator
We collected at 11 am 9/17/2026 in the UIC CDLRC Building. 

some notes from the pilot: We will continue recording noise level for each observation
20 mins for Elizabeth (all spots floors 1-2)
30 mins for Michelle all areas (1,2,3,4,5)
15 minutes for Michelle (all spots in the CS building excluding floors 3 and 5 and the private study rooms)
Don’t include private study rooms. They’re already enclosed rooms that people book in advance
To factor in students moving chairs we’ve concise super close proximity study areas together
Note: where chairs are frequently seen moved. 
In theory, the total number of chairs/tables stays the same within this space, even if someone moves furniture around

we decided to schedule a meeting with our professor to discuss. We were planning to incorporate chair differeces and seating types, but didn't because we couldn't figure it out and were just waiting until we met up with our professor and later after the meeting we determined it would be best to not factor seating types/arrangements. 

Post pilot but pre professor meeting: Attribute
Type
Description
Date
Temporal
Date of observation
Time
Temporal
Time of observation
Location
Categorical
Location of the study area
Weather Condition
Categorical
Description of outside weather
Weather Temperature
Quantitative
Degree in Fahrenheit
Noise Level
Quantitative
Average noise level across the span of 30 seconds
Occupancy
Quantitative
Total number of occupants at a location
1 Person Table Availability
Quantitative
Number of FULLY open tables for 1
2 People Table Availability 
Quantitative
Number of FULLY open tables for 2
3+ People Table Availability
Quantitative
Number of FULLY open tables for 3+
Nook Chair Availability
Quantitative
Number of open seats
Regular Plastic Chair
Quantitative
Number of open seats
Tall Plastic Chair (Not ADA friendly)
Quantitative
Number of open seats
Sofa Spot Availability
Quantitative
Number of empty soft seats (Note: each sofa holds 2 people)
Outlet 
Quantitative
Number of Outlets in a Location (2 holes = 1 outlet; 4 holes = 2 outlets)
Window Access
Categorical
Is there a to sunlight (it doesn’t count if window is the roof or if it’s into the building)
1 Person Table Amount
Quantitative
Number of tables in a location
2 People Table Amount
Quantitative
Number of tables in a location
3+ People Table Amount
Quantitative
Number of tables in a location
Nook Chair Amount
Quantitative
Number of chairs in a location
Regular Plastic ChairAmount
Quantitative
Number of chairs in a location
Tall Plastic Chair Amount (Not ADA friendly)
Quantitative
Number of chairs in a location
Sofa Spot Amount
Quantitative
Number of chairs in a location



# Task 3: Data description and domain questions

# Task 4: Task abstractions

# Task 5: Visualization sketches

# Task 6: Summarizing

# Task 7: Collaboration process