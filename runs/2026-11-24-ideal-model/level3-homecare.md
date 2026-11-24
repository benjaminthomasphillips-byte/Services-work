# Level 3. Home care in England, redesigned from scratch

Draft by Claude, 24 November 2026. One author, no sub-agents. **Revised the same day after three reviews**: a builder of a technology-led provider, a provider director, and a council commissioner (all written in character). What changed, and where the reviewers disagreed, is in the final section. It is the hardest test so far of the restated architecture in `architecture-scorecard.md` (core G1 to G8, conditional C1 to C9). It follows the six-step procedure in `step-3c-the-electricity-test.md` and the kinds of human need in `step-3b-the-agent-enterprise.md`. Today's rules and institutions are facts to design around; they are applied in full only in section 11. A few facts were checked on 24 November 2026; sources are at the end.

Labels:
- **[seen]** exists somewhere today, with source;
- **[reasoned]** follows from logic;
- **[conjecture]** plausible towards 2035.

Points the reviewers made as operators are marked "(review)" where they shaped the design. They are informed judgement, not evidence.

Every volume, price and headcount is a model figure for argument.

---

## The answer in brief

Level 1 asks: "how do agents run a home care agency?" That gives a cheaper rota, notes typed by voice and invoices that write themselves. This paper asks: **"what would an older or disabled person buy if nobody had ever built a home care agency?"**

1. **Nobody wants a visit.** The person wants to live their chosen life at home, safely, with people they know. Today's service sells timed minutes of task because that is what a council can count [reasoned].
2. **The product is a human act, every day.** Washing, dressing, eating with someone, noticing they are not right: that is the service. It cannot become a side effect. **Agents cannot produce it; they can only protect the time of those who do** [reasoned].
3. **So the design inverts the architecture.** People produce; agents are the edge. The firm is neighbourhood teams for **health and care at home together**: salaried practitioners with community nurses inside the team, each team caring for 40 to 50 people in a neighbourhood of 5,000 to 10,000 residents. Agents do what today pulls carers away from people: rotas, notes, medication records, GP and pharmacy liaison, invoicing, compliance, family updates [reasoned; teams modelled on Buurtzorg, seen].
4. **The condition sold is "a good day and a safe night at home, as the person defines it"**, with three floors: safe, fed and medicated; seen by a known face; heard when something changes. **Priced per person per week by need band, not by hours.** Human time is recorded by the person, not the payer, and checked against a minimum set at each review [reasoned].
5. **Four new products sit around the core**: "before care" for people a year or two from eligibility; a designed night service; paid, trained roles in the team for family carers and neighbours; and dignity technology offered first as privacy, not saving [reasoned; conjecture for scale].
6. **Labour stays the binding constraint, and it has a shape.** Everyone wants help between 7 and 10 in the morning. The design fills the middle of the day with work that counts and staffs the peaks with part-time and family roles. By 2035 the firm needs about 66% (A) to 77% (B) of a traditional provider's people for the same 12,000 people [conjecture].
7. **The gain is in the job and the outcome, not the margin.** Pay rises by a quarter to a third; overhead falls from about 12% to under 4% of staff; a person sees three or four faces a month, not a dozen. Margin is about 7% in landscape A and slightly negative in B and D on base price. The return lands with the NHS and councils, so the contract must share it from year one [conjecture].
8. **The architecture test.** C2 alone holds. **G5 breaks**: people are the centre, not the edge. **C7 and C9 break as conditionals** and become core: demand has a daily shape, and the person sets the pace. Everything else bends. Missing: the workforce as a designed condition, the service surviving the firm (the market), the shape of demand in time, rules on observation, a rationed public payer, decline as the trajectory, unpaid carers as co-producers (section 10).
9. **Verdict.** The architecture is a design for information services with physical edges. For care it is half right: its information logic is what frees the human centre, but the firm's centre of gravity is a workforce working against the clock, inside a public market, and the architecture says nothing about either [reasoned].

---

## 1. Outcomes, by party

### 1.1 What each wants to be continuously true [reasoned]

| Party | What they want true | Measure |
| --- | --- | --- |
| **The person receiving care** | "I live my life, at home, my way. The people who come are people I know and like. They come when I need them, not when the rota says. I am safe without being watched, by day and by night. I can still do things for myself. When I am dying, I can do it here." | Person-reported good days a week; number of different workers a month; time actually spent with them; independence gained or kept; nights without a crisis; place of death matches wish |
| **The family** | "Mum is all right and I would know if she were not. I am not the only one holding this together. I can be her daughter, not her care manager. If I want to care for her, that is valued." | Unpaid hours carried; alerts that turned out to matter; carer strain score; days of crisis; nights slept |
| **The care worker** | "A real job: steady hours I can fit round my life, paid for all my time, a team I belong to, people I know well, and the authority to do what they need. A career, not a shift." | Contracted hours; hourly-equivalent pay; share of paid time with people; turnover; injuries; training gained |
| **The council (payer and market steward)** | "Every eligible person gets safe care within budget, the market survives any one provider failing, and I meet my Care Act duties without a crisis on my desk." | Cost per person per year, not per hour; unmet need; packages handed back; complaints and safeguarding referrals; moves to residential care; provider failures absorbed without harm |
| **The NHS (payer and neighbour)** | "People leave hospital the day they are ready, do not come back needlessly, and die where they choose." | Delayed discharge days; avoidable admissions and readmissions; falls with injury; people at home 12 weeks after reablement; deaths at home against wish |
| **The regulator (CQC)** | "Care is safe, effective, caring, responsive and well led, and I can see it is." | Continuous evidence on its five questions; incidents; notifications |

### 1.2 What follows [reasoned]

- **The person must become the principal.** The council buys, the family often chooses, the person receives. Here the principal is the party who usually does not pay and sometimes cannot speak.
- **"Continuously true" fits only half the outcomes.** Safety, food and medication are conditions. A good life is a texture, judged day by day. And health declines: the condition is "as well as possible on this person's path".
- **Speed is rarely the outcome**, except at hospital discharge and at night. A breakfast visit ten minutes late from someone known beats one on time from a stranger. A fall at 3am is different: there, minutes matter.
- **The worker's outcome is part of the product.** A known face depends on the worker staying. In no earlier service did the worker's condition sit on the client's critical path.
- **The council's real unit is the person-year, not the hour.** A commissioner does not need care cheaper per hour; it needs it cheaper per person per year, including the residential placements and hospital days it avoids (review). That is the measure the contract should use.

---

## 2. Where information is born and decisions are taken

### 2.1 Today

| Source | What is born there | Where today's provider meets it |
| --- | --- | --- |
| **The person** | How they are, what they want today, what matters, what they fear | In passing, in a 30-minute call, if the worker has time to listen |
| **The home** | Movement, sleep, eating, temperature, falls, a missed pill, an unopened door | Mostly nowhere; noticed by the next visitor, hours later |
| **The care worker** | The richest signal: "she was not herself", a new bruise, a sore heel, the fridge empty | Typed into an app at the end of a call, or lost; read later by a coordinator, if at all |
| **GP, community nurse, pharmacy** | Diagnoses, medicines, changes | By phone and letter; the provider is rarely on the GP's system; the nurse visits the same home on a separate rota |
| **Hospital** | Admission, discharge plan, new needs | A discharge notice, often late; the package restarts by phone |
| **Family** | History, preferences, worries, what they will do | By phone, in complaints, at reviews |
| **Council** | Eligibility, hours, budget, the care and support plan | A commissioned package: "four calls a day, 30, 30, 15, 30 minutes"; changes need a reassessment |

The core fault [reasoned]: **the people who see the person every day have the least authority, and the people with authority see the person least.** A carer who notices that a 15-minute lunch call is not enough cannot change it. A council assessor who can change it has met the person once.

### 2.2 By 2035 [conjecture, from reasoned design]

- **The person and their home become the primary source.** A person-held record carries their own account, in their words. Sensors the person chose (no cameras by default) report a few things: up and about, eating, a fall, the door at night. Dispensers report medicines taken.
- **Observation becomes data without becoming paperwork.** The worker says what they saw in a few sentences on the doorstep; agents turn it into the record, medication chart, incident report, GP message and family update.
- **Assessment moves to the team.** Senior practitioners assess and change the plan within the person's band, and notify the council. Trusted-assessor schemes at discharge already do part of this [seen, general knowledge]. The council audits a sample rather than approving each change. **A change of band goes to an independent band reviewer**, neither the firm nor the council's budget holder, so finding need is separated from paying for it [reasoned].
- **Decisions move to the person and the team.** The council and NHS set the envelope (eligibility, pooled budget, outcomes). Within it, person and team decide the week. Nurses in the team delegate health tasks under protocol. Agents propose; the team decides; payers audit outcomes, not minutes.
- **The firm is on the shared care record**, scoped by the person's consent, so discharge is a handover, not a restart. **And the payers read it too.** Oversight both ways needs the council's and GP's systems to see the live view, which they cannot today [seen, review]. Until they can, authority has only partly moved (see G6).

---

## 3. What disappears, what becomes a side effect, what remains

### 3.1 The mechanisms [reasoned]

1. **Neighbourhood density.** A team serves people in a neighbourhood of 5,000 to 10,000 residents, about a 15-minute e-bike radius in a town. Travel falls from about a fifth or a quarter of paid time to about a tenth. Density comes from serving **several kinds of need** (long-term care, reablement, nursing tasks, before care, nights, self-funders), not from a monopoly contract.
2. **The week, not the call, as the unit.** If the person and team hold a weekly plan priced by need, most rota changes, call-time disputes and reassessment requests vanish.
3. **Records at the source.** Spoken observation, sensor readings and dispenser logs make notes, medication records and incident reports by-products.
4. **Paying for the person, not the minute.** Per-person-week pricing by need band removes call monitoring as the basis of invoicing. Time is still recorded, but as the person's receipt, not the payer's stopwatch.
5. **Standing policy.** The person's "how I want to live" policy, the payers' envelope and the nurse's delegation protocol replace approvals.
6. **Shaping the day.** The morning and evening peaks are staffed by part-time contracts and family and neighbour roles; the middle of the day is filled with reablement, nursing tasks, lunch with someone and training. Medicines move off the 8am call onto dispensers where the person agrees.

### 3.2 Today's main work, line by line

| Today's work | Level 3 | How |
| --- | --- | --- |
| **Scheduling calls** (coordinators building rotas daily) | **Disappears as a job** | The team plans each week; an agent proposes it from each person's policy, staff hours, the shape of the day and travel, and repairs it when someone is ill |
| **Travel between calls** | **Shrinks**, remains | Density; walking and e-bike patches in towns; cars and linked micro-providers in rural patches. Paid in full as working time |
| **Visits** | **Remain, change shape** | Fewer fixed 15-minute calls. Visits flex in length by need on the day. Some welfare checks replaced by sensors only where the person chooses; never companionship |
| **Care plans** | **Becomes a living record** | The person's own account plus the team's knowledge, updated continuously; no annual rewrite |
| **Medication records (MAR)** | **Side effect** | Pharmacy feed plus smart dispenser plus a worker's spoken confirmation; discrepancies raised at once. Electronic MAR exists today [seen, general knowledge] |
| **Rostering staff** | **Disappears as a central task** | Salaried and guaranteed part-time contracts; the team covers itself; a shared float pool covers the rest |
| **Separate community nursing rounds** | **Merge into the team** | Nurses sit in the neighbourhood team; insulin, wounds and observations are planned with the person's care, not on a second rota |
| **Assessment and reassessment** | **Moves to the team, within the band** | Senior practitioners assess and adjust; independent review only for band changes; council audits a sample |
| **Recruitment** | **Remains, changes** | Local, by referral; an academy for newcomers; family carers and neighbours as a new source; fewer hires as turnover falls. The largest early effort |
| **Training** | **Remains, grows** | Delegated health tasks, dementia, end of life, reablement; an agent tutor for knowledge, people for practice. A ladder, not a compliance tick |
| **Compliance and CQC evidence** | **Side effect for the evidence** | Continuous evidence from the record, mapped to CQC's questions. Inspection still needs people; CQC's capacity, not providers' data, has been the constraint [review] |
| **Electronic call monitoring** | **Replaced** | A person-held time record (visit start and end, confirmed by the person or their device), visible to the council. Used for safety and the minimum-time check, never as the unit of payment |
| **Invoicing councils** | **Side effect** | Per-person-week, generated from the live list of people served and their band |
| **Payroll by minutes** | **Disappears** | Salaries and guaranteed part-time hours; overtime by exception |
| **Family updates** | **Side effect, after a noisy start** | A plain summary, scoped by consent. Expect more calls in the first months, not fewer (review); the family speaks to the team, not a call centre |
| **Night sits and waking nights** | **Mostly replaced** | Remote-first nights with a mobile responder; waking nights kept for those who need them |
| **Incident and safeguarding reports** | **Side effect for the form; the judgement remains** | The form writes itself; the decision to raise a concern stays with people |
| **Hospital discharge paperwork** | **Shrinks** | A shared plan on the shared record; the team assesses on the ward |

**Why this is not level 1 done better** [reasoned]. Level 1 keeps timed calls and makes rotas faster. It cannot remove travel, the 15-minute call or zero-hours turnover, because they come from how care is **bought**. The redesign changes what is bought, and who assesses.

---

## 4. What appears that did not exist before

- **The neighbourhood health and care team** as the unit of service, owning the outcomes of 40 to 50 people, with nurses inside it [reasoned].
- **The person's week**: a plan of human time held with the person, flexed day by day, priced by need band [reasoned].
- **Reablement by default**, by the same team who stay if care continues. Today reablement is often a separate service followed by a handover to strangers [seen, general knowledge]. Good reablement takes a share of people off care altogether (review).
- **"Before care"** [reasoned; conjecture for effect]: for people a year or two from eligibility, found from GP frailty data with their consent. Strength and balance work, home adaptation, light monitoring they choose, a named practitioner. Paid by the NHS, self-funders and the council's prevention budget. If it delays the first package by a year for a fifth of people, it beats every efficiency in this paper.
- **The designed night** [reasoned; conjecture for form]: chosen sensors, a voice line, a night practitioner on an e-bike or in a car covering several neighbourhoods, and a response shared across providers in a town. People often move to care homes because of nights more than days (review). Responder services exist in some areas [seen, general knowledge].
- **Paid family and neighbour roles** [reasoned]: a family carer, where the person wants it, can join the team on a paid, trained, part-time contract to care for their own relative, with supervision, respite, pension and a second face who is not family. Trained neighbours can take morning or evening shifts in their own streets. This is the largest untapped workforce in England, and it lands exactly on the peaks.
- **Dignity technology first** [reasoned; conjecture for robotics]: toileting aids, assisted bathing and transfer devices offered first as privacy ("would you rather do this yourself, with this?"). Many people would rather a machine helped them than a stranger. The labour saved is a side effect, never the reason.
- **Planned dying at home**, set up weeks ahead with GP, hospice and family, not a crisis package in the last days [reasoned].
- **The family carer inside the team**, paid or not, with a named contact, planned respite and their strain watched [reasoned].
- **New conditions** [reasoned]: "seen by a known face today"; "nothing missed" (medicines, food, a change acted on within four hours); "heard" (today's wish asked and, where possible, met); "a safe night"; "ready to go home" for anyone in hospital.
- **A trajectory for each person**: function, mood, weight, sleep, falls over months, so decline is seen weeks earlier. Falls and admission prediction from home care data exists today [seen: Cera, used across NHS systems; accuracy figures are company claims].
- **A second pair of eyes**: a senior from another team visits each person about monthly. Continuity is the best safeguard and the worst; closed teams can normalise poor practice (review).
- **A portable person**: the record, wishes, advance decisions and the team relationship move with the person if the contract or the firm changes hands [reasoned].
- **A record of freed time**: what each returned hour was spent on, and whether it changed outcomes [reasoned].

---

## 5. The role of people

### 5.1 Centre or edge?

**The care worker is the centre.** This is the plainest finding of the paper [reasoned]. In accountancy people stand at the edges of an agent pipeline; in lettings and claims a physical edge grew large. In home care there is no pipeline to stand beside. Three reasons it stays human [reasoned]:

1. **The outcome is relational.** Loneliness is part of what is being treated. A machine can deliver lunch, not lunch with someone.
2. **Intimate care needs consent in the moment.** Washing, toileting, dressing a wound: each needs reading the person, asking, waiting, stopping.
3. **The best sensor is a worker who knows the person.** Sensors catch falls; people catch the start of a decline, a scam, a bruise, a new fear.

This does not mean every task stays human. Where a person prefers a machine for a private task, the machine is the more dignified choice [reasoned]. The rule is that the person chooses, and saving money never chooses for them.

### 5.2 What agents, sensors and devices do

- **Agents:** plan and repair the week against the shape of the day; turn speech into the record; reconcile medicines; message GP, pharmacy and hospital; write family updates, invoices and CQC evidence; watch trajectories; tutor; handle pay and hours; keep the person's time record.
- **Sensors, chosen by the person:** activity, sleep, door, kettle, falls, temperature. No cameras by default; each has a stated purpose and an off switch.
- **Devices:** medication dispensers (which move prompts off the 8am peak); a voice line to the team; ceiling hoists and single-handed transfer aids that cut double-handed calls [seen, general knowledge: single-handed care reviews]. Councils' telecare services already use dispensers and night sensors to cut night sits [seen, review]. These count from 2027, not as a 2035 hope.
- **Robots by 2035** [conjecture]: in landscape A, assisted toileting, bathing and some dressing for people who choose them; meals and laundry help. That frees time; it does not replace presence.

### 5.3 How the job changes

| | Today | Level 3 |
| --- | --- | --- |
| **Title** | Care worker | Home care practitioner; senior practitioner; nurse in the team |
| **Contract** | Often zero-hours or variable, paid per call; travel often poorly paid [seen, general knowledge] | Salaried full-time, or **guaranteed part-time** (school hours, mornings and evenings, weekends); travel paid as working time. Split shifts only by choice, with the gap paid or filled |
| **Pay** | Close to the National Living Wage, £12.71 an hour from April 2026 [seen, GOV.UK] | About £15.50 to £17.50 an hour equivalent in 2027 money, rising with skill [conjecture] |
| **Autonomy** | Follows a call list; cannot change time | Plans the week with the person and team; assesses and changes the plan within the band; delegated health tasks |
| **Team** | Alone, managed by a coordinator by phone | A self-managing team of 8 to 12, with a nurse, supported by a coach, not a manager |
| **Skill** | Induction plus mandatory training | A ladder: practitioner, senior practitioner with delegated health tasks and trusted assessment, a route to nursing associate and nurse |
| **Status** | Low, often invisible | A professional known by the GP by name |

The model is Buurtzorg: self-managing teams of no more than 12 nurses that split when they grow, supported by about 20 coaches and a back office of about 50 for many hundreds of teams [seen: HBS Working Knowledge; Springer 2024]. Two cautions: Buurtzorg is district nursing, better paid and more skilled than English social care; and UK pilots found its principles hard to apply, with evidence mostly small and qualitative [seen: BMC Health Services Research 2019; East London evaluation]. In English home care, Wellbeing Teams ran self-managed neighbourhood teams and were rated outstanding [seen: CQC archived report]. **What agents add** [reasoned]: they lift the planning and admin load that self-managing teams otherwise carry, the commonest complaint against self-management. **What merging with nursing adds** [reasoned]: it brings the Buurtzorg skill mix back, and it fills the middle of the day with nursing work that is less tied to the clock.

### 5.4 The 8am problem, redesigned around

Almost everyone wants to get up between 7 and 10, eat at midday and go to bed between 7 and 10, every day (review). A team on full-time salaries is overloaded at breakfast and idle at 2pm. "The week as the unit" does not move breakfast [reasoned]. Five moves, together:

1. **Shape the contracts to the day**: guaranteed part-time morning and evening contracts for parents, students, retired people and neighbours; full-time staff carry the middle of the day.
2. **Fill the trough with work that counts**: reablement sessions, nursing tasks, lunch with someone, trips out, before-care visits, second-eyes visits, training.
3. **Move tasks off the peak**: dispensers for medicines; meals prepared the evening before; sensors for "up and about" where the person wants it.
4. **Use family and neighbour roles** where they want them, which fall naturally at the peaks.
5. **Let the person's policy spread the peak** where they genuinely do not mind: some people would rather rise at 10.

Even so, the honest ceiling on contact time is lower than the first draft claimed: about 75% of paid time in landscape A and 70% in B, not 80% [reasoned, after review].

### 5.5 Kinds of human need, applied

| Kind of need (step 3b) | In home care |
| --- | --- |
| 1. Purpose | Board with a person who receives care, a family carer and a practitioner as members |
| 2. Definition of good | Nurse, occupational therapist, social worker, pharmacist, a dignity and data ethics lead |
| 3. Answerability | Registered managers, nominated individual, safeguarding lead, Caldicott guardian |
| 4. Capability gaps | A clinical support desk (nurses on call); shrinks slowly |
| 5. Client demand for a person | **The whole service.** Not a tier; the product |
| 6. Physical world | **Inside the firm and at its centre**, not a network outside it |
| New: the workforce itself | Coaches, an academy, team support, family-role supervision: the firm's main management task |
| New: the market | Step-in plans, portability, a shared float with a second provider: the firm designs for its own replacement |

---

## 6. Where the firm's capability sits; the boundary

### 6.1 Where capability sits

In the home (record, chosen sensors, dispenser, voice line); in the practitioner's hands and phone; in the neighbourhood (a team base in a health centre or library, beside the GP practice and pharmacy); in the payers' systems through counterparty agents. **Not in a central office**, which shrinks to standards, coaching, the academy, a few builders and officers [reasoned].

### 6.2 The boundary choice

| Option | What it means | Verdict [reasoned] |
| --- | --- | --- |
| **Employ the teams** | The firm is the employer and the registered provider | **Chosen.** Continuity, training, safeguarding and CQC accountability all need an employer that stands behind the worker, including family carers it employs |
| **Platform of self-employed carers** | Introductory agencies match people with independent carers [seen, general knowledge] | Rejected as the core in towns. Atomised labour defeats continuity, teams and training. **In rural patches**, the team links to local micro-providers and backs them with nursing, nights, training and cover. Somerset supports nearly 300 community micro-enterprises [seen: Somerset Council; Government Business] |
| **Operating system for others** | The week agent, person agent and time record, sold to other providers and councils' in-house teams | **Spun out from 2028 as a separate, neutral company**, governed apart from the care firm. A council will not license software from a rival bidder in its own patches (review); a neutral company removes the conflict and lets licensing start early |
| **Buy, not build, the commodity** | Care-management systems, eMAR, payroll | **Buy.** Good systems exist [seen, general knowledge]. Build only what is new: the person agent, the week agent and the person-held time record (review) |

### 6.3 Ownership [reasoned]

The margins are thin and the return lands outside the firm (section 8). That makes this a poor fit for capital that wants a high return and a good fit for **patient, mission-locked capital**: an employee-owned or public-interest company, with social investors, councils and NHS bodies as possible funders. Commissioners will want covenants on debt and on the minimum-time rule if private equity is involved (review). Employee ownership also serves G9: the people who are the product share in the firm.

### 6.4 Who else is in the picture

| Party | Stance |
| --- | --- |
| **Councils** | Payer, market steward and **co-designer of the contract**, not a barrier to route round. With them on outcomes, budget and the market; apart from them on need, through evidence to an independent reviewer, not pressure on social workers |
| **NHS** | **With them, closely.** Community nurses join the teams; GPs and discharge teams are colleagues; joint payer through pooled budgets from the first contract |
| **Families and unpaid carers** | Co-producers; some become paid team members; never made to manage the service |
| **Other providers** | Rivals for contracts and staff; partners in a shared float pool, shared night response and step-in; licensees of the neutral operating system |
| **Micro-providers** | Rural partners, backed by the team |
| **Platforms** | Rivals for private clients and for workers who want flexibility |
| **Community groups** | Companionship, transport, lunch clubs: the team connects people to them rather than selling hours against loneliness |
| **Device and data firms** | Suppliers, never owners of the person's data |

---

## 7. The organisation

### 7.1 The agent architecture

| Agent | One per | Sole writer of | Job |
| --- | --- | --- | --- |
| **Person agent** | Person | The record's structure and history (the content belongs to the person and their team) | Keep the record and the "how I want to live" policy; prepare the week's proposal; track trajectory; hold consents and decision authority; package the record for portability |
| **Time record agent** | Person | The person's time record | Log visit start and end, confirmed by the person or their device; show the person and the council delivered time against the review-period minimum; never feed pay or invoices |
| **Week agent** | Team | The team's plan | Propose and repair the plan from people's weeks, the shape of the day, staff contracts, skills and travel; cover sickness; never cut a person's minimum |
| **Night agent** | Town | The night response log | Watch chosen night sensors and calls; route to the night practitioner, the team or 999; hand over at dawn |
| **Health liaison agent** | Person | Messages with GP, pharmacy, hospital | Reconcile medicines; share observations; track discharge; book reviews |
| **Signal agent** | Person | Nothing; it raises | Read sensors and dispensers; rank alerts; mark a quiet home "unknown" |
| **Family agent** | Family member | That member's view | Updates scoped by consent or best-interests decision; same view to all siblings unless decided otherwise; carer strain check |
| **Budget agent** | Person | The person's budget account | Track the week's use of time and money; report to payers or self-funder; flag under-use and over-use |
| **Practitioner agent** | Worker | The worker's own record | Turn speech into notes; hours, pay, training, wellbeing; guard against overwork |
| **Counterparty agents** | Council, ICB, CQC, band reviewer | Their cases | Invoices, outcome reports, notifications, band-change cases with evidence |
| **Verifiers and governance** | Output type; firm | Nothing | Medication and clinical checks on a different model; dignity monitor (language, consent, use of data); safeguarding pattern watch, including on workers, paid family members and closed teams; budgets, limits, breakers |

Constitution clauses specific to home care [reasoned]:
1. **The person's day is theirs.** Their wishes rule, within the law; positive risk is allowed.
2. **Freed time goes to the person first**, before it goes back to the payer.
3. **Observe only with consent and for the person's benefit.** Home data never judges, never cuts a budget unseen, never monitors workers covertly. This is a contract term, with external audit, binding on the payer too.
4. **A known face, and a second pair of eyes.** Continuity is protected above efficiency; no person is seen only by one team.
5. **No reward for less care.** No target, price or bonus rises because human time falls.
6. **Advocate for need through evidence.** The firm tells the independent reviewer when need exceeds the band, with evidence, even though the council pays.
7. **When in doubt about consent, capacity or safety, a person decides.**
8. **Design for your own replacement.** The person, their record and their team relationship can leave the firm intact.

### 7.2 Rhythm

The rhythm follows the person's day, not the rota [reasoned]. **Daily:** a 15-minute team huddle in the mid-morning trough; the night service hands over at dawn. **Weekly:** the team plans each person's week. **Monthly:** a short review with each person, and family if wanted; a second-eyes visit; team outcomes with the coach. **Quarterly:** outcome reports to the pooled budget; band reconciliation; standards review; model releases through the test harness. **Seasonal:** winter, heatwave, school-holiday and discharge surge plans.

### 7.3 Headcount sketch [conjecture]

Volumes: **2027**, 300 people in one town (a mid-sized provider); **2030**, 3,000 in five areas; **2035**, 12,000 in about 25 areas, roughly 2.4% of the half a million people receiving regulated home care in England [seen: DHSC statistics, about 500,000 in early 2026]. The count covers long-term care only, so it compares like with like.

Assumptions:
- **Hours of care per person per week:** traditional 11. Level 3: 11 in 2027; 10.4 (A) or 10.8 (B) in 2030; **9.5 (A) or 10.3 (B) in 2035**, a wider range than the first draft, as reablement takes some people off care and dignity technology lands. A caution: if before care delays entry, people who do enter are frailer, which pushes hours up [reasoned].
- **Contact share of paid time:** traditional about 62% (travel, admin, gaps). Level 3: **66% in 2027; 71% (A) or 68% (B) in 2030; 75% (A) or 70% (B) in 2035**, lowered after review for the shape of the day, huddles, reviews, second-eyes visits and an 8% float pool. Reaching 75% depends on the trough being filled by nursing and reablement.
- **Paid hours per full-time equivalent:** 37.5 a week for 46 working weeks, about 1,725 a year. Part-time and family roles are counted as full-time equivalents.

| Role | 2027 | 2030 A | 2030 B | 2035 A | 2035 B |
| --- | --- | --- | --- | --- | --- |
| **Practitioners and senior practitioners (in teams, incl. float, part-time and family roles)** | **151** | **1,325** | **1,436** | **4,580** | **5,320** |
| Owners, board, officers (incl. registered managers) | 3 | 10 | 11 | 26 | 30 |
| Standard-setters (nursing, OT, social work, pharmacy, dignity and data) | 1 | 6 | 7 | 10 | 12 |
| Clinical support desk and night response | 3 | 16 | 20 | 40 | 52 |
| Coaches | 1 | 4 | 5 | 15 | 18 |
| Safeguarding, complaints, carer support, family-role supervision | 2 | 7 | 9 | 22 | 30 |
| Council, NHS and band-review liaison | 1 | 6 | 7 | 12 | 14 |
| Recruitment and academy | 2 | 10 | 14 | 25 | 34 |
| Builders (the firm's own; the operating system company is separate) | 3 | 5 | 7 | 8 | 12 |
| Human checkers (scaffolding) | 1 | 2 | 6 | 0 | 8 |
| Operations, finance, pay, growth | 2 | 5 | 8 | 15 | 22 |
| **Outside the teams** | **19** | **71** | **94** | **173** | **232** |
| **Total** | **170** | **1,396** | **1,530** | **4,753** | **5,552** |

| Traditional provider, same people served [conjecture] | 2027 | 2030 | 2035 |
| --- | --- | --- | --- |
| Care workers (FTE, at 11 hours and 62% contact) | 160 | 1,600 | 6,415 |
| Office: coordinators, care managers, registered managers, HR, training, finance (about 12%) | 20 | 200 | 770 |
| **Total** | **180** | **1,800** | **7,185** |
| **Level 3 as a share** | 94% | 78% (A) / 85% (B) | **66% (A) / 77% (B)** |

**Nurses in the teams** are not in this count. If community nursing joins, roughly one or two nurses per team of ten to twelve move across from NHS community services: perhaps 400 to 600 by 2035. That is a transfer, not an addition to the system [conjecture].

### 7.4 What drives the numbers [reasoned]

1. **Contact share is still the biggest lever, but smaller than claimed.** From 62% to 75% cuts the workforce by about a sixth. It comes from density, deleted paperwork and filling the trough, not cleverer agents. In landscape B, 70% is the honest figure.
2. **Hours per person is the second lever, and the dangerous one.** Reablement, before care and dignity technology cut need; so does rationing. Hours are judged against independent outcomes, never targets.
3. **"Time returned" changes the count.** If payers keep funding 11 hours and freed time goes back to people, 2035 A needs about 5,300 practitioners, not 4,580, and each person gets about 16% more time. Where loneliness is the real problem, that is the better outcome.
4. **The office nearly vanishes**: from about 12% of staff to under 4%, near Buurtzorg's ratio [seen, approximate]. Coordination and translation disappear.
5. **The ratio to traditional (about 2:3 in A, 3:4 in B) is the smallest in the programme.** Accountancy and lettings reached 1:4 or better. Labour does not compress. In 2027 the two are level.
6. **Paid family and neighbour roles do not cut the count; they change where it comes from.** They are the answer to recruitment, not to cost.

---

## 8. Economics [conjecture throughout]

### 8.1 Who pays, for what, how priced

Baseline [seen]: the Homecare Association's minimum price for 2026–27 is £34.42 an hour at the National Living Wage; average council rates are reported around £25 an hour (a secondary figure, not checked against the full report). Self-funders pay more than councils [seen, general knowledge]. Residential placements cost well over twice a home care package (review; not checked).

| Product | Paid by | Pricing |
| --- | --- | --- |
| **Life at home** (long-term care) | Pooled council and NHS budget, self-funder, or direct payment | **Per person per week, by need band** (need and trajectory, not hours). About £380–£420 a week in 2027 money for a band that today buys about 11 hours |
| **Home from hospital and reablement** | Pooled budget | **A capacity retainer** for the team's discharge slots, plus an outcome payment on people still at home at 6 and 12 weeks. A retainer, not per episode, because discharge volumes swing and salaried staff cannot be laid off when beds empty (review) |
| **Nursing in the team** | NHS | Inside the capitated neighbourhood contract, or per person-week while the contract is separate |
| **Before care** | NHS, council prevention budget, self-funders | Per person per year, light |
| **The night** | Pooled budget, self-funders | Per person per week, by band; shared across providers in a town |
| **End of life at home** | NHS (fast-track continuing healthcare) | Per week, with 24-hour response |
| **Live-in care** | Mostly self-funders | Per week, with team backing and planned breaks |

**The time check, redesigned** [reasoned]. The first draft promised a "floor of human hours" and no call monitoring. Reviewers showed both cannot be true: a guaranteed floor needs proof, and a fixed floor fights reablement. The revision:
- The **band** is defined by need and trajectory, not hours, so the floor does not become the product.
- Each person's plan sets a **minimum of human time for the review period**, set below the expected average and **reset at each review from evidence**.
- Time is logged in a **person-held time record**, visible to the person, family and council. It is the person's receipt, not the payer's stopwatch, and it never sets pay or invoices.
- Falling below the minimum for two weeks triggers an independent review, not just a penalty.

**Outcome payments: 15 to 20% at risk** [reasoned, after review]. At 10% nothing changes in behaviour (review). Only on what the team controls: continuity (no more than four different workers a month), reliability, person-reported quality of life on an independent scale, and reablement results at 6 and 12 weeks. The Better Care Fund already tracks people still at home 12 weeks after reablement [seen: BCF framework 2026–27]. Guarded by the minimum: **no payment rises because human time falls.** Claims showed a priced outcome can reward harm; here the harm would be loneliness.

**Shared savings from year one** [reasoned]. Better Care Fund money is already pooled under section 75 agreements, due in every area by September 2026 [seen: BCF framework 2026–27]. The first contract carries a share of avoided admissions, shorter delays and later moves to residential care. **The target by 2030 is a capitated neighbourhood contract**: one amount per person needing care at home in the patch, from council and NHS together. The first draft waited until 2033 "where offered"; that left the savings in the wrong pocket for a decade.

**Guards against gaming** [reasoned, after review]: independent band review, open books, yearly band reconciliation, and a duty to accept every referral in the patch, so the firm cannot choose easy people or drift people up bands.

Why per person-week [reasoned]: hourly pricing rewards dependency and punishes reablement. It forces timed calls, call monitoring and the 15-minute visit. A weekly price lets the team spend time where it matters on the day. It shifts risk to the firm, so bands must be honest and reviewed.

### 8.2 Care-worker pay

Salary about £31,000 for 37.5 hours in 2027 (about £15.90 an hour), rising to about £35,000 in today's money by 2035 for practitioners, more for seniors. Part-time and family roles are paid at the same hourly rate. With on-costs of about 22%, each full-time equivalent costs about £37,800 in 2027 and £42,700 in 2035. At 75% contact, that is about £33 a contact hour, against a traditional labour cost nearer £22–24 at the minimum wage. **The level 3 provider pays more per contact hour and must win it back on fewer hours, less overhead, lower turnover and shared savings.** The Fair Pay Agreement for adult social care, due to take effect from April 2028 [seen, GOV.UK and others], will raise the floor for everyone and narrow the gap.

### 8.3 Revenue, cost and margin

Long-term care only. Other products (night, before care, nursing, outcome and savings payments) are upside not counted here.

| | 2027 | 2035 A | 2035 B | 2035 D (price squeeze) |
| --- | --- | --- | --- | --- |
| People served | 300 | 12,000 | 12,000 | 12,000 |
| Average price per person-week | £390 | £400 | £412 | £360 |
| Revenue from care | £6.1m | £249.6m | £257.1m | £224.6m |
| Development grant (2027 only) | £0.8m | – | – | – |
| **Revenue** | **£6.9m** | **£249.6m** | **£257.1m** | **£224.6m** |
| Practitioners | £5.7m | £195.6m | £227.2m | £195.6m |
| Outside-team staff (about £75,000 loaded) | £1.4m | £13.0m | £17.4m | £13.0m |
| Devices, sensors, licences, models, verification (about £700 a person a year by 2035) | £0.4m | £8.4m | £8.4m | £8.4m |
| Travel | £0.2m | £5.0m | £6.0m | £5.0m |
| Insurance, CQC fees, team bases, compliance | £0.3m | £6.0m | £6.0m | £6.0m |
| Acquisition and partnerships | £0.3m | £3.0m | £3.0m | £3.0m |
| **Cost** | **£8.3m** | **£231.0m** | **£268.0m** | **£231.0m** |
| **Margin** | **about −21%** (−37% without the grant) | **about 7%** | **about −4%** | **about −3%** |

### 8.4 What the numbers say

- **On base price, the design only pays in landscape A.** Labour is about 85% of cost and agents do not compress it. With the honest contact share, landscape B needs about £430 a person-week to break even, about 7% above A. The Fair Pay Agreement raises every provider's cost, so B's market price should rise too, but this is a gain for people, not investors.
- **So the outcome share and shared savings are not upside; they are the business model.** A 15% outcome share on A's revenue is worth up to £37m; even a third of it turns B positive. That is why the payer's side of C1 matters most (section 10).
- **Landscape D hurts less here than anywhere.** No agent collapses the price of touch. What collapses is any software edge, which is why the operating system is spun out and the firm competes on teams.
- **The real return is outside the firm.** If the team keeps one person in ten at home six months longer, a large share of the premium is paid back to the council (review). The case is judged on **total cost per person per year in one patch against a matched patch**. That is the headline test.
- **The 2027 loss is a launch cost**, cut from −40% by buying systems, borrowing standard-setters from the NHS and a council development grant. The council's view is that it would rather co-fund a patch than watch the firm grow a self-funder business (review).
- **Profit comes from** density, retention, reablement, shared savings and private clients. **Not from** shorter calls, fewer hours or selling data.

---

## 9. How it is built from 2027

### 9.1 The first wedge: a co-designed patch with discharge inside it

The first draft led with hospital discharge. The provider reviewer wanted self-funders first; the commissioner wanted a co-funded council patch. The revision [reasoned]: **one patch, designed with one council and one NHS trust**, contracted per person-week, with:
- discharge and reablement inside it, paid as a capacity retainer from the section 75 pool, so volume swings do not sink salaried teams;
- a development grant for the first year's losses;
- a matched comparison patch, judged on total cost per person per year at two years;
- self-funders in the same streets as fill for density, not as the core.

Why not self-funders first: it would prove a different business. The thesis is that public care can be bought differently; only a public patch tests it.

### 9.2 Registration, recruitment and adoption

- **Buy a small registered agency** in the first town for its CQC registration. Converting it takes **nine to twelve months**, not 90 days: TUPE, existing contracts and staff who prefer flexible hours (review). Those who want flexibility join the float pool.
- **Buy commodity systems; build the person agent, week agent and time record.**
- **Recruit on the job, not the wage alone**: salary, guaranteed part-time hours that fit lives, paid travel, a team, a ladder. Guaranteed hours do more for retention than pay rises (review). Target people who left care over zero-hours work, family carers, neighbours, and newcomers through an academy. The care worker visa closed to new applicants in July 2025 [seen], so domestic recruitment is the only route.
- **Teams form around a founding senior practitioner and a nurse** and split at twelve.
- **Adoption** [reasoned]: people and families for a known face and a family view; councils through the matched-patch result; the NHS through discharge and admissions results.

### 9.3 Rural patches [reasoned]

Density fails where a third of a county is rural (review). The rural model is a hub-and-spoke: a team with nurses and a night service at the hub, linked to local micro-providers who are backed by it with training, cover, records and the week agent. Contact share and margin are lower; the pooled budget carries a rural uplift.

### 9.4 Sequence [conjecture for dates]

| Year | Step |
| --- | --- |
| 2027 | One co-designed patch; section 75 savings share and discharge retainer; first six teams; agents for week, record, time record, medication, liaison; dispensers and night sensors from day one |
| 2028 | Before care and the night service in the first town; operating system spun out as a neutral company and licensed; Fair Pay Agreement absorbed; academy opens; first paid family roles |
| 2029–30 | Five areas, including one rural hub; community nurses join teams; **capitated neighbourhood contract** in at least one area; trusted assessment within band; 3,000 people |
| 2031–32 | Shared night response across providers in each town; dignity technology at scale |
| 2033–35 | 25 areas, 12,000 people; capitated contracts the norm where the firm works |

---

## 10. The architecture test

### 10.1 Scoring G1 to G8 and C1 to C9

All verdicts are [reasoned]. The author designed and first scored them; three reviewers then challenged them. Changes from the first draft are marked.

| # | Element | Verdict | Reason and change |
| --- | --- | --- | --- |
| **G1** | The shared record | **BENDS** | Central, and the "thing" is a body and a daily life. **Change:** the record belongs to the person; it holds their own voice first and observations second; parts are hidden from some parties; it is written for the most vulnerable reader, the person, not only the most hostile; it is portable |
| **G2** | Acting in the flow, never an unchecked payee | **BENDS, to the limit** | The firm is the payee and, with trusted assessment and capitation, also judges need and gains from less time. That is the conflict G2 exists to stop. **Change:** the flow is the person's time, not money; three checks are written into the contract: the person-held time record, independent band review, open books. Without all three, G2 breaks |
| **G3** | Policy as work | **BENDS** | The person's policy is written in values ("I'd rather risk a fall than have someone in at night"), and capacity fluctuates. **Change:** made in conversation, revisited monthly, in the person's words; best-interests decisions named as such |
| **G4** | Conditions and moments | **BENDS** | "Safe, fed, medicated, seen today" is a natural condition. But decline means conditions cannot always be kept true. **Change:** conditions judged against the trajectory; moments (discharge, fall, dying) planned as part of it, not as failures |
| **G5** | People at the edges, sized by the service | **BREAKS** | People are the centre, every day, and the product is a human act. **Different design:** people produce, agents form the edge, and agents are judged by human time returned. Management is of a workforce, not an agent pipeline |
| **G6** | Capability where information is born, oversight both ways | **BENDS** (was HOLDS) | Information is born in the home and capability can sit there. But authority to change a band still sits with the payer, and oversight both ways needs council and GP systems to read the live view, which they cannot today. **Change:** trusted assessment within the band; band changes to an independent reviewer; payers on the shared record |
| **G7** | Duties to every party, controls on the firm | **BENDS** (much heavier) | The payer is the state, rationing a budget. The beneficiary often cannot speak. **Change:** a duty to advocate for need through evidence; no reward for less care; a duty to the worker; protection of the person from family and from staff; and a **market duty**: the firm supports the council's duty to keep the market alive if it fails |
| **G8** | Evidence rules | **BENDS** | Limits on use are not enough. **Change:** limits on collection too: consent sensor by sensor, a stated purpose, the right to be unobserved; data never used to cut a budget unseen, binding on the payer by contract, with external audit |
| **C1** | Priced and guaranteed outcomes | **BENDS** | Reliability, continuity and reablement results can be guaranteed. Health cannot. **Change:** 15 to 20% at risk on what the team controls; and the **payer's side**: a guaranteed outcome needs a payer who can hold the saving, which means pooled money, not a firm's promise |
| **C2** | The standard | **HOLDS** | Many parties read the record, so a neutral standard is needed; national social care record standards and the shared care record are the route [seen, general knowledge] |
| **C3** | Holding money | **BENDS** | For direct payments and individual service funds the firm may hold the person's budget while being its payee. **Change:** only through a separated account with independent audit, or leave it with a third party |
| **C4** | Pooled data | **BENDS** (was HOLDS, with care) | Prediction evidence is mostly company claims; pooling home and worker data needs more than consent, and every council and ICB in a region must sign data agreements. **Change:** pool only for named purposes, with independent evaluation of any model before it shapes care |
| **C5** | Mandate chain | **BENDS** | Capacity is decision-specific and fluctuates (Mental Capacity Act 2005). **Change:** authority recorded per type of decision; attorney or deputy for some, the person for others, best interests for the rest, each logged. Disagreeing children are the normal case, designed for: one view to all, disputes to an independent advocate |
| **C6** | Custody beyond the firm | **BENDS** (was HOLDS) | Home care providers fail and hand back contracts often. **Change:** a portability duty: the record, wishes, advance decisions and team relationship move with the person; step-in plans agreed with the council in advance |
| **C7** | Surge capacity | **BREAKS as a conditional** (was BENDS) | Surge is not occasional. Demand peaks every morning and evening; sickness, snow and school holidays hit every month. **Different design:** promote "capacity shaped to demand in time" to core (G11 below). Seasonal surge stays conditional, met by a 10% shared float with a second provider, trained family and neighbour reserves, and a **jointly funded NHS retainer**, not the firm's cost alone |
| **C8** | Licensed definition of good | **BENDS** (was HOLDS) | Councils will not license from a rival bidder; providers will not license from a rival for staff. **Change:** the operating system lives in a separate, neutral company from 2028, with the care firm as one customer |
| **C9** | Pace set by the client | **BREAKS as a conditional** | Not a crisis feature; it is the service every day. **Different design:** promote to core: the person sets the pace of their day, their care and their decline, within a team that serves others at 8am |

**Tally:** holds 1 (C2); bends 13 (G1, G2, G3, G4, G6, G7, G8, C1, C3, C4, C5, C6, C8); breaks 3 (G5, C7, C9). The first draft had 5 holds, 10 bends, 2 breaks.

### 10.2 What home care needs that the architecture lacks entirely

All [reasoned] unless marked.
1. **The workforce as a designed condition.** Pay, hours, autonomy, safety and career decide quality. **Needed:** "the worker's condition" kept true like the client's.
2. **The service surviving the firm: the market as a condition.** A council does not buy a firm; it buys a market that must survive any one firm failing (review). Continuity of relationship is the main asset, and it must outlive the employer. **Needed:** portability, step-in, shared float, designing for one's own replacement.
3. **The shape of demand in time.** Peaks at breakfast and bedtime, the night, seasons. **Needed:** capacity and contracts shaped to the clock, not to weekly totals.
4. **Rules on observation.** A service in a home sees a body, a marriage, a worker. **Needed:** consent per sensor, purpose limits, a right to be unobserved, no covert monitoring of workers, binding on payers.
5. **A rationed public payer.** A firm that finds need creates cost for its own customer. **Needed:** finding need separated from paying for it, through an independent reviewer.
6. **Decline and death as the trajectory.** **Needed:** measures against a trajectory, and dying well as an outcome.
7. **Unpaid carers as co-producers, and potential colleagues.** Families provide most care [seen, general knowledge]. **Needed:** the carer inside the team, paid where they and the person want it, their strain a measure.
8. **Place and density.** **Needed:** the neighbourhood as the unit of organisation and contract, with a rural variant.

**A proposed restatement** [reasoned].
- **Replace G5** with: **"People stand where the service needs a person. Where the product is a human act, people are the centre and agents are the edge; the firm's use of agents is measured by human time returned to the work only people can do."**
- **Add G9: the workforce as a designed condition**, which lettings' technicians and claims' crews hinted at and home care makes unavoidable.
- **Add G10: the service survives the firm.** The client, their record and their relationships can leave intact; the firm supports the market it sits in.
- **Add G11: capacity shaped to demand in time** (from C7).
- **Move C9 into the core** as **pace set by the person served**.

---

## 11. What would make this design wrong, and the stress test

### 11.1 What would make it wrong

- **Councils and the NHS will not pool and contract per person-week by patch.** Without density, shared savings and weekly plans, it reverts to timed calls with better software, and the margin goes negative.
- **The 8am problem is not solved.** If the trough cannot be filled, contact share stays near 68% and landscape B never pays.
- **Self-managing teams do not transfer** to English social care [seen: thin, mixed UK evidence]; overhead rises.
- **Recruitment fails even with better jobs**, or family roles create more safeguarding risk than they relieve.
- **Sensors are refused**, or their false alarms waste the time they should save.
- **Robotics arrives fast.** If machines dress, wash and move people well by the early 2030s, G5 may move back towards a bend. Unlikely by 2035 for most intimate care [conjecture].
- **Savings stay in the wrong pocket.** Without the payer's side of C1, the outcome case does not pay.
- **The firm is captured by its payer** and becomes the instrument of rationing, or inflates need to fill hours. The independent reviewer is the guard on both.

### 11.2 The stress test against rules, institutions, workforce and adoption

| Fact | Effect on the design |
| --- | --- |
| **CQC registration** of "personal care", with a registered manager per location [seen, general knowledge] | One registered manager per area (about 480 people), workable if seniors carry real delegated authority, as Wellbeing Teams showed [seen]. Registration bought in the first town |
| **Care Act 2014**: councils assess eligibility, set personal budgets, prevent need, shape the market and step in on provider failure [seen, general knowledge] | Assessment within the band moves to the team only by council delegation; the council keeps eligibility. Before care fits the prevention duty. The market duty drives step-in and portability (G10) |
| **Hourly commissioning with call monitoring** in most councils [seen, general knowledge] | The largest barrier. Start with one co-designed patch and a matched comparison |
| **Council fees below cost**: about £25 an hour against a £34.42 minimum price [seen, partly secondary] | The salaried model cannot run on today's average rate. It needs pooled money, shared savings and a person-year case, not an hourly one |
| **Better Care Fund** pooled under section 75; a 12-week reablement metric from 2026–27 [seen] | The vehicle for year-one shared savings and the discharge retainer exists today |
| **Integrated neighbourhood teams** in NHS plans [seen, general knowledge] | The route to merging community nursing; the capitated contract builds on it |
| **Delegated healthcare tasks** allowed with training and accountability [seen, general knowledge] | Senior practitioners take them, with nurse sign-off in the team |
| **Paying relatives**: direct payments can pay a close relative in the same household only in limited cases [seen, general knowledge] | The firm employs the family carer as a registered provider's staff member, with supervision and a second face; the council and CQC must accept the safeguarding design. Untested at scale |
| **TUPE** on acquiring an agency [seen, general knowledge] | Conversion takes nine to twelve months; flexible-hours staff move to the float pool |
| **Fair Pay Agreement** from April 2028; zero-hours rules tightening; travel counts as working time [seen] | All help a salaried model. The recruitment edge must then come from the team, guaranteed hours and the ladder |
| **Mental Capacity Act 2005**, attorneys, deprivation of liberty rules [seen, general knowledge] | Decision-specific authority in the record; sensors that restrict movement may be a restriction and need care |
| **Health data** is special category; the NHS controls the shared care record [seen, general knowledge] | Access by agreement and consent, not by right; pooled prediction needs regional data agreements |
| **Care worker visa closed** from July 2025; home care vacancies about 10%; sector turnover about 25% [seen] | Domestic recruitment only. Family and neighbour roles become essential. Target turnover below 12% |
| **Procurement and conflict of interest** in council licensing [reasoned] | The operating system must be neutral: a separate company |
| **Casey Commission** on a National Care Service, phases due 2026 and 2028 [seen, GOV.UK] | Pooled budgets and standard pay would help; a national hourly price would hurt |

### 11.3 What the stress test changes

1. **Not the core design.** Teams, the week, the person-held record, agents at the edge and per-person-week pricing survive today's rules.
2. **The pricing and pooling reform is the hardest dependency,** harder than any technical one, but its vehicle (section 75 and the Better Care Fund) exists. The firm reaches it with the council, not around it.
3. **Pay is shaped by law from 2028.** The Fair Pay Agreement removes part of the recruitment advantage and the biggest cost risk.
4. **The firm's political role is part of the product.** It must argue for capitated, outcome-led commissioning from its own matched-patch data.
5. **Paid family roles are the least tested move.** They need a safeguarding design the regulator accepts before they scale.

**Where this is weakest.** All figures are conjecture. Five unknowns decide it: whether councils and the NHS will pool and contract per person-week by patch; whether the 8am problem can be solved well enough to reach 75% contact; whether self-managing teams work in English social care at scale; whether recruitment responds to better jobs and family roles; and whether savings can be shared. The first three can be tested within two years in one patch.

---

## Review and response

Three reviews, all written in character on 24 November 2026: a builder of a technology-led provider who wanted to go further; a provider director testing against operations; a council commissioner testing from the payer's side. Their operator judgements are informed views, not evidence.

### What I took, and why

| Point | From | What changed |
| --- | --- | --- |
| The hour survives as the hidden unit ("11-hour band", "floor of hours") | Builder | Bands defined by need and trajectory; human time becomes a minimum, not the product |
| The floor needs proof, so call monitoring has not vanished | Provider | A person-held time record replaces call monitoring; it checks the minimum and never sets pay or invoices |
| A permanent floor fights reablement | Commissioner | The minimum is set per review period and reset from evidence |
| Merge community nursing into the team; capitate | Builder | Nurses in teams; capitated neighbourhood contract targeted for 2030, not 2033 |
| The 8am peak makes 80% contact share not credible | Provider | Section 5.4 redesigns around it; contact share cut to 75% (A) and 70% (B); headcount and margin recomputed |
| Density means near-monopoly in "a few streets" | Provider, Commissioner | Neighbourhood of 5,000–10,000; density from several products, not exclusivity; step-in, shared float and portability |
| Before care, nights, paid family and neighbour roles, dignity technology | Builder, Provider (nights, family) | Four new products in section 4 |
| Trusted assessment by the team | Provider, Commissioner | Seniors assess within band; independent band review for changes |
| Outcome share at 10% changes nothing; shared savings from year one | Commissioner | 15–20% at risk on controllable outcomes; section 75 savings share in the first contract |
| Gaming: up-banding, cherry-picking, inflating need | Commissioner | Independent review, open books, duty to accept referrals, advocacy through evidence |
| Continuity's dark side | Provider | Monthly second-eyes visit from another team |
| Families with dementia and disagreeing children are the normal case | Provider | Designed into C5 and the family agent |
| Guaranteed part-time contracts | Provider, Builder | In the job design |
| Buy systems; six builders is a software company's plan | Provider | Buy commodity; build three things; 2027 builders cut to three |
| Rural model | Commissioner | Hub with linked micro-providers |
| Conversion in 90 days is optimistic | Commissioner | Nine to twelve months |
| Devices count from 2027 | Commissioner | Dispensers and night sensors in the 2027 build |
| CQC will not become "reading a live view" | Provider | Softened: the evidence is a side effect, inspection is not |
| Who capitalises it | Commissioner | Patient, mission-locked capital; employee ownership considered |

### Where reviewers conflicted, and which way I went

1. **Hours: abolish or verify?** The builder wanted no hour guarantee; the provider wanted verified time records; the commissioner wanted a resettable floor. **I combined them**: no hours in the price, a resettable minimum, verified by a record the person holds. Reason: the builder is right that a guaranteed number becomes the target; the provider is right that a per-week payee needs a check. Putting the record in the person's hands meets both without restoring the payer's stopwatch.
2. **The first wedge.** Discharge (builder, first draft), self-funders (provider), or a co-funded council patch (commissioner). **I went with the commissioner**, with discharge inside the patch on a retainer to answer the provider's volatility point. Reason: self-funders first would prove a different business; the design's claim is about how public care is bought.
3. **G2.** The provider said BREAKS; the commissioner said BENDS was slightly harsh. **I kept BENDS, "to the limit"**, and made the condition explicit: it holds only with all three checks in the contract. Reason: G2's purpose, no unchecked payee, can be met; its form, "beside, not between", cannot.
4. **G5.** The builder said BENDS, because "sized by the service" puts people at the centre here; the others agreed with BREAKS. **I kept BREAKS.** Reason: G5's claim is about where people stand, and here it is wrong. The fix is short to write but changes what the firm manages, which is a break in substance.
5. **C8.** The builder wanted licensing earlier as the core business; the commissioner said no council would license from a rival. **I did both**: a neutral company, spun out in 2028. Reason: neutrality removes the conflict and lets the builder's timing work.
6. **C7.** The builder accepted BENDS; the commissioner wanted a bigger, jointly funded fix; the provider wanted promotion to core. **I took the provider's verdict and the commissioner's fix.** Reason: daily peaks are not surge, they are the shape of the service, while seasonal surge is still a real conditional that the NHS should help fund.
7. **Private clients.** The builder and provider want them early; the commissioner fears they pull the firm away. **They stay, as density fill in the same streets, not as the core.**

### Verdict changes

G6 HOLDS to BENDS (all three reviewers). C4 HOLDS to BENDS (provider, commissioner). C6 HOLDS to BENDS (builder, and the commissioner's portability point). C8 HOLDS to BENDS (commissioner, provider; builder's timing kept). C7 BENDS to BREAKS as a conditional (provider). G2 kept at BENDS, with a condition. G5 kept at BREAKS. New core elements proposed: G10 (the service survives the firm, from the commissioner's market point and the builder's portability) and G11 (capacity shaped to demand in time, from the provider's G10).

### What I did not take

- **Robotics at scale for intimate care by 2035** as a planning basis (builder). Taken as a choice offered for dignity; not counted on in the headcount beyond the cut in hours.
- **Licensing from day one inside the care firm** (builder). The conflict with councils is real; the neutral company comes in 2028.
- **A 10% float pool on top of the teams** (provider). I used 8% inside the team count plus a shared float with a second provider and an NHS retainer for winter; a firm-only 10% would push landscape B further below break-even with no better result for people.

### What the revision cost

The numbers got worse and more honest. 2035 workforce share rose from 65–72% to 66–77% of traditional; landscape B margin fell from 2% to −4% on base price. The design now depends openly on the payer's side: pooled money, shared savings and a person-year case. That is the right dependency to expose, because it is where today's service fails too.

---

## Sources checked in this run

- Homecare Association, Minimum Price for Homecare 2026–27 (£34.42 an hour): homecareassociation.org.uk/resource/minimum-price-for-homecare-2026-2027.html. Average council rate of about £25.37 from a secondary summary; not checked against the full report.
- National Living Wage £12.71 from April 2026: gov.uk/government/news/national-living-wage-increases-to-1271-per-hour.
- People receiving regulated home care, about 489,000 to 506,000 (October 2025 to February 2026): gov.uk, adult social care provider statistics, quarterly updates to December 2025 and February 2026.
- Skills for Care workforce data as reported (home care vacancies about 10%, turnover about 25%): King's Fund Social Care 360; Care Management Matters, November 2025; localgov.co.uk, 2025–26.
- Fair Pay Agreement timetable: gov.uk consultation response; socialcare.blog.gov.uk, 22 July 2026; Homecare Association, 16 July 2026.
- Care worker visa closure, 22 July 2025: gov.uk news; Irwin Mitchell.
- Buurtzorg: HBS Working Knowledge; Springer, Journal of Organization Design, 2024 (two directors, 21 coaches); company presentation (back office about 50).
- UK Buurtzorg pilots: BMC Health Services Research 2019 (Guy's and St Thomas'); East London evaluation; Welsh pilots, University of South Wales.
- Wellbeing Teams: CQC archived inspection report (outstanding); Centre for Public Impact, 2021.
- Cera falls and admission prediction: NHS England, March 2025; company figures as reported.
- Casey Commission: gov.uk terms of reference, updated October 2026.
- Better Care Fund framework 2026 to 2027 (section 75 pooling, agreements due 30 September 2026; 12-week reablement metric): gov.uk/government/publications/better-care-fund-framework-2026-to-2027 (checked in revision).
- Somerset community micro-enterprises (nearly 300 operating): somerset.gov.uk, Somerset micro-enterprise project; governmentbusiness.co.uk (checked in revision; count from a secondary report).
- Reviews: `level3-homecare-review-builder.md`, `level3-homecare-review-provider.md`, `level3-homecare-review-commissioner.md`, same folder.
