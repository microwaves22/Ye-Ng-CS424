# Task 1: Implementing interaction

Click [here](Notebooks/Assignment_3.ipynb) to access the static and interactive visualizations.

We chose to create an interactive version of visualization 2 because it benefits the most from interactions that can help uncover variations or underlying patterns. We implemented the interactive visualization using the Plotly package, which has allowed us to incorporate filtering to display data for varying times of day and details-on-demand so that users can hover over a point to view precise details. We expect that filtering by morning, afternoon, and all times can help reduce uncertainty by revealing potential variations in study spot reliabilities, allowing more questions to be answered. We also implemented details-on-demand because it's difficult to determine exact values for average availability rate and availability variability (std dev) by relying solely on what users can see. Exact values that get shown via hovering over points provide more precise metrics without creating unnecessary clutter. Furthermore, to make the static visualization more "fair" for comparison to the interactive version, we had to turn what originally was only an aggregated view (all times) into multiple views with morning and afternoon created as well. We did this to avoid making the static version less informative than the interactive version and to allow users to have nearly the same information necessary to complete the evaluation tasks.

# Task 2: Evaluation design

Ideas..
Which location shows the largest change in reliability between Morning and All Time?
Which location shows the largest change in reliability between Afternoon and All Time?

Estimate the availability rate of the 2nd Floor CS Study Lounge Collaborative during the Morning period.
Estimate the availability rate of the 2nd Floor CS Study Lounge Collaborative during the Afternoon period.




Improved ideas..???
Task Family 1: Quantitative Comparison

Variant A:
Estimate the difference in average availability rate between the 1st Floor CS Study Lounge and 4th Floor Study Lounge during the Morning period.

Variant B:
Estimate the difference in average availability rate between the 1st Floor CS Study Lounge and 4th Floor Study Lounge during the Afternoon period.

Analytical ability:
Comparing quantitative values.

Data subset:
Morning vs Afternoon.

Task Family 2: Temporal Change Identification

Variant A:
Which location shows the largest change in reliability between Morning and All Times?

Variant B:
Which location shows the largest change in reliability between Afternoon and All Times?

Analytical ability:
Detecting and comparing changes.

Data subset:
Morning vs All Times versus Afternoon vs All Times.


# Task 3: Conducting the evaluation


# Task 4: Quantitative analysis


# Task 5: Reflection and recommendations


