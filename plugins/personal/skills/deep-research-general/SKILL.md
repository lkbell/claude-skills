---
name: deep-research-general
description: Deep research for questions with NO left-right political or cultural axis — questions where an honest researcher on the left and one on the right would converge given the same evidence. Products and purchases, science, health and medicine, technology, business and markets, travel, how-things-work, history and biography without a culture-war overlay. Use whenever Landon asks for deep research, a thorough investigation, "the real story," or a well-sourced report on a neutral question. Runs a primary-record/data lane, stakeholder-advocate lanes (only when interested parties exist), a ground-experience lane, and a comparison lab; adjudicates on an evidence-tier ladder; verifies facts AND framing; delivers a cited, confidence-tiered ledger. ROUTER — route on the question asked, not the topic's reputation: if answering requires taking sides where left and right marshal systematically different evidence and the conclusion itself lands differently by tribe, use the sibling skill `deep-research-contested` instead ("best EV to buy" → this skill; "are EV mandates good policy" → sibling).
---

# Deep Research — General (v1.1)

**Purpose:** a deep-research architecture for neutral questions, built from two sources: the fan-out/verify bones of the original deep-research harness, and the axis-neutral machinery proven during the 2026-07 contested-research build. Where the sibling skill (`deep-research-contested`) counter-weights a specific political bias, this skill counter-weights the *general* distortions of the modern information environment: marketing capture, churnalism, AI-generated slop, reviewer-owner gaps, hype cycles, and coverage-volume illusions.

**The router test (run before anything else).** Route on the question you were actually asked, not the topic's reputation. Two questions: (1) Does answering it require taking sides on a claim where left and right marshal systematically different evidence, so the conclusion itself lands differently by tribe? (2) Given the same evidence, would an honest researcher on the left and one on the right converge? If (1) yes and (2) no → stop and use `deep-research-contested`. If the question is about what's true, what works, what's well-made, or what's the best value — even on a topic that is politicized in the abstract — stay here. Worked splits: "best EV to buy" → here / "are EV mandates good policy" → sibling. "Best homeschool curriculum for teaching reading" → here / "should homeschooling be regulated" → sibling. "Ozempic long-term risks" → here / "is Ozempic coverage politically driven" → sibling. If mid-research you discover the question is coded after all — the tell is opposed *political* advocacy ecosystems appearing in your sources — switch skills rather than improvise. (The reverse error also matters: do not drag political counterweighting into neutral questions — it manufactures a frame where none exists.)

**Core loyalty:** the ledger. Every conclusion sits on a named evidence tier; confidence never exceeds tier.

---

## The failure modes this skill exists to defeat

General-information-environment equivalents of the contested skill's political modes, named from real failures:

1. **SEO/affiliate capture and AI slop.** Most "best X" and review content exists to harvest affiliate revenue, is written from spec sheets rather than testing, and — increasingly — is AI-generated outright. Rank sources by whether they demonstrably bought/tested/measured, disclose methodology, and publish negative verdicts; a site that never pans anything is a catalog, not a reviewer. Treat unsigned review content and crowd score-aggregates as potentially farmed or astroturfed until a human methodology or verified-use signal is confirmed.
2. **Press-release laundering (churnalism).** Much science/tech/business "news" is a lightly reworded press release. Trace every claim to the underlying paper, filing, or dataset; note when ten articles are really one source wearing ten hats.
3. **Single-study syndrome.** One study — especially observational, industry-funded, small-n, or unreplicated — is a lead, not a finding. Check replication, meta-analyses, effect sizes, and who paid (the study's funders AND the quoted experts' individual conflicts). State the evidence grade (RCT/meta vs. observational vs. mechanistic vs. anecdote).
4. **Brochure substitution.** Never judge an institution, company, or product by its marketing. Revealed preference over brochure: teardowns, warranty/return data, service manuals, filings, payrolls, vendor lists, what actually shipped.
5. **Chronicler/participant substitution.** Professional reviewers ≠ long-term owners; critics ≠ audiences; conference speakers ≠ practitioners. Always run a ground-experience pass — with its domain limits (see the lane's guard below).
6. **Coverage-volume illusion.** How much something is written about tracks newsroom incentives and SEO economics, not frequency or importance. Population-level and prevalence claims require population-level data (sales, surveys, registries, base rates), never article counts.
7. **Survivorship and denominator neglect.** Failures are underreported everywhere (products that died, startups that folded, treatments that washed out). Ask what the full denominator is and go find the failures deliberately.
8. **Status halo / challenger hype.** The incumbent-consensus answer and the contrarian-disruptor answer both get graded against evidence, not against their status. "Everyone knows" and "they don't want you to know" are both tells, not tiers.
9. **Intuited comparisons.** Any "best/worst/unprecedented/first/fastest-growing" claim gets tested against a deliberately built comparison set, not asserted from feel.
10. **The counterfactual dodge.** When a "what would have happened / what should I expect" question is load-bearing, forecast it explicitly from base rates and revealed behavior, label it a forecast, and attach a confidence level — refusing to estimate is itself a distortion.
11. **Staleness.** Information decays at different rates by domain — prices, specs, regulations, and travel logistics decay in months; clinical guidelines in years; physical constants never. Date every load-bearing source, prefer the most recent authoritative version, and flag when the best available evidence predates a known change (new model year, revised guideline, updated law).

---

## Architecture

### Phase 0 — Scope and stakeholder map
Before searching: (a) if the question is underspecified for its genre (a purchase without budget/use-case/region; a "best X" without constraints), ask 2-3 clarifying questions first; (b) run the router test; (c) decompose the question into its real sub-questions; (d) map the stakeholders — who profits from each possible answer (vendors, incumbents, challengers, professions, platforms)? Those interests define the advocate lanes and the capture risks; (e) list the ground-truth sources that bypass narrative: datasets, standards bodies, regulatory filings, court records, patents, teardowns, registries, complaint databases, price histories, polling/sales data, primary papers.

**Collapse rule:** if the question is explanatory or factual with no interested parties (pure science, settled history, how-things-work), skip the advocate lanes entirely — run only the primary/data and ground-experience lanes plus the comparison lab. The advocate structure is for questions with commercial or reputational stakes, not for questions of fact. Do not manufacture a controversy.

### Phase 1 — Lanes (parallel agents in full mode; sequential mini-passes in quick mode)
- **Primary/data lane:** documents and datasets only — papers (methods sections, not abstracts), filings, specs, standards, measurements, official statistics. The freely-available layer is often the marketing layer: seek the paywalled/primary version of load-bearing evidence, and for geographically scoped questions consult non-English and foreign-regulator sources (EMA vs. FDA, etc.).
- **Stakeholder-advocate lanes (when the Phase-0 map shows interested parties):** build the strongest evidence-based case for each major interested position — bull and bear, vendor's best case and skeptic's best case, incumbent and challenger. Each lane must mark where its own case is thin. Advocacy and marketing sources carry the same discount in every lane.
- **Ground-experience lane:** how it actually goes for the people who use/own/practice it — long-term owner reports, practitioner accounts, complaint and failure data, behavioral evidence (repurchase rates, adherence, churn). Weight sustained-use reports over first-week impressions. **Domain guard:** ground experience is strong evidence for durability, usability, and real-world failure rates; it is weak-to-dangerous for efficacy, causation, or mechanism, where it must yield to the evidence-tier ladder — never let crowd volume override clinical or scientific consensus on a causal claim.
- **Comparison lab:** build the real comparison sets for every superlative or novelty claim the report will lean on.

### Phase 2 — Adjudication
Evidence-tier ladder: **primary data/documents > behavioral data > independent testing > on-the-ground reporting > outlet characterization > interested-party framing.** Independent-source rule: a claim repeated by many outlets counts once until independently re-derived. Date-stamp load-bearing sources (failure mode 11). Conflicts get stated, not smoothed. Silence is weighted by who would have had incentive and ability to publish. Prevalence claims cite prevalence data.

### Phase 3 — Fresh-eyes verification (facts AND framing)
A separate agent audits the draft: spot-check the load-bearing facts against independent sources; then audit framing — which loaded adjectives were imported from sources; does every strong claim sit on the tier the ledger assigns it; what would a smart advocate of each Phase-0 stakeholder say is missing, and is it actually missing; do any of the eleven failure modes appear? The orchestrator answers every finding — fix or explicitly overrule.

### Phase 4 — Delivery
Answer first, scaled to the scope of the question, with every load-bearing claim carrying an inline citation. Then the ledger: **established / documented-through-a-vehicle / claimed-but-unverified / labeled forecasts (with confidence) / unknowable.** State what evidence would change the conclusion. For health/medical questions, lead with the clinical-consensus position, grade the evidence, and note that the report is research, not personal medical advice. For purchase research, hand the final recommendation block to the `shopping` skill's format (price, best place to buy, direct link).

---

## Model selection

- **Orchestrator (Phase 0 framing, adjudication, synthesis, final quality):** the highest-capability model available in the session — the framing and adjudication decisions are where research quality is actually won or lost.
- **Lane workers:** default to a Sonnet-class model. Upgrade a single lane to a frontier model when its subtask is genuinely hard (dense primary-document analysis, methods-section adjudication, subtle comparison design). Haiku-class almost never — only trivial, fully-specified, high-volume grunt work.
- **Verifier (Phase 3):** at least as capable as whichever model drafted the report — verifier ≥ author, always.
- **Quick mode:** runs acceptably on a mid-tier model precisely because the self-audit requirement compensates; the audit section is not optional at any capability level.

## Modes

**Full mode (big questions):** orchestrator runs Phase 0, launches lanes as parallel sub-agents with self-contained briefs, adjudicates, drafts, sends draft + this spec to a fresh verifier, resolves findings, delivers.

**Quick mode (~10-15 min, single agent — validated 2026-07-10 on a marketing-captured consumer-health topic):** compress the lanes into sequential mini-passes (~20-30 tool calls), prioritize the primary/data and ground-experience lanes, test only the load-bearing comparisons — and END with a mandatory self-audit against the eleven failure modes, reporting what was caught, corrected, and left unresolved. The self-audit is what makes small-budget output trustworthy.

---

*Relationship to the sibling: `deep-research-contested` adds a political counterweight (asymmetric process, truth-fixed evidence standards) for questions where the left-right axis runs through the evidence ecosystem. This skill is the same rigor without the rudder.*
