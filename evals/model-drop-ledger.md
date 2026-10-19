# The model-drop ledger

> **Editorial scaffolding:** everything below the verbatim section is an implementation of Matt's stated intent, written
> for an agent on any machine where Matt works. It is not Matt-authored doctrine. The verbatim section is his wording,
> transferred unedited. No personal, property, financial or employer specifics are included; those live in the
> relevant private workspace.

## Verbatim (Matt Ricci)

> *"a massive list of things that get checked and tested every time a new model drops. Could be kind of neat as a
> way to QA all my stuff on some cadence as well as test new model capabilities"*

> *"keep a plan of all things to qa and test unlocks on"*

> *"Can we make it a benchmark and eval system too? Where I can keep records on how it all goes, based on what
> model is doing it?"*

**Provenance:** Matt Ricci, Claude Code chat, 2026-10-17.

> *"let's keep a running list of things that agents just can't fully do yet, and have THAT get tested every time too."*

> *"look at my entire agent operation system and recommend how to improve it. That means: should I refactor anything
> on my computer, my file system? Should I be using a different harness? Is anything stale? Should I use different
> tools or services or connectors? That's a big one, and ever changing, and useful to me"*

**Provenance:** Matt Ricci, Claude Code chat, 2026-10-18.

---

## Editorial scaffolding: the pattern

**One list, three uses.** A model-drop ledger is a single inventory of everything in a role or a life worth checking
whenever a new frontier model ships, used three ways:

1. **QA sweep.** Is each thing still correct? Read-only.
2. **Unlock test.** Can the current model own this item? Record a ladder level: 🔴 human-only · 🟡 model drafts, a
   human approves · 🟢 end to end · ⛔ never automated, by policy.
3. **Benchmark.** Frozen cases with a known right answer, scored identically on every model, one row per
   (case × model × run).

**Cases come from work you already did.** The best benchmark is not a synthetic task. It is a thing you (or a model
under your supervision) already completed, with the real inputs frozen and the real outcome as the answer: a filing,
a reconciliation, a review, a set of recommendations, a draft graded against what you actually sent. If you have ever
run the same task under two models, you already have two scoreboard rows; write them down.

**Cases must be hard.** A case any current model passes measures nothing. Pick the things you hesitate to delegate:
the subjective ones, the money ones, the ones that need taste or physical presence or a judgment call you would want
to review.

**Every incident becomes a case.** When something goes wrong, freeze the inputs and the right answer. The benchmark
grows from your own operations, not from a framework.

**Include impossible tasks.** At least one case where the right answer is "nothing exists, and here is exactly what
I checked", and one where the answer is partial and easy to over-claim. An invented citation, quote, path or number
fails the whole run, whatever else scored.

**Keep a can't-yet register.** A running list of what agents cannot fully do today, each row marked *capability gap*
or *policy*, with the blocker, the harness (or human) that can do it today, and the unlock condition. Re-test every
open row on every run. Move passed rows to an *unlocked* table with the date and model, so the register shows movement.
The "why not 🟢 yet" column is the product: over time it maps what holds models back in this role.

**Keep standing reviews, not just cases.** Some items are never finished: a living decision re-scored with fresh
numbers, and the **agent-operations review** itself (should anything be refactored, is any job on the wrong harness,
what is stale, which tools or connectors to add, drop or swap). Score these by what the human accepts, not by what
the model said.

**Inventory the operation first.** Before cases, write the one table of every harness, model seat, loop, clock,
connector and tool, with what each owns and its ladder level. Every run diffs that table against reality and hunts
for sprawl. The inventory is also what a future consolidation is built from.

**Run it** on every new frontier model and on a fixed cadence. Write scope during a run: **read + draft only**. Run
cases cold (a fresh session that sees only the case). Proposals come back as one numbered list the human answers
positionally.

**Keep records.** One row per (case × model × run): date, model, score, ladder level, rule violations, fabrications,
time and cost, grader. One summary line per run: what improved, what newly unlocked, what still blocks.

**Keep the specifics private.** The ledger, the cases, the scoreboard and the register live in the sanctioned
workspace for that context. Only this pattern is public.

## Editorial scaffolding: going deeper at work

A function lead who owns AI and product has more loops, more context, and a higher burden to understand what a new
model changes. The same pattern, heavier:

- **Inventory the loops you own as a function**, not just your own: every recurring report, review, ritual,
  pipeline, agent, evaluation, vendor integration and team-run automation. Who owns it, what model or vendor it runs
  on, what it is allowed to write, how it is measured.
- **Ladder every item**, and record the blocker for anything not 🟢: missing API, permission, policy, judgment, risk,
  cost, regulatory posture.
- **Every incident becomes a case**, including the ones your team hits. The scoreboard becomes the function's shared
  memory of what models could and could not do, by date.
- **Add an "impact of this model" section per drop**: what it changes for the roadmap, for cost, for the safety and
  compliance posture, for which vendor or build decision should be revisited. This is the part only the function lead
  can write, and it is the reason to run the ledger within days of a release rather than months.
- **Standing reviews**: the function's agent-operations review (harness, tooling, connectors, staleness), plus any
  living decision the function keeps re-scoring.
- **Grade by acceptance.** A recommendation nobody acted on is not a point.
- **Specifics stay in the employer's workspace.** Only the pattern travels.

## Editorial scaffolding: bootstrap prompt for a new machine

> Paste into an agent on a machine that has no personal context. It builds the ledger in 30 days.

```
You are setting up a model-drop ledger for this role. In the first 30 days:
1. Inventory every recurring piece of work I own or that my function runs: reports, reviews, rituals, pipelines,
   agents, automations, vendor integrations. One row each: owner, surface, trigger, what it writes, how it is
   measured, which model or vendor runs it today.
2. Give each row a ladder level (🔴 human-only · 🟡 model drafts, human approves · 🟢 end to end · ⛔ never by policy)
   and, for anything not 🟢, the blocker.
3. Start a can't-yet register from those blockers; mark each as capability or policy.
4. Find work I already completed that a model could be graded on, freeze the inputs and the real outcome as cases,
   and prefer the hard ones. Add one impossible case and one partial-answer case.
5. Create a standing agent-operations review and any living decisions this role keeps re-scoring.
6. Write the run protocol: read + draft only, cold sessions per case, numbered proposals, one scoreboard row per
   case × model × run, one summary line per run, an "impact of this model" section.
Then run it once on the current model as the baseline, and again on every new frontier model and on a fixed cadence.
Keep everything in this workspace; nothing leaves it.
```
