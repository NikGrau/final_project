# A Century of World Cup Football

A short data visualization project that looks at every FIFA World Cup match from
1930 to 2014 and answers three simple questions a fan might ask:

1. Are there fewer goals per game than there used to be?
2. Have the crowds grown over time?
3. Which countries have scored the most?

## What is in here

```
worldcup-viz/
|- worldcup-viz.Rproj          the RStudio project file
|- data/
|--- WorldCupMatches.csv       the raw dataset, one row per match
|- report/
|--- worldcup-analysis.Rmd     the analysis and write up
|--- worldcup-analysis.html    the knitted report
|- README.md                   this file
```

## The data

`WorldCupMatches.csv` is a summary of World Cup matches. Each row holds the year,
date, stage, stadium and city, the two teams and their goals, the half time
score, the attendance, and the match officials. The raw file ships with a lot of
blank trailing rows and several duplicated games, so the report cleans those out
before doing anything else. A few team names also arrive with a small scraping
artifact attached to the front, which the report strips away.
