## Combining Independent Matches 

In Champions League's (2018-19) Group B, a situation has arisen where last gameweek would decide that which team would qualify for Round of 16 after Barcelona. The competition is between Inter Milan and Tottenham Hotspurs. Now the current situation is:

 Team | Played | Win | Draw | Lost | GD | Points
 ------------ | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- 
 Tottenham | 5 | 2 | 1 | 2 | -1 | 7
 Inter | 5 | 2 | 1 | 2 | -1 | 7
 
Tottenham chances for going through is to get all 3 points against Barcelona at Nou Camp. But for Tottenham to go through they need to match Inter Milan's result against PSV Eindhoven at San Siro. 

So for evaluating Champions League games, I've used Club Elo Ratings which is a quite reliable measure to judge a club's overall strength intercontinentally. 

So Elo difference is calculated as, 

    E = 1 / (10(-dr/400) + 1) 
(where dr is the Elo point difference of the 2 clubs)

It is directly linked to the win probability of both teams in a direct confrontation. 
And through this I was able to create a model where I was able to use Poisson Distribution Model and include the net Elo of each team. The reason behind this is to value goal scored and conceded by each team. 

<p align="center">
  <img src = "https://github.com/raffa1996/Combining-Independent-Matches/blob/master/poi%20new.png" 
  alt="profilepic"/>
  </p> 

So the Poisson Distribution Model results for Barca-Spurs game are: 

 Goals | 0 | 1 | 2 | 3 | 4 | 5 
 ------------ | ------------ | ------------- | ------------- | ------------- | ------------- | ------------- 
 0 | 1.04 | 2.36 | 2.69 | 2.04 | 1.16 | 0.53
 1 | 2.38 | 5.41 | 6.16 | 4.67 | 2.66 | 1.21
 2 | 2.73 | 6.2 |  7.06 | 5.36 | 3.05 | 1.39
 3 | 2.08 | 4.74 | 5.39 | 4.09 | 2.33 | 1.06
 4 | 1.19 | 2.72 | 3.09 | 2.34 | 1.33 | 0.61
 5 | 0.55 | 1.25 | 1.42 | 1.08 | 0.61 | 0.28

Observations:<br>
<b>Favourable result</b>: BARCELONA 2 - 2 SPURS<br>
<b>Second Favourable result</b>: BARCELONA 1 - 1 SPURS<br>
<b>BARCELONA Win Percentage</b> -  38.0<br>
<b>SPURS Win Percentage</b> -  38.0<br>
<b>Draw Percentage</b> -  20.0<br>





So for Tottenham will go through to the Round of 16 if they are able to match Inter Milan's result against PSV. Now Inter vs PSV is an interesting match as form of both the teams complement each other. 
