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

- **Unified core:** Wickd.Core and Wickd.CLI handle market data ingestion, normalization, replay, and deterministic structure emission.
- **Standardized structures:** Bots should not need to reimplement swing, order block, FVG, expansion, or liquidity detection. They consume these outputs through stable contracts.
- **Independent decisions:** A strategy agent owns its rules for setup selection, validation, risk, order placement, lifecycle management, and failure handling.
- **Explainable automation:** Every useful trading decision should be traceable back to the market structures, settings, and strategy rules that produced it.

This separation lets multiple bots share the same deterministic foundation while operating with distinct strategy logic.

---

## Product Layers

| Layer | Purpose | Status |
|---|---|---|
| Deterministic Core | .NET libraries, CLI workflows, market data adapters, causal structure contracts, and reproducible SMC detection | Current correctness focus |
| Structure research platform | Chart-based inspection, causal replay, visual validation, and detector-tuning workflows | Next product deliverable |
| Strategy backtesting | Strategy playground, reusable simulation, outcomes, and research workflows over validated structures | After structure validation |
| Strategy agents and AI | Independent execution agents plus assisted discovery, explanation, evaluation, and optimization | Later platform layers |

The current technical foundation lives in `wickd-dotnet`: a .NET-first engine and CLI for historical data handling, deterministic replay, and structure journaling. WickdAlgo is proving structure correctness before strategy backtesting, then proving strategy backtesting before generalizing the agent platform. Chart inspection has immediate priority because the structure algorithms need a fast visual research loop. Live execution, marketplace mechanics, and autonomous AI research are roadmap items, not current production claims.

---

## Roadmap

### Phase I: Structure Correctness and Visual Inspection

Current focus: turn the existing data and replay foundation into a trustworthy, inspectable structure platform.

- Deterministic, causal Wickd.Core contracts with explicit subject and knowledge time.
- Visually verified internal and external swings, Market Structure Breaks, liquidity, Order Blocks, and ExpansionFvg lifecycles.
- A local chart inspector for causal replay, entity lifecycles, and algorithm tuning.
- A reusable React/TypeScript chart component designed to become part of the future public web platform.
- Regression fixtures created from visually reviewed market scenarios.

### Phase II: Strategy Backtesting Platform

Next focus: build strategies and simulation on top of structure contracts that have already been visually and deterministically validated.

- Generic backtesting and settlement infrastructure outside Wickd.Core.
- The first independent ExpansionFvg strategy module.
- Strategy playground and backtest visualization workflows in the public web platform.
- Explainable outcomes linked back to exact structures, settings, and strategy rules.
- Stable boundaries proven by real strategy use before broader agent abstractions are introduced.

Marketplace, social-trading, or copy-trading mechanics may be explored later, but they are secondary to the stability of the trading core.

### Phase III: Strategy Agents and AI Research

Future focus: generalize strategy-agent execution and use AI to accelerate research, explanation, and evaluation.

- Run independent strategy agents over shared deterministic Core contracts.
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
