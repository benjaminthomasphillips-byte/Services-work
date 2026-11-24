# Level 3. Lettings and property management in England, redesigned from scratch

Draft by Claude, 24 November 2026. Revised the same day after two reviews: a builder pushing it further (`level3-lettings-review-builder.md`) and a practitioner testing it against reality (`level3-lettings-review-practitioner.md`). One author, no sub-agents. It follows the six-step procedure in `step-3c-the-electricity-test.md`, the kinds of human need in `step-3b-the-agent-enterprise.md` and the engine in `step-1-the-engine.md`. It sets itself against `example-lettings.md`, which automated today's task list (level 1). The last section, "Review and response", lists every review point and what was done with it.

Labels:
- **[seen]** exists somewhere today, with source;
- **[reasoned]** follows from logic;
- **[conjecture]** plausible towards 2035.

Points carried from the reviews keep the reviewer's own label where it was [experience] (an operator's judgement, one step weaker than [reasoned]). Today's rules and institutions are facts to design around. They are applied in full only in the stress test (section 10). A few facts were checked on 24 November 2026; sources are at the end.

---

## The answer in brief

Level 1 asked: "how do agents run a lettings agency?" This paper asks: "what would a landlord and a tenant buy if nobody had ever built a lettings agency?"

The first draft answered: a firm whose unit of work is **the home**, which keeps five conditions true: **legal now, safe now, dry and warm now, paid now, next tenant ready**. The reviews kept that answer and moved it in two directions.

The builder showed it still sold a smoother version of today's bundle. A landlord in 2035 does not want "management at a fixed price". He wants **a known net income from a home he never thinks about, or a clean way out**. A tenant does not want to rent from a stranger. She wants **to belong to a network of homes she can move within**. The practitioner showed where the bricks push back: repair risk must be priced home by home, keys and turns stay physical in scattered stock, devices fail more than tenants refuse, and some exceptions do not shrink.

Seven design moves now do most of the work [reasoned]:
1. **The home record, as an open standard.** Owned by the landlord, maintained by the firm, published schema from 2027. Filled first from what the home already reports (smart meters, connected boilers, bank feeds, tenant video), with devices only where they pay.
2. **The property wallet.** Rent, float, tax pot and a repair reserve that is visibly the landlord's money, per home, with a regulated partner. Reconciliation, statements, payouts and landlord tax become side effects.
3. **Standing policy instead of approvals.** Spend limits, tenant criteria, rent strategy and risk appetite, set once and reviewed yearly. Most agreements already carry a spend limit, so this is an extension, not a leap.
4. **One annual home visit that is also the underwriting survey.** Gas, alarms, condition record and small fixes in one trip, with a paired electrician every fifth year. The first visit prices the home.
5. **Selling the outcome, priced home by home.** A banded fixed-cost home, and on top of it a **net-yield contract**: one guaranteed monthly payment to the landlord, with an insurer carrying the tail from day one.
6. **The renter network.** Verified tenants who carry their passport, rent history and deposit between the network's homes, and a machine-readable listing interface for tenants' own agents from 2028. Tenants become the distribution.
7. **The exit route.** A landlord who wants out sells with the tenant in place to a capital partner, priced from the record. The home stays in the network and the tenant stays in their home.

About 9 of level 1's 22 case types disappear or become side effects, and 5 more change shape. That is fewer than the first draft claimed (13). Inside headcount for 5,000 landlords falls to about 32 to 49 by 2035, against 35 to 60 at level 1 and 120 to 150 in a traditional firm [conjecture]. That gap is smaller than first claimed, because councils, complaints and fair referencing need people. The bigger change is still not the count. It is what is sold (an income and an exit, not a service), who brings the business (tenants and lenders, not portals), and the field, which the firm now runs itself. Because level 3 removes work rather than automating it, it still pays off if AI capability plateaus.

---

## 1. The client's outcome, segment by segment

### 1.1 What each party wants to be continuously true

| Party | Continuously true | Measure |
| --- | --- | --- |
| **Landlord** | A known net income arrives on a known day. The home is legal and in good order. Almost no time spent. The asset holds value. A clean exit is always available | Net income against contract; days out of compliance (target zero); landlord minutes per home a year; condition trend; days from "I want out" to sale completed |
| **Tenant** | The home works: warm, dry, safe, fixed fast. Fair treatment. Free to stay or move without friction or a second deposit | Fix time by class; hazard-free days; complaints upheld; cost and days to move within the network |
| **The asset** (for lender, buyer, insurer) | Its condition and history are known and believable without a new survey | Share of the home's life covered by verified records; lenders and buyers accepting the record |

"No hassle" is the landlord outcome that is rarely counted. Here it is a number: landlord minutes per home per year, outside decisions the landlord chose to keep. The target is close to zero [reasoned].

### 1.2 The segments

| Segment | Share [conjecture] | What they want | What they get |
| --- | --- | --- | --- |
| **Accidental and single-home** | about 55% | "Pay me each month and keep me out of trouble" | Net-yield contract or banded fixed-cost home; a named person; almost no decisions |
| **Small portfolio (2–10 homes)** | about 35% | "Low cost, clear numbers, my call on big things" | Policy control, live portfolio view, an asset plan per home, optional yield contract per home |
| **Professional (10–100 homes)** | about 8% | "Data, control, an interface my systems can call" | The firm's agents in their systems; operations to their policy; capital planning |
| **Institutional** (build-to-rent, single-family rental, funds) | a few dozen mandates, growing | "Run our operations to a standard we can audit" | The firm runs or embeds into their operations function |
| **Leaving** | a quarter to a third say they will cut back or sell [seen as reported: English Private Landlord Survey 2024; NRLA Q2 2026; not checked at source] | "Get me out without a fight or an empty home" | Tenanted transfer to a capital partner, priced from the record, with an independent valuation |
| **Overseas and absent** | about 5%, overlapping | "Tax handled, nothing to do" | Withholding and returns as a side effect |

Two populations are not paying clients but decide the result:
- **Tenants**, about 7,000 households in the reference book. In the first draft they were a "second customer". Here they are **members of the network and its main channel of supply** (section 4.1). Their product is paid from landlords' fees, since most fees to tenants are banned [seen: Tenant Fees Act 2019, general knowledge].
- **Contractors and trades**, mostly sole traders. Level 1 found supply, not dispatch, is the constraint. Level 3 brings routine work and turns in-house and changes the contract for the rest.

For comparison the reference book stays at level 1's scale: 5,000 landlords, 7,500 homes. Institutional mandates are sized per 10,000 homes, because they add homes without adding clients. Over time the exit route moves homes from the first segments into the institutional one without losing them.

---

## 2. Where information is born and decisions are taken

| Information | Where it is born | How it reaches the firm today | By 2035 |
| --- | --- | --- | --- |
| **Condition** | In the fabric and systems | Inspections every 6–12 months; tenant calls after failure | **Read before install**: smart meter data with the tenant's consent, connected boilers, a paid 60-second tenant video each quarter, the annual visit. Sensors only where the risk model says they pay, on cellular or low-power networks [seen: about two-thirds of domestic meters smart and working in smart mode at end 2025, DESNZ, cited by the builder and not rechecked; conjecture on inferring damp from energy data] |
| **Compliance** | Engineers' certificates, council licences, energy ratings | Documents emailed, filed, chased | Read from registers and engineers' apps at issue; council licensing still needs people who know the local officers [reasoned] |
| **Rent and costs** | Bank accounts | Pooled account reconciled by staff | Rent by open-banking mandate into each home's wallet [first wave of commercial variable recurring payments live since June 2026, seen] |
| **Tenant identity and income** | Passports, payroll, bank accounts | Documents uploaded, often forged | Consented, verified data shared once as a reusable passport; fraud moves to borrowed and mule accounts, so a judgement layer stays [seen: digital identity for right to rent; open-banking referencing in use, practitioner's experience] |
| **Landlord intent** | The landlord's head | A call per decision | Standing policy, reviewed yearly; for yield-contract landlords, almost nothing beyond hold or sell [reasoned] |
| **Demand** | Tenants' searches | Portals, enquiries, viewings | The network's own members first; tenants' AI agents reading verified listings from 2028; portals as one channel [conjecture on pace] |
| **Exit intent** | The landlord's head, usually at a remortgage, a tax change or a bad tenancy | An estate agent, after the tenant has been asked to leave | Asked at each yearly policy review; the record lets a capital partner price the home without a survey [reasoned] |
| **Counterparties** | Deposit schemes, councils, landlord database, HMRC, freeholders, lenders | Portals, letters, phone | Interfaces where they exist; named people where they do not [reasoned] |

**Decisions.** Today the firm carries information to the landlord so the landlord can decide, many times a year: each repair, each tenant, each renewal. At level 3 the landlord decides the rules once (spend limits, tenant criteria, rent strategy, a capital plan) and the firm decides the cases. Under a net-yield contract the landlord gives up even most of the rules, in return for a fixed payment. The landlord keeps the decisions that are really theirs: capital spend above policy, possession, hold or sell. Information no longer has to travel, so the work of carrying it disappears [reasoned].

---

## 3. What disappears, and why

### 3.1 The tasks and waits that go

Step 3c's test: a task goes when it existed only because information was in the wrong place, time or form, or because authority and money were badly arranged [reasoned].

- **Inspections** existed because nobody knew the home's condition between visits. Meter and boiler data, quarterly tenant video, the annual visit and sensors where they pay replace them.
- **Chasing certificates** existed because certificates were paper held by others. Registers feed the record. The annual visit does the gas check, which can be done up to two months early and keep its anniversary date, so rounds can be planned [seen: Gas Safety (Installation and Use) (Amendment) Regulations 2018].
- **Landlord approvals** existed because authority sat with the landlord, case by case. Policy and a visible reserve replace them.
- **Document referencing** existed because proof came as documents. Verified data from source replaces the checking. **The judgement does not go** (see case 5).
- **Reconciliation and statements** existed because rent landed in a pooled account with poor references. A wallet per home makes the statement a live view.
- **"Where is my repair?" calls** existed because status was hidden. Live status ends them.
- **The search for the next tenant** existed because it began after notice. Good operators already re-let inside the two-month notice [experience, practitioner]. The network's members make it routine.
- **Landlord tax as a project** existed because records were assembled late. The wallet is the ledger [Making Tax Digital applies above £50,000 from April 2026, £30,000 from April 2027 and £20,000 from April 2028, seen].
- **Selling a let home as a fight** existed because a buyer could not trust its condition and wanted it empty. The record and a capital partner let it sell with the tenant in place.

What does **not** go, on the practitioner's evidence: keys and access in scattered houses, the turn between tenancies, and eyes at check-out. Section 3.2 redesigns these rather than pretending they vanish.

### 3.2 Level 1's case types, line by line

**Gone**: the task no longer exists. **Side effect**: the outcome still happens, with no case opened. **Changed**: still real work, done in a different shape. **Remains**: still a case.

| # | Level 1 case type | Level 3 | Why | Who or what does what is left |
| --- | --- | --- | --- | --- |
| 1 | Landlord onboarding | **Remains, smaller** | Identity and title at source; the mandate is a policy set once; the home is underwritten at the first visit | Onboarding agent; underwriter's rules; asset partner for accidental landlords |
| 2 | Property baseline | **Side effect** | First annual visit builds the record and prices the home; registers fill the rest | Technician once, then the home agent |
| 3 | Marketing and applicants | **Side effect** | Listing written from the record and published to members and tenants' agents | Market agent; portals as one channel |
| 4 | Viewing | **Mostly gone** | Self-guided in empty build-to-rent homes; recorded tour in occupied ones; members moving within the network often skip it | Field host for shortlists only |
| 5 | Referencing, right to rent | **Changed: checking gone, judgement remains** | Verification of a consented passport is instant. Thin files (self-employed, students, new arrivals, Universal Credit, guarantors) and mule-account fraud need an explainable affordability judgement, now that large rent in advance and blanket bans are outlawed | Agent for the clear cases; judgement desk with the fairness lead for the rest |
| 6 | Tenancy creation, move-in | **Side effect** | Standard terms, deposit and prescribed information generated and served; tenant records move-in on video | Agents and verifier |
| 7 | Rent month | **Gone** | Mandate payment into the wallet; payout on a fixed day | Money agent; a person for the shrinking tail of benefit and unidentified payments |
| 8 | Arrears | **Remains, changed** | Earlier signal; under rent assurance or a yield contract the firm carries the loss, so it wants the tenancy to last | Household support first; early contact by agent |
| 9 | Repair job | **Changed: admin gone, physical work remains** | The annual visit and planned replacement cut call-outs; dispatch and payment automatic. About half of reactive spend (turnover, white goods, misuse) is not touched by sensors [experience, practitioner] | Home agent; own technicians for small jobs; contractors for the rest |
| 10 | Emergency hazard | **Remains, caught earlier** | Leak, smoke and carbon monoxide detection; shut-off valves where the risk model says | Night on-call; out-of-hours contractors |
| 11 | Damp and mould | **Changed: continuous condition** | Risk inferred from meter data and video; sensors in high-risk homes; alerts ranked so a January humidity spike is not a case | Home agent; building scientist owns the bands and "resolved"; surveyor for real cases |
| 12 | Compliance cycle | **Side effect** | Gas and alarms in the annual visit; electrical check every fifth year by a paired electrician; other certificates scheduled from the record | Technician and electrician; compliance agent |
| 13 | Periodic inspection | **Gone** | Data already in the home, quarterly video, the annual visit | — |
| 14 | Tenancy changes | **Side effect** | Rent changes from the landlord's strategy; pets and permissions from policy, in hours | Agent; a person for tribunal challenges |
| 15 | End of tenancy, deposit | **Changed: one visit, not two** | Sensors do not see a stained carpet. So the check-out visit is also the turn's scoping visit. Evidence and works order are made in one trip; disputes shrink because the before-state is continuous | Turn lead; agent; adjudication for the few disputes |
| 16 | Possession | **Remains** | Ending someone's home needs a person and a court, now on section 8 grounds only | Accountable officer; solicitor |
| 17 | Keys and access | **Remains, smaller (gone in build-to-rent)** | In blocks the firm controls the door. In scattered houses tenants change locks, freeholders hold communal doors and 24 hours' notice is required. Access becomes a booking: notice served automatically, tenant picks the slot, key safe where the tenant agrees | Agent; a person for refusals and lock-outs |
| 18 | Voids | **Changed: the void is the turn** | The search happens inside notice. What remains is clean, paint, carpet, snag, which takes 7–14 days today [experience]. Planned from the record during notice, materials ordered before keys return, own turn crew | Network agent; turn crew; field check on alert |
| 19 | Freeholders, managing agents | **Remains** | Information is born in someone else's building | Liaison agent; council and freeholder liaison |
| 20 | Insurance claims | **Remains; evidence is a side effect** | The timeline already exists | Claims agent; a person with loss adjusters |
| 21 | Landlord events | **Remains, with a new route out** | Authority must be checked by a person; a sale can now be a tenanted transfer with the record | Accountable officer; exit desk |
| 22 | Landlord tax | **Side effect** | The wallet is the ledger; overseas withholding automatic | Tax agent; officer signs |
| S1 | Enquiries, complaints | **Enquiries mostly gone; complaints remain and may grow** | Status is visible; the new ombudsman will raise volume | Complaints team of three, feeding the definition of good |
| S2 | Landlord advice | **Grows into products** | Asset plans, energy upgrades, yield contracts, exit | Asset partners and exit desk |
| S3 | Vulnerability | **Remains, flagged earlier** | Payment and contact patterns raise a quiet flag, with care | Household support |
| S4 | Fraud | **Shrinks; moves** | Verification at source closes document forgery; mule accounts and payee changes stay human | Fraud sentinel; named person |
| S5 | Councils: licensing, enforcement, HMOs | **Remains (new line)** | Selective and additional licensing differ by borough; enforcement needs people who know the officers | Council liaison |

Count: **3 gone or mostly gone** (4, 7, 13), **6 side effects** (2, 3, 6, 12, 14, 22), **5 changed in shape** (5, 9, 11, 15, 18), **8 remain as cases** (1, 8, 10, 16, 17, 19, 20, 21), most smaller. The first draft claimed 13 gone or side effects; the honest number is 9, with five more that are real work in a better shape. In a build-to-rent block, case 17 also goes [reasoned from the table and the practitioner's corrections].

### 3.3 Why this is not level 1 done better

Level 1's largest remaining cost was people who do not reply: landlords, contractors, key holders [example-lettings, 7.2]. Level 3 removes the reason to chase each of them [reasoned]:
- Landlords do not reply because they were asked. Here they are not asked; under a yield contract they have almost nothing to answer.
- Contractors do not come because work is scattered and payment slow. Here routine work and turns are done by the firm's own people on planned rounds, and contractors are paid per home, not per call-out.
- Key holders cannot be found because access is arranged by phone. Here access is a booking the tenant controls, with notice served automatically.

And level 3 changes where business comes from. Level 1 bought attention from portals. Level 3 earns supply from tenants who want to stay in the network, and from lenders who need the record.

---

## 4. What appears that did not exist before

### 4.1 New products

| Product | What it is | Basis |
| --- | --- | --- |
| **The banded fixed-cost home** | One monthly price per home, set by band at the first visit (component ages, building type): management, compliance, the annual service, routine and reactive maintenance under a per-job cap. Known defects go into the capital plan, not the price | [conjecture]; parts [seen]: boiler cover plans, social housing repair contracts priced per property |
| **The net-yield contract** | One guaranteed monthly payment to the landlord. Rent assurance, voids, maintenance, compliance and management folded in. A floor, plus a share of any year that comes in under cost. Only for underwritten homes. An insurer carries the tail from day one | [conjecture]; rent guarantee insurance and guaranteed-rent schemes [seen] |
| **Rent assurance** | Rent paid on a fixed day whatever the tenant does, priced per tenancy for a market without section 21 | [seen as rent guarantee insurance]; priced here from the firm's data |
| **The compliance promise** | "We keep it legal. If we fail, we pay to put it right, refund our fee for the period and cover provable losses up to a cap." Not a promise to pay fines, which may not be insurable or recoverable | [reasoned; needs legal advice] |
| **The home record, as an open standard** | Verified, dated history: condition, works, components and ages, energy, compliance. Owned by the landlord. Schema published in 2027; lenders, insurers and conveyancers invited to rely on it | [conjecture]; building logbooks exist in pieces |
| **The asset plan** | A dated capital plan per home; the route to EPC C; a hold, sell or refinance view | [reasoned] |
| **Energy upgrade, financed** | "EPC C done, financed from the rent", sold through buy-to-let lenders and brokers. Repaid from the wallet over time | [seen rule]: EPC C for privately rented homes from 1 October 2030; government says 48% already meet it. Financing [conjecture] |
| **Tenanted transfer** | The exit route. A landlord sells with the tenant in place to a capital partner, priced from the record and checked by an independent valuer. The firm keeps running the home | [conjecture]; portfolio sales with tenants in place exist [seen, general knowledge] |
| **The renter network** | Free to tenants. A verified passport; rent history that can count towards credit, with consent; a deposit carried between the network's homes; priority to view; a move within the network in days | [conjecture]; rent reporting to credit agencies exists [seen, general knowledge] |
| **The listing interface** | Machine-readable, verified listings: condition, energy, running costs from meter data, pet rules, viewing slots, an offer at the advertised rent. Built for tenants' AI agents from 2028 | [conjecture on agent adoption]; no bidding above advertised rent [seen: Renters' Rights Act] |
| **Tenant's home guarantee** | Published fix times; automatic credits when missed, paid from the firm's margin | [conjecture] |
| **Operations as a service** | The firm runs or embeds into an institutional owner's operations, on the owner's systems, including homes it brought them | [seen as outsourced management; reasoned on the agent layer] |
| **The network for self-managers** | Annual service, compliance promise and dispatch for landlords who will never buy management | [reasoned] |

### 4.2 New continuous conditions

Each is a live state, shown to landlord and tenant and checked by a verifier that does not depend on anyone choosing to reply [reasoned]:
- **Legal now:** every obligation in date, the next one scheduled.
- **Safe now:** no open hazard; alarms reporting; no leak or carbon monoxide alert.
- **Dry and warm now:** humidity and temperature in band, by season and building type, judged on sustained readings, not single spikes.
- **Known now:** the home is reporting. A home whose data has gone quiet is "unknown", never "fine". Fourteen days unknown triggers a video request, then a visit [reasoned, from the practitioner's point on uptime].
- **Paid now:** rent received or covered; contractors paid within 48 hours of evidence; the landlord's contract payment made.
- **Ready now:** for each home under notice, a next tenant matched and a turn planned with materials ordered.
- **Fit for 2030 and 2035:** the route to EPC C and to the Decent Homes Standard, which government says will apply to private renting from 2035, timing still to be consulted on [seen].

### 4.3 New data and the decisions it supports

New data: the condition and band of each home at entry; meter, boiler and video data by home; a register of components and their ages; works and whether the problem came back; payment reliability, with consent; turn days; contractor performance under per-home contracts. In aggregate, failure rates by component, building type and age. The home record is open. **The aggregate failure and loss data is not.** It is what lets the firm price the fixed-cost home and the yield contract better than an insurer without it [reasoned; step 1's P3: the fast layer feeds the slow, priced layer].

| Decision now supported | Taken by | Rests on |
| --- | --- | --- |
| What band a home is in, and what goes into the capital plan | Underwriter's rules; actuary owns them | First-visit survey, component ages |
| Replace a boiler before winter, not after it fails | Firm within policy; landlord above it | Boiler state, age, failure curves |
| Which homes to upgrade for EPC C, in what order, financed how | Landlord, with the firm's plan and a lender | Survey, costs, rent effect, lender products |
| Hold, sell or transfer with the tenant in place | Landlord, with independent valuation | Record, net yield, capital plan, value range |
| Rent, given the landlord's strategy | Firm within policy and law | Market data, tenant history |
| Which alerts need action | Building scientist sets bands; home agent applies them | Season, building type, sustained readings |
| Sustain a tenancy in difficulty | Household support | Payment pattern, circumstances |
| Where to add technicians and turn crews | Firm | Density, failure forecasts, notice pipeline |

---

## 5. Where the firm's capability sits

Its points of presence:
- **In the home:** first through what is already there (smart meter data with the tenant's consent, connected boilers, the tenant's phone camera); the technician once a year; devices only where the risk model says they pay, on cellular or low-power networks because many scattered homes have no landlord broadband [experience, practitioner].
- **In the money:** the wallet, with a regulated partner. The repair reserve shown as the landlord's own money, in their own account view.
- **In the tenant's phone:** the member app and voice line, which follow the household from home to home; later the tenant's own agent, through the listing interface.
- **In the landlord's channel:** one payment, a live view, a policy screen, a named person.
- **In lenders' and capital partners' processes:** the record as evidence for remortgages and upgrade finance; a pipeline of tenanted homes for funds.
- **In counterparties' systems:** registers, deposit schemes, the landlord database, HMRC, engineers' apps, council licensing.

Step 3c's four forms, by segment:

| Segment | Shared system | Agents in their tools | Embedded people | Firm runs their function | Why |
| --- | --- | --- | --- | --- | --- |
| **Accidental** | Simple view | No | Asset partner, by phone and video | **Fully** | They want an income, not a tool |
| **Small portfolio** | Portfolio view, policy | Sometimes: their accounting software | Asset partner, yearly review | **Yes**, within their policy | They want control of rules, not cases |
| **Professional** | Yes | **Yes**, both ways | Account lead, quarterly | Partly; they keep strategy | They have systems and want an interface |
| **Institutional** | Theirs, not the firm's | **Yes**, inside their property system | **Yes**: an operations lead on site some days | **Often**, to their service levels | They own the platform and brand; they buy capability [seen: outsourced operations exist] |
| **Leaving** | Record and valuation | No | Exit desk | Runs the sale with the tenant in place | They want out without a void |
| **Overseas** | Yes | No | Light | Yes | Nothing to do is the product |

The pattern [reasoned]: the smaller the client, the more the firm *is* their property function. The larger the client, the more the firm is a layer *inside* their function. So the firm must run on other people's platforms as well as its own. The exit route joins the two ends: homes leave the first group and arrive in the second without leaving the firm.

---

## 6. The boundary choice

| Option | For this firm | Strength | Weakness |
| --- | --- | --- | --- |
| **Own the platform and the record** | Closed home record, ledger, policy engine, agents | Controls where all parties meet | A record nobody else reads has little value; the state's database will hold the obligations layer anyway [reasoned, builder] |
| **Build on a platform** | A property management vendor, agents on top | Fast | The vendor owns the record. Wallet, telemetry and policy do not fit a system built for case handling [reasoned] |
| **Portable agent layer** | Agents in any client's system | Right for institutional clients | Owns little that lasts |
| **Open record, owned flows** | Publish the record schema; own the wallet, the work orders, the renter network and the loss data | Lenders and buyers can rely on a record that is not captive; the flows are where money and supply pass | A rival can run the same standard; the firm must win on operation and price |

**The choice: publish the record as an open standard; own the flows (money through the wallet, work through the network, tenants through the membership) and the aggregate loss data that prices risk; rent the rails; be a portable layer for institutional clients** [reasoned].

This moves from the first draft, which said "own the record". The builder's argument holds: a record is valuable only if others read it, and others read only what they do not have to trust a rival to keep. What should not be given away is the thing that prices the risk. That is the aggregate data across thousands of homes, not any one home's history.
- Money rails, identity, devices, deposit protection and insurance capacity are commodities or regulated. Partner for them.
- Institutional clients will not move onto a smaller firm's platform. Go to them.
- Be the best submitter to the state's landlord database, so its version is a subset of the open record.

**Who else is in the picture:**

| Player | Holds | Threat | Stance |
| --- | --- | --- | --- |
| **Portals** | Tenant attention; the "portal toll" [seen: counter-review synthesis] | Move into management or the tenant relationship | Use for demand; lean on them less through members and tenants' agents, which need trusted data, not attention |
| **Roll-ups** (Dwelly and others) | Clients; a fast level 1 engine [seen: 300 staff, 17,000+ homes, company figures] | Win the clients first and add level 3 later | Compete on what is sold; sell them the annual service; run the open standard with them; buy the books they do not want; be open to being bought |
| **Property software vendors and landlord platforms** | Agents' and self-managers' records | Become the shared system | Invite them to adopt the open schema; partner for self-managers buying the network |
| **Banks and buy-to-let lenders** | Accounts, mandates, lending | Bundle "landlord accounts" with basic management | Main partner from 2027: the record as evidence, upgrade finance, the wedge into landlords at remortgage |
| **Insurers** | Capital, claims data | Price the same risks without running homes | Carry the tail from day one; later, a managing general agent role [conjecture] |
| **Capital partners** (funds, single-family rental) | Money looking for homes | Buy without the firm | Supply them underwritten, tenanted homes; run those homes |
| **Device and energy firms** | Telemetry, meter data [seen: environmental sensors widely used by social landlords] | Sell straight to landlords | Read their data; buy devices only where they pay; own the interpretation and the action |
| **The state** | Landlord database (launch reported for 15 December 2026 [seen, law firm report]), energy register, councils, ombudsman | The database grows into the home record | Make the state's version a subset of the open record |

The contest to 2035 is between the roll-up that owns the clients and the firm that owns the flows of money, work and tenants. A roll-up can add sensors later. It is harder for it to change what it sells, because its branches and fees are built around today's service [reasoned].

---

## 7. The organisation that follows

### 7.1 The agent architecture

Level 1 had an orchestrator per tenancy and per repair. Level 3 changes the unit [reasoned]:

| Agent | One per | Sole writer of | Job |
| --- | --- | --- | --- |
| **Home agent** | Home | Condition, band, obligations, access, occupancy | Watch data and clocks; rank alerts; mark a quiet home "unknown"; open and close work; plan the turn during notice |
| **Portfolio agent** | Landlord | Policy, plan, contract | Apply policy; draft the asset plan; pay the yield contract; ask only what policy does not cover; ask about exit at each review |
| **Wallet agent** | Home | The home's money | Collect, pay, reserve, withhold tax, file records |
| **Member agent** | Household | The tenant interface and passport | Reports by text, video or voice; status; triage; access bookings; vulnerability flags. It follows the household when they move within the network |
| **Market agent** | Region | Listings and matches | Publish verified listings to members, portals and tenants' agents; match inside notice; take offers at the advertised rent |
| **Network agent** | Region | Rounds, turns and contractor work | Plan annual rounds with evening and Saturday slots; schedule paired electrical visits; run turn crews; dispatch; pay on evidence; track capacity |
| **Capital agent** | Firm | Underwriting bands and transfer pipeline | Apply the actuary's rules at entry; prepare transfer packs for valuers and capital partners |
| **Counterparty agents** | Counterparty | Their cases | Registers, schemes, HMRC, councils, freeholders, insurers, lenders |
| **Verifiers and governance** | Output type; firm | Nothing | Independent checks on other models; budgets, limits, breakers, fairness, client-money and privacy audits |

Level 1's constitution carries over. Five clauses are added:
1. **Home data is for the home's condition and safety only,** never for judging how a tenant lives.
2. **Prevent first.** Spend that lowers expected future cost or harm is approved within policy, even when nothing has failed.
3. **A missed promise to a tenant is paid for automatically,** without a claim.
4. **No conflicted advice.** The firm never advises a landlord to sell where it earns from the sale without saying so, and every tenanted transfer has an independent valuation.
5. **Membership never overrides fairness.** Priority for members works only among applicants who meet lawful, explainable criteria, and membership is open to anyone.

### 7.2 The people, by kind of need

| Kind of need | Role at level 3 | Change from level 1 |
| --- | --- | --- |
| **1. Purpose** | Owners and board, with an independent member for tenants | Same |
| **2. Definition of good** | Building scientist (alert bands, "resolved"); money and legal lead; **fairness lead** close to referencing; a **risk actuary and underwriter** owning bands and pricing tests | The actuary and underwriting are new: the firm now carries risk |
| **3. Answerability** | Officers for client money, safety, complaints, privacy, tax; solicitor partner for possession | Privacy grows with home data |
| **4. Capability gaps** | Judgement desk: hazards, hardship, thin-file affordability, stuck third parties, adjusters | Smaller than level 1, larger than the first draft: referencing judgement stays |
| **5. Client demand** | **Asset partners and exit desk**, one per 600 landlords at launch widening to 1,200; plans, upgrades, yield contracts, hold or transfer | Level 1's patch leads, with products to advise on |
| **6. Physical world** | **Employed technicians** on planned rounds; paired electricians; **an own turn crew**; contractors for larger work; a few hosts | New: the annual visit and the turn are where information is born and voids are lost |
| **7. Duty to non-clients** | Household support; **council and freeholder liaison** | Larger: rent assurance gives the firm a stake in sustaining tenancies, and councils need named people |
| **Network and scaffolding** | Network managers; builders; human checkers while evidence builds; an apprenticeship scheme | Fewer contractors to manage; more builders early |
| **Permanent insurance** | Night on-call rota; complaints team of three | Kept, and complaints kept at three |

**The rhythm** follows the home and the seasons, not the inbox [reasoned]. Agents keep conditions true continuously and route exceptions within minutes. Daily: open hazards, "unknown" homes, breached clocks and breaker trips. Weekly: a regional board on technician, electrician and turn-crew capacity, the notice pipeline and turn days. Monthly: each landlord's position and contract payment; asset partners call those with a decision due. Quarterly: tenant video round; model releases through the harness; the actuary reprices bands against claims. Each October: a winter readiness campaign. Each summer: planned works and energy upgrades. Yearly: each home's service, each landlord's policy and exit review, and the board's review of the constitution and the definition of good. For a newly bought book: a 90-day conversion (section 9.2).

### 7.3 Headcount sketch

Reference book: 5,000 landlords, 7,500 homes. Inside the firm, full-time equivalents. **All [conjecture].**

| Role | 2027 | 2030 A | 2030 B | 2035 A | 2035 B |
| --- | --- | --- | --- | --- | --- |
| Owners, board, accountable officers | 6 | 6 | 6 | 5 | 6 |
| Evaluator governors (incl. actuary, underwriter, fairness lead) | 5 | 4 | 5 | 3 | 4 |
| Judgement desk | 14 | 7 | 10 | 3 | 6 |
| Household support | 6 | 5 | 6 | 3 | 5 |
| Asset partners and exit desk | 8 | 6 | 7 | 3 | 5 |
| Council and freeholder liaison | 3 | 3 | 3 | 2 | 3 |
| Network and field planning (incl. devices) | 7 | 4 | 5 | 2 | 4 |
| Money, payee controls, tax | 4 | 2 | 3 | 1 | 2 |
| Complaints | 3 | 3 | 3 | 3 | 3 |
| Growth, lender and capital partnerships, book conversion | 6 | 4 | 5 | 2 | 3 |
| Renter network and listing interface | 2 | 2 | 2 | 1 | 1 |
| Builders | 16 | 7 | 9 | 2 | 4 |
| Human checkers (scaffolding) | 4 | 0 | 2 | 0 | 1 |
| Night on-call rota | 2 | 2 | 2 | 2 | 2 |
| **Inside the firm** | **86** | **55** | **68** | **32** | **49** |
| *Field: technicians (gas, heat, small works)* | *8 (incl. a bought heating firm)* | *20* | *20* | *18* | *20* |
| *Field: electricians, paired visits* | *1* | *3* | *3* | *3* | *3* |
| *Field: turn crew* | *4* | *12* | *12* | *12* | *12* |
| *Field: hosts, clerks, surveyors* | *24* | *6* | *10* | *3* | *6* |

| Model, inside the firm | 2027 | 2030 (A / B) | 2035 (A / B) |
| --- | --- | --- | --- |
| Traditional firm | 140–160 | 140–160 | 120–150 |
| Level 1 | 81 | 53 / 72 | 35 / 60 |
| Level 3, first draft | 79 | 44 / 60 | 26 / 43 |
| **Level 3, revised** | **86** | **55 / 68** | **32 / 49** |
| Dwelly, reference | about 88 per 5,000 homes in 2026 [seen, company figures] | — | — |

Institutional mandates add about 3 to 6 inside people per 10,000 homes by 2030, mostly embedded operations leads [conjecture].

**What drives the numbers** [reasoned]:
- **The revision raised the count.** Council liaison (3), complaints kept at three, a fairness lead and judgement for thin-file referencing, underwriting, and the exit desk outweigh what the builder's moves remove. The builder's floor of 12 to 18 is not reached: officers, the night rota, complaints, councils and household support alone come to about 15, before anyone does the work.
- **2027 and 2030 A are no better than level 1.** Homes are underwritten and recorded one visit at a time, and the builders are more. The inside gain is deferred.
- **The gap opens because work disappears, not because it gets faster.** Approvals, document checks, inspections and the search for tenants no longer exist. That is why level 3 beats level 1 by more in landscape B (49 against 60 in 2035) than in A (32 against 35). Removing a task does not depend on agents getting cleverer. **This is still the strongest argument for level 3.**
- **The field changes in kind and grows.** Twenty technicians, three electricians and a turn crew of twelve replace contractor spend on the annual round, small repairs and turns. Sixteen technicians could cover the annual round but not much reactive work as well [reasoned, practitioner]; the first draft double-counted them. About 11 technicians cover 7,500 visits a year at three to four a day with failed first appointments; the rest take in-house small repairs. Counting the field as overhead misleads.
- **Inside headcount is the wrong headline by 2035.** The builder is right that the measure that matters is **margin per home on the risk carried**, and turn days, and device uptime.

---

## 8. Economics

**Everything in this section is [conjecture].** Average rent £1,350 a month (£16,200 a year), as in level 1. Prices exclude VAT. The base case now assumes reactive maintenance falls 10 to 15% by 2035, as the practitioner advises. The first draft's 25% is shown as upside.

### 8.1 What the landlord pays today, and what is sold

A typical managed home costs the landlord, outside the mortgage: management at 12% (about £1,950), repairs (about £1,200 to £1,600), certificates (about £200 to £300), and a void of three weeks every three years or so (about £300 a year). That is **about £3,600 to £4,200 a year, with high variance**, plus arrears risk that has grown since section 21 went. The variance is much of the hassle.

| Product | Price | Notes |
| --- | --- | --- |
| **Fixed-cost home, banded** | £230 / £270 / £330 a month in 2027 for bands 1 / 2 / 3; average about £270 | Band set at the first visit; known defects into the capital plan |
| Named-person tier | +£25 a month | For accidental landlords |
| **Rent assurance** | 5–7% of rent, by tenancy | Up from 3–4% in the first draft, for a section 8 world with slow courts; insurer carries the tail |
| **Net-yield contract** | Fixed-cost home + rent assurance + void cover, about 27–30% of rent; landlord receives a floor and half of any saving below expected cost | Example: on £16,200 rent, a floor of about £11,500 a year (£960 a month) before mortgage and capital items, against an expected £12,000 to £12,600 today with variance and arrears risk. The landlord pays about 5% of expected income for certainty |
| **Repair reserve** | Set by the asset plan | The landlord's money in their own wallet view, not a deduction |
| **Energy upgrade, financed** | Works at cost plus a disclosed fee; lender finance repaid from the wallet | Wave of work to October 2030 |
| **Tenanted transfer** | About 1% of sale price, paid by the buyer, disclosed; independent valuation | The home stays under management at institutional rates |
| **Institutional operations** | £25–£45 a home a month | By scope |
| **Network for self-managers** | £20–£30 a home a month | Annual service, compliance promise, dispatch |
| **Renter network** | Free to tenants | Paid from landlords' fees; required by the Tenant Fees Act |

At an average £3,240 a year in 2027 the fixed-cost home is below the landlord's £3,600 to £4,200 today, with the variance removed. Underwriting means the worst third pays more and does not sink the pool [reasoned, practitioner]. The net-yield contract is dearer in expected terms and is sold to the landlords who value certainty most: accidental, overseas and nervous landlords.

### 8.2 Cost per home, fixed-cost home

Inside people at about £65,000 loaded per full-time equivalent.

| Per home a year | 2027 | 2030 A | 2030 B | 2035 A | 2035 B | 2035 D |
| --- | --- | --- | --- | --- | --- | --- |
| Inside people | £745 | £477 | £589 | £277 | £425 | £277 |
| Compute, verification, engine | £300 | £170 | £200 | £100 | £150 | £100 |
| Annual service, paired electrical, certificates | £220 | £190 | £200 | £170 | £180 | £170 |
| Maintenance and turns (the risk pool) | £1,300 | £1,250 | £1,270 | £1,170 | £1,200 | £1,170 |
| Devices and data access, amortised | £40 | £35 | £35 | £30 | £30 | £30 |
| Insurance, compliance promise, tenant credits, fraud | £120 | £110 | £110 | £100 | £100 | £100 |
| Acquisition | £180 | £120 | £140 | £90 | £110 | £110 |
| **Total cost** | **£2,905** | **£2,352** | **£2,544** | **£1,937** | **£2,195** | **£1,957** |
| **Price (average across bands)** | **£3,240** | **£2,880** | **£3,060** | **£2,400** | **£2,700** | **£2,150** |
| **Margin** | **10%** | **18%** | **17%** | **19%** | **19%** | **9%** |

Upside: if the first draft's 25% maintenance fall happens, the risk pool is about £1,010 in 2035 and margin in landscape A rises to about 26%.

Maintenance falls in the base case because of underwriting (known defects priced or excluded), planned replacement, small fixes on the annual visit, early detection of leaks, and per-home contracts. It does not fall much on turnover, white goods and misuse, which the practitioner puts at about half of reactive spend [experience]. Turns move in-house, which costs more inside the pool but cuts void days. This line is still the number the whole model is most sensitive to, and it is the first thing tested (section 9.4).

Cost per client at 1.5 homes: about £4,400 in 2027, £3,500 in 2030 A, £2,900 in 2035 A, £3,300 in 2035 B.

### 8.3 By landscape, and where the profit comes from

| | A: capability compounds | B: plateau | D: price collapse |
| --- | --- | --- | --- |
| Price | Rivals copy the management layer; price falls towards cost plus risk margin | Holds longer; level 1 rivals stay dearer | Basic management nearly free inside portals, banks and landlord software |
| Margin on the fixed-cost home | About 19% | About 17–19% | About 9% |
| Profit from | Risk spread on yield contracts, energy upgrades, institutional operations including transferred homes | The same, plus a management layer still paid for | The physical network, turns and carried risk, which cannot fall to zero because repairs and defaults are real |

Where the profit comes from [reasoned]:
1. **The risk spread.** The firm sells certainty (a monthly income, fixed cost, a compliance promise) and buys uncertainty (repairs, arrears, voids). It wins if underwriting at entry and its loss data make its expected cost lower than a rival's price. The spread is thinner than the first draft hoped. Measured as **margin per home on the risk carried**, it is the number the board watches.
2. **The energy upgrade wave.** About half the market must reach EPC C by October 2030. The firm holds the survey, the plan, the network and, through lenders, the finance.
3. **Institutional operations, fed by the exit route.** Steady fees, low acquisition cost. Each tenanted transfer keeps a home the firm would otherwise lose. If 3 to 5% of the book's homes transfer each year, that is about 225 to 375 homes a year in the reference book, each bringing a transaction fee and a long contract [conjecture].
4. **Not** from management fees, hidden maintenance commission or tenant fees.

The danger is that of any risk carrier: a bad winter, one boiler model failing across many homes, adverse selection that underwriting misses, or slow courts lengthening arrears. That needs a reserve, an insurer on the tail from day one, and an actuary not paid on volume.

---

## 9. How it is built from 2027

### 9.1 What exists, and what must be built

**Exists to use** [seen]: open-banking data and payments, with commercial variable recurring payments in a first, narrow wave since 2 June 2026; open-banking referencing; digital identity providers for right to rent checks since 2022; smart meters in about two-thirds of homes; connected boilers; environmental sensors, smart thermostats and smart locks, common in social housing; public registers (energy certificates, Land Registry, Gas Safe); the landlord database from late 2026; voice and text agents; rent guarantee insurance, deposit replacement and rent reporting to credit agencies.

**Must be built:** the home record schema, published; the obligations ledger; the policy engine; the wallet, with a banking partner holding client money per home; the home-centred agent architecture with verifiers, harness and governance; underwriting rules and bands; the annual service operation with paired electrical visits; the turn crew; per-home contractor contracts; the pricing model and yield contract with an insurer; the renter network and listing interface; the transfer process with a capital partner and independent valuers.

### 9.2 The first wedge

The first draft's wedge was the annual gas check. The builder showed it is too weak as a pitch: gas checks are bought on price and will shrink as heat pumps spread. The practitioner showed the annual visit itself works and is where information is born. Both hold. So the **visit stays as the delivery, and the pitch moves to the moments when a landlord must decide** [reasoned]:

- **The decision moment, through lenders.** EPC C by 2030, a remortgage, registration on the landlord database, a wish to sell. Sell "EPC C done, financed from the rent, with your income fixed after" through two buy-to-let lenders and brokers in 2027. The first visit is the energy survey, the underwriting survey and the start of the record.
- **The proof site, in build-to-rent.** Run one build-to-rent scheme from year one, where density, owned doors and one building system exist already. The record, policy engine, keyless access and damp control run at full strength there and give the evidence that sells to single homes [experience, practitioner].
- **The density, by buying a book** of 1,500 to 2,500 homes in one dense city region. Do not migrate its process. **Convert each landlord inside 90 days**, starting with something the landlord gains: payout on a fixed day, a compliance gap cleared at the firm's cost, the reserve shown as their own money. Most churn after a deal comes in those 90 days [experience, builder]. Each home's record and band still build at its next annual visit.
- **The annual service** stays on sale to self-managers and other agents as the recurring product. Heat pumps need a yearly service too, so the visit survives the change of heating [reasoned].

**Technicians are the bottleneck.** Gas-and-electric engineers are scarce and poached [experience, both reviewers]. So in 2027 buy a small heating firm in the region and start an apprenticeship scheme, rather than assuming 20 can be hired.

### 9.3 What makes clients adopt

- **Accidental landlords:** one payment a month they can count on; fear of new rules and penalties; a trusted named person.
- **Small portfolio:** the EPC C deadline with finance attached; Making Tax Digital reaching £30,000 and then £20,000; evidence that the banded price beats their last three years; a reserve that stays theirs.
- **Leaving landlords:** a sale with the tenant in place, no void and no fight.
- **Professional and institutional:** an interface, audited service levels, lower variance, and a supply of tenanted homes.
- **Tenants:** fix times that are kept, credits when they are not, and a move within the network in days without a second deposit.
- **Lenders:** a record that proves EPC C and condition, and finance that is repaid from a wallet they can see.
- **Contractors:** steady work in a dense patch, 48-hour payment, no wasted trips.

### 9.4 Sequence to 2035, and how it gets clients

| Period | Steps |
| --- | --- |
| **2027** | One dense region plus one build-to-rent scheme. Buy one book; 90-day conversion. Publish the record schema. Two buy-to-let lenders signed. Buy a heating firm; start apprentices. Annual service with underwriting at the first visit. Banded fixed-cost home. Wallet with a banking partner. Insurer signed for the tail. Renter network inside the firm's homes (passport, carried deposit, priority) |
| **2028** | Net-yield contract piloted on underwritten homes of the first book, insurer on the tail. Listing interface for tenants' agents. Tenanted transfer with a first capital partner. Rent assurance priced per tenancy. Own turn crew in the first region |
| **End 2028: the gate** | Measure three numbers on comparable homes over two years: reactive spend per home, device and data uptime, turn days. **If reactive spend has not fallen by 10%, stop carrying risk.** Sell the record, the service and the operation; leave the risk to insurers; the firm becomes a level 3 operator without the risk spread |
| **2029–2030** | Energy upgrade wave through lenders. Second and third regions, each by buying a book and building density. Renter network open beyond the firm's homes. Per-home contracts as default. Most scaffolding removed on evidence |
| **2031–2033** | Price risk in-house, perhaps as a managing general agent with reinsurance. Record accepted by most buy-to-let lenders and some conveyancers. Institutional operations, fed by transfers, a large line |
| **2034–2035** | Decent Homes readiness for every home. Tenants' agents a normal channel. Option to license the engine |

Client routes [reasoned]: **build** (self-managers through the annual service; institutions by direct sale); **buy books** (fastest route to density and data; prefer retiring owners in the chosen region); **partner** (buy-to-let lenders for the decision moment, upgrades and the record; capital partners for exits; accountants for tax; landlord associations; insurers); **tenants** (members who bring the next landlord, and the cheapest acquisition there is [experience, builder]); **platform** (sell the annual service and the open standard to other agents and roll-ups).

---

## 10. What would make this wrong, and the stress test

### 10.1 What would make this wrong

1. **Maintenance does not fall even 10%.** The gate at the end of 2028 catches it. The firm then stops carrying risk and runs as an operator.
2. **Adverse selection beats underwriting.** The worst homes join first [experience, practitioner]. Bands and capital-plan exclusions must hold; if not, the pool loses on the worst third.
3. **Rent assurance losses in a section 8 world.** Slow courts and long arrears make the yield contract dearer than landlords will pay. Lead with household support; price per tenancy; keep the insurer on the tail.
4. **Technicians and turn crews cannot be found.** The field is now the core. Without the apprenticeship and a bought heating firm, density does not pay.
5. **Homes go quiet.** Device and data uptime, not consent, is the risk [experience, practitioner]. "Unknown" must trigger action, or the continuous conditions are fiction.
6. **The exit route is seen as conflicted.** If landlords think the firm talks them into selling, trust in the whole firm falls. Independent valuation and disclosure are the guard.
7. **The open standard is taken over** by the state's database, a portal or a bank, and the flows follow it.
8. **Correlated risk.** A bad winter or one failing boiler model hits the pool in a way level 1 never faced.
9. **Roll-ups reach level 3 first,** funded by the clients they already hold.

The first draft's "landlords will not hand over standing authority" is dropped as a main risk. Most agreements already carry a spend limit. What landlords resist is cash held back, which the visible reserve answers [experience, practitioner].

### 10.2 The stress test, applied now

| Constraint | Status | Effect on the design |
| --- | --- | --- |
| **Renters' Rights Act phase 1**: section 8 only, periodic tenancies, one section 13 increase a year, no bidding above advertised rent, one month in advance at most, no blanket bans on families or benefit claimants | In force since 1 May 2026 [seen, level 1; practitioner] | Fits, with changes. Rent strategy runs yearly by rule. Periodic tenancies make the renter network more valuable. Offers at advertised rent only. Affordability judgement must be explainable; rent assurance priced higher |
| **Access to the home** | 24 hours' written notice for inspection [seen: Landlord and Tenant Act 1985, s.11, cited by the practitioner] | Access is a booking with notice served automatically; the tenant picks the slot |
| **Gas and electrical safety** | Gas check yearly, up to two months early keeping the date [seen: 2018 amendment]; electrical check at least every five years by a qualified person [seen: Electrical Safety Standards regulations 2020] | Planned rounds work; electrical visits paired every fifth year |
| **Landlord database; ombudsman** | Database launch reported for 15 December 2026; ombudsman dates conflict (late 2026 or 2028) [seen] | Feed the database automatically. Complaints team stays at three because volume will rise |
| **Council licensing** | Selective and additional licensing vary by borough [seen, general knowledge] | Council liaison as a named role |
| **Awaab's Law in private renting; Decent Homes from 2035** | Enacted, timescales to be set; Decent Homes timing to be consulted on [seen] | Raise the value of damp control and the 2035 plan; alert bands must be defensible |
| **EPC C from 1 October 2030** | Confirmed January 2026; E until then; homes rated C before October 2029 count until the certificate expires [seen] | Creates the upgrade wave and the lender wedge |
| **Making Tax Digital; Non-Resident Landlord Scheme** | £50,000 / £30,000 / £20,000 from 2026, 2027, 2028; agents withhold for overseas landlords [seen] | Side effects of the wallet; an officer signs |
| **Client money protection and redress** | Mandatory [seen, level 1] | The wallet sits in client accounts with a regulated partner; one account per home and a visible reserve must be agreed with the bank and scheme |
| **Is the fixed-cost home or yield contract insurance?** | Not checked. A fixed fee for uncertain future repairs, or a guaranteed income, may count as insurance under financial services rules [reasoned; needs legal advice] | **Still the biggest regulatory question.** Route: the firm does the work; an insurer carries risk above a band from day one; the firm acts as appointed representative, later managing general agent |
| **Indemnifying fines** | Paying a landlord's civil penalty or rent repayment order may be uninsurable or unrecoverable [reasoned, practitioner; needs legal advice] | The compliance promise covers putting it right, the firm's fee and capped losses, not fines |
| **Selling homes** | Acting in a sale is estate agency work with its own duties [seen, general knowledge: Estate Agents Act 1979; not checked in detail] | The exit desk follows estate agency rules; independent valuation; conflicts disclosed |
| **Deposits** | Each tenancy's deposit must be protected and its information served [seen, general knowledge] | A carried deposit is released and re-protected on each move, or replaced by an approved product; the member sees one balance |
| **Tenant Fees Act 2019** | Most tenant fees banned [seen, general knowledge] | The renter network is free to tenants and paid from landlords' fees |
| **Home data and automated decisions on tenants** | Meter and sensor data are personal data; access to smart meter data needs the bill payer's consent; rules on solely automated significant decisions recently amended; detail not checked [reasoned] | Purpose limits; a privacy officer; a route for tenants who refuse; stated reasons, review on request and a fairness audit on referencing |
| **National digital ID** | Mandatory use for citizens dropped in January 2026; later reports say the scheme was dropped [seen, not confirmed at source] | The passport rests on existing identity providers and open banking |
| **Payment rails** | Commercial VRP first wave since June 2026, narrow sectors [seen] | Rent by mandate may take years. Standing orders and Direct Debit stay as fallback |
| **Registration, courts, professional standards** | Gas Safe registration; reserved litigation; RICS AI standard since March 2026 [seen, level 1] | Technicians registered; possession stays with a solicitor; sampling, not per-output review |
| **Insurers' view of AI** | No wording found [level 1] | Bigger here, since the firm carries risk. A track record by home is the answer |
| **Contractors and freeholders** | Per-property contracts exist in social housing [seen, general knowledge]; freeholders control blocks and communal doors | Own technicians and turn crew first; a few trusted firms per region; block issues stay a case |

### 10.3 What survives

The core survives: the home record, the wallet, standing policy, the annual visit and the continuous conditions. No rule requires an inspection, a paper reference or a case-by-case approval. The rules push the other way: hazard clocks, a register of landlords, a dated energy standard, digital tax records and tenants free to move [reasoned]. The renter network and the exit route also survive; both are made more valuable by the Renters' Rights Act.

Four things change it:
1. **The fixed-cost home and the yield contract need an insurer from the start,** who takes the tail. The firm's margin depends on the terms its data can win.
2. **The physical world stays physical** in scattered stock: access, turns and check-out. The design runs them better; it does not remove them.
3. **Home data is partial.** Some homes go quiet and some tenants refuse. The design must work with "unknown" as a normal state.
4. **Rent by mandate is not ready in 2027.** The wallet starts with ordinary payments and moves as the rails mature.

The hardest constraint is not a rule. It is whether repair risk can be priced well enough to sell certainty at a profit. The design meets it by underwriting every home, starting where it is easiest to prove (build-to-rent and one dense region), putting an insurer on the tail, and setting a hard gate at the end of 2028.

---

## Sources checked for this paper

- GOV.UK, [Improving the energy performance of privately rented homes: government response](https://www.gov.uk/government/consultations/improving-the-energy-performance-of-privately-rented-homes-2025-update/outcome/improving-the-energy-performance-of-privately-rented-homes-government-response-html) (January 2026), with [Pinsent Masons' summary](https://www.pinsentmasons.com/en-gb/out-law/news/epc-reforms-mees-private-rented-property-confirmed).
- GOV.UK, [Making Tax Digital threshold to £20,000 from April 2028](https://www.gov.uk/government/publications/making-tax-digital-for-income-tax-self-assessment-reducing-the-mandation-threshold-from-30000-to-20000-from-april-2028/reduction-of-the-mandation-threshold-from-30000-to-20000-from-april-2028) and [one year until launch](https://www.gov.uk/government/news/one-year-until-making-tax-digital-for-income-tax-launches).
- GOV.UK, [Renters' Rights Act roadmap](https://www.gov.uk/government/publications/renters-rights-act-2025-implementation-roadmap/implementing-the-renters-rights-act-2025-our-roadmap-for-reforming-the-private-rented-sector); [MHCLG blog on Decent Homes](https://mhclgmedia.blog.gov.uk/2026/02/05/decent-homes-standard); [Osborne Clarke on phase 2](https://www.osborneclarke.com/insights/renters-rights-act-phase-2-introduces-landlord-database-and-rent-dispute-reforms-england). The 15 December 2026 database date is from a law firm report seen in search, not confirmed at source.
- [Open Banking Limited on the commercial scheme](https://www.openbanking.org.uk/insights/an-industry-first-the-uks-new-commercial-open-banking-scheme); [Lewis Silkin on the UK Payments Initiative launch](https://www.lewissilkin.com/insights/2026/06/11/uk-payments-initiative-launches-new-open-banking-recurring-payments-scheme-102n1ql).
- [GOV.UK digital ID explainer](https://www.gov.uk/government/publications/digital-id-scheme-explainer/digital-id-scheme-explainer); [The Register, January 2026](https://www.theregister.com/2026/01/14/uk_digital_id_climbdown/); [Full Fact tracker](https://fullfact.org/government-tracker/digital-id/).
- Cited by the builder review, not rechecked here: [DESNZ smart meter statistics](https://www.gov.uk/government/collections/smart-meters-statistics) (about two-thirds of meters smart and in smart mode, end 2025); [NRLA Q2 2026 survey](https://www.nrla.org.uk/news/more-than-quarter-landlords-selling-as-perfect-storm-hits); English Private Landlord Survey 2024 (31% reducing, as reported in search).
- Cited by the practitioner review, not rechecked here: Gas Safety (Installation and Use) (Amendment) Regulations 2018 (two-month early window); Electrical Safety Standards in the Private Rented Sector (England) Regulations 2020 (five-yearly check); Landlord and Tenant Act 1985, s.11 (24 hours' notice); Renters' Rights Act bans on blanket refusals of families and benefit claimants.
- From the earlier run, not rechecked: Dwelly's figures (step 3c); Renters' Rights Act phase 1, Non-Resident Landlord Scheme, RICS AI standard (example-lettings).
- General knowledge, not checked: Tenant Fees Act, Estate Agents Act duties, deposit protection per tenancy, rent reporting to credit agencies, council licensing, sensors in social housing, per-property repair contracts, whether a fixed-cost maintenance product or a guaranteed income is insurance, whether fines can be indemnified, data protection detail for home data. Every price, cost and headcount is a guess. The maintenance saving is still the number everything rests on, and nothing here measures it; the end-2028 gate is designed to.
