# Task 1: Implementing interaction

Click [here](Notebooks/Assignment_3.ipynb) to access the static and interactive visualizations.

We chose to create an interactive version of visualization 2 because it benefits the most from interactions that can help uncover variations or underlying patterns. We implemented the interactive visualization using the Plotly package, which allows us to incorporate filtering to display data for varying times of day and details-on-demand so that users can hover over a point to view precise details. 
We expect filtering by specific times rather than being constrained to using one overall view will help reduce uncertainty by revealing potential variations in study spot reliabilities, allowing more questions to be answered. We also implemented details-on-demand because it is difficult to determine exact values for average availability rate and availability variability (std dev) by relying solely on what users can see. Exact values that get shown via hovering over points provide more precise metrics without creating unnecessary clutter. 
Furthermore, to make the static visualization more "fair" for comparison to the interactive version, we had to turn what originally was only an aggregated view (all times) into multiple views for different times. We did this to avoid making the static version less informative than the interactive version and to allow users to have nearly the same information necessary to complete the evaluation tasks.

# Task 2: Evaluation design

## Evaluation Question & Hypothesis
* **Evaluation Question:** Does temporal filtering improve users' ability to analyze and compare seat availability reliability patterns across multiple times of day?
* **Hypothesis:** Participants using the interactive visualization will complete reliability analysis faster and with similar or greater accuracy than participants using the static visualization.
* **Domain Connection:** These tasks directly extend our Assignment 2 domain goal of helping UIC students evaluate study spot availability rates and variability patterns across different hours at the CDLRC.

## Analytical Task Sets and Expected Answers

To assess user performance while avoiding memorization effects, the evaluation includes two core analytical tasks split into two comparable variant sets ($Set\ A$ and $Set\ B$):

| Analytical Task | Task Variant | Question | Expected Answer | Scoring & Tolerance |
| :--- | :--- | :--- | :--- | :--- |
| **Task 1: Derive Quantitative Difference** | **Variant 1A (Q1)** | At **9 AM**, what is the approximate difference in availability rate between the most reliable location and the least reliable location? | Approximately **16%** (≈ 0.16) | Correct (1) if within 11%–21% ($\pm 5\%$) |
| | **Variant 1B (Q2)** | At **3 PM**, what is the approximate difference in availability rate between the most reliable location and the least reliable location? | Approximately **44%** (≈ 0.44) | Correct (1) if within 39%–49% ($\pm 5\%$) |
| **Task 2: Compare Temporal Changes** | **Variant 2A (Q3)** | Between **9 AM and 1 PM**, which location changes more in terms of availability and variability combined: **1st Floor Lobby Area** or **2nd Floor CS Study Lounge Quiet**? | **2nd Floor CS Study Lounge Quiet** | Binary ($1 = \text{Correct}, 0 = \text{Incorrect}$) |
| | **Variant 2B (Q4)** | Between **11 AM and 5 PM**, which location changes more in terms of availability and variability combined: **1st Floor Sandella Cafe** or **4th Floor Study Lounge**? | **1st Floor Sandella Cafe** | Binary ($1 = \text{Correct}, 0 = \text{Incorrect}$) |

### Counterbalancing

To reduce learning effects and ensure that task difficulty is not associated with a specific visualization condition, the four task variants are divided into two task sets:

* **Task Set A:** Q1 and Q3
* **Task Set B:** Q2 and Q4

Participants will complete one task set using the static visualization and the other task set using the interactive visualization. Participants will be assigned to one of four groups:

| Group | First Condition | First Task Set | Second Condition | Second Task Set |
| :--- | :--- | :--- | :--- | :--- |
| Group 1 | Static | Set A (Q1, Q3) | Interactive | Set B (Q2, Q4) |
| Group 2 | Interactive | Set A (Q1, Q3) | Static | Set B (Q2, Q4) |
| Group 3 | Static | Set B (Q2, Q4) | Interactive | Set A (Q1, Q3) |
| Group 4 | Interactive | Set B (Q2, Q4) | Static | Set A (Q1, Q3) |

This counterbalancing approach ensures that:
1. Half of the participants use the static visualization first, while the other half use the interactive visualization first.
2. Both task sets are completed under the static and interactive conditions an equal number of times.
3. No task variant is consistently associated with a particular visualization condition.
4. Potential learning and order effects are reduced.

## Experimental Variables & Measurements

* **Handling Invalid & Timed-Out Tasks: **
    * **Time-Out Cap:** A maximum time limit of 3 minutes (180 seconds) per task set is enforced (for a total maximum testing time of 6 minutes across both conditions). If a participant exceeds 3 minutes on a single task set, that set is marked as timed out, its time is logged as 180 seconds, and accuracy for those tasks is scored as 0.
    * **Incorrect Responses:** Numerical responses outside the defined range arescored as 0 (incorrect), but their recorded completion time will remain to keep individual-level measurements saved for Task 4.

* **Independent Variable:** Visualization condition with two levels:
  1. **Static:** A static image showing six reliability visualizations for different times of day simultaneously.
  2. **Interactive:** A single reliability visualization that displays one time period at a time, with a dropdown filter and hover tooltips.

* **Quantitative Measurements:**
  1. **Task Accuracy:** Measured by comparing the participant's answer to the correct answer for each task. Responses will be scored as either correct (1) or incorrect (0).
  2. **Task Completion Time (seconds):** Measured using a stopwatch from the moment the moderator finishes reading the question until the participant provides their final answer for that task.
  3. **Confidence Rating (1-10):** After completing each task, participants will rate how confident they are in their answer on a scale from 1 (not confident at all) to 10 (extremely confident).
  4. **Perceived Difficulty:** After completing each task, participants will rate how difficult they found the task on a scale from 1 (very easy) to 10 (very difficult).
* **Qualitative Measurements:**
  1. **Task Strategy and Explanation:** After each task, participants will briefly explain how they determined their answer and describe their approach to solving the task.

## Experimental Procedure & Participant Instructions

### Phase 1: Pre-Study Briefing and Setup

1. Prepare the static visualization and interactive visualization on a laptop before the participant arrives.
2. Open the Google Form containing the task questions, confidence ratings, difficulty ratings, and open-ended response fields.
3. Prepare a stopwatch to record task completion times.
4. Assign the participant to one of the four counterbalancing groups.

**Participant Script**

> Hi! Thank you for participating in our CS 424 visualization evaluation study. This study examines how different visualization designs support the analysis of seat availability reliability patterns across study spaces in the UIC CDLRC.
>
> You will answer four questions in total: two using a static visualization and two using an interactive visualization. Depending on your assigned group, you may use either the static or interactive visualization first.
>
> The questions will be provided through a Google Form. Please enter your answers directly into the form.
>
> For each visualization condition, you will be given two questions. After I finish reading both questions, I will start a timer. Please answer both questions as accurately and quickly as possible. The timer will stop once you have completed both questions.
>
> After completing the two questions, you will be asked to complete a brief survey. These responses will not be included in the recorded task completion time.
>
> This study is evaluating the visualizations, not your performance. You may ask questions about the study procedure before we begin; however, once the tasks start, I will not provide hints, answer clarifying questions about the tasks, or assist in finding the answers.
>
> Do you have any questions before we begin?

### Phase 2: Task Administration

1. Present the first visualization condition according to the participant's assigned counterbalancing group.
2. Display the corresponding task set page in the Google Form.
3. Read both questions in the task set aloud.
4. Start the stopwatch immediately after both questions have been read.
5. The participant completes and submits answers to both questions.
6. Stop the stopwatch once the participant has completed both questions.
7. Record the task completion time for the task set.
8. Have the participant complete the post-condition survey page, including:
   * Confidence rating (1-10)
   * Difficulty rating (1-10)
   * Brief explanation of how they arrived at their answers
9. Present the second visualization condition.
10. Repeat Steps 2-8 for the remaining task set.
11. Thank the participant for their participation.

#### Task Completion Time

Task completion time will be measured once per task set. Timing begins after the moderator finishes reading both questions in the task set and ends after the participant has completed both questions. Confidence ratings, difficulty ratings, and qualitative explanations are collected afterward and are not included in the recorded task completion time.

### Recording Results NOTE: Might modify the wording later but same idea

Participant responses will be collected through a Google Form. Each participant will be assigned a unique participant ID to organize and track responses throughout the study.

For each task set, the following information will be recorded:

* Task completion time (seconds)
* Answers to both task questions
* Task accuracy (correct/incorrect)
* Confidence rating (1-10)
* Difficulty rating (1-10)
* Open-ended explanation of how the participant arrived at their answers

Task completion times will be recorded manually by the moderator using a stopwatch. All participant responses entered through the Google Form will automatically populate a Google Sheets spreadsheet. After data collection is complete, the spreadsheet will be exported as a CSV file for analysis. Accuracy scores will be determined by comparing participant responses to the expected answers defined in the evaluation design.

# Task 3: Conducting the evaluation
Click [here] (https://forms.gle/xLU8eAzZ1AfFh8HZ6) to access the Google Form for the study group 1.
Click [here] (https://forms.gle/kZneG6HJMAcukAAm7) to access the Google Form for the study group 2.
Click [here] (https://forms.gle/owgsHrmeq6puK73v9) to access the Google Form for the study group 3.
Click [here] (https://forms.gle/1Ko2Qe4qF2Z9o1fu7) to access the Google Form for the study group 4.


### Pilot Evaluation Summary
TO BE ADDED
91: we didn't explain reliability, forgot to explain how the visualization works. didn't account for question udnerstanding (in question 2). didn't have participant fill out form first with info. google form did not have questions so split screen google doc, now we have four separate google forms.
90: struggled to understand the question and struggled to understand what to do with the graphs (will now explain and also explain the quadrants) 

### Participant Counterbalancing Matrix

| Participant ID | Major | Background | 1st Condition | 1st Task Set | 2nd Condition | 2nd Task Set | Group Cell |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **ID 90 (Pilot)** | Computer Eng. (CE) | STEM/Eng | Static | Set A (**Q1, Q3**) | Interactive | Set B (**Q2, Q4**) | Group 1 |
| **ID 91 (Pilot)** | Business | Non-Eng | Interactive | Set A (**Q1, Q3**) | Static | Set B (**Q2, Q4**) | Group 2 |
| | | | | | | | |
| **ID 01** | Computer Eng. (CE) | STEM/Eng | **Static** | Set A (**Q1, Q3**) | **Interactive** | Set B (**Q2, Q4**) | **Group 1** |
NOTE ID 02 DONE!
| **ID 02** | Computer Eng. (CE) | STEM/Eng | **Static** | Set A (**Q1, Q3**) | **Interactive** | Set B (**Q2, Q4**) | **Group 1** |
NOTE ID 02 DONE!
| **ID 03** | Biology | Non-Eng | **Static** | Set A (**Q1, Q3**) | **Interactive** | Set B (**Q2, Q4**) | **Group 1** |
NOTE ID 03 DONE!
| | | | | | | | |
| **ID 04** | Computer Sci. (CS) | STEM/Eng | **Interactive** | Set A (**Q1, Q3**) | **Static** | Set B (**Q2, Q4**) | **Group 2** |
NOTE ID 04 DONE!
| **ID 05** | Pre-Nursing | Non-Eng | **Interactive** | Set A (**Q1, Q3**) | **Static** | Set B (**Q2, Q4**) | **Group 2** |
| **ID 06** | Kinesiology | Non-Eng | **Interactive** | Set A (**Q1, Q3**) | **Static** | Set B (**Q2, Q4**) | **Group 2** |
| | | | | | | | |
| **ID 07** | Computer Sci. (CS) | STEM/Eng | **Static** | Set B (**Q2, Q4**) | **Interactive** | Set A (**Q1, Q3**) | **Group 3** |
NOTE ID 07 DONE!

| **ID 08** | Mechanical Eng. (ME) | STEM/Eng | **Static** | Set B (**Q2, Q4**) | **Interactive** | Set A (**Q1, Q3**) | **Group 3** |
| **ID 09** | Nutrition | Non-Eng | **Static** | Set B (**Q2, Q4**) | **Interactive** | Set A (**Q1, Q3**) | **Group 3** |
NOTE: ID 09 DONE
| | | | | | | | |
| **ID 10** | Computer Sci. (CS) | STEM/Eng | **Interactive** | Set B (**Q2, Q4**) | **Static** | Set A (**Q1, Q3**) | **Group 4** |
NOTE ID 10 DONE!
| **ID 11** | Business | Non-Eng | **Interactive** | Set B (**Q2, Q4**) | **Static** | Set A (**Q1, Q3**) | **Group 4** |
NOTE ID 11 DONE1 change stem/end to just non-eng
| **ID 12** | Public Health | Non-Eng | **Interactive** | Set B (**Q2, Q4**) | **Static** | Set A (**Q1, Q3**) | **Group 4** |

---

### Balance

1. **Condition Order Control:** Six participants start with the **Static** condition (IDs 01-03, 07-09), while six participants start with the **Interactive** condition (IDs 04-06, 10-12).

2. **Task Set Balance:** Task Set A (Q1, Q3) is completed under the **Static** condition three times and under the **Interactive** condition three times. Task Set B (Q2, Q4) is completed under the **Static** condition three times and under the **Interactive** condition three times.

3. **Background Balance:** STEM/Engineering and Non-STEM participants are distributed across all four groups to reduce the influence of academic background on task performance.

# Task 4: Quantitative analysis


# Task 5: Reflection and recommendations


