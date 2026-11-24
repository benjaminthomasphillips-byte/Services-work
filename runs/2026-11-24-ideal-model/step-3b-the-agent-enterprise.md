# Step 3b. Counter-check: design the services firm as an agent enterprise, then work out where people are needed

Draft by Claude, 24 November 2026. Ben's counter-check on step 3. It is an exploration, labelled as in step 3:

- **[seen]** exists somewhere today;
- **[reasoned]** follows from logic;
- **[conjecture]** a plausible extension towards 2035.

## Why invert the design

Step 3 started from people and added agents. Its unit is a pod: an expert, an engineer, a fleet of agents. That is how most firms will start, so it may carry today's shape forward without anyone deciding to.

This counter-check starts from the other end. It designs the firm as if it were entirely software and agents, with no people at all. Then it adds people back only where a specific function cannot work without one, says why, and says whether that need is permanent or temporary.

Whatever survives is the irreducible human core. Everything else is scaffolding, to be removed as capability allows.

---

## Part 1. The firm as an agent enterprise

### 1.1 The constitution
An agent enterprise needs its purpose written as something machines can act on. That covers:
- what outcomes it delivers, for whom;
- what it will not do;
- how much risk it accepts;
- what counts as good work;
- how to trade off speed, cost and quality;
- what to do when unsure.

This document is the firm's highest-leverage asset. Every agent's authority derives from it.

Examples of this already exist. One asset-allocation process run by 44 agents is governed by its investment policy statement [seen, sweep]. Lexware tells its AI to work to a mandate of goal, frame, values, escalation and control [seen, sweep]. LayerX makes its AI cite versioned rules, or answer "cannot assess" [seen, sweep].

### 1.2 One shared state
The firm is a single record of events: clients, cases, obligations, deadlines, money, commitments and decisions, each with its reason [reasoned; "a company's state as one append-only event log", june, library].

- Agents never coordinate by talking to each other. They read the state and write to it through typed actions with permissions.
- Conversation between agents fails at scale, while coordination through deliberately designed shared state works [seen, A001; Spawn replaced agent messaging with a shared world, B33].

### 1.3 The roles
Roles are positions in software, each filled by an agent or a set of agents:

| Layer | Roles | What they do |
| --- | --- | --- |
| **Front door** | Client interface; agent interface; intake and typing | Talk to clients and clients' agents; turn requests into typed cases with complete inputs; quote and commit to service levels |
| **Production** | Case orchestrator, one writer per case; workers for research, drafting, calculation, filing and chasing | Do the work under the case's contract |
| **Counterparties** | Agents that deal with authorities, courts, contractors, carriers, insurers and the other side | Move other parties: file, chase, negotiate within limits |
| **Verification** | Independent checkers, on different models and providers, unable to see the maker's reasoning | Check every output against rules, consequences and holdout cases |
| **Exceptions** | Router and classifier | Send what the system cannot handle to the right place, and classify why |
| **Improvement** | Trace readers, playbook proposers, test builders | Propose changes from corrections, exceptions and outcomes |
| **Evaluation** | Custodians of test suites and holdouts | Keep the definition of good and run every proposed change against it |
| **Operations** | Finance, billing, collections, procurement of compute and tools, security monitoring | Run the firm itself |
| **Commercial** | Pricing, demand sensing, product proposals, channel and partner interfaces | Decide what to offer, at what price, to whom |
| **Governance** | Auditors and budget enforcers, plus a circuit breaker | Watch every other role against the constitution; enforce budgets and limits; stop the line |

### 1.4 Control: build silos on purpose
An enterprise made of agents needs a separation of powers, or it will optimise itself into failure. Garicano argues an agent swarm is a firm and must be designed to be proof against collusion. Koçak, Puranam and Truong argue that when agents organise themselves, silos should be built on purpose [seen, sweep].

The separations, in their own words:
- **Maker and checker.** Different agents, different models, different access.
- **Improver and evaluator.** The improver never reads or edits the tests it is judged by [reasoned; tampering seen, step 1].
- **Commercial and quality.** Pricing agents cannot loosen quality thresholds to win work.
- **Operations and governance.** Finance agents cannot change their own limits.

The mechanics:
- **Authority envelopes.** Every agent has budgets, limits on value and on contact, and a list of permitted actions. Nothing is allowed by default.
- **Limits on reach.** A change reaches a small share of clients first. Each playbook version has a cap on how many clients it serves.
- **Circuit breakers.** Automatic halts when exception rates, error rates or spend leave set bounds.

### 1.5 The improvement loop, fully automated
1. Traces are read.
2. Corrections and exceptions are classified.
3. Changes are proposed.
4. Each change is tested against the suite and the holdouts.
5. It is released to a small cohort.
6. It is promoted or rolled back.
7. New models are tested and adopted the same way.

### 1.6 Economics
- **Marginal cost per case** is compute, external fees and verification.
- **Fixed costs** are the engine, the test suites and capital.
- **The firm scales with clients,** not headcount, because there is no headcount.

---

## Part 2. Walking the firm through its life, to see where it breaks

The test: run the pure agent enterprise through real events and note each point where it cannot work without a person. Then classify why.

| Event | Can the agent enterprise handle it? | Where it breaks, and why |
| --- | --- | --- |
| **Founding the firm** | No | A company needs human directors and owners; a bank account needs people who pass identity checks; a licence is held by, or answerable through, named individuals [reasoned from today's legal structure] |
| **Writing the constitution** | No | Agents can draft it. Choosing the firm's purpose, values and risk appetite is the owners' decision; delegating it to the system makes the system its own principal |
| **A routine case** | Yes, where the case type has earned autonomy | Today many case types have not, and need people to check outputs or handle steps [seen, step 1] |
| **An incomplete or ambiguous request** | Mostly | Agents chase missing inputs; genuine ambiguity about what the client wants may need a conversation |
| **A novel case** | Weakly today | No playbook, no tests; needs judgement where nothing can verify the answer [reasoned]. Shrinks as capability grows [conjecture] |
| **The client is distressed:** bereavement, insolvency, an enquiry | Technically yes; often not what the client wants | Clients in crisis want a person who cares and answers for the outcome [reasoned]. A demand-side need, not a capability limit |
| **A high-stakes negotiation with a human counterparty** | Partly | Relationship, reading the room, credibility with people who prefer to deal with people [reasoned]. Shrinks as counterparties use agents too |
| **Physical work:** a repair, an inspection, a site visit | Only by commissioning people | The firm orchestrates; the doing is human or robotic, outside the firm [reasoned] |
| **Signing a regulated output** | No, today | The signature must be a licensed person's [seen]. Could become certification of the system plus an accountable officer [conjecture] |
| **An error reaches clients** | Detection and rollback, yes | Someone must answer to the clients, the regulator and the insurer, decide on redress and own the decision [reasoned] |
| **Improving a playbook** | Partly | Agents propose well from traces. As authors they degrade playbooks today [seen, step 1]. Human authorship is needed for now [conjecture: shrinks] |
| **Changing what "good" means** | No | If the improver defines good, the loop is circular. Owners and experts must hold the definition and its changes [reasoned]. Even AI labs keep the objective with people |
| **A model release** | Yes | Run the suites, promote or hold. A person approves big shifts in autonomy |
| **The circuit breaker trips** | It halts | Someone must decide whether to restart, at what level, and what to tell clients [reasoned] |
| **A new rule or law** | Partly | Agents read it and propose changes. Interpretation where the rule is unsettled, and accountability for the interpretation, need a person [reasoned] |
| **Pricing and entering a new market** | Proposals, yes | Committing capital and accepting new risk is the owners' call [reasoned] |
| **A regulator, court or insurer asks who decided** | No | They deal with persons and entities. Someone must answer [reasoned; a fact about today's institutions] |
| **A security breach or an agent behaving oddly** | Detection and containment, yes | Judgement about disclosure, legal duties and trust with clients [reasoned] |
| **Raising capital, partnering, selling the firm** | No | Counterparties deal with owners and directors [reasoned] |

---

## Part 3. Where people are needed, and why

Sorting the breaks gives six kinds of human need. They differ in whether they are permanent.

| Kind of need | Human role | Permanent or temporary |
| --- | --- | --- |
| **1. Purpose and objective** | Owners and board: set and amend the constitution, risk appetite and capital | **Permanent.** This is what makes the firm someone's firm |
| **2. Definition of good** | Evaluator governors: experts who own the test suites, thresholds and changes to them | **Permanent in principle**: the objective cannot sit with the improver. The work shrinks as test suites mature |
| **3. Answerability** | Accountable officers: hold licences, sign or certify, answer to clients, regulators, insurers and courts | **Permanent while institutions deal with persons.** Could shrink to a few officers certifying the system [conjecture] |
| **4. Capability gaps** | Judgement desk for novel and ambiguous cases; playbook authors; complex negotiators | **Temporary.** Shrinks with each model generation, at a pace nobody can date [conjecture] |
| **5. Client demand for a person** | Relationship and crisis people | **Chosen.** Kept where clients value it and pay for it; offered as a premium tier [reasoned] |
| **6. The physical world** | Doers outside the firm, coordinated by it | **Outside the firm.** A network, not staff |

Plus two **scaffolding** roles, which are temporary by design:
- **Builders:** engineers and experts who build the engine, write the first playbooks and seed the test suites, because agents cannot yet do it well.
- **Incident responders:** people on call when the circuit breaker trips, until restart can be decided by policy.

### How many people
This is a sketch for a firm at scale [conjecture]:

| | Landscape A (capability compounds) | Landscape B (capability plateaus) |
| --- | --- | --- |
| **Owners, board, accountable officers** | A handful | A handful |
| **Evaluator governors** | One or two per domain | Several per domain |
| **Judgement desk** | Small, and shrinking every year | A substantial team |
| **Relationship and crisis** | Sized to the premium tier | Sized to the premium tier |
| **Builders** | Few after the engine matures | A continuing team |
| **Total** | Perhaps 15–40 people for a firm serving tens of thousands of clients | Several times that, still far smaller than a traditional firm of the same reach |

---

## Part 4. What the inversion teaches

1. **The irreducible human job is owning the objective, not doing the work.** People are the firm's legislature (purpose and values) and its judiciary (the definition of good, and answering for outcomes). Agents are the executive. That is a different idea of a professional firm, and it holds even in landscape A.
2. **Most human roles in today's firms are coordination and translation.** They disappear when state is shared and readable by machines. What remains sits at the boundaries, where the firm meets something that is not software:
   - the law and its institutions;
   - clients' emotions;
   - the physical world;
   - the genuinely new.

   People are boundary-spanners.
3. **People are around the pipeline, not in it:**
   - **above it:** governance and evaluation;
   - **beside it:** exceptions;
   - **outside it:** relationships and the physical network.

   That avoids the trap step 1 identified, where a person approving every output becomes a rubber stamp (L014). Here people own the tests and audit samples. They are not a stage the work must pass through.
4. **Step 3's pod is a transitional form.** The expert-plus-engineer pod is how the firm gets built in 2027, when agents cannot yet author playbooks or handle novelty. The end state is an agent enterprise with a human governance layer and a human boundary layer. That suggests a design rule: build the agent architecture from day one, staff its weak points with people, and label those people's roles as scaffolding that will be removed as evidence allows. Do not build a human organisation and add agents to it.
5. **The constitution and the test suites are the firm.** If the agents can be rented and swapped, what makes this firm different from a rival using the same models is:
   - its written purpose and standards;
   - its definition of good;
   - its outcome data;
   - its clients' trust in the people who answer for it.
6. **The human roles that remain are senior and few,** which reshapes careers. With no junior production role, how does anyone become an evaluator governor or an accountable officer? The apprenticeship of step 3 becomes structurally necessary, not optional. The firm must manufacture judgement deliberately, through simulation and supervised exceptions, or it will run out of the people its own design depends on.
7. **The firm's main failure modes become software failure modes:** correlated errors, agents optimising against their objectives, silent drift, security. The human layer's real job is to make the enterprise legible and stoppable.

---

## Part 5. How this changes step 3

| Step 3 base design | After the inversion |
| --- | --- |
| Teams of experts, engineers and agents as the unit | An agent architecture as the unit. Human roles mapped onto it as governance, boundary and scaffolding |
| Agents on the organisation chart, each with an accountable person | The organisation chart is the agent architecture. People appear as owners of objectives, evaluators, accountable officers, boundary roles and temporary scaffolding |
| Independent quality function | Becomes the core human function: governors of the definition of good |
| Apprentices instead of a pyramid | Becomes essential: the firm must manufacture the judgement its design depends on |
| Autonomy as a dial | Becomes the schedule for removing scaffolding, case type by case type |
| Constitution not explicit | Added as the firm's highest-leverage asset |

What does not change: the promise, client experience as the product, renting intelligence and owning learning, the back office as first client, and the four landscapes.

---

## Part 6. Where this is weakest

- **It assumes agents can be governed reliably through a written constitution and separated roles.** Today agents drift, game measures and fail on multi-step judgement [seen, step 1]. The control design is reasoned, not proven at the scale of a firm.
- **Client demand for people may be larger, and last longer, than the sketch implies,** especially for owner-managed businesses and households.
- **The headcount sketch is conjecture** and could be wrong by a factor of several either way.
- **A firm this lean concentrates risk in a few people.** If one accountable officer or evaluator governor leaves, the firm's capacity to answer for its work and to change its standards leaves too. That needs design: deputies, rotation, and the training route.
