---
name: snippets
description: Landon's snippet capture — fire-and-forget filing of the bits of info he sends all day. Use whenever he sends a bare link, quote, stray thought, event, to-do, or pasted fragment with no question attached; says "save this," "file this," "remember this"; or fires a quick one-off filing/update directive ("add X to my list," "put this on my favorites," "note that ..."). Treat all of these as fire-and-forget: classify and auto-file per the brain's Snippet Routing Protocol, reply with a one-line receipt, and never turn a one-off into a project. Requires ClickUp access and GitHub access (repo lkbell/brain).
---

# Snippets — fire-and-forget capture & auto-filing

Landon fires **snippets** at the assistant all day: links to articles or X posts, to-dos, events to remember, thoughts, quotes, stray facts, and quick one-off filing/update directives ("add X to my favorites," "put this on my list," "note that …"). The contract: he sends it and moves on; **the assistant figures out what it is, files it in the right place, and replies with a one-line receipt.** No interrogation, no summary back at him. **File into the smallest existing structure** — never invent a new section, list, or follow-up task for a single item, and keep the filing mechanics (PRs, file paths, sync status) out of the receipt; a structural question gets parked silently for a later curation pass, not raised in his face.

Before filing, **read `inbox/snippet-routing-protocol.md`** in the repo **lkbell/brain** (via **GitHub**) **and follow it** — it is the single home for the detection heuristics (snippet vs. conversation vs. mixed), the routing table (what type goes where: board task, calendar event, Links & Reading, Potpourri, Wiki, Inbox), the receipt format, the review loop, and the guardrails. The brain-collection destinations — 📚 Links & Reading and 📔 Potpourri — are now **`inbox/links-and-reading.md`** and **`inbox/potpourri.md`**: both are append-lane files, so filing is a direct commit — faster than the old ClickUp page-overwrite dance (no read-the-whole-page-first step needed). Board-task and calendar filing are unchanged. (This skill hardcodes no paths beyond these, so it survives brain restructuring.)

Two things worth holding up front:

- **Never drop a snippet.** If classification is uncertain, it lands in **`inbox/`** tagged `snippet` and the receipt says so — captured beats perfectly filed.
- **Bible guardrails apply:** filing is reversible, so act without asking; confirm first only for anything reaching a third party (e.g., a calendar invite to other attendees), spending money, or losing data.

If a message is genuinely conversation, not a snippet, respond normally — when it's a borderline call, answer as conversation and offer to file in one clause.

If ClickUp access isn't available on this surface, say so and capture what you can (e.g., calendar-only), listing what still needs filing.
