---
name: preflight
description: Prepare complex or inherited projects for execution by reconstructing intent, inspecting source artifacts and live state, repairing the durable plan, challenging it as a blank reader, and producing a readiness verdict plus frozen execution brief. Use when Landon says “preflight this,” asks whether a project is ready to build or launch, wants a plan or handoff checked before a foreman, builder, or long-running agent starts, or inherits messy or contradictory project context.
---

# Preflight

Turn scattered context into a verified plan and execution handoff. Do not turn preflight into implementation or project-management ceremony.

## Hold the boundary

- Treat planning and execution approval as different facts. Record evidence for authorization.
- Stop at the launch gate unless Landon has already approved execution of the current scope.
- Never infer authority for third-party communication, spending, deletion or data loss, public release, or access expansion. Name later confirmation points in the plan.
- Resolve safe, reversible planning uncertainty without asking. Keep checks proportional.

## Load the real record

Read supplied conversations, files, plans, handoffs, feedback, and current-state notes. Find the canonical home and read before rewriting.

For Landon's projects, use the Brain as a personal-context adapter:

1. Read the Brain `README.md`, Bible, `now.md`, and relevant project snapshot.
2. Follow its canonical-home, write-lane, write-ritual, one-fact-one-home, and landing rules; do not copy them into project artifacts.
3. Keep live actions on the task system and durable continuity in the Brain.

Keep the core agent- and provider-neutral; label platform adapters. If a missing source could change the verdict, name the blocker.

## Keep facts straight

Separate **verified facts** (observed), **settled decisions** (explicitly chosen, with reasons), **assumptions** (unverified, with consequence and check), **open questions** (outcome-relevant, with their gate), and **recommendations** (preflight judgment).

When sources conflict, prefer direct current observation over narrative, a canonical source over a copy, and a later explicit decision over an earlier proposal. Repair the durable record and mark the stale direction superseded.

## Run the preflight

### 1. Reconstruct intent and success

- State what will be different, for whom, and why it matters.
- Reconstruct scope changes; exclude rejected alternatives and stale instructions.
- Define observable success, non-goals, and the boundary between preflight and execution.
- Check traceability both ways: every named outcome and committed deliverable needs a pass condition and retained evidence; every deliverable or test must trace to a real need, constraint, or success measure.
- Flag incompatible goals instead of smoothing them into vague language.

### 2. Collect artifacts and inspect live state

- Inventory plans, decisions, assets, outputs, feedback, tasks, and in-flight work. Find missing, duplicated, obsolete, or unresolved pieces.
- Inspect the actual environment to the extent the project requires. For technical work, check relevant repositories, branches, dirty work, dependencies, versions, integrations, permissions, schedules, tests, data, and concurrent changes. For non-technical work, check the real documents, dates, people, inventory, vendors, commitments, and approval path.
- Verify checkable facts. Use read-only checks, reversible probes, or primary/official research only when it can change readiness.
- Compare the live result with plan claims. Treat a contradiction as a finding to resolve, not a footnote.
- Confirm the decision owner, required operators, access, time, cost, and abort authority when they affect feasibility.

### 3. Review only material gaps

Consider these failure classes, applying only what fits:

- unclear outcome, scope, non-goal, or acceptance evidence;
- untested approach, missing capability, incompatible environment, or unrealistic timing;
- hidden dependency, conflicting work, missing owner, external lead time, or brittle sequence;
- vague phase, missing deliverable, unclear destination, or verification detached from requirements;
- irreversible step, missing known-good state, no stop condition, or unproven recovery;
- missing owner, duplicated process, privacy/security exposure, hidden cost, or unapproved external action.

For each real gap, record evidence, consequence, owner, and disposition: resolve now, add to the plan, ask Landon, accept as a noted risk, or block launch. For a retained material risk, state mitigation, trigger, contingency, and owner.

### 4. Ask only material questions

Ask only when all three are true:

1. The answer is not discoverable from available sources or a safe check.
2. A reasonable assumption could change outcome, authority, cost, safety, scope, or architecture.
3. Work cannot progress by documenting the assumption and deferring the decision.

Group surviving questions, explain what each changes, and recommend a path when supported. If one blocks only a branch, finish the rest. Never ask ritual questions.

### 5. Repair the durable plan

Update the canonical plan when possible; create one only when none exists. Write for a blank reader.

Ensure the plan contains, in proportion to the project:

1. outcome, reason, measurable success, scope, and non-goals;
2. verified current state and authoritative sources;
3. settled decisions, assumptions, and remaining material questions;
4. phases, dependencies, roles, deliverables, and canonical destinations;
5. acceptance criteria mapped to method, pass threshold, and retained evidence;
6. stop conditions, known-good state, rollback or recovery, and validation after recovery;
7. relevant deadlines, costs, privacy/security limits, maintenance owner, and actions requiring confirmation;
8. first action, launch sequence, and definition of done.

Do not rely on a conversation, temporary path, unstored attachment, or unexplained local state. Do not create a parallel plan or status surface.

### 6. Freeze the execution brief

Create a self-contained, date-stamped brief in the canonical home. Link to the plan rather than copying changing detail. Exclude exploration and tool noise.

Include:

- outcome and definition of done;
- current state and authoritative sources;
- scope, non-goals, settled decisions, and constraints;
- authorization boundary and actions reserved for Landon;
- phased deliverables, dependencies, acceptance checks, and recovery requirements;
- first action, escalation conditions, and reporting contract;
- capability-routing policy, including any configured, inherited, automatic, or untested model, latency, reasoning, or cost constraint.

The brief must let a new agent locate inputs and outputs, begin without hidden context, and prove completion.

### 7. Challenge and decide

Use one independent fresh agent when available. Give it only the plan, brief, and referenced artifacts—not the conversation or expected verdict. Keep it read-only and ask:

- What is the outcome and first action?
- Does every outcome and deliverable have a concrete pass condition and evidence?
- What requirement, dependency, authority boundary, contradiction, or recovery step is missing?
- Could execution finish without guessing or hidden context?

The verifier must be at least as capable as the author. Keep one writer per artifact; the preflight owner integrates fixes. If unavailable, perform the same cold read and disclose it.

Use exactly one verdict:

- **READY:** No launch blocker; live state supports the approach; plan, brief, evidence, authority boundary, and recovery are complete.
- **READY WITH NOTED RISKS:** No launch blocker; named residual risks are understood, owned, and need no Landon decision before launch.
- **NEEDS LANDON:** A material product, scope, cost, risk, or authority decision requires Landon. State only those decisions and what each changes.
- **BLOCKED:** Missing access, evidence, capability, dependency, or external state prevents a reliable plan or verdict. State the exact unblock condition.

If execution is not already authorized, stop and give the exact launch action Landon can approve. Never treat silence or earlier planning enthusiasm as approval.

If current authorization clearly covers the preflighted scope and the verdict is `READY` or `READY WITH NOTED RISKS`, hand the frozen brief to the available supervised-execution workflow. For Landon's personal plugin, invoke `$foreman` and preserve the planning task as architect. Do not execute the build inside preflight.

## Report to Landon

Keep the user-facing report short:

1. verdict;
2. what was directly verified;
3. what changed in the plan;
4. remaining decision, blocker, approval, or noted risk;
5. openable plan and brief links;
6. exact next action.

Put detail in the artifacts. Never claim `READY` from documents alone when relevant live state was not checked.
