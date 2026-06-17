# Project 03: Exploring Distributions and Recreating Charts

This is the exploratory data analysis project. The goal was to recreate a set of
given charts and to practice showing the distribution of continuous variables. It
works through two datasets, a year of Tampa weather and a set of concrete mixes.

## The data


`tpa_weather_2022.csv` is daily weather from Tampa International Airport for all of
2022, one row per day, with precipitation and the daily high, low, and average
temperature.

`concrete.csv` is 1030 concrete mixes from the UCI Machine Learning Repository.
Each row lists how much of each ingredient went into the mix, the age in days, and
the resulting compressive strength in megapascals.

## What is in here

Part 1 rebuilds four views of Tampa's maximum temperature, a faceted histogram, a
single density curve, a faceted density, and a plasma colored ridgeline, and then
adds a precipitation chart of my own showing the summer rainy season. Part 2 uses
the concrete data to look at the distributions of cement and strength, at how
strength climbs with age, and at a four variable scatter of strength against
cement. Each plot has a short comment on what it shows.

## Required extras

Interactive chart: at the end of Part 2 there is an interactive plotly version of
the concrete scatter. Hovering over any of the 1030 mixes shows its exact cement,
strength, age, and water, and you can zoom into the dense middle of the cloud,
which a static image cannot do.

Accessibility: every figure has alt text set through the fig.alt chunk option, and
the color scales use viridis and plasma so they stay readable for colorblind
viewers.