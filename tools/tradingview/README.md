# TradingView setup receipt template

A tiny Pine Script v6 template for traders who want to log the plan before the result.

It draws:

- entry
- stop / invalidation
- target
- confidence
- status: open setup, closed win, closed loss, wait, skipped

Why it exists:

Most trading posts start after the candle already moved.

The 30-Day Public AI Trading Scanner Challenge does the opposite:
setup first, story later.

## Use it

1. Open TradingView.
2. Open Pine Editor.
3. Paste `setup-receipt-template.pine`.
4. Add to chart.
5. Fill entry, stop, target and confidence before you judge the trade.

Script:

- [`setup-receipt-template.pine`](./setup-receipt-template.pine)
- Raw: https://raw.githubusercontent.com/HugoRS00/HugoRS00/main/tools/tradingview/setup-receipt-template.pine

TradingWizard is TradingView with AI built in.
It reads the chart and gives entry, stop, target and confidence.

No fake PnL.
No win-rate claims.
Not financial advice.
