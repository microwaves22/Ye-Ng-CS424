# Task 1: Implementing interaction

Click [here](Notebooks/Assignment_3.ipynb) to access the static and interactive visualizations.

We chose to create an interactive version of visualization 2 because it benefits the most from interactions that can help uncover variations or underlying patterns. We implemented the interactive visualization using the Plotly package, which has allowed us to incorporate filtering to display data for varying times of day and details-on-demand so that users can hover over a point to view precise details. We expect that filtering by morning, afternoon, and all times can help reduce uncertainty by revealing potential variations in study spot reliabilities, allowing more questions to be answered. We also implemented details-on-demand because it's difficult to determine exact values for average availability rate and availability variability (std dev) by relying solely on what users can see. Exact values that get shown via hovering over points provide more precise metrics without creating unnecessary clutter. Furthermore, to make the static visualization more "fair" for comparison to the interactive version, we had to turn what originally was only an aggregated view (all times) into multiple views with morning and afternoon created as well. We did this to avoid making the static version less informative than the interactive version and to allow users to have nearly the same information necessary to complete the evaluation tasks.

# Task 2: Evaluation design

## Evaluation Question
Does temporal filtering improve users' ability to analyze seat availability reliability patterns across different time periods?

## Hypothesis
Participants using the interactive visualization will complete temporal analysis tasks faster and with similar or greater accuracy than participants using the static visualization because temporal filtering allows users to focus on one period at a time.

## Analytical Task 1
Derive a quantitative difference.
### Static Condition
What is the approximate difference in availability rate between the most reliable location and the least reliable location during the Morning period?
### Interactive Condition
What is the approximate difference in availability rate between the most reliable location and the least reliable location during the Afternoon period?

## Analytical Task 2
Compare temporal changes.
### Static Condition
Which location shows the largest change in reliability between Morning and All Times?
### Interactive Condition
Which location shows the largest change in reliability between Afternoon and All Times?



# Task 3: Conducting the evaluation


# Task 4: Quantitative analysis


# Task 5: Reflection and recommendations


