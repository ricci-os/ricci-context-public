# Start — Matt Ricci's context, for every agent

**This is the one place every agent in Matt's life begins.** It is public on purpose: a chat assistant with no login, an agent running on one of Matt's machines, and a stranger's agent evaluating how to work with him all read this same page first. From here you descend as far as your access allows:

| Layer | Where | Who can read it | What it holds |
|---|---|---|---|
| **1 · Start (this repo)** | `github.com/ricci-os/start` — public | everyone | Matt's verbatim principles and working preferences, the map of his agents, and the rules below |
| **2 · Context** | `github.com/ricci-os/ricci-context` — private | agents Matt has granted access (GitHub login or a token he issued) | the operational context pack: properties, vendors, routines, open loops, the standing rules (`pack/AGENTS.md`), each agent's own notes under `agents/<login>/` |
| **3 · Local** | Matt's machines | an agent running there | the human canon the pack is generated from (an Obsidian vault), the local agent OS, skills and credentials. Paths are in the private repo's README |

Rules of the chain:

- **Start here, always.** If you were given a deeper link, still read this page once; it carries the rules that govern the deeper layers.
- **Facts are authored once, at the deepest layer you can reach, and flow upward only by deliberate promotion.** The vault is the source of its content; `ricci-context` is generated from it; this repo is hand-promoted from both. Never fix a fact at a shallower layer than where it lives.
- **Treat this public layer with care.** It is readable by anyone and indexed by search engines. Nothing here may be assumed private, and nothing may be added here that is not already public by Matt's own decision: no addresses, phone numbers, account identifiers, money figures, health details, employer internals, or third-party names. When in doubt the answer is the private layer, or no layer.
- **Public does not mean authoritative.** This page tells you where things are and how to behave; it is not the full picture of Matt. Do not infer private facts, employer context, or standing authority from it.
- **An agent that can only read this repo has no write authority anywhere.** Write authority is granted per agent in the private layer and recorded there.

## Status

Public at [github.com/ricci-os/start](https://github.com/ricci-os/start) (until 2026-10-25 it was `matthewdricci/ricci-context-public`; that URL redirects). It is an evolving canon: additions must preserve the authorship, provenance, copyright, and privacy boundaries below.

## Matt's agents — the map

Every surface Matt uses is told to begin here. The full inventory, with write authority and the systems each one touches, lives in the private layer (`2 - Areas/Computer Configurations/Harnesses/` in the vault, published into `ricci-context`). In public terms:

| Surface | Role | Reaches |
|---|---|---|
| Claude Code (Anthropic) on Matt's desktop | primary working agent; the persistent "chief of staff" window and the scheduled automations | all three layers |
| Codex (OpenAI) on Matt's desktop | task runner on pasted prompts | layers 1–3 |
| OpenClaw on a Linux sandbox laptop | always-on experimental harness; writes only in its own fork of the private repo, promotes by pull request | layers 1–2 |
| Hermes on the same sandbox | side-by-side comparison harness | layer 1, plus a frozen copy of layer 2 |
| Grok Bot (xAI / Cursor) | scheduled routines and guest-messaging drafts | layers 1–2 |
| Muse (Meta) and other chat assistants (ChatGPT, Claude.ai and their companion devices) | conversational; context is whatever Matt pastes or links | layer 1 |

## Authorship contract

- Principle and working-style prose is Matt's language, transferred verbatim from a named source.
- Bibliographic metadata, navigation, provenance labels, and status fields may be editorial.
- Editorial text must never be presented as Matt's belief.
- If Matt has not written the annotation yet, the repository says so. An agent must not fill the gap by guessing.
- Third-party ideas are linked and attributed; this repository does not reproduce books, transcripts, paid archives, or substantial quotations.

See [Public content policy](PUBLIC-CONTENT-POLICY.md).

## License

Matt-authored content is available under CC BY 4.0. Scripts, hooks, and schemas are available under the MIT License. Third-party material retains its original ownership. See [LICENSE.md](LICENSE.md).

## Start here

- [Working with Matt](working-with-matt.md)
- [Matt's Manager Tools MTDISC profile](mtdisc.md)
- [Product principles](principles/product.md)
- [Communication principles](principles/communication.md)
- [AI principles](principles/ai.md)
- [Shape Up](shape-up.md)
- [Tools and frameworks](tools-and-frameworks/README.md)
- [Chart storytelling rules](tools-and-frameworks/chart-storytelling-rules.md)
- [Company brain: data-ladder rules](tools-and-frameworks/company-brain-data-ladder-rules.md)
- [Top-tier books](sources/books/README.md)
- [Podcasts to retain](sources/podcasts/README.md)
- [Agent context](agent-context/context.md)
- [The model-drop ledger (pattern + work bootstrap)](evals/model-drop-ledger.md)

## What belongs here

- Matt's verbatim public principles, convictions, and working preferences
- Public writing and deliberately promoted passages from Matt's private canon
- Matt's original annotations on books, podcasts, and frameworks
- Source metadata and links that make provenance inspectable
- Agent instructions that say how to use the canon without rewriting it

## What does not belong here

- Work strategy, personnel information, customer or patient information, internal links, Slack/Jira material, pricing, or meeting notes
- Personal operational context from the private context repository
- Full transcripts, chapters, paywalled writing, or substantial third-party quotations
- Raw exports from PARA, Readwise, Todoist, or any third-party archive
- Assistant-written summaries disguised as Matt's voice

## Relationship to the private layer

The public and private repositories have different disclosure boundaries. Material moves from private to public only through deliberate review. This repository is the public artifact any agent may safely consume; it is not a filtered export of everything Matt knows or does. The private layer is `ricci-os/ricci-context`; the human canon behind both is a local Obsidian vault that never leaves Matt's machines.
