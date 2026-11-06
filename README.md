# CorpusIQ Skills for Claude

Four Claude skills that turn a language model that guesses into a model that reads your own business numbers first.

A plain skill bundle can write a pitch deck, an investor email or a competitor brief. It cannot make those documents true, because the inputs live in your Stripe, QuickBooks, Shopify, HubSpot, GA4 and Search Console accounts, not in public data. These skills make the model pull the real numbers from your connected sources and cite them. Where a connector is missing, the skill says so instead of estimating.

## What is inside

| Skill | What it does |
|---|---|
| `corpusiq-truth-layer` | The base rule set: every business number must come from a connected source and carry a citation, or be labelled as unknown. |
| `corpusiq-investor-pack` | Builds a pitch deck and investor emails where traction, CAC, churn, margin and runway come from your own systems. |
| `corpusiq-competitor-scout` | Compares a competitor's public claims against your measured numbers, and names the gaps. |
| `corpusiq-monthly-review` | One blended monthly close across billing, accounting, store and analytics data, with the same metric defined the same way everywhere. |

## Requirements

- A CorpusIQ account: https://www.corpusiq.io (30-day trial, no credit card)
- CorpusIQ added to Claude as a remote MCP connector: https://www.corpusiq.io/mcp/mcp-server-for-claude
- At least one connected data source. External retrieval is read-only.

## Install as a Claude Code plugin

```
/plugin marketplace add CorpusIQ/corpusiq-claude-skills
/plugin install corpusiq-truth-layer@corpusiq
```

## Install as plain skills

Copy any folder under `plugins/*/skills/` into `~/.claude/skills/`, or upload its zip in Claude under Settings, Capabilities, Skills.

## Ground rule

Every skill here is instructed to stop and name the missing connector rather than produce a plausible number. A deck with a hole in it is worth more than a deck with an invented metric.

MIT licensed. Built by CorpusIQ.
