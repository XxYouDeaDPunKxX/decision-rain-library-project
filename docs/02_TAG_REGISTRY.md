# 02_TAG_REGISTRY - Controlled Tag Grammar And StackFit

Purpose: defines allowed tag grammar. Tags may grow, but only inside controlled families and only with operator approval.

## Allowed Families

`authority/*` = who or what supports the claim.

`truth/*` = confidence or state of truth.

`status/*` = operational decision.

`type/*` = what kind of object this is.

`domain/*` = topic or domain.

`source/*` = where it comes from.

`scenario/*` = usage scenario.

`risk/*` = adoption or trust risk.

`stack/*` = relevant technology stack.

`fit/*` = practical compatibility with the operator's real operating environment and adoption threshold.

`next/*` = next concrete action on this entry.

`priority/*` = optional operator attention marker, not a decision state and not a replacement for `status/*` or `next/*`.

## Status Values

- `status/dissect` = deserves close analysis now.
- `status/ready` = usable or applicable with low ambiguity and acceptable StackFit.
- `status/later` = useful but not current priority.
- `status/core-good` = core idea is valuable even if implementation or StackFit is not practical.
- `status/watch` = monitor maturity, pricing, maintenance, ecosystem, or access constraints.
- `status/rejected` = evaluated and not worth using except as historical evidence.
- `status/reference` = useful mainly as reference, documentation, directory, or learning material.
- `status/pending-review` = assistant has processed this entry but the operator has not yet validated it.

## Next Values

- `next/test` = try it in the operator environment.
- `next/spike` = timeboxed exploration, unknown outcome.
- `next/extract` = pull the pattern or idea, do not adopt the tool.
- `next/revisit` = park for later with intent to return.
- `next/archive` = move to `90_ARCHIVE`.
- `next/deploy` = ready to integrate into active workflow.

## Priority Values

- `priority/high` = operator attention marker for items that should stay visible.

`priority/high` does not mean ready, validated, urgent, or objectively more important.
Do not invent priority scales unless the operator approves them.

## StackFit Definition

StackFit is not a list of the operator's tools.
StackFit is the practical judgment of how realistically the operator can get value from an item.

Evaluate:

- value type
- operator capability
- adoption cost
- friction threshold
- final decision path

Value types include direct use, assisted implementation, workflow integration, idea extraction, reference, and discovery only.

Operator capability can include a local workstation, editor, AI assistants, GitHub, automation layers, and Raindrop as library backend.

Adoption cost includes dependencies, local tools, accounts, APIs, frameworks, service maintenance, unfamiliar ecosystems, payment, card, and billing risk.

Documented and assistant-assisted setup is acceptable.
Real free tier is acceptable.
Card traps, unclear billing, fake freemium, enterprise assumptions, or incompatible ecosystems lower fit.

Poor implementation fit does not mean worthless; use `next/extract`, `status/core-good`, `status/reference`, `status/watch`, or `status/later` when appropriate.

## Useful Fit Tags

- `fit/windows`
- `fit/vscode`
- `fit/ai-assisted`
- `fit/llm-chat`
- `fit/pipedream`
- `fit/automation-layer`
- `fit/mcp`
- `fit/local`
- `fit/free-tier-real`
- `fit/no-card`
- `fit/account-required`
- `fit/paywall-risk`
- `fit/freemium-risk`
- `fit/dev-heavy`
- `fit/discovery-only`
- `fit/owned-hardware`

Tool-specific fit tags may be added only when the operator needs that precision.
Prefer generic fit tags for public/shared templates.

Do not use `fit/raindrop` or `fit/browser` by default.
Raindrop is the library backend, not a fit tag.
Browser is a generic access surface, not a fit tag.

GitHub is a source, not a fit judgment.
A GitHub item may be code, docs, guide, pattern, directory, research, idea, example, or spark.

## Governance

No emotional free-form tags such as `cool`, `interesting`, `maybe`, `good`, `AI`, or `tool`.

Use interrogable tags such as:

- `truth/plausible`
- `authority/source-code`
- `status/core-good`
- `risk/overpromised`
- `fit/free-tier-real`
