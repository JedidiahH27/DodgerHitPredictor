⚾ Dodger Hit Predictor

This project explores predictive models aimed at forecasting whether Mookie Betts, Shohei Ohtani, or Freddie Freeman will record a hit in a given MLB game. These predictions can inform bets placed on platforms such as FanDuel, which offer markets on individual player performances.

📌 Introduction
FanDuel allows users to wager on various sports outcomes—including whether a specific MLB player will get a hit during a game. My own experiences with these bets have shown inconsistent results, often skewed by luck.

To address this and improve my long-term strategy, I created a systematic approach grounded in data science and baseball analytics. This project leverages machine learning to enhance the predictability of hit outcomes, reducing the reliance on chance.

🎯 Why These Players?
The model focuses on Mookie Betts, Shohei Ohtani, and Freddie Freeman for two main reasons:

Fan Perspective: As a passionate Dodgers fan, my betting interest naturally centers around Dodgers games.

Data Stability: All three players are secured with long-term contracts, offering a consistent and reliable dataset across multiple seasons—crucial for building robust predictive models.

By honing in on these star athletes, the project delivers targeted insights with potential real-world betting advantages.

🧠 Project Goal
To predict the likelihood of each player recording at least one hit in an MLB game using historical data and statistical learning techniques. This model aims to:

Reduce reliance on gut instinct or streaks

Surface actionable insights from historical and contextual data

Inform betting decisions with a more analytical foundation

📊 Data Collection
The primary dataset includes pitch-level and game-level data sourced from Statcast, MLB’s high-resolution tracking system. This data provides granular details about:

Pitch type and velocity

Batted ball outcomes

Player positions and matchups

Environmental factors (e.g., ballpark effects)

To access this data efficiently, the project uses the pybaseball Python library—a well-established tool in the baseball analytics community. Pybaseball offers direct access to Statcast’s API, allowing for seamless integration into predictive pipelines.

🛠️ Technologies & Tools
Python

Jupyter Notebook

pybaseball (Statcast data access)

pandas, NumPy (data manipulation)

scikit-learn, XGBoost (predictive modeling)

matplotlib, seaborn (visualizations)

📈 Future Directions
Add real-time data integration

Expand to other players or teams

Deploy a web interface for user-friendly access

Track model performance against actual game results over time

If you're a Dodgers fan, a fantasy baseball player, or a bettor looking to add analytical power to your picks, this project aims to deliver actionable insights and a bit of fun along the way.
