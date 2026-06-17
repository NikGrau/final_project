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
   early twenties, plateau through the late twenties, and peak around age 31 before
   slowly declining.
2. Younger players carry the most upside. Plotting current rating against potential shows
   a wide gap for young players that closes as they age, which is where clubs look for
   future stars.
3. Footballing strength is spread broadly. The map of average rating by country shows
   talent concentrated across Europe and South America but far from limited to them, and
   it highlights that an average rewards countries that export only their best players.
4. Mentality drives the rating. A standardized linear model shows that reactions and
   composure carry more weight than flashier attributes like finishing or sprint speed,
   and the model explains the overall rating very well.

## The three required extras, and where they live


**An interactive chart.** Visualization 2, titled "How much room does a player still have
to grow?", is an interactive plotly scatter of current rating against potential for every
player rated seventy and above. A dashed diagonal marks where a player has reached their
ceiling. Hovering over any dot pulls up that player's name, club, nationality, age, and
both ratings. A flat image of seventeen hundred overlapping dots would just be a blob, so the
hover and the zoom are what make the chart usable at all.

**Accessibility.** Every figure carries alt text through the fig.alt chunk option so a
screen reader can describe it. The two charts that use color to carry information, the
interactive scatter and the world map, both use viridis scales, which stay readable for
colorblind viewers instead of relying on a red to green range that many people cannot
separate. Where color does carry meaning, I back it up with something else, the dashed
reference line on the scatter, the sorted order and confidence intervals on the model
plot, and the dot sizes on the age curve, so nothing depends on color alone.

**A redesign, before and after.** The section "Fixing a bad chart" improves the age curve
from the start of the report. The first version plotted every age in the data, including
ages with only one or two players, so the right tail jumped around wildly and made it look
like players fall apart and then suddenly turn elite again in their mid forties. The fix
drops every age with fewer than fifteen players, which clears out the noisy tail, and
sizes each dot by the number of players so the reader can see which points are backed by
real data. Same data and same question, but the chart stops letting a handful of veterans
speak for everyone.

## My favorite visualization

My favorite is the interactive room to grow scatter, Visualization 2. It is the chart that
turns a flat cloud of points into something you can actually explore, and hovering to find
a cheap young player with a high ceiling sitting well above the line is the closest the
report gets to feeling like the game itself.



## Data source

FIFA 18 player data, available at
https://github.com/aalhamadani/datasets (file `fifa18.csv`). Country outlines from the
Natural Earth project.
