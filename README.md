# Bundesliga_Relegation
Determining the points needed to not be relegated to the Second Bundesliga.

I wanted to see, how many points a team realisticly had to score in order to no be relegated.  I started for the 1995-1996 season because that was the year the Bundesliga started to award three points for a win.  I had the stats from an old school project and I wanted to make a Power Bi visual.

I calculated the following measures in Power BI
Average Regulation Points = AVERAGE(Sheet1[Relegated]) = 32.08

StDevRelegation = STDEV.S(Sheet1[Relegated]) = 3.67

Total Years = COUNT(Sheet1[Relegated]) = 26  1995-1996 to 2020-2021

Margin of Error = 1.96 * [StDevRelegation] / SQRT([Total Years]) = 1.41 CI of 95%

CI Upper = [Average Regulation Points] + [Margin of Error] = 33.49


“Based on historical Bundesliga data, and a calculated confidence interval where the upper bound for relegated teams' point totals is 33.49, we can be reasonably confident (e.g., 95%) that a team with 35 or more points is unlikely to be relegated.”

From the scatter chart you can see, that this has happened seven times, where a team with 35 points or more was relegated with the last time being the 2004-2005 season
