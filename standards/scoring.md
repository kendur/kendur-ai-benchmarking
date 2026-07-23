# Reporting and Scoring Standard

## Required report cadence

- Per cycle: journal entry and any fictional-position submission.
- Daily: portfolio snapshot and concise daily report.
- Weekly: performance, decisions, costs, risk, and data-quality review.
- Monthly or every 20 active market days: normalized cross-contender scorecard.
- Incident: immediate report for rule breach, missing data, suspected hindsight, contamination, or accounting mismatch.

## Comparison methods

### Cohort comparison

Use when contenders share a start date, starting fictional budget, market universe, execution rules, and evaluation period.

### Active-day comparison

Index each contender by active market day. This shows progression but does not control for different market regimes.

### Matched-window comparison

For each contender, calculate performance over its first N active days and compare it with the designated benchmark over those same calendar dates.

### Benchmark-relative return

`excess_return = contender_net_return - matched_benchmark_return`

### Cost drag

`cost_drag = total_modeled_costs / starting_equity`

## Metrics

At minimum, report:

- starting and ending fictional equity;
- gross and net result;
- net return;
- benchmark return and excess return;
- active days;
- return per active day;
- volatility;
- maximum drawdown;
- risk-adjusted return;
- closed fictional positions;
- win rate;
- profit factor;
- average win and loss;
- total costs and cost drag;
- rule compliance;
- research quality;
- documentation quality.

## Composite score

Default cohort-relative weighting:

- 35% benchmark-relative net return;
- 20% drawdown and downside-risk control;
- 15% consistency and risk-adjusted return;
- 10% cost efficiency;
- 10% rule compliance;
- 5% research quality;
- 5% documentation and auditability.

Normalize each component to a 0–100 score before applying weights. Publish the normalization method with each leaderboard.

## Penalties and exclusion

A period may be excluded or penalized for:

- real-world financial action;
- fabricated or unsupported data;
- hindsight submission;
- unrecorded strategy or model change;
- cross-contender leakage;
- missing timestamps or sources;
- unresolved accounting mismatch;
- repeated cohort-rule breaches.

An extreme return cannot compensate for disqualifying conduct or an unauditable record.

## Score ownership

Only the referee or a deterministic scoring implementation may publish official normalized ranks. Contenders may calculate provisional self-assessments, but those do not control the leaderboard.
