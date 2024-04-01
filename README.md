# Sports-Analytics

## Project Summary
This project focuses on evaluating the cost efficiency of NBA point guards' contracts by analyzing their performance over the previous season by creating a metric ‘Cap Performance Index (CPI)’ and performing analysis to identify players who are not worth their contract.  

## Data Scraping and preparation 
Both player performance data and salary data are scrapped from basketball-reference.com. We did not account for multi-year contracts and guaranteed future money.

## Key Metrics Calculation
Performance Rating= (PTS×weight for PTS)+(AST×weight for AST)+(TOV×weight for TOV)
Points (PTS): Weight of 0.5 since it is the most critical indicator of a player’s contribution.
Assists (AST): Weight of 0.3 since it is a significant component of a player's contribution.
Turnovers (TOV): Negative weight of -0.2 since turnovers are detrimental to the team. 
Cap Performance Index (CPI) = Base Salary/ Performance Rating
Cap Performance Index (CPI): measures how economically efficient a player's contract is relative to their performance rating.

## Analysis - CPI Distribution
![Figure 1](https://github.com/dakyungsilvialee/Sports-Analytics/assets/105321151/c45db46f-80f0-4aac-8714-57b55fdd4f78) shows a right-skewed frequency distribution of CPI. Given the total number of data points to be 325 (N=325), CPI outliers can be found outside of the ranges below:
Lower Outlier = Q1 - (1.5 * IQR)
Upper Outlier = Q3 + (1.5 * IQR)

## Results
There are certain important assumptions made in deriving our conclusion of the 6 players who are unworthy of their contract value.

- assume that all players have the same overall game time over the course of the season.
- assume points, assists and turnovers to be the only measure of success for point guards.
 
Given these assumptions, a General Manager can use the analysis results to assess whether a player is worth their contract in this particular season assuming standard team tactics. If a particular team has a unique playing style and the point guard has different success metrics under this playing style, then the general manager should adjust the performance rating formula accordingly. However, no matter how the performance rating is defined, the ratio of a player’s salary to the player’s performance will always provide insights into the cost-effectiveness of the player.
