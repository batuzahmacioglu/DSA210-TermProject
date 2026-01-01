# Project Title: Home Advantage in European Football (2000-2024)
________________________________________
## Motivation
Football fans often claim that home teams perform better, but the strength and consistency of this advantage may not be the same across different eras. Over the past 25 years, European football has undergone major shifts including increased globalization, tactical changes, improved travel conditions, and the introduction of technologies such as VAR. These changes raise an important question: has home advantage in domestic European leagues increased, decreased, or remained stable over time? By analyzing 230,000+ matches from European Domestic Football Leagues (2000-2024), this project aims to measure long-term trends in home advantage.
________________________________________
## Data Source
This project uses a publicly available dataset containing match results from multiple European domestic leagues between 2000 and 2024. The dataset includes:
Match date
Home and away teams
Full-time scores
Match statistics
League/Division identifier
Elo ratings
This dataset is large (230,000+ matches) and contains all necessary variables to measure home advantage over time.
________________________________________
## Methodology
Data Collection:
Load and inspect the dataset containing matches from European domestic leagues between 2000 and 2024.

Data Cleaning:
Convert match dates into a usable format, extract the season or year, remove duplicates if present, and ensure that home/away goals and results are correctly parsed.

Exploratory Data Analysis (EDA):
Compute the home-win rate for each season between 2000 and 2024. Summarize trends by year and create initial visualizations such as line plots showing how the home-win rate changes over time. Identify any periods that show noticeable increases or decreases.

Statistical Testing:
Perform statistical tests to examine how home advantage changes across different time periods. This includes comparing home-win rates between earlier and more recent seasons, as well as testing whether the overall trend over time is statistically significant.

Time-Based Modeling:
Fit a simple regression model using year as a predictor for home wins to determine whether home advantage shows a significant upward or downward trend.

Visualization:
Create clear visualizations, including seasonal trend lines, bar charts comparing different eras, and summary plots that support the statistical findings.

Reporting:
Summarize results, interpret statistical patterns, relate trends to developments in modern football, and discuss potential limitations or future extensions of the analysis.
________________________________________
## Expected Outcomes
By analyzing home-win rates across European football leagues between 2000 and 2024, I expect to observe that home advantage has changed over time rather than remaining constant. It is possible that home advantage has gradually decreased due to factors such as improved refereeing consistency (with the help of technological advances such as VAR), tactical evolution, and better travel conditions for away teams. However, certain periods may show stronger or weaker home effects depending on changes in competitive balance and football environments. The results will reveal whether there is a clear long-term trend, stability, or fluctuation in home advantage across seasons.
________________________________________

## Exploratory Data Analysis (EDA)
<img width="1098" height="544" alt="Ekran Resmi 2025-11-30 17 30 48" src="https://github.com/user-attachments/assets/615b6370-2094-4f2a-87fa-3f5ff6082591" />
This plot shows how the home win rate has changed over the last 25 years across major European domestic leagues.

Key Insights
Home win rate starts at around 48–49% in 2000, the highest point in the dataset.
There is a clear and steady decline throughout the 2000s and 2010s.
The most dramatic drop occurs in 2020, when matches were played without fans due to COVID-19 restrictions.
After 2020, home win rates partially recover but never return to pre-2010 levels.
Overall, the long-term trend reveals a significant weakening in home advantage.

What This Shows
This graph provides strong visual evidence that home advantage has declined over time, and the 2020 no-fans season had a major impact. It supports the idea that:
crowd presence matters,tactical and travel improvements reduce home bias, and football is becoming more balanced between home and away teams.

<img width="1117" height="562" alt="Ekran Resmi 2025-11-30 17 37 39" src="https://github.com/user-attachments/assets/8056e327-9e13-4b66-b400-7562c71a0356" />
This visualization shows the average goal difference (home goals minus away goals) for every season from 2000 to 2024.

Key Insights
In the early 2000s, home teams typically outscored away teams by 0.45–0.50 goals per match, indicating a strong home advantage.
Across the next two decades, this margin steadily declines, reflecting a reduction in the goal-scoring dominance of home teams.
Just like the win-rate trend, the sharpest drop occurs in 2020, where goal difference reaches the lowest value in the entire dataset.
After 2020, there is a partial recovery, but home teams still maintain a noticeably smaller margin than in earlier years.

What This Shows
This plot reinforces the earlier conclusion:
Home advantage is weakening over time, not only in match outcomes but also in scoring performance. The COVID-19 no-fan period had a measurable impact on home scoring, and long-term trends suggest:
tactical evolution,
better preparation for away matches,
improved travel conditions,
and neutral officiating technologies (e.g., VAR)
all contribute to the shrinking home–away performance gap.

<img width="1037" height="549" alt="Ekran Resmi 2025-11-30 17 40 46" src="https://github.com/user-attachments/assets/e5bfaf3f-99c9-40c7-8298-6cb4330c33a2" />
2024.
This plot compares the scoring distribution of home and away teams across all matches from 2000 to 2024.

Key Insights
The peaks at 0 goals and 1 goal appear for both home and away teams.
Away teams score exactly 1 goal slightly more frequently than home teams — visible from the slightly higher blue peak at 1.
Home teams, however, score 2 or more goals more often, shown by the higher orange peaks at 2, 3, and 4 goals.
The long right tail for home teams indicates that they are more likely to produce high-scoring matches (3+ goals).

What This Shows
This scoring distribution reveals a balanced but still meaningful difference:
Away teams tend to score low consistent amounts (mostly 0 or 1).
Home teams produce more high-scoring outcomes, raising their overall scoring average.
This pattern supports the presence of home advantage:
Even though away teams often score one goal, home teams compensate by scoring more frequently in multi-goal matches.
________________________________________

## Hypothesis Testing

<img width="1132" height="421" alt="Ekran Resmi 2025-11-30 17 44 34" src="https://github.com/user-attachments/assets/bdbcfdd8-b545-48b7-ad7c-80df364092fb" />
Hypothesis Test 1 — Do Home Teams Score More Than Away Teams?
This hypothesis test compares the average number of goals scored by home teams vs. away teams across all matches from 2000 to 2024.
Test Details
Null Hypothesis (H₀): Home teams and away teams score the same number of goals.
Alternative Hypothesis (H₁): Home teams score more goals than away teams (home advantage exists).
A Welch’s t-test (unequal variances) was used because it is more robust for large, real-world datasets.
Rows with missing values were removed to avoid invalid calculations.
Results
T-statistic: 96.13
P-value: 0.0
Because the p-value is effectively zero, far below the 0.05 significance threshold:
Conclusion
There is extremely strong statistical evidence that home teams score more goals on average than away teams.
This confirms the presence of a baseline home advantage in European football.

<img width="1130" height="455" alt="Ekran Resmi 2025-11-30 17 45 21" src="https://github.com/user-attachments/assets/d6560291-a5b3-4c61-85a6-c486a145a7da" />
Hypothesis Test 2 — Has Home Advantage Changed Over Time?
This test examines whether the strength of home advantage has shifted between earlier and more recent years.
To do this, the data was split into two time periods:
Early Period: 2000–2010
Late Period: 2011–2024
We compare the average HomeWin variable (1 = home win, 0 = otherwise) between these two periods using a Welch’s t-test.
Test Details
Null Hypothesis (H₀): There is no difference in home advantage between the early and late periods.
Alternative Hypothesis (H₁): Home advantage has changed over time (early vs. late periods differ).
Missing values were removed before running the test.
Results
T-statistic: 7.81
P-value: 5.86 × 10⁻¹⁵
The p-value is far below the 0.05 threshold, indicating an extremely significant difference between the two periods.
Conclusion
Home advantage has changed significantly over the last 25 years — specifically, it has declined.
This statistical result matches the visual trends observed in the EDA:
Lower home win rates
Decreasing goal differences
The 2020 no-fan season accelerating the drop
Together, these results confirm that home advantage has weakened in modern European football.
________________________________________

### Hypothesis Test Results (Summary)


| Test | Comparison | Metric | Statistical Test | Test Statistic | p-value | Conclusion |
|------|------------|--------|------------------|---------------:|--------:|------------|
| Test 1 | Home vs Away teams | Goals scored | Welch’s t-test | 96.13 | < 0.001 | Home teams score significantly more goals |
| Test 2 | 2000–2010 vs 2011–2024 | Home win rate | Welch’s t-test | 7.81 | 5.86×10⁻¹⁵ | Home advantage changed significantly over time |


________________________________________

## Findings Summary

1. Trends in Home Advantage (2000–2024)
Home win rates have declined steadily over the past 25 years.
The home goal difference also shows a consistent downward trend.
A major drop appears in 2020 (COVID no-fan matches), confirming that crowd presence plays a role in home advantage.
After 2020, home advantage partially recovers but remains below early-2000s levels.
2. Goal Distribution
Away teams score exactly one goal slightly more often than home teams.
But home teams score 2+ goals more frequently.
Overall, home teams maintain a higher average scoring rate, supporting the existence of home advantage.
3. Hypothesis Testing Results
Test 1 — Home vs Away Scoring
Home teams score significantly more goals than away teams.
p-value ≈ 0 → strong evidence of home advantage.
Test 2 — Early vs Late Years
Home advantage has significantly changed over time (declined).
p-value ≈ 5.8e-15 → very strong evidence.
4. Conclusion
Home advantage in European football has weakened but still exists.
The decline is statistically significant and visually supported by multiple metrics.
Changes in travel, tactics, officiating, and especially the 2020 fan-free season likely contributed to this trend.
________________________________________

## Machine Learning 

A supervised machine learning approach was applied to the dataset to predict match outcomes.  
Specifically, the task was framed as a **binary classification problem**: predicting whether the home team wins a match.

### Problem Definition
- **Objective:** Predict whether the home team wins a given match
- **Type:** Binary classification

### Target Variable
- **HomeWin**
  - 1 if the home team scores more goals than the away team
  - 0 otherwise (draw or away win)

This target was constructed directly from full-time match scores.

### Feature Selection
Only **pre-match features** were used to avoid data leakage. These features are all known before kickoff:

- **HomeElo:** Elo rating of the home team  
- **AwayElo:** Elo rating of the away team  
- **Form5Home:** Recent form of the home team (last 5 matches)  
- **Form5Away:** Recent form of the away team (last 5 matches)

These variables capture both long-term team strength and short-term performance trends.

### Model Choice
- **Logistic Regression** was chosen as a baseline model due to its:
  - Simplicity
  - Interpretability
  - Suitability for binary classification tasks

The goal at this stage was not to maximize predictive performance, but to demonstrate a correct and meaningful application of machine learning.

### Training and Evaluation
- **Train–test split:** 75% training, 25% testing
- **Evaluation metric:** Accuracy

### Results
- **Accuracy:** 0.628

This result is substantially higher than random guessing and indicates that pre-match team strength and recent form contain meaningful predictive information about match outcomes.

### Interpretation
The model’s performance confirms that:
- Home advantage is partially explained by measurable factors such as Elo ratings and recent form
- Even a simple baseline model can capture non-trivial structure in football match data

This machine learning analysis serves as an initial benchmark and satisfies the January 2 deliverable requirements.






