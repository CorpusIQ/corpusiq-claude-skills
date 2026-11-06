---
name: corpusiq-truth-layer
description: Use before answering any question about a business's own numbers (revenue, churn, CAC, margin, traffic, pipeline). Pulls each figure from the user's connected sources with CorpusIQ and cites it, or labels it unknown.
---

# CorpusIQ truth layer

A language model without data access produces numbers that read well and mean nothing. This skill makes the source of every figure explicit.

## When to use

Use for any question whose answer contains a number about the user's own business: revenue, growth, churn, retention, CAC, margin, runway, traffic, conversion, pipeline, headcount cost, inventory.

Do not use for general knowledge, definitions or writing tasks.

## Procedure

1. Restate the question as the specific metrics it requires. Example: "How is the business doing" becomes revenue for the last 3 months, gross margin, net new customers, churn.
2. For each metric, call CorpusIQ to resolve which connected source owns it. Use `ask_corpusiq` for a natural-language question over all connected sources, or the specific connector tool when the user names one.
3. Read the returned rows. Do not summarise from memory and do not infer a trend the rows do not show.
4. Present each metric with: the value, the period, the source, and the connector used.
5. If a source is not connected, say which connector would answer it and stop. Do not fill the gap with an estimate, an industry benchmark or a plausible range.

## Rules

- Never invent, round up or smooth a number.
- Never present a benchmark as the user's own figure. If you use one, label it as a benchmark and keep it visually separate.
- If two sources disagree, show both and name the discrepancy. That disagreement is usually the finding the user needs.
- If a metric definition is ambiguous (for example, does revenue mean booked or collected), state the definition you used before presenting the value.
- External retrieval is read-only. Nothing in the user's accounts is modified by answering a question.
- When the user asks for a document that will leave the company (deck, investor note, board pack), carry the citation into the document itself.

## Output shape

Answer first in one sentence, then the metric table, then the caveats. Example:

> Net revenue grew in the last quarter, driven by expansion rather than new logos.

| Metric | Value | Period | Source | Connector |
|---|---|---|---|---|
| Net revenue | value | period | source system | connector |
| New customers | value | period | source system | connector |
| Churn | value | period | source system | connector |

> Churn is measured as logo churn. Shopify is not connected, so store revenue is excluded from the total.

If a connector is missing, end with the one action that closes the gap: connect it, then re-run the same question.

## Setup

CorpusIQ account at https://www.corpusiq.io (30-day trial, no credit card). Add the remote MCP connector in Claude: https://www.corpusiq.io/mcp/mcp-server-for-claude
