# 01_SYSTEM_SPEC - Decision Rain Library Project

Purpose: defines the Decision Rain Library Project.

## Core Principle

Do not catalog links; catalog decisions.

The library stores links plus judgment:

- authority
- truth
- practical fit
- operational status
- risk
- next action

## Collections

`00_SYSTEM` = canonical rules and governance entries.

`00_INBOX` = unprocessed incoming links. Every new entry starts here, no exceptions.

`10_REVIEW` = links worth analysis before becoming decisions. The assistant processes here; the operator validates.

`20_LIBRARY` = evaluated and operator-validated decision entries only.

`90_ARCHIVE` = rejected, outdated, duplicated, inactive, or historical entries.

## Ingestion Flow

1. New link arrives -> saved to `00_INBOX` with `status/pending-review` and one `next/*` tag.
2. Assistant processes -> fills full note template, proposes tags and collection.
3. Operator validates -> promotes to `10_REVIEW` or directly to `20_LIBRARY`.
4. If rejected or obsolete -> moves to `90_ARCHIVE`.

Never skip INBOX.
Never save a fully evaluated entry directly to `20_LIBRARY` without operator validation.

## Required Read Order

Before classifying or updating serious bookmarks, read `00_AGENT_CONTRACT` first, then entries `01` to `05` in order.

## Serious Entry Requirements

A serious evaluated entry must include:

- one collection
- `status/*`
- `type/*`
- `domain/*`
- `truth/*`
- `fit/*` when adoption is relevant
- `next/*`
- `Cataloged` date
- concise note in template format

Raindrop stores the system.
The assistant applies the system through Raindrop MCP or another authorized Raindrop integration.
