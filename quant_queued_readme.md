# Quant_Queued — Experimental Futures Strategies & R&D Refactoring Queue

**[Quant\_Queued](https://www.google.com/search?q=https://github.com/Deep-2k3/Quant_Queued)** serves as the active research, prototyping, and refactoring sandbox companion to **[Quant\_Strat](https://www.google.com/search?q=https://github.com/Deep-2k3/Quant_Strat)**. This repository houses work-in-progress **[TradingView Pine Script](https://www.tradingview.com/support/solutions/43000763320-how-to-work-with-pine-editor/)** strategies and multi-timeframe market-structure indicators queued for parameter optimization, signal-filtering upgrades, and eventual porting to **[NinjaTrader 8 (C# / NinjaScript)](https://docs.ninjatrader.com/ninjascript_explorer)**.

## Queued Scripts & Prototypes

| File Name | Category | Current Implementation | Queued Refactoring & Optimization Goals |
| :--- | :--- | :--- | :--- |
| **`Black Box and Red Box Liq. trap.pine`** | Visual Indicator ([Pine Script](https://www.tradingview.com/support/solutions/43000763320-how-to-work-with-pine-editor/)) | Plots session-based "Black Box" and "Red Box" liquidity trap zones directly on the chart. | Refine session range boundaries and filter false sweeps during low-volume consolidation windows. |
| **`RED and Black box strat.pine`** | Strategy ([Pine Script](https://www.tradingview.com/support/solutions/43000763320-how-to-work-with-pine-editor/)) | Systematic execution prototype built around the Red Box & Black Box Liquidity Trap visual model. | Improve stop-loss placement, add displacement confirmation before entry, and reduce whipsaw drawdowns. |
| **`LiquidityEdge.pine`** | HTF Overlay Indicator ([Pine Script](https://www.tradingview.com/support/solutions/43000763320-how-to-work-with-pine-editor/)) | Maps liquidity pools with a refactored dynamic higher-timeframe (HTF) overlay. | Eliminate multi-timeframe lookahead bias and optimize array rendering across intraday chart intervals. |
| **`Market structure break with retest (multi-timeframe).pine`** | Structure Indicator ([Pine Script](https://www.tradingview.com/support/solutions/43000763320-how-to-work-with-pine-editor/)) | Tracks Multi-Timeframe Market Structure Breaks and Retests (`MSB&R`) across intraday and higher-timeframe swings. | Tighten structural swing pivot validation and add confirmation alerts on retest rejection candles. |
| **`Trader Dale Pure VP strategy.pine`** | Volume Profile Strategy ([Pine Script](https://www.tradingview.com/support/solutions/43000763320-how-to-work-with-pine-editor/)) | Algorithmic implementation of Volume Profile (`VP`) value-area and high-volume node (`HVN` / `LVN`) setups. | Enhance intrabar volume approximation in Pine Script and test porting core execution logic to NinjaTrader 8 tick data. |

## Development Workflow

1. **Concept & Visual Prototyping:** Initial market-structure, liquidity-sweep, and volume-profile hypotheses are scripted in **[TradingView Pine Editor](https://www.tradingview.com/support/solutions/43000763320-how-to-work-with-pine-editor/)** inside `Quant_Queued`.
2. **Debugging & Regime Filtering:** Scripts undergo iterative refactoring to resolve repainting, multi-timeframe (`request.security`) alignment, and choppy-session overtrading.
3. **Graduation to Production:** Once a prototype demonstrates stable walk-forward performance on **NQ / MNQ** and **ES / MES**, it is promoted to **[Quant\_Strat](https://www.google.com/search?q=https://github.com/Deep-2k3/Quant_Strat)** or ported into **[NinjaTrader 8 C#](https://docs.ninjatrader.com/ninjascript_explorer)**.

## Disclaimer

All scripts in `Quant_Queued` are experimental research prototypes under active development and are not intended for live capital deployment without independent verification.
