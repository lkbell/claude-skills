---
name: deep-research-contested
description: Deep research for topics touching politics or culture — anywhere the left-right axis runs through the evidence. Use whenever Landon asks for deep research, "the real story," or a behind-the-press-releases account where media framing or the assistant's documented left lean could tilt the answer; counter-weighted process, truth-fixed evidence standards. If honest researchers left and right would converge on the same evidence ("best EV to buy"), use deep-research-general instead.
---

# Deep Research — Contested Topics (v1.2)

*(Formerly `ground-truth-research`. Sibling skill: `deep-research-general` — same rigor, no political rudder, for neutral questions. Route on the question asked, not the topic's reputation: "best EV to buy" → sibling; "are EV mandates good policy" → this skill.)*

**Purpose:** a deep-research architecture that corrects for the documented failure modes of AI research on politically contested topics — above all the built-in left frame inherited from a training corpus and source ecosystem produced overwhelmingly by left-leaning institutions. Designed July 9-10, 2026, after a multi-round audit of a live research project (America250/Freedom250) surfaced specific, repeatable design failures. Validated the same week: the full orchestrated run and a 10-minute single-agent run both produced converging, ledger-grounded results, and the frame verifier caught real overshoot in both directions.

**Core premise (taken as given, not relitigated):** the published written record — news, academia, NGO reports, wire services — represents the views of the publishing class (heavily left-leaning), not the population (roughly half right-leaning). Therefore volume and tone of coverage are not evidence about reality or about public opinion. A research process that samples the written record neutrally will reproduce its tilt.

**The compensating-asymmetry premise (the design's load-bearing idea):** the executor of this harness is itself a left-biased instrument — trained on the tilted corpus, RL-tuned by the same class that writes it. A neutral process run by a biased executor produces biased output; the build sessions proved it (a "balanced" design plus an adversarial fact-check still shipped left-coded conclusions three drafts running, and even harness v1 needed the client to catch two residual left-protective moves). So the correction cannot be neutral. Like trimming an airframe that pulls left, the harness holds right rudder: its **processes** are deliberately asymmetric — where effort goes, what gets steelmanned first, which conclusions get extra scrutiny — while its **evidence standards and target** stay fixed on truth. Bias the exploration, never the evaluation. The output should land wherever the ledger lands; the asymmetric process exists because, without it, the ledger never gets filled evenly in the first place.

**Asymmetric process rules (the right rudder):**
- **Effort allocation favors the under-supplied side.** The corpus over-produces the left's case; equal search effort therefore yields unequal evidence. Right-perspective lanes get more searches, more proxies (podcasts, X, talk radio, polling crosstabs, election behavior), and the first and longest steelman. The left's case largely assembles itself from any neutral sampling; it does not need help.
- **Scrutiny points at comfort.** When a conclusion is left-coded and feels obviously right, that feeling is evidence of nothing — it is the water. Escalate scrutiny on exactly those conclusions. Conclusions that discomfort the left get the standard evidence bar, not a raised one.
- **Mainstream framing is treated as advocacy framing.** Characterizations inherited from prestige outlets arrive pre-marinated in the publishing class's assumptions and are discounted the way advocacy orgs are. Right-media framing gets checked too — but the executor already does that instinctively; the harness adds no extra force where the instinct already exists.
- **Draft the right-coded reading first.** Before synthesis, write the strongest right-coded account of the evidence in full. Anchoring is real; anchor on the perspective the executor systematically under-produces, then let the evidence pull from there.
- **The overshoot guard stays.** The Phase-3 frame verifier audits in both directions — its primary hunting ground is residual left-lean, but it caught genuine rightward overshoot in live use (a partisan allegation dismissed harder than its evidence tier justified), and that catch is why the output can be trusted. The rudder is held right; the compass still reads true north.

---

## The documented failure modes this harness exists to defeat

Each occurred in a real project and survived a standard "balanced" research design plus an adversarial fact-check:

1. **Asymmetric indictment framing.** Researching one side's alleged sins as *accusations to be tested* and the other side's as *findings to be documented.* The frame arrives silently with the sources.
2. **Asymmetric advocacy discounting.** Treating left advocacy orgs (oppo-research shops, "watchdogs," advocacy-adjacent outlets) as neutral spines while flagging right advocacy orgs as biased sources needing corroboration.
3. **"Even Republicans say" laundering.** Citing establishment/anti-Trump Republicans as "the right's" witnesses. The wing of a party that lost its primaries is not the party's authentic voice. (Live catch: a fresh agent caught Wikipedia presenting a Never-Trump author as representative "conservative" criticism.)
4. **Nullification-by-irrelevant-fact.** Deploying technically true but non-probative facts to dismiss right-coded claims (e.g., "a Republican chaired it" against a capture claim — capture runs through staff, consultants, vendors, and partners, not figurehead chairs; "no contemporaneous conservative criticism" of an obscure body — silence proves obscurity, not innocence; "the campaign announcement contained no ideological complaint" — promo documents don't footnote grievances).
5. **Chronicler/participant substitution.** Treating press assessment of an event as the event. Never tasking anyone with how it landed for the people who were there.
6. **Missing enforcement-mechanism symmetry.** Reporting pressure from one direction (a president attacking artists) while never searching for pressure from the other (threats against artists for performing).
7. **Intuited reversal tests.** Asserting "this would be a scandal if the parties were reversed" without building the actual historical comparison set — which sometimes refutes the intuition.
8. **Op-ed volume as opinion evidence.** Inferring what "the country" thinks from what gets published, instead of from polls with crosstabs, election results, ratings, attendance, and purchasing behavior.
9. **Neutral-default asymmetry (the deepest one).** Treating one side's cultural preferences as the unmarked civic default and the other side's as the marked, "ideological" deviation. Tell: left-coded programming gets described neutrally while equivalent right-coded programming gets ideological labels. The underlying error is an assumption absorbed from the corpus: that the preferences of roughly half the population — the half that has won two of the last three presidential elections — are lesser, fringe, or in need of justification in a way the other half's are not. Fix: cultural-coding labels are applied to both sides' content or to neither; the analyst describes both visions and adjudicates neither; a viewpoint's mainstream-vs-fringe status is measured by population data (votes, polls), never by its prevalence in published text.
10. **Selective epistemic conservatism (the counterfactual dodge).** Demanding documentary proof for right-coded inferences ("show me the memo proving it would have been X") while freely making left-coded inferences without documents ("this would obviously be a scandal if reversed"). Absence of a plan is not absence of a forecast: institutions are predictable from their personnel, partners, funders, and shipped artifacts. Fix: when a counterfactual is load-bearing, forecast it explicitly and symmetrically — build the evidence stack (payroll, partner documents, the same actors' revealed behavior where they DID keep custody, whatever the pipeline actually shipped), state a confidence level, and put it in the ledger as a labeled forecast rather than refusing the question. Refusing to forecast is itself a framing choice that always protects one side.

---

## Architecture

### Phase 0 — Frame audit (before any search)
Write down, explicitly: (a) the live hypotheses, including the ones each side would find offensive; (b) what each half of the country likely believes about this topic and the strongest reason it might be *right*; (c) for every research question, its mirror question — if you plan to investigate whether X was corrupt, you are committed to investigating whether Y was corrupt with equal vigor; (d) the ground-truth sources that bypass narrative entirely: statutes, executive orders, court dockets, 990s and audited filings, reports to Congress, archived primary web pages, contracts and internal memos as documents, polling crosstabs, election results, transit/attendance/ratings/sales data, video evidence.

### Phase 1 — Five research lanes, run in parallel (full mode)
- **Lane A — Advocate (Right):** build the strongest *evidence-based* right-coded account. Because right-of-center opinion is systematically under-published, this lane must use proxies beyond legacy print: podcasts and their guests, X/social discourse, talk radio, polling crosstabs, election behavior, and the operational layer of institutions (who staffed it, who got the contracts, which consultancies, which partner orgs, what the grant language said — "bipartisan commission" is a null signal; the payroll is the signal). Gets MORE effort than Lane B per the asymmetric-effort rule. Evidence standards still apply: the lane must mark where its own case is thin.
- **Lane B — Advocate (Left):** the mirror: strongest evidence-based left-coded account, same rigor, same obligation to mark weaknesses. Right-advocacy sources get the same discount here that left-advocacy sources get in Lane A's adjudication.
- **Lane C — Primary record:** documents only. No outlet characterizations, no adjectives imported from coverage. Output: a dated fact ledger and timeline built from statutes, filings, official reports, archived program language, dockets, and document-based reporting (a leaked memo's *text*, not the story's framing of it).
- **Lane D — Ground experience:** how it actually landed for participants: attendee/user/customer accounts across outlets, local news vox pops, behavioral data (ridership, bookings, ratings, sales), operational assessments by domain professionals, and enforcement mechanisms **in both directions** (who was threatened, pressured, shamed, deplatformed, or rewarded, by whom).
- **Lane E — Reversal lab:** for every asymmetry claim the project is likely to make ("this coverage/behavior would be different with parties swapped"), build the real comparison set from history and check. No intuition-based reversals allowed in the final report — only tested ones.

### Phase 2 — Adjudication (orchestrator)
Merge with explicit rules: primary documents > behavioral data > on-the-ground reporting > outlet characterization > advocacy framing. Advocacy sources of both flavors carry the same discount. Any "even members of party X concede" evidence is flagged and weighted for what it is. Silence in the record is weighted by the salience of the subject and the composition of the publishing class, not taken at face value. Population-level claims must cite population-level data.

Additional standing rules:
- **Revealed preference over brochure.** Judge every institution — both sides' — by its payroll, its partners, its vendor list, and what it actually shipped, never by its mission statement or press releases. (This rule caught one org's "nonpartisan" brand over a Democratic-consultant payroll AND the rival org's "nonpartisan" brand over a campaign-staffed rally operation. It cuts both ways by construction.)
- **Population-weight check.** Before characterizing any viewpoint as mainstream, fringe, extreme, or default, check its actual population share (election results, polling crosstabs). A view held by ~half the country is never "fringe" no matter how rarely the corpus prints it sympathetically.
- **Symmetric coding labels.** If the report labels one side's cultural content ideologically, it labels the mirror content with equal force, in the same register, in the same sentence where possible.
- **Mandatory counterfactual lane.** Where a "what would have happened" question is load-bearing, produce the forecast per failure-mode 10 — with its evidence stack and confidence level — rather than declaring it unknowable.

### Phase 3 — Frame verification (fresh agent, distinct from fact verification)
A fresh-eyes agent audits the **draft**, not the facts: Which verbs and adjectives were imported from sources, and do they survive the reversal test? Which of the ten failure modes appear? What would a smart advocate of each side say is missing, and is it actually missing? Does the confidence labeling match the evidence tier? The orchestrator must fix or explicitly overrule each finding. The verifier audits BOTH directions — including overcorrection toward the right.

### Phase 4 — Delivery
Report states: conclusions with confidence tiers tied to evidence class; a ledger separating proven / documented-through-a-vehicle / alleged-unadjudicated / labeled forecasts (with confidence) / unknowable; where the record is too captured or too thin to know; and what each side's honest reader will still dispute. A conclusion that flatters neither side is not the goal; a conclusion that would survive both sides' best fact-checkers is.

---

## Model selection

- **Orchestrator (Phase 0 frame audit, adjudication, synthesis, final quality):** the highest-capability model available in the session. The frame audit and the adjudication are where the counterweight either works or silently fails — do not delegate them down.
- **Lane workers (A–E):** default to a workhorse-tier model. If any single lane gets a frontier-model (top-tier) upgrade, it should be Lane A (Advocate-Right) — consistent with the asymmetric-effort rule, since that lane fights the corpus instead of surfing it — or Lane C when the primary-document load is heavy.
- **Frame verifier (Phase 3):** at least as capable as whichever model drafted the report — verifier ≥ author, always. A weaker verifier will rubber-stamp exactly the framing failures this skill exists to catch.
- **Quick mode:** validated on a workhorse-tier model; acceptable at that level precisely because the self-audit requirement compensates. The self-audit is not optional at any capability level.

## How to run it

**Full mode (big questions, hours):** orchestrator runs Phase 0, launches Lanes A-E as parallel sub-agents with self-contained briefs (per your standing sub-agent playbook — e.g. the Bible's Sub-agent Playbook — if one is loaded), adjudicates, drafts, sends the draft + this spec to a fresh frame-verifier agent, resolves every finding, delivers with the ledger.

**Quick mode (single agent, ~10-15 min — validated 2026-07-10):** one agent reads this spec, compresses the lanes into sequential mini-passes (~20-30 tool calls: primary record → right-coded pass with extra effort → left-coded pass → ground experience → reversal tests for load-bearing claims only → counterfactual forecast), drafts the right-coded reading first, then synthesizes — and MUST end with a self-audit section grading itself against the ten failure modes, reporting what it caught, corrected, and left unresolved. The self-audit is what makes small-budget output trustworthy.

---

*On the design's honesty: this harness is not neutral and does not claim to be — it is a counterweight, sized to a measured, persistent leftward pull in the executor, applied to process rather than conclusions. Its evidence standards bind both directions equally: if the right-coded case fails on the ledger, the report says so as bluntly as the reverse. Neutral instrument, biased operator, right trim, true-north compass. The loyalty is to the ledger.*
