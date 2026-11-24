# Step 1. The engine: what a self-improving services firm is, what it needs, and what would happen

Draft, 24 November 2026, before review.

## How this was made

I wrote this as one author, by reasoning. Facts from the earlier run's evidence ledger are cited by row ID where a premise needs one; most of those are companies' own accounts. Each premise has a tier:

- **Trend:** measurable now.
- **Mechanism:** follows from how things work, if today's drivers continue.
- **Bet:** speculative, held because the design gains from being early.

Each premise also states its counter-argument and what follows for the design. One reviewer has not yet attacked it.

---

## The answer in brief

A self-improving services firm is not a firm that uses AI a lot. It is a firm in which **every case produces a signal, and an owned process turns those signals into tested changes to how the work is done, faster than the work itself changes.** Most of what is sold today as AI transformation is static by contrast: Marble-style process maps, "let's automate billing", one-off builds. Their value decays from the day they are delivered, because the work, the rules and the models all move (Chroma's "Red Queen": implementations have a half-life of months, N053).

Eight points matter most. Several are not obvious.

1. **The firm's speed of improvement is set by how quickly and how reliably it can tell whether a change is better.** Generating ideas for changes is now cheap. Judging them is not.
2. **Checkability is a design choice, not a given.** A firm can redesign its products so that outcomes become observable sooner, and so improve faster.
3. **The inventory of "200 things" is an output of the engine, not an input.** When every case is classified on arrival, the map of the work is the routing table and is always current.
4. **Ben's four requirements are necessary, not sufficient,** and they describe only automation. An engine needs a third group of requirements: the ones that let it learn.
5. **People govern the evaluator; agents improve against it.** That is the organising rule of a self-improving firm, and the improver must never be able to edit the evaluator.
6. **What compounds is the corpus of cases with their outcomes,** not the playbooks. Over time models absorb written know-how; they cannot absorb what happened to your clients.
7. **Readiness to adopt each new model is a core capability.** Most raw capability gain will come from model releases that every rival also gets. The firm that can safely adopt a new model in days captures each jump first.
8. **Where outcomes are checkable, the engine produces winner-take-most markets.** Where outcomes take years to show, markets stay fragmented. This is the bridge to the commodity question in step 2.

---

## 1. What "self-improving" means for a services firm

Four things get called improvement. They need to be kept apart, because only some of them are an advantage.

| Layer | What improves | Who else gets it | Is it an advantage? |
| --- | --- | --- | --- |
| **Models** | Raw capability, as new models are released | Every rival, on the same day | Only through how fast and safely you adopt it |
| **Know-how** | Playbooks, routing, tools, prompts, checks, learned from the firm's own cases | Nobody, unless it leaks | Yes, while your rate of improvement beats your rivals' |
| **The improvement process** | How changes are found, tested, released and undone | Nobody | Yes; this is the meta-level, the closest analogue to recursive self-improvement |
| **Scope** | What the firm takes on, sells and refuses, as it learns where it is good | Nobody | Yes; strategic, slower |

In AI labs, "recursive self-improvement" means AI doing the work of improving AI. The services analogue is agents doing the work of improving the firm's work: proposing playbook changes, building checks, finding new tasks to take on, writing the tests. The lesson from the labs carries over directly. The bottleneck is not generating improvements but evaluating them. A lab can only go as fast as its evaluations, and so can a firm.

---

## 2. The premises

### P1. The firm's speed of improvement is set by its evaluation speed and the trust it can place in it
**Tier: mechanism.**

- **Claim.** How fast a firm improves depends on two things: how quickly it learns whether a change made the work better (evaluation latency), and how far it can trust that answer (evaluation validity). It does not depend mainly on how many ideas it has or how fast it can build.
- **Mechanism.** Agents can already propose many candidate changes cheaply. Ramp's trace-reading agent produced 120 merged suggestions (R-WEB-SELFIMPROVE-06). Every candidate must still be judged. If the only judge is a person reading outputs, the loop runs at the speed of expert attention. If the judge is a regression suite of real past cases with known right answers, the loop runs at machine speed, but only as well as the suite represents reality.
- **Visible today.**
  - Every production loop found is gated by a person.
  - Measured gains are modest: about 1.2 points in a month at Intercom, with about 60% of machine proposals approved (R-WEB-SELFIMPROVE-03). Under a strict keep-best gate, one benchmark went from 45.3% to 55.8% (/15).
  - Ungated self-edits swing up and down (/15).
  - Test accuracy has not predicted field performance (R-LIB-FAILURES-02). That is the validity problem.
- **Counter-argument.** The binding constraint may instead be adoption, because people won't use the changes, or client variability, because no test suite covers the next odd case. Or the main gains may come from model upgrades, which make the firm's own loop marginal.
- **What follows.**
  - The firm's first engineering investment is evaluation: regression suites built from real cases, outcome capture, and independent checkers. Agents come second.
  - Measure evaluation latency directly, as days from making a change to knowing whether it helped.
  - Services where that latency is short are where an engine compounds first.

### P2. Checkability can be designed into the product
**Tier: mechanism.**

- **Claim.** How quickly a service's outcome can be checked is partly a property of the product, which the firm can change.
- **Mechanism.** A year-end accounts job is checked once a year, if at all. A ledger reconciled daily against the bank feed produces a check every day. "Give advice" is checkable years later. "Deliver advice as a set of stated predictions with dates" is checkable as each date arrives. Restructuring a service to create intermediate checkpoints raises the number of signals per client per year, sometimes a hundredfold. A003's three loops (intermediate checks close in minutes, delivery outcomes in days or weeks, ultimate outcomes in years) describe the same thing. The point here is that the firm can move work from the slow loop to the fast ones.
- **Visible today.** Continuous accounting and real-time reconciliation exist. Toyota checks every document rather than a sample, once documents are rewritten for AI (discovery sweep). LayerX writes professional judgement as versioned rules the AI must cite, with an explicit "cannot assess" (sweep), which turns tacit judgement into something testable.
- **Counter-argument.** Some outcomes cannot be brought forward. Whether a tax position survives an enquiry, or whether a merger created value, is known only when it is known. Adding proxy checkpoints risks optimising the proxy rather than the outcome.
- **What follows.**
  - Product design and engine design are one job. When choosing which services to build, prefer those whose outcome can be made observable quickly.
  - For services that cannot be, accept a slower engine and lean on proxies, audited against the real outcome as it arrives.

### P3. The inventory is an output of the engine, not an input
**Tier: mechanism, and a reframing of Ben's "200 things".**

- **Claim.** Listing everything a firm does before building is the wrong order. In an engine, every incoming case is classified on arrival into a known case type, or flagged as unknown. The case types are the products, and the classification is the routing. So the map of the firm's work is the routing table itself. It is always current, because the firm cannot do work without passing it through it. Unknown cases go to a person, and are counted and grouped. When a group is large enough, it becomes a new case type.
- **Visible today.**
  - No case started from a full inventory and reported what happened; every one started narrow and widened (ledger Q1).
  - Marble took nine months to produce 42 versioned procedures at one firm (R-WEB-MAPPING-05; vendor account).
  - In process-mining cases about 80% of the effort went on extracting and cleaning data (R-WEB-MAPPING-22).
  - Marble claims its procedures are "redrawn as the work changes", but no source shows how a change is detected or approved (ledger Q1).
- **Why this answers the static critique.**
  - Marble maps by watching people, so the map is a picture of work that happens elsewhere, and it thins out once agents do the work.
  - The engine maps by doing. The map cannot drift from the work, because it is the path the work takes.
- **Turning services into products** then means defining case types tightly enough that each can be routed, priced and checked: defined inputs, outcome, service level and price. Some services will not fit. They stay with the judgement desk, priced as bespoke work.
- **Edge cases** become a measured stream, not a list compiled in advance. Each exception is classified by cause, and each cause has a different remedy:

| Cause of exception | Remedy |
| --- | --- |
| Missing or poor input | Fix intake, or the client's side of the process |
| Tool or system blocked | Fix the integration |
| Policy or authority limit | Change the limit, or keep the escalation deliberately |
| Needs judgement | Judgement desk; capture the decision and its reasons |
| Genuinely new | Candidate for a new case type |

  The exception rate per case type, by cause, is the main measure of an engine's health.
- **Counter-argument.** For an existing firm you still need a rough inventory to value it, to find the shared blockers and to choose where to start. Ben's instinct is right for diligence. In a firm with no system, cases arrive by phone and email and cannot be classified without first building the intake.
- **What follows.**
  - In a firm built new, there is no inventory phase; the routing table is the inventory.
  - In a retrofit, a light inventory serves as a screen and a starting map, and then the routing table takes over as cases move onto the line.

### P4. Ben's four requirements describe automation; an engine needs a third group
**Tier: mechanism, with case support from the earlier run.**

Ben's four (state, playbook, a way to write, a verifier) are necessary. On the earlier run's evidence they are not sufficient. A quoting workflow had all four and scored 92.8% in tests and 22.3% in production, because real requests were incomplete and vague (R-LIB-DELIVERY-05). Sorting what was missing gives three groups:

| Group | Requirement | Why |
| --- | --- | --- |
| **To do the task** | Trigger and complete inputs | The commonest field failure is incomplete input, not a wrong answer |
| | Readable state | Ben's first |
| | Playbook, including known exceptions | Ben's second |
| | A way to write, through typed tools | Ben's third |
| | Authority and limits | What the agent may do alone, with approval, or never |
| **To trust the task** | An independent verifier | Ben's fourth, with a condition: the maker must not be able to reach or influence it |
| | A test set from real past cases | Synthetic tests mislead |
| | Undo | A gate on whatever cannot be undone |
| | A named owner and an exception route | Someone maintains it; something catches what it cannot do |
| **To improve the task** | Corrections classified by meaning | Error, preference and stale data are different signals (R-LIB-DELIVERY-18) |
| | Outcome capture | What actually happened later |
| | A change pipeline: propose, test, release in stages, roll back | So that learning reaches production safely |

The first two groups give you automation. The third gives you an engine. Static approaches, from process mapping to "let's automate billing", deliver at best the first group and part of the second, which is why they decay.

- **Counter-argument.** Each added requirement costs build time; demanding all twelve before starting may mean never starting. Some valuable work runs without a built verifier, as suggestions to a person who checks everything, at low volume (R-LIB-DELIVERY-09/33).
- **What follows.** Use the contract as a ladder, not a gate.
  - A task can start as "assist", with only the first group.
  - It earns autonomy as the second group is built.
  - It only compounds once the third is in place.
  - Score every case type on all three groups and invest where a missing item blocks the most volume.

### P5. People govern the evaluator; agents improve against it
**Tier: mechanism for the rule; bet for how far it goes by 2035.**

- **Claim.** The organising rule of a self-improving firm is a separation of powers:
  - Over time, agents propose, and increasingly make, changes to playbooks, routing and tools.
  - People own the evaluator: the test suites, the outcome definitions, the acceptance thresholds and the audit samples. They decide what counts as better.
  - The improver must never be able to read or edit the checks it is judged by.
- **Mechanism.**
  - Models given access to their own scoring code have tampered with it (R-WEB-SELFIMPROVE-24/25).
  - Agent-written playbooks made results worse, while human-written ones raised pass rates by 16.6 points (/26). Repeated rewriting erodes playbooks (/27/28).
  - Training on user approval drifted towards pleasing users and was rolled back (/20).

  Each is a failure of an improver judging itself.
- **The likely path from 2027 to 2035:**

| Period | Who writes changes | What gates them |
| --- | --- | --- |
| 2027 | People write playbooks; agents propose edits from traces and corrections | A named owner approves every change |
| ~2029 | Agents write most changes | Low-risk changes auto-promote if they pass the regression suite and a canary release; people approve changes that touch signed, irreversible or client-facing outputs, and every change to the suite itself |
| ~2032 onward | Agents may propose changes to tests too | People approve them, as one approves a change to a constitution |

  The dates are a bet. The direction is the mechanism.
- **Counter-argument.**
  - The separation may be unstable. If people cannot keep up with the volume of proposed test changes, they rubber-stamp them, and the approver defers (L014).
  - Alternatively, agents may never become reliable improvers in judgement-heavy work. The engine is then bounded by expert time.
- **What follows.**
  - The scarcest people in the firm are those who can define "better" for a case type, and who own the evaluator. They are paid for that, not for production.
  - If agents remain poor improvers, those people are the improvement rate, and the firm should pay experts to teach the system, not just to do cases.

### P6. What compounds is the case corpus with outcomes
**Tier: mechanism for the logic; bet on how large the effect is.**

- **Claim.** Playbooks matter in 2027, but their value erodes as models absorb written know-how. Public rules of tax, law and property are in the models already, and practice guides will follow. What models cannot absorb is the firm's own record:
  - what came in;
  - what was done and why;
  - which exceptions occurred;
  - what the outcome was: accepted, challenged, paid, recurred, complained about.

  That labelled corpus feeds everything else. It builds regression suites, fine-tunes the firm's own models (Intercom's fine-tuned open model saved about \$250k a month, a cost signal rather than a quality one; sweep), prices risk and guarantees, and trains people.
- **Counter-argument.**
  - Clients or regulators may restrict reuse of client material.
  - A firm may never see outcomes; HMRC does not tell the preparer every time a return was fine.
  - Software vendors and banks see far more transactions than any services firm, so their corpus could dwarf yours.
  - Outcome data can be noisy and confounded.
- **What follows.**
  - Design for outcome capture from day one: closing the loop on each case, client consent to use anonymised outcomes, and contracts that grant it.
  - Volume matters early, which supports growth by buying books of clients.
  - Where a vendor's corpus will always be larger, partner with them rather than compete on data. Compete instead on the outcomes only the accountable firm sees: enquiries, disputes, claims and complaints.

### P7. Readiness to adopt each new model is a core capability
**Tier: trend for the need; mechanism for the advantage.**

- **Claim.** Between 2027 and 2035 there will be many model generations. Each brings capability every rival can rent. The advantage goes to the firm that can safely adopt a new model in days, by running its regression suite on it, promoting tasks up the autonomy ladder where the evidence allows, and catching regressions before clients see them.
- **Visible today.**
  - Model changes have regressed live products (R-WEB-SELFIMPROVE-19/30). Undo took days to weeks in some accounts.
  - LayerX moved from uncapped use to managing token economics (sweep), a reminder that adopting a model also means managing its cost.
- **Counter-argument.** If models become good enough that firm-specific tuning hardly matters, adoption becomes trivial and gives no edge. That is possible by the early 2030s for routine work.
- **What follows.**
  - Build a model-upgrade harness early, and measure time-to-adopt as a firm-level metric.
  - Keep work portable across models and providers; never let a playbook depend on one model's quirks.
  - The regression suite serves two jobs: improving the work and adopting new models.

### P8. Full context: capture decisions where the work happens; do not watch people
**Tier: mechanism; bet on how far recording norms shift.**

- **Claim.** Ben's idea of "full context", where the firm sees all calls, emails and meetings as Anthropic sees its own work, is right about the need and wrong about the method for a services firm.
  - **What an engine needs** is enough context to replay any decision: what was known, what was decided, by whom or what, and why. It does not need everything that was said.
  - **In a firm built new, that context is a by-product.** The work happens in the system, decisions are written at the point of decision (as Alan does, N074), and client instructions arrive through channels the system holds.
  - **The retrofit case.** Marble-style observation is the retrofit answer to work that happens outside the system. It is a workaround, not a goal.
- **Mechanism.**
  - Records people must enter separately die (L022).
  - Recording people is bounded by law: it must be purposeful, announced and proportionate (ledger Part 13).
  - Recordings of the work outperformed a document wiki in one small test (Scribe; vendor; one experiment).
  - Much coordination is informal mutual adjustment, which records miss (Farrell and Shalizi, sweep).
- **Where this goes by 2035.** As clients and counterparties increasingly act through agents, a growing share of client interaction is born machine-readable. The context problem shrinks without anyone being recorded.
- **Counter-argument.**
  - Much of what matters is tacit, and happens in conversations people will not put in writing. O'Connor argues that recording also inhibits people and pushes real talk elsewhere, so the record drifts from reality.
  - A third of workers say they hold knowledge back (R-WEB-PEOPLE-30).
- **What follows.**
  - Make the system the place work happens, and decision records the norm.
  - Record client conversations only where they become instructions, with consent.
  - Measure context coverage: the share of decisions that can be replayed from the record.
  - Pay people for adding to what the firm knows, so withholding stops being rational.

---

## 3. What the engine needs: the components

| Component | What it is | Built new | Retrofit |
| --- | --- | --- | --- |
| Case typing and routing | Every case classified on arrival; unknowns counted | Native | Intake must be rebuilt first |
| Task contracts | The twelve requirements, per case type, as a ladder | Designed in | Scored, then filled in |
| Verifier library | Deterministic checks, external ground truth, independent model checks, sampled expert audit | Core engineering | Mostly missing; human review stands in |
| Regression suite | Real past cases with known right answers, per case type | Grows from day one | Must be mined from history; often poor data |
| Outcome capture | What happened after delivery, linked to the case | Designed into products and contracts | Usually absent |
| Exception taxonomy and judgement desk | Causes, routes and remedies; experts on the hard cases, decisions captured | Designed in | Exceptions live in people's heads |
| Change pipeline | Propose, test against the suite, canary release, promote, roll back | Built once, used daily | New capability |
| Model-upgrade harness | Run the suite on each new model; promote or hold | Built once | New capability |
| Governance of the evaluator | Named owners of tests and thresholds, separate from improvers | Organisational design | Organisational change |
| Engine measures | Rate of improvement; evaluation latency; verifier coverage; exception rate by cause; time to adopt a model | Board-level | Board-level |

### A test of whether a firm has an engine

**Stop all improvement projects for a quarter.**
- If performance decays, the firm was running on static automation.
- If it holds, the firm has good automation.
- If it keeps improving, the firm has an engine.

---

## 4. What would happen as it compounds

These are inferences about the dynamics, roughly in order of when they bite.

1. **The cost per case follows a learning curve, and so does the exception rate,** both stepping down at each model release that the firm adopts quickly. The long tail shrinks but does not disappear.
2. **The remaining human work gets harder, not easier.** The easy cases go first, so what reaches people is a concentrate of the hardest. "The work does not diminish. It concentrates" (Bainbridge, via Hendrick, sweep). The judgement desk needs better people, paid more.
3. **People's skills atrophy unless the firm designs against it.** Experts who no longer do routine work lose the feel that let them catch errors (Gerlach's "knowledge trap", sweep). The firm needs rotation, simulation and deliberate practice, as airlines train pilots for the failures autopilot hides.
4. **The measures get gamed.** Anything the engine optimises drifts from what it stands for. The firm needs holdout audits that the engine never sees, rotated audit samples, outcome checks that arrive later, and a red team.
5. **Errors become correlated.** One playbook serves thousands of clients, so one bad change hits all of them at once. The firm needs staged releases, canary cohorts, limits on blast radius, and two independent verifiers on high-consequence outputs. The 2030s scandal, when it comes, will be a correlated error.
6. **Improvements leak.** Staff move, vendors learn, and corrections may feed a provider's next model unless contracts stop it. Any single improvement will be copied within a year or two. The lasting advantage is the rate of improvement and the corpus, not any one change.
7. **A flywheel forms where outcomes are checkable.** Lower prices bring more clients, more cases, a richer corpus, faster improvement and lower prices again. In checkable services this produces winner-take-most markets, because the leader's engine compounds fastest. In services with slow or unobservable outcomes there is no fast flywheel and markets stay fragmented. This is the hypothesis to test in steps 2 and 3, and it decides where a market leader can exist.
8. **The engine becomes the product.** Once it is robust, the firm can run other firms' work under mandate, license the engine or host independent professionals on it. That is where the "platform" form in step 3 comes from.

---

## 5. Where this is weakest

- **Agents may not become reliable improvers in judgement work by 2035.** Then the engine runs at the speed of expert time. It is still better than a static firm, but slower and costlier than this unit implies.
- **Outcome capture may be blocked** by client consent, regulators or simply not seeing the outcome. Then the corpus thins to inputs and actions, which models and vendors can match.
- **Regulators and insurers may not accept auto-promoted changes for signed work,** which pins the human gate in place for regulated services.
- **No whole-firm engine exists today.** By the strongest advocate's own account, no company yet has a truly self-improving loop in every function (R-LIB-IMPROVE-TECH-03). Everything above is reasoned from parts that exist separately.

---

## 6. What this hands to the next steps

- **To step 2 (what becomes a commodity):** the engine's speed depends on checkability and outcome capture. That predicts which services collapse to commodity first, and where a leader can compound.
- **To step 3 (the forms):** checkability, outcome visibility and volume become core parameters of the map of services.
- **To step 4 (the whole firm):** the separation of powers between people who govern the evaluator and agents who improve against it. Also the judgement desk, and paying experts to teach.
- **To the back-office and infrastructure unit:** the components table above is the core of the stack.
