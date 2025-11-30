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

##Exploratory Data Analysis (EDA)
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

