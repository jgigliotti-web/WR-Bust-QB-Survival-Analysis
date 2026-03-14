# WR Bust Probability & QB Longevity

###  Objective
This project applies actuarial risk-pricing and advanced statistical modeling to NFL draft prospects. By moving beyond subjective scouting, I developed two distinct models to optimize draft capital: one to flag high-risk Wide Receivers and another to predict the "Life Expectancy" of Quarterback prospects.


### Project 1: Wide Receiver Profiling & Bust Probability
The Problem: Teams often draft WRs based on "prototype" physical traits and collegiate pedigree, ignoring the statistical "probability of ruin."

Methodology:
* Gamma Generalized Linear Model: Because receiving data is heavily right-skewed, I used a Gamma distribution to predict a player's expected Yards-Per-Year.
* Logistic Regression: I engineered a "Bust" variable (defined as a Top-100 pick with <500 career yards) to calculate the baseline probability of failure.
* Feature Engineering: Isolated "Power School" pedigree to test if elite schooling inflates draft value.

Key Finding: The model identifies "Paper Tigers"—prospects whose draft slot is driven by pedigree rather than the underlying efficiency predicted by the Gamma GLM.

---

### Project 2: Quarterback Survival Analysis
**The Problem: The QB position is a high-cap investment. Understanding "NFL Life Expectancy" is more critical for a franchise than predicting single-season yardage.

Methodology:
* Kaplan-Meier Survival Curves: Developed curves to visualize the percentage of QBs remaining in the league at various year-markers.
* Log-Rank Testing: Segmented the population into High QBR (>70) and Low QBR (<70) tiers to identify the divergence in career length.



Key Finding: The QBR Shield. High-efficiency college QBs are 30% more likely to "survive" into a second NFL contract (Year 4/5). While traits determine the ceiling, collegiate QBR sets the statistical floor for career longevity.

---

###  Tools & Data
* Languages: R (tidyverse, survival, stats)
* Data Source: Longitudinal NFL career data (1967–Present) and Collegiate QBR metrics.
