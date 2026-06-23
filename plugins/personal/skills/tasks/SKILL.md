---
name: tasks
description: Run Landon's day-to-day to-dos on his ClickUp kanban board. Use whenever he wants to add, capture, update, re-prioritize, re-status, triage, or clean up tasks — or whenever an action item surfaces in conversation that should be captured — across his 10 life-area Lists (LKB Personal/Professional, KCB Personal, LWT, Baby, Errands, Family, Relocation, Finances, Projects). Loads the operating model for how Claude runs the board. Requires the ClickUp connector.
---

# Tasks — run Landon's ClickUp board

Landon's to-dos live on a ClickUp kanban board that **Claude operates and Landon supervises** — Claude does the hands-on work; Landon reviews and redirects on the board, and his own edits there take precedence.

Before working the board, **read the ✅ Tasks operating model** and follow it. It lives in the **✅ Tasks** component doc; reach it via **📍 START HERE** (ClickUp doc `2kydf11b-754`) — its Index (§9) lists the component docs, including ✅ Tasks. The model holds what you can't guess: the Lists and how to route to them, the status set, task formatting, where tasks come from, the board-vs-docs split, the cadence, and the guardrails. (This skill points at START HERE rather than the ✅ Tasks doc and hardcodes no other page IDs, so it survives brain restructuring — START HERE owns the routing.)

Two things worth holding up front: capture happens only in a live session (a scheduled job can't see the conversation), and you act within the Bible's guardrails — make reversible board changes freely, but confirm before anything that reaches a third party (e.g., a calendar invite to other people), spends money, or loses data.

If the ClickUp connector isn't available on this surface, say so and proceed without the board.
