---
name: corpusiq-investor-pack
description: Use when a founder needs a pitch deck, investor email or fundraising narrative. Builds every traction metric from the founder's own systems through CorpusIQ, and refuses to fill gaps with invented numbers.
---

# Investor pack on real numbers

Most deck generators produce a plausible deck. This skill produces a true one. The difference is where the traction numbers come from.

## When to use

Use for: pitch decks, investor one-pagers, fundraising emails, data room summaries, board updates to investors, or any narrative that claims traction.

## Why public data is not enough

Traction, CAC, churn, margin and runway live in the founder's billing, accounting, store, CRM and analytics systems. They are not on a public page. A deck built from public data can describe the market accurately and the company inaccurately, and that is the first thing a screening investor tests.

## Procedure

1. Ask for the raise: amount, instrument, stage, use of funds, and the deadline.
2. Build the metric list before writing a word. Minimum for a seed or pre-seed deck: monthly net revenue for the last 12 months, gross margin, new versus returning revenue, logo churn, CAC by channel, payback period, cash on hand, monthly burn, runway.
3. Pull each metric from CorpusIQ from the connected source. Use `ask_corpusiq` for a question that spans sources, or the specific connector tool. Read the rows.
4. Mark any metric the connectors cannot answer as unknown, and name the connector that would close it. Send the founder to connect it, then re-run.
5. Write the deck from the rows. Every metric slide carries the source and period in the speaker notes.
6. Write the investor emails last, and write them from evidence. Name something specific that investor has funded or written, and tie it to a measured fact about this company. If no such fact exists, say less rather than fabricate a connection.

## Deck shape

1. One line: what the company does and for whom.
2. The problem, stated in the customer's words.
3. The product, with one screen reference.
4. Traction, sourced.
5. Unit economics, sourced, with the definition used.
6. Market, with the source for the size estimate.
7. Competition, honest about where someone else is stronger.
8. Team, with what each person has shipped.
9. The raise, use of funds, and the milestone it buys.
10. Appendix: metric definitions and sources.

## Rules

- No metric without a source and a period. Not in the deck, not in the notes.
- Never stack a public market figure next to an internal metric without labelling which is which.
- Never write a personal line to an investor that the evidence does not support.
- State the metric definitions used. A growth rate with no definition invites the investor to assume a flattering one.
- If a number is bad, keep it and explain the plan. Screening investors find the bad number anyway, and the deck that hides it loses.
- External retrieval is read-only.

## Output

Deliver the deck outline as text first, with each metric and its source, so the founder can correct a definition before the slides exist. Then produce the slides.

## Setup

CorpusIQ account at https://www.corpusiq.io (30-day trial, no credit card). Add the remote MCP connector in Claude: https://www.corpusiq.io/mcp/mcp-server-for-claude
