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

For match up prediction inspiration refer to:
https://multithreaded.stitchfix.com/blog/2016/11/22/nba-rankings/
