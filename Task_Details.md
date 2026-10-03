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
- Location ID Issue: Needing to cross-reference `Location ID` numbers with the `Location Descriptions` caused extra unnecessary mental load and slowed us down. 
- Enclosed Study Rooms: Initially we planned to include the study rooms on the second floor that can be booked. However, because these spaces are enclosed, pre-booking is required, and there are multiple of the study rooms, recording the occupancy and noise levels inside them did not align with our focus on open/shared study spaces.
- Office Hour Study Spaces: Initially we also planned to factor in all of the Office Hour areas on the second floor, but due to time and also the notion that it is meant for students in the courses at specific tables, we decided it did not align with our focus on open/shared study spaces.
- Movable Furniture: students frequently moved chairs between nearby tables. Trying to track exact counts per table was chaotic, and also affected if two separate study areas we nearby and one chair was moved from one study area to another. Thus we decided to create bigger study areas by combining areas where furniture could easily be moved and change to counting open seats and people sitting.
- Seating Types: We initially wanted to track chair/table variations (e.g., 1-person tables, nook chairs, tall plastic chairs, ADA accessibility, sofa spots). However, caputring these granular seating types was overly complex and difficultto standardize.

**Revisions & Professor Consulation**
Following our pilot, we scheduled a meeting with our professor to discuss issues that arose, how to simplify our attributes without loosing data, and more. 

Based on our pilot findings and feedback from our professor we decided to make the following changes
1. Remove study rooms and Office hour study areas
2. simplified seating and furniture  to seat avaialble and people there. 
3. make zones bigger by merging close study areas.
4. replaced location Id system with direct location description.
5. removed floors 3 and 5 because it was just a small area next to elevator and did not seem to provide useful as it was one table and 2-3 seating. 


### Revised Data Dictionary (Post-Pilot)

| Attribute | Type | Description |
| :--- | :--- | :--- |
| `Date` | Temporal | Date of observation |
| `Time` | Temporal | Time of observation |
| `Location` | Categorical | Specific study area within UIC CDRLC |
| `Weather Condition` | Categorical | External weather description |
| `Weather Temperature` | Quantitative | Outdoor temperature in °F |
| `Noise Level` | Quantitative | Average noise level across a 30-second interval |
| `Occupancy` | Quantitative | Total number of people occupying the space |
| `Table Availability` | Quantitative | Number of open, available tables |
| `Seat Availability` | Quantitative | Number of available open seats |
| `Outlet Access` | Quantitative | Number of usable power outlets (2 sockets = 1 outlet) |
| `Window / Natural Light` | Categorical | Presence of direct natural sunlight (excluding interior glass or skylights) |

---


# Task 3: Data description and domain questions

# Task 4: Task abstractions

# Task 5: Visualization sketches

# Task 6: Summarizing

# Task 7: Collaboration process