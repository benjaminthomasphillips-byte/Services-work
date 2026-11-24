# Level 3: commercial legal services for growing UK companies, redesigned from scratch, as a test of the architecture

Draft by Claude, 24 November 2026. Revised the same day after two reviews: a builder pushing it further (`level3-legal-review-builder.md`, a co-founder of an AI-native firm) and a practitioner testing it against reality (`level3-legal-review-practitioner.md`, the general counsel of a 300-person scale-up). One author, no sub-agents. It follows the six-step procedure in `step-3c-the-electricity-test.md` and the kinds of human need in `step-3b-the-agent-enterprise.md`, uses the accountancy and lettings redesigns only for their pattern, and draws on the law partner's counter-review where noted. Labels: **[seen]** exists somewhere today, with its source; **[reasoned]** follows from logic; **[conjecture]** plausible towards 2035. Every volume, price and headcount is a model figure for argument. Today's rules are facts to design around, applied in full in section 10. The last section, "Review and response", lists every review point and what was done with it.

**What changed in revision.** The practitioner's main charge is right: the first draft put the gate on the signature, but most commitments are never signed in an e-signature tool. They are accepted in portals, agreed on calls and sent in late-night side letters. The builder's main charge is also right: the draft sold readiness as a project, kept a law firm's org chart under new names, and still thought in documents. This version moves the firm from the signature to every **commitment point**, makes **the client's policy** (not the document) the unit of work, treats **the record as a liability** as well as an asset, turns the **counterparty into the growth channel**, redesigns **the round from the investors' side**, enters through **one stuck contract and one forced change**, organises the firm into **flow pods**, prices **per commitment**, and narrows two products (supervision and the certificate) that would not survive an insurer. Four verdicts move: [element] from breaks to bends; [element] and [element] from holds to bends; [element] stays bends with a smaller downside.

---

## The answer in brief

1. **Legal work exists because of a gap between when a company commits and when anyone checks what it committed to.** Founders, sales directors and managers commit every day: on calls, in emails, in portals, in signatures. What those acts mean (who owns the code, what the liability cap is, how someone can be dismissed) is found out later, under pressure: in diligence, a dispute or a tribunal [reasoned].
2. **So put legal capability at every point where the company commits, not where a lawyer looks.** Those points are the deal desk in the sales system, the purchase order and the vendor sign-up, the HR system, the cap table, outbound email and, last, the signature. Where a gate is possible, it says "yes" within policy at once. Where it is not (a call, a side letter), a catcher records the commitment and routes it to a person [reasoned].
3. **The unit of work becomes the client's policy, not the document.** A company states what it will accept: caps, data terms, notice, governing law, equity. By 2035 a routine contract is a logged handshake between two parties' policies, agreed by their agents [conjecture]. The firm's job moves from drafting paper to **making, defending and updating policies**, which founders cannot state unaided. The client's officers own the risk appetite; the firm proposes it [reasoned].
4. **Much of today's work then stops existing.** NDAs, routine sales and supplier terms, offer letters, registers, minutes, option grants and sell-side diligence become side effects. What remains is adversarial or new: terms outside policy, imposed paper, disputes, dismissals, exits, regulators [reasoned].
5. **Law differs from accountancy and lettings in four ways.** Its facts are contestable. Its outcomes are co-produced with an opposing party. Its key moments are episodic. And its own record can be used against the client. So the firm sells **conditions kept true** and **moments made fast**, and designs its record **for a hostile reader** [reasoned].
6. **The boundary.** An **open commitment standard under a neutral body**, where peers trade with peers; the **best negotiating endpoint** against large buyers' own agents, who will not use a neutral standard; a **portable agent layer** in the client's systems; and an **owned accountable firm** [reasoned].
7. **Growth comes through the other side.** Every contract the firm's agent negotiates lands with another company, which sees terms agreed in minutes. It cannot be advised on that deal. It can be offered its own agent for every other deal [reasoned].
8. **People shrink less than in accountancy, but more than the first draft said.** At 2,000 clients in 2035 the firm needs about 195 people in landscape A and 295 in B, against about 640 for a traditional firm doing the same work. Flow pods that remove each exception at its source cut the middle; the adversarial edge, the boardroom and the courts set a floor [conjecture].
9. **The architecture test.** One element holds ([element] people at the edges). Seven bend. None breaks: [element] bends into the **commitment flow**. The architecture also lacks six things, chiefly **a design for the counterparty**, **the record as a liability**, **privilege and conflicts as constraints**, and **policy-making as work** (section 9).

---

## 1. The client's outcome, segment by segment

The outcome: the company always knows its legal position and obligations, is never held up by legal work, signs good deals fast, avoids disputes and regulatory surprises, and is ready for a raise, sale or diligence at any moment.

These are of two kinds [reasoned]:
- **Conditions**: "I know what we have promised", "our records are right", "we are compliant", "we are ready". True or false right now.
- **Moments done well**: "this deal closed today", "this dismissal was lawful", "this dispute ended before a claim". True once, when it matters.

Accountancy was almost all conditions. Law is a mix, and the mix differs by segment.

| Segment | Typical company | Continuously true | True at the moment | Least wants |
| --- | --- | --- | --- | --- |
| **Venture-backed** (20–150 staff) | Software, fintech, health tech; a round every 18–24 months | "Sales never wait for legal." "Our cap table, IP and contracts would pass diligence today." | A stuck contract signed today; a follow-on round closed in days; clean option grants; a sale with no surprises | Paying for clean-up; founders' evenings on paperwork; a retainer they do not feel |
| **Owner-led and PE-backed** (20–250) | Manufacturing, services, distribution, care | "Our staff contracts and processes are lawful." "We get paid." "No regulator surprises." | A dismissal done right; a debt recovered; a dispute settled; the eventual sale | Tribunal claims; a lawyer's bill for a phone call |
| **Scale-up without a GC** (150–500) | No general counsel (GC) yet | "We have a legal function that scales without hiring ten lawyers." "The board trusts our compliance." | Acquisitions; a regulator's enquiry; a big customer won on time | A team they cannot fill |
| **Scale-up with a GC** | A GC and a small team using AI daily | "I know what every new rule touches." "My panel spend shows outcomes per pound." | Specialists and capacity on call for disputes, regulators, deals | Panel firms billing for juniors; an outside firm inside its systems [seen, practitioner review] |
| **Overlay: regulated** (any size) | Payments, lending, health, energy, AI-heavy products | "We know which rules bite, and we meet them." | An authorisation; an incident handled well | Learning of a rule from a regulator's letter |

Five points follow [reasoned]:
- **The client is a set of decision-makers, not a legal department.** Below about 150 staff nobody inside is a lawyer. The founder, finance lead, head of people and sales leader take legal decisions without knowing it. The firm serves all four.
- **Founders buy unblocking, not prevention.** A small company will pay today for the contract stuck in its pipeline. It will not pay up front for a readiness project [builder review, from experience; reasoned]. So readiness must be a by-product of moments handled, not a thing sold first.
- **No segment wants a law firm, but every segment wants cover.** Boards buy "we took advice" as protection, which is social and reputational [seen, counter-review]. So a named person who answers is part of the outcome, not a cost of it.
- **Readiness bridges conditions and moments.** If "ready" is true, the moment is shorter. But only the company's half of the moment. The other half belongs to investors, buyers and courts (section 3.3).
- **At the top end the client's own team and AI do the routine work.** In-house teams were over 40% of Legora's new customers in the third quarter of 2026 [seen, company statements reported by press]. A GC will not hand an outside firm the record or the gate [seen, practitioner review]. There the firm sells moments, specialists, capacity, a name, and its tested definition of good under licence.

---

## 2. Where information is born and decisions are taken

| Information | Born today | Where today's firm meets it | By 2035 |
| --- | --- | --- | --- |
| **What the company promised a customer** | Calls, email threads, quotes in the sales system, the customer's portal or paper | A PDF sent for review after the deal is fixed | Terms set at the **deal desk** in the sales system, before any paper; agreed agent to agent, on the open standard with peers or against the customer's own agent [conjecture]. Standards exist: oneNDA claims over 6,000 adopters, followed by oneSaaS, oneDPA and oneSLA [seen, Law Insider, company figures] |
| **What the company promised a supplier** | Purchase orders, vendor click-throughs, card sign-ups | Rarely, until a renewal or a breach | At the **purchase order and the sign-up**: vendors reached through the company's spend and single sign-on tools, terms read and recorded as they are accepted [reasoned] |
| **Who works here, on what terms** | Offer letters, HR system, managers' notes | A call when something has gone wrong | Read from the HR system as events: hire, probation, pay change, warning [reasoned] |
| **Who owns the company** | Term sheets, share issues, grants | A spreadsheet rebuilt at each round | A live register kept by the firm's agent, filings derived from it. Companies House has required identity checks for directors and controllers since November 2025 [seen, law firm summaries] |
| **Who owns what the company made** | Code commits, contractor work, AI output | Diligence, two years later | Assignment signed before access is granted [reasoned] |
| **Personal data held and where it goes** | System settings, vendor sign-ups | A data map drawn once by consultants | Read from systems' actual configuration [conjecture] |
| **That a dispute is coming** | A late payment, an angry email, a grievance | A letter before action, months later | Not predicted by a score. The company's own processes are checked as facts (was the review held, was the chaser sent); any view on claim risk is counsel's advice, in a privileged channel (section 3.1) [reasoned] |
| **What the rules are** | Parliament, regulators, courts | A newsletter | Changes mapped to the company's own contracts and processes on publication, with the fix [conjecture] |

**Decisions.** The legal decisions that matter are taken by non-lawyers at the moment of commitment: a salesperson accepting unlimited liability to close a quarter; a manager telling someone in month five they will not pass probation; a founder promising an adviser 1% by email; a sales director's side letter at 11pm on the last day of the quarter [seen, practitioner review, from experience]. Today legal either learns afterwards or is a queue that slows the decision [reasoned]. **So put the firm at each commitment point, able to say "yes" within policy at once, with a fast path to a person outside it, and a catcher where no gate can stand.**

**Where the chokepoint is [reasoned].** In accountancy meaning is born in one place, the invoice, and money confirms it. In law it is born in a dozen systems, and half is written by the other side. The first draft took the signature as the nearest chokepoint. The practitioner showed why it is not: by value, much of a scale-up's revenue is on customers' paper, accepted in their portals, and much of its buying is on vendors' click-through terms. The signature sees the tidy minority. The real chokepoints are **upstream of paper**: the deal desk where price and terms are approved, the purchase order, the sign-up. The signature becomes the last check, not the gate.

**What a record can be [reasoned].** A contract's meaning can be disputed. So the record never holds "truth". It holds **positions with evidence and confidence**. And whatever it holds may one day be read by the other side, in disclosure or a subject access request. So it is written for that reader.

---

## 3. What disappears, what becomes a side effect, what remains

### 3.1 The mechanisms [reasoned]

- **The client's policy as the unit of work.** Each client has a written policy envelope: caps, indemnities, data terms, payment terms, notice, governing law, equity, hiring terms. Founders cannot state these from scratch [builder review, from experience]. So the firm **infers** them from the client's past contracts and decisions, proposes them in a short conversation, and the client's officers **sign** them. The CFO or chief revenue officer owns the risk appetite; the firm writes and defends it [practitioner review; reasoned].
- **Gates at commitment points.** At the deal desk, the purchase order, the vendor sign-up, the HR system, the cap table and the signature, the firm's agent checks the commitment against policy. Within policy it approves at once. Outside it, a person decides.
- **A catcher where no gate is possible.** Calls and side letters cannot be stopped. Outbound email and meeting notes the company chooses to share are read for commitments; each is recorded and, if outside policy, routed to counsel within the day [reasoned].
- **Overrides with a name.** At quarter end, people senior to legal will override the policy [seen, practitioner review, from experience]. The design does not fight this. An override is allowed, takes ten seconds, and records who decided and why. The board sees overrides by person each month. The policy is a default with a visible price, not a wall.
- **Policies that negotiate.** On the open standard, a counterparty's agent queries the client's published envelope, finds the overlap and binds both sides. Against a large buyer's own agent, the firm's agent finds where the buyer's envelope bends and escalates to a person at the right moment [conjecture].
- **Exceptions removed at source.** Every exception a lawyer resolves ends with a change to a policy, a test or a template, so it does not recur (section 6.2) [builder review; reasoned].
- **Events from the client's systems.** A hire in the HR system creates the contract, the IP assignment, the right-to-work check and the option grant. A board decision creates the minute and the filing.
- **Process checks, not predictions.** The first draft had a "friction monitor" scoring which employees or customers might sue. The practitioner showed that such a score writes evidence against the client: in a tribunal it is likely disclosable, and an automated score built from operational data may not meet the tests for litigation privilege [practitioner review; reasoned]. "We knew in March and did nothing" is the worst sentence in a bundle. **Redesign:** the operational record checks only whether the company followed its own lawful process (probation review held, warning recorded with reasons, invoice chased on time). These are facts that help the company if read by a hostile party. Any assessment of risk is **advice from counsel**, requested by counsel, held in the firm's privileged systems, with retention limits. Whether that advice is privileged in every case is untested in England [reasoned].
- **Two layers in the record.** An **operational layer** (commitments, terms, process facts), written to be read by a hostile reader; and an **advice layer** (assessments, positions under dispute, risk notes), held by the regulated firm as legal advice. Nothing moves from the second to the first without a lawyer's decision.
- **The live record is the data room.** Diligence becomes reading, not building.
- **Rule change mapped to the record.** New law becomes a list of affected contracts and processes, each with a fix, done as a fleet.

### 3.2 Today's main work

| Today's work | Fate | What does what remains |
| --- | --- | --- |
| NDAs | **Disappears**: standard terms, agreed policy to policy | Gate agent |
| Sales and supplier contracts between peers | **Side effect**: agreed on the standard within each side's policy | Negotiation agents; counsel above the envelope |
| Contracts on a large buyer's paper or portal | **Remains, faster, then machine to machine**: the firm's agent negotiates against the buyer's agent where it has one; marks up against policy where it does not | Negotiation agents; counsel decides trade-offs |
| Vendor click-through terms | **Side effect**: read and recorded at sign-up; blocked only where they breach a hard rule (data leaving the UK without terms, say) | Gate agent at the sign-up |
| Obligations tracking, renewals | **Side effect**: recorded at each commitment point | Record |
| Writing the playbook | **Transformed**: inferred from past decisions, signed by the client's officers, revised from overrides | Flow pods; named counsel |
| Employment documents | **Side effect**: created from HR events, current with law | People agent |
| Performance, grievance, discipline, dismissal | **Remains; earlier, better evidenced**: people, conflict, fairness | Employment counsel; people agent for process |
| Minutes, registers, filings | **Side effect** of the live register | Corporate agent |
| Option grants | **Side effect, with a valuation residue** | Corporate agent; pod lawyer |
| Round: company-side diligence | **Disappears**: the record is the data room | Record |
| Round: consents, waivers and documents | **Redesigned** from the investors' side (section 3.3): within agreed bounds, consents are given in advance | Corporate agent; a human deal lead for new lead investors |
| Exit or acquisition | **Remains, compressed**: continuous vendor diligence; warranties and negotiation stay human | Deal team; warranty insurers price from the record |
| IP assignments | **Side effect**: signed before access | Rights agent |
| IP filings and portfolio | **Shrinks** | Rights agent; specialist for contested marks |
| Data protection records, notices, vendor terms | **Side effect**: read from systems | Rights agent |
| Subject access requests | **Mostly automated**, and safer because the operational record was written for the reader | Rights agent; counsel when the request is a tactic in a dispute |
| Data breaches | **Remains**: fast judgement with consequences | Counsel; accountable officer |
| Debt recovery | **Mostly a side effect**: an SRA-authorised AI firm already pursues small debts [seen, SRA, May 2025] | Disputes agent; authorised litigator if defended |
| Commercial disputes | **Remains; earlier, fewer** | Disputes team; external advocates |
| Tribunal claims | **Remains; fewer reach a claim** | Employment counsel |
| Regulatory questions and change projects | **Transformed** into continuous mapping and fleet fixes; sold to GCs as a product | Regulatory agent; specialist counsel |
| Everyday "can we...?" questions | **Transformed**: answered at once in chat, within policy | Company counsel agent; named counsel above a set stake |
| Managing external legal spend (GC-led) | **Transformed**: spend, budgets and outcomes per pound across all firms, run as a flow | Spend agent; account lead |
| Onboarding and conflicts checks | **Mostly a side effect; conflicts remain judged** | Operations agent; conflicts officer |
| Time recording, billing, write-offs | **Disappears**: priced per commitment and per moment | Operations agent |

**The count.** Of 26 lines, 13 disappear or become side effects. Six remain mostly human: people issues, exits, disputes, tribunal claims, breaches and imposed paper. The rest change shape. What remains is bigger, more adversarial and more senior than in accountancy [reasoned].

### 3.3 The round, redesigned from both sides

The first draft promised "a round in days" from a clean record. The practitioner is right that this was the wrong cause. Rounds are slow because of investment committees, existing investors' consents, pre-emption waivers and arguments over a few rights. Standard documents already exist and rounds still take weeks [practitioner review, from experience; reasoned]. So the redesign moves to the investors' side [reasoned]:

- **Standing investor consents.** At each round, existing investors agree in the articles and shareholders' agreement the bounds of the next one: a price floor, a dilution cap, standard documents, no new senior rights. Within those bounds, consents and pre-emption waivers are given in advance. UK company law already lets members disapply statutory pre-emption by the articles or special resolution [seen, Companies Act 2006, ss. 567–571, general knowledge]. This is [element], standing policy, applied to investors.
- **Investors' agents check the bounds.** Each fund's agent confirms the round sits inside its consent. A person is needed only outside the bounds.
- **What remains human.** A new lead investor's committee and the few rights it negotiates. So a follow-on or insider round within bounds can close in days. A round with a new lead takes as long as its committee takes, minus the company's half [reasoned].
- **Who sells it.** The investors themselves. A fund that offers standing consents to its portfolio gets faster follow-ons and cheaper ones. This is the investor channel, recast.

---

## 4. What appears that did not exist before

**New conditions, each checked daily:** "nothing committed blind" (every commitment in force, wherever it was made, what it obliges, what it risks); "every override has a name"; "diligence-ready today" (a readiness score by area and an always-open data room); "our people processes are followed and lawful"; "we own what we built"; "we know the rules that bite"; "our record would read well to the other side".

**New products:**
1. **The legal position statement**, monthly: what we have promised, what we are owed, what could hurt us, what we own, and which overrides were taken by whom. The legal equivalent of a balance sheet. Boards have never had one [reasoned].
2. **The client's policy, written and defended.** A signed risk appetite for contracting, hiring and equity, inferred from past decisions, revised from overrides. Founders have never had one [reasoned].
3. **Agent-to-agent contracting**, on the standard with peers and against large buyers' own agents [conjecture].
4. **Continuous vendor diligence for exits.** Vendor diligence reports with reliance letters to buyers and insurers already exist in UK private equity sales [seen, practitioner review, from experience]. The new part is that the record makes them continuous and cheap. The firm does not stand behind the record with a wide reliance letter of its own. Warranty insurers get the record and price the policy; the firm's liability stays at ordinary professional negligence, capped as vendor diligence is today. Later, the firm may co-own a small insurance vehicle with one insurer, its record being the underwriting data [builder review; conjecture]. Fits exits; rounds are handled by section 3.3.
5. **The definition of good, under licence.** For GC-led clients: the firm's tested playbooks, clause positions and test suites, loaded into the GC's own tools and updated when the law changes. The firm answers for the playbook's correctness, which it controls. It does not answer for the outputs of tools it does not control. No insurer would cover that on terms a GC would value [practitioner review; reasoned].
6. **Rule-change maps.** "Here is every contract and process this new rule touches, with the fix." Sold to GCs as a product, today [practitioner review, from experience].
7. **External spend management for GCs.** The firm runs the GC's panel, budgets, e-billing and outcome data across all firms, rivals included [practitioner review; reasoned]. The conflict is obvious: the firm would steer work to itself. So the GC sets the allocation policy, the firm's own share is shown on every report, and the spend agent's rules are open to the GC's audit.
8. **Fixed-price moments with service guarantees**: a dismissal process, an option scheme, a small acquisition, a round within bounds. The firm guarantees what it controls (turnaround on its side, price, completeness of the record) with part of the fee returned if it misses. It does not guarantee the close, which the other side drives [builder and practitioner reviews; reasoned].
9. **Disputes with a risk partner**: early assessment, then fixed or outcome-linked fees with after-the-event insurance or funding. The one area of law where carrying risk and doing the work already go together [seen, counter-review].
10. **Own agent for the counterparty.** After a deal closes, the other side is offered the firm's agent for its other deals, in one step (section 8.1). Never on the deal just done.

**Dropped from the first draft:** pooled term data sold or shared across clients. The practitioner would not opt in, and in a small market anonymised terms are easy to trace [practitioner review, from experience]. The firm keeps only what any law firm keeps: its lawyers' and agents' general know-how, used internally, never disclosed, never used against the client it came from.

**New data:** commitments structured at every commitment point; overrides by person and outcome; cycle times by kind of moment, split into the firm's half and the other side's; process facts against later claims; readiness scored against what diligence later asked.

---

## 5. Where the firm's capability sits, and the boundary choice

### 5.1 By segment, with an adoption ramp

| Segment | First (no integration) | Later (embedded) | People | Firm runs the function? |
| --- | --- | --- | --- | --- |
| **Venture-backed** | Email, chat, the e-signature tool | Deal desk, HR system, cap table, repository access | **Named counsel** in the founders' chat, about 1 per 50–70 at maturity; a deal lead at rounds | **Yes**: no lawyer inside |
| **Owner-led and PE-backed** | Email, chat, HR system for the re-papering | Receivables, purchase orders | Named counsel, 1 per 50–70; pooled **employment counsel** | **Yes**: employment is the main risk |
| **Scale-up without a GC** | All of the above | Plus regulatory mapping and the sales deal desk | A **fractional GC** at the board, on site some days, 1 per 6 | **Fully** |
| **Scale-up with a GC** | The GC's own tools, through the licence | Never in HR or chat unless the GC asks | An **account lead**; specialists for moments | **No**: the GC owns the record and the gate [seen, practitioner review] |

The builder and the practitioner agree that agents in HR, chat and sales systems are the hardest thing to sell [both reviews]. So the firm starts where work already happens without integration (email, chat, e-signature) and goes deeper once it has earned trust. For GC-led companies it never goes in unless asked [reasoned].

### 5.2 The boundary choice

| Option | Strength | Weakness here |
| --- | --- | --- |
| **Own the platform** (record, contract tools, agents as one product) | Control | Harvey ($15.5bn) and Legora ($8.8bn) were valued in autumn 2026 at sums no firm can match [seen, company announcements]. Contract, e-signature and cap-table tools are mature. Counterparties will not adopt a rival firm's paper |
| **Build on a platform** | Fast | The vendor sells the same tools to the client's GC and to rival firms. Nothing is owned |
| **Portable agent layer** | Fits where information is born (many systems) and clients with a GC | Owns little that lasts, unless something else is owned |

**The choice [reasoned]:**
- **Give the standard away.** Back an open commitment standard (machine-readable clauses, variables, policy envelopes and a protocol for agents to negotiate) under a neutral body, building on oneNDA and its successors and the venture capital association's model documents [seen, general knowledge]. A bilateral standard cannot belong to one firm; the other side must trust it. It will win among peers: startups, SMEs and their suppliers.
- **Expect rival standards from large buyers.** Banks, retailers and government buyers hate negotiation volume more than anyone. They are likely to deploy negotiating agents early, with their own envelope, not a neutral standard [practitioner review, from experience; conjecture]. That is not a defeat for the design. It is a second route to structured, fast commitments.
- **Own the best endpoint.** Whatever standard or buyer's agent sits opposite, the firm's agent is the one other agents prefer to deal with: it knows its client's policy exactly, answers at once, and escalates to a person at the right moment [builder review; conjecture]. That is owned capability, not a platform.
- **Be a portable layer.** The record lives in the client's own systems on an open schema and leaves with them. Models, e-signature, storage and cap-table tools are rented.
- **Own five things:** the **accountable firm** (licence, insurance, named people); the **definition of good** (policies, playbooks and test suites refreshed from outcomes); the **negotiating endpoint**; **moment capacity** (deal leads, litigators and employment counsel available tomorrow); and the **counterparty channel** (section 8.1).

Accountancy owned the ledger, because a ledger is a single chokepoint with a single owner. A contract has two owners, and its chokepoints are spread across many systems the firm does not own [reasoned].

### 5.3 Who else is in the picture

| Player | Threat | Stance |
| --- | --- | --- |
| **Elite and large firms** | None at the core; they keep the biggest exits and disputes, protected by the cover they sell [seen, counter-review] | **Refer up and work beside them**; the record makes their diligence faster |
| **Mid-market firms** | Being consolidated by private equity and accountancy-led groups into fixed-fee packages [counter-review, from experience] | **Compete** on speed and per-commitment pricing. Do not buy their books: they bring hourly habits [builder review] |
| **AI-native firms** | Crosby sells fixed-fee contract review, reportedly around $400 a document, with lawyers checking agents' work [seen, as reported in the builder review, not checked here]. Lawhive bought an SRA-regulated firm in 2025 [seen, Legal Cheek]; Garfield.Law is authorised for small debt claims [seen, SRA] | **Compete** on the policy and the record behind each contract; **partner** for debt recovery |
| **Legal AI platforms** | Make the GC self-sufficient | **Use as rails**; license the definition of good into them |
| **Startup legal platforms** | SeedLegals claims 35,000–60,000 companies and a large share of UK early rounds (its own figures conflict) [seen, company pages] | **Partner**: their documents on the standard; the firm takes employment, disputes, exits and policy |
| **HR, payroll, cap-table, spend platforms** | Bundle "legal" into their products | **Integrate**: they supply commitment points; the firm supplies consequence |
| **Large buyers' procurement agents** | Impose their envelope at machine speed | **Negotiate against them**, better than anyone |
| **The client's in-house team and AI** | The main competitor at the top end [seen, counter-review] | **Serve it**: licence, rule-change maps, spend management, moments, cover |
| **Insurers and funders** | Already the "integrated operator" for transaction risk [seen, counter-review] | **Supply evidence**: warranty and legal expenses cover priced from the record; dispute funding; perhaps a joint vehicle |
| **Investors (VC and PE)** | None | **Main channel**: same-day contracts as a portfolio perk; standing consents for follow-ons |
| **Accountancy firms** | Sister legal arms | **Partner**: finance record and legal record are two halves of readiness |

**The 2035 contest** is over who is trusted to say what a company has committed to, and who answers for it. Platforms hold tools, GCs hold the function, large buyers hold their own envelopes, elite firms hold cover at the top. The firm aims to hold the policy, the endpoint and the moments [reasoned].

---

## 6. The organisation

### 6.1 The agent architecture

One shared state (step 3b). Its centre is **each client's legal record**, in two layers: the operational layer (commitments, rights, obligations, process facts, policies, overrides, moments in progress) and the advice layer (assessments and risk notes, held by the firm).

| Agent | One per | Sole writer of | Job |
| --- | --- | --- | --- |
| **Company counsel agent** | Client | The operational record | Orchestrates; answers in chat; raises decision moments; writes the position statement |
| **Policy agent** | Client | The draft policy | Infers the envelope from past decisions; proposes changes from overrides; the client's officers sign |
| **Gate agents** | Commitment point | Commitments in force | Check each commitment against policy at the deal desk, purchase order, sign-up, HR system, cap table and signature: approve, route or block |
| **Catcher** | Client | Uncaught commitments | Read outbound email and shared notes for commitments made outside any gate; record and route |
| **Negotiation agents** | Contract | Mark-ups | Negotiate within the envelope, with people, on the standard, or against a buyer's agent |
| **People, corporate and rights agents** | Client | Employment terms and process facts; register and board record; IP chain and data map | Turn events into documents, filings and lawful processes; check the process was followed |
| **Advice desk agent** | Client | The advice layer | Prepare risk assessments only at counsel's request, in the firm's privileged systems, with retention limits |
| **Rule-change engine** | Firm | Rule-to-fact map | Turn new law into affected items and fixes per client |
| **Spend agent** | GC-led client | Panel spend and outcomes | Run budgets and e-billing across all firms under the GC's allocation policy |
| **Moment orchestrators** | Round, sale, dispute | The moment's plan | Run the agent side under a named human lead |
| **Verifiers** | Output type | Nothing | Independent checks on different models; every citation checked against a primary source |
| **Confidentiality guard** | Firm | Barriers and consents | Enforce information barriers, conflicts, the two-layer rule and the counterparty rule |
| **Governance** | Firm | Nothing | Budgets, limits, circuit breakers, audit against the constitution |

**Constitution clauses specific to law [reasoned]:**
1. **One side only.** The firm never negotiates for both parties. Where both are clients, the standard does the work and neither is advised on the other's terms.
2. **No offer on the live deal.** A counterparty is never offered the firm's services on a deal in which the firm acts for the other side, and never during it.
3. **No learning against a client.** Nothing learned from one client's positions is disclosed, or used against that client.
4. **Write for the hostile reader.** The operational record holds facts, not speculation. Risk assessments live only in the advice layer, at counsel's request.
5. **The client owns its risk appetite.** The firm proposes policy; the client's officers sign it and may override it, by name.
6. **Privilege discipline.** Advice runs through the regulated firm, in confidential systems, under authorised people's supervision.
7. **Candour to courts.** Nothing goes to a court or tribunal without an authorised person's review.
8. **People decisions belong to people.** No dismissal, sanction or settlement with an employee proceeds on an agent's decision alone.

### 6.2 The people, by kind of need, organised by flow

The builder's charge is fair: "judgement desk", "named counsel" and "deal leads" were associates, partners and transaction teams renamed [builder review]. The revision organises the middle by **flow**, not by seniority [reasoned]:

- **Flow pods.** Small teams of one or two lawyers and one engineer, each owning a type of commitment end to end: sales terms, buying, hiring and people process, equity and financing, IP and data, regulatory change. A pod owns the policies, tests and agents for its flow, and resolves the exceptions in it.
- **The pod's rule.** Every exception a lawyer closes ends with a fix to a policy, test or template, so it does not recur. The pod is measured on exceptions per thousand commitments, falling each quarter, not on matters handled [builder review; reasoned]. The judgement desk of the first draft is folded into the pods and shrinks every year, not only with model releases.
- **The edges stay as teams.** Deal leads, disputes and employment counsel face people on the other side. They do not compress by fixing policies.

| Kind of need | Role |
| --- | --- |
| **1. Purpose** | Owners and board: constitution, risk appetite, capital, stance on the standard body |
| **2. Definition of good** | Flow pods: own the policies, tests and thresholds for their flow; decide what "ready" means; audit samples |
| **3. Answerability** | The SRA-required compliance officers for legal practice and finance; money-laundering officer; authorised litigators |
| **4. Capability gaps** | Pod lawyers: novel questions, contested positions, imposed paper, valuations; each closed at source |
| **5. Client demand for a person** | Named counsel; fractional GCs; account leads for GC-led clients. The relationship and the cover |
| **6. The adversarial edge** (new) | Deal leads, disputes team, employment counsel: people facing people on the other side |
| **7. A counterparty's channel** | Court and registry desk |
| **Scaffolding** | Shadow reviewers; trainees; a small central model and evaluation team inside the pods' count |

**The training route [reasoned].** Juniors learned by doing diligence and first drafts. That school closes. Instead trainees work past matters blind and compare with what happened, write test cases for the engines, resolve disagreements between maker and verifier, sit in a pod closing exceptions at source, and from year two own a small book of moments under a deal lead. The SRA's work-based qualification route allows this in principle [seen, general knowledge]. This is also the firm's best recruiting pitch, and it should say so [builder review].

**Rhythm.** Continuous: commitments gated and caught, events turned into documents, processes checked, rules mapped. Daily: exceptions; anything blocked over a day; overrides. Weekly: each pod reviews its exception rate and the fixes; each counsel reviews their clients' decision moments. Monthly: position statements, overrides by person, readiness scores. Quarterly: sampled audits; model releases through the harness; policy proposals from overrides. Yearly: each client's policy re-signed; the board's review of the constitution. Event-driven: a round, sale or dispute gets a named human lead within a day.

### 6.3 Headcount sketch [conjecture]

**Clients:** 2027 starts in **one segment**, venture-backed, with about 100 clients on standing terms, plus one-off buyers of the two entry products (section 8.1). Owner-led clients from 2028; scale-ups from 2029. 700 clients in 2030; 2,000 in 2035 (800 venture-backed, 800 owner-led, 200 scale-ups without a GC, 200 with one). **Traditional comparison:** the same clients buying the same work conventionally, at about £35,000 a year for venture-backed, £30,000 owner-led and £150,000 scale-ups, and about £175,000 revenue per head [conjecture, from general knowledge of mid-market UK firms].

| Role | 2027 | 2030 A | 2030 B | 2035 A | 2035 B |
| --- | --- | --- | --- | --- | --- |
| Owners and board | 3 | 4 | 4 | 4 | 4 |
| Accountable officers and authorised litigators | 3 | 6 | 6 | 8 | 8 |
| Flow pods (lawyers and engineers) | 16 | 34 | 50 | 40 | 70 |
| Named counsel | 4 | 10 | 16 | 23 | 40 |
| Fractional GCs | 1 | 10 | 13 | 33 | 45 |
| Account leads for GC-led clients | 0 | 2 | 4 | 6 | 10 |
| Deal leads | 3 | 10 | 16 | 20 | 35 |
| Disputes team | 2 | 8 | 14 | 18 | 30 |
| Employment counsel | 3 | 7 | 10 | 14 | 20 |
| Court and registry desk | 1 | 3 | 4 | 4 | 6 |
| Operations, conflicts, risk | 3 | 6 | 7 | 8 | 10 |
| Trainees | 3 | 10 | 10 | 15 | 15 |
| Shadow reviewers | 4 | 5 | 12 | 0 | 0 |
| **Total** | **46** | **115** | **166** | **193** | **293** |
| **Traditional, same clients** | **about 25** | **about 210** | **about 210** | **about 640** | **about 640** |
| **Clients per person** | 2.2 | 6.1 | 4.2 | 10.4 | 6.8 |

**What drives the numbers [reasoned]:**
1. **The share of commitments structured at birth**, on the standard or agent to agent with a large buyer. Imposed paper handled by hand keeps pods large. That is the gap between A (40 in pods) and B (70).
2. **The pods' rule.** If exceptions per thousand commitments fall by a fifth a year, pods stay near A while volume triples [conjecture].
3. **The adversarial edge.** Deal leads, disputes and employment counsel are 52 of 193 people in 2035 A. They shrink only as counterparties negotiate through agents; courts and tribunals stay human.
4. **Moment volume.** About 250 rounds, 60 exits, 150 substantial disputes and 400 contentious employment matters a year at 2,000 clients. Readiness cuts the company's half of the effort, not the number.
5. **Fractional GCs at 1 per 6.** Agents prepare everything; board meetings and regulators still do not compress.
6. **The review rule.** If insurers and the SRA accept sampling plus independent verification, shadow reviewers go by the early 2030s. If courts demand personal review of every output, B holds in A.
7. **In 2027 the firm needs more people than a traditional one** for the same book, because it is building the engine.

**Why not 15–20 clients per person, as the builder proposes.** The builder's pod logic is taken and moves the 2035 A figure from 8.8 to 10.4. Going further would need the edge and the board work to shrink too. In 2035 A about 120 of 193 people sit where policy fixes do not reach: the adversarial edge, fractional GCs, named counsel, officers and the court desk. 15–20 is reachable only in a world where most counterparties negotiate through agents and tribunals are rarer, which is beyond landscape A [reasoned]. **Against accountancy:** that redesign reached about 80 clients per person; law reaches about 10.

---

## 7. Economics

**All of this section is [conjecture].** UK law firms typically earn margins of roughly 25–35% [general knowledge, not checked].

### 7.1 What is sold and how

| Product | For | Price, 2027 |
| --- | --- | --- |
| **Per commitment**: each contract agreed, each hire onboarded, each grant issued, each vendor sign-up recorded; with the record, policy, everyday questions, named counsel and position statement included | Venture-backed, then owner-led | Perhaps £100–150 a commitment within policy, £400–600 where a lawyer decides; monthly cap about £1,500 venture, £1,300 owner-led |
| **Entry products**: "send us the contract blocking your quarter, signed today"; employment re-papering for the 2027 changes | Anyone, including GC-led companies | A stuck contract, about £500–800 fixed; re-papering about £3,000–10,000 by headcount, fixed |
| **Fractional GC** | Scale-ups without a GC | £6,000–10,000 a month |
| **For GC-led clients**: licence of playbooks and tests; rule-change maps; spend management | Scale-ups with a GC | Per area licensed; per rule; a share of spend managed |
| **Moments**: dismissal process, option scheme, round within bounds, acquisition, sale, regulator response | All | Fixed, from cycle-time data, with part refunded if the firm misses its own turnaround |
| **Disputes**: early assessment inside the subscription; then fixed or outcome-linked with an insurer or funder | All | By case |
| **Continuous vendor diligence** at exit | All, at a sale | Fixed; insurer prices the warranty cover from the record |

**Pricing logic [reasoned].** Price the commitment, the condition and the moment, never the hour. Hours reward the work the design removes. Per-commitment pricing tracks the client's growth and feels like infrastructure, not a bill; a monthly retainer is cancelled by founders who do not feel it [builder review, from experience]. The cap keeps the bill predictable. The guarantee covers only what the firm controls, because the other side drives much of any cycle time [practitioner review].

### 7.2 Revenue, cost and margin

| | 2027 | 2035 A | 2035 B | 2035 D (price collapse) |
| --- | --- | --- | --- | --- |
| Average yearly charge (venture / owner-led / no-GC scale-up / GC-led) | £15k / — / — / — | £10k / £10k / £60k / £40k | £18k / £16k / £90k / £60k | £4k / £4k / £35k / £15k |
| Commitments, fractional GCs and GC products | £1.5m | £36m | £57m | £16m |
| Entry products, moments, disputes, vendor diligence | £2.7m | £16m | £22m | £17m |
| **Revenue** | **£4.2m** | **£52m** | **£79m** | **£33m** |
| People (loaded £110k in 2027, about £128k later) | £5.1m | £25m | £37.5m | £22m (about 170) |
| Models, verification, rented tools | £0.5m | £3m | £3.5m | £2.5m |
| Standard body (share) | £0.6m | £1m | £1m | £1m |
| Indemnity and other insurance | £0.3m | £3m | £3.5m | £3m |
| Acquisition (no books bought) | £0.4m | £2.5m | £2.5m | £2m |
| Other overhead | £0.5m | £3m | £4m | £2.5m |
| **Cost** | **£7.4m** | **£37.5m** | **£52m** | **£33m** |
| **Margin** | **about −76%** (a build year) | **about 28%** | **about 34%** | **about 0%** |
| Clients' total spend against traditional (£112m) | — | **46%** | **71%** | **29%** |

**What the numbers say [reasoned, on conjectured numbers]:**
- **A:** clients spend under half of today and get more (speed, policy, prevention). The firm earns a normal law-firm margin with under a third of the people.
- **B:** prices hold longer; the firm earns more, being far cheaper to run.
- **D:** the routine layer becomes free inside clients' own AI, startup platforms and HR tools. The firm survives on moments, disputes, the endpoint and fractional GCs, at break-even. The first draft had −5% here; owning the best endpoint, not a platform, softens D a little but does not remove it. **That is still the price of the boundary choice.**
- **2027 costs less than the first draft** (£7.4m, not £10.5m), because no firm is bought and one segment is served.

**Where the profit comes from:** (1) **moments made fast**, at fixed prices and lower effort than any rival starting from a cold file; (2) **fractional GCs**, priced against a hire; (3) **disputes with a risk partner**; (4) **per-commitment volume**, which grows with clients' growth; (5) **products for GCs** (licence, rule-change maps, spend). **Not from** drafting, review or diligence hours, from term data, or from referral fees from insurers.

---

## 8. How it is built from 2027

### 8.1 The first wedge: one stuck contract, one forced change

The first draft led with "the always-ready company": 30 days of record-building, sold through investors. The builder is right that this is a consulting project with a subscription attached [builder review]. The revision enters through **units of urgent work**, and lets readiness accumulate as a by-product [reasoned]:

- **"Send us the contract blocking your quarter; signed today."** A fixed price, delivered in hours, a lawyer accountable. Each contract handled adds to the client's record and teaches the policy agent the client's positions. After ten contracts, the firm proposes the client's policy. After the policy is signed, the gates go live in email and e-signature. Readiness is what is left behind [reasoned].
- **Employment re-papering for 2027.** Every employer must change its contracts and processes for the new unfair dismissal rules: qualifying period cut to six months, compensation cap removed, for dismissals from 1 January 2027 [seen, law firm timetables; dates indicative]. A fixed price by headcount. The practitioner would buy this now [practitioner review, from experience]. It also brings the firm into the HR system, by invitation, for a reason the client already accepts.
- **One segment first: venture-backed.** Three segments at 100 clients is too many [builder review]. Venture-backed companies' counterparties are mostly their peers, which feeds the counterparty loop. The re-papering product is sold to anyone, including GC-led companies, as a product, not a segment.
- **Investors as the channel, recast.** A fund pays for "your companies get same-day contracts" as a portfolio perk, and offers standing consents to its portfolio for follow-ons (section 3.3). Not a readiness audit.
- **The counterparty loop.** Every contract the firm's agent agrees lands in another company's inbox, with terms back in minutes. After the deal closes, the other side is offered its own agent for its other deals, joining in one step [builder review; conjecture]. Conflicts rules limit this: never on the live deal, never advised on it, never during it (constitution clause 2). Traditional firms cannot copy the loop, because their paper carries no product.
- **Authorisation, not acquisition.** Do not buy a firm in 2027: a bought book brings hourly habits and clients who expect the old service [builder review, from experience]. Hire authorised solicitors and apply now; the SRA took about eight months to authorise an AI-driven firm [seen, SRA; Law Gazette]. If authorisation slips past mid-2027, the hired solicitors deliver through a partner firm on referral until it lands [reasoned].

**What makes clients adopt:** a deal stuck today; a forced change they must make anyway; contracts back the same day; one price per commitment, capped; their investor or accountant recommending it; a senior named person from day one.

**The weakness.** Venture-backed companies are price-sensitive. The wedge proves the machine and feeds the loop; owner-led companies and scale-ups pay for the firm.

### 8.2 Sequence to 2035 [conjecture for dates]

| Period | Main moves | Commitments structured at birth (standard / agent to agent) |
| --- | --- | --- |
| **2027** | Apply for authorisation as an alternative business structure; hire authorised people; stuck-contract and re-papering products; venture-backed only; two or three investor perks; join or found the standard body; review every output | about 10% / under 5% |
| **2028** | Policies signed for standing clients; gates in email, e-signature and HR; owner-led clients; counterparty loop live; standing investor consents with one fund | 20% / 5% |
| **2029** | Gates at the deal desk and the purchase order; scale-ups; fractional GCs; rule-change maps and licence for GCs; disputes with an insurer and funder | 25% / 10% |
| **2030** | Negotiation against large buyers' agents; sampling replaces full review where insurers accept; spend management for GCs | 30% / 15% (A) |
| **2031–33** | Continuous vendor diligence priced by warranty insurers; perhaps a joint insurance vehicle; combined finance and legal readiness with an accountancy partner | 35% / 25% |
| **2034–35** | Routine contracts mostly policy to policy; a legal function for smaller clients; products and moments for GC-led ones | about 40% / 30% (A); 25% / 15% (B) |

The first draft forecast 50–70% of commitments "on a standard" by 2035. The practitioner is right that this is too generous for any company that sells to banks, retailers or government [practitioner review]. The revision splits the measure: the neutral standard wins in the middle (NDAs, data terms, SaaS between peers), about 40% in A; agent-to-agent deals against large buyers' own envelopes add another 30%. The total structured at birth, about 70% in A, is what drives headcount [reasoned].

---

## 10. What would make this wrong, and the stress test

### 10.1 What would make this design wrong

1. **Large counterparties neither adopt the standard nor deploy agents.** Then imposed paper stays manual, pods stay near B, and the firm is a fast level 2 firm with a better record [reasoned].
2. **The client's own AI takes the routine layer for free**, early. Landscape D arrives by 2030 [conjecture].
3. **Founders will not sign a policy, or seniors override it so often it means nothing.** Then gates become a review queue. Measure overrides per hundred commitments from 2028 [reasoned].
4. **The advice layer is not privileged.** If English courts treat agent-prepared risk notes as operational documents, the two-layer design fails and risk assessment must stay manual and occasional [reasoned].
5. **The counterparty loop does not convert,** or regulators treat the offer as soliciting the other side improperly. Then acquisition costs return to normal [conjecture].
6. **Courts and insurers demand personal review of every output.** The *Ayinde* warning on fake citations (2025) points that way [counter-review; general knowledge]. Then B holds in A.
7. **Moments are too lumpy.** Profit from rounds and exits rides the funding cycle [reasoned].
8. **A correlated error.** One wrong clause in a standard, one wrong policy template, or one misreading of new employment law, repeated across hundreds of clients. Indemnity insurers may aggregate such claims [counter-review; reasoned].
9. **The training route fails**, leaving the pods without successors [reasoned].

### 10.2 The stress test

| Fact | Effect on the design |
| --- | --- |
| **Reserved activities** (conducting litigation, rights of audience and others) need authorised persons [seen, Legal Services Act 2007]. The Court of Appeal in *Mazur* (March 2026) allowed supervised staff to do litigation tasks [seen] | Authorised litigators conduct litigation, with agents as their tools. Whether "supervised AI" is treated like supervised staff is untested. An authorised person signs every court step |
| **Outside ownership** is allowed through alternative business structures in England and Wales, not in most of the US [seen, general knowledge; counter-review] | Build in England and Wales. The model does not export to the US as is |
| **The SRA authorised an AI-driven firm** with named solicitors accountable, after about eight months [seen, SRA; Law Gazette] | Apply at once; hire rather than buy; deliver through a partner firm until authorised |
| **Client money** brings strict rules, under review [seen, SRA] | Hold none. Money at rounds, exercises and settlements runs through an escrow partner. [element] bends to the commitment flow |
| **Conflicts and confidentiality rules** in the SRA codes | One side only; no offer on the live deal; no learning against a client; no pooled term data; a conflicts officer |
| **Disclosure and subject access**: a company's documents, including automated records, may be disclosable in litigation and tribunals; litigation privilege needs litigation in reasonable contemplation and a dominant purpose [seen, general knowledge; practitioner review] | Two-layer record; process facts only in the operational layer; risk notes only at counsel's request, in the firm's systems, with retention limits |
| **Privilege**: client chats with a public AI held not privileged in the US [seen, *Heppner*]; English position untested | Advice through the regulated firm, in confidential systems. Warn clients about their own generic AI use. A selling point and a risk |
| **Monitoring staff** is limited by data protection law and ICO guidance [seen, general knowledge] | The catcher reads outbound business email and shared notes, not private messages; staff are told; an impact assessment per client. No scoring of individuals |
| **Indemnity insurance** is compulsory and yearly [seen, counter-review] | Agree aggregation terms and the review rule with insurers before launch; reach limits on every change to the standard or a policy template. No wide reliance letters; no liability for tools the firm does not control |
| **Pre-emption and investor consents** are set by the Companies Act 2006 and each company's articles and shareholders' agreement [seen, general knowledge] | Standing consents are written into the articles at a round, by members' own decision |
| **Litigation funding is unsettled**: the government promised in December 2025 to reverse *PACCAR*; the 2026 King's Speech left it out [seen, law firm reports] | After-the-event insurance and fixed fees first; funding once the law is clear |
| **Employment law changes through 2027** [seen; dates indicative] | The entry product; higher stakes for every dismissal keep employment counsel busy |
| **Companies House reform** in force; checks on filing agents not before November 2027 [seen] | The corporate agent keeps the register and files as a verified agent |
| **Powerful counterparties impose their paper** [seen, practitioner review] | The standard wins among peers; the endpoint negotiates against buyers' agents |
| **GCs insource** [seen, counter-review; in-house growth at legal AI vendors] | Licence, rule-change maps, spend management and moments for GC-led clients; never compete for their routine work or their record |

### 10.3 What the stress test changes

1. **Not the core design.** Commitment points, the client's policy, the two-layer record and moments survive today's rules.
2. **It confirms [element]'s restatement.** Client-money rules make "in the money flow" costly; the commitment flow is not regulated as such.
3. **Authorised people stay at every court step**, whatever capability does. That sets a floor under the disputes team.
4. **Disclosure shapes the record** more than privacy does. That is new to the architecture.
5. **Insurers set two limits**: the review rule, and what the firm can stand behind (its own playbooks and turnaround, not others' tools or wide reliance).

**Where this is weakest.** Every figure is conjecture. Five unknowns decide whether it works: the share of commitments structured at birth, including against large buyers' agents; whether founders sign policies and seniors respect them; whether the advice layer stays privileged; whether counterparties convert; and whether funds adopt standing consents. The first, second and fourth can be measured within a year of the first clients. That is the reason to start with stuck contracts in one segment.

---

## Sources checked in this run

- *Mazur*: [2026] EWCA Civ 369, 31 March 2026 (judiciary.uk); SRA "conducting litigation"; HSF Kramer and Law Society summaries.
- Garfield.Law: SRA news release, May 2025; Law Gazette. Lawhive: Legal Cheek, September 2025; Business Wire, March 2026.
- Employment Rights Act 2025 timetable: Slaughter and May, DLA Piper and Irwin Mitchell summaries (indicative dates).
- *PACCAR*: Dechert, January 2026; Osborne Clarke and JD Supra on the 2026 King's Speech.
- Companies House: Mishcon de Reya, Burges Salmon, HSF Kramer.
- oneNDA and successors: LawNext, February 2025; Law Insider Standards Hub. SeedLegals: company pages.
- Harvey and Legora: Harvey, September 2026; TechCrunch, March 2026; reports of Legora's October 2026 round.
- SRA client money: SRA consultation pages, 2024–2026. *Heppner*: HSF Kramer, Proskauer and Orrick summaries, 2026.
- From the reviews, not checked in this run: Crosby's fees, funding and Cursor volume (builder review, citing Contrary Research, TechCrunch, Artificial Lawyer, Law360); vendor diligence reliance practice and round timelines (practitioner review, from experience).
- Not checked: *Ayinde*; law firm margins; legal spend by company size; ICO monitoring guidance; qualification route details; Companies Act pre-emption sections (general knowledge).

---

