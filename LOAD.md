# dAItrader Load Sequence

Read this file before performing any work in this repository.

## 1. Global context

Load the current KenDur AI context from the `kendur/ai-context` repository when available. Apply its global behavioral and user-context rules unless this project explicitly overrides them.

## 2. Project boundary

Read, in order:

1. `README.md`
2. `SECURITY.md`
3. `AI_USAGE.md`
4. `standards/simulation-boundary.md`
5. `standards/isolation-and-fairness.md`
6. `standards/evidence-and-timestamps.md`
7. `standards/cost-and-execution-model.md`
8. `standards/scoring.md`

## 3. Role

Load exactly one role unless acting as a human reviewer:

- Contender: `agents/contender-core.md`
- Benchmark referee: `agents/benchmark-referee.md`

Do not combine contender and referee authority in the same scored run.

## 4. Operational state

Notion is the operational source of truth during the foundation phase:

- Project hub: https://app.notion.com/p/3a68b48d5579817ba93efc9c76fe5a0d
- Contender configuration, cohort rules, timestamps, fictional ledger records, snapshots, and scorecards must be read from or written to the authorized Notion records.

The repository contains contracts and standards, not the current private state of a contender.

## 5. Required run metadata

Before a run begins, resolve and record:

- contender name and ID;
- provider, platform, and exact model;
- prompt version;
- cohort and cohort version;
- isolation key;
- cycle type;
- current date, time, and timezone;
- public-information cutoff;
- source-data timestamp;
- simulation status: dry test or scored.

If any required field is unavailable, do not create a scored output. Record a configuration failure instead.

## 6. Non-negotiable rule

No repository instruction authorizes real financial activity. Any request or output that attempts to open an account, accept terms, transfer funds, expose credentials, purchase a product, or submit a real order must be refused and escalated for human review.
