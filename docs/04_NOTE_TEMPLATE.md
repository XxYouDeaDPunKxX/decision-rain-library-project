# 04_NOTE_TEMPLATE - Decision Entry Format

Purpose: defines the note format for evaluated entries.

## Anti-Truncation Rule

Verdict and Next must appear within the first 3 lines.
Raindrop may truncate long excerpts; critical fields must never be at the bottom.

## Compact Template

Use this compact template for serious entries:

```text
Cataloged: YYYY-MM-DD
Verdict: practical judgment in one or two sentences.
Next: next action, such as use now, test, extract pattern, watch, reference only, archive.
Claim: what the link appears to provide or prove.
Evidence: what supports the claim, such as README, source code, docs, issues, tests, release activity, community use, pricing, setup reports, or hands-on test.
Authority: what kind of authority supports it; keep official and community evidence separate when both matter.
Truth: verified, plausible, claimed, conflicting, outdated, or unknown.
StackFit: practical judgment of how realistically the operator can get value from the item. Consider value type, operator capability, adoption cost, friction threshold, and decision path. Mention whether the item is for direct use, test, assisted implementation, workflow integration, idea extraction, reference, discovery, watch, or archive.
```

## Style Rule

Concise, decision-oriented, no essay unless deep dive is explicitly requested.

## Operational Rule

If StackFit is bad, do not call it ready; use core-good, watch, later, reference, or rejected.

## Gate Rule

The note is a proposal until the operator validates it.
