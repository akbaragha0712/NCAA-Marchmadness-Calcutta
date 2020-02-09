# NCAA-Marchmadness-Calcutta

## Problem Statement

Create a model to evaluate the max price that should be paid for a NCAA team in my Calcutta betting pool

## Calcutta Pool Rules

All teams will be auctioned off with each team being assigned to the highest bidder. Payouts for the pool will depend on
the total pot size and the number of games each of a contestant’s teams win according to the following structure:

| No. of wins | Payout (as % of pot) |
|-------------|----------------------|
| 1 | .5% |
| 2 | 1.75% |
| 3 | 4.25% |
| 4 | 12% |
| 5 | 15% |
| 6 | 22% |

For example, the owner of the tournament’s winning team will receive 22% of the total pot, and the owner of the
tournament’s runner up will receive 15% of the total pot.

Teams will be auctioned off from lowest seeds to highest seeds. As bidding evolves, this aids bidders in estimating the
final pot size since the heavily favored teams that command the highest bids are auctioned at the end, thereby limiting
the risk on the larger bets.

The 16th to 13th seeded teams from the each Region will be bid upon as a bundle named the &quot;Dogs of the [Region]&quot;.
The winning bidder will own all 4 teams and can recoup their investment if one or two of the Dogs wins an upset.
For play-in games, contestants will bid on the winner of the game rather than each team in the play-in game. In other
words, a contestant who buys the winner of a play-in game will inherit whichever team happens to advance to the
Round of 64.

Each owner has a salary cap of $200, but can exceed this cap by paying a “luxury tax.” Every dollar spent over the salary
cap will only count for half as much in the bidding process. For example, an owner who has already exceeded the salary
cap can still bid on a team, but must pay twice as much for that team as a similar owner buying that team without
having exceeded the salary cap.

## Brainstorming

Working backwards from our final output. We want a max price value above which we are taking on too much risk for the likelihood that the team wins a certain number of rounds. If we use a regularized logistic regression to predict the likelihood a team wins a match up. For simplicity, we assume that the team with the higher probability wins the match up each time and we pick the 2nd, 3rd, 4th, 5th, and 6th round matchups accordingly. 

For example, 0.9x0.8x0.7x0.6x0.5x0.4 = 0.06 or a 6% chance of winning the entire league. Like so each team will have a % chance of winning. To convert this chance of winning to an appropriate price we must know what the prize for picking the winning team will be. Based on history, I believe the pot will be approximately $2,000 with 11 players - this means the prize for the winning team will be $440. For a team with a 6% probability, the most we'd want to pay for round 6 is $27. 

## Misc

For match up prediction inspiration refer to:
https://multithreaded.stitchfix.com/blog/2016/11/22/nba-rankings/
