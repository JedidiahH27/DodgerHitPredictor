# Dodger Hit Predictor

In this notebook (best viewed here: https://nbviewer.org/github/JedidiahH27/DodgerHitPredictor/blob/main/HitPredictor.ipynb), I explore predictive models aimed at forecasting whether Mookie Betts, Shohei Ohtani, and Freddie
Freeman will record a hit in MLB games. This analysis supports wagers on player performances, a feature offered by
platforms such as FanDuel.

## Introduction
FanDuel allows users to bet on various sports outcomes, including whether a specific MLB player will achieve a hit during a
game. My personal experiences with these bets have yielded mixed results, which I attribute primarily to luck. Recognizing
the inherent risks posed by the Law of Large Numbers, I am compelled to develop a more systematic and reliable predictive
model to enhance the accuracy of my betting strategies over the long term.

## Rationale For Player Selection
The focus on Mookie Betts, Shohei Ohtani, and Freddie Freeman is twofold. Firstly, as a Dodgers enthusiast, my betting
interest naturally gravitates towards games featuring this team, making the choice to analyze these players both practical
and enjoyable. Secondly, their secured long-term contracts with the Dodgers ensure a stable dataset for ongoing analysis.
This stability is critical for developing a robust model that requires consistent performance data over multiple seasons.
By concentrating on these three prominent Dodgers players, I aim to create specialized models that can offer insights
specific to their performance trends, thereby providing a strategic edge in sports betting focused on these athletes.

## Data Collection Methodology
For the purpose of this project, the primary dataset will be sourced from pitch-level and game-level records, which provide
comprehensive details relevant to predicting the outcomes of a player's plate appearance. This data is mcollected by
Statcast, a high-resolution, automated tool developed to analyze player movements and game dynamics in Major League
Baseball.
To facilitate efficient and effective data retrieval, I will utilize the pybaseball library, a widely recognized tool in the baseball
analytics community. This library grants direct access to Statcast's database, allowing us to fetch detailed metrics such as
pitch type, pitch velocity, player positions, hit outcomes, and other variables critical to our analysis.
