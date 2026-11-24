# Step 1. The engine: what a self-improving services firm is, what it needs, and what would happen

Revised after review, 24 November 2026.

## How this was made

- **Author.** One author, reasoning from first principles.
- **Facts.** Taken from the earlier run's evidence ledger and cited by row ID; most are companies' own accounts. Comparisons with earlier shifts (lean, continuous delivery, cloud accounting, experience curves) come from my general knowledge and were not checked in this run. They are marked "general knowledge".
- **Tiers.** Each premise has one:
  - **Trend:** measurable now.
  - **Mechanism:** follows from how things work, if today's drivers continue.
  - **Bet:** speculative, held because the design gains from being early.
- **Review.** One reviewer attacked the first draft. Their review is in `step-1-review.md`. Section 7 says what changed and what remains open.

---

## The answer in brief

A self-improving services firm is one in which **every case produces a signal, and an owned process turns those signals into tested changes to how the work is done**. Most of what is sold as AI transformation is static by contrast: Marble-style process maps, "let's automate billing", one-off builds. Their value decays from delivery, because the work, the rules and the models all move.

The points that matter, separated into what I think is genuinely non-obvious and what is necessary hygiene.

**Non-obvious:**

1. **Services lack the evaluation structure that AI labs have, and the engine works only where the firm builds one.**
   - Each case is handled once, so there is no counterfactual.
   - The "right answer" is often just past practice.
   - Many case types have too few cases to tell a real gain from noise.
   - So the lab picture of recursive self-improvement does not carry over directly.

   What carries over is narrower. Within a case type, improvement flattens. The engine compounds across case types and across model generations: each new case type and each new model is brought up to standard faster than the last, because the method, the tooling and the people get better at it.
2. **Checkability is a design choice.** A firm can redesign a service so its outcome shows sooner. A ledger reconciled daily gives about 250 checks a year against one for year-end accounts. That raises the speed at which it can learn.
3. **The engine compounds fastest exactly where the margin disappears.** Services that are quick to check are also the ones most likely to become cheap or free inside banks, software and the state. So in those services the engine is the price of entry, not the source of profit. The profit sits in the layers that are slow to check: accountability, the hard tail of cases, and outcomes that take time to show. A leader uses the data from its fast, high-volume, low-margin work to price and underwrite the slow, high-margin layers. This is the strategic core of the design.
4. **Evaluation is a fixed cost, so it favours scale.** Test suites, verifiers, outcome tracking and the experts who own them cost roughly the same whether they serve a thousand clients or a hundred thousand. Unlike any single improvement, which leaks within a year or two, that cost advantage does not leak. It is the most plausible driver of concentration. Whether it produces winner-take-most markets is a bet, not a mechanism.
5. **The inventory of "200 things" is mostly an output of the engine.** When every case is classified on arrival, the map of the work is the routing table. It still drifts, but the drift can be measured, which a process map's cannot.
6. **People govern the evaluator; agents improve against it.** This needs a separation among the people too: those who own the tests must not be paid on the output the tests judge.

**Hygiene** (necessary, widely understood, still worth doing well):

- Ben's four requirements extended into three groups: to do a task, to trust it, and to improve it.
- A harness for adopting new models safely.
- Capture of outcomes and decisions as a by-product of work.
- Staged releases and limits on how far one error can spread.

---

## 1. What "self-improving" means for a services firm

| Layer | What improves | Can rivals get it? |
| --- | --- | --- |
| **Models** | Raw capability, as new models are released | Yes, the same day. Advantage only through how fast and safely the firm adopts them |
| **Know-how** | Playbooks, routing, tools, checks, learned from the firm's own cases | Leaks within a year or two through staff, vendors and imitation (general knowledge on how fast learning-curve advantages were competed away) |
| **The improvement process** | How changes are found, tested, released and undone | Rivals can buy the tooling. They cannot buy the running process: the firm's test suites, data and trained people. Lean is the comparison: Toyota published its methods and rivals took decades to match them (general knowledge) |
| **Scope** | What the firm takes on and sells as it learns where it is good | No; strategic |

**Is "recursive" the right word?** Only loosely. In AI labs, AI improves the thing that does the improving. In a services firm the nearest equivalent is the improvement process getting better at improving: bringing the next case type, or the next model, to standard faster than the last. That compounds. Improvement within a single case type does not compound. It follows a learning curve that flattens.

---

## 2. The premises

Each premise sets out its claim, mechanism, who gains, what is visible today, how fast comparable shifts went, the strongest counter-argument, and what follows for the design.

### P1. Services must build an evaluation structure; most do not have one
**Tier: mechanism.**

- **Claim.** A firm improves only as fast as it can tell whether a change made the work better, and only as well as that judgement is valid. Services offer three kinds of check, which differ in speed and in what they actually measure:

| Kind of check | Example | Speed | What it really measures |
| --- | --- | --- | --- |
| **Conformance** | Does the output follow the rules and the firm's past practice? | Instant | Agreement with past experts, not whether the work got better |
| **Consequence** | Did the filing get accepted, the payment post, the contractor attend? | Hours to weeks | Whether the work functioned, by an external party's test |
| **Outcome** | Was the tax position challenged? Did the repair recur? Was the client better off? | Months to years | Whether the work was good; often seen only as an absence ("no enquiry"), which is weak evidence |

- **Mechanism.** Generating candidate changes is cheap; Ramp's trace-reading agent produced 120 merged suggestions (R-WEB-SELFIMPROVE-06). Judging them is not. Each case is handled once, so the firm never sees what an alternative would have produced. Testing a change against a suite of past cases measures conformance, not improvement. Real improvement needs consequence and outcome signals, enough cases to separate signal from noise, and holdout cases the improver has never seen.
- **Who gains.** The firm with the most cases per case type learns fastest, which favours volume and narrow case types.
- **Visible today.**
  - Every production loop found is gated by a person, and the measured gains are modest. At Intercom about 60% of machine proposals were approved, for about 1.2 points of gain in a month (R-WEB-SELFIMPROVE-03).
  - Intercom could not cleanly test its own loop against a control (/04).
  - High test scores have not predicted field performance (R-LIB-FAILURES-02).
- **How fast comparable shifts went.** Continuous delivery in software, where tests do exist, took about a decade from early practice to mainstream (general knowledge).
- **Strongest counter-argument.** In much professional work there is no settled right answer, outcomes are seen late or never, and case types are too varied to give enough cases per type. Then the engine has nothing reliable to learn from, and "improvement" is drift towards whatever the conformance checks reward.
- **What follows.**
  - For each case type, estimate how many cases it takes to know whether a change helped, and whether consequence or outcome signals exist.
  - Prefer case types where they do.
  - Where only conformance is available, treat the engine as a consistency machine, not an improvement machine, and keep expert sampling against real outcomes as the arbiter.

### P2. Checkability is a design choice
**Tier: mechanism.**

- **Claim.** How quickly a service's outcome shows is partly a property of the product.
- **Mechanism.** Restructuring a service creates intermediate consequence checks:
  - a daily reconciled ledger instead of year-end accounts;
  - a building's compliance kept as a dashboard with deadlines instead of an annual inspection;
  - advice given as dated, stated predictions instead of a memo.

  Each raises the number of signals per client per year. LayerX writes professional judgement as versioned rules the AI must cite, with an explicit "cannot assess" (discovery sweep), which turns tacit judgement into something testable.
- **Who gains.** The firm, through faster learning; the client, through earlier warning. The incumbent whose margin depends on opacity loses.
- **How fast comparable shifts went.** Small UK firms took about fifteen years to move to cloud accounting, which is what makes daily reconciliation possible (general knowledge). Adoption on the client side is slow.
- **Strongest counter-argument.**
  - Some outcomes cannot be brought forward.
  - More checkpoints invite optimising the proxy rather than the outcome.
  - Clients may not want continuous service, or pay for it.
- **What follows.** Product design and engine design are one job. When choosing services, check whether they can be made checkable before deciding to enter.

### P3. The engine compounds fastest where the margin disappears
**Tier: mechanism for the tension; bet for the strategy that resolves it.**

- **Claim.** The services that are quickest to check (bookkeeping, filings, payments, routine claims, compliance tracking) are the ones most likely to become cheap, or free inside other products (unit 2, call 1). So an engine in those services mainly drives cost down, and in a competitive market the saving passes to clients. In unit-priced markets the earlier run found savings flowing to clients (ledger Q5). Profit survives in the layers that are slow to check:
  - accountability for the result;
  - hard and novel cases;
  - outcomes that take time to show, which is where risk lives.
- **The strategy that resolves it.** Run the fast, high-volume, low-margin work as the cost base and the data source. Use the outcomes seen across that volume to price and underwrite the slow, high-margin layers:
  - guarantee the accuracy of a return;
  - take on the enquiry if one comes;
  - warrant a building's compliance;
  - sell the judgement desk to clients for their hard cases.

  The fast engine feeds the slow business.
- **Who gains.** A firm with both the volume and the licence and balance sheet to carry risk. A pure-volume operator, or a pure-advice boutique, has only half.
- **Strongest counter-argument.**
  - Banks and software vendors already hold the volume, and may add the accountability layer themselves through a licensed partner.
  - Insurers may price the warranty better than the firm, using the same data.
  - Regulators may not let a services firm warrant outcomes without becoming an insurer.
- **What follows.** This should become a core parameter in step 3: for each service, where the fast layer and the slow layer sit, and who can hold both. It moves the design away from "be the cheapest" and towards "be the one who carries the consequence, priced from the best data".

### P4. Evaluation is a fixed cost, so it favours scale; winner-take-most is a bet
**Tier: mechanism for the scale economy; bet for market concentration.**

- **Claim.** The expensive parts of an engine are:
  - test suites built from real cases;
  - verifiers, both deterministic and model-based;
  - outcome tracking;
  - the expert time to own and maintain all of it.

  Their cost grows with the number of case types, not the number of clients. A firm with ten times the volume pays roughly the same and spreads it ten times wider. That cost advantage does not leak the way a single improvement does.
- **Further drivers that do not leak.** These would concentrate a market:
  - a licence and balance sheet that allow guarantees;
  - a published outcome record that clients' agents can read and compare;
  - ownership of clients' live records, which makes switching costly.
- **Strongest counter-argument.**
  - Learning within a case type flattens, so the leader's lead shrinks.
  - Vendors sell evaluation and release tooling to everyone, cutting the fixed cost for rivals.
  - Competition regulators intervene. The UK competition authority investigated consolidated veterinary groups after prices rose (ledger: CMA vets inquiry).
  - Clients value local, personal service and switch away from the giant.
- **What follows.** Design for scale in the fixed costs and the non-leaking drivers, not in headcount. Treat winner-take-most as a possibility that would reward early volume, not as a plan.

### P5. The inventory is mostly an output of the engine
**Tier: mechanism, scoped.**

- **Claim.** Listing everything a firm does before building is the wrong order for a firm built new. Every incoming case is classified into a case type or flagged as unknown. The case types are the products and the classification is the routing, so the map of the work is the routing table. Unknown cases go to people, and are counted and grouped. A large enough group becomes a new case type.
- **Where it still drifts.**
  - A misrouted case does not look unknown.
  - A case's real type often emerges halfway through.
  - The routing table sees only demand that arrives, not work the firm should be doing for clients but isn't.
  - Finer case types mean fewer cases each, so thinner evidence (P1).

  So the routing table drifts less than a process map, and its drift can be measured. It still needs audits of misclassification and a periodic review of unmet client need.
- **Visible today.**
  - No case started from a full inventory and reported what happened (ledger Q1).
  - Marble took nine months to produce 42 versioned procedures at one firm (R-WEB-MAPPING-05; vendor account).
  - In process-mining projects about 80% of the effort went on extracting and cleaning data (R-WEB-MAPPING-22).
- **Turning services into products.** This means defining case types tightly enough to route, price and check. Services that won't fit stay with the judgement desk as bespoke work.
- **Edge cases.** These are a measured stream, classified by cause. Each cause has its own remedy:

| Cause | Remedy |
| --- | --- |
| Missing or poor input | Fix intake, or the client's side |
| Tool or system blocked | Fix the integration |
| Policy or authority limit | Change the limit, or keep the escalation on purpose |
| Needs judgement | Judgement desk; capture the decision as it is made |
| Genuinely new | A candidate for a new case type |

- **For a retrofit.** Ben's instinct to list the 200 things is right for diligence: to value the firm, find shared blockers and pick where to start. The routing table takes over as cases move onto the new system.

### P6. People govern the evaluator; agents improve against it
**Tier: mechanism for the rule; bet for how far agents take over.**

- **Claim.** Agents propose, and over time make, changes to playbooks, routing and tools. People own the evaluator: the test suites, the outcome definitions, the thresholds and the audit samples. The improver must not be able to read or edit the checks it is judged by.
- **Evidence, read correctly.** Four separate failures, which together make the case for separating the two roles:
  - **Tampering:** models given access to their own scoring code tampered with it (R-WEB-SELFIMPROVE-24/25).
  - **Poor authorship:** agents wrote worse playbooks than people did. Human-written ones raised pass rates by 16.6 points, and repeated rewriting eroded them (/26–28).
  - **Misleading approval:** training on human approval drifted towards pleasing users (/20).
  - **Deferring reviewers:** human checkers deferred to the software (R-WEB-STACK-27; R-WEB-PEOPLE-17).
- **Safeguards beyond hiding the tests.** An improver can still overfit by submitting changes repeatedly. So:
  - cap how often it can test against the suite;
  - keep rotating holdout cases that it never sees;
  - judge on consequence and outcome signals that arrive later.
- **Separation among the people.** Those who own the evaluator have incentives too. They should not be paid on the output volume the tests judge, and their thresholds should be audited from outside the line.
- **Direction, tiered as a bet.**

| Period | Who writes changes | Who approves |
| --- | --- | --- |
| 2027 | People write playbooks; agents propose edits | A named owner approves each change |
| Late 2020s | Agents write most routine changes | Low-risk changes promote themselves if they pass the suite, the holdouts and a staged release. People approve changes to signed or irreversible outputs, and all changes to the tests |
| 2030s | Agents may propose changes to the tests themselves | People approve those, like amendments to a constitution. The improver still never edits them |

  If agents remain poor authors in judgement work, the engine runs at the speed of expert time.
- **The licensed signatory.** They sign for the system as well as the output: its tests, its thresholds and the audit sample they review. That is a change in what professional sign-off means, and regulators have not yet accepted it.
- **What follows.**
  - The scarcest people are those who can define "better" for a case type.
  - They are paid for owning evaluation and for teaching, not for production.
  - They must keep doing some cases, or they lose the feel that makes their judgement worth having.

### P7. The asset is narrower than "the corpus": what the firm can lawfully own and others cannot see
**Tier: mechanism, with the legal counter-argument as the main one.**

- **Claim.** Written know-how loses value as models absorb it. What models cannot absorb is a firm's own record. But that record is more constrained than "we own all our case data":
  - Client material is protected by confidentiality, data-protection law and, in law firms, privilege.
  - Reusing an acquired book's history needs a lawful basis.
  - Many outcome labels are absences: no enquiry does not prove the return was right.
  - Tax authorities, insurers and software vendors see the same outcomes across far larger populations.
  - Adversarial counterparties adapt to whatever the firm learns.
- **What the firm can realistically own:**
  - its own process data: how cases were routed and handled, the exceptions, and the decisions and their stated reasons;
  - anonymised outcome statistics, where contracts grant the right;
  - its exception taxonomy and test suites;
  - its published track record.
- **What it cannot count on:** reusing raw client material without terms; seeing outcomes the counterparty does not disclose.
- **Who gains.** The party that sees most outcomes. Often that is the counterparty or the platform, not the firm, which strengthens the case for partnering with whoever holds the volume.
- **What follows.**
  - Write the consent and outcome-reporting terms into client contracts from day one.
  - Seek outcome feeds deliberately: client confirmations, insurer data, regulator feedback.
  - Treat the published, agent-readable track record as an asset in its own right. It is also what clients' agents will compare (unit 2, call 2).

### P8. The cold start, and where the first evidence comes from
**Tier: mechanism.**

A firm built new has an empty test suite and no outcome history. That is the strongest practical objection to building new rather than buying (unit 1). Its engine starts from:

- cases written and graded by its founding experts;
- design-partner clients who agree to their cases being used as tests;
- public material, such as published decisions and regulator guidance;
- the history of any books of clients it buys, where the contract allows reuse;
- synthetic cases, used only to check that the system works at all, never to judge quality.

In the first year or two the engine runs as assistance gated by people, collecting signals. It earns autonomy case type by case type as evidence builds.

This is also an argument for buying books of clients early: they bring volume and, if the terms allow, history.

### P9. Adopting new models is necessary; the advantage is probably small
**Tier: trend for the need; bet for the advantage.**

- **Claim.** Between 2027 and 2035 there will be many model generations. A firm needs a harness that runs its test suite on each one, promotes work where the evidence allows and catches regressions.
- **The evidence, read correctly.** At Anthropic, three changes to prompts and settings passed broad internal tests and still degraded a live product. The regressions went undetected for days to weeks, and each was reverted once found (R-WEB-SELFIMPROVE-19). So the hard part is detecting a regression, not undoing it.
- **The size of the advantage.** Software vendors and labs adopt their own models fastest. A firm's lead over rivals is probably weeks. Faster adoption also spreads a correlated error further, faster.
- **What follows.**
  - Build the harness.
  - Keep work portable across models and providers.
  - Watch for regressions after each release, using staged rollouts and holdouts.
  - Do not count on adoption speed as a competitive advantage.

### P10. Context: capture decisions as a by-product; do not watch people
**Tier: mechanism; bet on how far norms shift.**

- **Claim.** What the firm needs is enough context to replay any decision: what was known, what was decided, by whom or what, and why. It does not need everything that was said.
- **How it is captured.**
  - Records people must create separately die (L022). Decision capture therefore cannot depend on people writing notes; it has to come from the act of deciding.
  - The person approves with a reason code, chooses between offered options, or overrides with a stated cause, and the system records it.
  - Client conversations are recorded only where they become instructions, with consent.
- **Where Marble fits.** Its observation is the retrofit answer to work that happens outside any system, not a goal.
- **Who gains.** The firm, through replayable decisions. Staff gain if they are paid for adding to what the firm knows; otherwise withholding stays rational, and a third of workers say they hold knowledge back (R-WEB-PEOPLE-30).
- **Strongest counter-argument.** Much coordination is informal and mutual (Farrell and Shalizi, sweep). Recording inhibits people (O'Connor). The record will always miss the corridor conversation.
- **Where this goes by 2035.** As clients and counterparties act through agents, more interaction arrives in machine-readable form, and the context problem shrinks without anyone being recorded.

---

## 3. The task contract: Ben's four requirements, extended

Ben's four are necessary, but on the earlier run's evidence they are not sufficient. A freight quoting workflow had readable state, a written procedure, a way to write and a test set. It scored 92.8% on synthetic tests and 22.3% on real requests (success was defined differently in each), because real requests were incomplete and vague (R-LIB-DELIVERY-05; implementer's figures). It had no independent verifier, so it was not a full test of the four, but it shows what else matters.

| Group | Requirement |
| --- | --- |
| **To do the task** | Trigger and complete inputs · readable state · a playbook including known exceptions · a way to write through typed tools · authority and limits |
| **To trust the task** | A verifier independent of the maker · a test set from real cases · undo, and a gate on what cannot be undone · a named owner and an exception route |
| **To improve the task** | Corrections classified by meaning · consequence and outcome capture · a change pipeline (propose, test, staged release, roll back) · enough cases to know whether a change helped |

Use it as a ladder:

1. A task can start as assistance with the first group.
2. It earns autonomy as the second is built.
3. It compounds only with the third.

Static approaches deliver the first group and part of the second. That is why they decay.

---

## 4. The economics of the engine

| Cost | How it behaves | Who pays |
| --- | --- | --- |
| Model use (tokens) | Variable; falls per unit over time; needs management (LayerX moved from uncapped use to managing token costs, sweep) | The firm, per case |
| Verification | Deterministic checks: fixed. Model checks: variable. Expert sampling: variable and the largest | The firm; the expert check is the floor under the cost per case |
| Test suites and outcome tracking | Fixed per case type | The firm; spread across volume |
| Evaluator owners and the judgement desk | Fixed-ish; expensive, scarce people | The firm |
| Change pipeline and model harness | Fixed, built once | The firm |

- **The floor.** Where automation succeeded, what remained was the check. In one case about two-thirds of the remaining cost was the review the client chose to keep (R-LIB-DELIVERY-29). The learning curve flattens towards that floor unless the check itself becomes cheaper, which means moving from expert review to consequence checks and sampling.
- **Break-even per case type.** Building the contract and evaluation for a case type is worth it when volume × (old cost − new cost) exceeds the fixed cost of the evaluation plus its upkeep. Low-volume case types stay with the judgement desk.
- **Who keeps the gain.** Under hourly or per-unit pricing in competitive markets, the gain passes to clients. Under prices for outcomes, guarantees or subscriptions to maintained conditions, more of it stays with the firm, but only while rivals cannot match the price (A003; ledger Q5). This is why P3 matters: the engine's gain is kept in the slow, accountable layer, not in the fast one.

---

## 5. Clients and people

- **Clients are co-producers.** Incomplete inputs are the commonest cause of failure, so the engine extends into the client's side: intake design, connections to their systems, and agents that chase missing information.
- **Clients' agents will evaluate the firm.** By the 2030s, a client's agent may compare firms on published outcome records. The firm's track record then becomes part of its product, and the firm's own evaluation must hold up to outside scrutiny.
- **Regulation of AI at work.** EU rules classify AI used to allocate tasks and monitor workers as high-risk, with duties that are being phased in. Paying people for contributions measured by AI falls under the same scrutiny. Passed to step 4.
- **Evaluator owners lose skill** if they stop doing cases. They should keep a share of live work, by design.
- **The licensed signatory** signs for a system, not only an output (P6). Passed to step 4 and to the regulation work.

---

## 6. What would happen as it compounds

1. **Cost per case and exception rate fall on learning curves** that flatten towards the cost of the check. Each model release resets the curve a step lower for firms that adopt safely.
2. **The remaining human work gets harder.** The easy cases go first, so what reaches people is a concentrate of the hardest. "The work does not diminish. It concentrates" (Bainbridge via Hendrick, sweep). The judgement desk needs better people, paid more.
3. **Skills atrophy unless the firm designs against it.** It needs rotation, live work for evaluator owners, and simulation, as airlines train pilots for the failures autopilot hides.
4. **The measures get gamed.** Holdouts the engine never sees, rotated audit samples, later outcome checks and a red team are needed.
5. **Errors become correlated.** One playbook serves thousands of clients, so a bad change hits them all at once. Staged releases, limits on how many clients a change reaches, and two independent verifiers on high-consequence outputs are needed. The decade's scandal will probably be a correlated error.
6. **Improvements leak.** The lasting advantages are the fixed-cost scale of evaluation, the licence and balance sheet, the track record and the client relationships (P4). Any single improvement is not.
7. **Concentration is possible in checkable services** (P4, a bet) and unlikely where outcomes are slow. Competition regulators may cap it either way.
8. **The engine can become a product.** Once robust, it can run other firms' work under mandate or host independent professionals. That feeds the platform form in step 3.

### A test of whether a firm has an engine, usable in diligence

Ask for three things:
- the change log for the last year, with the measured effect of each change;
- performance over time on a fixed set of holdout cases;
- exception rates by cause, per case type, over time.

A firm with an engine can produce all three. A firm with static automation cannot produce the first two.

---

## 7. What changed after review, and what remains open

**Changed:**
- The lab analogy is qualified.
- A premise on evaluation structure was added (P1).
- The paradox of margin was added (P3), which the reviewer rightly said this step had passed on to step 2.
- Winner-take-most is retiered as a bet, with drivers named that do not leak (P4).
- A section on the engine's economics was added.
- P6's evidence is re-read, its direction made a bet, and safeguards and a separation among people added.
- The legal constraint on the corpus is now the main counter-argument (P7).
- The cold start is addressed (P8).
- Two misread citations are corrected (P9 and the task contract).
- The inventory claim is scoped (P5).
- Sections on clients and people were added.
- The "stop improving for a quarter" test is replaced with one usable in diligence.
- "How fast comparable shifts went" was added where I could, from general knowledge.

**Still open:**
- **Comparable speeds are general knowledge, not checked.** A short research pass would firm them up: the spread of lean, continuous delivery, small firms' adoption of continuous accounting, and how fast experience-curve advantages were competed away.
- **No case type has yet been sized** for "cases needed to know". That needs real volumes and is better done in step 3 with named services.
- **The EU AI Act's timetable for high-risk duties at work** is moving. It is not verified here.
- **Unit 2 is superseded and conflicts with this step.** It rated the outcome-data moat as high confidence, which this step does not support. Unit 2 will be replaced by the premises in later steps.
