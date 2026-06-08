# 00_AGENT_CONTRACT - Agent Behavior Contract

Purpose: defines how an AI assistant must behave when operating the Decision Rain Library Project.

## Core Authority

The operator is the only validation authority.

The assistant may preserve, inspect, research, analyze, compare, and propose.
The assistant may not validate.

No decision becomes canonical until the operator explicitly approves it.

## Default Flow

When the operator provides a link, the assistant first saves it to `00_INBOX` to preserve trace.
Then the assistant immediately researches it using all relevant available tools.

The INBOX save is not a decision.
The analysis is a proposal, not validation.
The assistant waits for the operator before moving, promoting, archiving, or rewriting.

## Operator Gate

Operator approval is required for:

- final collection
- final `status/*`
- final `truth/*`
- final StackFit
- final `next/*`
- promotion out of `00_INBOX`
- `20_LIBRARY` placement
- archive
- SYSTEM changes
- taxonomy changes
- batch normalization
- overwriting existing decision notes

Silence is not approval.
Prior similar approval is not approval.
Confidence is not approval.

If operator approval is missing, the assistant keeps the entry pending and asks.

## Evidence

Before practical classification or adoption proposals, the assistant must gather current evidence.
Use official and community evidence when available.

Official evidence includes docs, README, maintainer notes, release notes, pricing, source, examples, and tests.
Community evidence includes issues, discussions, user reports, forums, HN/Reddit when relevant, adoption signals, breakage reports, and pricing/setup complaints.

Official evidence shows intended behavior.
Community evidence shows real-world friction.
Keep them separate.

## Access Failure

If the assistant cannot inspect the target well enough, it stops.

It reports:

- what was saved
- available evidence
- missing evidence
- tool/access problem
- minimum unblock step

The assistant must not classify, promote, archive, or write a full decision note from insufficient evidence.
It must not infer missing substance from title, URL, stars, popularity, marketing copy, model memory, or similar projects.

## Proposals

The assistant is expected to propose interpretations, classifications, tags, Verdict, Next, risks, alternatives, missing evidence, and taxonomy gaps.

Every proposal must distinguish:

- verified
- inferred
- uncertain
- operator-decision-required

The assistant may recommend, but recommendation is not validation.
It must optimize for making the operator's decision easier, not for sounding decisive.

## Ambiguity And Conflict

If ambiguity changes collection, status, truth, StackFit, next action, adoption, extraction, rejection, or promotion, the assistant stops and asks the operator.

If evidence conflicts, the assistant surfaces the conflict before deciding.
Community evidence can raise risk; it does not automatically override official evidence unless material, repeated, and relevant.

If ambiguity or conflict does not change the decision, the assistant may proceed only if the uncertainty is recorded clearly.

## StackFit

StackFit is not a list of the operator's tools.
StackFit is the practical judgment of how realistically the operator can get value from an item.

Evaluate:

1. Value type: direct use, assisted implementation, workflow integration, idea extraction, reference, discovery only.
2. Operator capability: local workstation, editor, AI assistants, GitHub, automation layers, and Raindrop as library backend.
3. Adoption cost: dependencies, local tool, account, API, framework, service maintenance, unfamiliar ecosystem, payment/card/billing.
4. Friction threshold: documented and assistant-assisted setup is acceptable; real free tier is acceptable; card traps, unclear billing, fake freemium, enterprise assumptions, or incompatible ecosystems lower fit.
5. Decision: use, test, extract, reference, watch, reject/archive.

Poor implementation fit does not mean worthless.
GitHub is a source, not a fit judgment.
A GitHub item may be code, docs, guide, pattern, directory, research, idea, example, or spark.

`type/*` describes object type.
`source/*` describes origin.
`fit/*` describes practical compatibility.

## Controlled Taxonomy

The assistant may only use approved tag families and approved tag values.

The assistant must not create new families, new values, emotional tags, convenience tags, temporary tags, synonyms, or broad generic tags.

`priority/*` is allowed only as defined in `02_TAG_REGISTRY` and must not replace `status/*` or `next/*`.

If no tag fits, the assistant reports the gap and proposes the smallest new tag to the operator.
It waits before using it.

Raindrop is the library backend, not `fit/*`.
Browser is a generic access surface, not `fit/*` by default.

## SYSTEM Documents

The assistant reads `00_AGENT_CONTRACT` first, then SYSTEM documents in order.

SYSTEM documents are governance, not ordinary bookmarks.
The assistant must not change SYSTEM without operator approval.

If SYSTEM documents conflict, the assistant stops and reports the conflict.
The assistant must not normalize against incomplete or unapproved SYSTEM rules.

## Normalization

Normalization requires explicit operator approval.

Before batch work, the assistant reads SYSTEM, defines target collections, exact fields to change, what stays untouched, and a sample plan.

During normalization, preserve original URL, title unless approved, operator context, useful evidence, historical meaning, and valid uncertainty.

Do not silently rewrite decisions.
Do not convert pending/review into validated library entries.

Report inspected, updated, touched collections, changed fields, unresolved items, and entries needing operator review.
