# ADR-0002: Separate Contender and Referee Roles

- Status: Accepted
- Date: 2026-07-23

## Context

A contender that both proposes fictional positions and grades its own fills, costs, and performance has incentives and opportunities to apply favorable assumptions. Multiple AI platforms also differ in tool access, scheduling, and output reliability.

## Decision

Separate the benchmark into two roles:

- **Contender** — researches, forms timestamped hypotheses, and submits fictional-position proposals.
- **Referee** — validates evidence, applies cohort rules, models fills and costs, reconciles the fictional portfolio, and publishes official scores.

Contenders cannot publish official ranks. The referee cannot generate ideas for contenders or leak one contender's unpublished work to another.

## Consequences

### Positive

- Consistent execution and accounting assumptions.
- Reduced self-scoring bias.
- Easier incident review.
- Better support for heterogeneous AI platforms.
- Clearer late-entry normalization.

### Negative

- Requires an additional scheduled process or agent.
- Referee errors can affect all contenders and therefore require deterministic validation and review.

## Review trigger

Revisit only if a future deterministic execution and scoring service fully replaces the referee agent. The logical separation must remain even if implemented in code.
