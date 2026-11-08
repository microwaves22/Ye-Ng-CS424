# Task 1: Implementing interaction

Click [here](Notebooks/Assignment_3.ipynb) to access the static and interactive visualizations.

We chose to create an interactive version of visualization 2 because it benefits the most from interactions that can help uncover variations or underlying patterns. We implemented the interactive visualization using the Plotly package, which has allowed us to incorporate filtering to display data for varying times of day and details-on-demand so that users can hover over a point to view precise details. We expect that filtering by specific times rather than being constrained to using one overall view can help reduce uncertainty by revealing potential variations in study spot reliabilities, allowing more questions to be answered. We also implemented details-on-demand because it's difficult to determine exact values for average availability rate and availability variability (std dev) by relying solely on what users can see. Exact values that get shown via hovering over points provide more precise metrics without creating unnecessary clutter. Furthermore, to make the static visualization more "fair" for comparison to the interactive version, we had to turn what originally was only an aggregated view (all times) into multiple views for different times. We did this to avoid making the static version less informative than the interactive version and to allow users to have nearly the same information necessary to complete the evaluation tasks.

# Task 2: Evaluation design

## Evaluation Question
Does temporal filtering improve users' ability to analyze seat availability reliability patterns across different time periods?

## Hypothesis
Participants using the interactive visualization will complete temporal analysis tasks faster and with similar or greater accuracy than participants using the static visualization because temporal filtering allows users to focus on one period at a time.

## Visualization Tasks
| Analytical Task | Static Condition | Interactive Condition |
|----------------|----------------------------------------|--------------------------------------------|
| Derive a quantitative difference | What is the approximate difference in availability rate between the most reliable location and the least reliable location during the Morning period? | What is the approximate difference in availability rate between the most reliable location and the least reliable location during the Afternoon period? |
| Compare temporal changes | Which location shows the largest change in reliability between Morning and Afternoon? | Which location shows the smallest change in reliability between Morning and Afternoon? |



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


