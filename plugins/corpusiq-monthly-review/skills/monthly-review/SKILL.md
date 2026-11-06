---
name: corpusiq-monthly-review
description: Use for a monthly or weekly business review, close, or board pack. Blends billing, accounting, store, CRM and analytics data through CorpusIQ so one metric is defined one way across every source.
---

# Monthly review with one definition per metric

Two systems will give you two revenue numbers. Neither is wrong. They count different things. This skill fixes the definition first, then pulls every source against it.

## When to use

Use for: monthly close, weekly review, board pack, investor update, operating cadence, or any report that combines more than one system.

## Procedure

1. Fix the calendar: the exact period, and whether it is calendar or fiscal.
2. Write the metric dictionary before pulling data. For each metric, one sentence defining it and one sentence naming its source of record. Example: "Revenue means collected payments net of refunds. Source of record: the billing system, not the accounting system."
3. Pull each metric from its source of record through CorpusIQ. Use `ask_corpusiq` for a question spanning sources, or the connector tool when precision matters.
4. Reconcile. Where two systems disagree, show both values, the difference, and the reason (timing, refunds, currency, fees). Do not average them.
5. Write the review: what changed, why, what it means, what to do next.
6. Keep the dictionary with the report. Next month uses the same one.

## Sections for the final report

1. Headline: three sentences on the state of the business.
2. Scorecard: metric, this period, prior period, change, source.
3. Revenue: new versus expansion versus returning, and what drove each.
4. Cost: the two or three lines that moved, and whether the movement is structural or one-off.
5. Customers: additions, losses, concentration risk.
6. Cash: balance, burn, runway, and the assumption behind the runway figure.
7. What to change next period: no more than three items, each with an owner.

## Rules

- One definition per metric, stated once, used everywhere in the report.
- No blended number the reader cannot rebuild from the scorecard.
- Percentage changes always carry their base. A 200 percent increase on 3 units is not a trend.
- If a source is not connected, the metric is missing, not estimated. Name the connector.
- Never use the user's internal numbers in external content of any kind.
- External retrieval is read-only. A review reads data, it does not write back.
- Percentages and deltas are computed, not estimated. If you cannot compute a figure exactly, show the inputs and let the reader see the arithmetic.

## Setup

CorpusIQ account at https://www.corpusiq.io (30-day trial, no credit card). Add the remote MCP connector in Claude: https://www.corpusiq.io/mcp/mcp-server-for-claude
