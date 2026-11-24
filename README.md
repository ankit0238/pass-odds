# Pass Odds

A free challenge pass simulator for prop traders. Enter how you trade, and Pass Odds runs 4,000 simulated challenges under the plan's rules to show how often you would pass.

**Live demo:** https://ankit0238.github.io/pass-odds/

## What it tells you

- Your chance of passing the challenge
- How you are most likely to fail: the daily loss limit or the max loss limit
- How many trades a pass typically takes
- Which risk per trade (0.25% to 3%) passes most often for your style
- The effect of a "stop for the day after N losses" rule

## How to use it

1. Pick a plan: Select, Prime, Signature or Elite.
2. Enter your win rate, average win (in R), and trades per day.
3. Move the risk slider and watch your odds change.

## How it works

Each simulated challenge is a sequence of trades. A win adds risk × average win, and a loss subtracts the risk. A run passes when it reaches the profit target, and fails when it hits the daily loss or max loss limit. Runs that do neither within 250 trading days count as unfinished. Results use a fixed random seed, so the same inputs always give the same answer.

The simulator was checked against a known result: a fair coin-flip trader on a 9% target with a 3% max loss should pass about 25% of the time, and the simulator gives about 24%.

## Limitations

- Trades are treated as independent. Streaks and market conditions are not modeled.
- Fees, slippage, swaps and open-trade swings are ignored.
- Plan rules come from the published challenge rules and may change. Check the official site.
- This is a simulation of the numbers you enter, not a prediction or a promise of results.

## Roadmap

- v2: import real trade history through the MyFundedPerps API to fill in your stats automatically
- v3: shareable result cards and per-plan comparison

## Run it yourself

No install needed. Download `index.html` and open it in any browser.

## Disclaimer

An independent community tool. Not official MyFundedPerps software and not affiliated with them. Built with AI assistance (Claude) and tested.
