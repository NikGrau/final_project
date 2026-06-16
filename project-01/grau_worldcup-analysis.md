# A Century of World Cup Football

A short data visualization project that looks at every FIFA World Cup match from
1930 to 2014 and answers three simple questions a fan might ask:

1. Are there fewer goals per game than there used to be?
2. Have the crowds grown over time?
3. Which countries have scored the most?

## The data

`WorldCupMatches.csv` is a summary of World Cup matches. Each row holds the year,
date, stage, stadium and city, the two teams and their goals, the half time
score, the attendance, and the match officials. The raw file ships with a lot of
blank trailing rows and several duplicated games, so the report cleans those out
before doing anything else. A few team names also arrive with a small scraping
artifact attached to the front, which the report strips away.

## The three required extras

The final project asked for three things on top of the original report. Here is
where each one is handled.

**An interactive chart.** Toward the end of the report there is a plotly scatter
titled "Every World Cup, in one view." Each dot is one tournament, placed by year
and goals per game, sized by the number of games, and colored by the average
crowd. Hovering over a dot brings up the exact figures for that year, and you can
zoom into the crowded modern tournaments and pan around.

**Accessibility.** The colors
come from the Okabe and Ito palette and from viridis, both of which were built to
stay readable for people with color blindness. Wherever color carries a meaning,
such as Brazil's highlighted bar or the orange 1994 attendance bar, I backed it up
with a label or a sorted order so the message never depends on color alone.

**A redesign, before and after.** The section called "Fixing a bad chart" takes my
attendance bar chart and improves it. The original is perfectly honest, the axis
starts at zero and the bars are the right height, but it leaves the 1994 spike
unexplained, which could fool a reader into thinking the sport suddenly got much
more popular that year. The fix colors that one bar orange, adds a short note
saying the spike comes from the enormous American stadiums that hosted the 1994
tournament, and sharpens the title into a clear takeaway. The before and the after
sit next to each other so the change is easy to see.

## My favorite chart

My favorite is the goals per game line chart. It is the one that surprised me the
most, because I had always assumed modern football was full of more goals rather
than fewer. Seeing the wild 1954 peak of over five goals a game sitting next to the
1990 low made the whole story of a tighter, more careful game click into place in a
single picture.
