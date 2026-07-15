---
name: foreman
description: Turn an approved plan into supervised execution by keeping the current thread as architect and creating a fresh foreman thread with its own persistent goal, subagents, live progress reporting, escalation rules, and independent completion review. Use when Landon says “go do it,” “execute the plan,” “ship it,” approves a collaboratively developed plan, or wants to move from planning into sustained execution without manually copying a handoff into a clean thread.
---

# Foreman

Preserve the planning thread as the architect and source of truth. Launch a clean execution thread as the foreman, supervise it through completion, and keep Landon able to see progress without making him operate the handoff.

## Preserve the Brain 2.0 operating model

Treat the Brain Operating Manual and Bible as governing architecture throughout planning, execution, and closeout.

- Read the relevant project snapshot before launch when one exists; checkpoint an approved multi-session plan and material execution state in its canonical project home.
- Keep live action items on the task board and durable decisions, outcomes, and continuity in the Brain. Link across systems instead of copying changing facts.
- Route every Brain write through its defined lane, write ritual, checks, review requirements, and landing checklist.
- Extend existing Brain components and canonical homes; never create a parallel memory, policy, task, status, or control system for the foreman workflow.
- Keep the workflow agent-agnostic. Express roles and capability requirements neutrally; isolate unavoidable platform-specific mechanics as adapters rather than letting them shape the core process.

## Gate the transition

Use this workflow only when the architect and Landon have reached meaningful alignment on the outcome. Before launching, ensure the record contains:

- approved outcome and scope;
- key decisions and constraints;
- required artifacts or systems;
- verification criteria and definition of done;
- actions that still require Landon’s confirmation.

Resolve only genuinely blocking ambiguity. Do not reopen settled design questions or make Landon prepare a handoff.

## Freeze the execution brief

Write a self-contained brief from the architect thread’s approved plan. Include enough context for a blank execution thread, but exclude exploratory conversation, rejected alternatives, and tool noise.

The brief must name:

1. outcome;
2. current state and relevant sources;
3. scope and non-goals;
4. settled decisions with their reasons;
5. constraints and guardrails;
6. deliverables;
7. verification for every material requirement;
8. escalation conditions;
9. architect callback contract: source thread ID, milestones that require a direct message, and the fallback if callbacks are unavailable.
10. capability-routing policy, including any user-pinned model, reasoning, latency, or cost constraint.

Keep the capability-routing policy inside the frozen brief even when it also appears in a separate routing plan or dashboard. State whether concrete mappings are explicitly configured, inherited, automatically routed, or still untested before launch.

## Route models by capability

Keep routing policy agent-agnostic. Use the Brain sub-agent playbook's capability tiers, then map them at runtime to configurations the current platform actually exposes.

- Choose the foreman's tier from the execution brief: use the top tier for ambiguous, cross-cutting, or high-risk execution; use the workhorse tier for bounded implementation with a settled plan.
- Let the foreman assign each direct worker the tier its subtask warrants. Workers normally use the workhorse tier; hard judgment and integration use the top tier; verifiers are at least as capable as authors.
- When available, set thread- or child-level model, reasoning, and service-tier controls explicitly. Do not hardcode provider or model names into the core workflow.
- If an override is unavailable, inherit the parent configuration or allow the platform to route automatically, and disclose that fallback in the progress dashboard.
- Treat an accepted override as evidence that the requested configuration was accepted, not independent proof of the worker's runtime identity unless the platform exposes that evidence.
- Expect controls to vary by delegation depth. Keep routing at the nearest parent that exposes the required controls rather than assuming every descendant can select models for its own children.

## Launch the foreman

Create a separate thread rather than merely spawning a worker inside the architect thread.

- Use a project-backed target when the work belongs to an available project; otherwise use a projectless target.
- Use a worktree for parallel code changes when shared-directory edits could conflict.
- Give the foreman the execution brief and instruct it to create a persistent goal.
- Include the architect thread ID and require a direct message back to that thread when the goal starts, at every meaningful phase gate, when a decision or blocker appears, after recovery, and at completion. A final answer posted only inside the child task is not a callback and will not wake the architect.
- Apply the same callback contract to any separate worker task the architect creates alongside the foreman.
- Tell the foreman it owns implementation, decomposition, subagents, recovery, and verification.
- Permit nested delegation when useful, while keeping one writer per artifact and avoiding overlapping write scopes.
- Require the foreman to continue until done, genuinely blocked, or stopped by the architect.

Do not ask Landon to copy, download, or paste the brief into another thread.

## Supervise from the architect thread

The architect remains accountable for the result and does not become a passive mailbox. Separate tasks do not automatically wake it; direct callbacks are the primary control path.

1. Record the foreman thread identifier and initial goal, then verify the foreman sends the required started callback.
2. Read the foreman’s status at meaningful checkpoints. If direct callbacks are unavailable or fail, install a heartbeat or poll the task as the explicit fallback.
3. Send steering when execution diverges from the approved plan, evidence is weak, a worker stalls, or the foreman tries to finish partially.
4. Resolve questions from the existing plan when possible. Involve Landon only for a real product decision, third-party action, spending, deletion/data loss, new authority, or a hard blocker.
5. Let the foreman own execution. Do not duplicate its implementation work in the architect thread.

## Maintain a progress dashboard

The architect owns the human-facing status view. Create it when the foreman launches and update it after meaningful state changes, steering events, verification results, or Landon’s status requests.

Prefer an in-conversation visualization when supported; otherwise use one compact Markdown dashboard. Show:

- overall state: queued, running, blocked, verifying, or complete;
- phase and approximate completion percentage;
- completed milestones;
- work in progress;
- next milestone;
- blockers, risks, and decisions needed from Landon;
- latest verification evidence;
- foreman capability tier and a compact worker-routing summary, including inherited or automatic-routing fallbacks;
- last checkpoint time.

Keep it operational and plain-English. Avoid constant narration, fake precision, and raw tool logs. A percentage is an estimate tied to completed milestones, never a claim of certainty.

## Close the work

When the foreman reports completion:

1. Require the completion callback to arrive in the architect task; do not infer completion merely because the child task becomes idle.
2. Compare the result against the original approved plan and every definition-of-done item.
3. Inspect material evidence and artifacts rather than accepting the foreman’s summary alone.
4. Send the foreman back for any missing requirement, weak verification, regression, or quality problem.
5. Mark the dashboard complete only after the architect’s review passes.
6. Brief Landon on what shipped, what was verified, any remaining limitation, and where the result lives.
7. Capture durable decisions and project state in the Brain under the applicable write lane.

## Fallbacks

If separate-thread creation or monitoring is unavailable, say which capability is missing before falling back to a direct subagent or a manual handoff. Never present the fallback as equivalent to the architect–foreman model.
