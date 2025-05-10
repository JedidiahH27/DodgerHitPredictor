# ⚾ Dodger Hit Predictor

This project explores machine learning models that aim to predict whether Mookie Betts, Shohei Ohtani, or Freddie Freeman will record a hit in an MLB game. These predictions are intended to support decision-making in player prop bets—a market offered by platforms like FanDuel.

## 📌 Introduction
FanDuel allows users to wager on outcomes like whether a specific MLB player will get a hit. My personal experiences with these bets have produced mixed results. To reduce reliance on luck, I set out to build a data-driven prediction model using pitch-level MLB data to make smarter wagers over time.

## 🎯 Why These Players?
I'm a Dodgers fan, so my focus naturally falls on Dodgers games.

Betts, Ohtani, and Freeman have long-term contracts, ensuring consistent data across seasons—ideal for building reliable models.

## 📊 Data Collection
Sourced via Statcast using the pybaseball library.

Covers pitch-level and game-level data from 2018 to 2023.

Includes pitch types, velocities, strike zone location, outcomes, and more.

Spring training and deprecated variables were filtered out to improve model relevance.

## 📉 Exploratory Data Analysis (EDA)
Players face over 1 million pitches across 5 seasons.

Around 27% of games end with no hits for Betts and Freeman; Ohtani is slightly worse at ~35% no-hit games.

Pitch outcome distributions (e.g., singles, doubles, home runs) align with expected performance from All-Stars.

## ⚙️ Modeling Approaches
### 1. Binary Classification Models (Hit vs. No Hit)
Models Used: Logistic Regression, Random Forest, XGBoost

Features: pitch location, count, pitch type, handedness

Issue: Class imbalance—far more “no hit” pitches than “hit” ones.

Even after undersampling and class weighting, models struggled:

Best accuracy: ~65–70%

F1-scores for predicting hits: below 0.2 in all models

### 2. Pitch Location Only
Used only plate_x and plate_z as predictors.

Slight performance drop, indicating most features had low predictive power.

### 3. Expected Batting Average (xBA) Regression
Regressed estimated_ba_using_speedangle using pitch location and spin rate.

Models performed very poorly (R² ≈ 0.01).

Added distance_from_center of strike zone as a new feature.

Still failed to improve model performance.

## 📈 Hitting Streak Model
Tested whether hitting streaks (momentum or slumps) could predict next-game performance.

Used logistic regression with lagged hitting streaks as predictors.

Model predicted “hit” for every instance; recall = 1.00, but precision = 0.00 for "no hit".

Visualization confirmed no strong correlation between hitting streaks and future performance.

## 🚫 Key Takeaways
Predicting individual hits per pitch or per game is extremely difficult due to high variance.

Even strong predictors like pitch location, count, or xBA provide little improvement.

The assumption that past performance or streaks influence the next game is not supported by the data.

FanDuel’s implied odds (73–74% chance of a hit) match historical frequencies well.

## 🧠 Final Thoughts
This project highlights the limits of prediction in high-variance scenarios like MLB batting. While the models don't (yet) outperform the market, the analytical process offers deep insight into what’s signal vs. noise in player prop betting.

## 🛠️ Tools & Libraries
Python, Jupyter Notebook

pybaseball, scikit-learn, xgboost, pandas, plotly, matplotlib, seaborn
