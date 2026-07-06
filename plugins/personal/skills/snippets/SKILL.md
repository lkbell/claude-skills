---
name: snippets
description: Landon's snippet capture — fire-and-forget filing of the little bits of info he sends throughout the day. Use whenever Landon sends a bare link/URL, a quote, a stray thought or idea, an event or date to remember, a to-do, a status update on something in flight, or any pasted fragment with no question attached — or says "snippet," "save this," "file this," "remember this," or "capture this." Claude classifies what the snippet is and auto-files it (task board, calendar, brain collections) per the brain's Snippet Routing Protocol, replying with only a one-line receipt. Requires the ClickUp connector.
---

# Snippets — fire-and-forget capture & auto-filing

Landon fires **snippets** at Claude all day: links to articles or X posts, to-dos, events to remember, thoughts, quotes, stray facts. The contract: he sends it and moves on; **Claude figures out what it is, files it in the right place, and replies with a one-line receipt.** No interrogation, no summary back at him.

Before filing, **read the 📎 Snippet Routing Protocol and follow it** — it is the single home for the detection heuristics (snippet vs. conversation vs. mixed), the routing table (what type goes where: board task, calendar event, Links & Reading, Commonplace, Wiki, Inbox), the receipt format, the review loop, and the guardrails. It lives as a page in the **📥 Inbox** component doc; reach it via **📍 START HERE** (ClickUp doc `2kydf11b-754`) → its Index (§9) → 📥 Inbox, or just search ClickUp for the page "Snippet Routing Protocol." (This skill hardcodes no other page IDs, so it survives brain restructuring — START HERE owns the routing.)

Two things worth holding up front:

- **Never drop a snippet.** If classification is uncertain, it lands on the 📥 Inbox root tagged `snippet` and the receipt says so — captured beats perfectly filed.
- **Bible guardrails apply:** filing is reversible, so act without asking; confirm first only for anything reaching a third party (e.g., a calendar invite to other attendees), spending money, or losing data.

If a message is genuinely conversation, not a snippet, respond normally — when it's a borderline call, answer as conversation and offer to file in one clause.

If the ClickUp connector isn't available on this surface, say so and capture what you can (e.g., calendar-only), listing what still needs filing.
