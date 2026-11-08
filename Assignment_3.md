# Task 1: Implementing interaction

Click [here](Notebooks/Assignment_3.ipynb) to access the static and interactive visualizations.

We chose to create an interactive version of visualization 2 because it benefits the most from interactions that can help uncover variations or underlying patterns. We implemented the interactive visualization using the Plotly package, which has allowed us to incorporate filtering to display data for varying times of day and details-on-demand so that users can hover over a point to view precise details. We expect that filtering by specific times rather than being constrained to using one overall view can help reduce uncertainty by revealing potential variations in study spot reliabilities, allowing more questions to be answered. We also implemented details-on-demand because it's difficult to determine exact values for average availability rate and availability variability (std dev) by relying solely on what users can see. Exact values that get shown via hovering over points provide more precise metrics without creating unnecessary clutter. Furthermore, to make the static visualization more "fair" for comparison to the interactive version, we had to turn what originally was only an aggregated view (all times) into multiple views for different times. We did this to avoid making the static version less informative than the interactive version and to allow users to have nearly the same information necessary to complete the evaluation tasks.

# Task 2: Evaluation design

## Evaluation Question & Hypothesis
* **Evaluation Question:** Does temporal filtering improve users' ability to analyze and compare seat availability reliability patterns across multiple times of day?
* **Hypothesis:** Participants using the interactive visualization will complete reliability analysis faster and with similar or greater accuracy than participants using the static visualization.


## Analytical Task Sets and Expected Answers

To assess user performance while avoiding memorization effects, the evaluation includes two core analytical tasks split into two comparable variant sets ($Set\ A$ and $Set\ B$):

| Analytical Task | Task Variant | Question | Expected Answer |
| :--- | :--- | :--- | :--- |
| **Task 1: Derive Quantitative Difference** | **Variant 1A (Q1)** | At **9 AM**, what is the approximate difference in availability rate between the most reliable location and the least reliable location? | Approximately **16%** (≈ 0.16) |
|  | **Variant 1B (Q2)** | At **3 PM**, what is the approximate difference in availability rate between the most reliable location and the least reliable location? | Approximately **44%** (≈ 0.44) |
| **Task 2: Compare Temporal Changes** | **Variant 2A (Q3)** | Between **9 AM and 1 PM**, which location changes more in terms of availability and variability combined: **1st Floor Lobby Area** or **2nd Floor CS Study Lounge Quiet**? | **2nd Floor CS Study Lounge Quiet** |
|  | **Variant 2B (Q4)** | Between **11 AM and 5 PM**, which location changes more in terms of availability and variability combined: **1st Floor Sandella Cafe** or **4th Floor Study Lounge**? | **1st Floor Sandella Cafe** |

* **Task Set A:** Questions $Q1$ & $Q3$
* **Task Set B:** Questions $Q2$ & $Q4$


## Experimental Variables & Measurements

* **Independent Variable:** Visualization condition with two levels:
  1. **Static:** A static image showing six reliability visualizations for different times of day simultaneously.
  2. **Interactive:** A single reliability visualization that displays one time period at a time, with a dropdown filter and hover tooltips.
* **Quantitative Measurements:**
  1. **Task Accuracy:** Measured by comparing the participant's answer to the correct answer for each task. Responses will be scored as either correct (1) or incorrect (0).
  2. **Task Completion Time (seconds):** Measured using a stopwatch from the moment the moderator finishes reading the question until the participant provides their final answer for that task.
* **Qualitative Measurements:** Noted during the session (e.g., misinterpreting visual encodings, UI navigation friction).


## Experimental Procedure & Participant Script

### Phase 1: Pre-Study Briefing & Setup
1. We will prepare our laptop with the full-screen static image being viewed and the VS Code instance ready for the interactive visualization.
2. We will have a Google Form to record time and accuracy entries. The participant will answer the Google Form on their laptop to a
3. We will also be manually recording time through our phone stopwatch.
3. **Participant Script:**
   > *"Hi! Thank you for participating in our CS 424 visualization evaluation study today. We are looking at seat availability reliability patterns across different study spots in the UIC CDLRC.*
   >
   > *You will answer two analytical questions using a static visualization and two questions using an interactive visualization with a time dropdown menu. I will be timing each task with a stopwatch. There are no right or wrong answers regarding your speed—we are testing the visualization design, not you. Do you have any questions before we begin?"*

# Task 3: Conducting the evaluation
Michelle will be conducting the evaluations and reaching out to people: 

Hello! My friend Elizabeth Ng and I are taking CS 424: Visualization and Visual Analytics, and we're conducting a study comparing static and interactive visualizations. We were wondering if you'd be willing to participate!
It shouldn't take too long. I would just meet up with you and walk you through the study on my laptop.
If you're interested, feel free to let me know what time works best for you! Also, please let me know if you have any questions. Thank you!

### Analytical Task Sets
* **Task Set A:** $Q1$ & $Q2$
* **Task Set B:** $Q3$ & $Q4$

### Participant Counterbalancing Matrix

| Participant ID | Major | Background | 1st Condition | 1st Task Set | 2nd Condition | 2nd Task Set | Group Cell |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **ID 01 (Pilot)** | Computer Eng. (CE) | STEM/Eng | Static | Set A ($Q1, Q2$) | Interactive | Set B ($Q3, Q4$) | Group 1 |
| **ID 11 (Pilot)** | Business | Non-Eng | Interactive | Set A ($Q1, Q2$) | Static | Set B ($Q3, Q4$) | Group 2 |
| | | | | | | | |
| **ID 02** | Computer Eng. (CE) | STEM/Eng | **Static** | Set A ($Q1, Q2$) | **Interactive** | Set B ($Q3, Q4$) | **Group 1** |
| **ID 03** | Computer Eng. (CE) | STEM/Eng | **Static** | Set A ($Q1, Q2$) | **Interactive** | Set B ($Q3, Q4$) | **Group 1** |
| **ID 08** | Biology | Non-Eng | **Static** | Set A ($Q1, Q2$) | **Interactive** | Set B ($Q3, Q4$) | **Group 1** |
| | | | | | | | |
| **ID 04** | Computer Sci. (CS) | STEM/Eng | **Interactive** | Set A ($Q1, Q2$) | **Static** | Set B ($Q3, Q4$) | **Group 2** |
| **ID 09** | Pre-Nursing | Non-Eng | **Interactive** | Set A ($Q1, Q2$) | **Static** | Set B ($Q3, Q4$) | **Group 2** |
| **ID 10** | Kinesiology | Non-Eng | **Interactive** | Set A ($Q1, Q2$) | **Static** | Set B ($Q3, Q4$) | **Group 2** |
| | | | | | | | |
| **ID 05** | Computer Sci. (CS) | STEM/Eng | **Static** | Set B ($Q3, Q4$) | **Interactive** | Set A ($Q1, Q2$) | **Group 3** |
| **ID 06** | Mechanical Eng. (ME)| STEM/Eng | **Static** | Set B ($Q3, Q4$) | **Interactive** | Set A ($Q1, Q2$) | **Group 3** |
| **ID 12** | Nutrition | Non-Eng | **Static** | Set B ($Q3, Q4$) | **Interactive** | Set A ($Q1, Q2$) | **Group 3** |
| | | | | | | | |
| **ID 07** | Computer Sci. (CS) | STEM/Eng | **Interactive** | Set B ($Q3, Q4$) | **Static** | Set A ($Q1, Q2$) | **Group 4** |
| **ID 13** | Business | Non-Eng | **Interactive** | Set B ($Q3, Q4$) | **Static** | Set A ($Q1, Q2$) | **Group 4** |
| **ID 14** | Public Health | Non-Eng | **Interactive** | Set B ($Q3, Q4$) | **Static** | Set A ($Q1, Q2$) | **Group 4** |

---

### Balance
1. **Condition Order Control:** 6 main participants start with **Static** (IDs 02, 03, 08, 05, 06, 12) and 6 main participants start with **Interactive** (IDs 04, 09, 10, 07, 13, 14).
2. **Task Difficulty Control:** Task Set A ($Q1, Q2$) is evaluated under **Static** 6 times and **Interactive** 6 times. Task Set B ($Q3, Q4$) is evaluated under **Static** 6 times and **Interactive** 6 times.
3. **Stratified Major Control:** Each of the 4 group cells contains a balanced mix of STEM/Engineering and Non-Engineering majors (3 STEM and 3 Non-STEM in each condition order block), eliminating domain background as a confounding factor.


# Task 4: Quantitative analysis


# Task 5: Reflection and recommendations


