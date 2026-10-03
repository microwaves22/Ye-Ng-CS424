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
| Attribute | Type | Description | Example |
|------------------------------------|--------------|---------------------------------------------------------------|---------------------------|
| date                               | Temporal     | Date of observation                                           | 09/17/2026                |
| time                               | Temporal     | Time of observation                                           | 13:00                     |
| location                           | Categorical  | Location of the study area                                    | 2nd Floor CS Study Lounge |
| weather_condition                  | Categorical  | Description of the outside weather                            | Sunny                     |
| weather_temperature                | Quantitative | Degree in Fahrenheit                                          | 75                        |
| noise_level                        | Quantitative | Average noise level in decibels across the span of 30 seconds | 81.2                      |
| occupancy                          | Quantitative | Total number of occupants at a location                       | 15                        |
| single-person_tables               | Quantitative | Number of fully open tables for 1                             | 6                         |
| two-person_tables                  | Quantitative | Number of fully open tables for 2                             | 3                         |
| tables_for_multiple_people         | Quantitative | Number of fully open tables for 3+ people                     | 5                         |
| nook_chair_availability            | Quantitative | Number of open nook seats                                     | 4                         |
| regular_plastic_chair_availability | Quantitative | Number of open regular pastlic seats                          | 8                         |
| tall_plastic_chair_availability    | Quantitative | Number of open tall plastic seats                             | 3                         |
| sofa_spot_availability             | Quantitative | Number of empty soft seats                                    | 1                         |
| outlets                            | Quantitative | Number of outlets at a location                               | 4                         |
| window_access                      | Categorical  | Is there access to direct sunlight?                           | Yes                       |
| number_of_single-person_tables     | Quantitative | Number of tables for 1 at a location                          | 5                         |
| number_of_two-person_tables        | Quantitative | Number of tables for 2 at a location                          | 4                         |
| number_of_multiple_people_tables   | Qunatitative | Number of tables for 3+ people at a location                  | 4                         |
| number_of_nook_chairs              | Quantitative | Number of nook seats at a location                            | 7                         |
| number_of_regular_plastic_chairs   | Quantitative | Number of regular plastic chairs at a location                | 4                         |
| number_of_tall_plastic_chairs      | Quantitative | Number of tall plastic chairs at a location                   | 8                         |
| number_of_sofa_spots               | Quantitative | Number of sofa spots at a location                            | 2                         |                                      


# Task 2: Pilot and data collection

# Task 3: Data description and domain questions

# Task 4: Task abstractions

# Task 5: Visualization sketches

# Task 6: Summarizing

# Task 7: Collaboration process