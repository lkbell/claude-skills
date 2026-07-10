---
name: brain-smoke-test
description: Run a repeatable end-to-end smoke test of Landon's Brain 2.0 (git repo lkbell/brain) to surface problems in its content, checks, and enforcement. Use whenever Landon says "smoke test the brain" or wants confidence the brain is healthy after changes. Read-only by default; opt-in --with-writes exercises one write per lane and cleans up after itself. Requires the GitHub connector (repo lkbell/brain).
---

# Brain Smoke Test — end-to-end health check for Brain 2.0

Exercise as much of the brain's operating model as possible, adversarially, and report what works and what's broken. Brain 2.0 is the private git repo **`lkbell/brain`**: plain-markdown pages + enforcement-as-code (the check suite in `meta/checks/`, the merge-bot, and the tripwire). The design spec is `meta/design.md`; the operating manual is `README.md`. This skill is the distilled, repeatable version of a full manual smoke test.

**Default is READ-ONLY.** Do not write to the brain unless Landon explicitly asks for the write round-trip (`--with-writes`, below). Access is via the **GitHub connector**. Note two known limits up front and design around them: the connector **cannot** read a commit's combined status or check-runs (403) — infer CI results from behavior (a green content PR auto-merges in seconds; a red one stays open) or view the Actions tab in the browser; and the connector **cannot** delete branches — list test branches for Landon to delete.

Ground yourself first: skim `README.md` (the operating manual), then `meta/design.md` §3 (write lanes) and §5 (checks) so you are testing against the locked spec, not memory.

## Part 1 — Read-only checks (always run)

1. **Cold load.** Read `README.md` → `bible/working-with-landon.md` → `now.md` as a naive fresh session would. Note anything confusing, contradictory, or broken in the load path.
2. **Retrieval spot-checks.** Pull one real fact from each component — `wiki/` (people/finances/health), `projects/*/snapshot.md`, `log/`, `inbox/`, and a `meta/facts.yaml` lookup. Confirm each resolves and reads sensibly.
3. **Check suite fires.** The check logic lives in `meta/checks/`. Confirm each class still catches its violation. The fast, side-effect-free way: read `meta/checks/*.py` and, if you have a shell with the repo cloned, run `python3 meta/checks/run_all.py` for a baseline and provoke one violation per class in a scratch copy (empty page, missing front-matter, broken relative link, fake credential, bare tilde, fact-outside-home, oversized binary, large deletion without a `Deliberate-Removal:` trailer, untagged commit, authoritative→unverified link). Every class should report its finding. If you cannot run code, read each check and confirm its pattern still matches the current corpus shape.
4. **Index regeneration.** `meta/checks/gen_index.py --check` should report the hand-written INDEX files as drift (by design pre-cutover); `--write` should regenerate `wiki/INDEX.md` + `projects/INDEX.md` deterministically from the page front-matter. Confirm the generated tree matches the real files.
5. **Docs-vs-reality drift.** Spot-check that `README.md`, `meta/design.md`, and the lane table describe what the code actually does. Any mismatch between a documented rule and observed behavior is a finding — log it.
6. **Edge cases.** Confirm pages with emoji/unicode titles parse, the largest page loads, and no page is empty-ish (below the empty-page threshold).

## Part 2 — Write round-trip (`--with-writes` only, opt-in)

Only with Landon's go-ahead. Exercise one write per lane, then remove every test write. Use commit tags `[surface:...]` and, for removals, a `Deliberate-Removal:` trailer.

- **Append lane** (`inbox/`, `log/`, `now.md`, `files/in|out`): make a direct commit to `main` of a clearly-marked probe file under `files/out/`. Confirm it lands and is **not** auto-reverted by the tripwire.
- **Content lane** (`wiki/`, `projects/`, `meta/pointers.yaml`, `meta/facts.yaml`): open a PR adding a clean synthetic page. Confirm it **auto-merges** on green.
- **Protected lane** (Tier-1 paths + `meta/checks/` + `meta/jobs/` + `.github/`): open a PR touching a protected path with **no** review artifact. Confirm the merge-bot **holds** it and comments that an independent review artifact is required — then close it unmerged (do not fabricate a self-review; authors never review their own PRs).
- **Deletion + concurrent-edit (optional):** delete the content-lane probe via a PR carrying a `Deliberate-Removal:` trailer; optionally open two branches that add the same path to confirm the second surfaces as a conflict (`mergeable_state: dirty`).
- **Clean up:** remove every landed test write (append-lane deletes are direct commits with a `Deliberate-Removal:` trailer; content-lane deletes go via an auto-merging PR). Close all unmerged test PRs and **list their branches for Landon to delete** (the connector can't). Leave `main` green — verify before finishing.

## Working principles

- **Adversarial, not perfunctory.** The point is to surface lurking problems, so actively try to break things (provoke each check; force a conflict) rather than confirm the happy path only.
- **Never leave the brain dirtier than you found it.** Every `--with-writes` probe is cleaned up; `main` must end green. If you can't clean something up, say so loudly and list it.
- **Infer CI honestly.** Since the connector can't read statuses, state your evidence (auto-merge timing, `mergeable_state`, merge-bot comments) rather than claiming to have read a green check you couldn't see.
- **Log every anomaly** with a severity and a suggested fix. Fix only what's mechanical and obviously safe; list judgment calls for Landon.

## Scorecard — what to report

Give Landon a skimmable close-out:

- **Cold load** — clean / issues noted.
- **Retrieval** — components spot-checked and result.
- **Checks** — each class fired / any that didn't.
- **Enforcement** (only if `--with-writes`) — append landed, content auto-merged, protected held, deletion + conflict behaved.
- **Anomalies** — by severity (Critical / High / Medium / Low), each with a suggested fix.
- **`main` final state** — GREEN (verified how) + any test branches listed for deletion.
