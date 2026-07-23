# KenDur AI Benchmarking

A model-agnostic framework for comparing AI systems under controlled, auditable conditions.

The first benchmark is **dAItrader**, a paper-market simulation that compares how different AI contenders research tools, form hypotheses, manage a fictional budget, model costs, and document results.

> **Simulation only:** This repository must never be used to open accounts, accept financial terms, transfer money, store brokerage credentials, or submit live financial orders. All brokerages, subscriptions, fills, positions, fees, and returns are hypothetical.

## Current status

- Foundation phase
- Operational source of truth: [Notion — dAItrader](https://app.notion.com/p/3a68b48d5579817ba93efc9c76fe5a0d)
- Initial contender: Notion Custom Agent
- Additional contenders planned: ChatGPT, Claude, Gemini, Grok, Copilot, API-hosted models, and local models
- Scored activity remains disabled until a cohort has explicit budget, risk, asset, timing, and execution rules

## Design principles

1. **Comparable conditions** — contenders share explicit cohort rules.
2. **Isolation** — one contender cannot see another contender's unpublished decisions.
3. **No hindsight** — forecasts and hypothetical positions are timestamped before evaluation.
4. **Net performance** — subscriptions, fees, slippage, and data costs count against the fictional budget.
5. **Risk-aware scoring** — raw profit cannot erase severe drawdown, rule breaches, or missing records.
6. **Append-only history** — original decisions and failed hypotheses are preserved.
7. **Late-entry fairness** — comparisons include cohort, active-day, and matched-market-window views.

## Repository layout

```text
LOAD.md                    AI entry point and loading order
AI_USAGE.md                AI governance and disclosure
SECURITY.md                secrets and financial-action boundaries
CHANGELOG.md               notable repository changes

agents/                    contender and referee instructions
standards/                 evidence, isolation, execution, cost, and scoring rules
schemas/                   platform-neutral record contracts
notion/                    Notion database map and deployment notes
docs/architecture/         system design
docs/decisions/            architecture decision records
docs/deployment/           cross-platform setup guidance
data/examples/              synthetic examples only
reports/examples/           synthetic reports only
```

## Start here

AI systems and contributors should read [`LOAD.md`](LOAD.md) first.

Human setup sequence:

1. Review the Notion cohort configuration.
2. Set the fictional starting budget and explicit risk limits.
3. Register a contender with an exact model and prompt version.
4. Deploy the contender using the applicable platform guide.
5. Run a historical dry test and exclude it from scoring.
6. Activate the contender only after referee validation passes.

## Data policy

The public repository contains reusable prompts, standards, schemas, decisions, and synthetic examples. It must not contain:

- current contender watchlists or unpublished hypotheses;
- raw simulated portfolio history unless intentionally published later;
- credentials, API keys, account identifiers, or paid-data tokens;
- personally identifying financial records;
- private Notion exports.

Operational records remain in Notion until a dedicated private data pipeline is approved.

## License

License selection is pending. Do not assume permission beyond ordinary GitHub viewing and contribution until a license file is added.
