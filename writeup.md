# xG Analysis – Individual Player xG
## Background:
The nerds are changing sports. This happened first with baseball (we’ve all seen Moneyball) and has happened in basketball (blame Steph Curry or Daryl Morey, either way the nerds have won and teams have to shoot threes). The statistical revolution has come slower to soccer,
in some ways because there are fewer quantifiable moments. NBA games average around 42 made baskets per game[^1], EPL matches hover between 2 and 3 goals[^2] – you’re just talking about very different sample sizes.  
  
The nerds solved this problem, though, with a little thing called Expected Goals (xG). XG is actually pretty impressive (I highly suggest you read the write up from fbref: https://fbref.com/en/expected-goals-model-explained/). Basically, it looks at the entire context of a 
shot (i.e. distance, angle, what part of the body the ball is struck with, defender positions) and assigns a rating based on how many of a similar shot was scored. Easiest example is this: penalty kicks have an xG of 0.78 because they’re scored 78% of the time.  
  
When you think about it, though, there feels like there’s something missing from xG. It’s all about the context of the shot – where it’s taken from, where the opposition is – it doesn’t take into account at all how good the shooter is at finishing. I think it is a fair 
assumption that some players should be better than average at shooting the ball: maybe they kick the ball harder than other players so it is harder for the goalkeeper to block, or maybe they are better at kicking the ball into a part of the goal the goalkeeper can’t reach.
  
More than that, though, I feel like we almost look down on players scoring above their xG. We act as if it surely must be a statistical anomaly and that their scoring will revert to the mean. In effect, we act as if we shouldn’t expect players to outperform xG – we assume 
finishing isn’t a skill some players will be better at than others.  
  
Ultimately, there’s only one question to answer: do certain players consistently out-perform their xG? And, if so, what characteristics define those players?

## Dataset:
For this analysis, I've collected individual player statisitcs for the last 6 completed years of Europe top 5 men's leagues (English Premier League, Spanish La Liga, German Bundesliga, Italian Serie A, and French Ligue 1). The 2017-18 season was the first in which fbref has xG data. I'm planning on doing an addendum focused on women's football, but for intitial analysis I've chosen to use the men's top 5 leagues, which is very common in these kinds of analyses.

## Data Preparation:
The initial dataset had roughly 16,500 rows of player-seasons (each row comprised the stats of one season for one player). I first removed goalkeepers, as goalscoring is not a part of their game. Then, I instituted a games played cutoff of 30% of the player's possible minutes, as well as a shots cutoff of 0.395 per game. In doing so, I am limiting outliers -- playing very few games or barely taking any shots could weird to statistical anomalies. The cutoffs are arbitrary, but were chosen based on what fbref uses as cutoffs for statistics ranking. I am happy to be deferential to their rules.

After limiting rows, there ends up being 5,145 qualifying seasons from 2,164 players. Of these, 1091 are primarily defenders, 2,182 are primarily midfielders, and 1,872 are primarily forwards.



[^1]:  https://www.basketball-reference.com/leagues/NBA_stats_per_game.html
[^2]:  https://theanalyst.com/na/2023/05/the-great-premier-league-goal-explosion-record/
