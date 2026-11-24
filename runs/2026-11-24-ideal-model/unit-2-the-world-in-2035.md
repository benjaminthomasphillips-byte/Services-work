> Superseded on 24 November 2026: this was a first pass written without research or checking. Kept for the record.

# Unit 2. The world in 2035, and what it means for what we build in 2027

Draft by Claude, 24 November 2026. These are forecasts and inferences, stated sharply so they can be argued with. Each has a confidence level, a signpost to watch and a "so what" for the design. Library and discovery-sweep records are named where they prompted a point.

**The goal behind this unit.** Working in the world as it is today, what would we build, starting in 2027, to be the market leader in 2035? A design that merely survives 2035 is not enough. It has to be the firm that others in 2035 are measured against.

---

## A. Twelve calls about 2035

### 1. Codified professional work is nearly free, and much of it is given away inside other products.
Bookkeeping, payroll, routine tax returns, standard contracts, routine conveyancing steps, compliance checks and first-line claims handling cost a small fraction of today's price. Much of it is not bought from a firm at all. It comes bundled in the bank account, the accounting software, the payroll provider and, increasingly, the state: pre-filled tax returns, and digital-by-default registries.
- **Confidence:** high on direction, medium on how far.
- **Signpost:** HMRC pre-population under Making Tax Digital; banks and Xero or Intuit bundling "done for you" tiers; fee indices for small-business accounting.
- **So what:** never build where the end state is "free inside someone else's product". The work itself is a means to an end, not the thing sold. Where the work will be given away, the firm must either own the place it is given away, or sell what sits on top of it: the signature, the hard cases, the outcome.

### 2. The client is an agent.
By 2035 a large share of small firms and households buy services through their own AI agent. That agent compares offers, reads track records, negotiates and switches. Enterprises already move this way through procurement software (V007).
- **Confidence:** medium-high.
- **Signpost:** assistants that can transact; procurement agents in large buyers; protocols for agent-to-business commerce.
- **So what:** distribution changes from referrals and relationships to being the agent's default choice. That needs:
  - machine-readable offers and prices, with instant quotes;
  - a verifiable track record: outcome statistics an agent can check;
  - guarantees an agent can enforce.

  The firm sells to two audiences: the human, who trusts the brand, and the agent, which trusts the data. Firms that cannot be read by agents become invisible.

### 3. Counterparties are agents too, so volume explodes and the work becomes adversarial.
Claims against insurers, debt against debtors, tax authority against taxpayer, landlord against tenant: both sides run agents. Contacts, filings and disputes multiply ("agents fighting agents to stand still", Alloway; L012).
- **Confidence:** high.
- **Signpost:** volumes of complaints, claims and disputes rising faster than the underlying activity; institutions pricing or rationing machine-generated volume.
- **So what:** in adversarial markets the value is in being the better-armed side at scale, or in owning the settlement layer: arbitration, resolution and the rules. A firm sized for today's volume drowns. Design for ten times the volume of contacts per client.

### 4. Accountability becomes the product, and it needs a balance sheet.
When producing the work is cheap, what the client pays for is someone carrying the consequence. The licensed signature evolves.
- **Regulation shifts towards licensing systems.** Regulators move from licensing only individuals to certifying systems with a named responsible officer, as aviation certifies aircraft types and licenses pilots. The SRA authorising Garfield.Law (N065) and the RICS AI standard are early steps.
- **Services become warranties.** "We guarantee this return is right; if HMRC disagrees, we pay." That needs capital, insurance and actuarial data on your own error rates.
- **Confidence:** medium-high that accountability is the scarce good; medium on the regulatory route.
- **Signpost:** regulators authorising AI-based firms; professional-indemnity insurers pricing on system evidence; firms offering outcome guarantees.
- **So what:** the market leader carries risk others cannot. Build the error data, the verification evidence and the capital to warranty outcomes. Treat the insurer as a design partner from day one, and consider owning a captive insurer by the mid-2030s.

### 5. Firms split into many tiny ones and a few platforms; the middle is squeezed.
Two forms win:
- **Very small firms:** one or a few experts with agents. Kim and Koning find AI-native services start-ups about 70% smaller.
- **A few large platforms** that own the line, the licence, the insurance, the brand and the distribution.

The 50-to-500-person firm loses: too big to be personal, too small to own the stack. Choudary's "the unit of work shrinks" and Garicano's "expert work moves inside the client" both push this way.
- **Confidence:** medium-high.
- **Signpost:** small-firm formation in professions; the share of revenue going to the top ten firms; partner moves to "solo plus AI".
- **So what:** this is the least vanilla implication. The 2035 market leader may not be a big employer. It may be the platform that many small expert teams run on: its licence, its line, its insurance, its brand, its client flow. Estate agency already has this shape (eXp, Keller Williams), and Crosby's lawyers-plus-system model points the same way (N067). Design the firm to host independent experts as well as employ them.

### 6. Codified know-how stops being a moat; outcome data becomes the moat.
By 2035 general models know most of what is written down about tax, law and property management. A playbook that encodes public rules is worth little. What stays private is the data on what actually happened:
- which returns HMRC challenged and why;
- which claims paid;
- which repairs recurred;
- which clauses were litigated;
- the exceptions and their resolutions.

- **Confidence:** high.
- **Signpost:** open models matching specialist tools on public-rule tasks; vendors' advantage moving to proprietary outcome data. Intercom's fine-tuned open model saved about \$250k a month, a sign that firms train their own models on their own data.
- **So what:** design the firm to capture outcome-labelled data at scale. The corpus of cases with known outcomes is the crown jewel. This argues for volume early, for owning the client relationship long enough to see outcomes, and for training the firm's own models.

### 7. Services become maintained conditions, not jobs.
There is no year-end, only a ledger that is always closed. There is no annual compliance check, only continuous monitoring. There is no repair job, only a building held compliant, with a clock. The client subscribes to a state of affairs with a service level, not to tasks (A003: "a condition maintained continuously").
- **Confidence:** high in finance and compliance, medium in physical services.
- **Signpost:** real-time tax regimes; continuous-assurance audit pilots; statutory clocks such as Awaab's Law (N068).
- **So what:** whoever holds the client's live state holds the client. Design every product as an ongoing condition with a measurable service level, priced by subscription or by outcome.

### 8. Services and software converge, and the winner holds both the system of record and the licence.
In 2035 the distinction between "accounting software" and "accounting firm" is blurred. The software does the work, and the firm carries the liability. Whoever owns both wins. Banks, the software vendors and the AI labs are all moving towards it. The labs' own deployment companies are already here (N055).
- **Confidence:** medium-high.
- **Signpost:** software vendors acquiring or launching regulated service arms; banks offering bookkeeping and tax; labs buying services firms.
- **So what:** the competitor in 2035 is not another firm. It is Xero, Intuit, a neobank, or a lab-backed operator. The design has to answer "why doesn't Xero eat us?" There are three answers:
  - hold the liability and licence they don't want;
  - own the hard cases and the outcome data they can't get;
  - own the client relationship across several products, so the firm is the client's operating system rather than one app.

  The alternative is to be the regulated firm inside their distribution, as a partner.

### 9. The physical world is the last mile, and it is orchestrated rather than staffed.
Repairs, inspections, site visits and care stay physical. Robotics helps at the margin by 2035 but does not replace trades. The value is in owning the network of contractors, the scheduling, the clock and the quality data across thousands of jobs.
- **Confidence:** medium.
- **So what:** in coordination businesses, the moat is a network of trusted doers plus the data on their performance. That is a marketplace, not a firm.

### 10. Experts are scarce and expensive, and the junior route has broken across the industry.
Junior work went first (Furman, Catalini, Reuters on AT&T). By the early 2030s there is a shortage of people with real judgement. Gerlach's "knowledge trap" applies: firms that cut their experts see their models degrade without noticing.
- **Confidence:** high.
- **So what:** a firm that can make experts has a talent moat others lack. It trains juniors on simulated and real cases, teaching-hospital style, with AI used to explain rather than to do, as Shen and Tamkin advise. Design training as a product of the firm, not a cost.

### 11. Model capability is abundant and cheap; verification, data, distribution and capital are scarce.
Compute keeps getting cheaper per unit of capability. Garicano and Imas, in the sweep, argue progress is accelerating but each step costs more, with no "intelligence explosion" yet. Either way, a firm cannot win on model access. Every rival rents the same models.
- **Confidence:** high.
- **So what:** rent the intelligence, own the learning (Vikram Aditya in the sweep). Put engineering into verification, outcome data, workflow, distribution and the client's state, not into model research.

### 12. Regulation and public trust swing at least once.
Somewhere between 2027 and 2035 there is a scandal: an AI firm's correlated error hits thousands of clients at once, or an agent defrauds people at scale. Rules tighten after it.
- **Confidence:** high that it happens, low on when.
- **So what:**
  - Limit the blast radius by design: stagger releases and use canary cohorts.
  - Keep audit-grade records of every decision.
  - Be the firm regulators point to as doing it right. A firm that is already over-compliant when the swing comes takes share from those caught out.

---

## B. Two uncertainties that matter most, and a design that wins in all four corners

| | **Regulation stays permissive** | **Regulation tightens hard** |
| --- | --- | --- |
| **Capability races ahead** | Commodity work collapses fast; the winners own distribution, outcome data and capital. Speed matters most. | Licensed, insured, audit-grade firms capture the market; the unlicensed get shut out. |
| **Capability plateaus near 2027 levels plus** | The hard tail stays human for longer; operating discipline and the human-plus-agent line win. | Incumbents survive longer; the winners are those who already hold licences and clean records. |

The design that leads in all four corners:
- holds licences and is over-compliant;
- owns the client's state;
- builds outcome data and verification as its core asset;
- keeps real experts and makes new ones;
- has a line that improves automatically as models get better, without depending on them doing so.

---

## C. What this suggests we build: a first sketch to test in later units

**A licensed, insured platform for one domain of professional and compliance work.** It does four things:
- holds the live financial and compliance state of many small clients;
- sells maintained conditions with a warranty, rather than hours or jobs;
- runs the work on a compiled line that improves every week and with every model;
- hosts independent experts as well as employing them.

It grows mainly by moving clients onto its line. Its assets are its outcome data, its verification system, its licence and capital, its client relationships and its ability to make experts.

### Why buy books of clients, not companies

In 2027 the cheapest supply of trusted client relationships is the succession problem in small professional firms. Many owners are near retirement, have no successor and run firms that are worth little to anyone who wants to keep the old operation.

| | Buy the company | Buy the book of clients |
| --- | --- | --- |
| **What you pay for** | Clients plus staff, premises, systems, processes, culture, liabilities | Clients and the relationship, a handover from the owner, and the few people you actually want |
| **What you must then undo** | Everything about how the old firm works: the retrofit problem | Nothing; clients move onto your line from day one |
| **How the price is set** | A profit multiple, which capitalises the old cost base | Price per client or a share of fees, which is effectively a customer-acquisition cost |
| **Risk** | Integration, key people, inherited liabilities | Client attrition at handover |

So an acquisition becomes a way of acquiring customers, not a way of acquiring operations. A licence-holding entity may still have to be bought in some regimes, but as a shell rather than an operation. The comparison to make is cost per client acquired this way against acquired through agents, software partners or marketing. This is developed in the build-path unit.

### The questions the sketch has to survive

- Why don't Xero, Intuit or a bank do this themselves?
- Does a platform hosting independent experts keep quality and liability under control?
- Can a new firm get licences and insurance on terms that allow warranties?
- What happens to the design if capability stalls?

---

## D. Revised plan of units

1. Foundations (done)
2. The world in 2035 (this unit)
3. The end state: the market-leading firm in 2035, the whole organisation on a page, and what it sells, owns and is
4. The work system: the task contract, autonomy levels, verification, how a case flows
5. The self-improving firm, and what happens as it compounds
6. People, agents, organisation and principles
7. **Back office and infrastructure (new).**
   - The firm's own back office, run as its first client.
   - The technology stack and data architecture.
   - Model strategy (rent, fine-tune, route) and compute economics.
   - Identity, permissions and audit; security.
   - Evidence that regulators and insurers can read.
   - Whether to sell the back office to others as a product.
8. The commercial model, moats and distribution when clients are agents
9. The build path from 2027 to 2035, year by year: founding team, licences and insurance, buying books, milestones and capital
10. Retrofitting a messy incumbent: what it takes to get from many systems and tacit know-how to the end state
11. Variation by type of business, and where to build or invest
