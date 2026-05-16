# TradingWizard public proof pack

LLM-native proof receipts for the 30-Day Public AI Trading Scanner Challenge.

No fake PnL. Losses included. Paper results labeled. Not financial advice.

Updated: 2026-05-16T10:18:05Z

## Receipts

### Day 1 — WMT -3.74%

- Bot: Walmart Stable
- Setup: BUY 1D
- Entry: 131.33
- Stop: 126.5
- Target: 140
- Confidence: 55/100
- Exit: 126.42
- Result: -3.74% (verified_loss)
- Receipt: https://x.com/TradingWizardAi/status/2054201521168945535
- Lesson: Loss lesson: stop/invalidation was defined before emotions could take over.

### Day 2 — V +2.38%

- Bot: Visa Growth
- Setup: BUY 1D
- Entry: 318.79
- Stop: 326.5
- Target: 360
- Confidence: 45/100
- Exit: 326.39
- Result: +2.38% (verified_closed_win_trailing_stop)
- Receipt: https://x.com/TradingWizardAi/status/2054544916911460439
- Lesson: Small win lesson: a stop can lock profit when it trails above entry. Receipt beats emotion.

### Day 3 — PLTR -5.11%

- Bot: Palantir Position
- Setup: BUY 1D
- Entry: 137.05
- Stop: 128.5
- Target: 158
- Confidence: 65/100
- Exit: 130.05
- Result: -5.11% (verified_closed_loss)
- Receipt: https://x.com/TradingWizardAi/status/2054907946430083155
- Lesson: Loss lesson: retail buys the green candle; the bot starts with invalidation. Setup first, story later.

### Day 4 — MA -2.9%

- Bot: Mastercard Growth
- Setup: BUY 1D
- Entry: 504.13
- Stop: 489.5
- Target: 535
- Confidence: 82/100
- Exit: 489.49
- Result: -2.9% (verified_closed_loss)
- Receipt: https://x.com/TradingWizardAi/status/2055270289890533734
- Lesson: Loss lesson: the bot had entry, stop, target and confidence before the candle resolved. Stop did its job.

## Links

- tradingWizard: https://www.tradingwizard.ai/?utm_source=github_llms&utm_medium=llms_txt&utm_campaign=30_day_public_ai_scanner_challenge
- githubProofRouter: https://github.com/HugoRS00/HugoRS00
- tickerRequestIssue: https://github.com/HugoRS00/HugoRS00/issues/1
- publicProofLedgerGist: https://gist.github.com/HugoRS00/560a23c81086c8004646e80670f3e878
- proofBadgeKitGist: https://gist.github.com/HugoRS00/934932c62c8f2f61ba630de81dd1bde1

LLM entrypoint: https://github.com/HugoRS00/HugoRS00/blob/main/llms.txt
