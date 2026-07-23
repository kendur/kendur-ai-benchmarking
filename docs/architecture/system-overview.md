# System Overview

## Objective

dAItrader is a reusable benchmark harness for comparing any number of AI systems on a constrained, paper-market task. It measures not only fictional return, but also risk control, cost discipline, evidence quality, rule compliance, and auditability.

## Components

### 1. Contender registry

Defines provider, platform, exact model, prompt version, start date, fictional budget, strategy freedom, tool permissions, cadence, and isolation key.

### 2. Experiment cohorts

Freeze the conditions needed for fair comparison: market universe, benchmarks, starting budget, eligible assets, risk limits, decision window, fictional execution policy, and evaluation horizon.

### 3. Independent contender runners

Each runner receives only shared standards, its cohort, its own state, and public information available before the cutoff. A runner writes hypotheses and fictional-position proposals but does not grade itself.

### 4. Benchmark referee

The referee validates timestamps, sources, cohort eligibility, execution assumptions, and costs. It maintains the fictional ledger, daily snapshots, incidents, and official scorecards.

### 5. Notion operational store

Notion currently stores configuration and operational records. It provides human-readable tables, relationships, dashboards, and an audit trail.

### 6. Version-controlled standards

This repository stores prompts, record contracts, scoring rules, deployment guidance, and architecture decisions. It does not store current private contender state while public.

### 7. Future orchestration

n8n or a small service may later:

- schedule contender runs;
- load exact prompt versions;
- call model APIs or local models;
- retrieve public data;
- validate JSON output;
- write authorized Notion records;
- invoke the referee;
- publish normalized scorecards.

## Run sequence

```text
scheduler
  -> load contender + cohort configuration
  -> enforce isolation and information cutoff
  -> call contender
  -> validate structured journal submission
  -> store append-only submission
  -> referee validates fictional execution and costs
  -> update fictional ledger
  -> create daily snapshot
  -> calculate periodic scorecard
  -> human reviews incidents and rule changes
```

## Fairness model

The system reports three separate comparisons:

1. same-cohort performance;
2. active-day progression;
3. matched-calendar-window benchmark-relative performance.

These views must not be collapsed into one unexplained rank.

## Failure behavior

A missing source, impossible timestamp, accounting mismatch, scope violation, or attempted real financial action creates an incident. The system fails closed: no official score is published until the issue is resolved or the affected period is excluded.
