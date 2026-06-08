# 03_DECISION_RULES - Authority Truth Status Fit Next

Purpose: defines decision rules.

## Status Rules

`status/dissect` = deserves close analysis now.

`status/ready` = usable or applicable with low ambiguity and acceptable StackFit.

`status/later` = useful but not current priority.

`status/core-good` = core idea is valuable even if implementation or StackFit is not practical.

`status/watch` = monitor maturity, pricing, maintenance, ecosystem, access constraints, or community friction.

`status/rejected` = evaluated and not worth using except as historical evidence.

`status/reference` = useful mainly as reference, documentation, directory, or learning material.

`status/pending-review` = assistant has processed and saved this entry, but the operator has not yet validated it. Do not treat as canonical until the operator confirms.

## Next Rules

Always add one `next/*` tag per evaluated entry. Choose the most specific action.

`next/test` = try it in the operator environment now.

`next/spike` = timeboxed exploration with unknown outcome.

`next/extract` = pull the pattern or idea, do not adopt the tool itself.

`next/revisit` = park with intent to return, not passive archiving.

`next/archive` = move to `90_ARCHIVE`, evaluation complete.

`next/deploy` = ready to integrate into active workflow.

## Authority Rules

`authority/official` = official docs, maintainer statement, product page.

`authority/source-code` = code, examples, tests, commits.

`authority/community` = issues, discussions, Reddit, HN, forum signals.

`authority/vendor-claim` = marketing, README promise, sales copy, unverified claim.

`authority/internal` = internal rule, operator context, or validated local judgment.

## Truth Rules

`truth/verified` = confirmed by primary evidence, working test, or strong corroboration.

`truth/plausible` = likely true but not tested enough.

`truth/claimed` = asserted but not verified.

`truth/conflicting` = credible sources disagree.

`truth/outdated` = likely stale or obsolete.

`truth/unknown` = not enough evidence.

## Fit Rules

Never mark `status/ready` unless fit is acceptable and the operator has validated the decision.

A project can be `status/core-good` if the idea is strong but implementation fit is bad.

Directories and mega-lists often use `fit/discovery-only`.

Poor implementation fit does not mean worthless; it may mean extract, reference, watch, or later.

Always separate Claim from Evidence before Verdict.

When official and community evidence conflict, surface the conflict before deciding.
