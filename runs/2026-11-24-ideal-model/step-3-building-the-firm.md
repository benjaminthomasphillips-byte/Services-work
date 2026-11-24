# Step 3. Building an AI-native services firm for 2035: a base design, the choices that shape it, and possibilities to explore

Revised 24 November 2026, after a panel review and Ben's steer.

## How this was made, and the stance

This is an exploration, not a plan. It has three parts:

- **A base design.** The parts of the firm that hold whatever strategic choices are made.
- **The main choices.** For each, the options and how the base design flexes. These are for Ben and me to pick together.
- **Bolder possibilities.** Explored as thought experiments, including ones the review panel raised.

Constraints such as regulation, insurance and courts come later, as a stress test. They are not a starting limit: designing to today's rules first narrows the space before it has been explored.

Labels:
- **[seen]** exists somewhere today, cited where useful;
- **[reasoned]** follows from logic;
- **[conjecture]** a plausible extension towards 2035.

The panel's reviews are kept in `panel-review-*.md` and `panel-synthesis-step3.md`. The first draft is `step-3-building-the-firm-draft.md`.

---

## 1. Four landscapes for 2035

These are not predictions. The design is tested against all four.

| Landscape | What it looks like | What the firm needs to be |
| --- | --- | --- |
| **A. Capability keeps compounding** | Agents do most cognitive work end to end; people for judgement, accountability and relationships | A firm whose engine absorbs each model and whose client base grows far faster than its headcount |
| **B. Capability plateaus** | Excellent assistants, unreliable alone on multi-step judgement | A firm that still wins decisively on workflow, experience and quality with modest autonomy |
| **C. Markets run through agents** | Clients and counterparties act through their own agents | A firm machines can read and call, with published service levels and verifiable outcomes |
| **D. Prices collapse** | Routine work is so cheap that volume rises and revenue falls; clients' own agents plus a hired signature do much of it | A firm that has moved its revenue to what stays scarce before the collapse arrives |

**Who the rivals are in each:**
- in A and C: AI labs, software platforms and clients' own agents;
- in B: well-funded roll-ups and incumbents that adopt quickly;
- in D: all of them.

The sleepy incumbent is not the main rival in any landscape.

---

## 2. The base design: what holds whatever is chosen

### 2.1 The promise
One public promise that incumbents cannot match without rebuilding themselves. For example: "returned in four hours, fixed price, every change explained"; "your books closed every day"; "every compliance date met, live status". It is the specification, the marketing and the quality bar at once. A founder on the panel said, from experience, "our promise became the backlog".

### 2.2 The client experience is the product
Speed, clear prices, live status, the firm raising issues before the client asks, explanation in plain words, and one interface that both people and clients' agents can use. It is improved weekly with real clients, as a product company would.

### 2.3 Experts and engineers build together
The firm's core skill is pairing people with professional judgement and engineers with craft, every day, so that judgement becomes part of the engine.

### 2.4 Teams
Small teams own work end to end. The base design leaves open what a team is organised around; section 3, choice 3 covers it. Two rules hold either way:
- **Design to the expert's span of attention.** A team splits when its accountable expert is saturated, not when its headcount grows. Garicano's knowledge hierarchy applies: routine work at the base, exceptions rising to people who can solve them [reasoned].
- **Someone owns what the client sees across teams,** so one client gets one coherent experience even when several teams serve them [reasoned].

### 2.5 Agents are members of the organisation, each with an accountable person
Agents appear on the organisation chart with roles, identities, permissions, budgets and records. Each has a named person who answers for it, as a team lead answers for a team. Agents are onboarded, have their authority raised or lowered on evidence, and are retired [seen at Talentsconnect, sweep; reasoned]. Token spend is a budget line next to payroll [seen at Cars24 and LayerX, sweep].

### 2.6 Apprentices instead of a pyramid
New people learn on simulated cases and supervised live cases, using AI to explain rather than to do. The pyramid is replaced by a ladder of judgement [reasoned].

### 2.7 A small centre
- A platform team owns the shared engine.
- An independent quality function owns the definition of good, the holdout cases and audits, and reports to the board.
- Talent and training.
- Commercial.

### 2.8 The engine
Covered in step 1:
- every case typed and routed;
- a task contract per case type, used as a ladder;
- checks independent of the maker;
- test suites from real cases;
- outcomes captured;
- a change pipeline;
- a model-upgrade harness;
- people own the evaluator.

### 2.9 Autonomy is a dial for each case type
Raised on evidence, lowered after a failure, without stigma. Ratios of people to agents follow it.

### 2.10 Rent the intelligence, own the learning
Use frontier models through one layer that can switch between them. Build the case system, playbooks, test suites, review interface, client interface and change pipeline.

### 2.11 The back office is the engine's first client
Finance, billing, HR administration and compliance run on the engine from the first month.

### 2.12 How it runs and what it believes, briefly
- **Exception debt.** Exceptions are reviewed and their causes fixed daily, and the firm aims to carry no unexamined exceptions.
- **The engine review.** Weekly: changes shipped and their measured effect.
- **Stopping the line.** Anyone can do it. A named person responds, and false stops are counted, so stopping is used and not abused.
- **Paying for the work.** Nobody is paid on volume they also check.
- **Adding complexity.** Anyone adding a process or a layer has to show why it is needed.

---

## 3. The main choices, and how the base flexes

Each choice has several options. None is chosen here. For each option, the table says what it does to the organisation.

### Choice 1. How the firm earns

| Option | What the client pays for | What it does to the organisation |
| --- | --- | --- |
| **Fixed price per item** | A defined output | The engine must control scope; a function prices the work and catches matters that balloon. A founder on the panel notes that the 8–10% of matters that turn into three matters drive the margin |
| **Subscription to a maintained condition** | A state kept true: books closed, compliance met | Teams are organised around continuous service; the engine monitors rather than responds; revenue is recurring |
| **A share of the outcome** | Recovered money, savings, wins | The engine must predict outcomes in order to choose cases; the firm needs working capital |
| **A guarantee** | The result plus taking on the consequence if it is wrong | The quality function becomes a pricing function too; the firm needs capital and an insurance partner; it starts to resemble a specialist insurer that does the work (section 4a) |
| **Selling the engine** | Software and support to other firms | A product and support organisation; conflicts with competing against those firms |
| **Assurance over clients' own agents** | The firm checks and signs work the client's AI did | The engine is pointed at other people's outputs; the expertise is audit and sign-off (section 4b) |

These can be combined. A plausible path starts with fixed price or subscription and adds others as data and capital build.

### Choice 2. How it reaches clients

| Option | What it does to the organisation |
| --- | --- |
| **Direct, on its brand** | Marketing, sales and a brand function; acquisition cost is the main economic issue |
| **Embedded in someone else's channel:** banks, payroll and accounting software, marketplaces | Partnership and integration teams; the partner owns the relationship; volume is faster, margin thinner |
| **Through clients' agents** | Interface-first: the portal is the interface's first user; published service levels and outcomes; legibility to machines is the main investment |
| **Through other firms** | The firm as a supplier to other professionals; an account-management organisation |

### Choice 3. What teams are organised around

| Option | Strength | Weakness |
| --- | --- | --- |
| **Type of work** | Deep expertise, clean engine ownership | A client with several needs meets several teams |
| **Client segment** | One face to the client, cross-selling | Expertise and engine ownership spread thinner |
| **A matrix:** segment teams own clients, and capabilities by type of work own the engine | Both strengths | Needs clear decision rights at the joins |

### Choice 4. How it grows

| Option | What it does to the organisation |
| --- | --- |
| **Build only** | Slow, clean, one culture; acquisition cost is the constraint |
| **Build, then buy books of clients** | An integration function that moves clients onto the engine, treating integration itself as a case type; pricing books as customer acquisition |
| **Buy firms** | Larger integration and change capability; inherited culture and systems (step 7 covers the retrofit) |
| **Host independent professionals** | A platform organisation: onboarding, quality standards, revenue share; the firm owns the engine, brand and client flow, and the professionals own their clients or share them |

### Choice 5. Legal and ownership form

| Option | What it allows |
| --- | --- |
| **One licensed firm with outside capital,** where rules permit | Simple; the full model in one entity |
| **A holding company with licensed operating firms and a technology company** | Separates capital, licence and engine; allows several licences and countries |
| **A platform company with independent licensed members** | The federated form; members own their practices |
| **A professional-owned firm with a services company supplying it** | Where outside ownership of the licensed firm is restricted |

### Choice 6. The end form by 2035

- **A large operator:** many teams, few people per client, a strong brand.
- **A platform:** hosting independent experts on its engine, licence and client flow.
- **An engine supplier:** to other firms.
- **An assurer:** checking and signing others' AI-made work.
- **A specialist insurer that does the work.**
- **Combinations,** with the conflicts between them stated.

The panel argued this should be settled early because ownership and capital lock it in. The counter-argument is that the right end form depends on which landscape arrives. The compromise is to choose a primary end form early and keep the one or two options compatible with it open. That pick is for later.

---

## 4. Bolder possibilities to explore

Each is a thought experiment [conjecture], with what it would mean for the organisation.

### 4a. The firm that guarantees its work
The firm sells a result and carries the consequence. "If this filing is rejected, we fix it and pay the penalty." The engine's error data prices the guarantee. Quality becomes underwriting. Capital and an insurance partner become core.
- **By 2035:** it may look like a specialist insurer whose claims are low because it also controls the work.
- **Organisation:** an actuarial and pricing function next to quality, and a capital plan.
- **Where it fits best:** short-tail, fast-checking work the firm fully controls. Lettings compliance is an example; long-tail tax positions are not (practitioner reviews).

### 4b. Assurance over other people's agents
If clients' own agents do most routine work by the 2030s, the scarce thing is someone credible to check it, sign it and stand behind it. The firm audits and certifies work it did not do.
- **Organisation:** mostly experts and evaluation engineers, with deep test suites across many clients' systems.
- **Why it matters:** it turns the threat of in-house AI into the market.

### 4c. The firm with almost no headcount
Take landscape A to its limit: twenty people serving a hundred thousand clients. Almost all of them are accountable experts, evaluator owners and engine engineers. Every client interaction is agent-to-agent or agent-to-person, and people appear only for judgement and crisis.
- **The question it raises:** what is the firm's brand, if clients rarely meet a person? And what stops a rival doing the same with the same models? The answers in step 1 are evaluation at scale, outcome data and trust.

### 4d. The platform that hosts independents
Professionals run their own practices on the firm's engine, brand and licence framework. The firm earns a share and sets the quality bar. Estate agency already has hybrid platforms of self-employed agents [seen, practitioner review].
- **Organisation:** a platform, a standards body and a training academy rather than a firm of employees.
- **Upside:** it scales through other people's ambition.
- **Risk:** quality and accountability across independent members.

### 4e. The firm that trains the profession
The firm's simulation library and supervised-case programme become the best route to becoming a qualified professional once junior work has gone elsewhere. It trains its own people and licenses the programme to others.
- **Why it matters:** whoever trains the next generation of signatories controls the scarcest input of the 2030s.

### 4f. The firm that writes the standard
The firm publishes its quality standards, test suites and audit methods, and works with regulators and insurers until they become the reference. It shapes the market's rules instead of complying with them.
- **Upside:** credibility, and an advantage for whoever already meets the standard.
- **Cost:** some exposure of method to rivals and to counterparties' agents probing it.

### 4g. The agent-native firm
Built for landscape C from the start. The primary interface is for clients' agents. Prices, capacity, service levels and outcomes are published in machine-readable form, and the firm competes to be the default choice of the agents that buy.
- **Organisation:** interface and data engineering are central; brand matters for the humans who set their agents' preferences.

### 4h. The firm built for price collapse
Assume routine prices fall towards zero by the early 2030s. The firm gives the routine work away, or sells it at cost, to own the client's live records and the relationship. It earns on what stays scarce: judgement, accountability, coordination of other parties, and crisis support.
- **Organisation:** the routine engine is a cost centre and a source of data; the profit centres are the expert teams.

---

## 5. Target numbers, to argue with

These are design targets, not forecasts [conjecture]. They show what "AI-native" would have to mean in numbers for the design to be worth building.

| Measure | 2028 | 2030 | 2035, landscape A | 2035, landscape B |
| --- | --- | --- | --- | --- |
| Cases closed with no human touch (routine types) | 10–30% | 30–60% | 80–95% | 40–60% |
| Clients per accountable expert, relative to a traditional firm | 2–3× | 5× | 20×+ | 5–8× |
| Expert minutes per routine case, relative to 2027 | 0.7× | 0.4× | 0.1× | 0.4× |
| Token and compute spend as a share of payroll | 5–10% | 10–20% | 30%+ | 10–20% |
| Time to adopt a new model safely | Weeks | Days | Days | Days |

If, by 2030, the firm is near the bottom of these ranges, it is a better traditional firm, not an AI-native one.

---

## 6. Choices to make together

From section 3, in the order they most shape everything else:

1. **How the firm earns.** Which one or two options to design around first.
2. **How it reaches clients.**
3. **How it grows:** build, build then buy, buy, or host.
4. **The primary end form,** and which others to keep open.
5. **Which bolder possibilities from section 4** to develop properly.
6. **Which one or two types of service** to use as worked examples, so the base design can be shown in detail.

---

## 7. Where this is weakest

- **The base design is reasoned from parts seen mainly in software and product companies.** No services firm has yet run all of it.
- **Winning on experience assumes clients will move for it.** Reviewers who see switching costs and inertia doubt it outside moments of change.
- **The target numbers are conjecture** and could be far off in either direction.
- **The bolder possibilities are unevaluated.** Some will not survive contact with economics or with the rules once those are applied as a stress test.
