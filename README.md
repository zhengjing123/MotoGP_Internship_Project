# Internship Project <br>
## MotoGP rider analysis

Author: Zheng Jing <br>
Programming Language 1: Python (.ipynb) <br>
Programming Language 2: R (.rmd) <br>

## Goals

for all races and all riders, we

​ a) implemented the predator index and prey index

​ b) implemented the net index, volatility index, and efficiency index

​ c) developed weighted predator & prey indexes (additional weight & exponential weight)

​ d) implemented summary statistics & data aggregation

​ e) visualizaions of riders' annual trajectory (2015 - 2019)

## Indexes Descriptions & Algorithm design

Grid = Rider's starting position, determined from the qualifying race

Final = Rider's final position

Predator = the total number of positions that a rider moves forward, regardless of him moving backward

Prey = the total number of positions that a rider moves backward, regardless of him moving forward

Net = Predator - Prey = Final - Grid, (which measures a rider's pure movement/displacement throughout the entire race)

Volatility = Predator + Prey, (which measures a rider's riding style - high means aggressive; low means conservative)

Efficiency = Net/Volatility, (the percentage of efficient movements)

- For example, a rider has net =2 and volatility = 10 . That means only 2 out of 10 moves are efficient for moving forward, and the other 8 moves are 4-4 cancelled off. So net/volatility = 2/10 = 20% gives us the efficiency of the rider’s movement.

Weighted Predator = Predator - Grid, (a way to compare riders' offensive ability by taking grid position into account)

Weighted Prey = the number of total riders - Grid - Prey, (a way to compare riders' defensive ability by taking grid position into account)

## Data
https://www.motogp.com/en/Results+Statistics <br>
All the data (lap charts) are collected from MotoGP official website. <br>


## Methodology

​ a) data cleaning 

​ b) data aggregation (tables) <br>

- compute the summary statitics - grouped by rider, rider and year, rider and circuit...

*by looking at the summary table, we are able to break down riders' performance in parts: offensive, defensive, volatility, efficiency, and final position*

​ c) plot graphs <br>
 
- efficiency vs volatility, e.g. Joan Mir (rookie) vs Alex Rins (veteran) <br>
- riders' annual trajectories (to study riders' improvement)
- a comparison of riders' performances by circuit <br>

## Conclusion & Analysis
