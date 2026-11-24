# Step 3. How we would build an AI-native services firm, starting in 2027 and built for 2035

Draft, 24 November 2026, before review.

## How this was made

This is a design, reasoned forward from today's tools and from what is likely to come. Evidence is used where it exists and is otherwise not required. Every substantive claim carries one of three labels:

- **[seen]** Something already done somewhere today. The library or the discovery sweep is cited where relevant. Most of these are firms' own accounts.
- **[reasoned]** Follows from logic and from how things work.
- **[conjecture]** A plausible extension to 2035. Held because a firm designed this way is better placed if it comes true, and not much worse off if it does not.

The design does not assume a particular service. Examples are drawn from law, accountancy, property and insurance. Where a choice depends on the type of service, it says so, and the later step on variation takes it up.

---

## The answer in brief

Build the firm as a product company that delivers professional work. That means a narrow wedge first, a client experience far better than the incumbents', small senior teams of experts and engineers working together, and agents as part of the workforce. It also means an engine that improves the work every week. The whole design is built so that it gets better on its own as models improve, still wins if they stall, and is easy for clients' agents to read once those agents arrive.

Ten design choices carry the weight:

1. **Win on experience, not price.** The opening move is to be remarkably better for one kind of client: hours instead of weeks, a fixed price instead of a meter, live status instead of chasing, and the firm raising problems before the client has to. Cost advantage follows; it does not lead. (Crosby's speed and per-document pricing [seen, N067]; Linear's quality-as-strategy, applied to services [reasoned])
2. **The pod is the unit.** A pod is a licensed expert, an engineer and a fleet of agents. It owns a type of work end to end, from the client's request to the signed result and the improvements that follow. It is not a department.
3. **Experts and engineers build together, every day.** The expert's judgement goes into the engine through the engineer's craft. Neither can do it alone. This pairing is the core skill of the firm.
4. **No classic juniors; apprentices instead.** New people learn on simulated and supervised live cases. They are taught to use AI to explain, not to do the work for them. The pyramid is replaced by a ladder of judgement.
5. **The engine is shared; the pods are close to clients.** One platform holds case handling, playbooks, checks, test suites and the model harness. Pods build on it and improve it.
6. **Low context, high writing.** Decisions, playbooks and client status are written down, so any person or agent can pick up a case without asking. Coordination runs through shared state, not meetings.
7. **Agents are staff, with identities, roles, budgets and owners.** They sit on the organisation chart, are onboarded and reviewed, and are retired when they are replaced.
8. **Quality is designed into the work, then audited independently.** Every case passes checks built into the line. A separate quality function, which does not report to the pods, samples the work and owns the definition of good.
9. **Rent the intelligence; own the learning.** Use frontier models through a layer that can switch between them. Build only what compounds: the case system, the playbooks, the test suites, the review interface, and the client experience.
10. **Keep the shape adaptive.** Ratios of people to agents, the level of autonomy each task has earned and pod size are dials. The firm turns them as capability moves, case type by case type.

---

## 1. Three landscapes for 2035, and what the design must do in each

These are not predictions. They span what is plausible, so the design can be tested against each.

| Landscape | What it looks like | What the firm must be |
| --- | --- | --- |
| **A. Capability keeps compounding** | By the early 2030s agents do most cognitive work end to end, reliably, across long tasks. People are needed for accountability, hard judgement and relationships [conjecture] | A firm whose engine absorbs each new model and moves work up the autonomy ladder quickly, so that its headcount barely grows while its client base does |
| **B. Capability plateaus** | Models are excellent assistants, but unreliable when left alone on multi-step judgement. People stay in most loops [conjecture] | A firm whose human-plus-agent workflow, client experience and quality still beat incumbents decisively, even with modest autonomy |
| **C. Markets run through agents** | Clients and counterparties act through their own agents. Offers, prices, status and track records are read by machines [conjecture] | A firm that is legible to machines: an interface agents can call, published service levels, verifiable outcomes |

The design below is meant to win in all three. Where a choice only pays off in one, it is marked.

---

## 2. The first two years: wedge, team and promise

### Choosing the wedge [reasoned]

Pick one type of work for one kind of client. It should meet as many of these as possible:

- **The client hates the incumbent experience:** slow, opaque, billed by the hour, hard to reach. That pain is the opening.
- **The work recurs often**, so the engine gets many cases to learn from.
- **Inputs are mostly digital**, or can be made so.
- **Experts are needed, but much of the work follows patterns.** Most cases are variations on known types.
- **Outcomes can be checked fairly soon:** a filing accepted, a contract signed, a repair completed.
- **The clients are growing fast** and will expand with the firm. Crosby chose fast-growing companies [seen].
- **There is a natural way to expand** into adjacent work for the same clients.

The wedge is deliberately narrower than the firm's ambition. Crosby started with contract work for fast-growing companies, not "law" [seen]. Garfield started with debt chasing under £10,000, not "litigation" [seen, N065].

### The founding team [reasoned]

- **One or two licensed experts** with judgement and a reputation in the wedge. They are also the first evaluator owners: they decide what good looks like.
- **Two or three product engineers** who can build agent workflows, interfaces and test suites, and who will sit with the experts daily.
- **One person who owns the client experience** end to end: the promise, the interface, onboarding and communication. In a product company this is the designer and product lead combined.
- **No separate managers.** Founders do it.

The team is small and senior. Kim and Koning find AI-native start-ups markedly smaller and flatter, because the work moves into the product [seen, sweep]. Talent density matters more than headcount [reasoned].

### The promise [reasoned]

Make one public promise that incumbents cannot match without rebuilding themselves. For example:

- "Reviewed and returned within four working hours, fixed price, with every change explained."
- "Your books closed every day, not every year."
- "Every compliance date for your building tracked and met, with live status."

The promise does three jobs. It defines what the engine has to deliver, it is the marketing, and it is the quality bar.

### What exists in 2027 and what to build

| Available to rent or buy in 2027 [seen] | Build, because it is where the advantage compounds [reasoned] |
| --- | --- |
| Frontier models; agent runtimes; tool gateways with permissions; workflow tools; document and e-signature tools; payments; cloud systems of record (ledgers, practice management) | The case system (intake, typing, routing, status); the playbook library; the test suites and verifiers; the review interface experts use; the client interface (portal, and an API for clients' agents); the change pipeline; the model-upgrade harness |

---

## 3. The organisation

### The pod [reasoned; seen in parts]

A pod owns one type of work for one kind of client, end to end.

| Member | Does | Does not |
| --- | --- | --- |
| **Principal** (licensed expert) | Judgement on hard cases, sign-off, owning the definition of good, client relationship at the senior level, teaching the system | Routine production |
| **Engineer** | Builds and improves the workflow, tools, checks and test suites, with the principal | Sign-off or client advice |
| **Client lead** (where the work warrants one) | Scoping, onboarding, communication, expansion | Production |
| **Apprentices** | Supervised live cases, simulated cases, the exception desk | Unsupervised sign-off |
| **Agents** | Intake, drafting, research, checking, chasing, status updates, first-line client questions | Anything outside their authority |

Some parts of this are already seen elsewhere:

- Intercom pairs a forward-deployed engineer with a data scientist who proves the value, in what it calls swarms [seen, sweep].
- Mercari found one-person "AI pods" hit a quality ceiling [seen, sweep], which argues for at least the expert-plus-engineer pair.
- Lexware is moving to two-person teams, and FINN abolished the software-engineer title for small cross-functional teams [seen, sweep].

**How pods grow [conjecture].** In landscape A, a pod's client base grows tenfold or more between 2027 and 2035 with little added headcount, because tasks climb the autonomy ladder. In landscape B, pods add apprentices and exception handlers as volume grows. The pod's design is the same in both; only the ratio changes.

### The centre

- **Platform.** A small engineering team owns the shared engine: case system, gateways, test-suite tooling, model routing, cost control and security. Pods are its customers.
- **Quality and assurance.** Independent of the pods. It holds the test suites' holdout cases, samples live work, investigates errors and runs the audit trail that regulators and insurers read. It reports to the board, not to the person who runs the pods. This is the separation of powers from step 1 made into an organisation [reasoned].
- **Talent and training.** Recruits experts, runs the apprentice programme and the simulation library, and keeps evaluator owners doing live work so they do not lose their feel [reasoned].
- **Commercial.** Brand, pricing, partnerships, and the interface that clients' agents call [conjecture for the agent interface].
- **Back office.** Run on the firm's own agents from day one, so the back office is the engine's first client: finance, billing, HR administration, compliance records.

### Who the firm hires [reasoned]

- **Experts with taste and a teaching instinct,** not the fastest producers. Their job is to define good and encode it.
- **Engineers who like messy domains** and sit with clients and experts.
- **High-agency generalists** over narrow specialists in non-expert roles. Bird cut from more than 1,000 people to 120 and kept generalists of this kind [seen, sweep].
- **A deliberate share of experienced people released from squeezed mid-sized firms** between 2027 and 2031 [reasoned, from step 2].

### Pay and ownership [reasoned]

- Experts are paid for defining and improving the work as well as for signing it. A "contribution" component credits playbooks, tests and exception resolutions that others reuse. It is judged by peers and by the quality function, not by usage counts, which can be gamed.
- Broad equity, because the scarce goods are held by individuals (step 2, Q8).
- Nobody is paid on volume they also check.
- Chen Chunhua's cases pay people for making the team smarter rather than for individual targets [seen, sweep].

### How decisions get made [reasoned; seen in parts]

- **Written by default.** Alan makes decisions in writing, challenged by standing agent "voices" for members, data, legal and customers [seen, N074]. Mercari's former CTO argues for low-context organisations [seen, sweep].
- **Burden of proof on complexity.** Anyone adding a process, a layer or a meeting must justify it, as at Bending Spoons [seen, sweep].
- **Pods decide inside their type of work.** The centre decides on the platform, quality standards, pricing frameworks, and anything that crosses pods.
- **Anyone can stop the line.** A person or an agent that sees an abnormality halts the case type, as in Toyota's andon [reasoned; Jansen's application to agents, sweep].

### Agents as members of the organisation [seen in parts; reasoned]

- Each agent has a role, an identity, permissions, a budget, an owner and a performance record. Talentsconnect onboards agents onto its organisation chart and retires them [seen, sweep].
- Agents report status into the shared record, and that record replaces most status meetings. Block describes a company "world model" doing work middle management did [seen, sweep].
- Token spend is managed as a budget line next to payroll. Cars24 reports token spend at 8.88% of its salary bill, and LayerX manages "token economics" [seen, sweep].
- Agents with authority are distinct from agents that only advise. Authority is earned by record on each case type (step 1's ladder).

---

## 4. The client experience is the product

[reasoned; Linear's lens applied to services]

| Element | Incumbent norm | The firm's design |
| --- | --- | --- |
| Speed | Days to weeks | Hours for routine work; a stated time for everything |
| Price | Hourly, estimated | Fixed per item, or a subscription to a maintained condition |
| Status | Phone and chase | Live status, readable by the client and the client's agent |
| Initiative | Reactive | Proactive: the firm raises issues and deadlines first |
| Explanation | Opaque | Every output explained in plain words, with the reasoning available |
| Access | Office hours, through a person | Always-on for routine questions; a named expert for judgement |
| Interface | Email and attachments | A portal, plus an API for clients' agents [conjecture on timing] |
| Quality | Implicit, trust the brand | Stated standards; published service levels and outcome statistics where meaningful |

The design is built with clients in a weekly loop. Pods watch real clients use the service, fix friction and ship improvements. This is how a product company works, and few professional firms do it.

---

## 5. The engine inside the firm

Step 1 holds the design. In short:

- every case typed and routed;
- a task contract per case type, used as a ladder;
- checks independent of the maker;
- test suites from real cases;
- outcomes captured;
- a change pipeline;
- a model-upgrade harness;
- people own the evaluator.

How it fits the organisation:

| Engine component | Organisational owner |
| --- | --- |
| Playbooks and workflows | Pods |
| Test suites, holdouts and the definition of good | Quality and assurance, with the pod's principal |
| Platform, gateways, model harness | Platform team |
| Prioritising improvements | Each pod, with a weekly review |

---

## 6. The operating rhythm

[reasoned; seen in parts]

| Cadence | What happens | Who |
| --- | --- | --- |
| **Daily** | Exception review: what the engine could not handle, by cause. Each person improves their own work for a short fixed time, as Qonto does with 30 to 60 minutes a day [seen, sweep] | Each pod |
| **Weekly** | Engine review: changes shipped, their measured effect, the main exception causes, client friction seen | Each pod; platform joins |
| **Monthly** | Outcomes and economics per case type: service levels met, errors found by audit, cost per case, client retention | Pods, quality, founders |
| **Quarterly** | Scope: which case types to take on next, which model upgrades to adopt, which autonomy levels to raise or lower | Founders and pod principals |
| **On any model release** | Run the test suites on the new model; promote or hold, case type by case type | Platform and quality |

There are few standing meetings. Status comes from the shared record [reasoned]. Anthropic's own data shows meetings rising as agent work grows [seen, ledger], so the design treats coordination time as a cost to watch, not a given.

---

## 7. Principles for people and agents

**For everyone:**

1. The client's experience is the product.
2. Work happens in the system, or it did not happen.
3. Write it down: decisions, reasons, status.
4. Anyone can stop the line.
5. The maker never checks its own work.
6. Every exception is a lesson. Classify it, then fix the cause.
7. Earn autonomy with evidence, task by task. Lowering autonomy after a failure is normal, not a disgrace.
8. Add complexity only with proof that it is needed.

**For people:**

9. Spend your time on judgement, relationships and teaching the system.
10. Keep doing some live work, so your judgement stays sharp.

**For agents:**

11. Act only within your authority. When unsure, escalate rather than guess.
12. Show your sources and reasoning. Say "cannot assess" when you cannot. LayerX's design harness requires this [seen, sweep].
13. Never touch the tests you are judged by.

---

## 8. Technology and back office, in outline

The full unit comes later. The decisions that matter for the organisation [reasoned]:

- **Models:** rent from several providers through one layer that can switch between them. Fine-tune smaller models on the firm's own cases once volume allows, mainly for cost; Intercom's fine-tuned open model is an example [seen, sweep].
- **Build:** the case system, playbooks, test suites, review interface, client interface, change pipeline and model harness.
- **Buy:** systems of record clients already use, payments, identity, document handling.
- **Security and permissions:** a gateway with tools off by default, every agent action logged, and data separated by client [seen as convergent practice, ledger].
- **Back office:** the firm's own finance, billing, HR administration and compliance run as case types on the engine from the first month. That gives a test bed with no client risk, and a working demonstration.

---

## 9. From 2027 to 2035: how the firm grows

Options, not a plan. The later step on growth develops them.

1. **2027–2028: the wedge.** One pod, one type of work, design-partner clients, the promise met, the engine running gated by people.
2. **2028–2030: adjacent work.** More pods on the same clients' neighbouring needs, sharing the platform. Possibly buy books of clients from retiring owners to speed up volume, moving them straight onto the system [reasoned].
3. **2030–2033: new segments or geographies.** The engine is proven. Pods replicate. Autonomy rises where it has been earned.
4. **2033–2035: choose the end form.** By then the firm knows which landscape it is in [conjecture]:
   - **A large operator** with many pods, few people per client and a strong brand.
   - **A platform** hosting independent experts on its engine, licence and client flow.
   - **A supplier of the engine** to other firms.
   - **A combination** of these.

---

## 10. Where this is weakest

- **The pod design is reasoned from parts seen in software and product companies,** not from a services firm that has run it at scale.
- **Experts may not want to teach a system that reduces the need for experts.** The pay and ownership design is the answer offered, and it is untested.
- **Winning on experience assumes clients switch for experience.** In some markets inertia and relationships dominate (step 2), and the wedge has to be chosen where they do not.
- **Landscape A could arrive fast enough to make the expert-engineer pairing temporary,** and landscape B could last long enough to make the engine's promised gains small. The design is meant to survive both, but its economics differ greatly between them.
- **Regulation and insurance** for agents with authority over client work are unresolved, and could cap autonomy in regulated work (practitioner reviews).
