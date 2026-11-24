# What the library offers the design: a synthesis

Claude, 24 November 2026. For the owner, to read only. Nothing has been changed in the design files or in Notion, and nothing here is incorporated.

**What this rests on.** Two of the three planned reviews: `cases-core.md` (the 200 non-Pluris Cases; 50 bodies read) and `cases-pluris.md` (231 Pluris Cases; 30 bodies read). **The third, `findings-analyses.md`, does not exist in the folder**, so the library's Findings and Analyses collections are not covered here. Everything below is drawn from Cases only, and the reviewers read about a fifth of those in full.

**Labels.** "The record says" means a claim made in a library record, usually a company's own. "Inference" means my reading or the reviewers' reading, not the record's.

---

## 1. The ten most useful things, ranked

1. **Review rules already exist in some sectors** (N069, N065, N067; P048, P070, P145). *Bears on G5, step 4 §2.4, architecture §8 "biggest unknown".* The records say an NHS teleradiology call-off requires independent audit of at least 5% of reports; the SRA authorised Garfield.Law with named accountable solicitors; Crosby says people review all work. Pluris records describe three further forms: a bounded action space (P048), review by confidence band (P070), and a human gate only on the final act (P145). Inference: the "sampling or every output" choice is really five or more options, and some answers can be collected now rather than negotiated in 2027.

2. **Size on expert minutes per acceptable output** (N069). *G5 sizing.* The record says AI drafting saved 29.4 seconds per radiology report, with total radiologist time unmeasured; the Royal College's planning figure is about 15 minutes per CT. Inference: that is roughly a 3% saving, and the right sizing unit includes verification and correction.

3. **A retrofit sequence** (P210, P179, P128, P100, P145, P216). *Step 4 §10, §8 "Buy firms".* See section 5.

4. **A missing deployment-and-adoption layer** (N060, N016, N071, N088, P159). *Step 4 §2.1 five layers.* The records say freed capacity becomes profit "only when management puts it to work", that a tool built in a day took months of in-person work to be accepted, and that the lack of a product owner was the consistent barrier in law, freight and billing firms. Inference: the design has Builders and an Academy but no one whose job is turning capacity into volume.

5. **Where the saving lands** (N051, N061, N081). *Architecture §6 margins, G4.* The record N081 says a tax firm cut work about 75% and revenue about 15%, keeping owner earnings, purely by moving to subscriptions, with no AI. Inference: the seven designs' margins do not separate AI from repricing and consolidation; N081 is the control case.

6. **Awaab's Law as a ready-made condition** (N068). *G4, G1, G11; lettings.* The record (government guidance) gives 24-hour, 10-day, 3-day and 5-day clocks, starting when any part of the landlord or agent "becomes aware", with records supporting an "all reasonable steps" defence. Inference: "the home is dry and legal" already has a legal form, the add-only record becomes a statutory defence, and field capacity is the constraint.

7. **Engine practice in numbers** (N050, B3, N053, N005, B33). *Step 4 §5, §6.3.* Shadow mode before go-live with an agreed baseline (N050); separating genuine errors from carried-over preferences before corrections become tests (B3); a "graveyard" of failed uses re-tested at each model release (N053, N061); every action scored succeeded, blocked or errored (N005); full test suite every 15 minutes and 30-second rollback (B33). All company or vendor claims.

8. **Agent positions with a lifecycle** (N078, N086, N044, N048). *Step 4 §2.3.* Onboarding of about a week, retirement after three to six months, graded write rights ("none may send"), and time saved checked by a controller (N078); three supervised runs before autonomy (N086); fewer agents because overlapping ones conflict (N086). N048 adds a "state map" and a stop path.

9. **Move the check to the maker** (P068). *G5, G6.* The record says content arriving at compliance went from about 30% to 95% compliant once originators could self-screen. Inference: a second lever on review headcount, cutting what arrives before the review rule applies.

10. **Conduct as a real difference from rivals** (F004, N062, N073). *G7, G2.* The records say Dwelly's maintenance function targets contractor commission, and Debtist plans to hold collected client money for about 80 days to fund itself; Supa passes contractor costs at cost. Inference: G7 and G2 are not hygiene; they separate this firm from named rivals, who may undercut it by breaking them.

---

## 2. Counter-opinions, ranked by how much they should worry the designer

1. **A person's sign-off may add little** (N018, B33; P145, P174). *Challenges G5's named person, step 4's judgement-desk sizing, principle 8.* The record N018 (an Anthropic trial, secondary summary) says analysts took the agent's lean 86% of the time. B33 says judges trained on founder decisions learn "what is usually approved". P145 and P174 write approved decisions straight back into the agent's knowledge. Inference: if reviewers defer, approvals become precedent and the review rule buys less safety than the design assumes. This is the most serious, because headcount, safety and the evaluator all lean on it.

2. **Agents still break on multi-step judgement** (N015, N045, N086). *Challenges the 2027 row of step 4 §8 and the pace in §2.3.* An owner letter reports "shockingly poor" results and a pull-back; a peer-reviewed benchmark reports 41 to 87% failure across seven frameworks; a builder says verification now takes longer than building. Inference: not a refutation, but a first public promise met in 2027 looks optimistic.

3. **Adversaries learn the agent** (N079, B29, P089). *Challenges "autonomy is a dial" and test suites built from past cases.* N079 (anonymous, weakest) says a refund agent passed every test, then customers learned its phrasing and fraud rose fourfold. B29 records a flood of AI-written complaints in courts and at the Ombudsman. Inference: past cases cannot contain counterparties who adapt to you.

4. **Plain rules and integration may carry most of the gain** (P173, P165, P100). *Challenges reading G5 as "agents by default"; supports principle 15.* The library's analyst reading of P173 says integration and explicit rules produced the gain and AI was supplementary.

5. **Watching people is the market's cheapest retrofit tool** (P179, P155, P086). *Challenges G8 "never track what can be declared".* Keystroke capture, camera scoring of caregivers feeding pay, GPS alerts. Inference: the design's stance is deliberate, but rivals buying incumbents will use these and claim faster integration.

6. **Savings counted before demand is seen** (N001, N004). *Challenges any acquisition model that books savings in year one.* Commonwealth Bank reversed redundancies; Klarna repriced its human tier. Supports G5's measured sizing.

7. **Ownership may not be the cause** (N127, B15, N071, N059). *Challenges step 4 §7–8.* N127 (a working paper) finds AI-native start-ups 25% smaller, mostly where AI is built into what is sold. Inference: the product route (C8, the platform) may explain more of the headcount gap than operating firms does.

8. **Generalists versus specialists** (N113, N110). *Step 4 §2.2.* Bird kept only multidisciplinary staff; Mercari's one-person pods fell short on quality. Possibly reconciled if specialists write the frameworks generalists apply.

9. **Juniors self-serving precedent** (P191). *Against G9.* A 60% cut in senior time spent on juniors, with "no measure of independent judgment". Weak, but it shows the easy saving undermines the apprenticeship.

---

## 3. Where the library would make the design more specific

- **G5 / step 4 §2.4:** list the review-rule forms seen (sampling at a stated percentage, every output, bounded action space, confidence band, final-act gate); size on total expert minutes per acceptable output (N069).
- **Step 4 §2.1:** a deployment layer, or a named product owner per case type (N060, P159).
- **Step 4 §2.3:** agent position lifecycle, graded write rights, supervised runs before autonomy, a controller checking claimed savings (N078, N086).
- **Engine / step 4 §5:** gate autonomy changes on four measures: missed escalations, unnecessary escalations, reversals, material errors (B7, inference); a failed-use graveyard re-tested per model (N053); shadow mode with an agreed baseline (N050).
- **Step 4 §6.3:** a state map beside blast radius (N048); numbered circuit breakers and spend-anomaly detection (B33); PR revert rate as a change-pipeline metric (P009).
- **Step 4 §6.2:** production-data replay as one harness for both migrations and model upgrades (P216); per-client licence fees as a named "scale tax" (P039); Cars24 already at 8.88% of salaries on tokens (N080), so the 10–30% band for the 2030s may be low.
- **Step 4 §8 stop rules:** a six-week feasibility gate per case type with an accuracy threshold set in advance (P012).
- **Architecture §5:** a parameter for "a third party's statutory price funds the service" (N062, N065).
- **Architecture §6:** split margin into AI, repricing and consolidation (N081).

---

## 4. What the library is weak on, and how much weight it bears

**Status of the records.** Almost every B and F record is "Imported unverified"; most N records are "sources read; not independently verified"; all 231 Pluris records are promotional pages from one implementer, and five of the eight Pluris verification records come from one vendor. Several Pluris records duplicate B records, so they do not confirm them. B17 and B23 also cite Pluris.

**Claims versus results.** Nearly every operating figure is a company's own claim. The only observed sources are a few filings, regulator or government documents, a peer-reviewed benchmark (N045), a working paper (N127) and N018's trial, at second hand. Pluris reports no failure, rollback, staff outcome, full cost or later re-measurement.

**Coverage.** About 80 of 431 Case bodies read; Findings and Analyses not reviewed at all (missing file). Two negative-sounding Pluris titles (P038, P080) were not read.

**Where it is silent.** Error rates before and after a change of review rule; cost per condition including verification; a successor running another firm's service (G10); capital behind an outcome promise (G13); how judgement is grown without junior work (G9); outcomes for parties the firm does not serve; AI's share of holding-company results; a firm winning law reform; anything UK-specific beyond Awaab's Law and the SRA.

**How much weight.** Inference: good for patterns, vocabulary and examples of practice; enough to make sections more specific; not enough to settle any open question in architecture §8, and not enough to support any number in the margin or headcount tables. The counter-evidence is, if anything, better sourced than the success stories.

---

## 5. What bears on the next unit: retrofitting a messy incumbent

- **A sequence, assembled by the Pluris reviewer from separate vendor claims (inference):** read-only extraction first (P210); map what people actually do, not the org chart (P179, P128 "35+ disconnected systems"); find money lost between systems so the retrofit pays for itself (P100 billing rounded down, P165); write the policy before building agents (P145, P089); replay production data to prove equivalence (P216); cut over in phases and switch the old tool off (P128, P030); make onboarding of each site repeatable (P187).
- **The record is built beside the old systems, read-only, before anything is written back** (inference from P210, P216). That is a concrete answer to how G1 starts in a retrofit.
- **Past tickets become the first playbook and tests** (P128). A cold-start source for the engine.
- **Acquired firms bring ungoverned AI** (P119: 75 shadow-AI cases, 20 unauthorised connection paths). The tool gateway needs a day-one acquisition rule.
- **Keep the current judges** (N003: Ford rehired 300 veteran engineers; N071 founders roll over equity; N073 sellers leave). Inference: retention and rollover terms are a design variable, distinct from G9.
- **The adoption wall is the main cost** (N060, N016, N071 "two-to-five-year transformation"; P113 "change management, not engineering").
- **Staff may already have level-1 habits** (P057, P162) that the redesign must replace.
- **Leakage as the first promise** (P100, P086). Inference: a measurable early win that funds the rest.
- **The tension to settle:** the cheapest mapping tools watch people (P179), against G8. And integration plus rules may deliver the first gains before any agent (P173).
- **Missing for this unit:** any failed retrofit, staff outcomes, full cost, or who owns the record after migration (P-review gaps 1, 2, 4, 7).
