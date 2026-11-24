# Level 3. Cross-border payroll and employment, redesigned from scratch

Draft by Claude, 24 November 2026, revised the same day after two reviews written in character: a builder of a global employer-of-record (EOR) platform, and a head of global payroll for 3,000 staff in 25 countries. One author, no sub-agents. It is the control test of the architecture in `architecture-scorecard.md` section 7 (core G1 to G11, conditional C1 to C12). It follows the six-step procedure in `step-3c-the-electricity-test.md` and sets itself beside `level3-accountancy.md`, the closest prior design. Today's rules and institutions are facts to design around; they are applied in full only in section 11. A few facts were checked on 24 November 2026; sources are at the end. What changed after review, and why, is in the final section.

Labels:
- **[seen]** exists somewhere today, with source;
- **[reasoned]** follows from logic;
- **[conjecture]** plausible towards 2035.

Reviewers' operator judgements are cited as "[experience, builder review]" or "[experience, practitioner review]". They are informed views in character, not evidence.

Every volume, price and headcount is a model figure for argument. "Landscapes" follow the earlier papers: **A** capability compounds, **B** capability plateaus, **D** prices collapse.

---

## The answer in brief

Level 1 asks: "how do agents run a global payroll and employer-of-record business?" That gives faster runs, fewer tickets and cheaper onboarding. This paper asks: **"what would a company with people in nine countries, and a person who works across several, buy if nobody had ever built a payroll bureau?"**

1. **Nobody wants a payroll run.** A company wants four things true at every moment: everyone is lawfully employed; everyone is paid right and on time; every authority is square; the cost of each person is known. The run and the cut-off are artefacts of batch computing [reasoned]. The pay *period* survives, but only as a legal unit that states close, not as work (section 2.3) [reasoned].
2. **Pay is a function, not a job.** Net pay is a function of a contract, events and rules. The rules come in three layers: the country's law, the sector's collective agreement and the company's own agreement. If all three are machine-readable and events are born structured, gross-to-net becomes a side effect [reasoned].
3. **Where people are is a pay event.** People increasingly work from more than one country. Tax residency, social-security cover and the client's permanent-establishment exposure should follow each day's location, computed live, like a pay rise. This, not gross-to-net, is the hard and valuable problem [reasoned; raised by both reviewers].
4. **Employment form is a dial with four settings.** Contractor; EOR; the client's own entity, formed and run by the firm; the client's own entity, run by the client. In much of Europe and Latin America, EOR is regulated as labour leasing or banned outright. So the dial is not a feature; it is the lawful form of the business. Moving between settings is a legal transfer of employment, planned in advance [reasoned; seen for France, Germany and Mexico].
5. **Pay first, bill after; hold nothing that is not owed.** As EOR, the firm is the legal payer. Its invoice is revenue, not client money. So the default is credit: the firm pays wages and taxes on time from its own funding, and the client pays after. That abolishes the deposit, removes client money and float in one move, and makes credit the firm's priced core skill. Accrued liabilities (thirteenth-month pay, holiday, severance) stay with the client until risk signals say otherwise [reasoned].
6. **Guarantee what the law does not.** The law already makes the EOR owe wages if a client defaults, so that is not a product. The product is a guarantee against **the firm's own failure** (an independent trustee, a named successor employer in every owned country, a standby facility, published solvency), an **error policy the employee can see**, and penalties paid by the firm when its computation is wrong [reasoned].
7. **Boundary:** own entities in 25 to 40 countries; certified partners for the tail; open, co-maintained rule packs; a portable layer for clients with their own entities. Own the record, treasury, credit and accountability; rent the rails; give away the code [reasoned].
8. **Headcount:** about 294 people for 150,000 employees in 2035 in landscape A, 395 in B, against about 750 for a traditional provider. In 2027 the firm needs more people per employee than a bureau [conjecture].
9. **Economics:** about 38% margin in A, 44% in B, and near break-even (about 3%) in D. In D, taking the incumbent model's deposits and accrual float would lift margin to about 26%. That is the design's sharpest test, and larger than the first draft said [conjecture].
10. **The architecture test.** The control result is **not clean**. The information core holds. Sixteen elements hold, five bend, one breaks and one is untested. **C3 breaks as a conditional**: for an EOR, holding and advancing money is the business every day. G2, G3, G7, G8 and C2 bend. **G10 is untested**. Two parameters are missing from the scorecard: **agent or principal in law**, and **who writes the rules: client, state or social partners** (section 10).

---

## 1. Outcomes by party

### 1.1 What each wants to be continuously true

| Party | Wants continuously true | Wants at moments |
| --- | --- | --- |
| **Founders and executives** | "I can hire the best person wherever they live." "Nothing about employing abroad will surprise me: no penalty, no permanent establishment, no lawsuit." | Hire; exit lawfully and humanely; convert to an own entity; pass due diligence |
| **Finance** | "I know the loaded cost of every person, live, in my currency." "My cash is not tied up in deposits." "Cash leaves only when it must, at a fair rate." | Close, audit, fundraise |
| **HR** | "Contracts and benefits are fair and lawful in every country and under every collective agreement." "I can prove pay equity." | Reorganisation, relocation, grievance |
| **Employees** | "I am paid right, on time, in my currency, and I understand it." "My tax, pension and social security are actually paid." "If you get it wrong, you fix it fast and I do not pay for your mistake." | Joining; moving country; illness, parental leave, bereavement; leaving with what they are owed; proving income |
| **Mobile professionals** | "My employment, pension and seniority survive changing client or country." | Starting with a new client; moving |
| **Tax and social-security authorities** | "Every employer reports at the event and pays in full on time." | Audits; period close; rule changes taking effect cleanly |
| **Labour and financial regulators** | "Workers keep their rights, including equal treatment where they are lent." "Money held for others is safe." | Inspections; a provider's failure handled without harm |
| **Social partners** (unions, employers' associations) | "Our agreements are applied as written." | Bargaining rounds; disputes |
| **Rented local directors** | "I will not be personally liable for contributions the firm failed to pay." | Signing accounts; an inspection |
| **Banks** | "Flows are predictable, KYC clean, fraud low." | A client default |

### 1.2 What follows [reasoned]

- **The firm sells states, not runs.** Each condition is true or false at any moment.
- **One paying principal, many people affected, and the law ranks them.** The company pays; employees receive. They mostly want the same thing. Where they part (exits, overpayments, data use), the law, not the firm, often decides who wins. As employer, the firm must side with the employee against its paying client when the law says so.
- **Authorities and social partners are rule-writers, not just counterparties.** The firm does not set most of the rules it applies.
- **Some people are the client.** A mobile professional may in time buy employment for themselves (section 4).

---

## 2. Where information is born and decisions are taken

### 2.1 Information

| Information | Where it is born | Where today's provider meets it | By 2035 |
| --- | --- | --- | --- |
| **Terms of employment** | Offer and contract | A PDF, re-keyed into payroll | A machine-readable contract generated from three layers: law, sector agreement, client policy. It *is* the payroll configuration. Where agency-work law requires equal treatment, the EOR contract mirrors the client's terms for comparable staff, which the firm reads from the client's HR system [reasoned] |
| **Collective agreements** | Sector and company bargaining tables | Read by specialists, coded by hand per country | Agreements published as code, co-maintained with the social partners who wrote them [conjecture] |
| **Identity, tax and social-security numbers** | State identity systems and registers | Forms and scans | Pulled from registers and state identity wallets with consent [reasoned] |
| **Location** | Where the person sleeps and works each day | Discovered late, often at a tax audit | Declared by the person, through their own agent if they wish, and counted against thresholds. Never tracked [reasoned] |
| **Changes** (pay rise, promotion, move) | The client's HR system | A monthly change file, often late | Events streamed as they happen [seen in part: today's integrations; reasoned: the role] |
| **Time, leave, absence, sickness** | Time systems, managers, doctors | Spreadsheets at cut-off; sick notes arrive late | Events at source. Late facts still arrive; the record keeps them with the date they became known (2.3) [reasoned] |
| **Equity** | The cap table at grant, vest, exercise | Late reports; vesting tax missed | Read at source, taxed when it arises, sourced by location for movers [reasoned] |
| **Expenses** | The card swipe | Claims at month end | Card under policy; taxable benefits flagged at the swipe [reasoned] |
| **Benefits** | Insurers, pension schemes | Lists reconciled by hand | Two-way feeds; enrolment follows the contract [reasoned] |
| **Money** | Firm's treasury and local accounts | Client pre-funding days ahead | Firm pays from its own funding; client settles after [reasoned] |
| **What authorities need** | Law and authorities' systems | Filings after the event | Reports at each pay event; authorities offered read access to the event stream from the start (2.3) |

### 2.2 Decisions

The decisions that matter are few: where to hire, employment form, where people may work from, pay and equity, benefits, exits, entities. Today the provider learns of them from a change file, after the fact [reasoned]. **The redesign puts the firm before the decision**: inside the offer, the reorganisation, the relocation request and the board paper on a new country.

### 2.3 What the state already does, and what it still requires [check results]

| Regime | What it does | Status |
| --- | --- | --- |
| **UK, Real Time Information** | Employers report pay, tax and National Insurance to HMRC on or before each payday | [seen, vendor and HMRC-linked summaries; live since 2013, general knowledge] |
| **Ireland, PAYE Modernisation** | Payroll submission to Revenue on or before each payment | [general knowledge, since January 2019; not checked in this run] |
| **Australia, Single Touch Payroll** | Each pay event reported to the tax office | [seen; mandatory for 20+ employees from July 2018] |
| **Brazil, eSocial** | Event-driven, near-real-time reporting of employment events | [seen; phased from 2018] |
| **France, DSN; Norway, a-melding** | Single monthly declaration replacing many filings | [seen, named in a Canadian payroll association paper; details not checked] |
| **EU, VAT in the Digital Age** | E-invoicing and near-real-time reporting for intra-EU trade from 1 July 2030 | [seen, European Commission] |
| **EU Pay Transparency Directive** | Pay-gap reporting and pay-range rights; transposition due 7 June 2026 | [seen; only about four member states fully on time] |

**What this means** [reasoned]. Many states already want employment data at the event, in a fixed schema. What remains is coherence across many states at once, the money, and the rules that unions and employers write. By 2035 some authorities may compute deductions themselves [conjecture]; the design must survive that.

**The period does not disappear** [reasoned; raised by the practitioner]. Authorities close periods. UK income tax is cumulative across the tax year. Corrections to filed periods follow each state's own process [general knowledge]. So the run disappears as *work*, but the period survives as a *legal unit*. The design answers this with a record that keeps three versions of every fact: **as true** (what actually happened), **as known** (when the firm learned it) and **as filed** (what each authority was told). A late sick note changes "as true" at once, pays the employee at once, and generates the correction each state's process demands. No person reconciles the three by hand.

---

## 3. What disappears, what becomes a side effect, what remains

### 3.1 The mechanisms [reasoned]

1. **The executable contract**, generated from law, sector agreement and client policy, configures pay: no re-keying.
2. **Events at source**, under standing policies that replace approvals. Location is one of the events.
3. **Continuous computation** of gross, net, employer cost and liabilities, checked by an independent recomputer on different code.
4. **A three-version record** (as true, as known, as filed), so late facts are corrections, not crises.
5. **Reporting as a side effect**, at the event where the state takes it, closed by period where the state requires.
6. **Money on a schedule set by law and the employee, not by batch.** The firm pays first and bills after.

### 3.2 Today's main work

| Today's work | Today | By 2035 | Why |
| --- | --- | --- | --- |
| **Onboarding** (forms, IDs, tax codes, bank details, right to work) | Days to weeks of chasing | **Mostly disappears.** Identity and tax data pulled with consent; payee confirmed; right to work checked digitally. **Remains:** visas, background checks and, in some countries, opening a local bank account [experience, builder review] | Information was in the wrong place [reasoned] |
| **Choosing the employment form** | A sales conversation, then a project | **A dial setting** chosen by policy from expected tenure, country law and headcount. **Remains:** the conversion itself, which is a legal transfer with consultation | Form is a policy [reasoned] |
| **Contracts** | Lawyer templates per country, edited | **Side effect** of three rule layers. **Remains:** negotiated executive terms; works-council agreements | Contract is generated, not drafted [reasoned] |
| **Payroll runs** | Monthly batch, cut-off, inputs, variance checks, approval | **Disappears as work.** Pay is continuous; the employee chooses when to draw it, within law. **Survives** as a legal period that states close | Batch was a computing limit; the period is a legal one [reasoned] |
| **Gross-to-net** | Specialist calculation per country | **Side effect** of layered rule packs. **Remains:** defining and testing the agreement layer, which is where most of the variety lives [experience, practitioner review] | Rules are functions [reasoned] |
| **Corrections** (backdated rises, late sick notes, unreported leavers) | The bulk of a payroll team's pain [experience, practitioner review] | **Side effect** of the three-version record. Underpayments paid the same day; corrections filed by each state's process | Late facts are normal, not errors [reasoned] |
| **Filings** | Monthly, quarterly, annual returns per authority | **Side effect** where real-time regimes exist; generated and confirmed elsewhere. **Remains:** authority notices, audits | States moving to event data [seen, 2.3] |
| **Mobility** (certificates, day counting, shadow payroll, permanent-establishment checks) | Fastest-growing risk; handled late and by hand [experience, practitioner review] | **Side effect** of location as an event. **Remains:** judgement on residency disputes and on roles that create permanent establishment | Location is an input to pay [reasoned] |
| **Payments** (net pay, tax, social security, pensions) | Client pre-funds days ahead, many bank files | **Side effect** of payday release from the firm's own funding. **Remains:** treasury, credit and fraud judgement | Credit as default [reasoned] |
| **Benefits** | Enrolment lists, reconciliations, renewals | **Side effect** for enrolment; **remains** for design of benefits and claims in crisis | Two-way feeds [reasoned] |
| **Statutory sick and parental pay reclaims** | Forms to state funds, reclaims chased | **Side effect** where states take events; **remains** as a dealing with rationed public payers | Event at source [reasoned] |
| **Terminations** | Calculations, documents, negotiations | **Remains**, smaller. Final pay, notice and statutory amounts computed instantly. The decision, the conversation, the process and disputes need people | Human and legal moment [reasoned] |
| **Equity** | Late vesting reports, tax corrections | **Side effect** of cap-table events, sourced by location. **Remains:** plan design | Event at source [reasoned] |
| **Expenses** | Claims, receipts, approvals | **Disappears** for most: card at source under policy | Policy at the swipe [reasoned] |
| **Compliance changes** (new rates, new laws, new agreements) | Research, bulletins, manual updates per country | **Rule-pack releases**, tested against the whole population before they take effect. **Remains:** reading new law and agreements and setting the standard | Rules as code [reasoned] |
| **Employee queries** ("why is my pay different?") | The largest ticket volume | **Mostly disappears.** A live pay statement explains each change at the event; the employee's own agent can ask. **Remains:** questions that are really about fairness, illness or a dispute, in the employee's language | Explanation at the event [reasoned] |
| **Year-end** | P60s, W-2s, annual reconciliations | **Confirmation** of a state reconciled all year | Continuous [reasoned] |
| **Reconciling payroll to the ledger** | Monthly journals, suspense accounts | **Disappears**: one event, one posting | Same record [reasoned] |

What remains is judgement about law and agreements, people at hard moments, money and credit, mobility disputes and unusual dealings with authorities: accountancy's shape, plus treasury and credit.

---

## 4. What appears that did not exist before

1. **The employment form as a dial with four settings** [reasoned]. Contractor; EOR; the client's own entity formed and run by the firm ("entity in a box"); the client's own entity run by the client. Policy chooses the setting from tenure, country law and headcount: for example, "EOR only where lawful and only up to the legal cap; entity in a box from the fifth hire". Where EOR is banned or capped, the dial skips it. Moving between settings is a transfer of employment, with consultation and continuity of service as the law requires; the record carries the evidence of continuity [reasoned; builder's correction]. Germany's labour-leasing permit and 18-month cap [seen, AÜG summaries], France's general ban on profit-making labour supply outside narrow routes [seen, cited in builder review], and Mexico's 2021 ban on personnel subcontracting [seen, cited in builder review] make the dial the lawful design, not a convenience.
2. **Form-neutral pricing** [reasoned]. The firm earns the same margin whichever setting the dial is on. So it never gains from keeping a client on EOR longer than is good for the client. Incumbents earn most from EOR and so lean against conversion; this firm does not.
3. **Location as a pay event** [reasoned; both reviewers]. The person declares where they are working; the record counts days against tax-residency and social-security thresholds; it requests certificates of cover; it runs shadow payroll where needed; and it warns the client before a role creates permanent establishment. Where a move is lasting, the dial can move that one person to an entity in the new country. Location is declared, never tracked, so it can pass a works council.
4. **Live cost of a person**, including accruing notice, severance, holiday, thirteenth-month pay and employer taxes [reasoned].
5. **Hire in the right form, once.** Starting within days is already claimed today in established countries [experience, builder review]. The new thing is a lawful start in the form that fits the expected tenure, so nobody is moved twice by accident. Remaining gates are visas, background checks and bank accounts; pay to any account or regulated wallet the person already holds removes the last for many [reasoned].
6. **The guarantee against the firm's own failure** [reasoned; builder's bolder move]. As legal employer the firm already owes wages if a client defaults; that is law, not a product. Employees' real exposure is the **firm** failing. So: an independent trustee holds any money the firm receives ahead of paying it out; a standby facility from a capital partner, sized to one payroll cycle in owned countries, is drawable by the trustee; a named successor employer is pre-agreed in every owned country; solvency and reserves are published quarterly.
7. **The employee error policy** [reasoned; practitioner's bolder move]. Underpayments are paid the same day they are found. Overpayments caused by the firm below a set threshold are never reclaimed. Larger ones are recovered only where law requires it, interest-free, in instalments the employee agrees. Every correction is explained in the live statement. The firm's penalty guarantee covers the authority; this covers the employee's trust.
8. **The penalty guarantee.** The firm pays penalties and interest caused by its own computation or late filing. Classification and permanent-establishment risk, which depend on client facts, go to an insurer, priced from the firm's data [reasoned].
9. **Pay on the employee's terms** [reasoned; builder's bolder move]. Pay is known continuously, so the employee chooses cadence, currency and rail within law: weekly, at month end, or drawn as earned, at no fee. Law limits this: many states set minimum pay frequency, require pay in local currency or to a local account [general knowledge, not checked]. The period still closes; withholding on early draws is trued up at period close.
10. **The employee's portable record, linked not rival** [reasoned; practitioner's correction]. A mortgage lender trusts the tax authority's data more than an employer's. So the record links the firm's signed employment facts to the authority's own data and to state identity wallets, where they exist, rather than competing with them [conjecture for the wallets; the EU's digital identity wallet is general knowledge, not checked].
11. **Agreements as code, co-maintained and open** [conjecture]. The firm builds the tools; unions and employers' associations publish their agreements in them, free; authorities co-maintain the statutory layer. The firm's rule packs are open. Its edge is accountability, not code [reasoned; builder's bolder move].
12. **Equal treatment and pay transparency as side effects** of the same record [reasoned; required by the EU directives, seen and general knowledge].
13. **Law and agreement changes simulated** against the whole population before they bite [reasoned].
14. **Authorities offered the event stream from the first year** in the real-time states, rather than waiting for them to ask [reasoned; practitioner's bolder move]. Whether they read it is their choice; the design does not depend on it.
15. **The worker as client** [conjecture; builder's bolder move]. By 2035 a mobile professional could hold one lasting employment with the firm, with pension, benefits and seniority, across many clients and countries. Clients buy work; the person owns the relationship. France's *portage salarial* already lets a worker bring their own employer [seen, cited in builder review]; Sweden has similar "self-employment companies" [general knowledge, not checked]. The UK's experience with umbrella companies shows the abuse to avoid (section 11.2). The clean version accepts full employer liability, opens its books and runs no tax schemes.
16. **Agent to agent.** By the 2030s the employee's agent, the client's agent and authorities' systems talk to the firm's agents directly [conjecture].

---

## 5. Where the firm's capability sits; the boundary

### 5.1 Where capability sits

In the client's HR system, cap table, card programme, bank and ledger; in the firm's own entities, where it is the employer; in client entities it runs; in each authority's interface; at the social partners' tables; in the employee's phone. The firm is not a bureau that receives inputs. It is the layer where employment, pay, location and the state meet [reasoned].

### 5.2 The boundary choice

| Option | What it means | Verdict |
| --- | --- | --- |
| **Own entities everywhere** | Entity, accounts and registrations in 150 countries | Too costly for the tail; Deel built 150+ countries over years with large capital [seen, company claims] |
| **Partners everywhere** | Resell in-country providers | Cannot guarantee what it does not run |
| **Portable layer only** | Software over clients' own entities | Cannot serve companies without entities |
| **Recommended: hybrid, with the dial** | Own entities in the 25 to 40 countries holding most employees, used as EOR only where lawful; entity in a box where EOR is banned or capped; certified partners elsewhere, working on the firm's record, with step-in rights; a portable layer above clients' entities | The firm owns what it guarantees, and only what it can make true [reasoned] |

**Own** the record, recomputer, treasury, credit, guarantees and accountability. **Open** the rule packs and agreement tools. **Rent** rails, bank accounts, FX liquidity, benefits products, local statutory accounting and resident directors. **Certify** the tail [reasoned].

**What "own entity" really costs** [experience, builder review; reasoned]. An owned entity needs a bank that will keep a large cross-border payroll account open, a statutory audit and transfer-pricing files in many countries, local accounting, and directors who may be personally liable for unpaid social contributions (criminally so in Germany, general knowledge, not checked). Directors sign only if they can see the money controls work. So each director gets a live view of their entity's contributions paid and solvency. Treasury becomes how the firm recruits directors, not only a desk. Banks get the same view, which is the design's answer to de-risking: a payroll account whose every flow is explained in advance.

### 5.3 Who else is in the picture

| Player | What they are doing | How the firm stands |
| --- | --- | --- |
| **Deel** | Past $1bn run rate in early 2025; 35,000+ companies and 1.25m workers in 150+ countries in mid-2025; licences in the US, Canada, UK, Belgium, the EEA and Australia [seen, company and press] | The scale leader at level 1 to 2. Built its own entities and payments. **Competes on incentives:** form-neutral pricing, no deposit, no float or FX income, guarantee against own failure |
| **Remote** | Global HR platform founded 2019; own-entity model; EOR list prices $599 to $699 per employee-month [seen, pricing pages, cited in builder review] | Same as Deel, smaller |
| **Rippling** | HR, IT and payroll on one employee record [general knowledge] | Closest to G1. **Rival** |
| **ADP and incumbents** | Global payroll; large float income [seen] | Rival for enterprises. **Float is its weakness:** it cannot easily give it up |
| **Local bureaus** | Country depth, low tech | **Partners** for the tail and for entity accounting; certify or acquire |
| **HR systems** (Workday, HiBob, Personio) | Hold the employee master; several now sell EOR themselves [experience, builder review] | **Channel only where they do not sell EOR**; rival where they do. Never compete on the HR system |
| **Banks** | Rails, FX, credit | **Rented rails and capital partners** |
| **Governments** | Real-time reporting; free basic tools in some [general knowledge] | **Data partners and co-maintainers** of the statutory layer. If a state computes deductions, the firm keeps employment, money, mobility and coherence |
| **Unions and employers' associations** | Write the agreements that set most pay terms in much of Europe [general knowledge] | **Co-authors** of the agreement layer |

**The 2035 contest** [reasoned]: who holds the employment record and legal status across borders and through moves, trusted by employees, social partners and states. Software is near free; being the employer and answering for it is not.

---

## 6. Money

This is where payroll differs most from every earlier design, and where the first draft was wrong on mechanics.

### 6.1 The flows

A client with 100 people in nine countries pays, each month, 100 accounts in perhaps seven currencies, about 20 authorities and a dozen benefit providers. At the 2035 model volume, about $12.6bn a year of employment cost passes through the firm's systems; about $5bn of that is EOR, where the firm is payer [conjecture: 150,000 employees at about $84,000 average employer cost, 40% on EOR]. Contractors are paid on top.

### 6.2 Who is the payer, and what that makes the money

Three cases [reasoned]:
- **The client's own entity, run by the client or by the firm.** The client is the employer and payer. The firm acts as agent: it initiates payments from the client's account under a revocable mandate. **It holds nothing.** This is accountancy's "beside, not between". Entity in a box keeps the firm an agent in countries where it could not lawfully be the employer.
- **EOR.** The firm's entity is the legal employer. It owes the wages and the employer's taxes, whatever the client does. **The client's payment to the firm is revenue for a service, not client money** [experience, builder review; reasoned]. Once paid, it is the firm's money. So the question is not "how to safeguard client money" but "how much the firm advances, and how it protects employees from its own failure".
- **Contractors.** The firm pays them for the client. That is money transmission, which needs a licence. So the firm pays contractors from the client's own account under mandate, or through a regulated partner, and holds no balance [reasoned; licence point from builder review].

### 6.3 Design of the money [reasoned unless marked]

1. **Pay first, bill after, by default** [both reviewers]. A US client cannot pay a Polish employee in złoty on instant rails; the Polish entity pays from a Polish account. Corporate treasuries often block third-party debits; FX must settle before payday; payment returns arrive days later [experience, practitioner review]. "Debit on payday morning" was therefore credit from the firm in disguise. The redesign makes it open: the firm pays wages and taxes on time from its own funding line, then invoices; the client settles within a set number of days. Credit is priced from live data on the client's cash (with consent) and its payment history.
2. **No deposit.** Today's EOR deposits of one to three months' cost tie up clients' cash [experience, practitioner review]. Credit as default removes them.
3. **Accruals stay with the client, unless risk says otherwise.** Thirteenth-month pay, holiday pay and severance build up for months [experience, builder review]. Billing them monthly and holding them would recreate float. Instead the firm carries them as a priced credit exposure. A **springing reserve** applies: when the client's live cash data shows runway falling below a set threshold, accruals start to be funded, held by the trustee. Strong clients keep their cash; weak ones fund before trouble, not after.
4. **Prepayment, for clients who refuse data access.** They pay before payday. Those sums sit with the independent trustee or a regulated partner, not in the firm's operating accounts. Whether this triggers safeguarding rules is checked country by country; at first a regulated partner holds them.
5. **No float profit and no FX spread.** The firm holds almost nothing, by design, so float is small. What is held earns interest for the client, net of a disclosed cost. FX at interbank rate plus a fixed, disclosed fee, about 0.2%. G7's revenue rule forbids income that rises with holding the client's money [reasoned].
6. **No worker wallets.** The firm pays into accounts or regulated wallets the person already holds. It does not hold workers' balances, which would need e-money licences and create a new float [reasoned; builder's point on wallets].
7. **Protection against the firm's own failure** (section 4, item 6): trustee, standby facility, named successor, published solvency.
8. **Fraud controls.** Bank-detail changes, the classic payroll fraud, need verified identity and confirmation of payee [reasoned].

### 6.4 Who carries the risk if a client fails to fund

| Layer | Who carries it |
| --- | --- |
| **Early warning** | The firm. Live cash data shows trouble weeks ahead; the springing reserve starts; the client's policy names an orderly wind-down plan agreed at signing |
| **First loss** | The springing reserve, where it has started; for prepay clients, their prepayment |
| **Next** | The firm's own capital, a first-loss layer |
| **Tail** | A credit insurer or capital partner, priced from the firm's default and recovery data |
| **Employees** | Paid by the firm as legal employer, as the law already requires, then exits handled lawfully. Where states run wage-guarantee funds for insolvent employers, those funds may apply only to the firm's own insolvency, not a client's [reasoned; such funds exist in EU states under the Insolvency Directive, general knowledge] |
| **Authorities** | Paid by the firm as legal employer; this is not optional |

**A warning** [reasoned]. Client failure is correlated. A downturn in venture funding hits many start-up clients in the same quarter, and the firm's own funding line may tighten at the same time. Credit risk here behaves like correlated surge: it must be sized for a bad year, with committed facilities, not an average one.

### 6.5 Licences

- **As employer:** employer, withholding and social-security registrations in each owned country; labour-leasing permits or agency licences where required, as in Germany [seen] and, by the builder's experience, Spain, Italy, Poland and the Netherlands [not checked].
- **As money handler:** paying your own employees from your own money usually needs no payments licence; holding funds for others or paying contractors for clients does. Credit as default keeps the firm out of client money for EOR. Contractor payments and prepayments go through a regulated partner first; authorisation follows volume. Deel shows the end state: 26 US state money-transmitter licences in early 2025, plus UK, EEA, Canadian and Australian licences [seen, secondary source and company].
- **As lender:** in some countries, routinely extending credit to clients may need consumer or commercial lending permissions; the capital partner holds them at first [reasoned; not checked].
- **As tax agent:** filing authorisations per country [general knowledge].

---

## 7. The organisation

### 7.1 The people, by kind of need

| Kind of need | Role | What they do |
| --- | --- | --- |
| **Purpose** | Owners and board | Constitution, risk appetite, capital, country entry |
| **Definition of good** | **Rule-pack and agreement standard-setters** by country cluster | Read new law and collective agreements; work with social partners; own tests; sign off releases |
| **Answerability** | **Accountable officers**, including **country employer officers** | Answer to authorities, regulators, banks, insurers, clients, employees, directors |
| **Capability gaps** | **Employment counsel desk** | Agency-work law, conversions and transfers, classification, works councils |
| **Mobility** | **Mobility desk** | Residency disputes, certificates of cover, permanent-establishment judgement, equity for movers |
| **Client demand** | **Client partners**; pooled support | New countries, conversions, reorganisations |
| **The non-paying party** | **Employee relations** and **employee support** | Exits, disputes; illness, bereavement, parental leave. A person at the front, in the employee's language and time zone |
| **A counterparty's channel** | **Authority desk** | Notices, audits, period corrections, reclaims from state funds, countries without interfaces |
| **Money** | **Treasury and credit desk** | Funding, liquidity, FX, credit limits, springing reserves, wind-down plans |
| **Entities** | **Entity and bank operations** | Entity in a box, statutory audit, transfer pricing, bank relationships, director support |
| **Scaffolding** | Builders and evaluators; fraud desk; growth and partner certification | Engines, adapters, recomputer, evaluation, open agreement tools |

### 7.2 Agent architecture

One shared state. Its centre is **each employment**: contract, events, location, liabilities, money, authority positions, the person's rights, in three versions (as true, as known, as filed).

| Layer | Agents |
| --- | --- |
| **Per employment** | **Employment agent**: holds the executable contract, applies events including location, keeps the conditions true, explains pay, applies the error policy |
| **Per client** | **Client orchestrator**: policies, the dial, decision moments, credit limit, wind-down plan |
| **Rule engines** | Statutory packs per country; agreement packs per sector and company; an **independent recomputer** on different code and model |
| **Mobility** | Day counter, threshold monitor, certificate and shadow-payroll agents |
| **Money** | Treasury agent; credit monitor and springing-reserve trigger; payee verification |
| **Counterparties** | Authority adapters; HR systems; cap tables; benefits; banks; partners; social partners; outside agents |
| **Verification and governance** | Condition monitors; release harness running each rule change against everyone; constitution auditor; director and bank views; **four circuit breakers**: money, credit, filings, terminations |

**Constitution clauses** [reasoned]: hold only what law or a client's refusal of data requires, briefly, with an independent trustee, and take no float or FX income; earn the same margin in every setting of the dial; as legal employer, owe employees the law's full duties even against the client, and run no unlawful exit; where law ranks the employee above the client, follow the ranking without commercial appeal; use payroll data against an employee only where law compels it, and tell them; never use absence, sickness, union, location or family data otherwise; track no one's location; the record leaves on request, and every owned entity has a named successor.

### 7.3 Rhythm

Continuous: events, pay, location counts, conditions, reports. Daily: treasury, credit signals, exceptions. Each payday the employee chose: release of a state already checked. Each period end: close and corrections as each state requires. Monthly: authority positions, a cost letter to each client, partner audits. Before each law change and bargaining round: simulation. Quarterly: published solvency. Annually: year-end as confirmation, a successor drill, a policy review. Agents absorb the payday and year-end peaks; the human peak is exits after a downturn [reasoned].

### 7.4 Headcount sketch [conjecture]

Volumes: **2027**, 250 clients, 5,000 employees, half on EOR, 12 owned countries. **2030**, 1,200 clients, 35,000 employees, 25 owned countries. **2035**, 3,500 clients, 150,000 employees (40% EOR or entity in a box), 40 owned countries, partners in about 100 more. A traditional provider at the same mix is assumed to need one person per 200 employees, counting sales, support, legal and finance [conjecture].

| Role | 2027 | 2030 A | 2030 B | 2035 A | 2035 B |
| --- | --- | --- | --- | --- | --- |
| Owners and board | 3 | 3 | 3 | 3 | 3 |
| Accountable officers, incl. country employer officers | 6 | 10 | 10 | 16 | 18 |
| Rule-pack and agreement standard-setters | 10 | 22 | 26 | 34 | 48 |
| Employment counsel desk | 6 | 12 | 16 | 24 | 34 |
| Mobility desk | 1 | 4 | 6 | 12 | 18 |
| Employee relations desk | 4 | 10 | 14 | 25 | 40 |
| Employee support | 4 | 14 | 20 | 40 | 55 |
| Authority desk | 3 | 6 | 8 | 8 | 14 |
| Treasury and credit | 4 | 7 | 8 | 12 | 16 |
| Entity and bank operations | 3 | 6 | 7 | 12 | 16 |
| Client partners and pooled support | 6 | 15 | 18 | 35 | 45 |
| Builders and evaluators | 20 | 30 | 32 | 40 | 46 |
| Fraud and security | 2 | 4 | 5 | 8 | 12 |
| Growth and partner certification | 6 | 15 | 17 | 25 | 30 |
| **Total** | **78** | **158** | **190** | **294** | **395** |
| Employees per person | 64 | 222 | 184 | 510 | 380 |
| **Traditional at the same volume** | **25** | **175** | **175** | **750** | **750** |

The first draft had 226 (A) and 306 (B). The rise comes from the agreement layer, support in many languages and time zones, mobility, entity operations and credit [reasoned, from both reviews].

### 7.5 What drives it [reasoned]

1. **Countries owned.** Each needs a rule-pack owner, an employer officer, an entity team and authority links, whatever its volume: a fixed cost.
2. **Agreements, not countries, set the rule workload.** Belgium's joint committees, France's *conventions collectives*, Germany's *Tarifverträge* and Italy's national agreements each multiply the rules [general knowledge, not checked; practitioner review]. Open co-maintenance with social partners is what keeps standard-setters at 34 rather than 100.
3. **Exits.** At 15% turnover, about 22,000 a year by 2035 [conjecture]. The contested few per cent make employee relations the largest human edge, and the most sensitive to landscape B.
4. **Mobility.** Grows with remote work, whatever the volume of employees.
5. **Languages and time zones.** Support for illness and bereavement cannot be pooled across them.
6. **Authorities' interfaces.** Each country without them adds to the authority desk.
7. **The review rule.** If authorities or auditors want per-payslip sign-off, B's numbers hold even in A.
8. **The 2027 penalty.** Engines, entities and credit come first, so the firm costs more per employee than a bureau for three years.

---

## 8. Economics [conjecture throughout]

### 8.1 What is sold, and how it is priced

| Product | Price, 2027 | 2035 A | 2035 B | D |
| --- | --- | --- | --- | --- |
| **Employment** (EOR or entity in a box: conditions, contract, guarantees), per employee-month, form-neutral | $450 | $220 | $300 | $100 |
| **Payroll** for clients' own entities, per employee-month | $60 | $25 | $40 | $8 |
| **FX** | Interbank plus 0.2% | 0.2% | 0.2% | 0.1% |
| **Credit** (paying first, carrying accruals) | About 0.5% of EOR flows, disclosed | Same | Same | 0.4% |
| **Mobility and portable employment** | Per mobile person-month | Same | Same | Same |
| **Rule packs** | Open, free | Open | Open | Open |

Today's EOR list prices sit around $600 per employee-month [seen: Remote's pages at $599 to $699, cited in builder review]. **Pricing logic:** price the condition, the accountability and the credit, never the run, and never the time money sits still.

### 8.2 Revenue, cost and margin

| $m | 2027 | 2035 A | 2035 B | 2035 D |
| --- | --- | --- | --- | --- |
| Employment (EOR and entity in a box) | 13.5 | 158 | 216 | 72 |
| Payroll | 1.8 | 27 | 43 | 9 |
| FX fee | 0.3 | 12 | 12 | 6 |
| Credit and guarantees | 0.5 | 25 | 27 | 20 |
| Mobility and portable employment | 0.3 | 20 | 24 | 12 |
| **Revenue** | **16.4** | **242** | **322** | **119** |
| People (about $150,000 loaded) | 11.7 | 44 | 59 | 42 (about 280) |
| Partner fees for tail countries | 3.0 | 16 | 19 | 9 |
| Entities, banks, audits, local accounting, directors | 3.5 | 12 | 13 | 11 |
| Funding, insurance, capital cost, credit losses | 1.5 | 23 | 25 | 22 |
| Models, compute, verification | 0.6 | 8 | 10 | 6 |
| Banking and rails | 0.5 | 7 | 7 | 6 |
| Acquisition and partners | 4.0 | 30 | 35 | 12 |
| External counsel, licences | 3.0 | 8 | 10 | 6 |
| Error-policy write-offs | 0.1 | 1 | 1 | 1 |
| **Cost** | **27.9** | **149** | **179** | **115** |
| **Margin** | **about −70%** | **about 38%** | **about 44%** | **about 3%** |

Credit cost in 2035 A is built as: funding about ten days of EOR payroll (about $140m average) at 5%, about $7m; credit losses about 0.15% of EOR flows, $8m, which a bad year could triple or quadruple; insurance and capital charge, about $8m.

### 8.3 Where profit comes from, and where it does not

1. **Employment as an accountable service.** Being the employer and answering for it is the scarce layer.
2. **Credit, priced from the firm's own data** on cash, defaults and recoveries. This replaces deposits and float as the money business, and it is aligned: the firm earns by keeping clients' cash free, not by holding it.
3. **Mobility,** the problem that grows fastest and that only a holder of cross-border employment records can solve continuously.
4. **Low marginal cost per employee in owned countries.**

**Not from float, deposits or FX spread.** The first draft put the forgone float at about $15m. The builder was right that this counted all flows; only EOR flows would be held, so transit float is about $6m. But the incumbent model also holds **deposits** (a month of EOR cost, about $420m) and **accruals** (perhaps 1.5 months, about $630m) [conjecture]. With transit balances, that is about $1.2bn, or about $37m a year at 3%. A spread of 0.5% rather than 0.1% on $6bn of cross-currency flows would add about $24m. **In landscape D, the incumbent's money model would lift margin from about 3% to about 26% on float alone.** The temptation is larger than first stated, not smaller. The design's answer is structural: it does not hold the balances at all, so there is nothing to be tempted by.

### 8.4 What the numbers say [reasoned, on conjectured numbers]

- **A and B are both good,** B slightly better, as in accountancy: prices hold while people cost more.
- **D is break-even.** The firm survives D by owning fewer countries (about 25, partners for the rest), which would recover perhaps seven to ten points [conjecture], not by taking float.
- **2027 loses about $11m,** plus first-loss capital for the credit facility.

---

## 9. How it is built from 2027

### 9.1 The wedge

The first draft chose companies of 50 to 500 people in 4 to 15 countries. The builder is right that this is exactly what Deel, Remote and Rippling already sell to [experience, builder review]. Competing there on design alone is weak.

**The redesigned wedge: companies already on an EOR who are paying too long, in the wrong form, or with cash tied up** [reasoned]. Typically 50 to 500 people, with staff on EOR past a year, in countries where agency-work caps or equal-treatment rules bite, or with people working from countries where nobody is registered. The offer: **the provider that is paid the same whether you stay or graduate; no deposit; no FX spread or float; location handled live; and a guarantee against our own failure.** Incumbents cannot easily match form-neutral pricing or abolish deposits, because both cut their income [reasoned].

### 9.2 Distribution

Through investors and venture lenders, who want employment risk clean in due diligence and dislike cash sitting in deposits; through the accountancy platform in `level3-accountancy.md` for UK companies' first hires abroad; through immigration and mobility advisers; through HR systems that do not sell EOR; through certified partners in the tail [conjecture].

### 9.3 Country sequence [conjecture for dates]

| Period | Owned countries | Mode | Why |
| --- | --- | --- | --- |
| **2027** | UK, Ireland, Netherlands, Germany, France, Spain, Portugal, Poland, US, Canada, Australia, India (12) | EOR where lawful; Germany EOR with permit, capped, then entity in a box; Netherlands EOR mirroring client terms; France entity in a box and *portage* only; Spain, Poland and Portugal checked one by one | Where target clients hire most; four have real-time or single monthly reporting to prove the design (UK, Ireland, Australia, France's DSN) |
| **2028–30** | Brazil, Mexico, Colombia, Argentina, Philippines, Singapore, Japan, Italy, Sweden, Denmark, Switzerland, Israel, South Africa (25 in all) | Mexico entity in a box only; Italy with agency rules checked | Event-reporting Brazil early; hiring hubs; Nordic states with mature digital government |
| **2031–35** | 15 more by volume (40); certified partners elsewhere | By country law | Own where volume pays for fixed cost |

**Capabilities in order** [conjecture]: **2027**, executable contracts with the statutory layer; credit as default through a capital partner; no deposits; the error policy; penalty guarantee; trustee and named successors; location as an event; authorities in the four reporting states offered the event stream. **2028**, the full dial with entity in a box and conversions; agreement packs with the first social partners; partner certification. **2029–30**, own payments authorisation for contractor flows; portable record linked to authority data; standby facility at full size; trusted-status talks with two authorities. **2031–35**, agreements as code across owned countries; worker as client where law allows; agent to agent.

---

## 10. The architecture test

### 10.1 Scoring G1 to G11 and C1 to C12

All verdicts are [reasoned]. One author designed and scored them; two reviewers in character challenged them. Where my verdict differs from a reviewer's, the reason is in the table and in the final section. The test I applied: **an element breaks when its purpose fails or it is filed in the wrong place; it bends when its purpose survives but its wording or mechanism must change.**

| # | Element | Verdict | Reason |
| --- | --- | --- | --- |
| **G1** | Shared record | **HOLDS** | Owned by the employer; the employee reads it and holds a linked copy; authorities read their slice; three versions (true, known, filed) make it fit for a tribunal or tax audit; outlives the relationship |
| **G2** | Acting in the flow, never an unchecked payee | **BENDS, deeply** | Holds fully for clients' own entities and entity in a box: the firm acts from the client's account under a revocable mandate. **As EOR, the firm is principal in law**: it pays first from its own money and is paid after, as a creditor. Its purpose survives (the firm never controls money it does not owe and never earns from holding it), so this is a bend, not a break. **Change:** "under a revocable mandate, or, where law makes the firm principal, as a principal and open creditor whose role is transferable, backed by capital, with no income from holding or converting money" |
| **G3** | Policy as work | **BENDS, mildly** | Policy still does the work. But the client writes only one of three layers; the state and social partners write the others, and works councils must agree some systems. **Change:** "policy as work, in layers, each owned by whoever has the right to write it" |
| **G4** | Conditions and moments | **HOLDS** | Four conditions kept continuously; the period close is a moment, short because the conditions hold |
| **G5** | People at the edges | **HOLDS** | The product is information, money and legal status; people at exits, crises, novel law, mobility disputes, authorities, credit |
| **G6** | Capability where information is born | **HOLDS** | In HR systems, cap tables, banks, authority interfaces, social partners' agreements and the person's own declaration of location; oversight both ways, including the client's conduct to workers |
| **G7** | Duties to every party, controls on the firm | **BENDS** | G7 asks for neutrality to non-paying parties and a revenue unit that rises only with the client's outcome. Here the firm is not neutral: the law ranks the employee above the paying client, daily. And per-employee-month EOR revenue rises with time on EOR, which can run against the client's interest. **Change:** "where law ranks duties, follow the ranking as a constitutional rule; and price so the firm gains nothing from the client staying in a form that no longer suits it" (form-neutral pricing) |
| **G8** | Evidence rules | **BENDS** | "Payroll data never used against the employee" cannot hold. Law requires overpayment recovery, attachment of earnings orders and reports to authorities. **Change:** "used against the person only where law compels it, and they are told"; location declared, never tracked |
| **G9** | Workforce as a designed condition | **HOLDS** | Applied to its proper object, the firm's own staff: scarce country, agreement and mobility experts are the binding constraint (7.5). The first draft's claim that "the client's workforce is the product" is withdrawn; duties to EOR employees belong in G7 |
| **G10** | The service survives the firm | **UNTESTED** | Designed for: trustee, standby facility, named successors, published solvency. But moving employees to a successor is governed by transfer-of-undertaking law and, in some countries, employee consent [general knowledge]. It holds on paper until a successor has run shadow payroll for a full year in at least one country |
| **G11** | Capacity shaped to demand in time | **HOLDS** | Paydays, period closes, year-ends, law-change dates, bargaining rounds; the human peak is exits after a downturn |
| **C1** | Priced and guaranteed outcomes | **HOLDS** | Guarantee computation, filing and payment timing, and the firm's own survival; insure classification and permanent-establishment risk. The first draft's wage guarantee against client default is withdrawn as a product: the law already gives it |
| **C2** | The standard | **BENDS** | One owner of the record, but the outward standard is set by forty states and many social partners, not one neutral body. The firm's data model becomes the de facto cross-border one. **Change:** "where many rule-writers exist, the firm opens its model and co-maintains it with them" |
| **C3** | Holding money | **BREAKS as a conditional** | Its trigger reads "one aligned principal, a regulated partner and no payee conflict"; otherwise "route and reserve". For an EOR, holding and advancing money is not a choice and cannot be routed. It is the business every day. As with home care's C7 and C9, the condition is met permanently, so the element is filed in the wrong place. **Fix:** under the principal-in-law parameter, custody and credit become core for that class of firm |
| **C4** | Pooled data | **HOLDS** | Error, default and mobility data pool lawfully; pay benchmarks are limited by competition law as well as privacy |
| **C5** | Mandate chain | **HOLDS, switched on** | Filing authorisations per country; who may change pay, bank details or location |
| **C6** | Custody beyond the firm | **HOLDS, within G10** | Pension and service records span decades; tested with G10 |
| **C7** | Surge capacity | **HOLDS, switched on in an unexpected place** | Correlated client failure in a downturn: credit losses, funding squeeze and exits together |
| **C8** | Licensed definition of good | **HOLDS, switched on in a new form** | Rule packs are open, so the large client with its own team buys the recomputer and the firm's accountability, not the code |
| **C9** | Pace set by the person | **HOLDS, switched on at moments** | Illness, bereavement, exits |
| **C10** | Rationed public payer | **HOLDS, switched on** | Statutory sick and parental pay often run through state funds with employer reclaim [general knowledge, not checked]. The firm deals with rationed public payers every month |
| **C11** | Decline as the trajectory | **HOLDS, switched on** | A good EOR relationship is meant to end in conversion. The firm plans its own decline with each client, and form-neutral pricing makes that decline cost it nothing |
| **C12** | Unpaid co-producers | **HOLDS, switched on modestly** | Employees declare location and correct their own record; the design removes most other data entry |

**Tally:** holds 16; bends 5 (G2, G3, G7, G8, C2); breaks 1 (C3, as a conditional); untested 1 (G10). The first draft said 21, 2, 0. The builder said 18, 3, 2; the practitioner 17, 5, 0, with one untested.

### 10.2 What the result means

**The control is not clean** [reasoned]. The first draft called it "nearly clean". That was the generous reading of a single author, and the generous verdicts sat where the firm owes duties against its paying client. The honest headline: **the information core holds; the money assumption breaks where the firm is principal in law; and the rule and loyalty assumptions bend where others write the rules and the law ranks the parties.**

**The information core holds where it should.** G1, G4, G5, G6 and G11 hold without strain. Executable contracts, events at source, continuous computation and reporting as a side effect survive every challenge. The elements home care added (G9, G10, G11) are general, though G10 is unproven here [reasoned].

**First missing parameter: agent or principal in law** [reasoned]. Every earlier design was an agent. An EOR is a principal: it owes the money itself, to employees and states, whatever the client does.
- *Agent:* act under a revocable mandate; hold nothing or hold under client-money rules.
- *Principal:* hold or advance by necessity; refuse income from holding; price credit openly; back the role with capital; make the role transferable.

Two things are new. First, the parameter is partly a **design choice**: the dial lets the firm be principal (EOR) in one country and agent (entity in a box) in the next, and law decides which is allowed where. Second, being principal **removed** the client-money problem rather than creating it: because the client's payment is revenue, credit as default means the firm holds almost nothing. The same parameter applies to any firm that stands in a client's legal shoes: a corporate trustee, an importer of record, a carrier, an insurer [reasoned].

**Second missing parameter: who writes the rules** (client, state or social partners) [reasoned; practitioner]. Every earlier design assumed the client writes policy and the state sets a stable frame. In much of Europe, unions and employers' associations write the pay rules. That bends G3 and C2 together. It also predicts where the standard must be open and co-maintained rather than owned.

**A third finding: duties can be ranked by law.** Earlier designs had non-paying parties owed neutrality (lettings' tenants) or advocacy (home care's person). Here the law ranks the non-paying employee above the paying client on defined matters. That is a third form of G7, sitting between neutrality and advocacy [reasoned; builder].

**What did not bend, and might have** [reasoned]. *Many regulators at once* multiplies G6 and C5 by the number of countries; **number of jurisdictions** sets fixed cost and the boundary, as volume sets headcount. It is a scale parameter, not a shape one. *Penalty guarantees* fitted C1 exactly. *Mobility* fitted G6, because location is born with the person and declared there.

**One finding goes beyond the scoring.** G7's revenue rule, followed honestly, gives up the largest profit pool incumbents have: ADP's interest on client funds is about $1.2bn a year [seen]. In landscape D, the incumbent money model is worth about 23 points of margin to this firm. The design's answer is to remove the balances, not to resist the temptation each year. Whether clients value that enough to switch is the commercial bet. The practitioner's view is that "no deposit" sells and "no float" barely registers [experience, practitioner review]. So the ethics are sold as cash freed, not as virtue.

---

## 11. What would make this design wrong, and the stress test

### 11.1 What would make it wrong

1. **States close the EOR route further.** EOR becomes a short bridge everywhere; entity in a box and conversion become the product. The dial already allows this [reasoned].
2. **States compute pay themselves.** Gross-to-net goes; employment, money, mobility and coherence remain [conjecture].
3. **HR systems bundle payroll and EOR free:** landscape D early [reasoned].
4. **Deel or Rippling reaches level 3 first.** They have clients, entities and licences. The clean-sheet edge is incentives: form-neutral pricing, no deposits, no float. If clients do not care, it is small [reasoned].
5. **Correlated client failure** in a funding downturn, with the firm's own funding line tightening at the same time, breaks capital sized for an average year. Credit as default makes this the firm's largest single risk [reasoned].
6. **A rule-pack error at scale** hits thousands of payslips; the recomputer and payday breaker matter most [reasoned].
7. **Payroll fraud** through bank-detail changes; one large incident would end trust [reasoned].
8. **Clients will not share cash data,** so prepayment stays common and credit stays small [conjecture].
9. **Social partners will not publish agreements as code,** so the agreement layer stays hand-built and standard-setters double [conjecture].
10. **Country, agreement and mobility experts are scarce** for 40 owned countries [reasoned].
11. **Banks de-risk** payroll accounts with large cross-border flows faster than the firm can explain them [experience, builder review].

### 11.2 The stress test against rules, institutions and adoption

| Fact | Effect on the design |
| --- | --- |
| **Germany requires a labour-leasing permit; one worker may be leased for at most 18 months** [seen, AÜG summaries]; equal pay after nine months [general knowledge, not checked] | Germany needs the permit from day one; the dial moves German staff to entity in a box well before the cap |
| **France prohibits profit-making supply of labour in principle; EOR is lawful mainly through *portage salarial*, with criminal penalties otherwise** [seen, cited in builder review: Addleshaw Goddard, Deloitte Avocats, 2026] | No EOR in France as such. Entity in a box for clients; *portage* for qualifying professionals, which is also the seed of "worker as client" |
| **Mexico banned personnel subcontracting in 2021, allowing only registered specialised services** [seen, cited in builder review: Littler, EY, PwC] | Mexico is entity in a box only |
| **EU agency-work rules require equal treatment with the client's comparable staff; the Netherlands has payrolling rules since 2020** [general knowledge, not checked] | The EOR contract mirrors the client's terms, read from its HR system. Agency licences checked country by country |
| **Collective agreements set much of pay in Belgium, France, Germany and Italy** [general knowledge, not checked] | Agreement layer in the rule engine; co-maintenance with social partners; standard-setters sized for it |
| **UK agencies became jointly and severally liable for umbrella companies' unpaid PAYE from 6 April 2026** [seen] | States are pushing liability up employment chains. The design accepts full employer liability, so this favours it. It also marks the danger for "worker as client": it must never look like an umbrella scheme |
| **Holding client funds and paying contractors need authorisation** (UK and EEA payment rules; US state money-transmitter licences; Deel held 26 in early 2025) [seen in part] | Credit as default keeps EOR money the firm's own; clients' own entities paid under mandate; contractors and prepayments through a regulated partner; own licences at volume |
| **Transfer of undertakings law and, in some countries, employee consent govern moving employees between employers** [general knowledge, not checked] | Conversions and successor step-in are run as lawful transfers with consultation. G10 stays untested until drilled |
| **Directors may be personally liable for unpaid social contributions, criminally in Germany** [general knowledge, not checked; builder review] | Directors get a live view of their entity's contributions and solvency; money controls are their reason to sign |
| **Minimum pay frequency, local-currency and local-account rules** [general knowledge, not checked] | Employee choice of cadence, currency and rail is bounded per country by the rule pack |
| **Authorities close periods; UK tax is cumulative** [general knowledge] | Three-version record; corrections by each state's process |
| **Real-time reporting exists in the UK, Ireland, Australia and Brazil; monthly single declarations in France and Norway** [seen, 2.3] | Start there; offer read access from 2027. The design does not depend on any state moving faster |
| **Employee data moving across borders** (EU transfer rules) [general knowledge] | Data held in-region; only aggregates cross |
| **Works councils must agree systems that can monitor employees** (Germany) [general knowledge, not checked] | Location declared, not tracked; evidence rules designed for works-council agreement |
| **Many countries require a resident director for a local company** [general knowledge] | Rented directors, supported by entity operations and the live view |
| **Permanent-establishment risk for clients whose staff conclude contracts abroad** [general knowledge] | Location as an event warns before the threshold; policy blocks risky roles under EOR; insurer carries the residual |
| **Clients trust incumbents with payroll; switching is feared** [reasoned] | Land on clients already paying deposits or stuck in the wrong form, and on new countries; the dial brings the rest over time |
| **Employees distrust payroll changes** [reasoned] | The live pay statement and error policy are the first things employees see; payday unchanged in year one unless the employee chooses |

### 11.3 What the stress test changes

1. **Not the information core.** Executable contracts, continuous pay, the three-version record, policy and the conditions survive today's rules.
2. **The dial is the business, not a feature,** because labour-leasing and agency rules make EOR a bridge, or unlawful, in many owned countries. Entity in a box is as important as EOR.
3. **Money comes first in the build:** capital partner, trustee, named successors and insurance before the first payday; own licences follow volume.
4. **The architecture's two new parameters are facts of law.** Labour-leasing permits, joint and several liability and money-transmission licences all treat the EOR as a principal. Collective-bargaining law makes social partners rule-writers. Neither is a design preference.

**Where this is weakest.** Every number is conjecture. Six figures decide it, and none is known: how much of a client's pay data can be born structured in year one; credit losses in a bad year with funding tight; how many countries and agreements the firm can own well; whether social partners will co-maintain agreements; whether clients value no deposit and form-neutral pricing enough to switch; and how fast authorities move to event data. The first two can be measured in the wedge's first year. G10 needs a live drill before anyone should rely on it.

---

## Sources checked in this run

- ADP interest on client funds, financial year 2025 (about $1.2bn on $37.6bn average balances): ADP fourth-quarter 2025 earnings release, SEC exhibit 99.
- Deel licences and scale: Deel legal hub and licence pages; Deel blog on its Australian licence (August 2025); Business Wire releases, June and October 2025; Sacra estimates (not company figures).
- German labour leasing (AÜG): Bird & Bird factsheet; Noerr FAQ; Freshfields "Employers of record" series; statutory text on gesetze-im-internet.de (not fully read).
- UK umbrella company joint and several liability from April 2026: gov.uk policy paper; KPMG; Pinsent Masons; Clyde & Co; Osborne Clarke.
- EU Pay Transparency Directive status: Baker McKenzie (June 2026); King & Spalding; Littler.
- EU VAT in the Digital Age: European Commission adoption notice, March 2025.
- Real-time payroll regimes: Canadian Payroll Association paper on global trends; Australian STP summaries; Brazil eSocial summaries (Oracle, activpayroll).
- Checked by the builder reviewer, not re-checked by me: France's rules on labour supply and *portage salarial* (Addleshaw Goddard, September 2026; Deloitte Société d'Avocats); Mexico's 2021 subcontracting reform (Littler, EY, PwC); Remote's EOR pricing ($599 to $699 per employee-month).
- Not checked in this run, general knowledge: Ireland PAYE Modernisation start date; France DSN and Norway a-melding details; EU Temporary Agency Work Directive and Dutch payrolling rules; German equal pay after nine months; collective-agreement systems in Belgium, France, Germany and Italy; deposits; instant payment rails; EU insolvency wage-guarantee funds; transfer-of-undertakings rules; directors' liability for social contributions; German works-council rules; resident director rules; minimum pay frequency rules; statutory sick and parental pay reclaims; EU digital identity wallets; Swedish self-employment companies; Rippling's product scope.
- Reviewers' [experience] claims are operator judgement in character, unchecked.

---

## Review and response

Two reviews, both written in character on 24 November 2026: a founder of a global EOR and payroll platform (the builder), and a head of global payroll and employment compliance (the practitioner). Both found the control result stated too kindly. Their operator judgements are informed views, not evidence.

### What I took, and why

| Point | From | What changed |
| --- | --- | --- |
| The EOR invoice is revenue, not client money; a trust is a choice and may pull in safeguarding rules | Builder | Section 6.2 rewritten. The firm's position is creditor, not custodian. Trustee kept only for prepayments and for protection against the firm's own failure |
| "Debit on payday morning" is credit in disguise; it will not work across currencies, treasury blocks and cut-offs | Builder, Practitioner | **Bolder fix:** credit as the default, priced openly; deposits abolished |
| The real balances are accruals | Builder | Accruals stay with the client; a springing reserve starts only on risk signals |
| Float overstated: only EOR flows are held | Builder | Transit float cut to about $6m. But deposits and accruals were missing; the full incumbent money model is about $37m, so the temptation rises (see conflicts) |
| EOR is labour leasing or banned in much of Europe and Latin America; France and Mexico unsafe as written | Builder, Practitioner | Dial redesigned with four settings and entity in a box; France and Mexico moved off EOR; Germany capped; Netherlands mirrors client terms |
| Conversion is a transfer of employment, not a record carrying across | Builder | Run as a lawful transfer with consultation; record carries continuity evidence |
| Equal treatment means the contract must mirror the client's terms, which the firm "does not hold" | Practitioner | Redesigned around: the firm already reads the client's HR system, so the EOR contract is generated from the client's terms for comparable staff |
| Entities need banks, audits, transfer pricing and directors who fear personal liability | Builder | Entity and bank operations role; cost line doubled; live director and bank views; treasury as the way to recruit directors |
| Contractors and worker wallets are missing | Builder | Contractors paid under mandate or via a regulated partner; no worker wallets |
| The unit of rules is country × sector agreement × company agreement | Practitioner | Three-layer rule engine; standard-setters up from 20 to 34 (A) and 26 to 48 (B); agreements as code with social partners |
| Late facts and closed periods: the run survives as a legal unit | Practitioner | Three-version record (true, known, filed); period close kept as a moment |
| Publish an employee-first error policy | Practitioner | New item 4.7; write-off line in costs |
| Location as a live event; mobility is the biggest missing product | Builder, Practitioner | New item 4.3, mobility desk, revenue line, headline point 3 |
| Payday survives; let the employee choose cadence, currency and rail | Builder | Item 4.9, bounded by law per country |
| "72 hours" is today, not 2035 | Builder | Replaced with "hire in the right form, once"; real gates named |
| The wage guarantee restates the law; the real gap is the firm's own failure | Builder | Client-default guarantee withdrawn as a product; trustee, standby facility, named successors, published solvency added |
| Open the rule packs; the edge is accountability | Builder | Rule packs open; licensing revenue removed; C8 switched on as certification and recomputer |
| Portable record should link to authority data and identity wallets | Practitioner | Item 4.10 rewritten |
| Support too lean for languages and time zones | Practitioner | Employee support doubled (20 to 40 in A; 32 to 55 in B) |
| The wedge is the incumbents' core; HR systems sell EOR | Builder | Wedge moved to clients stuck on EOR, in the wrong form or with cash in deposits; form-neutral pricing as the offer; HR systems that sell EOR treated as rivals |
| Offer authorities the event stream from day one | Practitioner | Moved from 2031 to 2027, as an offer the design does not depend on |
| Sell "no deposit"; buyers pay for one accountable party, controls evidence, local support and fast fixes | Practitioner | Sales story in 9.1 and 10.2 leads with cash freed |
| Make the worker a client | Builder | Item 4.15, from 2031, with the UK umbrella danger named |

### Where reviewers conflicted, or I differed from one, and which way I went

1. **G2: bends or breaks?** The builder said BREAKS for EOR, because the fix reverses "sit beside the money". The practitioner called BENDS fair. **I kept BENDS, marked "deeply".** Reason: I applied the same test as home care's G2: an element breaks when its purpose fails, bends when its mechanism changes. G2's purpose, never controlling or profiting from money the firm does not owe, survives intact. Credit as default makes it survive better: the firm now holds almost nothing. What reverses is the mechanism, from mandate to principal.
2. **C3: bends or breaks?** The builder said BREAKS as a conditional; the practitioner accepted BENDS. **I went with the builder.** Reason: his precedent is exact. Home care's C7 and C9 broke as conditionals because their condition was met every day. C3's alternative, "route and reserve", is not available to an EOR at all.
3. **Is the float temptation smaller or larger?** The builder said smaller, so the commercial bet is cheaper. **I found it larger.** He is right on transit float, but the first draft and his review both left out deposits and the accrual balances he himself named. With them, the incumbent model is worth about 23 points of margin in D. My response is not to resist the temptation but to remove the balances.
4. **G9: bends or holds?** The builder said BENDS, because "the workforce is the product" stretches G9. **I agreed with his reasoning and differed on the verdict.** The stretch was mine; I withdrew it. Applied to its proper object, the firm's own scarce experts, G9 holds plainly. The duties to EOR employees belong in G7, which I moved to BENDS.
5. **G7.** The builder said BENDS (ranked duties); the practitioner did not contest HOLDS. **I took the builder's verdict and added a second reason:** per-employee-month EOR revenue rises with time on EOR, which can run against the client. Form-neutral pricing is the fix.
6. **G3, G8, C2, C10, G10.** Raised by the practitioner (C2 also by the builder). The builder did not contest G3, G8, C10 or G10. **I took all five**, because each rests on a rule the first draft ignored: social partners, compelled data use, many rule-writers, state funds for statutory pay, and transfer law.
7. **C11.** The builder said switched on; the practitioner was silent. **Taken:** conversion is planned decline, and form-neutral pricing makes it costless to the firm.
8. **Which missing parameter?** The builder saw one (agent or principal); the practitioner saw two (adding who writes the rules). **I went with two**, because G3 and C2 bend together for the same reason, and no earlier parameter explains it.
9. **Was the money section the best part, or misdescribed?** The practitioner praised it; the builder said its mechanics were wrong. **Both were right:** the direction (no float, no spread, shrink custody) held; the mechanics did not. I kept the direction and rebuilt the mechanics.

### What I declined

- The builder's BREAKS on G2 (point 1 above).
- The builder's BENDS on G9 (point 4 above).
- Owning France and Mexico as EOR countries in any form; both reviewers implied this, and the redesign goes further by making entity in a box the default there.
- Making the design depend on authorities reading the event stream; it is offered, not assumed.

### Verdict changes

G7 HOLDS to BENDS (builder). G8 HOLDS to BENDS (practitioner). G3 HOLDS to BENDS, mildly (practitioner). C2 HOLDS to BENDS (both). C3 BENDS to BREAKS as a conditional (builder). G10 HOLDS to UNTESTED (practitioner). C10 not switched on to switched on (practitioner). C11 not switched on to switched on (builder). C8 switched on in a new form (from the builder's open rule packs). G2 kept at BENDS, now "deeply". G9 kept at HOLDS, for a different reason. **Tally: 16 holds, 5 bends, 1 break, 1 untested. The control is not clean.** Two parameters are added to the scorecard: agent or principal in law, and who writes the rules.

### What remains true of the process

One author still designed, scored and revised this. The reviewers were written in character, and their [experience] claims are unchecked. The direction of every change after review was towards more bends, not fewer. That suggests the first draft's scoring was generous, and it may still be.
