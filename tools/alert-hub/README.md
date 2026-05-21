# Crypto Alert Hub Test Kit

Most crypto alert tools send pings.

A useful alert tells you what changed, whether it is still fresh, where the trade is wrong, and whether it deserves action.

Use this before trusting any Discord alert, webhook, scanner, bot, or price notification.

## The Rule

An alert is not a trade.

It becomes useful only when it has:

- trigger
- freshness
- decision
- entry
- stop
- target
- confidence
- invalidation
- delivery route
- audit trail
- paper-first review before live execution

If those fields are missing, you do not have a setup.
You have noise with better formatting.

## Ping vs Setup

| Field | Basic ping | Setup-grade alert |
| --- | --- | --- |
| Asset | BTC moved | BTC / timeframe / market state |
| Trigger | Price crossed level | Exact condition plus trigger time |
| Freshness | Usually unclear | First triggered, last triggered, stale state |
| Decision | Buy/Sell vibes | BUY, SELL, WAIT, or REVIEW |
| Entry | Missing | Entry area or no-entry reason |
| Stop | Missing | Invalidation before entry |
| Target | Missing | Target or review level |
| Confidence | Missing | Confidence score plus reason |
| Delivery | Everything to Discord | Route by urgency and quality |
| Audit | Lost in chat | Saved setup, later result, paper/live state |

## 30-Day Challenge Receipt

This kit uses one real TradingWizard proof-loop setup as the example.

Not a win.
Not PnL.
Not a prediction flex.

It was a WAIT receipt.

| Field | Value |
| --- | --- |
| Date | 2026-05-20 |
| Source | TradingWizard terminal authenticated API |
| Asset | PEPE |
| Market | Crypto |
| Timeframe | 15m |
| Decision | WAIT |
| Status | Awaiting |
| Entry zone | 0.00000369-0.00000370 |
| Stop | 0.00000365 |
| Target | 0.00000385 |
| Confidence | 65/100 |
| Trade likelihood | 42/100, Possible |
| Reason | Price was below daily pivot resistance. Breakout confirmation was required. |

WAIT is a signal when confirmation is missing.

That is the point.

## Alert Hub Checklist

Run this before you send an alert into Discord:

| Check | Pass condition | Fail condition |
| --- | --- | --- |
| Trigger | The event says what happened | The alert only says the asset moved |
| Timestamp | Trigger time is visible | Nobody knows if it is stale |
| Decision | BUY, SELL, WAIT, or REVIEW is explicit | The trader has to guess |
| Entry | Entry area exists, or no-entry reason is stated | The alert pushes action without a plan |
| Stop | Invalidation is defined | Risk is decided after fear starts |
| Target | Target or review level is shown | The exit is hope |
| Confidence | Confidence and reason are included | Every alert feels equally urgent |
| Delivery | Route matches urgency | Every ping hits every channel |
| Paper mode | Bot/test flow is paper-first | Live execution is treated as default |
| Audit | Setup can be reviewed later | The signal disappears into chat history |

## Discord Payload Template

Use `discord-payload-template.json` as a starting payload.

The important part is not the exact JSON shape.
The important part is refusing to send naked pings.

Minimum useful payload:

```json
{
  "event_type": "setup_card",
  "symbol": "PEPE",
  "timeframe": "15m",
  "decision": "WAIT",
  "triggered_at": "2026-05-20T07:22:06Z",
  "freshness_seconds": 120,
  "entry_zone": {
    "min": 0.00000369,
    "max": 0.00000370
  },
  "stop": 0.00000365,
  "target": 0.00000385,
  "confidence": 65,
  "invalidation": "Breakout confirmation missing below daily pivot resistance.",
  "paper_first": true
}
```

## How TradingWizard Fits

TradingWizard is TradingView with AI built in.

It reads the chart and gives entry, stop, target and confidence.
Bots scan 100+ assets 24/7 so you do not stare at candles all day.

Use the full alert hub guide here:

https://www.tradingwizard.ai/academy/crypto-alert-hub-software-features-active-traders-need

Try the product here:

https://www.tradingwizard.ai/?utm_source=github&utm_medium=alert_hub_test_kit&utm_campaign=30_day_public_ai_scanner_challenge

## FAQ

### Is WAIT a real signal?

Yes.

WAIT means the setup does not have enough confirmation yet. It is often more useful than another fake BUY alert.

### Does this prove TradingWizard is profitable?

No.

This is not a win-rate claim, profit claim, backtest, or financial advice. It is a setup-structure checklist.

### Can I use this with my own Discord bot?

Yes.

Copy the JSON template, add your own routing logic, and keep paper-first review before live execution.

### Why include entry, stop and target on a WAIT alert?

Because it shows the condition that would make the idea actionable.

No entry without invalidation.

### Why not send every alert to Discord?

Because a Discord channel full of weak pings becomes unusable.

Route only useful events. Log the rest.

### Where is the public proof loop?

The 30-Day Public AI Trading Scanner Challenge ledger is here:

https://gist.github.com/HugoRS00/560a23c81086c8004646e80670f3e878

## Not Financial Advice

Use this for alert hygiene and paper-first workflow design.

Trading risk is real.
Live execution is your responsibility.
