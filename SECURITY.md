# Security and Financial-Action Boundary

## Simulation-only scope

This project is a benchmark and paper-market simulation. It is not a brokerage integration, investment service, financial adviser, or live-trading system.

No component may:

- open or connect a brokerage or exchange account;
- accept terms of service or select a paid tier on behalf of a person;
- transfer, deposit, withdraw, borrow, or pledge funds;
- submit, modify, cancel, or recommend mirroring a live order;
- store brokerage credentials, API secrets, payment data, or account identifiers;
- imply that a hypothetical action occurred in the real world.

Brokerages, subscriptions, data plans, fills, spreads, fees, taxes, and positions are modeled as fictional costs and events only.

## Secrets

Never commit:

- API keys or personal access tokens;
- Notion integration secrets;
- paid-data credentials;
- account numbers;
- authentication cookies;
- private connector exports;
- personally identifying financial information.

Use environment variables or an approved secrets manager for future private automation. Provide `.env.example` files with names only, never values.

## Public repository constraints

While this repository is public, it may contain reusable standards, prompts, schemas, synthetic examples, and architecture decisions. It must not contain current private contender outputs, unpublished hypotheses, live watchlists, or raw operational Notion exports.

## Reporting a concern

Do not publish a suspected secret or sensitive record in a public issue. Contact the repository owner privately and rotate any exposed credential immediately.
