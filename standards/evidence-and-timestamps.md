# Evidence and Timestamp Standard

## Core requirement

Every scored hypothesis and fictional position must be reproducible from the information available before its evaluation cutoff.

## Required timestamps

Record:

- run start and completion time;
- timezone;
- public-information cutoff;
- source publication time when available;
- source-data or quote time;
- journal submission time;
- fictional execution evaluation time.

Use ISO 8601 timestamps with an explicit offset. Store display dates and times in the user's preferred timezone, `America/Indiana/Indianapolis`.

## Source hierarchy

Prefer, in order:

1. exchange, regulator, issuer, brokerage, data vendor, or original publisher;
2. official filings, releases, documentation, and fee schedules;
3. reputable financial or technical reporting;
4. secondary summaries and aggregators;
5. promotional or community claims, clearly labeled and independently checked.

## Evidence categories

Every material statement must be identifiable as one of:

- observed fact;
- calculation;
- assumption;
- forecast;
- interpretation;
- unresolved uncertainty.

## Data integrity

Do not invent or interpolate precise prices, volume, fees, quotes, or timestamps.

When data sources conflict:

1. preserve both values and sources;
2. explain the likely cause;
3. choose the cohort's approved source or the more conservative assumption;
4. flag the record for referee review.

## Hindsight prevention

A hypothesis cannot be edited after its evaluation window begins. Corrections require a new entry that references the original. Original text, timestamp, and sources remain preserved.

## Unavailable data

If required data is unavailable, delayed, or paywalled, record the limitation. Do not replace missing evidence with a confident estimate.
