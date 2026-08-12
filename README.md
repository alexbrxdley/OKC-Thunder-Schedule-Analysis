# NBA Schedule Analysis -- OKC Thunder Data Science Technical Assessment

A data science technical assessment covering NBA scheduling analysis, trend identification, an original visualization tool, and a statistical model isolating how much a team's schedule -- not just its on-court talent -- affects its win total.

10 seasons of NBA schedule and game data (2014-15 through 2023-24), plus an 80-game draft of the 2024-25 season, used to answer a series of increasingly open-ended analytical questions.

## What This Covers

**Schedule density analysis** -- counting "4 games in 6 nights" stretches across the league, identifying which teams have historically faced the most and least demanding schedules, and testing back-to-back defensive performance (Brooklyn's defensive eFG% overall vs. specifically against opponents on the second night of a back-to-back).

**Trend identification** -- two verified, decade-long scheduling trends: league-wide back-to-backs have declined substantially (reflecting the NBA's player-rest initiatives), and road trips have become fewer but longer, consolidating travel into fewer total trips.

**An original visualization tool** -- a reusable function that plots a full season's schedule for any team, showing game density, rest before each game, and travel distance between consecutive games on a single chart. Applied to both OKC and Denver's 2024-25 draft schedules to identify the most demanding and most favorable stretches of OKC's season.

**Win-impact modeling** -- a logistic regression estimating each team's win probability from team strength, home court, rest, and travel, used to isolate how many wins each team gained or lost purely from schedule factors (both opponent strength and travel/rest) from 2019-20 through 2023-24. The team most helped by its schedule over this span was Detroit (+4.6 wins); the team most hurt was the LA Clippers (-3.6 wins) -- a result consistent with the well-documented Western Conference strength imbalance during this era.

## Tools

- R, tidyverse, lubridate, ggplot2 (plotly-compatible for interactive versions)

## Files

- `progress.Rmd` — the full analysis and write-up
- `data_dictionary.txt` — column definitions and dataset notes
- `schedule.csv`, `schedule_24_partial.csv`, `locations.csv`, `team_game_data.csv` — source data

## Running This

```r
install.packages(c("tidyverse", "lubridate"))
```

Then knit `progress.Rmd` from the project directory.
