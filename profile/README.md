# WickdAlgo

**WickdAlgo** is an SMC-first modular algorithmic trading ecosystem for technical traders building strategy agents from standardized market-structure outputs.

Our mission is to help traders turn market-structure ideas into testable, explainable, and eventually deployable autonomous strategy agents. WickdAlgo separates the universal work of data processing and structural analysis from the unique work of strategy design, trade selection, execution rules, and risk decisions.

The platform is built around one principle:

> Core emits structures. Agents make decisions.

---

## Vision

WickdAlgo aims to become a modular operating layer for algorithmic and AI-assisted trading.

The long-term platform is not a single bot, dashboard, or indicator. It is an ecosystem where:

- market data is normalized through shared infrastructure;
- Smart Money Concepts structures are detected once and emitted consistently;
- independent strategy agents consume those structures as inputs;
- traders can prototype, inspect, tune, backtest, and later deploy strategies through higher-level tools;
- AI research agents can explain, evaluate, and improve strategy ideas on top of deterministic outputs.

Smart Money Concepts are the first strategy family we are building around: swings, order blocks, fair value gaps, expansion candles, liquidity sweeps, and related lifecycle events. The architecture is designed to stay open to additional strategy modules over time.

---

## Core Philosophy

WickdAlgo is built on abstraction through modularity.

The "how" of market processing should be reusable. The "why" of a trade should belong to each strategy agent.

- **Unified core:** Wickd.Core, Wickd.CLI, and future Wickd.MCP tooling handle market data ingestion, normalization, replay, and structure emission.
- **Standardized structures:** Bots should not need to reimplement swing, order block, FVG, expansion, or liquidity detection. They consume these outputs through stable contracts.
- **Independent decisions:** A strategy agent owns its rules for setup selection, validation, risk, order placement, lifecycle management, and failure handling.
- **Explainable automation:** Every useful trading decision should be traceable back to the market structures, settings, and strategy rules that produced it.

This separation lets multiple bots share the same deterministic foundation while operating with distinct strategy logic.

---

## Product Layers

| Layer | Purpose | Status |
|---|---|---|
| Engine and tooling | .NET core libraries, CLI workflows, market data adapters, deterministic backtest replay, and SMC structure journaling | Current focus |
| Web platform | Strategy playground, chart-based structure inspection, algorithm tuning, backtesting interface, and research workflows | Next platform layer |
| Strategy agents | Independent bots that consume validated structures and manage strategy-specific execution decisions | Later execution layer |
| AI research layer | LLM-assisted discovery, explanation, evaluation, and optimization over deterministic engine outputs | Future intelligence layer |

The current technical foundation lives in `wickd-dotnet`: a .NET-first engine and CLI for historical data handling, deterministic replay, and structure journaling. The web platform has higher priority than fully functional live trading bots because WickdAlgo needs a strong visual research loop for tuning each structure-detection algorithm before real execution. Live execution, marketplace mechanics, and autonomous AI research are roadmap items, not current production claims.

---

## Roadmap

### Phase I: Tooling and Engine

Current focus: build a robust, high-performance foundation for data handling and structure emission.

- Wickd.Core for reusable trading and analysis primitives.
- Wickd.CLI for local fetch, replay, backtest, and journal workflows.
- Wickd.MCP direction for agent/tool integration.
- SMC structure outputs including swings, order blocks, expansion/FVG events, and liquidity behavior.
- Architecture that can support multiple independent strategy-agent instances.

### Phase II: Web Platform

Next focus: make structure research, strategy prototyping, and backtesting accessible through a user-facing platform.

- Strategy playground for building and testing rules without writing backend code.
- Chart-based inspection tools for validating swings, order blocks, FVGs, liquidity, and other SMC structures.
- Backtesting and visualization workflows for market-structure strategies.
- Algorithm tuning workflows before live execution is introduced.
- Future subscription access for deployed user-owned bots once the structure engine and strategy layer are mature enough.

Marketplace, social-trading, or copy-trading mechanics may be explored later, but they are secondary to the stability of the trading core.

### Phase III: AI Research Layer

Future focus: use AI agents to accelerate strategy research, explanation, and evaluation.

- Discover strategy ideas from market data and external signals.
- Backtest candidate ideas against WickdAlgo's deterministic core.
- Explain why a strategy did or did not qualify.
- Audit live and historical strategy behavior.
- Suggest optimizations while keeping execution rules explicit and reviewable.

AI should strengthen the research and evaluation loop without hiding the deterministic basis of a trading decision.

---

## Principles

- **Modular by design:** core, bots, web, and AI layers should evolve independently.
- **SMC-first, not SMC-only:** WickdAlgo starts with market-structure trading but should remain extensible.
- **Deterministic foundation:** data, structures, settings, and journals should be reproducible and inspectable.
- **Agent-ready contracts:** CLI, MCP, and APIs should make WickdAlgo usable by both humans and software agents.
- **Practical automation:** the platform should help traders build, test, and operate real workflows, not just produce signals.

---

## Disclaimer

WickdAlgo is software and research infrastructure for algorithmic trading, automation, and market analysis.

Nothing in this organization is financial advice. Trading involves risk. Users are responsible for their own strategies, exchange connections, configurations, risk management, and live execution decisions.
