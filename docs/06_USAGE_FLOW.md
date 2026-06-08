# 06_USAGE_FLOW - Operating The Library

Purpose: describes the normal operating loop for a local/offline copy of the system.

## Daily Flow

1. The operator finds a signal: repository, tool, article, service, guide, idea, or research spark.
2. The assistant saves the original link to `00_INBOX`.
3. The assistant researches the item with available tools.
4. The assistant proposes classification, tags, Verdict, Next, and uncertainty.
5. The operator validates, corrects, or rejects the proposal.
6. The assistant updates and moves the entry only after validation.

## What Counts As A Signal

A signal is anything that may be worth later attention.

Examples:

- a GitHub repository
- a documentation page
- a product or API
- a guide
- a pattern
- a research project
- a workflow idea
- a directory of tools
- a small spark that may become useful later

The library does not require the operator to know why the signal matters at capture time.
The point is to preserve the trace, then turn it into a decision later.

## Decision Levels

Separate these levels:

- Signal: the item caught attention.
- Analysis: the assistant explains what it is, what evidence exists, and what is missing.
- Decision: the operator validates what to do with it.

Do not collapse these levels.
Saving a link is not a decision.
Analysis is not validation.
A clean-looking proposal is not validation.

## Recommended Maintenance

Periodically review:

- `00_INBOX` for unprocessed items
- `10_REVIEW` for pending decisions
- `20_LIBRARY` for entries whose `next/*` tag implies action
- `90_ARCHIVE` for obsolete or rejected items
- SYSTEM documents for taxonomy drift

Batch normalization should be rare, explicit, and traceable.
