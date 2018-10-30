This was an attempt to support or refute the idea that as the NFL season progresses we learn about the teams, allowing us to better predict game outcomes later in the season. My guess was that any such effect was limited, akin to saying, “I should have picked those lotto numbers” after a drawing is complete.

I scraped data from two different websites. One included results and betting spreads from NFL games from 1978 through 2013. The other site included each team’s total predicted wins prior to each season for the 2001 through 2013 seasons.

I used to first data set to analyze how the difference between the betting spreads and actual results changed over the course of a season. I was unable to find any evidence that the predictions (i.e. the betting spreads) improve as a season progresses.

I then hypothesized that the predictions might improve, but only for the subset of games involving teams that ended up being significantly better or worse than expected. To find support for this I combined the two datasets (using only the 2001 through 2013 seasons). I defined a metric called “total wins error” for each game, representing the teams combined differences from their-season expectations. E.G. if team A won 4 games more than expected and team B won 4 games fewer than expected, that game would have a “total wins error” of 8. We might expect that if this game occurred early in the season the prediction would be relatively poorer than later in the season (when we’ve “realized” that team A is better than expected and team B is not as good as expected). I found slight evidence supporting a small effect of this nature - mean absolute error of predicted game scores was 10, but during the first two weeks of the season, during games between teams with “total wins error” of greater than five the mean error was about 12.5.

The .pdf document "Accuracy of NFL spreads over the course of season" describes this in more detail.

As an exercise I also created plots using Bokeh, but since I generally did not find much effect the graphs aren’t especially interesting:

WinPredictions.html is a visualization of each team’s performance compared to pre-season predictions. Note the 2004 Chargers who 7.5 games more than expected!

SpreadErrorsByTime.html shows each game in the dataset. The games are split into two sets: “Expected Games” are between teams that performed similar to their preseason expectations, while “Unexpected Games” are between teams that over/under performed expectations. The y axis shows the error or magnitude of the error for that game’s prediction. The (debataly real) very slightly larger error for early season “unexpected” games can be seen.
