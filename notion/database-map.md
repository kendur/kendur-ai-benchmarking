# Notion Database Map

Operational source of truth: [dAItrader](https://app.notion.com/p/3a68b48d5579817ba93efc9c76fe5a0d)

## Databases

| Database | Purpose | Data source ID |
|---|---|---|
| dAItrader — Contenders | One configuration record per model or agent | `3fc5eddc-3124-4424-a632-ad3aefa86720` |
| dAItrader — Experiment Cohorts | Shared rules and starting conditions | `e2c29db4-6db3-410c-91b4-0df5df3dab35` |
| dAItrader — Platforms & Tools | Hypothetical broker, paper-trading, data, scanner, charting, and bot research | `985a5822-1599-45b0-83f0-be5928bc7e7d` |
| dAItrader — Simulation Journal | Append-only hypotheses, research, and decisions | `75f218a7-8928-464c-9801-2d2bce4047e3` |
| dAItrader — Simulation Ledger | Fictional positions and modeled transaction costs | `bada706b-a187-49a0-860d-189cfc2a535a` |
| dAItrader — Daily Snapshots | Daily fictional equity, costs, drawdown, and benchmark comparison | `f2cb978e-5c24-49d1-8079-8d861f0f62ba` |
| dAItrader — Reports & Scorecards | Daily, periodic, matched-window, and normalized leaderboard reports | `3104f75f-d1de-4b3f-993e-9b790c2e526a` |

## Instruction pages

- Contender Core Instructions
- Benchmark Referee Instructions
- Reporting & Scoring Standard
- Notion Agent Setup
- Cross-Platform Deployment Guide
- Repository Plan

## Initial records

- Cohort: `Cohort 001 — Initial Open Sandbox`
- Contender: `Notion Agent — Contender 01`

Both remain `Not started`. Budget, exact model, start date, tool budget, risk limits, eligible assets, benchmark set, and fictional execution assumptions must be completed before scored activity.

## Authority split

- **Notion** holds current operational state and private benchmark records.
- **This repository** holds versioned prompts, standards, schemas, architecture, and synthetic examples.
- **Future private automation** may synchronize records, but must preserve Notion IDs and append-only history.

## Write rules

1. Every shared database write must include a contender relation or referee authority.
2. Contenders must use only their own isolation key and related rows.
3. The referee may read all rows for scoring but cannot expose one contender's unpublished work to another.
4. Dry-test records must be clearly labeled and excluded from official scorecards.
5. Never delete a failed hypothesis to improve apparent performance.
