# 05_EXAMPLES_GOLDEN - Canonical Classification Examples

Purpose: canonical examples to prevent taxonomy drift.

## Example 1 - GitHub Framework With Strong Idea But Poor Implementation Fit

Collection: `20_LIBRARY`

Tags:

```text
source/github, type/framework, domain/agents, stack/kotlin, authority/source-code, authority/vendor-claim, truth/plausible, status/core-good, risk/ecosystem-mismatch, fit/dev-heavy, next/extract, scenario/power-user
```

Note:

```text
Cataloged: YYYY-MM-DD
Verdict: core idea valuable, implementation not practical now.
Next: extract pattern, do not adopt the tool.
Claim: framework for structured multi-step agents.
Evidence: source code and examples exist, but limited evidence of daily use.
Authority: source-code plus vendor-claim.
Truth: plausible.
StackFit: poor implementation fit due to stack/setup friction; useful as idea extraction.
```

## Example 2 - GitHub Guide Or Docs

Collection: `20_LIBRARY`

Tags:

```text
source/github, type/guide, type/docs, domain/devtools, authority/source-code, truth/verified, status/reference, fit/vscode, fit/ai-assisted, next/revisit, scenario/learning
```

Note:

```text
Cataloged: YYYY-MM-DD
Verdict: keep as reference for future implementation.
Next: retrieve when implementing a similar workflow.
Claim: explains a workflow or technical pattern.
Evidence: docs and examples are clear and reproducible.
Authority: source-code/docs.
Truth: verified.
StackFit: usable with editor and AI assistance.
```

## Example 3 - Product, Service, Or API Directory

Collection: `20_LIBRARY`

Tags:

```text
source/github, type/directory, domain/automation, authority/vendor-claim, authority/community, truth/plausible, status/reference, fit/discovery-only, fit/account-required, fit/paywall-risk, risk/vendor-bias, next/extract
```

Note:

```text
Cataloged: YYYY-MM-DD
Verdict: useful for capability discovery, not direct adoption.
Next: extract candidates only when a workflow requires them.
Claim: directory of services or APIs for workflow capabilities.
Evidence: large curated list and traction, but individual services are not verified.
Authority: vendor-claim plus community signal.
Truth: plausible as directory, unknown for individual entries.
StackFit: discovery-only; every candidate must be checked for real free tier, no-card use, setup friction, and current community reports.
```

Rule: new classifications should imitate these examples before creating new tags.
