# What Makes an Elite Footballer? A Look at FIFA 18 Player Data

## Executive summary

This mini project uses the FIFA 18 EA Sports player dataset to ask a simple question
with a few different answers: what separates the best footballers from the rest, and
where in the world do they come from? The analysis works through four visualizations
that build on one another, moving from how ratings change with age, to how much room
young players have to grow, to a world map of national strength, and finally to a model
of which attributes the rating actually rewards.

## Motivation

Sports data is a friendly place to practice visualization because the questions are easy
to feel even when the analysis gets involved. FIFA 18 is especially nice because every
player carries a long list of clean numeric attributes that all feed into a single
headline rating. That structure lets me explore relationships, geography, and a simple
predictive model using one tidy file.

## Description of the data

The dataset is a single CSV with roughly seventeen thousand players and forty columns.
The first few columns describe each player by name, nationality, club, and age, and the
remaining columns are skill attributes scored from zero to one hundred, such as reactions,
composure, finishing, sprint speed, and the goalkeeping ratings. Two summary columns,
overall and potential, capture a player's current quality and their estimated ceiling.
There are no missing values anywhere in the file. The players span more than one hundred
and sixty nationalities and several hundred clubs, which is what makes a geographic view
worthwhile.

The spatial visualization also uses Natural Earth country outlines, included as a
shapefile in `data/ne_countries`.

## Summary of findings

1. Ratings follow a clear career arc. Average overall ratings climb through a player's
   early twenties, plateau, and peak around the late twenties before slowly declining.
2. Younger players carry the most upside. Plotting current rating against potential shows
   a wide gap for young players that closes as they age, which is where clubs look for
   future stars.
3. Footballing strength is spread broadly. The map of average rating by country shows
   talent concentrated across Europe and South America but far from limited to them, and
   it highlights that an average rewards countries that export only their best players.
4. Mentality drives the rating. A standardized linear model shows that reactions and
   composure carry more weight than flashier attributes like finishing or sprint speed,
   and the model explains the overall rating very well.

## Project structure

```
fifa18-analysis/
|- fifa18-analysis.Rproj
|- data/
|--- fifa18.csv
|--- ne_countries/
|----- ne_110m_admin_0_countries.shp
|----- ne_110m_admin_0_countries.shx
|----- ne_110m_admin_0_countries.dbf
|----- ne_110m_admin_0_countries.prj
|- report/
|--- fifa18-analysis.Rmd
|--- fifa18-analysis.html
|--- interactive_potential_overall.html
|- README.md
```


## Data source

FIFA 18 player data, available at
https://github.com/aalhamadani/datasets (file `fifa18.csv`). Country outlines from the
Natural Earth project.
