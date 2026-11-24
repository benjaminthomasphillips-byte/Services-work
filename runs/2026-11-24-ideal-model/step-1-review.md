# Review of step 1, "The engine" (draft of 24 November 2026)

Single reviewer. The job here is to attack the draft. It is not praised and not rewritten. Cited rows were checked against the 2026-11-23 evidence files and ledger. Sweep items could not be checked, so only obvious stretches are flagged.

## Verdict

The draft has a useful skeleton: the four layers, the three groups of task requirements, the separation of powers, and the idea that checkability can be designed. But it is less inferential than it looks. Its central analogy, that a services firm improves the way a lab does, depends on an evaluation structure that services mostly lack: repeatable trials, a counterfactual, a settled right answer, and enough cases per type to tell a real gain from noise. The draft never tests that analogy. Its boldest call, that checkable services become winner-take-most, is really a bet. In the summary it is stated as a flat claim, and the draft's own leakage point contradicts it. Its moat claim, that the corpus compounds, ignores who legally owns the corpus and who else sees the same outcomes. And it leaves out the economics of the engine altogether: what evaluation costs, who pays for it, and who keeps the gain. Against the agreed standard, it skips "how fast comparable shifts went" for every premise and rarely says who gains. Several citations are stretched in ways that matter. The client turned down an earlier attempt for bold calls with nothing behind them, and this draft is at risk of the same objection on points 7 and 8 and on P5's timeline.

---

## 1. Does the engine framing and the lab analogy hold?

Only partly, and the draft relies on the parts that do not hold.

**What carries over.** Generating a change is cheap and judging it is expensive. An improver must not grade itself. Model upgrades need regression testing. These hold.

**What does not carry over.**

- **There is no counterfactual.** A lab can run the old model and the new model on the same 10,000 tasks. A services firm handles each client case once. It never sees what the other playbook would have done for that client. Without randomisation, there is no clean comparison. Randomising clients between two versions of a signed tax return or legal letter raises regulatory and ethical problems, and the draft does not mention them.
- **"Known right answers" are mostly past expert decisions.** A regression suite of past cases with "known right answers" (P1, components table) measures agreement with how experts used to do the work. It rewards copying and penalises a genuine improvement that departs from past practice. Only outcome data can show that a change is *better* rather than *the same as before*, and outcome data is the slow loop. So the fast loop and the "better" loop measure different things. The draft treats them as one dial ("evaluation latency"). This is the most important gap in the reasoning.
- **Sample size is ignored.** How fast a firm can tell whether a change helped depends on the number of cases per case type and on how often failures happen, not just on elapsed days. Suppose a case type has a few hundred cases a year and its serious errors are rare. A one-point improvement then cannot be confirmed for years, however fast each check runs. P3's routing table splits the work into many case types, which makes this worse: each type has a thinner sample. Most of the long tail will never produce a statistically usable signal. The draft's measure, "days from making a change to knowing whether it helped", should be "cases needed to know", turned into days by volume.
- **There is no recursion.** In a lab, the improved system improves the improver: better models do better AI research. In the firm, the improver is a rented model the firm does not improve. The table names a meta-level ("the improvement process") but gives no mechanism or measure for how that process improves itself. As written, this is kaizen with machine-generated suggestions. That may be valuable, but calling it "recursive self-improvement" oversells it to an investor.
- **The gains are S-curves, not compound growth.** Within one case type, the exception rate and the cost per case approach a floor. The draft accepts this ("the long tail shrinks but does not disappear") yet uses the language of compounding throughout. Compounding, if any, comes from widening scope, trust and distribution. The engine does not supply those by itself.
- **The analogy cuts the other way.** The actors with real recursive improvement are the labs. Unit 2 (call 8) already says labs and vendors are moving into services. If "the engine" is the winning asset, the best-placed owner of it may be a lab-backed operator, not this firm. The draft does not ask this question.

**Fix.** Add an explicit premise on the evaluation structure of services. Separate *conformance* evaluation (fast; checks agreement with the rules and with past practice) from *outcome* evaluation (slow; checks whether the work was better). Add sample size per case type. Say which services have repeatable, counterfactual-friendly structure, such as high volume with defined outcomes like reconciliations and claims triage, and which do not. Rename "recursive self-improvement" or justify the recursion.

---

## 2. Over-inference, by premise

### Summary and section 4.7: winner-take-most (point 8)
- In the summary it is stated with no tier: "the engine produces winner-take-most markets". Section 4.7 calls it a hypothesis. It is a bet, and the summary should say so.
- **The mechanism does not follow from the draft's own premises.** Section 1 says model gains reach every rival on the same day. Section 4.6 says any single improvement is copied within a year or two. If both are true, a learning-rate lead is bounded and erodes. Learning-curve advantages have historically been worn down by spillovers and tend to produce oligopolies and price wars, not single winners. Winner-take-most needs something that does not leak: network effects, switching costs, regulatory licences, a balance sheet for warranties, or the fixed cost of evaluation infrastructure spread over volume. The draft names none of these as the driver.
- **The evidence the run already holds points the other way.** In two UK local-service roll-ups, the measured result was *higher* prices, followed by competition remedies (ledger, Part 1: vets and funerals). That is the opposite of the "lower prices bring more clients" flywheel. A leader that gets close to winner-take-most in a UK professional market can expect the CMA and the professional regulators to step in.
- The strongest counter-argument is not stated: learning saturates, and scale in services has historically been limited by local licensing, trust and regulation rather than by unit cost.

### P1: evaluation sets the speed (tiered as a mechanism)
- This is a reasonable mechanism, but the counter-argument is the weak one. The strongest is that *validity*, not latency, is the binding constraint. A fast evaluation of a proxy makes the wrong thing improve faster. If so, the headline "speed of evaluation" points the firm at the wrong investment. Sample size, covered above, is the second strongest counter.
- **Citation problems.**
  - Ramp (R-WEB-SELFIMPROVE-06): the row says the reported gains are efficiency measures (tokens, tool calls, time), not quality, and a human accepts every suggestion. The draft cites "120 merged suggestions" as evidence that candidates are cheap, which is fair, but it should note that none was shown to improve the work.
  - Starbucks (R-LIB-FAILURES-02) was a computer-vision counting tool that failed on reflections and Wi-Fi. The ledger itself flags "computer vision, 2025, not a language model". It is one case, and it is generalised here to "test accuracy has not predicted field performance".
- **Cold start is a missing point.** A firm built new in 2027 has no past cases, so its regression suite starts empty. "The first engineering investment is evaluation" collides with having nothing to evaluate against. That reverses part of Unit 1's argument that building new is better (axiom 2): for the corpus, the incumbent or the acquired book has the history, though the data is poor. The draft needs a view on how the engine runs in years one and two.

### P2: checkability can be designed (tiered as a mechanism)
- The possibility is a mechanism. "Sometimes a hundredfold" has nothing behind it.
- The Toyota example is about inspecting every document rather than a sample. That is inspection coverage, not moving an outcome from the slow loop to the fast one, so it is a stretched illustration.
- **The strongest counter-argument is missing, and it is strategic.** The services whose outcomes can be made fast-checkable, such as reconciliations, routine returns and compliance checks, are the same services Unit 2 (call 1) expects to become nearly free and bundled into banks, software and the state. So the engine compounds fastest exactly where the margin disappears. The draft passes this to step 2 as a neutral parameter. It is a direct tension with the investment case and belongs in this step.
- A second counter: daily checkpoints check easier things, not the thing that matters. Whether the tax position is right is still known only at enquiry. More signals of the wrong kind can make the firm more confident without making it better.

### P3: the inventory is an output (tiered as a mechanism)
- "It is always current" and "the map cannot drift from the work" overclaim. The routing table records what the classifier *believes* each case is. A case forced into the nearest known type is not flagged as unknown. It is silently misrouted, and the map then drifts exactly as Marble's map does, only less visibly.
- In services, what a case really is often becomes clear only part-way through: a "simple" return turns out to involve a trust. So classifying on arrival is a weaker idea than the draft implies.
- The routing table only sees demand that arrives. It cannot show work the firm should offer but does not. That was part of the point of Ben's inventory: choosing what to turn into products.
- There is a conflict with sample size, covered above: finer case types give more precise routing but thinner evidence for each type.
- Ledger Q1 adds that each firm's process is "bespoke" even where the name is shared (R-LIB-IMPROVE-TECH-36). That matters for pooling cases across acquired books, and the draft does not mention it.

### P4: the third group of requirements (tiered as a mechanism)
- **This is the most serious citation stretch in the draft.** It says the quoting workflow "had all four" of Ben's requirements. The row (R-LIB-DELIVERY-05) says it had "a test set", not a verifier, and the draft's own table defines a verifier as independent of the maker. The row also warns that "success [is] defined differently for the two rates", so 92.8% against 22.3% is not like for like. The case shows that synthetic tests mislead. It does not show that Ben's four are insufficient.
- The three groups are sensible but standard. Anyone who has run machine learning in production would list the same items. Present them as a useful checklist, not as an insight.

### P5: people govern the evaluator (mechanism for the rule, bet for the dates)
- **The evidence is miscast.** The draft says "each is a failure of an improver judging itself". That is true of R-WEB-SELFIMPROVE-24 and -25 (models tampering with scoring code). It is not true of the others:
  - /26 is playbooks that agents wrote for themselves *before* attempting the work;
  - /27 is distilled playbooks doing worse than reusing raw records;
  - /28 is repeated rewriting that erodes detail;
  - /20 is a proxy built from *human* approval signals.

  These show that agents are poor *authors* of know-how and that human signals can be poor evaluators. Neither is the same as evaluator capture.
- **"The direction is the mechanism" is not earned.** The direction, agents writing most changes by about 2029, depends on agents becoming good improvers. The draft's own evidence (/26, /27, /28) points against that today. The direction is a bet. Only the separation rule is a mechanism.
- **The strongest counter-argument is understated.** The ledger (Part 6) has human checkers deferring to the machine (R-WEB-STACK-27; R-WEB-PEOPLE-17: half of 523 junior staff did no better than the agent alone). "People own the evaluator" assumes people who do not defer. The draft cites only L014.
- **The rule is too weak as stated.** An improver that never reads the checks can still overfit to them by submitting repeatedly and keeping what passes. That is the keep-best gate in /15. Isolation must be backed by limited query budgets and fresh, rotating holdouts. Section 4.4 says this, but P5's rule does not.
- **Who governs the governors?** If the people who own the evaluator are paid or promoted on the engine's improvement rate, they have a reason to set lenient thresholds. The separation must also hold among the people, not only between people and agents.

### P6: the corpus compounds (mechanism for the logic, bet on the size)
- **Legal ownership is barely touched.** The corpus is mostly client material. Several questions are missing entirely: purpose limitation under data protection law; confidentiality and privilege (R-WEB-LAW-13/14); whether the outcome history of acquired books legally transfers; what happens to a client's records and derived data when the client leaves; and whether derived models trained on that material are a lawful reuse. "Contracts that grant it" assumes clients will sign. Clients' agents (Unit 2, call 2) will read those terms and negotiate them.
- **The strongest counter-argument is missing.** For the outcomes the draft calls the firm's own (enquiries, disputes, claims, complaints), the counterparty sees more than the firm does. HMRC sees enquiry outcomes across every preparer, insurers see every claim, and Xero sees every ledger. The accountable firm sees only its own slice. In adversarial work (Unit 2, call 3), the counterparty also changes its behaviour in response, so the corpus of past outcomes goes stale faster than the draft assumes.
- Most outcomes are the *absence* of a signal: no enquiry, no complaint. Absence does not mean the work was right. Labels are therefore sparse and biased.
- The Intercom fine-tuning item comes from a software vendor with thousands of customers, not from a services firm. The draft notes it as a cost signal, but it still uses it to support the value of a services firm's corpus.
- One point in the draft's favour: /27 (replaying raw records beats distilled playbooks) supports P6 better than anything cited, and the draft does not use it.

### P7: readiness to adopt new models (trend for the need, mechanism for the advantage)
- **The citations are misread.**
  - R-WEB-SELFIMPROVE-19 was Anthropic's own *prompt and settings changes*, not a model release.
  - The degradation lasted days to weeks *before it was detected*; the revert was immediate once it was found. "Undo took days to weeks" misreads that.
  - The same row says the changes passed "multiple human and automated code reviews, as well as unit tests, end-to-end tests". That directly undercuts the idea that running the regression suite makes adoption safe in days.
  - R-WEB-SELFIMPROVE-30 is from 2023 and covers silent drift in a rented model, which is a different problem.
- **The size of the advantage is never estimated.** If rivals adopt within weeks, the gain from adopting first is a few weeks of each capability jump. Software vendors and labs, who adopt fastest of all, are also competitors (Unit 2, call 8). Faster adoption also widens the blast radius for correlated errors (section 4.5). As written, "mechanism for the advantage" is not earned. The need is a trend; the advantage is a modest bet.

### P8: full context (mechanism, bet on recording norms)
- **There is an internal contradiction.** The draft cites L022 ("records people must enter separately die") and also relies on "decisions are written at the point of decision". Writing down *why* is exactly the separate entry that L022 says dies. The draft needs a mechanism that makes the reason a by-product of the work, or it needs to concede the point.
- The Scribe item (vendor, one experiment) adds nothing and weakens the list.
- **A legal point is missing.** "Pay people for adding to what the firm knows" means measuring each person's contribution. AI that evaluates workers or allocates tasks by individual behaviour is high-risk under the EU AI Act from December 2027, and works councils hold a veto in Germany and the Netherlands (ledger, Part 13). The routing of cases to people and the judgement desk may fall under the same regime.

### Other unearned confidence
- "The 2030s scandal, when it comes, will be a correlated error" (section 4.5) is an assertion.
- Chroma's "Red Queen" half-life (N053) comes from a rival buyer with no completed deals (ledger). It sits in the opening paragraph as if it were established.
- "Two independent verifiers" (section 4.5) are not independent if both are models from the same provider or trained on the same corpus.

---

## 3. Vanilla: which of the eight points are non-obvious

| # | Point | Verdict |
| --- | --- | --- |
| 1 | Evaluation sets the speed | Common knowledge among AI practitioners ("evals are the bottleneck"). It may be new to a services investor, but it is not insight. It would become insight if it were turned into "cases needed to know, per case type". |
| 2 | Checkability is a design choice | **Genuinely non-obvious, and the best idea in the draft.** It is underdeveloped and misses its own strategic tension (see P2). |
| 3 | Inventory as output | Partly non-obvious as a reply to Ben. To an operations person it is ticket triage. It is overclaimed. |
| 4 | Third group of requirements | Vanilla for anyone who has run machine learning in production. A useful checklist. |
| 5 | Separation of powers | Standard AI-safety thinking ("don't let the model grade its own homework"). The framing is useful; the people side, which would be the non-obvious part, is missing. |
| 6 | Corpus with outcomes is the moat | Vanilla: every venture capitalist says "proprietary data is the moat". It is already Unit 2's call 6. The non-obvious versions would be the counterparty point or the legal-ownership point, and both are missing. |
| 7 | Model-adoption readiness | Common practice in AI engineering. The advantage is unsized. |
| 8 | Winner-take-most where checkable | **Non-obvious and the most consequential.** It is also the least supported. |

So the claim that "several are not obvious" is fair only for 2 and 8, and partly 3. The summary should lead with these and present the others as hygiene.

Further vanilla items: section 4, points 1 to 4 (learning curves, the hard cases concentrate, skills atrophy, measures get gamed) are well-known automation lore (Bainbridge 1983, Goodhart). They are correct, but there is nothing new in them as written.

---

## 4. What is missing entirely

1. **The economics of the engine.**
   - What does building and maintaining a verifier and regression suite cost per case type?
   - What volume per case type pays for that?
   - How many experts who can define "better" exist, and how many case types can each one govern? Expert time to own evaluators is probably the binding constraint on how many case types can run as an engine.
   - The ledger (Part 6) says that where automation succeeded, the check was about two-thirds of the remaining cost (R-LIB-DELIVERY-29), and that the signed check stays human. That sets a cost floor the learning curve in section 4.1 ignores.
2. **Who gains.** The agreed standard asks for this in each mechanism, and the draft rarely gives it. In unit-priced markets, savings went to clients: RWS margin and profit fell while repeat revenue held (ledger, Part 1). If the engine lowers cost and competition lowers price, the client gains, not the firm. Chroma's point, that the saving stays with the owner only where the firm is short of capacity, needs answering.
3. **Who pays for evaluation.** Clients do not pay for regression suites. Is evaluation an overhead, a cost of the licence, or something insurers subsidise? Unit 2 makes the insurer a design partner. The engine's evidence could be what insurers price on, and that would be a real reason to invest.
4. **The client side.**
   - The client co-produces the work (Unit 1), and incomplete input is the commonest failure (P4). The engine's improvement rate is therefore partly set by the client's discipline.
   - Clients may not want their service restructured for checkability.
   - Clients' agents will run *their own* evaluations of the firm (Unit 2, call 2). That is an external evaluator the firm does not govern. It could be a threat, or it could be a cheaper source of outcome signals.
5. **Legal ownership of the corpus and of improvements.** Covered under P6. Also missing: whether corrections sent through a model provider's API improve the provider's models, and therefore rivals' (mentioned only in passing in section 4.6); and what transfers on exit or sale. The investor will care about this at exit.
6. **The people side of the separation of powers.**
   - How does someone become an evaluator owner when juniors no longer do routine work? Skill atrophy (section 4.3) hits the evaluator owners hardest, because they stop doing cases.
   - Status, pay and career for evaluators compared with producers.
   - Whether experts will codify the judgement that keeps them employed (R-WEB-PEOPLE-30 is cited only under P8).
   - The licensed signatory's place: the ledger places the release gate for shared procedures at the centre and sign-off with the signatory. How does that fit with auto-promotion?
7. **Adversarial and non-stationary outcomes.** Unit 2 says counterparties will run agents and adapt. A corpus built against yesterday's counterparty behaviour misleads.
8. **The comparable-speed evidence the standard requires.** No premise says how fast comparable shifts went. Usable comparables include:
   - the spread of lean and total quality management outside Toyota (decades);
   - continuous delivery and DevOps in software (roughly a decade from niche to mainstream);
   - continuous accounting and real-time reconciliation (available for years, adopted slowly in small firms);
   - how quickly experience-curve advantages were competed away.

---

## 5. Internal contradictions and poor fit

- **The layer table against section 4.6.** The table says know-how and the improvement process are got by "nobody" else. Section 4.6 says improvements leak within a year or two. The improvement process, meaning evaluation and release tooling, is also exactly what vendors sell: the Ramp evidence comes from a Langfuse customer story. It is the most copyable layer, not the least.
- **P5's rule against P5's timeline.** "The improver must never be able to … edit the checks" sits beside a 2032 row in which agents propose test changes that people approve. Given the rubber-stamp counter-argument the draft states itself, that amounts to editing.
- **P8's reliance on L022 against decision records written by people.** See above.
- **"Prefer fast-checkable services" (P2) against "never build where the end state is free" (Unit 2, call 1).** These pull in opposite directions, and nothing reconciles them.
- **Building new against having a corpus.** Unit 1 says building new is the strongest choice. This draft's engine needs history that only incumbents and acquired books hold. P6 says buying books supports volume, but the acquired data may not be usable or lawful to reuse.
- **Tiering differs between units.** Unit 2 gives the outcome-data moat "high" confidence. This draft calls its size a bet. Pick one.
- **The "stop all improvement for a quarter" test is confounded.**
  - If the engine is automated, "stopping improvement projects" does not stop it, so what is being switched off?
  - A model release, a rule change or seasonal mix in the quarter would swamp the result.
  - Holding steady is ambiguous: it fits either good automation or a stable quarter.
  - An investor cannot run this test in diligence.

---

## 6. Ranked objections

1. **Section 1 and P1–P2: the lab analogy assumes an evaluation structure services lack.** There is no counterfactual, "right answers" are past practice, and the sample per case type is thin. *Fix:* add a premise separating conformance evaluation from outcome evaluation; measure "cases needed to know" per case type; say which services have the structure; drop or justify "recursive".
2. **Summary point 8 and section 4.7: winner-take-most is a bet stated as a mechanism**, contradicted by section 4.6 and the layer table, and against the ledger's roll-up price and regulation evidence. *Fix:* tier it as a bet; name the non-leaking driver (fixed cost of evaluation, licence, balance sheet, agent-readable track record); give the counter-argument about saturation, spillovers and competition regulators.
3. **Missing: the engine's economics and who gains.** Evaluator cost, expert-time limits, the cost floor of the check (two-thirds of the residual), and price pass-through to clients. *Fix:* add a section with per-case-type break-even and value capture.
4. **The agreed standard is not met.** No comparable speeds anywhere, and "who gains" is mostly absent. *Fix:* add both to every premise.
5. **P2: the engine compounds fastest where the margin disappears** (Unit 2, call 1). *Fix:* confront it here. Either fast-checkable services are a training ground and not the profit, or the profit is in the warranty and the signature on top.
6. **P5: evidence miscast and the direction unearned.** /26–28 and /20 are not evaluator capture. Human checkers defer. Isolation alone does not stop overfitting. The evaluators have incentives of their own. *Fix:* recast the evidence, tier the direction as a bet, and add query budgets, rotating holdouts and separation among the people.
7. **P6: legal ownership and the counterparty's larger view.** Data rights on client and acquired material; HMRC, insurers and software vendors see more outcomes; most labels are absences; counterparties adapt. *Fix:* add these as the main counter-argument and say what the firm can lawfully own.
8. **P1 and P6: cold start for a firm built new.** The regression suite starts empty, which is in tension with Unit 1's case for building new. *Fix:* say how the engine runs in years one and two, and where the first corpus comes from.
9. **P4 and P7: citation misreadings.** The quoting workflow had a test set, not a verifier, and its two rates are defined differently. R-19 was prompt and settings changes, its regressions went undetected despite broad test suites, and the revert was quick. *Fix:* correct both; let R-19 qualify P7's "adopt in days".
10. **P7: the advantage is unsized and probably small.** *Fix:* estimate the lead in weeks against rivals and vendors; set it against the risk of correlated error; tier the advantage as a bet.
11. **P3: "cannot drift" overclaims.** Misclassification is silent, case types often emerge mid-case, the table sees only incoming demand, and finer types mean thinner evidence. *Fix:* add misclassification audits and scope the claim.
12. **The client side and the people side are missing.**
    - Clients as co-producers.
    - Clients' agents as external evaluators.
    - EU AI Act high-risk duties for task allocation and contribution pay.
    - Evaluator skill atrophy.
    - The licensed signatory against auto-promotion.
    - The L022 contradiction.

    *Fix:* add a short section on each, or pass each explicitly to steps 4 and 7.

Also correct the summary's "several are not obvious": only points 2 and 8, and partly 3, are. Lead with them.
