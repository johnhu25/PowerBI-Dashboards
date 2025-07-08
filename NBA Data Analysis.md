Dashboard Link: https://github.com/johnhu25/PowerBI-Dashboards/blob/main/NBA.pbix

## Executive Summary
- The first dashboard analyses individual NBA player performance using publicly available player statistics from the 2024 - 2025 season the dashboard to assist NBA teams in evaluating player talent.

## Key Findings:
- Nikola Jokić is the most efficient player in the league, being in the top 5 categories averaging in scoring, assists, rebounding, and steals when filtered to 50+ games.
- Shai Gilgeous-Alexander leads all players in scoring average scoring of 32.7 PPG with strong all-around stats.
- The average player scores 8.6 PPG, with a field goal percentage of 45% and free-throw percentage of 75% (Not adjusted to 50 games).
- Better evaluation of a player would be best to include Games played and Field Goal attempts.
- For Guards a better indicator instead of Field Goal percentage would be Effective Field Goal percentage as Guards take more 3 Point Shots more often.

## Problem Statement
- How can NBA teams use player metrics to assist in identifying the most impactful players beyond traditional scoring statistics?

## Data Sources
- The data was sourced from https://www.basketball-reference.com. 

## Metrics
- Effective Field Goals is a better metric compared to Field Goals made due to accounting for the added value of 3 Point Shots compared to just 2 Points Shots.
- Formula = (Field Goals Made + 0.5 * 3-Pointers Made) / Field Goal Attempts

## Dashboard Overview
To filter outliers I recommend filtering to at least 50 games.

**Regular Season Leaders 2024-2025 (Using 50+ Played Games)**
- This Dashboard shows the players season average statistics and able to filter the data based on Team, Player, Position and Games.
- Data shows Shai Gilegous-Alexander is a dynamic scorer as he has the highest points on average at 32.70 which is more then 21 points on average.
    - A higher on average Field Goal Percentage at 52% more then 5% on average.
    - Higher Free Throw Percentage at 90% by 13% and ability to draw fouls at 8.8 Free Throws Attempts Per Game.
    - He also shows he can be a playmaker with 6.4 Assists 3.67 more on average however when compared to his same role at the point guard position it is only 1.5. 
    - Shai has a Assist to Turn over ratio of 2.67:1 (Assist/Turnovers), 2:1 is a good ratio often cited as a benchmark for a good assist-to-turnover ratio. 
    - Shoots 38% from Three Point 2% more then the average with 5.7 Three Point Attempts 0.76 more then average generally 40% is a good bench mark for a great Three Point Shooter.
- Trae Young has the highest assists with 11.6 and has a 4.7 turnovers giving it a 2.47:1 assist  to turn over ratio (Assist/Turnovers).
which is a good ratio often cited as a benchmark for a good assist-to-turnover ratio. 
- Generally Centers have higher then average Field Goal percentages.

**3 Point Dashboards**
- 3 Point Percentages haven't fluctuated too much since 1994 - 1995 Season.
- 3 Point Attempts has been slowly rising and has peaked at 37.60, which looking at the trend it should increase each year.
- Total 3 Points is increasing each year.
- Total Average points are increasing this can be correlated with the increase of 3 point scoring.

## Conclusion
Using traditional statistics like Points, Assist, Rebounds, Blocks per game while can be good indicators of evaluating a player, these statistics do not show other metrics on evaluating
if the player took a lot of field goal attempts to achieve high points on average, or how many turnovers to achieve high assists. 
Other metrics needs to be included to provide a better evaluation of the player besides the traditional metrics.
For deeper evaluations it would need more data like how much Field Goal Attempts had opponents contesting the shot or how much of the rebounds were contested?
