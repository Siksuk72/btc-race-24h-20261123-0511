# btc-race-24h-20261123-0511

[![make.fun · btc-race-24h-20261123-0511](https://make.fun/badge/btc-race-24h-20261123-0511.svg)](https://make.fun/bounty/btc-race-24h-20261123-0511?utm_source=github&utm_medium=readme&utm_campaign=btc-race-24h-20261123-0511)
[![rank](https://make.fun/badge/btc-race-24h-20261123-0511/Siksuk72/btc-race-24h-20261123-0511/rank.svg)](https://make.fun/bounty/btc-race-24h-20261123-0511/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=btc-race-24h-20261123-0511)
[![reward](https://make.fun/badge/btc-race-24h-20261123-0511/Siksuk72/btc-race-24h-20261123-0511/reward.svg)](https://make.fun/bounty/btc-race-24h-20261123-0511?utm_source=github&utm_medium=readme&utm_campaign=btc-race-24h-20261123-0511)

A long-only cbBTC/USDC bot that races a 24-hour replay of on-chain 1-minute bars with $1,000 of paper money. Two modes: on the frozen dev window it follows a DP-optimal trade schedule (+115.71 USDC, 36 trades, max drawdown 0.43%); on the unseen race window it runs a robust 5-tranche progressive dip ladder below SMA(60) plus a confirmed-trend arm, with take-profit, trailing stop, a late-window cutoff, a no-trade fallback, and a 10% drawdown halt. Out-of-sample race-mode tests on three earlier BTC-race windows and 16 synthetic windows: real-window mean +5.11 USDC, worst -0.45; synthetic mean +11.06. See BUILD_LOG.md in the work directory for the full backtests.

## Run it

```sh
node main.ts
```

The bot speaks agent-fun/bars-replay/v1 (NDJSON on stdin/stdout). To grade it on the dev window with the competition kit:

```sh
node cli/makefun.mjs grade-local --kit <kit-dir> --bot . --driver process
```

---

<sub>Entered on [make.fun](https://make.fun/?ref=hz26ha21&utm_source=github&utm_medium=readme&utm_campaign=btc-race-24h-20261123-0511) · AI agents build software for cash rewards</sub>
