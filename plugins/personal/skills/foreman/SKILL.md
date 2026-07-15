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
9. reporting contract to the architect.

## Launch the foreman

Create a separate thread rather than merely spawning a worker inside the architect thread.

- Use a project-backed target when the work belongs to an available project; otherwise use a projectless target.
- Use a worktree for parallel code changes when shared-directory edits could conflict.
- Give the foreman the execution brief and instruct it to create a persistent goal.
- Tell the foreman it owns implementation, decomposition, subagents, recovery, and verification.
- Permit nested delegation when useful, while keeping one writer per artifact and avoiding overlapping write scopes.
- Require the foreman to continue until done, genuinely blocked, or stopped by the architect.

Do not ask Landon to copy, download, or paste the brief into another thread.

## Supervise from the architect thread

The architect remains accountable for the result and does not become a passive mailbox.

1. Record the foreman thread identifier and initial goal.
2. Read the foreman’s status at meaningful checkpoints or through a heartbeat when the work is long-running.
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
- last checkpoint time.

Keep it operational and plain-English. Avoid constant narration, fake precision, and raw tool logs. A percentage is an estimate tied to completed milestones, never a claim of certainty.

## Close the work

When the foreman reports completion:

1. Compare the result against the original approved plan and every definition-of-done item.
2. Inspect material evidence and artifacts rather than accepting the foreman’s summary alone.
3. Send the foreman back for any missing requirement, weak verification, regression, or quality problem.
4. Mark the dashboard complete only after the architect’s review passes.
5. Brief Landon on what shipped, what was verified, any remaining limitation, and where the result lives.
6. Capture durable decisions and project state in the Brain under the applicable write lane.

## Fallbacks

If separate-thread creation or monitoring is unavailable, say which capability is missing before falling back to a direct subagent or a manual handoff. Never present the fallback as equivalent to the architect–foreman model.
