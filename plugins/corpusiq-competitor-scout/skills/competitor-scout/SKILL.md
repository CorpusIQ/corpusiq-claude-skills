---
name: corpusiq-competitor-scout
description: Use when analysing a competitor, a rival's launch, pricing page or reviews. Pairs public competitor evidence with the user's own measured numbers from CorpusIQ, and separates what is known from what is assumed.
---

# Competitor scout with your own numbers

Public competitor research produces a confident document built on marketing pages. It tells the founder what the rival says about itself, not what the rival costs that founder.

## When to use

Use for: competitor teardowns, pricing comparisons, win and loss analysis, positioning reviews, board slides that include a competitive section.

## Procedure

1. Name the competitor and the exact question. "How do we compare to X" is too broad. "Why do we lose deals to X, and what does X charge" is a question.
2. Gather public evidence: pricing page, changelog, review sites, job posts, funding announcements. Record the URL and the date read for each claim.
3. Gather the same dimensions from the user's own systems through CorpusIQ: actual price paid by their customers, discount depth, win rate where a CRM tracks it, churn reasons, support volume by topic, and the features customers actually use.
4. Build a two-column comparison: competitor claim (with URL) against buyer-measured reality (with source).
5. Write the finding: the one thing the competitor does better, the one thing the data shows buyers care about that they do not do, and what to change.
6. If a dimension has no data on either side, mark it unknown. Do not infer a competitor's price, headcount or churn.

## Rules

- Never state a competitor's internal metric as fact. You can quote their public claim and date it.
- Never use the user's internal numbers in anything that will be published. Internal comparison is for internal decisions.
- One thing the competitor does better, always. A comparison where the user wins every row is not analysis, and the reader knows it.
- Churn reasons and win rates come from systems that track them. If the CRM does not capture loss reasons, that is the finding: the gap is the process, not the intelligence.
- External retrieval is read-only. Public pages are read, never scraped for private data.

## Output shape

1. The question, verbatim.
2. What the competitor claims, each claim with URL and date.
3. What the user's own data shows, each figure with source.
4. Where the two disagree, and which one the buyer experiences.
5. One recommendation, with the change it requires.
6. What is still unknown, and the connector or process that would answer it.

## Setup

CorpusIQ account at https://www.corpusiq.io (30-day trial, no credit card). Add the remote MCP connector in Claude: https://www.corpusiq.io/mcp/mcp-server-for-claude
