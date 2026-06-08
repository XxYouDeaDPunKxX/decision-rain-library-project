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

## Technical Notes

Raindrop requires every bookmark to have a URL. The SYSTEM documents can use placeholder URLs because the useful content lives in the bookmark excerpt.

The assistant should read SYSTEM entries from Raindrop before doing serious review work. The intended read order is:

```text
00_AGENT_CONTRACT
01_SYSTEM_SPEC
02_TAG_REGISTRY
03_DECISION_RULES
04_NOTE_TEMPLATE
05_EXAMPLES_GOLDEN
06_USAGE_FLOW
```

If the assistant cannot read the SYSTEM entries, it should stop and ask for access instead of guessing the rules.

If you use remote MCP or a custom connector, the connector description should only bootstrap the assistant. The real rules should live in `00_SYSTEM`.

Keep private bookmark data out of this repository. This repository is only the skeleton and template.

</details>
