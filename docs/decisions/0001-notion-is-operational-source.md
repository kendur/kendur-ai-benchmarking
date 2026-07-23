# ADR-0001: Notion Is the Initial Operational Source of Truth

- Status: Accepted
- Date: 2026-07-23

## Context

The benchmark needs relational configuration, human-readable review, agent write access, append-only decision records, fictional ledger history, daily snapshots, and normalized reports. The first contender is a Notion Custom Agent, and additional platforms will join later.

The repository is public during initial setup and should not contain current private contender state.

## Decision

Use Notion as the operational source of truth for the foundation phase.

Use this repository for versioned prompts, standards, schemas, architecture, deployment instructions, decisions, and synthetic examples.

## Consequences

### Positive

- Fast human review and configuration.
- Native support for the initial Notion contender.
- Clear separation between public contracts and private operational records.
- Platform-neutral schemas can be developed before automation code exists.

### Negative

- Notion calculations and automation may be less deterministic than a dedicated service.
- Cross-platform contenders may require connectors or external orchestration.
- Exports and synchronization must be designed carefully to preserve IDs and append-only history.

## Review trigger

Revisit this decision when the project adds executable scoring code, automated market-data ingestion, frequent API-based contenders, or a private data warehouse.
