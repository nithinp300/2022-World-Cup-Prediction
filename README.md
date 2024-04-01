# 2022-World-Cup-Prediction
__Objective__:
- Prediction of the winner of an international matches Prediction results are  "Win / Lose / Draw" or "goal difference"
- Apply the model to predict the result of FIFA world cup 2022.

__Data__: Data are assembled from multiple sources, most of them are from Kaggle, others come from FIFA website / EA games.

__Feature Engineering__: To determine who will more likely to win a match, based on my knowledge, I come up with 4 main groups of features as follows:
1. head-to-head match history between 2 teams
2. recent performance of each team (10 recent matches), aka "form"
3. bet-ratio before matches
4. squad strength (from FIFA video game)

Feature list reflects those factors.

# Project Structure
1. __EDA__: Data Exploratory Analysis
2. __LE__: saved model for Label Encoder
3. __data__: completed dataset
4. __save_model__: saved Machine Learning model after training

# Data
### Data Source
The dataset are from all international matches from 2000 - 2022, results, bet odds, ranking, squad strengths
1. [FIFA World Cup 2022](https://www.kaggle.com/datasets/muhammad4hmed/2022-fifa-worldcup-qatar-full-live-dataset)
2. [International match 1872 - 2022](https://www.kaggle.com/martj42/international-football-results-from-1872-to-2017/data)
3. [FIFA Ranking through Time](https://www.fifa.com/fifa-world-ranking/ranking-table/men/index.html)
4. [Bet Odd](https://www.kaggle.com/austro/beat-the-bookie-worldwide-football-dataset/data)
5. [Bet Odd 2](http://www.oddsportal.com)
6. [Squad Strength - Sofia](https://sofifa.com/players/top)
7. [Squad Strength - FIFA index](https://www.fifaindex.com/)


### Feature List
- _*difference: team1 - team2_
- _*form: performance in 10 recent matches_

| Feature Name  | Description              |
|:-------------:|:------------------------:|
| team_1        | Nation Code (e.g US, NZ)      | 
| team_2        | Nation Code  (e.g US, NZ)     | 
| date          | Date of match yyyy - mm - dd  | 
| tournament    | Friendly,EURO, AFC, FIFA WC   | 
| h_win_diff    | Head2Head: win difference      |   
| h_draw        | Head2Head: number of draw      |   
| form_diff_goalF | Form: difference in "Goal For" |   
| form_diff_goalA | Form: difference in "Goal Against" |   
| form_diff_win   | Form: difference in number of win  |   
| form_diff_draw  | Form: difference in number of draw |   
| odd_diff_win    | Betting Odd: difference bet rate for win  | 
| odd_draw        | Betting Odd: bet rate for draw            | 
| game_diff_rank  | Squad Strength: difference in FIFA Rank   | 
| game_diff_ovr   | Squad Strength: difference in Overall Strength  | 
|game_diff_attk   | Squad Strength: difference in Attack Strength   | 
|game_diff_mid    | Squad Strength: difference in Midfield Strength | 
|game_diff_def    | Squad Strength: difference in Defense Strength  | 
|game_diff_prestige | Squad Strength: difference in prestige        | 
|game_diff_age11    | Squad Strength: difference in age of 11 starting players  | 
|game_diff_ageAll   | Squad Strength: difference in age of all players          | 
|game_diff_bup_speed| Squad Strength: difference in Build Up Play Speed         | 
|game_diff_bup_pass | Squad Strength: difference in Build Up Play Passing       | 
|game_diff_cc_pass  | Squad Strength: difference in Chance Creation Passing     | 
|game_diff_cc_cross | Squad Strength: difference in Chance Creation Crossing    | 
|game_diff_cc_shoot | Squad Strength: difference in Chance Creation Shooting    | 
|game_diff_def_press| Squad Strength: difference in Defense Pressure            | 
|game_diff_def_aggr | Squad Strength: difference in Defense Aggression          | 
|game_diff_def_teamwidth  | Squad Strength: difference in Defense Team Width    | 

# How to Run:

```
python experiment1-W-D-L.py
python experiment2-GoalDiff.py
python experiment3-WorldCup.py
```