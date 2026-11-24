# Step 4. Building the firm: the base design, rewritten around the architecture

Claude, 24 November 2026. This replaces the base design in step 3. It is built on `architecture-v1.md`, which was tested on seven services. Those seven redesigns (`level3-*.md`) are the worked examples.

Labels used throughout:

- **[seen]** exists today
- **[reasoned]** follows from logic
- **[conjecture]** a plausible extension towards 2035

Unlabelled points are design choices, reasoned from the architecture.

---

## 1. How to design a firm for a given service

Use this order. Each step points to the part of the architecture it applies.

1. **Choose the service and the segment.** Read off the parameters (architecture, section 5): principals, agent or principal, who writes the rules, continuous or episodic, who pays, who controls the outcome, client size, what is produced, trajectory, honesty of inputs, horizon.
2. **State the outcome each party wants to be true.** Do this for every party, not only the payer (G7).
3. **Split the service into components by what each produces:** information, contested status, physical change, or a human act (architecture, section 2). This decides where agents, crews and people go (G5).
4. **Find where information is born and decisions are taken.** Put the capability there (G6). Delete the tasks and waits that exist only because of distance.
5. **Define the record and the authority to act** (G1, G12). Set the evidence rules (G8).
6. **Define what is sold:**
   - the conditions kept true, and the moments made fast (G4);
   - what is promised, and how it is backed (G13);
   - the money position (G2).
7. **Write the policy layers:** whose rules, whose overrides, and what needs a person (G3).
8. **Assign who produces each component, and where named people stand.** Size each group from exception rates and the review rule (G5).
9. **Name the parties and the principal, and design out the conflicts** (G7).
10. **Design for time** (G11), **for the client leaving and the firm failing** (G10), and **for the next generation of judges** (G9).
11. **Build the engine** (step 1) and the back office on it (section 6 below).
12. **Choose the boundary:** own the platform, build on one, be a portable layer, or contribute to a standard (section 7 below).
13. **Turn on whichever conditional elements apply** (C2 to C13).

---

## 2. The organisation

### 2.1 Five layers

| Layer | What it is | Who is in it | Permanent or scaffolding |
| --- | --- | --- | --- |
| **Governance** | Purpose, risk appetite, capital; the definition of good; conduct towards every party | Owners and board; accountable officers; the evaluation function (owners of test suites, thresholds and holdouts), which is independent of production and reports to the board; a conduct lead for the parties the firm does not serve | Permanent |
| **The agent architecture** | The firm's production system, on one shared record | Agents in positions: front door, production, counterparty agents, independent checkers, exception router, improvers, operations, commercial, governance and audit agents (step 3b). Each position has a named person who answers for it | Permanent, growing |
| **The boundary** | Where the firm meets what is not software | Named people for clients; the judgement desk; people for opposition and crisis; field crews and care workers where the product is physical or human (C13) | Permanent, sized by the service |
| **Builders** | Making and changing the engine | Platform engineers; domain engineers paired with experts, writing playbooks, checks and tests | Shrinks as agents author more, but never to zero [conjecture] |
| **The academy** | Growing the next generation of judges (G9) | Trainees on simulated and supervised cases; senior people who teach | Permanent |

### 2.2 How teams are cut

Teams are organised around the client's world: a segment of clients, a neighbourhood, a portfolio of homes. Capability teams own case types and engine components across them. That is a matrix, so the decision rights at the joins are written down:

| Decision | Who decides |
| --- | --- |
| What the client experiences, end to end | The client team, with one owner of everything the client sees |
| How a case type is done, and its playbook | The capability team |
| What counts as good, and every change to the tests | The evaluation function |
| Raising or lowering autonomy for a case type | The capability team proposes; evaluation approves |
| Promises, prices, capital | The board, on advice from pricing and risk |
| Anything that touches a party the firm does not serve | The conduct lead can veto |

The pod idea in step 3 survives as the pairing of experts and engineers inside capability teams. It no longer serves as the whole organisation.

### 2.3 Agents in the organisation

Agents hold positions on the organisation chart. Each position has:
- a role;
- a signed authority recorded in the record (G12);
- a budget;
- a named person who answers for it;
- a version, and a change log.

Positions are created, promoted, constrained and retired on evidence [seen in parts, Talentsconnect and Cars24, discovery sweep]. People are accountable; agents are not. The chart shows both.

### 2.4 How big each group is

There is no fixed ratio. Each group is sized from a measurable driver:

| Group | What drives its size |
| --- | --- |
| Judgement desk | Rate of exceptions needing judgement, by case type |
| Review and sign-off | The review rule regulators and insurers accept, sampling or every output, multiplied by volume |
| Named client people | Clients per person the relationship can bear. Seven designs used about one per 300 to 600 small clients, or embedded leads at 8 to 12 larger ones [conjecture] |
| Opposition and crisis | Rate of disputes, enquiries and crises |
| Field crews and care workers | Physical or human work hours, shaped by demand over the day and year (G11, C13) |
| Evaluation and builders | Number of case types and how fast they change, not client volume |

The single biggest unknown is the review rule. It decides headcount in every design, and no reasoning can settle it. Regulators and insurers have to be brought in early to settle it.

---

## 3. Organising principles for people and agents

Fifteen principles, each traceable to the architecture.

1. **The record is the truth, and work happens in it.** (G1)
2. **Act where the client's acts take effect.** (G2, G6)
3. **Policy before cases.** Agree the rules once; act within them; name every override. (G3)
4. **Sell conditions; make moments fast.** (G4)
5. **Promise only what you control, and back what you promise.** (G13)
6. **Agents produce information. People stand at judgement, accountability, opposition, crisis and consent.** Where people produce, agents give them time back. (G5)
7. **Name the principal, and never gain from anyone's loss.** (G7)
8. **The maker never checks itself; the improver never touches the test.** (engine)
9. **Autonomy is earned and reversible.** Lowering it is normal, not failure. (engine)
10. **Every exception is a lesson.** Classify it and fix the cause, not the case.
11. **Collect for a purpose, and tell people.** (G8)
12. **Design for the client being able to leave, and for the firm failing.** (G10)
13. **Grow judges on purpose.** (G9)
14. **Anyone, person or agent, can stop the line.** A named person responds, and false stops are counted.
15. **The burden of proof is on complexity.**

**For agents specifically:**
- Act only within recorded authority.
- Show sources and reasoning.
- Say "cannot assess" when you cannot.
- Escalate rather than guess.

---

## 4. Who needs to be "AI-pilled"

The question is about which roles need conviction and which need scepticism. Belief is a design choice by role [reasoned]:

| Who | What they need | Why |
| --- | --- | --- |
| **Founders and board** | Conviction that redesign beats automation, and patience for losses in the early years | Every design loses money at first, and the gains come from redesign that looks slow at the start |
| **Evaluation owners and senior experts** | AI fluency combined with professional scepticism | They define good and must catch what the agents get wrong |
| **Engineers** | Conviction and domain humility | They build the engine and must learn the work from the experts |
| **Boundary people** | Trust in the tools, and ownership of their judgement | People defer to machines unless the check is designed to prevent it (L014) |
| **Acquired staff** | Not belief: a clear role, fair pay, and a reason to teach the system | Conviction follows demonstration |
| **Clients** | Nothing | They buy an outcome, not a technology |
| **Regulators, insurers, counterparties** | Engagement as design partners | They set the review rule, accept records of authority, and provide interfaces |

---

## 5. The engine and the rhythm

The engine is set out in step 1 and under the core of the architecture. Its operating rhythm:

| When | What | Who |
| --- | --- | --- |
| **Continuous** | Cases flow; checks run; exceptions are routed; outcomes are captured | Agents, with boundary people |
| **Daily** | Exceptions reviewed by cause, and causes fixed | Capability teams |
| **Weekly** | Changes shipped and their measured effect; the main causes of exceptions; friction clients met | Capability teams, evaluation, platform |
| **Monthly** | Conditions met, errors found by audit, cost per condition, parties' outcomes, promises and claims against them | Client teams, evaluation, conduct, board committee |
| **On each model release** | Run the test suites; promote or hold each case type | Platform and evaluation |
| **Quarterly** | Scope, autonomy levels, promises and prices, capital, law-reform agenda | Board and accountable officers |

**Measures that show the firm is improving rather than just busy:**
- the share of the client's affairs handled as a side effect;
- touches per outcome;
- exception rate by cause;
- errors found by independent audit;
- time to adopt a new model safely;
- outcomes for parties the firm does not serve;
- the junior pipeline.

---

## 6. Back office and infrastructure

### 6.1 The back office is the engine's first client

The firm's own operations run as case types on its own engine from the first month. That gives a test bed with no client risk, and a working demonstration [reasoned].

| Function | How it runs |
| --- | --- |
| **Finance** | A continuous close on the firm's own ledger; revenue recognised per condition, per moment and per promise; the same design the accountancy firm sells |
| **Billing** | Driven by events: billed when a condition is met, a moment is completed or a promise period passes. No timesheets |
| **Treasury and capital** | Cash, any client money (only through regulated partners), credit advanced as principal (G2), capital and reinsurance behind promises (G13), with stress tests sized for a bad year |
| **Workforce and HR** | Recruitment, contracts, pay, rotas and skills for boundary people, crews and the academy (G9, C13), shaped to demand over time (G11) |
| **Compliance and assurance** | Evidence for regulators, insurers and auditors produced as a by-product of the record and the audit trail, not compiled by hand |
| **Legal and authority** | Mandates, policies and authority records (G3, G12); contracts with clients, partners and suppliers |
| **Procurement** | Compute, models, tools and data, managed as a budget line beside payroll [seen, LayerX and Cars24, sweep] |
| **Security** | Monitoring, separation of each client's data, incident response, limits on how far one change can spread |

### 6.2 The technology stack

| Layer | What it does | Build, rent or open |
| --- | --- | --- |
| **The record** | An add-only event store per client and per thing; the source of every entry; a protected advice layer where disputes are possible | **Build.** Where several parties rely on it, publish the schema as an open standard (C2) |
| **Authority and identity** | Signed mandates and policies; identity for agents and people; proof of authority others can carry and check | **Build** the authority model; **rent** identity rails |
| **Interfaces** | Client portal; an interface clients' agents can call; connectors to counterparties (banks, authorities, registries, insurers, contractors) | **Build** the client and agent interfaces; **rent or build** connectors as needed |
| **Agent runtime** | One orchestrator per case that alone writes to it; workers; routing across models | **Rent** the runtime; **build** the orchestration and case logic |
| **Tool gateway and permissions** | Every tool off by default, granted per position and per client; every action logged | **Rent or build**; this is now common practice [seen, ledger] |
| **Verification** | Deterministic checks; independent model checks on different providers; the interface experts use for sampling and review | **Build.** This is the core of the quality advantage |
| **Evaluation** | Test suites from real cases; holdouts the improvers never see; outcome capture | **Build.** This is the crown jewel |
| **Change pipeline** | Propose, test, release in stages, limit how many clients one change reaches, roll back | **Build** on rented tooling |
| **Model harness and routing** | Run the suites on each new model; route each task to the cheapest model that passes; fine-tune small models on the firm's own cases once volume allows [seen, Intercom, sweep] | **Rent** the models; **build** the harness |
| **Observability and audit** | Every decision traceable; evidence regulators and insurers can read | **Build** on rented tooling |
| **Pooled data** | Error, outcome and fraud data across clients, where lawful (C4) | **Build**, under strict rules on purpose |
| **Money rails** | Payments, wallets, client money, foreign exchange | **Rent** from regulated partners; never hold client money directly unless the law requires it (G2) |
| **Physical operations** | Dispatch, sensors and devices, crew scheduling, parts | **Rent** devices; **build** dispatch and scheduling where speed decides the outcome |

**What the infrastructure costs** [conjecture]:
- Compute and model spend rises from about 5–10% of payroll early on to 10–30% by the early 2030s, depending on landscape.
- The fixed costs are the record, verification, evaluation and the change pipeline. They scale with the number of case types, not the number of clients. That is the source of the scale advantage (step 1, P4).

### 6.3 Failure and safety

Lessons from the seven designs [reasoned]:
- **Limit the blast radius.** A playbook version serves a capped number of clients until proven.
- **Circuit breakers.** Automatic halts on exception rates, error rates and spend.
- **A kill switch for every agent position,** held by its named person.
- **Rehearsed rollback,** and a written plan for an error that has already reached thousands of clients.
- **Capital and insurance** sized for correlated loss.

---

## 7. The boundary choice

| Choice | When it fits | Examples |
| --- | --- | --- |
| **Own the platform** | The record has one owner; the firm needs scale it cannot reach alone; buyers of the platform are not rivals, or the platform is a separate company | Accountancy's two entities; Pennylane chose to be the platform and never sell the service [seen] |
| **Build on a platform** | A platform already holds the client's information at source, and the firm's edge is service, judgement and accountability | Firms on Pennylane or Xero [seen] |
| **Portable layer** | Large clients with their own systems and teams; information spread across many systems | Commercial legal for companies with their own general counsel; payroll over clients' HR systems |
| **Contribute to a neutral standard** | Many parties rely on the record or the rules; nobody would trust one firm to own it | Claims protocols given to a trade body; probate and the home record; home care's operating system as a neutral company |
| **Sell the definition of good** (C8) | Clients, peers or their AI can produce the work themselves | Licensed playbooks for in-house legal teams; payroll rule packs opened up |

A firm can combine these, but the conflicts between them must be stated. Selling the engine to rivals arms them. Owning the platform while also selling the service invites distrust from other firms.

---

## 8. Building it, 2027 to 2035

A generic sequence. Each service's own path is in its design.

| Period | What happens | What has to be true to move on |
| --- | --- | --- |
| **2027** | Pick one segment where the parameters favour the architecture. Build the record, authority and the first conditions with design-partner clients. Bring insurers and regulators in as design partners. Run the back office on the engine. Make one public promise | The promise is met for design partners, and the review rule is agreed for the first case types |
| **2028–2029** | Grow the wedge into conditions. Acquire clients through the cheapest route the parameters allow (table below). Begin backed promises with a capital partner. Open the academy | Cost per condition falling; errors found by audit stable or falling; the first promises paying out within their price |
| **2030–2032** | Add adjacent components and segments. Contribute to or found the standard. Possibly spin out the platform. Raise autonomy where it has been earned, and remove scaffolding | Scaffolding falling case type by case type; parties' outcomes holding |
| **2033–2035** | Choose the end form the parameters favour: operator, platform, engine supplier, assurer, or a specialist insurer that does the work | — |

### Ways to grow

| Route | When it fits | Example |
| --- | --- | --- |
| **Build only** | Clients buy at moments of change and switching is cheap | Legal for venture-backed companies |
| **Buy books of clients** | Incumbents are retiring; clients rarely switch; buying is effectively customer acquisition | Lettings, accountancy |
| **Buy firms** | Licences, local trust or crews are the scarce asset | Lettings in a dense region; customs and payroll entities |
| **Partner channels** | Someone else meets the client at the moment of need | Buy-to-let lenders (lettings), employers and pension schemes (probate), insurers (claims), councils and the NHS (home care) |
| **Host independents** | Professionals want their own practice but not the stack | A possible end form in several services [conjecture] |

### Stop rules

Each design sets hard gates. For example, lettings stops carrying risk if reactive repair spend has not fallen 10% by the end of 2028. The general rule: every promise and every autonomy level has a dated test, and a named decider who can stop it.

---

## 9. Where a first firm looks most promising, from the seven

This is judgement, not a ranking. All economics are conjecture.

| Service | For | Against |
| --- | --- | --- |
| **Cross-border payroll** | The architecture holds best (information, money, status; continuous; one principal). High margins in every landscape | Crowded (Deel, Remote, Rippling); labour-leasing law across Europe and Latin America; credit and entity risk |
| **Probate** (readiness in life) | High margins; a redesign incumbents cannot follow; paid by employers and banks | Depends on law reform and on banks relying on the firm's records of authority; slow to prove |
| **Accountancy** (sole traders and landlords entering Making Tax Digital first) | A dated wedge (Making Tax Digital); information born at the source; a platform option | Platforms such as Pennylane and Xero, and banks, are strong rivals; early losses |
| **Commercial legal** for venture-backed companies | Clear moments, fast switching, a proven builder model (Crosby) | Rivals and in-house AI; adversarial; fixed-price risk on scope |
| **Lettings** through regional book purchases | Roll-ups show the market buys; redesign beyond them is open | Physical crews and capital; thinner margins; Dwelly and others already moving |
| **Claims** | A large spend; prevention is a big idea | Buyers are large and slow; capital for restoration promises |
| **Home care** | Great social value; labour-short market | Thin margins; a payer who gains from less service; the workforce is the whole problem |

The parameters suggest the strongest first firms combine:
- one aligned principal;
- continuous service;
- a product that is information, money or status;
- data born at the source;
- a dated external push (a mandate or reform);
- fragmented incumbents.

---

## 10. Still to do

- **Retrofitting a messy incumbent** with many systems: what it takes to reach this design, and what to throw away.
- **Where to build or invest,** in detail, across the whole map of services rather than only these seven.
- **A blind test on a service none of the seven shaped:** statutory audit.
- **Putting the work into the library** as a draft synthesis, with your notes.
