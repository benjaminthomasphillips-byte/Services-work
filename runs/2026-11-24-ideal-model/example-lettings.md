# Worked example. Lettings and property management in England, designed agent-first

Draft by Claude, 24 November 2026. Revised the same day after a practitioner review (`example-lettings-review.md`). One author, no sub-agents. It applies the design in `step-3b-the-agent-enterprise.md` to one service. It uses the engine and task contract from `step-1-the-engine.md`, the landscapes from `step-3-building-the-firm.md`, and the list of work in `../2026-11-23-rollup-org/design/inventory-B.md` (lines I1 to I28 and the back office, J).

Labels:
- **[seen]** exists somewhere today;
- **[reasoned]** follows from logic;
- **[conjecture]** plausible towards 2035.

Method, from step 3b: design the firm as all software and agents, walk it through real events, and add people only where a function fails without one. Rules, insurance and courts appear as facts that show where people stand, and as a stress test in section 8. They do not set the design. Domain facts were checked on 24 November 2026 (sources at the end). Volumes start from the inventory's guesses for 600 tenancies, scaled up, and were corrected after review for realistic turnover.

**What changed in revision.** The reviewer's main charge is fair: the first draft modelled the firm as a set of cases, but the work is mostly a set of people who do not reply. Landlords who will not approve, contractors who will not come, keys nobody can find. This version adds those as design problems with structural answers, adds seven missing event types, fixes the turnover error, pushes further on viewings, inspections, triage, voice and sensors, and rebuilds the headcount and economics. The section "Review and response" at the end lists every point.

---

## 1. The service as products

### 1.1 The clients
The reference firm serves about **5,000 landlords** with about **7,500 managed homes** [conjecture: 1.5 homes each], plus about **1,250 let-only instructions** a year. Four segments [conjecture on shares]:

- **Accidental and single-home landlords** (about 55%): want it all to just work; fear breaking a rule they did not know existed; want to reach a person when something breaks.
- **Small portfolio landlords**, 2 to 10 homes (about 35%): want low cost, clear numbers and control of big decisions; fear voids, arrears and repair bills.
- **Larger landlords and build-to-rent operators**, 10 or more homes (about 8%): want data, accept rules, and want an interface their own systems or agents can call.
- **Overseas and absent landlords** (about 5%, overlapping): want tax handled and nothing to do. The firm must withhold tax for them by law (section 3.17).

A second population matters as much: about 7,000 **tenant households**. They are not the client, but they are the people the service touches most and the law now protects most [reasoned]. The design treats them as a party the firm owes duties to.

A third population decides whether the promise can be kept at all: about **400 to 600 contractors**, mostly sole traders, plus freeholders and managing agents for the flats [reasoned]. The firm does not employ them and cannot order them. It has to be the agent they prefer to work for.

### 1.2 The promise
One sentence to build against: **"Your homes stay legal, let and paid, and every repair is fixed to a stated time, with live status you can see."**

Each part is checkable: certificates and protections in date, shown live; rent paid out on a stated day; each repair class fixed to a published time, or explained. It is a subscription to a maintained condition (step 3, choice 1), and fits lettings well because statute and dates define most of the condition [reasoned].

The review showed the promise has two hidden preconditions, which now sit in the landlord contract [reasoned]:
1. **The firm may act on repairs without asking** inside a pre-agreed spend matrix, funded by a float held per home. Without this, the repair clock depends on the slowest landlord.
2. **The firm controls access**: a key or code for every home, logged. Without this, the repair clock depends on whoever has the key.

A landlord who will not accept both gets a weaker promise, priced and labelled as such.

### 1.3 The work as case types
The inventory's 28 lettings lines, plus what the review showed was missing, collapse into 22 case types. A case type is one job from trigger to closure, not a row of the table. A repair is one job crossing six inventory lines.

Volumes were corrected after review. Managed tenancies turn over at about 25 to 35% a year [experience, per reviewer], not the near 60% the first draft implied. This version uses 30%, so about 2,250 new managed lets a year, plus 1,250 let-only.

| # | Case type | Inventory lines | Volume a year (scaled, guess) | Kind |
| --- | --- | --- | --- | --- |
| 1 | Landlord onboarding: identity, title, consents, mandate, spend matrix, float, keys | I2 | 700 new landlords (about 1,000 homes) | Routine, with fraud checks |
| 2 | Property baseline: certificates, licence, energy rating, inventory, condition record, access record | I17 (first time), I9 part | 1,000 | Routine, with diagnostic gaps |
| 3 | Marketing and applicant handling | I3, I4 | 3,500 lets; about 60,000 enquiries | Routine |
| 4 | Viewing | I5 | about 21,000 | Physical; much of it can become self-guided or remote |
| 5 | Tenant selection and referencing, right to rent | I6, I7 | about 5,000 applicants | Routine, with residual judgement (landlord's choice) and rising fraud |
| 6 | Tenancy creation and move-in: written terms, prescribed information, deposit protection, check-in | I8, I9 | 3,500 packs; 2,250 managed check-ins | Routine, plus physical |
| 7 | Rent month: collect, allocate, pay out, statement | I10, I22, I24 | 90,000 rent-months | Routine, with a messy tail (unidentified receipts, statement queries) |
| 8 | Arrears | I11 | about 7,500 actions; 1,500 cases | Diagnostic; residual judgement in hardship |
| 9 | Repair job: report to paid invoice | I13, I14, I15 | 37,500 reports; about 7,500 fixed by guided triage; about 30,000 jobs | Diagnostic |
| 10 | Emergency hazard | part of I13 | 2,000 | Diagnostic, physical, time-critical |
| 11 | Damp, mould and other statutory hazards | part of I13 | 2,500 reports; about 800 significant cases | Diagnostic, with a long outcome |
| 12 | Compliance cycle: gas, electrics, alarms, energy rating, licences, database | I17 | 12,500 due items | Routine |
| 13 | Periodic inspection | I16 | 15,000 visits today | Physical; the report is diagnostic |
| 14 | Tenancy changes: rent increase, pets, sharers, permissions | I18, I19 | 8,000 | Routine, some diagnostic |
| 15 | End of tenancy: notice, check-out, deposit return, dispute | I20, I21 | 2,250; about 300 disputed | Diagnostic; disputes residual |
| 16 | Possession | I12 | about 300 | Residual judgement |
| 17 | **Keys, access and appointments** | new | about 40,000 access arrangements | Routine; failures are diagnostic and physical |
| 18 | **Voids**: drain-down, insurance unoccupancy limits, council tax, utilities, security | new | about 2,250 voids; about 150 homes empty at any time | Routine, physical |
| 19 | **Third parties who must act**: freeholders, managing agents, neighbours' landlords | new | about 1,000 issues (flats are perhaps a third of homes) | Diagnostic; clocks run while someone else sleeps |
| 20 | **Insurance claims**: escape of water, storm, malicious damage | new | about 300 | Diagnostic, long-running, multi-party |
| 21 | **Landlord events**: death, receivers, sale with tenant in place, landlord leaves mid-tenancy | new | about 700 (landlord churn of 10 to 15% a year) | Diagnostic; authority questions |
| 22 | **Landlord tax**: Non-Resident Landlord Scheme, Making Tax Digital records | J part | 250 overseas landlords; quarterly records for perhaps 2,000 | Routine clocks; a product |

Four further streams cut across the case types and are not products:
- **Enquiries and complaints** (I23, I26: about 120,000 contacts, 400 complaints).
- **Landlord advice and portfolio reviews** (I25, I27).
- **Vulnerability and crisis**, which can attach to any case.
- **Fraud, enforcement and conduct**: forged documents, title fraud, rent-to-rent operators, bank detail changes, council notices, anti-social behaviour, subletting, cannabis farms, police warrants. Each attaches to a home or tenancy and changes who may be told what.

By count, over 90% of cases are routine. By effort, perhaps half is diagnostic and a small, heavy share is residual judgement [reasoned]. The review adds a third axis: **waiting**. Much of the elapsed time in this service is spent waiting on people outside the firm. The engine wins the count quickly. The effort sits in the diagnostic middle. The elapsed time sits with counterparties, and is fixed by contract, payment and access, not by better chasing.

---

## 2. The agent enterprise for this service

### 2.1 The constitution, in concrete clauses
Written by the owners, readable by every agent. The clauses that do most work:

1. **Purpose.** Keep each managed home legal, safe, let and paid for the landlord, treating the tenant fairly and lawfully at every step.
2. **Duty to the non-client.** If a landlord's instruction would breach a tenant's rights or put anyone at risk, the firm does not carry it out, and says why.
3. **Statutory clocks are hard limits.** No case is scheduled past a legal deadline. If one cannot be met, escalate before it passes.
4. **Money.** Client money is used only for its purpose. No agent changes a payee's bank details. A named person does, after a call-back on a number already held.
5. **Spend.** Inside the landlord's spend matrix, act and pay from the float. Above it, ask with a deadline; if the landlord does not answer by the deadline, the contract's default applies. To make a home safe, take the minimum safe step and tell the landlord at once.
6. **Fairness.** Selection uses only lawful criteria. Every rejection has a stated reason the applicant can see.
7. **When unsure.** If a case fits no known type, or maker and verifier disagree, stop and route. Never guess on what cannot be undone: notices, court papers, deposit deductions, rejections, payouts to new accounts.
8. **Vulnerability.** Any sign of distress, abuse, bereavement or risk to life moves the case to a person and pauses all automated chasing of that household.
9. **Trade-off order.** Safety, legality, the client's money, speed, cost.
10. **Honesty.** Status shown to anyone is the true state, including when the firm is late. **Silence is not success**: an unconfirmed outcome is shown as unknown.
11. **Verify at source, not by document.** Income, identity, title, registration and bank ownership are checked against the issuing system where one exists, not against a document someone supplied [reasoned: generated documents make documents worthless as evidence].
12. **Pay counterparties fast.** Contractors who meet the evidence standard are paid within 48 hours. This is a design choice, not a courtesy: capacity follows payment [experience, per reviewer].

### 2.2 The shared state
One append-only record, read and written through typed actions. Agents never message each other.

- **Entities:** landlord (identity, verified title, mandate, spend matrix, float balance, tax status, authority holders such as executors or receivers); home (licence, certificates, energy rating, condition record, hazard history, **access record**: keys, codes, who holds what; tenure: freehold or leasehold, with freeholder and managing agent); tenancy (parties, rent, deposit and protection, documents served and when); household (contacts, vulnerability flags, **who must not be told**); contractor (trades, area, registration, verified bank details, performance, **capacity and preference**); third party (freeholder, managing agent, insurer, loss adjuster, council officer); job; **obligation** (every certificate, notice period and statutory clock, with its deadline and who owns the next move); money; decision (who or what decided, under which playbook version, on what evidence).
- **Events:** report received; hazard classed; clock started; approval requested, defaulted; job offered, accepted, attended, evidenced, closed; key issued, returned, missing; invoice matched; rent due, received, unidentified, missed; notice served; certificate issued; deposit protected; claim opened; third party chased; complaint opened; vulnerability flagged; fraud flag raised; breaker tripped; playbook promoted or rolled back.

The obligation entity is the heart of the service. Most of the law here is a set of clocks. Put every clock in the state and the promise becomes a query [reasoned]. The revision adds one field that matters: **whose move it is**. A clock where the next move belongs to a freeholder or a silent landlord is a different risk from one where it belongs to the firm, and should be shown that way.

### 2.3 Agent roles and counterparties
On the ten layers of step 3b, the service-specific roles are:

- **Front door:** landlord concierge; tenant line (any channel, any language, any hour, **including voice calls out and in**); applicant agent; a video triage agent for repairs; an interface for landlords' and tenants' own agents.
- **Production:** a tenancy orchestrator per tenancy and a repair orchestrator per job, each the sole writer; workers for referencing, documents, rent allocation, arrears, compliance scheduling, inspection reports, deposit evidence, rent-increase notices, void management and landlord tax.
- **Counterparty agents:** contractor dispatcher; access coordinator; freeholder and managing-agent liaison; insurer and loss-adjuster liaison; deposit scheme, referencing, council and database, utilities, portal, HMRC and solicitor liaison.
- **Exceptions and governance additions:** a vulnerability detector that can pause any case; a legal-deadline watchdog; a fairness auditor testing selection outcomes across groups; a client-money auditor reconciling daily; a **fraud sentinel** watching documents, title changes, payee changes and odd letting patterns.

Counterparties are mostly people. Tenants use phones, and the tenants on old phones answer calls, so voice is the default for chasing [seen: voice agents already make collection calls]. Contractors are sole traders who accept a job offer by text with price, address, access notes and a photo checklist, and are paid only on evidence [seen: repair platforms dispatch this way]. That works for the middle of the market. It does not create capacity [experience, per reviewer]. Deposit schemes, referencing providers and HMRC have interfaces. Councils and courts are people and portals. Freeholders and managing agents are slow and owe the firm nothing. Landlords' own agents are rare now [conjecture: common among larger landlords by 2030] and get the same typed interface and limits as the landlord.

### 2.4 Verifiers, by main case type
Each has the three checks of step 1: rule, consequence, outcome.

| Case type | Rule check | Consequence check | Outcome check | Fastest close |
| --- | --- | --- | --- | --- |
| Tenancy creation | Every prescribed document served; deposit protected; right to rent recorded | Scheme certificate issued | No penalty claim; no notice later invalid | Hours |
| Rent month | Allocations sum to receipts | Bank reconciles to the penny; suspense account below set level | No landlord query; year-end ties | Same day; suspense items days |
| Arrears | Contact rules, timing, lawful language | Payment or plan agreed | Plan holds; tenancy sustained or lawfully ended | Days to months |
| Repair job | Right trade, inside matrix, clock set | Attendance by geo-time and photos; **independent check**: sensor, next-visit photo, or a call to the tenant on a sample | No repeat report in 90 days **from any channel**; silence counted as unknown | Hours; tail 90 days |
| Emergency | Classed in minutes; safe step ordered | Made safe in 24 hours, with evidence | No harm, no repeat | 24 hours |
| Damp and mould | Hazard class and clock; investigation booked | Done in time; cause found; works done | **Humidity readings continuous** after works; no recurrence | Weeks; outcome signal in weeks, confirmed in a year |
| Compliance cycle | Every obligation has a deadline | Certificate by a registered person, checked at source, served on tenant | No lapse, no enforcement | Days |
| End of tenancy | Deductions only beyond fair wear, with evidence | Agreed or adjudicated | Adjudication win rate; no upheld complaint | Weeks |
| Tenant selection | Lawful criteria; income and identity verified at source | Tenancy starts | Sustained 12 months; fairness audit clean; no fraud found later | Months |
| Possession | Ground, notice period and form correct | Court accepts claim | Order or settlement; no finding against firm | Months |
| Landlord tax | Withholding computed; quarterly return due date in state | HMRC accepts return | No assessment against the firm | Quarter |

The review's point on tenant confirmation is right, and changes this table. Tenants rarely confirm a fix. They report again, or they do not [experience, per reviewer]. So a confirmation request is an input, not a verifier, and under-reporting will flatter any recurrence rate built on reports. The fix is a verifier that does not depend on the tenant choosing to reply: sensors where they exist, a sample of short calls, and the next inspection or tenant video checking past jobs [reasoned].

### 2.5 Authority envelopes and circuit breakers
**Envelopes** [reasoned]: repair spend inside the landlord's matrix, paid from the float; a capped safety override (say £500) to make safe only. The matrix sets a limit by repair class, not one number: a boiler repair up to £400, a like-for-like boiler replacement up to an agreed sum, glazing, locks and drains each with their own cap. Above the matrix, the firm asks with a deadline (48 hours for urgent, 5 working days for routine), and the contract sets the default on silence: proceed with the cheapest compliant quote [conjecture on the exact terms]. Notices are drafted freely but served only after an independent check of form and date. Never, for any agent: change bank details, serve possession notices, deduct from a deposit without the verifier's pass, reject an applicant without a lawful reason, release a deposit or payout to a new account, or auto-chase a household flagged as vulnerable. Contact limits and quiet hours per tenant, except for safety.

**Circuit breakers:** repeat-report rate rises for a contractor or playbook version, so dispatch on it stops; any template change reaches 2% of tenancies until consequence checks clear; hazard clocks breached above a set rate, so the line halts and the on-call person is paged; any reconciliation difference halts payouts on that account; suspense account above a set level halts automated allocation; fairness audit drifts, so the selection playbook freezes; a cluster of fraud flags on one applicant pattern, so referencing for that pattern goes to a person.

---

## 3. Walking the firm through its life

Each event says what the agents do, whether it works with no person, and if not which need applies: (1) purpose, (2) definition of good, (3) answerability, (4) capability gap, (5) client demand for a person, (6) physical world, (7) duty to a non-client (added in section 7.2).

### 3.1 A landlord signs up with three properties
The concierge takes the mandate in conversation. It checks identity, then **title at the Land Registry, and that the person signing is the registered owner**, which stops most title fraud and rent-to-rent lets at the door [reasoned]. It asks for lender, freeholder and insurer consents, and checks licensing for each address. It records tenure: two are leasehold flats, so it records the freeholder and managing agent. It pulls energy ratings and existing certificates. It agrees the spend matrix, the float (say £300 to £500 a home) and the default on silence, and sets up keys: one set and a code for each home. It finds a lapsed gas record and a home in a selective licensing area with no licence. It books an engineer and drafts the licence application. The landlord sees a live dashboard with two amber items and dates.

**Without a person?** Yes, for most landlords [reasoned]. The baseline condition of each home needs a visit (**6**). Many accidental landlords want to meet someone first, and choose a firm on whether they can reach a person (**5**). So every landlord gets a named patch lead from day one (section 4).

### 3.2 Finding and referencing a tenant
The applicant agent writes the listing from the condition record; the verifier checks every claim against the state. Enquiries are answered at once, any hour, and viewings booked. In an empty home, the default is a **self-guided viewing**: the applicant is identity-checked, gets a one-time code for a smart lock or key safe, and the visit is recorded at the door [seen: self-guided viewings with smart locks exist in the US]. In an occupied home, where most viewings happen during the notice period, the tenant's consent and comfort come first: a recorded video tour, then a hosted viewing for shortlisted applicants only [reasoned]. Offers are taken at the advertised rent only, since bidding above it is now unlawful [seen].

Referencing runs through providers. The revision changes how evidence is taken. Payslips and bank statements as documents are now weak evidence, because generated documents are cheap [conjecture: forged documents will rise sharply]. So income is checked through open-banking or payroll data with the applicant's consent, identity against issuing systems, and right to rent through the online checks [reasoned]. The selection agent gives the landlord a short list with lawful reasons. The landlord chooses.

**Without a person?** The paperwork, yes. Hosted viewings in occupied homes need a body (**6**). Borderline affordability (self-employed, guarantors, overseas income) is judgement today (**4**, temporary). Applicants who refuse open-banking checks need another route, and someone must decide what that route is (**2**). The fairness of selection outcomes needs a person who owns what "fair" means (**2**). The landlord's choice is the principal's authority, not a gap.

### 3.3 Move-in and the deposit
The orchestrator assembles the written terms and required documents, takes no more than a month in advance, protects the deposit and serves the prescribed information well inside 30 days. The verifier checks each step against the scheme's certificate. The tenant gets keys or a code, logged. The check-in is a clerk visit with timed photos and meter reads; by 2030 the incoming tenant captures it with a guided video, checked against the check-out record, with a clerk only on high-value or disputed homes [conjecture].

**Without a person?** All but the check-in today (**6**). Missed deposit steps cost up to three times the deposit and hamper possession [seen]. This is the clerical error a verifier catches every time [reasoned], so here agents should beat people most clearly.

### 3.4 Rent collection, and a tenant falls into arrears
Rent arrives by open-banking payment where the tenant agrees. Much of it does not. Universal Credit arrives late and in odd amounts; payments lack references; one payer covers two tenancies [experience, per reviewer]. The allocation agent matches on amount, payer, date and history, and posts confident matches. Anything below a set confidence goes to a **suspense account** with a proposed match, and a person in client accounts approves or corrects it. Each correction is a training case. Landlord statements are posted the same day; fee and works queries go first to the concierge, which can show the evidence for every line.

A tenant pays half. The arrears agent calls that day by voice, then sends a factual message, offers a plan within the landlord's limits and signposts free debt advice. The plan holds for a month, then the tenant misses again and stops replying.

**Without a person?** Clean receipts, yes. Unidentified receipts and statement disputes need a person in 2027 (**4**, shrinking as the suspense rate falls). The first 30 days of arrears, yes. Then hardship becomes a judgement about a household, where an accountable, sympathetic voice changes the outcome (**7**, and **4** for now). Advising the landlord on possession is residual judgement (**4**). Silence may hide a crisis (section 3.11).

### 3.5 An emergency repair at night
At 02:10 a tenant reports water through a ceiling light. The tenant line classes it as an emergency: water plus electrics. It tells the tenant how to isolate the electricity and where the stopcock is, from the home's record. It dispatches an out-of-hours plumber and electrician under the safety override, with the key-safe code. It tells the landlord and opens a 24-hour clock. Photos of the isolated circuit and stopped leak close the first job. The flat is on a first floor: the agent also checks whether water has gone below, and opens an insurance claim case (section 3.16).

**Without a person?** Mostly yes [reasoned]. The doing is physical (**6**). A frightened or vulnerable tenant should be able to reach a voice (**7**). If no contractor accepts in time, a person must find one or arrange a hotel (**4**). **One night on-call person for the whole firm stays permanently**. It costs under £100,000 a year in rota pay and caps the worst outcome [experience, per reviewer]. Some scaffolding is too cheap to take down.

### 3.6 A damp and mould report with statutory timescales
A tenant sends photos of black mould in a child's bedroom. Social landlords must now make emergency hazards safe in 24 hours and investigate significant damp and mould within 10 working days [seen]. The Renters' Rights Act extends Awaab's Law to private renting, with timescales still to be set [seen]. The firm adopts the social-sector clocks now as a published standard [reasoned].

The agent asks for more photos and who sleeps in the room; a child raises severity. It sends a **humidity and temperature sensor** by post the same day [seen: social landlords already use them]. It books a damp surveyor within the clock. A diagnostic agent reads the sensor trace and the surveyor's moisture readings and proposes a cause: no extraction, a defective gutter, rising damp, or a home that is cold because heating is unaffordable. It drafts works and a written summary. The sensor stays, and its trace is the outcome check.

**Without a person?** Logistics, yes; diagnosis, partly. Causes are often mixed, building and occupancy. Telling a family that drying clothes indoors is part of the problem is delicate (**4** for diagnosis today, **7** for the conversation). If the landlord refuses works, someone must hold the line on safety and answer for it (**3**). Someone must own what "resolved" means (**2**). The sensor changes the speed of learning: a 12-month outcome becomes a continuous signal, readable within weeks of the works [reasoned]. This is still the case type with the largest human share per case, but it can now shrink faster than the first draft allowed.

### 3.7 A gas safety certificate about to expire
Sixty days out, the compliance agent calls the tenant and offers slots, books a Gas Safe engineer, confirms access the day before, files the record and serves a copy on the tenant within 28 days. If access is refused, it logs each reasonable step [seen: the duty].

**Without a person?** Yes; the engineer is physical (**6**). Repeated refusal with a vulnerable tenant routes to a person, rarely. This is the cleanest case type in the firm and the first product to sell as a guarantee (step 3, 4a).

### 3.8 A contractor does not turn up, and there is no second contractor
No geo-time check-in arrives in the window. After 30 minutes with no answer, the dispatcher re-offers the job, gives the tenant a new time and records the no-show.

The first draft then suspended any contractor with three no-shows in a quarter. The reviewer is right that this empties a rural panel in a winter. Revised: the dispatcher **ranks** contractors on reliability, quality and price, and suspends only where the panel in that area stays above a set depth. Where it would not, it flags the gap to the regional network manager.

The deeper point is that dispatch is not the constraint. Supply is. Good plumbers and Gas Safe engineers are overbooked and choose the agents who pay fast and send tidy jobs [experience, per reviewer]. The firm's answer is to make itself the preferred client: payment within 48 hours on evidence, clean job packs, guaranteed access, no wasted trips, steady volume in a defined patch, and help with paperwork such as certificates [reasoned]. Regional network managers recruit, keep and grow the panel. Where a region is thin, the firm offers guaranteed minimum volumes to a small number of contractors, or employs a handful of multi-trade operatives directly [conjecture].

**Without a person?** The re-dispatch, yes. Building and keeping the network, no (**4** and **6**, and arguably a permanent role: a relationship with a sole trader is a human trust relationship). The network is the asset.

### 3.9 A deposit dispute at the end of a tenancy
After the check-out, a comparison agent proposes deductions tied to photo evidence and adjusted for fair wear. A separate verifier checks each against the scheme's guidance. The landlord approves; the tenant disputes £400 for carpets, declines a split, and the agent submits the evidence pack to adjudication. The refund goes only to the tenant's account on record; any new account goes through the payee-change control.

**Without a person?** Up to adjudication, yes; the adjudicator is an outside verifier and a clean learning signal [reasoned]. A landlord wanting more than the evidence supports must be told no (**5**). The firm's standard of a fair deduction must be owned by a person, not by the drafter (**2**).

### 3.10 A landlord wants possession under the new rules
Since 1 May 2026 possession needs a section 8 ground [seen]. The landlord wants to sell. The agent checks the selling ground, the protected first year, the notice period, and the deposit, certificate and licensing history the court will look at. It explains the timetable and the bar on re-letting. It drafts the notice; the verifier checks form and dates; a person approves service. If the tenant stays, a solicitor issues the claim.

**Without a person?** No. Advising on ending someone's home, and standing behind the advice, is answerability (**3**). Conducting litigation is a reserved legal activity (**3**). Hearings need a person in the room today (**3**, **6**). Many cases involve a tenant in difficulty (**7**). The agents' gift is near-perfect paperwork, where most failed claims go wrong [reasoned from practice].

### 3.11 A tenant in distress: bereavement, domestic abuse
A sole tenant dies and a relative calls. The vulnerability detector moves the case to a person and stops all chasing; the person explains what happens to the tenancy, belongings and deposit, and agents do the paperwork. A tenant discloses abuse by a joint tenant and asks for new locks. The firm must not alert the abuser through any automated message. A person contacts the right services, arranges an urgent lock change and handles the tenancy change with legal advice. The access record changes at once: old codes revoked, new keys issued only to the named tenant.

**Without a person?** No (**7**, and **3** because a wrong move can cause harm). Agents can detect and pause, never be the only voice. Structural lesson: the state must hold **who must not be told**, not only who must be. In a joint tenancy every routine message is a possible danger [reasoned].

### 3.12 A new model release
The harness runs every suite and holdout. Rent, compliance and document cases pass and move to 5% of homes, then all. Repair-photo triage improves and goes to staged release. Tone with distressed tenants is worse on one holdout, so the tenant line stays on the old model.

**Without a person?** Yes, within existing autonomy. A person approves any rise in autonomy, such as serving notices without a check (**2**).

### 3.13 An error repeated across many properties
A template update puts a wrong clause in the prescribed information. Under the reach limit it went to 2% of new tenancies: four in three weeks, out of about 200. A scheme rejects one; the consequence check flags it; the circuit breaker halts the template, rolls back and lists every affected tenancy. Agents re-serve correct documents where the window allows.

**Without a person?** Detection and repair, yes. Telling the landlords and tenants, deciding redress, and whether to notify the insurer and redress scheme is answerability (**3**). Finding why the tests missed it, and changing them, is the definition of good (**2**). Without the reach limit the error would have hit about 200 tenancies first, and kept going [reasoned].

### 3.14 A landlord will not approve a quote (new)
A boiler fails in October. The engineer quotes £2,600 for a replacement, above the matrix. The firm asks the landlord with a 48-hour deadline. No answer. A second quote comes in at £2,300. Still no answer. Meanwhile the tenant has temporary heaters from the float, and the repair clock is running.

**Design response.** The contract, not the chase, solves this. Under the default on silence, the firm proceeds with the cheapest compliant quote at the deadline and tells the landlord [reasoned]. The float covers the deposit to the engineer; the balance is taken from the next rent payout. If the landlord disputes the invoice afterwards, the evidence pack (two quotes, the engineer's condemnation report, the clock) is the answer. For landlords who refuse the default clause, the promise on repair times does not apply, and the dashboard says so.

**Without a person?** Mostly yes. A landlord who disputes after the event, or refuses works that are needed for safety, needs a person who can say no and answer for it (**3**, **5**). In a rising number of cases the landlord simply cannot pay; that is a hardship case on the landlord side, and a person decides whether to fund and recover (**4**).

### 3.15 Nobody can get in (new)
A plumber arrives for a leak. The tenant is at work and the key is "in the office", which means a drawer in a branch that closed in 2025. Most missed appointments are access failures, not no-shows [experience, per reviewer].

**Design response.** Access is a case type with its own state. Every home has an access record: which keys exist, who holds each, a key-safe or smart-lock code where the landlord and tenant agree, and the tenant's standing consent for routine entry with notice [reasoned]. The access coordinator confirms access the day before every visit, sends a one-time code to the contractor, and logs entry and exit. Missing keys open a job to rekey. Physical keys that remain are held in a few tracked key stores, not branches.

**Without a person?** The coordination, yes. A tenant who refuses access for a safety check, or a key that cannot be traced, needs a person, rarely (**4**, **6**). Smart locks raise their own questions of consent and security, which a person owns (**2**).

### 3.16 Water goes through to the flat below (new)
The leak in section 3.5 has stained the ceiling of the flat below, which the firm does not manage. A neighbour, the block's insurer and a loss adjuster are now involved. Such claims run for months [experience, per reviewer].

**Design response.** An insurance claim case type, owned by the claims liaison agent. It assembles the timeline from the state (report time, made-safe time, photos, contractor reports), notifies the right insurer (the block policy for a flat, the landlord's for a house), tracks the adjuster's requests as clocks and chases them. It keeps the tenant and landlord informed of the true state.

**Without a person?** The evidence and chasing, yes. Negotiating with a loss adjuster on cause, liability and scope is judgement today (**4**). A neighbour's anger is not a case for an agent alone (**5**).

### 3.17 An overseas landlord, and the tax clocks (new)
A landlord moves to Dubai. Unless HMRC has approved gross payment, the firm as letting agent must deduct basic-rate tax from the rent, pay it to HMRC quarterly and file an annual return, and it is liable if it gets this wrong [seen: HMRC guidance]. Separately, Making Tax Digital for income tax is starting for landlords above an income threshold [seen].

**Design response.** Both are clocks and records, so both are products, not risks. The landlord's tax status is a field in the state. A status change triggers withholding from the next payout. The quarterly return is an obligation with a deadline. For all landlords, the firm already holds every income and expense line, so a quarterly digital record and submission is close to free to produce [reasoned].

**Without a person?** Yes, with an accountable officer who signs off the returns (**3**) and a person for the odd case (a landlord who disputes residence).

### 3.18 A landlord dies; a lender appoints receivers (new)
A landlord dies. Their executors ring. Until the firm sees the grant of probate or letters of administration, who can instruct it? Separately, a lender appoints receivers over another landlord's three homes and writes demanding the rent.

**Design response.** Authority is a field in the state, with evidence. On a death, the firm keeps the homes running under the existing mandate (rent collected, safety kept, payouts held in client money), and records the executors as interim contacts with limited rights until the grant is seen [reasoned; exact legal position not checked in this pass]. On receivers, rent is redirected only after their appointment is verified. On a sale with the tenant in place, or a landlord leaving mid-tenancy, the deposit transfer, new mandate and notices to the tenant become a checklist case.

**Without a person?** Verifying authority documents and deciding who may instruct is answerability (**3**). A bereaved family needs a person (**5**). Everything after the decision is agent work.

### 3.19 The council serves an improvement notice (new)
A council inspects after a tenant complaint and serves an improvement notice on a home with an unsafe staircase. Councils can now impose civil penalties of up to £7,000 for breaches and up to £40,000 for offences under the Renters' Rights Act regime [seen: GOV.UK guidance]. Councils want a named person [experience, per reviewer].

**Design response.** The notice's deadline goes into the state as an obligation. Works are dispatched under the safety clause if the landlord does not respond. The compliance officer is the named contact for the council.

**Without a person?** The works and clocks, yes. The relationship with the council, and representations against a penalty, need the accountable officer (**3**).

### 3.20 A void in January; and a home used for something else (new)
A tenant leaves in early January. The home will be empty for three weeks. The landlord's insurance has an unoccupancy clause, often 30 to 60 days, after which cover narrows [experience; exact terms vary]. Pipes can freeze. Council tax and utilities change hands.

**Design response.** A void case opens on the check-out. It drains down or sets heating to frost protection, schedules weekly checks (a sensor plus a short visit by the local network), notifies the insurer if the void will exceed the clause, and moves council tax and utilities. Every day of void is also on the marketing clock.

Another home shows a sharp rise in electricity use, condensation on windows, and a neighbour's complaint about smell. The fraud and conduct sentinel raises a flag: a possible cannabis farm or illegal sublet.

**Without a person?** The void, yes, apart from the physical checks (**6**). Suspected crime, a police warrant, anti-social behaviour between neighbours, or subletting need a person who can talk to the police and decide what the firm may say to whom (**3**, **4**). Fraud flags are never acted on by an agent against a household; they route.

### 3.21 Someone asks to change the payout account (new)
An email from a landlord's address asks for rent to go to a new bank account from next month. This is the main target for fraud in the sector [experience, per reviewer].

**Design response.** No agent can make the change. The request opens a case. The account is checked with Confirmation of Payee [seen: UK banks run name checks]. A named person in client accounts calls the landlord back on the number held before the request, not any number in the email. The first payout to a new account is held for a set period and the landlord told through the existing channel. Deposit refunds follow the same rule.

**Without a person?** No, by design. This is a control where a person is cheaper than the loss, and where a human voice on a known number is the verifier [reasoned]. It is small: a few hundred changes a year.

### 3.22 What the walk shows
- **No person needed:** rent (clean receipts), compliance, tenancy creation, landlord tax, most repairs, access coordination, voids, enquiries, model releases.
- **Physical people, outside the firm:** hosted viewings, check-outs, inspections that remain, every repair, the damp survey, void checks.
- **A person inside the firm:** contested hazards, hardship, possession, distress, landlords who will not accept a no, errors that reach clients, changes to the definition of good, the contractor network, suspense items and payee changes, authority after death or receivership, council and police relationships, loss adjusters, and stuck freeholders.
- **The new class the review exposed:** **people outside the firm who do not reply**. Landlords, contractors, freeholders, adjusters. Chasing does not fix them. Contract terms (the default on silence), money (the float, fast payment), access (keys and codes) and relationships (patch leads, network managers) do.

---

## 4. The people

### 4.1 Roles by kind

| Kind of need | Role in this service | Why |
| --- | --- | --- |
| **1. Purpose** | Owners and a small board, with one independent member who speaks for tenants' interests | The constitution's duty to the non-client needs a voice at the top |
| **2. Definition of good** | Evaluator governors: one for money and documents; one for repairs and hazards (a building surveyor); one for tenancy, fairness and possession (a housing lawyer or senior lettings professional) | Each owns test suites, thresholds and audit samples for a domain |
| **3. Answerability** | Accountable officers: client money; compliance and safety (the council's named contact); complaints and redress, with a small team handling complaints to the ombudsman's standard; data protection; landlord tax; a solicitor for possession (in-house or partner) | Regulators, schemes, HMRC, courts and councils deal with persons |
| **4. Capability gaps** | Judgement desk: hazards, hardship, borderline referencing, landlord disputes, landlord advice, possession files, loss adjusters, stuck freeholders. Client accounts: suspense items, statement disputes | Shrinks with capability; size set by exception rate |
| **5. Client demand** | **Patch leads**: one named person per 600 landlords at launch, for escalation and retention, not property management | Landlords choose on trust and on reaching a person when something breaks [experience, per reviewer] |
| **6. Physical world** | Viewing hosts, inspectors, check-in and check-out clerks, damp surveyors, void checkers, contractors | A network of partners and self-employed people, coordinated by the firm |
| **7. Duty to non-clients** | Household support team (tenants in distress, bereavement, abuse) | A duty sized by vulnerability, not willingness to pay |
| **Network** | Regional contractor network managers | Supply, not dispatch, is the constraint; relationships with sole traders are human |
| **Controls** | Payee-change and fraud controls; keys, access and voids coordination | A person on a known phone number is the verifier; access failures need someone who can sort keys |
| **Growth** | Landlord acquisition and book migration | Landlords leave at 10 to 15% a year; the book must be refilled |
| **Scaffolding** | Builders (engineers and lettings experts writing first playbooks); human checkers on notices and deductions while evidence builds | Temporary by design |
| **Permanent insurance** | One night on-call person for the whole firm (a rota of five) | Cheap, and caps the worst outcome |

### 4.2 Headcount sketch
Firm serving about 5,000 landlords and 7,500 managed homes. Inside-firm staff only. The physical network is counted separately because it is mostly outside the firm in both models. All numbers are **[conjecture]**, now set against workload estimates rather than a single ratio.

| Role | 2027 | 2030 A | 2030 B | 2035 A | 2035 B |
| --- | --- | --- | --- | --- | --- |
| Owners, board, accountable officers | 6 | 6 | 6 | 5 | 6 |
| Evaluator governors | 3 | 3 | 4 | 2 | 4 |
| Judgement desk | 18 | 8 | 14 | 3 | 10 |
| Household support (tenant distress) | 6 | 5 | 6 | 4 | 6 |
| Patch leads (named person per landlord group) | 8 | 6 | 8 | 5 | 7 |
| Contractor network managers | 5 | 4 | 5 | 3 | 4 |
| Client accounts, payee controls, landlord tax | 5 | 3 | 4 | 2 | 3 |
| Keys, access, voids and fraud coordination | 4 | 2 | 3 | 1 | 3 |
| Complaints team | 2 | 2 | 2 | 1 | 2 |
| Landlord acquisition and migration | 6 | 5 | 6 | 4 | 5 |
| Builders (engineering and playbooks) | 10 | 6 | 8 | 3 | 6 |
| Human checkers (scaffolding) | 6 | 1 | 4 | 0 | 2 |
| Night on-call rota (permanent, in FTE) | 2 | 2 | 2 | 2 | 2 |
| **Inside the firm** | **81** | **53** | **72** | **35** | **60** |
| Physical network, in full-time equivalents (outside) | 37 | 22 | 33 | 13 | 28 |

**How the judgement desk was sized** [reasoned, from guessed volumes]. In 2027, at about 1,600 productive hours a person: above-limit escalations that the spend matrix does not settle (about 1,500 at 1 hour), arrears past 30 days (about 600 at 4 hours), significant damp cases (about 800 at 6 hours), borderline referencing (about 1,000 at 1 hour), possession files (300 at 6 hours), stuck third-party and insurance cases (600 at 6 hours), landlord advice (2,000 at 1 hour). That is about 17,000 hours, or 11 people, plus peaks and the launch rule that every complaint and every arrears case after 30 days goes through the desk: about 18. The reviewer's sense that 14 was light is right. A much larger desk is not needed if the contract fixes approvals.

**How the physical network was sized** [reasoned]. At corrected volumes in 2027: 21,000 viewings at 1 hour with travel; 15,000 inspections at 1.5 hours; 4,500 check-ins and check-outs at 3 hours; 800 damp surveys at 3 hours; void checks about 2,000 hours. About 61,000 hours, or 37 full-time equivalents. By 2030 in landscape A: self-guided viewings in empty homes and video tours halve hosted viewings; one inspection a year becomes a tenant video with sensor data; tenant-captured check-ins with clerk sampling. About 22. By 2035 A: about 13. Repair contractors are extra and the same in every model.

**A traditional firm serving the same clients.** The inventory's lettings team is 11 people for 600 tenancies, about 55 tenancies per head, plus a share of central staff. Scaled to 7,500 homes: about **140 to 160 staff**, of whom perhaps 15 to 20 are inspectors and clerks. On like-for-like terms (excluding the physical network), that is about 125 to 145 against 81 in 2027, 53 to 72 in 2030, 35 to 60 in 2035. Homes per inside person rise from about 55 to about 93 in 2027, and 125 to 215 by 2035.

The change in kind matters more than the count. The traditional firm is mostly property managers coordinating by phone and email. The agent-first firm has almost none. Its people are governors, officers, a judgement desk, household support, patch leads, network managers and a few controllers. The first draft's sketch was too thin because it counted only the people who handle exceptions, and missed the people who keep counterparties willing: patch leads for landlords, network managers for contractors. Those roles shrink least, because they are relationships, not tasks [reasoned].

---

## 5. 2027 against 2035: removing the scaffolding

### 5.1 What exists at launch
- People check every outward notice: section 13 rent increases, section 8 notices, deposit prescribed information, deduction proposals.
- People approve every rejection of an applicant.
- People own every significant hazard case from report to closure, with agents doing logistics.
- A judgement desk takes every repair escalation the matrix does not settle, every arrears case after 30 days, every complaint.
- Client accounts approves every suspense-account allocation.
- Builders write playbooks; agents propose edits; a named owner approves each change.
- An on-call person sits behind the night emergency line, and stays.
- Each landlord has a named patch lead.

### 5.2 The order of removal
Each step needs the evidence in the right-hand column. Removal is by case type, and any failure puts the scaffolding back without stigma.

| Order | Case type | Scaffolding removed | Evidence that justifies it | Plausible date |
| --- | --- | --- | --- | --- |
| 1 | Rent month, clean receipts | Human review of payouts and statements | 12 months of daily reconciliation with no unexplained differences; client-money auditor sign-off | 2027 |
| 2 | Compliance cycle | Human scheduling and filing | No lapse across a full annual cycle of all homes; certificates verified at source | 2027–28 |
| 3 | Landlord tax | Human preparation of returns | Four quarters accepted with no correction | 2028 |
| 4 | Tenancy creation | Human check of each document pack | 2,000 consecutive packs with zero defects on independent re-check; no scheme rejections; holdout set passes | 2028 |
| 5 | Enquiries and access coordination | Human sampling of most answers and bookings | Error below set rate for two quarters; access failure rate below human baseline | 2028 |
| 6 | Repair job inside the matrix, with guided triage | Human triage and close-out | Repeat-report rate within 90 days, from any channel, at or below human baseline over 10,000 jobs; independent sample checks agree | 2028–29 |
| 7 | Rent month, suspense items | Human approval of each allocation | Suspense rate below 1% and correction rate on proposed matches below set bound for two quarters | 2029 |
| 8 | Marketing and referencing | Human approval of each rejection | Fairness audit clean for a year; reasons contested below set bound; fraud found after letting below human baseline | 2029 |
| 9 | Deposit deductions | Human check of each proposal | Adjudication win rate at or above human baseline over 300 disputes; tenant complaints flat | 2029–30 |
| 10 | Rent increases (section 13) | Human check of each notice | No tribunal referral lost on form; tribunal outcomes match predicted market rent | 2030 |
| 11 | Damp and mould | Human ownership of each case | Sensor-confirmed resolution at or above human baseline across 800 cases; surveyor diagnosis agreement high on holdouts | 2030–31 (A); partly retained (B) |
| 12 | Arrears, first 60 days | Human handling of plans | Plan success and tenancy-sustainment rates at or above human baseline; no rise in complaints from vulnerable tenants | 2031 (A); never fully (B) |
| 13 | Possession | Human check of notices; solicitor | Notices: as row 10. The solicitor and the hearing stay while courts deal with persons | Partial only |
| — | Night on-call | **Never removed** | Cheap insurance; what goes is routine night handling, not the person | — |
| — | Payee changes | **Never removed** | The human call-back is the control | — |
| — | Tenant distress | **Never removed** | It is a duty, not a scaffold | — |

Three cautions [reasoned]. Slow outcome checks set the pace, but sensors can make slow checks fast: damp moves up the order because of them. Thin regional volume, such as rural night emergencies, may keep scaffolding long after national numbers look good. And outcome data built on tenant replies will flatter the engine; every removal above uses evidence that does not depend on the tenant choosing to report.

---

## 6. Economics sketch

**Everything in this section is conjecture.** No firm's accounts were read. Average rent assumed £1,350 a month; full management fee 12% of rent plus VAT, in line with the commercial guides cited in the inventory. Revised after review: traditional revenue includes ancillary income; traditional staff costs are lower.

### 6.1 Today's traditional firm
- Management revenue per home: about £1,950 a year before VAT; about £14.5m for 7,500 homes.
- Ancillary revenue: set-up and let fees on about 2,250 new lets (about £1m), maintenance commission on contractor spend (perhaps £100 to £150 a home), interest on client money, referral fees. Renewal fees fall away under periodic tenancies [reasoned]. Total perhaps **£16m to £17m**.
- Cost: 150 people at about £40,000 loaded (property managers are nearer £35,000 to £45,000 [experience, per reviewer]) is about £6m; branches, portal subscriptions, systems, marketing, insurance, management and outsourced clerks perhaps £6m to £7m.
- Margin perhaps **15 to 25%**, higher than the first draft's 8 to 15%. The inventory's weak marker of 11.9% is likely a firm carrying branches or acquisition debt.
- Cost per home: about £1,600 to £1,750 a year.

### 6.2 The agent-first firm

| Cost line, per home a year | 2027 | 2030 A | 2035 A | 2035 B |
| --- | --- | --- | --- | --- |
| Inside people (blended about £62,000 to £70,000 loaded) | £690 | £460 | £330 | £530 |
| Compute and verification | £60 | £40 | £20 | £40 |
| Engine fixed cost (spread) | £250 | £150 | £100 | £150 |
| Physical network (viewings, inspections, clerks, void checks) | £210 | £120 | £75 | £150 |
| Devices (smart locks, key safes, sensors), amortised | £15 | £40 | £35 | £25 |
| Insurance, schemes, database fees, fraud losses, guarantee reserve | £70 | £75 | £80 | £75 |
| Acquisition (marketing, book purchase amortised) | £150 | £120 | £100 | £120 |
| **Total** | **£1,445** | **£1,005** | **£740** | **£1,090** |

Cost per client, at 1.5 homes: about £2,150 in 2027, £1,500 in 2030 A, £1,100 in 2035 A, £1,650 in 2035 B.

**The finding the revision forces** [reasoned]. In 2027 the agent-first firm costs only about 10 to 15% less per home than a good traditional firm. The first draft showed a gap of nearly half. Two things closed it: real people costs in the traditional firm are lower than assumed, and the agent-first firm needs more relationship and control roles than assumed. The cost case rests on 2030 and after, when the gap becomes 35 to 55%. Launch economics depend on keeping the incumbent's revenue while the engine matures.

### 6.3 Prices and models
- **Buy a book and keep its price, at first.** Acquire an existing book in one dense region, migrate it, and keep the percentage fee for the first one to two years. At £1,950 revenue against £1,445 cost, the margin is about 25%, from day one, on real data [reasoned]. This is the reviewer's entry route, and it is better than the first draft's.
- **Percentage of rent, undercut:** 8 to 10% once costs fall. Familiar; passes the gain to clients and invites matching.
- **Subscription to a maintained condition, in two tiers.** A portfolio tier for landlords with three or more homes who accept the spend matrix, default on silence and data interface: about £65 a month a home in 2027, falling. A **named-person tier** for accidental landlords, with the patch lead visible: about £95 a month a home. The first draft's single £65 price would not have covered 2027 costs, and the low-fee online managers that tried this mostly retreated to let-only or left the market [experience, per reviewer]. Landlords who buy on price are portfolio landlords; accidental landlords buy trust.
- **Repairs at cost, plus a disclosed dispatch fee** (say 8% of works). This replaces hidden maintenance commission. The firm gives up some margin and gains a sales line: every invoice is shown live with the contractor's own price.
- **Guarantees on top:** a compliance warranty (a lapsed certificate or missed deposit step, and the firm pays the penalty and fixes it), sold first because it is the cleanest case type and the strongest trust signal; repair-time credits; rent protection with an insurance partner, priced from the firm's arrears data.
- **Landlord tax** as an add-on: Making Tax Digital records and submissions, and the Non-Resident Landlord Scheme handled as standard.
- **The contractor network as a product.** Dispatch, verified contractors, 48-hour payment and live status, sold to self-managing landlords who will never buy management [conjecture]. If the network is the asset, it should earn outside the managed book.
- **Per event** for let-only landlords.

### 6.4 By landscape

| | Landscape A | Landscape B | Landscape D (price collapse) |
| --- | --- | --- | --- |
| Price per home a year | £700–£1,000 (subscription tiers) | £1,100–£1,500 (percentage fees persist) | £300–£500; base management bundled into portals, banks or landlord software |
| Cost per home | about £740 | about £1,090 | about £700 unless scale doubles or trebles |
| Margin on base service | 0–25%, depending on how fast rivals follow | 0–25% | Negative |
| Where profit sits | Guarantees, rent protection, contractor network sold outside the book, named-person tier | Base service still profitable; guarantees as extra | Guarantees, the contractor network, possession and dispute service, crisis support, data-priced insurance |
| Against a traditional firm | Traditional margin collapses as clients move; the agent firm captures volume and buys books cheaply | Traditional firm survives with adoption; gap narrows | Traditional firm cannot price this low; consolidation, in which the agent firm is the natural buyer |

The plain reading: the base service probably becomes cheap in every landscape. The agent-first firm wins on cost from about 2029, not at launch, and cannot count on the margin lasting. What lasts is the network, the relationships, and carrying consequences, priced from better data than anyone else's.

---

## 7. What this example shows that the general design missed

### 7.1 Where agent-first holds better than expected
1. **The law is mostly clocks:** deposit deadlines, certificate cycles, notice periods, hazard timescales, rent-increase windows, tax withholding, council notice deadlines. Clocks are perfectly checkable. Much of what regulation demands here is what agents do best and people do worst at volume [reasoned].
2. **Outside verifiers already exist:** adjudicators, scheme certificates, Gas Safe records, bank reconciliation, HMRC acceptance, courts accepting a claim. The sector supplies consequence checks [reasoned].
3. **The signature is thin.** No licensed signature on every output; answerability sits in a few named roles, so the accountable layer can be small [seen: inventory 3.4].
4. **Coordination was the job.** Most property manager hours are chasing. Shared state and typed dispatch remove most of it, as step 3b predicted.
5. **Physical work can move to the tenant and to devices faster than assumed.** Guided repair triage, self-guided viewings in empty homes, tenant video inspections and humidity sensors each remove visits [seen for each in parts of the market]. Perhaps half of today's visits by 2030 [conjecture].
6. **Sensors turn slow outcomes into fast ones.** The step 1 rule that slow outcome checks set the pace has an exception: where a cheap sensor can measure the outcome continuously, the slow loop becomes fast [reasoned]. Damp is the example; voids and heating are others.

### 7.2 Where the human layer has to be larger
1. **A second population with rights.** Step 3b's "client demand for a person" assumes the client chooses. Here the people most likely to need a person are tenants, who are not clients and cannot be sold a premium tier. Household support is a duty sized by vulnerability, not willingness to pay. The general design needs a seventh category: **duties to non-clients**.
2. **People who do not reply are the real bottleneck.** Step 3b assumed delay is a coordination problem that shared state removes. Here the slowest step is usually a landlord, contractor, freeholder or adjuster who has no reason to hurry. Agents chase perfectly; chasing is not the problem. The answers are **structural**: contract terms that set a default on silence, money that moves first (a float, 48-hour payment), and control of access. The general design needs a principle: **design out waiting on counterparties through contract and money, not messages** [reasoned].
3. **The network is the asset, and it needs people.** The outcome the client buys is a physical state, so the firm's quality is mostly that of people it does not employ. Contractor supply, not dispatch, is the constraint, and a sole trader's loyalty is a human relationship. The general design counted physical-world people as outside the firm; the people who build and keep that network are inside it, and shrink slowly.
4. **Counterparties are not agents.** They are sole-trader plumbers, tenants on old phones, and freeholders. Landscape C arrives late here; interfaces must work for people with no software, and voice is the right channel for many.
5. **Physical evidence is the hard verifier, and silence is not evidence.** Photos can be staged or reused; a "fixed" leak may recur; tenants rarely confirm. Repair verifiers combine geo-time, image checks, sensors, independent sampling and recurrence from every channel.
6. **The client holds authority the firm does not, and that authority can change hands.** The landlord chooses tenants, approves works and decides on possession, and can instruct badly. Authority also passes to executors, receivers and buyers. A person must be able to say no, and must decide who may instruct.
7. **Messages can harm, and money can be stolen.** In joint tenancies and abuse cases a correct automated message can be dangerous. Payout and refund details are the main fraud target. Some controls should be human by design, because a voice on a known number is itself the verifier, not a gap in capability.
8. **Retention is a human role.** Landlords leave at 10 to 15% a year and choose on trust. The general design treated client demand for a person as a premium. Here a named person is the retention mechanism for most of the book, at a ratio that widens but does not vanish.

### 7.3 A sharper rule
Agent-first holds where the outcome is a record, and where the counterparty is a system. It weakens where the outcome is a physical state, a person's situation, or depends on someone who owes the firm nothing. Lettings has all three. The general design was right about the shape. It was too optimistic about the size of the boundary layer for a household-facing service, and it missed a whole class of boundary work: **keeping counterparties willing**. Its cost advantage arrives later than the general design implied, so the entry route (buy a book, keep its price, migrate) matters as much as the architecture.

---

## 8. Stress test: rules, insurance and institutions, applied now

| Fact | Status | What it changes |
| --- | --- | --- |
| **Renters' Rights Act phase 1:** section 21 gone; section 8 grounds only; periodic tenancies; annual section 13 increases; no bidding above advertised rent; one month in advance at most; pet requests answered in 28 days; no discrimination on benefits or children | In force from 1 May 2026 [seen] | Makes notices high-value and checkable (case types 14, 16). Bidding and discrimination rules become verifier rules on selection. Periodic tenancies remove renewal fees and may change turnover either way |
| **Council civil penalties**: up to £7,000 for breaches, up to £40,000 for offences | In force from 1 May 2026 [seen] | Raises the value of the compliance guarantee; keeps a named compliance officer as the council's contact |
| **Landlord database and ombudsman** | Database rolling out from late 2026; ombudsman membership expected 2028 [seen] | The database is a counterparty and an obligation in the state. The ombudsman makes complaint handling visible; keeps an accountable officer and a small complaints team |
| **Awaab's Law in private renting** | Enacted; timescales to be consulted on [seen] | The design already runs social-sector clocks. Wider scope or stricter clocks would grow the hazard team and contractor network |
| **Decent Homes Standard in private renting** | Proposed for 2035 or 2037 [seen] | The condition record becomes a compliance asset; a survey and works programme near the end of the period |
| **Non-Resident Landlord Scheme** | Agents must withhold basic-rate tax unless HMRC approves gross payment, and file returns [seen] | A clock and a product; an accountable officer signs off |
| **Making Tax Digital for landlords** | Starting for landlords above an income threshold [seen] | The firm already holds the records; a cheap add-on |
| **No statutory licence for letting agents; client money protection and redress membership mandatory** | Licence point not checked against a primary source | Keeps the accountable layer small. Licensing would add one named licensed person, not change the architecture |
| **Deposit rules and penalties; right to rent penalties** | [seen] | Strongest case for a guarantee; keep a human sample on right to rent until the evidence in section 5 exists |
| **Gas Safe registration; electrical reports every five years; alarms** | [seen] | The doing stays with registered people outside the firm; verify registration at source |
| **Conducting litigation is reserved** | [seen] | Possession needs a solicitor, in-house or partnered |
| **Data protection rules on solely automated decisions with significant effects** | Recently amended; detail not checked | Tenant rejection is likely one. Keep review on request, stated reasons and the fairness audit. Open-banking income checks need clear consent and an alternative route |
| **Smart locks and sensors in someone's home** | Privacy and consent rules apply; detail not checked | Tenant consent is a field in the state; a tenant can refuse and get a keyed route. Sensor data is the tenant's home life, so use is limited to safety and condition |
| **Insurance unoccupancy clauses** | Common in landlord policies [experience, per reviewer] | Voids become a clocked case type |
| **RICS AI standard** | Binds RICS-regulated firms from 9 March 2026 [seen in inventory] | Dip sampling instead of per-output review suits the design. Disclosure in terms. A landlord's opt-out means the firm must be able to run a home the old way, at a higher price |
| **Professional indemnity insurers on AI** | No wording found; insurers expected to probe [seen in inventory, as forecast] | The largest unknown. If insurers price per-output review, scaffolding is held by premiums, not capability. Answer with evidence (holdouts, reach limits, error rates per case type), self-insure a layer, or partner with an insurer that uses the firm's data |
| **Courts and tribunals deal with persons** | [seen] | Hearings, rent tribunal challenges and enforcement contacts need people indefinitely; small volume, small team |

**What survives.** The architecture survives intact. Nothing in today's rules requires a person inside the routine pipeline. The rules put people at the boundaries the walk had already found: client money, safety, tax, court, councils, complaints and fairness in selection. Two facts could enlarge the human layer: insurers demanding review of every output, and data protection keeping a person in tenant selection. Both are worth engaging early, with evidence. The review's lesson is that the bigger pressure on headcount is not rules at all. It is counterparties who do not reply, and the fix for that is commercial design.

---

## Sources checked for this example
- [Implementing the Renters' Rights Act 2025: roadmap](https://www.gov.uk/government/publications/renters-rights-act-2025-implementation-roadmap/implementing-the-renters-rights-act-2025-our-roadmap-for-reforming-the-private-rented-sector), GOV.UK. Phase dates, database and ombudsman, Awaab's Law and Decent Homes timings.
- [Awaab's Law guidance for tenants in social housing](https://www.gov.uk/government/publications/awaabs-law-guidance-for-tenants-in-social-housing/awaabs-law-guidance-for-tenants-in-social-housing) and [timeframes guidance for social landlords](https://www.gov.uk/government/publications/awaabs-law-guidance-for-social-landlords/awaabs-law-guidance-for-social-landlords-timeframes-for-repairs-in-the-social-rented-sector), GOV.UK. The 24-hour and 10-working-day clocks.
- [Which?: key dates confirmed for Renters' Rights Act reforms](https://www.which.co.uk/news/article/key-dates-confirmed-for-renters-rights-act-reforms-aYmEN6Z3S3w6) and council guidance pages, as cross-checks.
- [Civil penalties under the Renters' Rights Act 2025 and other housing legislation](https://www.gov.uk/government/publications/civil-penalties-under-the-renters-rights-act-2025-and-other-housing-legislation/civil-penalties-under-the-renters-rights-act-2025-and-other-housing-legislation) and [enforcement measures for landlords](https://www.gov.uk/guidance/enforcement-measures-for-landlords-renters-rights-act-2025), GOV.UK. The £7,000 and £40,000 tiers.
- [Non-resident landlords scheme: notes for letting agents](https://www.gov.uk/government/publications/non-resident-landord-guidance-notes-for-letting-agents-and-tenants-non-resident-landlords-scheme-guidance-notes/notes-for-letting-agents) and [paying tax on rent to landlords abroad](https://www.gov.uk/paying-tax-on-rent-to-landlords-abroad), GOV.UK. Withholding, gross approval, agents' returns.
- Practitioner review, `example-lettings-review.md`: turnover, contractor supply, approvals, access, money, fraud and pay levels. Marked [experience, per reviewer] where used.
- Stated from general knowledge and not checked in this pass: deposit penalty levels, right-to-rent penalty levels, the arrears threshold and notice periods for section 8 grounds, the protected first year before selling or moving-in grounds, Making Tax Digital thresholds and dates, the data protection position on automated decisions after recent amendment, the legal position of executors before a grant, typical unoccupancy clauses, and the absence of a statutory licence for letting agents.

## Where this is weakest
- Every volume and cost is a guess scaled from a desk-built inventory, corrected by one practitioner's experience. A bought book's real data would replace all of it within a year.
- The headcount assumes the contractor network can be deepened by payment terms and steady volume; in rural areas even that may not be enough.
- The default on silence and the float are untested with accidental landlords. Some will refuse them, and the weaker promise may not sell.
- The removal schedule assumes outcome data can be collected without relying on tenants' replies; sensors and sampling help but cost money and consent.
- Acquisition is now costed, but churn and book prices are guesses.

---

## Review and response

Each point from the operations director's review, and what this version did with it.

| # | Reviewer point | Response | What changed |
| --- | --- | --- | --- |
| 1 | The example models cases; the work is people who do not reply | **Agreed.** The strongest point in the review | New class of boundary work in 3.22 and 7.2(2); "whose move it is" added to the obligation entity |
| 2 | Landlord approvals stall repairs; needs float, spend matrix, right to act | **Agreed** | Contract preconditions in 1.2; constitution clause 5; matrix and default on silence in 2.5; new event 3.14 |
| 3 | Contractor supply, not dispatch, is the constraint; "three no-shows and suspend" empties rural panels | **Agreed** | 3.8 rewritten: ranking, depth-aware suspension, 48-hour payment (clause 12), guaranteed volumes; network managers added (4 to 6 in 2027 → 5) |
| 4 | Tenant confirmation is a weak verifier; treat silence as unknown | **Agreed** | Clause 10; verifier table in 2.4; independent sampling and sensors; removal evidence in 5.2 no longer relies on replies |
| 5 | Money is messier; unidentified receipts and statement disputes need a person in 2027 | **Agreed** | Suspense account and human approval in 3.4; client accounts line in headcount; separate removal row 7 |
| 6 | Viewings and inspections: self-guided viewings and video self-inspection; half the visits could go by 2030 | **Agreed, with a limit.** Self-guided viewings suit empty homes. Most viewings happen while the outgoing tenant is still in, where consent and safety rule them out; video tours and hosted second viewings fit there | 3.2 and 3.3 rewritten; physical network falls from 37 to 22 by 2030 A |
| 7 | A fifth or more of repairs fixed by guidance | **Agreed** | Video triage agent; 7,500 reports resolved without a visit in the case-type table |
| 8 | Voice agents for early arrears, access and reminders | **Agreed** | Voice added to the front door and used in 3.4 and 3.7 |
| 9 | Non-Resident Landlord Scheme and Making Tax Digital missed; a product, not a risk | **Agreed** and checked against HMRC guidance | Case type 22; event 3.17; landlord tax in prices and stress test |
| 10 | Humidity sensors beat photos for damp | **Agreed, and pushed further**: sensors turn a 12-month outcome into a continuous one, which changes the general rule on slow loops | 3.6; damp moves up the removal order; new point 7.1(6) |
| 11 | Keys and access need their own case type | **Agreed** | Case type 17; event 3.15; access record in state; contract precondition |
| 12 | Leasehold flats: third parties hold the fix | **Agreed** | Case type 19; tenure in state; liaison agent; judgement desk covers stuck cases |
| 13 | Insurance claims with neighbours, block insurers and adjusters | **Agreed** | Case type 20; event 3.16 |
| 14 | Fraud: forged payslips, title fraud, rent-to-rent, bank details | **Agreed, and pushed further**: verify at source rather than review documents better | Clause 11; title check in 3.1; open-banking income in 3.2; event 3.21; fraud sentinel |
| 15 | Landlord events: death, receivers, sale, leaving mid-tenancy | **Agreed** | Case type 21; event 3.18; authority holders in state |
| 16 | Council enforcement wants a named person; higher civil penalties | **Agreed** and checked: £7,000 and £40,000 tiers | Event 3.19; stress test row |
| 17 | Voids: frozen pipes, unoccupancy clauses, council tax | **Agreed** | Case type 18; event 3.20 |
| 18 | Neighbours and behaviour: ASB, subletting, cannabis farms, warrants | **Agreed** | Cross-cutting stream; event 3.20 |
| 19 | Turnover of near 60% is wrong; 25 to 35% is typical | **Agreed.** It was an error | Volumes rebuilt at 30% plus let-only |
| 20 | Physical network undercounted; about 50 FTE | **Partly agreed.** Reviewer's figure used the inflated volumes. Recounted at corrected volumes with the same hours per visit: 37 | Sizing shown in 4.2 |
| 21 | Inside the firm, 55 is too low by about 25; about 80 in 2027, 45 to 55 in 2030 | **Largely agreed.** Now 81 in 2027. 2030 is 53 in A and 72 in B; B is above the reviewer's range because B assumes slow adoption and retained scaffolding | Headcount table rebuilt with all five missing roles |
| 22 | Judgement desk of 14 is light | **Partly agreed.** Raised to 18, sized from workload. Not raised further, because the spend matrix and default on silence remove most approval traffic | Sizing shown in 4.2 |
| 23 | Never remove the night on-call person | **Agreed** | Removal row changed to "never removed"; permanent line in headcount |
| 24 | Traditional revenue understated (maintenance commission, interest, referrals); costs overstated (£35,000 to £45,000) | **Agreed** | 6.1 rebuilt; traditional margin now 15 to 25% and the 2027 gap now small. This is the most important consequence of the review for the business case |
| 25 | Acquisition cost missing; books trade at a multiple of fees | **Agreed** | Acquisition line in costs and headcount |
| 26 | Low-fee online managers retreated; £65 subscription will be bought by portfolio landlords | **Agreed on the segment, with a reason.** Those firms removed people without replacing the coordination. This design keeps a named person and a network, so it is not the same bet. But the single £65 price did not cover 2027 cost, which the first draft hid | Two price tiers; named-person tier for accidental landlords |
| 27 | Buy a book in one dense region and migrate it | **Agreed**, and it fixes the launch economics | First item in 6.3 |
| 28 | Make the contractor network the first product | **Agreed, and pushed further**: sell it to self-managing landlords too | 6.3 and 6.4 |
| 29 | Fix approvals in the contract | **Agreed** | See point 2 |
| 30 | Start with portfolio and build-to-rent clients | **Partly disagreed.** They are the right buyers of the low-price tier and the interface. But a bought book will be mostly accidental landlords, and they are where the compliance guarantee and the duty design earn most. Starting with both segments, priced differently, is better than choosing one | Two tiers in 6.3 |
| 31 | A named patch lead per 400 to 600 landlords, for escalation and retention | **Agreed at 600 for launch.** The ratio should widen to about 1,000 by 2035 as agents carry routine contact, because the role is escalation and retention only | Patch lead line replaces the premium relationship line |
| 32 | Build access, fraud controls and leasehold liaison from day one | **Agreed** | Case types 17, 19 and the fraud stream |
| 33 | Sell the compliance guarantee first | **Agreed** | Guarantees list in 6.3 |
| 34 | Maintenance commission as revenue | **Disagreed for the agent-first firm.** Hidden commission conflicts with clause 10 (honesty) and the live-status promise. Replaced with a disclosed dispatch fee, which also sells | 6.3 |
