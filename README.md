# 💧 Decision Rain Library Project

Turn interesting links into reviewed decisions with Raindrop and ChatGPT.

For people who save repos, tools, docs, articles, products, or research sparks, then later forget why they looked interesting.

> **Independent project:** Decision Rain Library Project is an independent user-created template for organizing reviewed decisions around saved links. It is not affiliated with, endorsed by, or sponsored by Raindrop.io.

```text
save the link -> let ChatGPT inspect it -> decide later with context
```

## ✨ What This Is

Decision Rain Library Project is a small set of rules, tags, examples, and note templates for using Raindrop as more than a bookmark manager.

Instead of only saving links, you save a short review of:

- 🧠 what the link is
- 🔍 why it may matter
- ✅ what is known
- ❓ what is uncertain
- ➡️ what the next step should be

It is meant to work with ChatGPT or another AI assistant connected to Raindrop.

## 🧩 Why It Exists

Sometimes a link is not clearly useful yet.

It might be:

- 🧪 a GitHub repo with one good idea
- 🛠️ a tool that may fit a future workflow
- 📚 a guide you do not have time to read now
- 🌐 a product worth checking later
- 🗂️ a directory full of possible candidates
- 💡 a research spark that should not disappear

Saving it as a normal bookmark is often not enough. Later, you still have to ask: what was this, why did I save it, and what should I do with it?

This project gives ChatGPT a repeatable way to answer those questions before the link disappears into a pile.

## 🔁 How It Works

The basic loop is:

1. 🔗 You give ChatGPT a link.
2. 📥 ChatGPT saves the original link in Raindrop.
3. 🔎 ChatGPT reads the page, repo, docs, or available sources.
4. 📝 ChatGPT writes a short review: verdict, next step, claim, evidence, confidence, risks, and practical fit.
5. 🧭 You decide what to do with it.
6. 📦 The link moves into review, library, or archive.

The important part: ChatGPT can inspect and propose, but you decide.

## 🗃️ Collection Structure

Create a parent collection in Raindrop:

```text
Decision Rain Library Project
  00_SYSTEM
  00_INBOX
  10_REVIEW
  20_LIBRARY
  90_ARCHIVE
```

Use them like this:

- ⚙️ `00_SYSTEM` stores the rules and examples.
- 📥 `00_INBOX` stores new links before they are reviewed.
- 🔎 `10_REVIEW` stores links that need more thought.
- 📚 `20_LIBRARY` stores reviewed links you want to keep.
- 🗄️ `90_ARCHIVE` stores rejected, outdated, inactive, or historical links.

Every new link starts in `00_INBOX`.

## 🚀 Basic Setup

1. 🗃️ Create the collection structure above in Raindrop.
2. 📄 Add the files in `docs/` as SYSTEM entries in `00_SYSTEM`.
3. 🔌 Connect Raindrop to ChatGPT if your account supports remote MCP or custom connectors.
4. 🧠 Give ChatGPT a short description that explains how this Raindrop library should be used.
5. 🔗 Start by sending one link and asking ChatGPT to save it, inspect it, and propose a review.

The exact ChatGPT connector screens may change. Treat this as a direction, not a permanent step-by-step UI guide.

## 🔌 Suggested Connector Description

If you can add a custom description to the Raindrop connector, keep it short:

```text
Use Raindrop as a Decision Library backend, not as generic bookmarks.
New links should first be saved to 00_INBOX.
Before reviewing or moving links, read 00_SYSTEM.
ChatGPT may inspect and propose, but the user decides final placement, tags, and next steps.
```

## 📝 What ChatGPT Should Produce

For reviewed links, use this shape:

```text
Cataloged: YYYY-MM-DD
Verdict: short practical judgment.
Next: the next useful action.
Claim: what the link appears to provide.
Evidence: what supports or weakens that claim.
Authority: where the evidence comes from.
Truth: how confident the review is.
Practical fit: whether this is realistically useful for your situation.
```

The review should be short enough to scan later.

## 🧰 What You Customize

This template is not meant to be universal. Customize it before using it seriously.

The main things to adapt are:

- 🧩 your fit tags: what tools, accounts, devices, budget, and setup friction matter to you
- 🏷️ your domains: automation, writing, design, hardware, research, productivity, etc.
- 📦 your item types: repo, guide, paper, service, directory, pattern, tutorial, idea
- 📌 your priority markers
- 🧪 your examples
- ✅ your threshold for calling something verified, ready, or worth testing

Keep the rule simple: tags should help you find and decide later.

## 🧱 What This Is Not

This is not a complete personal knowledge system.

This is not a full knowledge base.

This is not an automation framework.

This is not a promise that AI can decide for you.

It is a small review system for links that may matter later.

## 🗺️ Docs Map

- ⚙️ `docs/00_AGENT_CONTRACT.md` - what the AI assistant may and may not do
- 🧭 `docs/01_SYSTEM_SPEC.md` - collection structure and core flow
- 🏷️ `docs/02_TAG_REGISTRY.md` - tag families and allowed values
- ✅ `docs/03_DECISION_RULES.md` - status, truth, authority, fit, and next-step rules
- 📝 `docs/04_NOTE_TEMPLATE.md` - note format
- 🧪 `docs/05_EXAMPLES_GOLDEN.md` - examples to copy
- 🔁 `docs/06_USAGE_FLOW.md` - day-to-day usage loop
- 📄 `examples/sample-entry.md` - one sample reviewed entry
- 🗃️ `templates/collection-structure.md` - collection layout
- 🔗 `templates/system-bookmark-links.md` - placeholder URL pattern for SYSTEM entries

---

## 🤖 AI-assisted development

This project was developed with AI assistance.

The project, documentation, and repository materials were shaped through human-directed work supported by AI tools during drafting, structuring, review, and refinement.

AI assistance does not make the project automatically correct, complete, or suitable for every use case. Read it, test it, and adapt it to your own context.

---

## 📜 License

This project is licensed under CC BY-SA 4.0: Creative Commons Attribution-ShareAlike 4.0 International.

See `LICENSE`.

---

<details>
<summary>🛠️ Technical notes</summary>

## 🧰 Technical Notes

This repository is a portable governance package for a link-decision library. It is not an application, package, plugin, or automation framework. The runtime is the combination of:

- Raindrop as the bookmark and collection backend;
- SYSTEM documents stored as governance entries;
- a human operator as the only validation authority;
- an AI assistant or connector that can preserve, inspect, research, and propose;
- external evidence sources used to evaluate saved links.

🎯 The main design goal is not knowledge capture. The goal is to preserve signals and turn them into reviewed decisions without letting the assistant silently convert guesses into canonical library state.

### 🗂️ Repository Surface

The repository contains the public skeleton of the system:

```text
README.md                         human-facing overview and setup
docs/00_AGENT_CONTRACT.md          assistant authority, gates, failure rules
docs/01_SYSTEM_SPEC.md             collection model and ingestion flow
docs/02_TAG_REGISTRY.md            controlled tag grammar and StackFit model
docs/03_DECISION_RULES.md          status, truth, authority, fit, and next rules
docs/04_NOTE_TEMPLATE.md           canonical evaluated-entry note shape
docs/05_EXAMPLES_GOLDEN.md         drift-prevention examples
docs/06_USAGE_FLOW.md              day-to-day operating loop
examples/sample-entry.md           sample evaluated entry
templates/collection-structure.md  Raindrop collection layout
templates/system-bookmark-links.md placeholder URL pattern for SYSTEM entries
```

There is intentionally no CI, build system, package manifest, deployment workflow, or GitHub Pages surface. Maintainers should not add these unless the project grows a real executable or site surface that justifies them.

### 🧱 Runtime Data Model

The live system is expected to exist inside Raindrop, not inside GitHub.

A normal decision entry is a Raindrop bookmark with:

- the original URL as the durable trace;
- one collection representing its lifecycle state;
- controlled tags representing source, type, domain, authority, truth, status, risk, fit, scenario, priority, and next action;
- a compact note or excerpt containing `Cataloged`, `Verdict`, `Next`, `Claim`, `Evidence`, `Authority`, `Truth`, and `StackFit`.

The GitHub repository provides the schema, rules, and seed documents. It does not contain the operator's private bookmark corpus.

A SYSTEM entry is different from a normal bookmark. It is a governance document stored inside the `00_SYSTEM` collection. Because Raindrop requires every bookmark to have a URL, SYSTEM entries may use stable placeholder URLs. For SYSTEM entries, the bookmark excerpt or note is the source of truth; the placeholder URL is only an addressable shell.

### 🔁 Collection State Machine

Collections are lifecycle states, not topical folders.

```text
00_SYSTEM  -> governance documents only
00_INBOX   -> preserved but not evaluated
10_REVIEW  -> analyzed or worth analysis, not necessarily validated
20_LIBRARY -> evaluated and operator-validated decisions
90_ARCHIVE -> rejected, obsolete, duplicated, inactive, or historical entries
```

Every new external signal starts in `00_INBOX`. This preserves the trace before analysis and prevents the assistant from pretending that capture equals classification.

The normal state transition is:

```text
signal -> 00_INBOX -> analysis proposal -> operator validation -> 10_REVIEW / 20_LIBRARY / 90_ARCHIVE
```

A direct write into `20_LIBRARY` is only valid after explicit operator validation. Previous similar approval, high assistant confidence, clean formatting, or strong source evidence do not count as validation.

### 🛡️ Authority Boundaries

⚖️ The assistant has proposal authority, not validation authority.

It may:

- preserve a new link;
- inspect official and community evidence;
- identify missing evidence;
- propose tags, collection, verdict, next action, risks, and alternatives;
- surface taxonomy gaps;
- recommend a decision path.

It may not, without operator approval:

- mark a decision as canonical;
- promote an entry into `20_LIBRARY`;
- archive an entry;
- change SYSTEM documents;
- create or use new tag values;
- normalize batches;
- overwrite existing decision notes;
- treat silence as approval.

This boundary is the core safety property of the project. Maintainers should preserve it even if they add automation later.

### 📚 Required SYSTEM Read Order

Before serious classification, update, normalization, or promotion, the assistant should read the SYSTEM entries in this order:

```text
00_AGENT_CONTRACT
01_SYSTEM_SPEC
02_TAG_REGISTRY
03_DECISION_RULES
04_NOTE_TEMPLATE
05_EXAMPLES_GOLDEN
06_USAGE_FLOW
```

`00_AGENT_CONTRACT` comes first because it defines authority boundaries and stop conditions. The tag registry and decision rules must be read before assigning final tags. Golden examples should be used to prevent taxonomy drift.

If the assistant cannot read SYSTEM entries from Raindrop, it should stop and report the access failure. It should not reconstruct rules from memory, repo names, README fragments, connector descriptions, or similar prior systems.

### 🏷️ Controlled Taxonomy

Tags are a constrained grammar, not free-form labels. The current approved families are:

```text
authority/* truth/* status/* type/* domain/* source/* scenario/* risk/* stack/* fit/* next/* priority/*
```

The system intentionally separates concerns:

- `source/*` describes where the item came from;
- `type/*` describes what kind of object it is;
- `authority/*` describes what supports the claim;
- `truth/*` describes confidence or evidence state;
- `status/*` describes operational decision state;
- `fit/*` describes practical compatibility with the operator's environment;
- `next/*` describes the concrete next action.

Do not collapse these into vague tags such as `interesting`, `good`, `AI`, or `tool`. Do not use `priority/high` as a substitute for status or next action. Do not treat GitHub as a fit judgment; GitHub is a source. Do not use Raindrop as a fit tag; Raindrop is the backend.

New tag values are allowed only through explicit operator approval. When a gap appears, the assistant should report the smallest proposed addition and wait before using it.

### 🔍 Evidence Model

The assistant should keep official and community evidence separate.

Official evidence includes documentation, README claims, source code, examples, tests, release notes, pricing pages, maintainer notes, and product pages.

Community evidence includes issues, discussions, forum reports, Reddit/HN signals, adoption friction, setup failures, pricing complaints, and breakage reports.

Official evidence describes intended behavior. Community evidence reveals operational friction. A useful decision note should not blur those two. If they conflict, the conflict must be surfaced before a verdict.

Truth states should follow the controlled vocabulary:

```text
truth/verified    primary evidence, working test, or strong corroboration
truth/plausible   likely true but not tested enough
truth/claimed     asserted but not verified
truth/conflicting credible sources disagree
truth/outdated    likely stale or obsolete
truth/unknown     insufficient evidence
```

### 🧩 StackFit Model

StackFit is a practical adoption judgment. It is not a list of the operator's tools.

A StackFit assessment should consider:

- value type: direct use, assisted implementation, integration, extraction, reference, discovery;
- operator capability: local workstation, editor, AI assistants, GitHub, automation layers, and supported connectors;
- adoption cost: dependencies, accounts, APIs, frameworks, unfamiliar ecosystems, billing, payment cards, maintenance;
- friction threshold: documented setup, real free tier, no-card use, account requirements, fake freemium, enterprise assumptions;
- decision path: use, test, spike, extract, reference, watch, revisit, deploy, archive.

Bad implementation fit does not automatically make an item worthless. It may still be `status/core-good` with `next/extract`, or `status/reference` with `next/revisit`. Conversely, a polished project is not `status/ready` unless StackFit is acceptable and the operator validates it.

### 📝 Note Format Contract

Evaluated entries use the compact note format in `docs/04_NOTE_TEMPLATE.md`.

`Verdict` and `Next` must appear near the top because Raindrop may truncate long excerpts. The note should optimize for later retrieval and decision recall, not for essay-style explanation.

The key invariant is:

```text
Claim != Evidence != Verdict
```

The claim states what the item appears to provide. Evidence states what supports or weakens the claim. Verdict states the practical judgment after considering authority, truth, risk, and StackFit.

### 🔌 Connector And MCP Behavior

A connector description should only bootstrap the assistant. It should not contain the full operating system. The canonical rules should live in `00_SYSTEM` so they can be inspected, versioned, corrected, and reused.

A minimal connector instruction should tell the assistant to:

1. treat Raindrop as the Decision Library backend;
2. save new links to `00_INBOX` first;
3. read `00_SYSTEM` before serious work;
4. propose but not validate;
5. ask before moving, archiving, normalizing, or changing taxonomy.

Connector implementations should be conservative about writes. Prefer a preserved pending entry over an overconfident classified entry. When read/write APIs are unreliable, report what was read, what was changed, and what still requires operator review.

### 🛠️ Maintenance And Extension Rules

Maintainers should preserve the smallest useful surface.

Good extensions include:

- additional golden examples for recurring classification patterns;
- small approved additions to tag values;
- clearer failure rules for a specific connector;
- improved note templates that keep the anti-truncation rule;
- migration notes when changing SYSTEM behavior.

Avoid adding:

- broad placeholder docs;
- generic community files with no operating need;
- CI for a Markdown-only repository;
- Pages unless there is a real documentation-site requirement;
- automation that bypasses operator validation;
- uncontrolled tags that make retrieval worse.

For batch normalization, define the exact target collections, fields to change, fields to preserve, sample transformation, and rollback risk before touching entries. Batch normalization should be rare, explicit, and traceable.

### 🔒 Privacy And Publication Boundary

This repository should not contain private bookmark data, saved-link notes, operator history, credentials, connector tokens, exports, or personal decision corpora.

Safe public material:

- schema and rules;
- blank templates;
- synthetic examples;
- placeholder SYSTEM URLs;
- documentation explaining the operating model.

Unsafe material:

- real private Raindrop exports;
- personal saved links with notes;
- assistant transcripts containing private decisions;
- API keys, connector credentials, cookies, or account identifiers;
- unpublished operator-specific taxonomy that exposes private workflows.

🧭 The repository is the skeleton. The live library is the private Raindrop corpus.

</details>
