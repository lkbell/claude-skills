---
name: shop-walk
description: Run an end-of-day "shop walk" to close out a work session: review the day's work, verify and tidy the Brain, catch what was missed, and deliver an end-of-day report. Use whenever Landon says "shop walk," "wrap up," "clock out," or "end of day" — and offer it proactively at the natural end of a substantive session. Requires ClickUp access (task board) and GitHub access (the Brain, repo lkbell/brain).
---

# Shop Walk — end-of-day review & cleanup

Act like a shop manager walking the floor at close: review the day's work, make sure everything's in order, catch what got missed, and give clear final tasking before the team clocks out. Be thorough, not perfunctory — this is the safety net that keeps the Brain trustworthy, so it's worth doing properly.

Ground yourself first: if you haven't already this session, skim **`README.md`** in the repo **lkbell/brain** (via GitHub) so you're working from its current structure and rules — it routes you to **`bible/working-with-landon.md`** and **`now.md`** if you need them too.

## The walk

1. **Review the whole session** for anything open, deferred, promised, or needing action — yours or Landon's. Don't let loose ends drop silently.
2. **Walk the task board** — the board itself stays in ClickUp; its operating model now lives at **`tasks/README.md`** in **lkbell/brain** (GitHub access). Bring statuses current, capture the day's loose ends as tasks in the right Lists, chase "pending / needs flup" items, tee up tomorrow's priorities, and push any time-bound items to the calendar.
3. **Verify the real state of everything created or edited this session.** Actually read each artifact back from where it lives — do not trust your memory or a tool's "success" response. For Brain artifacts, **read the day's commits/diffs via `list_commits`** (GitHub access) to confirm what actually landed — a commit list is the literal record, so this replaces the old ClickUp keyword-search caveat entirely rather than just supplementing it. For board/calendar items, read them back directly as before. This is the most important step: past sessions have reported changes that hadn't really landed, so reading back the true state is non-negotiable.
4. **Check cross-doc consistency.** The Brain's files should agree — design, links, status, naming. Reconcile contradictions (e.g., a Snapshot still saying "planned" for something now built).
5. **Inventory for cruft.** Look for orphaned, outdated, test, or overcome-by-events content: list the Brain's directories (`wiki/`, `projects/`, `inbox/`) and cross-check against README.md's index. Flag anything to archive or delete (route any deletion through the normal lane process for that path). Unlike the old ClickUp doc search, a repo directory listing is exhaustive, not keyword-limited — no "may not be exhaustive" caveat is needed here.
6. **Log the day.** Append today's entry to **`log/YYYY-MM.md`** (append lane — direct commit) if it isn't already done.
7. **Update what changed, and tidy `now.md`.** Refresh any touched **`projects/*/snapshot.md`** (protected lane — PR + independent review artifact; batch multiple snapshot updates on one branch for the session) and triage **`inbox/`** items ready to route home. **Tidy `now.md`**: delete resolved / no-longer-hot lines, leave the next agent a note on anything in-flight, and keep it to about one screen — it's a scratchpad, so prune and update, don't rebuild wholesale.
8. **Deliver the end-of-day report** (structure below).

## Working principles

- **Read before you overwrite.** A Brain file update replaces the whole file — read the current content first and write back the full intended result; removals must be deliberate, never accidental.
- **Don't over-churn.** Fix real inconsistencies and errors; for trivial or cosmetic staleness, just note it rather than rewriting whole files (a whole-file rewrite for a typo risks introducing new errors, and a protected-lane file still needs a review artifact no matter how small the change).
- **Be honest.** Actually check before saying "all good," and separate must-do from optional. If you're unsure something landed, say so plainly.
- **Stay thin and Brain-driven.** Operate through README.md's index; don't hardcode paths beyond the load-bearing ones (`README.md`, `bible/`, `now.md`, `tasks/README.md`, `log/`, `inbox/`, `projects/`), which change when the Brain is restructured.

## End-of-day report — structure

Give Landon a clear close-out he can skim:

- **✅ Verified** — what you checked and confirmed is correct.
- **🔧 Fixed** — what you corrected, briefly.
- **⚠️ Still open / flagged** — loose ends, unresolved inconsistencies, things needing his judgment.
- **📋 Tasking** — split into **Landon's** (e.g., a decision only he can make, or reviewing a pending protected-lane PR) and **the assistant / next session** (what to pick up next time).

The point is that Landon can clock out trusting the shop is clean.

If ClickUp access isn't available on this surface, say so and do what you can from the session alone. If GitHub access isn't available, say so and skip the Brain verification/log/inbox/snapshot steps — do what you can with the board and the session alone.
