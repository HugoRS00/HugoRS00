# AI Trading Bot Risk Control Scorecard

Most bot reviews ask the wrong first question.

Do not ask if it can make money.
Ask what happens when it is wrong.

This is a free 10-point scorecard for AI trading bots, scanners, Discord signal tools, alert hubs, and paper-to-live execution flows.

## Direct Answer

A trading bot is not ready for live capital unless it can show the setup before entry, define invalidation before risk, reject stale signals, cap loss exposure, and save a receipt after the trade.

If those controls are missing, you do not have a trading system.
You have an alert feed with better branding.

## Score It

Give each control:

- 0 = missing
- 1 = manual only
- 2 = visible, but not enforced
- 3 = enforced and receipt-backed

| Total score | Verdict | What to do |
| --- | --- | --- |
| 24-30 | Usable for serious paper testing | Keep monitoring paper/live drift and audit logs |
| 18-23 | Paper-only | Do not connect live capital yet |
| 10-17 | Scanner, not a bot | Use for ideas, not execution |
| 0-9 | Noise | Walk away |

Try the checklist on your own setup.
Then run a free TradingWizard chart analysis:

https://www.tradingwizard.ai/terminal?first_analysis=1&symbol=BTCUSDT&utm_source=github&utm_medium=risk_control_scorecard&utm_campaign=30_day_public_ai_scanner_challenge

## The 10 Controls

| # | Control | Pass condition | Fail smell |
| --- | --- | --- | --- |
| 1 | Paper-first mode | New strategies can run in paper mode before live execution | The default path is live money |
| 2 | Entry is defined before action | The bot gives entry or entry zone before the trade | Entry is explained after the candle moves |
| 3 | Stop/invalidation is defined | Stop loss or invalidation is visible before entry | Risk is decided after fear starts |
| 4 | Target or review level exists | The exit plan is known before the trade | The target is "let it run" with no rule |
| 5 | Confidence has a reason | Confidence score includes setup context | Every alert feels equally urgent |
| 6 | Stale signals are rejected | Old payloads expire or move to review | Late alerts still trigger trades |
| 7 | Position size is capped | Max risk per setup is enforced | Size changes with emotion or hype |
| 8 | Daily kill switch exists | Bot can pause after loss or error limits | Losing streaks keep firing |
| 9 | Paper/live drift is audited | Slippage, fills, and rejected orders are logged | Paper wins silently become live losses |
| 10 | Receipts survive the trade | Setup, result, and no-trade decisions are saved | The signal disappears into Discord history |

## Proof Loop Examples

These are not performance claims.
They are structure receipts from the 30-Day Public AI Trading Scanner Challenge.

| Receipt | What it proves | Source |
| --- | --- | --- |
| WLD paper bot target hit: entry 0.29196, stop 0.281, target 0.325, exit 0.3258, confidence 45/100, result +11.59% | The target was defined before greed showed up | https://x.com/TradingWizardAi/status/2059618183569453235 |
| LINK paper setup then stop loss: entry 9.8172, stop 9.60, target 10.24, confidence 80/100, result -2.46% | The loss was logged instead of rewritten | https://x.com/TradingWizardAi/status/2057805714970616167 |

## Practical Workflow

1. Pick one bot, scanner, or signal tool.
2. Score all 10 controls from 0 to 3.
3. If the score is under 18, use it only as an idea scanner.
4. If the score is 18-23, run paper mode only.
5. If the score is 24+, run a small paper/live comparison and log drift.
6. Never upgrade a bot because one trade was green.
7. Upgrade only when the receipts survive wins, losses, stale alerts, and no-trade decisions.

## JSON And CSV

- Machine-readable checklist: `ai-trading-bot-risk-scorecard.json`
- Spreadsheet version: `risk-controls-checklist.csv`

Use these in your own docs, alert hub, bot QA flow, or affiliate review.

## How TradingWizard Fits

TradingWizard is TradingView with AI built in.

It reads the chart and gives entry, stop, target and confidence.
Bots scan 100+ assets 24/7 so you do not stare at candles all day.

Starter is free: 3 AI analyses/day, 1 trading bot, Basic Kai AI.
No credit card required.

## FAQ

### Does a high score mean the bot is profitable?

No.
This scorecard tests risk controls and evidence quality, not future returns.

### Why include losses?

Because a bot that hides losses cannot be trusted.
Loss receipts show whether the system respects invalidation.

### Is paper trading enough?

No.
Paper mode is the first filter.
You still need paper/live drift checks for slippage, fills, rejects, and execution timing.

### What is the most important control?

Predefined invalidation.
If the bot cannot say where it is wrong before entry, it is not ready for live execution.

### Why is a no-trade receipt useful?

Because WAIT is often the highest quality signal.
A scanner that refuses weak setups is more useful than one that forces action.

### Can I use this for non-crypto trading?

Yes.
The controls work for stocks, crypto, forex, futures, and options workflows.
Execution details change, but risk discipline does not.

## Bottom Line

Green trades are easy to market.

Risk controls are harder to fake.
Score those first.

Not financial advice.
Trading risk is real.
