---
name: cloud-brain
description: Landon's Brain — his private GitHub repo (lkbell/brain) of durable knowledge, project-continuity records, and the standing orders for working with him (the Bible). Use it to LOAD his context at the start of essentially any substantive session, and to CAPTURE durable info back — decisions, milestones, lasting facts, or whenever Landon says "update the wiki," "remember this," or "get up to speed." Requires GitHub access (repo lkbell/brain).
---

# The Brain — load & capture

Landon's Brain is his persistent, cross-session memory: the private GitHub repo **lkbell/brain**, accessed via **GitHub**. It replaced the old ClickUp wiki ("Brain 1.0") — same job, new home. **The task board stays in ClickUp** (the `tasks` skill) — only the Brain itself (knowledge, continuity, standing orders) moved.

**Always start at `README.md`** — the single entry point. It's the operating manual: explains how the repo is organized, holds the write mechanics (lanes, commit conventions, the review-artifact rule), and routes you onward to **`bible/working-with-landon.md`** (the Bible — standing orders for how to work with Landon) and **`now.md`** (the Situation Board — what's hot today). This skill points only at README.md and the handful of load-bearing paths below — it does not hardcode deeper structure, so it survives repo reorganization.

**Follow the checklists literally.** README.md's write ritual and landing checklist exist because skipping a step has already caused a real failure (lost content, stale duplicates, broken pointers). Run them mechanically, especially the steps that feel unnecessary in the moment.

## Mode 1 — Load / get up to speed
1. Read **README.md** and follow it, including the pages it routes you to — **`bible/working-with-landon.md`** (standing orders; read and heed it) and **`now.md`** (the one-page working memory: deadlines, active-project states, what's waiting on whom). README + Bible + Now is the full load.
2. Use README.md's index to find the right resource: **`wiki/`** for durable knowledge (people, knowledge, work, finances, health), **`projects/`** for project continuity, **`log/`** for the episodic daily record, **`inbox/`** for raw capture.
3. For a project: open **`projects/<name>/snapshot.md`** — a complete briefing on its own; open sibling files only for deeper detail.
4. For a specific item elsewhere in the repo: list the directory first, then read only the file you need — don't pull a whole tree for one fact.
5. Briefly confirm what you loaded and the current state before acting. If the structure you observe differs from what README.md describes, the live structure (what's actually in the repo) wins.

## Mode 2 — Capture / save
When a decision is made, direction changes, a milestone or substantial chunk of work completes, durable facts appear, or Landon says "update the wiki":
1. **Know your lane before you write** (defined in README.md; repeated here because it governs every write):
   - **Append lane** — `inbox/`, `log/`, `now.md`, `files/` — direct commits to main. Fast, no review needed.
   - **Content lane** — `wiki/`, `projects/` (excluding `snapshot.md`) — a PR that auto-merges once checks pass.
   - **Protected lane** — `README.md`, `bible/`, `meta/checks`, `meta/jobs`, the People principals' pages, `projects/*/snapshot.md` — a PR **plus** an independent review artifact (below). A GitHub-native approval does not satisfy this requirement.
   - For a multi-file content-lane batch in one session, use **one branch for the whole session** rather than a branch per file.
2. Write for a blank reader: be specific and complete, not punchy-but-vague. Use absolute dates (`YYYY-MM-DD`). One fact, one home — link to a changeable fact's canonical file instead of copying it.
3. Every commit message ends with a surface tag, e.g. `[surface:web]`, `[surface:phone]`, `[surface:cowork]`, `[surface:mini]`, or `[surface:<job-name>]`. Never omit it.
4. At the end of a substantial session, run the **landing checklist**: rebuild **`now.md`** if the picture changed (append lane — direct commit); update any touched **`projects/*/snapshot.md`** (protected lane — PR + review artifact); add a **`log/`** entry for the day; triage **`inbox/`**.
5. GitHub access **cannot delete branches or repos** and **cannot move or rename files atomically** — a rename is really a delete-plus-create, which shows up as two changes, not one. Plan file placement deliberately up front.

## The review-artifact convention
A protected-lane PR only merges once someone other than its author pushes an independent review file to the PR branch at `meta/reviews/pr-<n>-*.md` — a GitHub-native approval does not count. In practice: if you opened the protected-lane PR, don't self-review it; get a separate session (or Landon) to push the review file before it merges.

## Feedback handling
When Landon gives a preference, correction, or feedback: capture one line to **`inbox/`** (append lane — direct commit), apply it immediately for the rest of the session (confirm in one line), and let it get triaged during maintenance per README.md's aging rule.

## Proactive capture
At the end of a substantial session, or when a clear decision / milestone / durable fact lands, **briefly offer** to capture it to the Brain — one line, don't nag. Capture only during a live session (a detached or scheduled job can't see the conversation it would record); scheduling is reserved for maintenance.

## Key resources
- **`README.md`** — the entry point: repo structure, lane rules, write mechanics, routing to the Bible + `now.md`.
- **`bible/working-with-landon.md`** — the Bible (standing orders for working with Landon).
- **`now.md`** — the Situation Board (working memory, rebuilt at landing).
- Repo: **lkbell/brain** (private), accessed via GitHub.

## GitHub access limits (known — don't rediscover these mid-session)
- **Cannot read CI/Actions status** — those calls come back 403. To check whether a PR's checks passed, check the PR's merged state instead, or use the browser.
- **Cannot delete branches or repos.**
- **Cannot move or rename files atomically** — it's always delete + create.
- **~50-60KB practical ceiling** on file content passed through a single tool call — split the write or use another path for anything larger.

## If GitHub access isn't available on this surface
Say so plainly and proceed without the Brain here; offer to load or capture later on a surface where GitHub is connected.
