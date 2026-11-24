# Level 3. Claims handling and loss adjusting for UK insurers, redesigned from scratch

Draft by Claude, 24 November 2026. One author, no sub-agents. A stress test of the architecture that came out of `level3-accountancy.md` and `level3-lettings.md` ([element] to [element]). It follows the six-step procedure in `step-3c-the-electricity-test.md` and the kinds of human need in `step-3b-the-agent-enterprise.md`. Today's rules and institutions are facts to design around; they are applied in full only in section 10. A few facts were checked on 24 November 2026; sources are at the end. Revised the same day after two reviews, one from a builder and one from a buying claims director; section 11 says what changed and why.

Labels:
- **[seen]** exists somewhere today, with source;
- **[reasoned]** follows from logic;
- **[conjecture]** plausible towards 2035.

---

## The answer in brief

Level 1 asks: "how do agents run a claims firm?" This paper asks: "what would an insurer buy if nobody had ever built a loss adjuster?"

1. **A loss adjuster exists to close an information gap.** At the loss, the insurer does not know what happened, what the thing was like before, what the policy says, or what repair should cost. The policyholder knows some of this and has a reason to shade it. Most of today's work is closing that gap late, by hand, at a distance [reasoned].
2. **Close the gap before the loss.** Cover can be known in advance (wording compiled into rules at bind). So can the thing's condition (a pre-loss baseline). What happened can be captured at the loss, from devices, telematics, weather and the phone, with provenance. Then most of the adjuster's informational role disappears [reasoned].
3. **Reverse the default.** For in-envelope losses, the insurer's agent starts restoration within the hour and pays the repairer on verified completion. The policyholder confirms rather than proves. The claim stops being a request to argue over and becomes an obligation being discharged [reasoned].
4. **Move upstream: sell an intact home or car, with claims as the failure case.** The firm already runs the sensors, the baseline and the first-hour crews. So it should also fix the failing valve the sensor flagged, not only dry the floor afterwards. It is paid per policy-year, plus a share of lower claim frequency measured against a matched control book [reasoned; size of the frequency effect is conjecture].
5. **Promise restoration by a date, not a sum.** Co-design policies that promise the thing put right to a standard by a date, with cash on request at a fair market rate. Then most claims have no "quantum" to argue over: there is a job, a date and a sign-off [reasoned].
6. **Own the scarce part.** The firm owns regional drying and make-safe crews, bought rather than built, and contracts priority trade capacity with penalties. It is a portable layer inside insurers' claims systems. It proposes a neutral exchange and gives it away; it does not own the insurer's ledger or the exchange [reasoned].
7. **People stay where claims are physical, adversarial or human.** For 200,000 claims a year: about 220 core people in 2035 under landscape A and 290 under B, against about 850 in a traditional firm, plus about 250 people in owned crews [conjecture]. The bigger prize is lower indemnity and fewer losses, not lower expense.
8. **The architecture test.** [element] [verdict removed], [element] [verdict removed], [element] [verdict removed], [element] [verdict removed] (once the product is risk care), [element] [verdict removed], [element] [verdict removed], [element] [verdict removed], [element] [verdict removed]. Nothing breaks outright, but almost everything bends, and the bends share causes: parties with opposed interests, inputs that lie, demand that arrives in storms, revenue that can rise with losses, and a firm that both judges and repairs. The architecture lacks a neutrality layer, adversarial design, physical surge capacity, a balance sheet for physical promises, long-tail time, limits on using evidence against its owner, and control of self-dealing (section 9).

---

## 1. The client's outcome, segment by segment

### 1.1 What each party wants to be true

| Party | What should be true, and when | Measure |
| --- | --- | --- |
| **Insurer** (the paying client) | Continuously: fewer losses; valid losses paid accurately, fast and fairly; nothing paid that should not be; lowest total cost of risk net of recoveries; Consumer Duty evidenced; case reserves right | Claim frequency against a control; indemnity per policy-year; verified leakage; expense ratio; recovery yield; case reserve accuracy; Ombudsman upholds; acceptance consistency |
| **Policyholder** | Before any loss: no loss, and no surprise about what is covered. At the loss and until restored: made whole fast, with little effort; treated as honest; a person when it matters | Losses avoided; hours to mitigation; days to restoration; minutes spent; repair complaints; vulnerable customers served |
| **Third-party claimant** | At the loss: paid fairly and fast without a middleman | Days to offer; share settled without a claims firm or solicitor |
| **Reinsurer and Lloyd's** | Continuously, and at a catastrophe: data they trust without auditing | Days to a credible event estimate; reserve surprises |
| **Regulator** | On demand: fair outcomes provable from data | Evidence available within a day |

The FCA reviewed home and travel claims handling in July 2025. It looked at 15 home insurers and asked how they oversee outsourced claims handlers and use management information. It doubted that limited oversight could deliver Consumer Duty outcomes [seen, FCA, via search summary]. FCA figures cited by a House of Lords committee put home claims acceptance at 62% to 71%, against 99% for motor [seen, as reported]. So "fairness provable from data" is not a soft aim. It is what the insurer is being asked for now.

### 1.2 The segments

| Segment | What they want | What they get |
| --- | --- | --- |
| **Capacity providers behind MGAs** (insurers, Lloyd's syndicates, reinsurers) | "Clean, live data and controlled claims across all the MGAs we back" | One approved claims function, placed into many MGAs; live view of every book. **This is the real buyer for the MGA wedge**: capacity providers approve, and often name, the claims handler [conjecture; both reviewers report it from practice] |
| **MGAs and insurtechs** (no claims function of their own) | "Be our claims function, so our capacity provider trusts us" | The firm runs the whole function, on its own stack, under delegated authority |
| **Mid-size insurers, household and SME property** | "Lower total cost of claims, fewer complaints, oversight we can show the FCA" | The firm's agents inside the insurer's claims system; field force and restoration network; fairness evidence |
| **Motor** (own damage, third-party property, injury) | "Cut repair cost and credit hire; settle injury inside the portal" | Telematics-born first notice; fixed-price repair; recoveries cleared between insurers; injury handled through the Official Injury Claim portal |
| **Large and complex commercial** (fire, flood, business interruption) | "A senior adjuster I trust on site within a day, and a number I can reserve to" | Embedded major-loss adjusters, backed by agents reading the business's own ledger and building data |
| **Liability** (employers', public, motor injury; long tail) | "Control of litigation spend and reserves over years" | Litigation managed against outcome data; case reserves live and their data certified. Book reserves stay with the insurer's actuaries |
| **Lloyd's and the London market** | "Clean data and claims control across delegated business" | Coverholder-level claims under delegated authority; data in the market's own claims standard |
| **Self-insured fleets, councils, corporates** | "Our own losses handled as if we were an insurer" | The same service, priced per vehicle or per site |

The policyholder and the third-party claimant are not paying clients. They decide the result all the same, as tenants did in lettings.

---

## 2. Where information is born and decisions are taken

### 2.1 Today

- **Cover** is born in the wording at bind, but read by a handler after the loss, often for the first time.
- **The thing's prior condition** is born over years in the home, car or building, but reconstructed after the loss from photos, memory and the adjuster's eye.
- **What happened** is born in the pipe, the car, the weather and the fire service log, but reported by phone days later and re-collected.
- **Cost** is born in repairers' prices, but gathered and challenged quote by quote.
- **Honesty** shows in patterns across insurers (the Claims and Underwriting Exchange, the Insurance Fraud Bureau), but is judged by referral after the fact.
- **Liability** is born at the scene, but argued in letters between insurers and lawyers.

So the decisions (cover, quantum, liability, fraud, reserve, recovery, settle or litigate) are taken late, by a handler, after a chase. Most of the delay is the chase [reasoned].

### 2.2 By 2035

| Information | Where it is born and captured | What changes |
| --- | --- | --- |
| Cover | Wording compiled into rules at bind; ambiguities flagged to the underwriter before sale | Cover for most events is computable in seconds. Disputes move to wording design [conjecture] |
| The pre-loss baseline | Smart meters, connected boilers, leak sensors, telematics, building systems, a short guided video at inception for higher-value homes, survey data for commercial | "What was it like before" is a record, not an argument [conjecture for scale; leak sensors already offered by Hiscox, Aviva, RSA and Covéa, seen, vendor and insurer pages] |
| The loss | The device or vehicle reports it; the phone captures signed media; weather and peril data are attached | The claim opens itself, often before the policyholder calls [conjecture; vehicle crash data and eCall exist today, seen, general knowledge] |
| Cost | Network prices and repair data across many losses | The estimate is a lookup with checks [seen in part: Tractable's AI Estimating goes from first notice to an approved motor estimate without a person, vendor claim] |
| Honesty | Provenance of each piece of evidence, plus pooled patterns | Fraud is judged on provenance gaps, not on suspicion of the person [reasoned] |
| Liability | Telematics from both vehicles; agents of both insurers apply a shared protocol | Most motor liability settled agent to agent [conjecture] |

**The design rule** [reasoned]: put the firm's capability where cover is defined (at bind), where the baseline is kept (in the insured thing) and where the loss is born (in the device and the phone). Better still, put it where the loss is *prevented*: the same sensor that reports a burst pipe first reports a dripping valve. Do not wait for the claim to arrive at an office.

**A correction on adoption** [conjecture]. Take-up of free leak devices is modest today, and many households never install what is posted to them (the practitioner reviewer's experience; not checked at source). Renters, landlords and older customers are hardest. So born evidence will reach motor first, through the car itself, and household more slowly. The design therefore does not post devices and hope. It fits them during the first contact that brings a person into the home anyway (a prevention visit, a boiler service partner, a previous claim's repair) and it pays for them out of the prevention fee (section 7).

One warning. By the 2030s the policyholder's own AI agent will file claims, and fraudsters will use the same tools to fabricate evidence [conjecture]. Evidence born on a device with a provenance trail becomes more valuable, and a photo emailed in becomes worth less. That is a central design fact, not a side issue.

---

## 3. What disappears, what becomes a side effect, what remains

### 3.1 The mechanisms

- **Cover is known before the loss, by both sides.** At bind the policyholder is shown, in plain words, what each likely loss would and would not pay. Home acceptance of 62% to 71% reflects surprise as well as fraud [reasoned]. Fixing surprise at sale cuts declines, and declines set the size of the judgement desk. Only genuine ambiguity remains, and it goes back to wording.
- **Losses are prevented.** Sensor alerts lead to a repair visit, paid by the firm, before a loss. A claim is the failure of the service, not its product [reasoned].
- **The baseline exists.** Wear-and-tear and "was it like that before?" disputes shrink. Wear and tear and storm disputes were a focus of the FCA's 2025 work [seen, FCA via search].
- **The loss reports itself.** First notice by phone, and the chasing after it, mostly go.
- **Standing authority replaces approvals,** set by peril, value and evidence grade once a year. Delegated claims authority already works this way at lower levels [seen, general knowledge].
- **Restoration starts at once.** Drying in the first hours shrinks the loss itself. Water damage grows fast in the first two days, so speed is an indemnity saving [reasoned].
- **Restoration is the promise.** The policy promises the thing put right to a standard by a date. Cash is paid on request, at the rate the policyholder would pay their own builder, not the network's discounted rate. There is no quantum to negotiate [reasoned].
- **First-response cash.** When a sensor or flood gauge confirms the event, a small fixed sum lands within the hour for emergency costs, before any assessment [conjecture].
- **Money follows evidence,** paid to the repairer on verified completion.
- **Recoveries clear between insurers** by netting, not letters [conjecture].

### 3.2 Today's main work, line by line

| Today's work | At level 3 | Why |
| --- | --- | --- |
| First notice of loss by phone or form | **Disappears** for instrumented risks; a guided capture for the rest | The loss is born on a device or captured with provenance |
| Coverage verification | **Disappears**; ambiguity goes to a judgement desk and back to wording | Cover compiled at bind and shown to the policyholder then |
| Triage and allocation | **Side effect** | The orchestrator routes by evidence grade and value |
| Desk adjusting and reserve setting | **Side effect** for most; judgement for complex | Reserve recomputed from live evidence and network prices |
| Routine site visit to validate | **Mostly disappears**; replaced by device data, guided video and short technician visits | Validation from the baseline and the loss record |
| Loss adjuster's report | **Disappears** as a document; the record is the report | Nobody writes up what the record holds |
| Gathering and challenging quotes | **Disappears** | Fixed-price restoration from the network |
| Appointing contractors and chasing | **Side effect** | Dispatch within standing policy |
| Payment authorisation | **Side effect** | Payment on verified completion within authority |
| Settlement negotiation (household, small commercial) | **Mostly disappears** | Restoration by a date is the promise; where cash is chosen, it is priced at a fair market rate; a person handles disagreement |
| Major-loss adjusting (fire, flood, business interruption) | **Remains**, changed | Senior people on site; agents read the business's ledger and building data |
| Fraud referral and investigation | **Remains**, smaller in volume, harder per case | Provenance gaps flag cases; investigators handle organised and novel fraud |
| Subrogation: spotting recoveries | **Side effect** | Cause and liable party known from the record |
| Pursuing recoveries | **Mostly disappears** for insurer-to-insurer; remains against uninsured parties | Netting through the exchange |
| Motor liability decisions | **Mostly disappears** | Shared protocol, telematics on both sides |
| Credit hire disputes | **Shrinks** | The referral is sold upstream, before anyone else calls. So the design changes the referral economics, not the call race (section 4, item 11) |
| Injury claims through the portal | **Remains**, partly automated | The Official Injury Claim portal takes about 54,000 to 61,000 claims a quarter, about 96% with a whiplash tariff element [seen, OIC data; my sums] |
| Litigation management | **Remains** | Courts, lawyers, long tail |
| Complaints | **Remains**, fewer | Fewer causes; human handling of the rest |
| Vulnerable customer identification | **Changes**: signals detected early, people deployed | A person for people in crisis |
| Bordereaux and management reports | **Side effect** | Live data to insurer, Lloyd's and reinsurer |
| Insurer file audits | **Disappear**; replaced by live access and fairness evidence | The insurer sees the state |
| Catastrophe surge | **Changes**: pre-positioned from the forecast | See section 4 |

Of these 23 lines, 9 disappear or mostly disappear, 6 become side effects and 8 remain, shrink or change shape. That is a smaller share than in accountancy, because more of what remains is physical, adversarial or human [reasoned].

### 3.3 Why this is not level 1 done better

A level 1 firm automates the phone call, the coverage check and the adjuster's report. It is faster but still learns about the loss days later and still argues about what was there before. Level 3 changes when information exists. That cuts the loss itself (water stopped in hours, not days), and, once the firm runs prevention, the number of losses. It removes the argument too, because the promise is a restored home by a date, not a sum. Indemnity is roughly ten times expense, so this is where most of the money is [reasoned; ratio is a conjecture for a typical book].

---

## 4. What appears that did not exist before

1. **Coverage as code, shown to both sides.** Wordings compiled into rules at bind. The underwriter sees which events are ambiguous before the policy is sold. The policyholder sees, in plain words, what each likely loss would and would not pay. This is a wording-design product the firm can sell on its own [conjecture].
2. **The pre-loss baseline.** The insured thing's condition, kept up by devices and short captures. The policyholder owns it; the insurer reads it under consent. For commercial risks, a "loss-ready file": plans, valuations, stock and ledger access agreed in advance [conjecture]. **The baseline-use rule** [reasoned]: the baseline may be used to pay faster without limit. It may be used to decline or reduce only where the policyholder was told at the time. A leak alert the customer saw and ignored is fair to use. A reading they never saw is not. Without this rule, better evidence produces more gradual-damage declines, and an insurer that instruments homes and then declines more will be on the front page.
3. **Prevention as the main service.** A sensor flags a weeping valve or a failing hose; a technician fixes it within days, paid by the firm, because a £150 visit is cheaper than a £5,000 claim. The aim is "loss avoided" first and "loss contained" second [reasoned; costs are conjecture].
4. **Mitigation in the first hour.** A drying or make-safe crew, owned by the firm, goes when a leak sensor trips, before any claim [reasoned].
5. **Restoration by a date as the policy promise.** A standard, a date and a workmanship guarantee per peril and size, with the firm carrying the variance up to a cap per event. Cash on request, at a fair market rate [conjecture].
6. **First-response cash.** A parametric sum paid within the hour of a confirmed event, for emergency costs [conjecture].
7. **Catastrophe readiness as a data product.** On a storm forecast, the firm models the footprint, opens claims for instrumented homes before anyone calls and gives reinsurers a credible event estimate within days. Physical surge comes from owned crews and contracted priority capacity, not from names on a list [conjecture].
8. **Live fairness evidence.** Acceptance, reductions, offers and times by peril and customer group, so the insurer can show the FCA on demand that outcomes do not differ without reason [reasoned].
9. **Evidence provenance.** Every photo and reading carries its origin and any alteration. Claims are graded by evidence, not by suspicion of the person [reasoned].
10. **A shared protocol between insurers.** Insurers' agents settle liability and net recoveries daily under an open protocol, held by a trade or standards body, not by the firm [conjecture].
11. **A replacement-car protocol that removes the referral margin.** The credit hire referral is sold by whoever the not-at-fault driver calls first, usually their own insurer or broker. Racing for that call loses. Instead, under the shared protocol, the not-at-fault insurer provides a like-for-like car at once and is repaid by the at-fault insurer at a protocol rate, cleared through daily netting, with a handling fee that competes with the referral fee. Liability is agreed in minutes from both cars' data. The referral stops being worth selling [reasoned; whether insurers will give up referral income is conjecture]. The industry has run voluntary rate agreements on credit hire for years, so this extends an existing habit [seen, general knowledge].
12. **The claimant's agent as the most demanding user.** By the 2030s the policyholder's own AI will file the claim, compare outcomes, cite Ombudsman decisions and complain in seconds [conjecture]. The firm designs for that agent first: an open record, machine-readable reasons for every reduction, restoration started within the hour, and evidence accepted only with provenance. If nothing is hidden and the work has started, the agent has little to argue about [reasoned].
13. **Claims and prevention as live underwriting data,** instead of quarterly reports [reasoned].

---

## 5. Where the firm's capability sits, and the boundary

### 5.1 By segment

| Segment | Where capability sits |
| --- | --- |
| MGAs | The firm is their claims function, on its own stack |
| Mid-size insurers, property | Inside the insurer's claims system; in the policyholder's phone through the insurer's app; in devices; an embedded lead in the insurer's team; field technicians locally |
| Motor | Vehicle data feeds, repairers' estimating systems, the injury portal, the exchange |
| Large commercial | The business's ledger (for business interruption), building systems; major-loss adjusters on site within a day |
| Capacity providers and reinsurers | A live view across every MGA book the firm handles; event estimates in a catastrophe |
| Liability | Court and solicitor systems, medical reporting, the insurer's reserving |
| Lloyd's | The market's claims data standard |

The capability sits in three worlds at once: the insurer's systems (authority and money), the policyholder's world (where the loss is born, and now where it is prevented) and counterparties' systems. In accountancy and lettings it sat mainly in one.

There is also a reverse embedding. The regulator holds the insurer responsible for outsourced claims [seen, FCA 2025 review], so the insurer reads the firm's state in real time. Oversight becomes a view, not an audit.

### 5.2 The boundary choice

| Option | For this service |
| --- | --- |
| **Own the platform** (the claims ledger itself) | Right for MGAs, which have none. Wrong for insurers. Their claims ledger holds reserves, solvency data and reinsurance; they will not hand it to an outsourcer, and core systems change every ten years or so [reasoned] |
| **Build on a platform** (the insurer's core system) | Necessary but not enough. Each insurer's system differs, so tying the firm to one vendor limits its market [reasoned] |
| **Portable layer** | **The main choice.** The firm's agents, engines and field force plug into any insurer's claims system through interfaces. Evidence, coverage code and restoration live in the firm; reserves and payments are recorded in the insurer's ledger |

**Recommendation** [reasoned]: own the drying and make-safe crews, the field force, the prevention service, the evidence and coverage engines and the accountability; contract priority trade capacity with penalties; be a portable layer in insurers' systems; run a full stack for MGAs; and propose the shared protocol, then give it away.

**The exchange: propose it, give it away, be its best user.** Provenance, the coverage-code schema, recoveries netting and the replacement-car protocol are worth something only if competing insurers use them. They will not join a utility founded by one outsourcer. The UK's shared utilities (the Claims and Underwriting Exchange, the Insurance Fraud Bureau, the Motor Insurers' Bureau, the injury portal) were formed by insurers through trade bodies, or by statute [seen, general knowledge]. The first draft had the firm co-found the exchange with a capped stake; both reviewers said that gives the firm little and needs allies it does not have, and they are right. So the firm writes the specifications, publishes them openly, and offers them to a trade body or market standards body to own [reasoned]. Its advantage is being the first and best user, with years of data already in the format, not owning the rails. The London market is building a common claims data standard while Lloyd's moved away from Blueprint Two in March 2026 [seen, as reported]. Standards can win where big platforms stall.

### 5.3 Who else is in the picture

| Player | What they are doing | How the firm stands |
| --- | --- | --- |
| **Global adjusters and claims administrators** (Sedgwick, Crawford and others) | Large field networks; automating at level 1; publishing on AI and outsourced oversight [seen: Sedgwick reports, June and September 2026] | **Competitor.** They win any contest bought by headcount, such as catastrophe surge. The firm must win on prevention, indemnity outcomes and fairness evidence, not price per claim or bodies per storm |
| **Insurers' own claims functions** | Large insurers bring AI in-house; consolidation (Aviva bought Direct Line in 2025) [seen, general knowledge] | **Client for layers, rival for the core.** Sell prevention, field, restoration, event estimates and fairness evidence even where the insurer keeps handling |
| **Claims AI vendors** (estimating, fraud scoring, document reading) | Selling tools to insurers [seen: Tractable with Ageas and Aviva] | **Suppliers.** Rent their models; own the outcome and the network |
| **Core system vendors** | Adding agents to their platforms [seen in part, general knowledge] | **Rails.** Integrate; never depend on one |
| **Repair networks and trades** | Short of skilled labour [seen, general knowledge] | **Owned where speed decides the loss** (drying, make-safe, small repairs), bought as small regional firms; **contracted with priority and penalties** for building trades. Capacity limits every speed promise |
| **Credit hire firms, claims management companies, claimant solicitors** | Profit from delay and from referral fees paid upstream [seen, general knowledge] | **Adversaries.** Remove the referral margin through the shared protocol; parametric cash and an open record leave less to sell |
| **Device and car makers** | Hold loss data at birth | **Data partners** under consent |
| **Shared utilities and regulators** | Rules and data | **Design within;** seek recognition of provenance standards |

**The 2035 contest** [reasoned]: who holds the evidence at the moment of loss, and who controls restoration capacity. Insurers hold authority and money. Vendors hold models. The firm aims to hold the months before a loss, the first hour after it, and the proof that what followed was fair.

---

## 6. The organisation

### 6.1 The agent architecture

One shared state, as step 3b requires. Its centre is not a claim queue but **each insured risk**, and within it **each loss record**: evidence with provenance, cover result, baseline, restoration plan, money, decisions with reasons. Above it sits **each insurer's book**: its conditions, authority, fairness metrics and reserves.

| Layer | Agents |
| --- | --- |
| **Per risk** | Risk agent: watches device signals, books prevention visits, keeps the baseline current |
| **Per loss** | Loss orchestrator: one writer per loss; acts within the insurer's authority |
| **Per insurer book** | Book agent: watches the conditions in 6.4, live to the insurer |
| **Shared engines** | Coverage, provenance, estimating, reserve, liability, recovery, restoration dispatch, catastrophe planning |
| **Money** | Payment agent, paying from the insurer's claims fund on verified completion |
| **Counter-fraud** | Pattern engine across books and shared databases, separate from settlement |
| **Counterparties** | Insurers' systems, the exchange, repairers, device feeds, the injury portal, solicitors, claimants' agents |
| **Verification** | Independent recomputation of quantum; independent re-scoping of a sample of completed jobs; **fairness monitor**; vulnerability monitor |
| **Governance** | Constitution auditor; separate circuit breakers on payments, on declines and reductions, and on payment clustering near any authority level |

**Six constitution clauses that this service needs** [reasoned]:
- **Asymmetric authority, split by where the reason came from.** Agents may pay within graded authority. They may apply a reduction automatically only if it comes from a rule the policyholder was shown at bind: the excess, a declared sum insured, a stated limit. The reason is given in plain words, with a one-tap route to a person within a day. Discretionary reductions (betterment, partial wear and tear, causation) and declines need a named person, until evidence earns a change. The first draft required a person for every reduction; the practitioner reviewer pointed out that reductions touch almost every claim, so the desk would have scaled with volume. The reason for the asymmetry is also corrected. It is not that paying is cheap to reverse: paid money is almost never recovered from a policyholder. It is that a wrong "no" harms a person and goes to the Ombudsman, while a wrong "yes" costs money the fraud and payment controls are built to limit. UK data protection law also restricts solely automated decisions with significant effects [seen, general knowledge; scope changed by the Data (Use and Access) Act 2025, not checked in detail].
- **No visible cliff.** Payment authority is graded by evidence grade, not by a fixed sum, so there is no threshold to cluster claims beneath. The payment breaker watches for clustering anyway, because automatic thresholds attract claims just below them [reasoned; clustering is the practitioner reviewer's experience].
- **Fairness firewall.** No agent or person who decides settlement can see the firm's savings-share revenue or targets. The commercial layer cannot change settlement thresholds.
- **Scope separation.** The firm both scopes repairs and earns on doing them, so it could pay itself. Scope is set by the estimating engine, not by the crew, and shown to the policyholder. Restoration is paid per job band, not per pound of scope. An independent sample of completed jobs is re-scoped each month and the result published to the insurer [reasoned; from the builder review].
- **Fraud separation.** The fraud engine flags; it never settles. Settlement agents never see a fraud score, only a request for more evidence.
- **Neutral evidence, used fairly.** The loss record is shown to the policyholder, who may add to it. Evidence is never edited, only added. The baseline-use rule (section 4, item 2) applies: evidence the policyholder never saw may help them, never surprise them.

### 6.2 The people, by kind of need

| Kind of need | Role | What they do |
| --- | --- | --- |
| **1. Purpose** | Owners and board | Constitution, risk appetite, capital, the protocol proposal |
| **2. Definition of good** | Standard-setters by line (household, motor, commercial, liability) and for fairness, fraud and vulnerability | Own tests and thresholds; decide what a fair offer is; audit samples |
| **3. Answerability** | Accountable officers with deputies: head of claims, conduct officer, head of claims funds, head of data and reserves | Answer to insurers, the FCA, Lloyd's, the Ombudsman and courts |
| **4. Capability gaps** | Judgement desk | Coverage ambiguity, discretionary reductions, unusual causation, all declines, appeals against rule-based reductions |
| **5. Client demand for a person** | Crisis and vulnerability team; client leads | People after fire, flood and bereavement; the insurer's or capacity provider's named lead |
| **6. Physical world** | Field and prevention technicians; owned drying and make-safe crews; major-loss adjusters; network managers | Fit devices, fix flagged faults, validate, measure, dry, make safe; run large losses on site; manage contracted trade capacity |
| **7. Adversarial** (new) | Counter-fraud investigators; litigation and injury specialists | Organised fraud; courts; claimant lawyers |
| **Scaffolding** | Shadow reviewers; builders and evaluators; trainees | Removed or reduced as evidence allows, except trainees |

The adversarial need is new. Step 3b's six kinds did not include it. It is permanent, because the opponent also improves [reasoned].

**The training route** [reasoned]. Adjusters learn by visiting hundreds of ordinary losses. If ordinary losses need no visit, that school closes. So trainees rotate through field work, blind re-adjustment of past losses, the judgement desk and a catastrophe deployment each year. Owned crews and prevention visits partly reopen the school: trainees spend their first months in homes again, with drying and make-safe crews, seeing ordinary losses at first hand. Whether this counts towards qualifications is for the Chartered Institute of Loss Adjusters to answer, asked in 2027.

### 6.3 Rhythm

- **Continuous:** losses born, cover computed, restoration dispatched, payments made, fairness and fraud monitored.
- **Daily:** people decide declines and clear exceptions.
- **Weekly:** each client lead reviews the book with the insurer or capacity provider; prevention visits are planned from the week's device alerts.
- **Event mode:** a named storm switches the firm to surge: pre-position owned crews, call contracted priority capacity, open claims from the footprint, report an event estimate to reinsurers daily.
- **Quarterly:** case-reserve data certified to the insurer's actuaries, who set the book's reserves. The first draft said the firm would certify reserves; the practitioner reviewer is right that reinsurers will not take an outsourcer's certificate in place of the insurer's.
- **Annually:** authority and wording review with each insurer.

### 6.4 What the firm keeps continuously true for each insurer

For each instrumented risk: it is watched, and every flagged fault is fixed within an agreed time. For the book: no loss waits on the firm; case reserves match evidence today; fairness metrics, including reductions, are within bounds; every vulnerable customer has a person; the insurer and capacity provider can see everything. The first set is a condition of the client's "thing", the insured risk. That is why [element] now holds (section 9).

### 6.5 Headcount for a book of 200,000 claims a year [conjecture]

The reference book: about 120,000 household, 60,000 motor, 15,000 commercial property and 5,000 liability claims a year, roughly £800 million of indemnity. That is a realistic book for a mid-size outsourcer serving a mid-size insurer and several MGAs. The firm will not carry this whole book in 2027 (section 8); the table shows what it would take in each year.

Assumptions (revised after review):
- **Share of losses with a baseline or device data**: 10% in 2027; 35% (A) or 25% (B) in 2030; 60% (A) or 45% (B) in 2035. Motor gets there faster than household; the first draft's 70% was a stretch for household.
- **Share of property losses needing a person on site**: 25% today, falling to 14% (A) or 18% (B) by 2035.
- **Rule-based reductions are automated** with a fast human appeal; discretionary reductions and declines stay human. Restoration in kind removes most quantum disputes. The judgement desk scales with declines, discretionary reductions and appeals, not volume.
- **Owned crews are counted separately**, so the core can be compared with a traditional firm, which does not count its repairers either. Contracted trades and accredited adjusters on retainer are not counted.

| Role | 2027 | 2030 A | 2030 B | 2035 A | 2035 B |
| --- | --- | --- | --- | --- | --- |
| Owners and board | 3 | 3 | 3 | 3 | 3 |
| Accountable officers and deputies | 6 | 6 | 6 | 6 | 6 |
| Standard-setters | 8 | 8 | 8 | 7 | 8 |
| Judgement desk | 90 | 45 | 60 | 20 | 34 |
| Major-loss and commercial adjusters | 28 | 24 | 26 | 18 | 22 |
| Liability, injury and litigation | 40 | 25 | 32 | 14 | 24 |
| Counter-fraud investigators | 24 | 18 | 20 | 16 | 18 |
| Field technicians | 60 | 48 | 55 | 38 | 48 |
| Prevention team (planners and technicians) | 10 | 18 | 16 | 16 | 14 |
| Crisis and vulnerability team | 45 | 35 | 40 | 28 | 34 |
| Client leads (insurers and capacity providers) | 6 | 8 | 8 | 8 | 8 |
| Network managers | 14 | 10 | 12 | 8 | 10 |
| Shadow reviewers | 40 | 12 | 25 | 0 | 10 |
| Builders and evaluators | 30 | 22 | 26 | 15 | 20 |
| Operations, funds, complaints | 30 | 20 | 24 | 14 | 18 |
| Trainees | 12 | 12 | 12 | 10 | 12 |
| **Core total** | **446** | **314** | **373** | **221** | **289** |
| Owned drying and make-safe crews (separate) | 30 | 180 | 160 | 260 | 240 |

| Comparison, same book, core people | 2027 | 2035 A | 2035 B |
| --- | --- | --- | --- |
| Traditional firm | about 850 | about 650 (incumbents automate somewhat) | about 700 |
| Level 1 agent-first firm | about 600 | about 280 | about 420 |
| **Level 3** | **446** | **221** | **289** |

The traditional figure comes from rough ratios: about 450 desk handlers, 90 field adjusters, 40 liability handlers, 35 major-loss adjusters, plus fraud, supply chain, complaints, management and systems [conjecture]. The crews figure assumes owned crews handle drying and make-safe for about 40,000 jobs a year by 2035, at about 150 jobs per person [conjecture].

### 6.6 What drives the numbers

1. **The share of losses with a baseline and born evidence.** Adoption of devices and guided captures, not model capability, sets 2027 to 2030. Fitting devices during visits that happen anyway matters more than posting them [reasoned].
2. **The decline and reduction rules.** The judgement desk floor is set by declines, discretionary reductions and appeals. Clear cover at bind and restoration in kind reduce these more than better models do [reasoned].
3. **Physical work.** Field and major-loss staff shrink slowly. Devices remove visits to check; they add visits to prevent; they do not remove visits to measure, make safe or rebuild [reasoned].
4. **The adversary.** If AI-made fake evidence outruns provenance, investigators and field visits rise again [conjecture].
5. **Catastrophe years.** A bad storm year doubles demand for weeks. Owned crews and contracted priority capacity absorb it, not the core.
6. **The review rule.** If insurers and the FCA accept sampling plus independent recomputation, shadow reviewers go by the early 2030s.

**The honest point.** The 2035 A gap between the level 3 core and a good level 1 firm is about 20%. Most remaining people are physical, adversarial or caring, and those do not shrink much with capability. The case for level 3 is not headcount. It is fewer losses, smaller losses, fewer frauds paid, more recoveries and less credit hire.

---

## 7. Economics

**All of this section is conjecture**: arithmetic on assumed numbers, to show the shape.

### 7.1 Baseline

On the reference book, today's fee pool for claims handling and adjusting is perhaps £60 million, about 7.5% of indemnity, or £300 a claim on average. A traditional firm earns perhaps 8% to 12% margin on it. Leakage (paid when it should not have been, or paid more than needed) is often put at several per cent of indemnity across the industry [conjecture; industry estimates vary]. Detected fraud alone was £1.16 billion in 2024 and £1.34 billion in 2025 across UK general insurance [seen, ABI as reported]. Motor insurers paid £11.9 billion in 2025 across 2.5 million claims [seen, ABI].

### 7.2 What is sold, and how it is priced

| Product | Price | Why this shape |
| --- | --- | --- |
| **Claims capability per policy-year** | A fee per policy in force, by line | A per-claim fee pays the firm for losses. A per-policy fee pays it for the book [reasoned] |
| **Prevention fee** | A share of the fall in claim frequency, measured against a control | Pays the firm for losses that never happen. The control is built by rolling devices out in a randomised order across the book, so the counterfactual is designed in, not argued about afterwards [reasoned]. The firm pays for devices and prevention visits out of this fee, which answers "who pays for the devices?" |
| **Restoration by a date** | A price band, date and workmanship guarantee per peril and size; owned crews paid per job band | The firm carries repair variance up to a cap per event. That is contracting risk after the event, not insurance risk, but across a storm season it still needs a balance sheet (below) [reasoned; take advice] |
| **Verified savings share** | 15% to 20% of savings, counted only from fraud stopped, recoveries, repair price and avoided credit hire; never from lower acceptance, more reductions or lower offers on valid claims | Behind the fairness firewall, with floors on acceptance and complaint outcomes. **The audit method is agreed and fixed before the contract is signed**, or the share becomes an annual argument (practitioner review) |
| **Major loss, liability and litigation** | Time and outcome-adjusted fees | Remains bespoke |
| **Data and event estimates** | Fee for certified case-level data to capacity providers, reinsurers and Lloyd's; event estimates within days of a catastrophe | Trustworthy data is an outcome in itself, and it is sold to the buyer behind the buyer |

**The capital boundary, made sharper.** The firm still does not guarantee the insurer's loss ratio. Guaranteeing total cost of claims is taking insurance risk. It needs capital and authorisation, and it is the incentive the FCA worries about most in outsourced claims [reasoned]. But "take advice" is not enough for restoration variance, which is the firm's largest risk. So: a per-event cap from day one; from about 2030, a protected cell, or a quota-share with a reinsurer partner, that carries restoration guarantees and later prices loss-ratio guarantees from the firm's data. Otherwise the reinsurer captures all the value of that data (builder review) [conjecture].

### 7.3 By landscape, reference book, 2035

Revenue is now larger than today's £60 million fee pool, because the firm does drying and make-safe work that today sits inside indemnity paid to repairers.

| £ million a year | A (capability compounds) | B (plateau) | D (price collapse) |
| --- | --- | --- | --- |
| Per policy-year fees | 20 | 24 | 7 |
| Prevention fee | 8 | 5 | 4 |
| Owned crews' work (about £40m of the £250m repair spend) | 40 | 38 | 36 |
| Network restoration margin (about 4% on £210m) | 8 | 8 | 7 |
| Verified savings share | 8 | 6 | 4 |
| Major loss, liability, litigation | 7 | 7 | 6 |
| Data and event estimates | 4 | 4 | 3 |
| **Revenue** | **95** | **92** | **67** |
| Core people (221 / 289 / about 200 at lower pay) | 17 | 22 | 12 |
| Owned crews: people, vans, drying kit, materials | 31 | 31 | 30 |
| Devices and prevention visits | 7 | 6 | 6 |
| Compute and tools | 5 | 4 | 3 |
| Overhead, insurance, workmanship guarantee provision | 8 | 8 | 6 |
| Cost of capital for restoration guarantees | 3 | 3 | 3 |
| Exchange fees and partner costs | 2 | 2 | 2 |
| **Cost** | **73** | **76** | **62** |
| **Margin** | **about 23%** | **about 17%** | **about 7%** |

The first draft showed 44% under A. Both reviewers rejected it: owned crews carry people and vans, and procurement benchmarks margins down to the mid-20s by the second renewal [conjecture, from both reviews]. The revised figure is lower in percentage and similar in pounds, on a business that is harder to copy.

The insurer's gain is larger than the firm's revenue. The first draft put the indemnity cut at 3% to 5%. With prevention cutting frequency, and mitigation within hours for escape of water, 5% to 8% across the book is the revised working range: £40 million to £64 million on £800 million, plus lower expense [conjecture]. The first winter of the wedge should test for more on escape of water, where damage grows fast in the first two days.

### 7.4 Where profit comes from

- **Not from handling.** In landscape D, per-claim and per-policy handling fees collapse, because insurers' own AI and every incumbent can do routine handling.
- **From restoration capacity.** Drying, make-safe and skilled trades are scarce, and scarcity holds price in every landscape [reasoned]. This is why the firm owns crews: in D it survives as a restoration and prevention firm.
- **From avoided losses.** Only a firm that runs devices, visits and crews together can be paid for frequency.
- **From verified savings.** Only a firm that can prove it saved money without being unfair can take a share.
- **From accountability and senior judgement** on large losses and litigation.
- **From trusted data** sold to capacity providers and reinsurers.

B now does worse than A, unlike the first draft. Prevention and owned crews both depend on device adoption, which is slower in B.

---

## 8. How it is built from 2027

### 8.1 First wedge

**Capacity providers backing MGAs that write household and small commercial property**, starting with escape of water.

Why [reasoned]:
- MGAs often lack a claims function. But the MGA does not choose its handler alone: the insurer, syndicate or reinsurer behind it approves, audits and often names the handler (both reviewers, from practice) [conjecture]. So the firm sells once to a capacity provider and is placed into several MGAs. The FCA's focus on oversight of outsourced claims [seen] makes a firm that is transparent by design easier to approve.
- Escape of water is the peril where level 3 shows most: devices exist and are offered by insurers today [seen]; prevention and mitigation speed both cut the loss; repair is standard enough for fixed prices.
- Running the whole function for an MGA lets the firm use its own stack from day one, without integrating into an insurer's core system.

**The second wedge is data, not bodies: event estimates for reinsurers.** The first draft proposed catastrophe surge. The builder reviewer is right that surge is bought from panels by headcount and priced as a commodity, and a firm with 60 technicians loses to the global adjusters. Reinsurers instead buy a credible event estimate within days of a storm, from instrumented homes and footprint models. That uses data the firm already has, and it puts the firm in front of the buyer behind the buyer again [reasoned].

### 8.2 What makes clients adopt

- **For capacity providers:** one claims function they can watch live across every MGA they back; event estimates; certified case data.
- **For MGAs:** a claims function in weeks that their capacity provider has already approved.
- **For insurers:** fairness evidence for the FCA; lower indemnity and frequency, proved against a randomised control with the method agreed before signing; no change to their core system.
- **For policyholders:** a device fitted during a visit, not posted; faults fixed free; an excess waiver for instrumented homes (Covéa already offers one with a device, seen); cover explained at bind; a crew within hours; restoration by a date or fair cash.

### 8.3 Sequence to 2035 [conjecture for dates]

| Years | Step |
| --- | --- |
| 2027 | One capacity provider; one or two MGA books; escape of water in two regions; buy one regional drying firm; coverage code for their wordings; about 8,000 to 15,000 claims (the first draft's 30,000 ignored six to twelve months of onboarding and delegated-authority audit per MGA). Measure device take-up, days to restoration and complaint rate on network repairs. Those three decide the rest |
| 2028 | Event-estimate product for reinsurers; priority capacity contracts with penalties; randomised prevention trial results published; second capacity provider |
| 2029 | Motor own damage for MGAs and telematics insurers; publish the shared protocol (provenance, netting, replacement car) and offer it to a trade or standards body |
| 2030 | First mid-size insurer's household book as a portable layer; about 120,000 claims; co-design a restoration-by-date policy with one insurer; protected cell or reinsurer partnership for restoration guarantees |
| 2031–32 | Commercial property and business interruption, with ledger access (linking to the accountancy design's record); Lloyd's coverholder claims |
| 2032–33 | Liability and injury, once litigation outcome data supports it |
| 2035 | 300,000 claims or more; prevention running on most instrumented risks; the protocol used by most UK motor insurers; claimant-agent interface live |

---

## 10. What would make this design wrong, and the stress test

### 10.1 What would make it wrong

1. **Insurers keep claims in-house,** outsourcing only field and restoration. The design survives as a prevention and restoration firm [reasoned].
2. **Devices and baselines are not adopted.** Below a quarter of losses with born evidence by 2030, this is a good level 1 firm with owned crews [conjecture].
3. **Prevention does not cut frequency.** If the randomised trial shows little effect, the prevention fee goes and the firm is a fast restoration business [conjecture].
4. **Network repairs generate the complaints.** Snagging, missed dates and poor finish are already the worst source of complaints (practitioner review). If restoration in kind raises complaints, the promise turns against the firm. The workmanship guarantee, fair cash option and complaint rate measured in the first winter are the defence [reasoned].
5. **Fake evidence wins.** Field visits return and costs rise [conjecture].
6. **The savings share is banned or distrusted.** Margin falls towards landscape D [reasoned].
7. **The shared protocol is not adopted.** Recoveries stay letter by letter and credit hire keeps its referral margin [reasoned].
8. **Repair capacity is the limit.** Dates cannot be promised [seen in part, general knowledge].
9. **Fast payment attracts organised fraud.** The breaker and evidence grades must hold [reasoned].
10. **Core system vendors build the layer free,** squeezing the firm to field, restoration and accountability [conjecture].
11. **The judges run out.** Without ordinary visits to learn on, major loss cannot be staffed in the 2030s [reasoned].

### 10.2 The stress test against rules, institutions, counterparties and adoption

| Fact | Effect on the design |
| --- | --- |
| **Capacity providers and Lloyd's managing agents approve and audit claims handlers under delegated authority** [conjecture as to how often they name them; both reviewers report it] | Sell to them first; build the live view for them |
| **The Financial Ombudsman Service looks at whether cash settlement reflects what the customer would pay, not the insurer's discounted rate** [seen in part, general knowledge; FCA 2025 work touched cash settlement, not checked in detail] | Cash option priced at a fair market rate; restoration in kind is the default, never a trap |
| **Book reserves are set by the insurer's actuarial function under Solvency UK** [seen, general knowledge] | The firm certifies case data, not reserves |
| **Referral fees are banned for personal injury but not for credit hire** [seen, general knowledge, Legal Aid, Sentencing and Punishment of Offenders Act 2012] | The replacement-car protocol must out-compete the referral fee; it cannot rely on a ban |
| **Insurers must handle claims promptly and fairly, and not reject unreasonably** (FCA rules for insurance conduct, ICOBS 8) [seen, general knowledge] | Fits the design. The asymmetric authority rule and fairness evidence answer it directly |
| **Consumer Duty, and FCA focus on outsourced claims oversight** [seen, FCA 2025 review; Sedgwick September 2026 release] | Helps. Live oversight is the firm's selling point. Expect the FCA to scrutinise any savings share: publish the firewall and audit method from day one |
| **The insurer stays responsible for outsourced functions; senior managers are accountable** [seen, general knowledge of outsourcing rules and the Senior Managers regime] | Embed the insurer's view into the firm's state; give the insurer's accountable manager a live dashboard and breaker access |
| **Financial Ombudsman Service** decides complaints on fairness, not just contract [seen, general knowledge] | Calibrate standard-setters' "fair offer" to Ombudsman decisions; feed upheld complaints into tests |
| **Solely automated decisions with significant effects are restricted** under UK data protection law, as amended in 2025 [seen, general knowledge; detail not checked] | Declines stay human; automated payment is favourable to the person. Sensor and vehicle data need consent at inception |
| **Competition law limits sharing between competitors** [seen, general knowledge] | The protocol shares evidence, netting and a replacement-car rate method, not prices or strategy; a protocol rate needs particular care, so it is set by a trade body with legal review, not by the firm |
| **Shared fraud and claims databases require membership** (Claims and Underwriting Exchange, Insurance Fraud Bureau) [seen, general knowledge] | Access through insurer clients at first; seek membership as an outsourcer |
| **Injury claims follow the portal and court protocols; whiplash tariffs set by law** [seen: Civil Liability Act 2018, OIC data] | Injury work remains procedural; automate within the portal; litigation stays with specialists |
| **Lloyd's delegated authority rules; Blueprint Two moved away from in March 2026** [seen, as reported] | Enter Lloyd's late (2031), through standards, not platforms |
| **Fixed-price restoration and paying repairers** | Contracting risk after the event, not insurance, but it needs capital across a storm season: per-event cap now, protected cell or reinsurer partner from 2030; legal advice on the line between the two. Pay from the insurer's claims fund under its mandate, never from the firm's account |
| **Insurers procure slowly**: pilots, audits, a year or more to contract; MGA onboarding six to twelve months [seen in part, general knowledge; MGA timing from the builder review] | Hence capacity providers and MGAs first, at 8,000 to 15,000 claims in 2027; insurers' main books from 2030 |
| **Credit hire firms and claimant representatives resist** [seen, general knowledge] | Change the referral economics through the protocol; third-party offer within days; open record for claimants' agents |
| **Climate is increasing storm and flood losses** [seen, general knowledge] | Raises the value of mitigation and surge, and the risk on fixed-price restoration: cap the firm's exposure per event and carry the rest in the capital vehicle |

### 10.3 What the stress test changes

1. **Not the core design.** Coverage as code, baselines, born evidence, prevention, standing authority, restoration by a date and the shared protocol all survive today's rules.
2. **Declines and discretionary reductions stay human** for longer than capability alone would suggest. The judgement desk floor is set by law and the Ombudsman, not by models. One test is worth running in the wedge: for simple rule-based declines (no cover in force, a peril the customer was shown as excluded), a fast human appeal may satisfy the Ombudsman better than a slow human first decision [conjecture]. Measure it; do not assume it.
3. **The savings share is the most exposed part.** It must be designed with the regulator in view, and the firm must remain viable without it.
4. **Sequencing changes:** capacity providers and their MGAs first, because insurers procure slowly; liability last, because the tail is long.
5. **The protocol needs a trade body and a lawyer** before it needs a product.

**Where this is weakest.** Every number is conjecture. Seven things decide the design, and none is known: how many policyholders accept a device fitted during a visit; how much prevention cuts frequency and faster mitigation cuts severity for escape of water (vendor figures exist, independent ones were not found); whether owned and network repairs can be delivered without a rise in complaints; whether provenance beats AI fraud; whether insurers and the FCA will accept a verified savings share; whether insurers will give up credit hire referral income for a protocol; and whether a trade body will take the protocol. The first three can be measured in the wedge's first winter. The rest need conversations in 2027.

---

## Sources checked for this paper (24 November 2026)

- ABI detected fraud, 2024 and 2025, as reported: https://www.abi.org.uk/media-hub/news-post/fraudulent-insurance-claims-continue-to-top-1-billion ; https://www.insurancetimes.co.uk/news/fraudsters-target-bigger-payouts-as-false-claims-hit-13bn/1459863.article
- ABI motor claims 2025: https://www.abi.org.uk/media-hub/news-post/119-billion-paid-out-in-2025-to-support-motorists-across-25-million-claims
- FCA claims handling review, July 2025, and super-complaint response, December 2025 (search summaries): https://www.fca.org.uk/publications/good-and-poor-practice/home-travel-claims-handling-arrangements ; https://www.insurancebusinessmag.com/uk/news/breaking-news/lords-tell-fca-to-move-faster-on-home-and-travel-insurance-594663.aspx
- Tractable with Ageas and Aviva: https://www.insurancetimes.co.uk/ageas-ai-partner-tractable-takes-its-claims-product-to-next-level/1425391.article
- LeakBot and Covéa: https://www.coveainsurance.co.uk/brokers/how-leakbot-can-help-our-customers/
- Official Injury Claim data: https://www.officialinjuryclaim.org.uk/media/osknpodb/oic-april-june-2026-data-publication.pdf
- Lloyd's Blueprint Two and claims data standard: https://www.reinsurancene.ws/lloyds-unveils-new-strategy-as-market-adapts-to-blue-print-two-sunset ; https://www.insurancebusinessmag.com/uk/news/claims/london-market-group-launches-consultation-on-new-core-data-record-for-claims-558180.aspx
- Sedgwick UK, September 2026: https://www.sedgwick.com/press-release/sedgwick-leads-the-conversation-on-the-future-of-claims-in-the-uk/

Not checked at source: ICOBS 8, outsourcing rules, data protection changes in 2025, competition law on information exchange, the Aviva–Direct Line deal, and industry leakage estimates. All are labelled as general knowledge where used.
