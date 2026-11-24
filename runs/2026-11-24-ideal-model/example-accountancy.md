# Worked example: accountancy and tax for small UK businesses, designed as an agent enterprise

Draft by Claude, 24 November 2026. Revised the same day after a practitioner's review (`example-accountancy-review.md`). It applies step 3b to one service, using step 1, step 3 and inventory A. Labels: **[seen]** exists today; **[reasoned]** follows from logic; **[conjecture]** plausible towards 2035. Every volume, price and headcount is a model figure for argument, not a finding. Rules, insurance and courts show where people are needed and are applied as a stress test in section 8, not as the starting point. Section 9 lists each review point and what changed.

**The main change after review.** The first draft treated production as the hard part. It is not. The hard part is getting true, complete facts out of owners on time, and getting them to approve and pay. Production is still worth automating, because that is what frees people and makes the live tax estimate possible. But the design now puts the client side at the centre: intake, approval and payment are case types with their own agents, metrics and people.

---

## 1. The service as products

### 1.1 Clients

A firm of about 5,000 clients, in about 4,000 households, split for the model as follows [conjecture]:

| Segment | Clients | What they need most |
| --- | --- | --- |
| **Owner-managed companies, stable** (one to ten staff) | 2,000 | Accounts, corporation tax, payroll, VAT, the directors' own tax returns, remuneration planning |
| **Growing companies** (ten to fifty staff, rising revenue) | 500 | All of the above, plus monthly management information, cash forecasts, lender reporting, advice on hiring, funding and structure |
| **Sole traders and partnerships** | 1,000 | Bookkeeping, VAT where registered, Making Tax Digital quarterly updates, self-assessment |
| **Landlords** | 1,000 | Rental records, quarterly updates, self-assessment, capital gains on sale |
| **Individuals tied to the above** (directors, partners, spouses) | 500 extra returns | Self-assessment; often the same household as a company client |

The owner of a small business does not separate the business's money from their own. The real client is usually a household with a company attached [reasoned]. The shared state is built around that, not around entities.

**How the firm reaches 5,000 clients.** Realistically by buying practices, at around one times annual fees [seen, from the reviewer's practice]. Bought books arrive with desktop software, old habits, a retiring partner the clients trust, and churn of 5–15% after the sale [seen, from practice]. Migration is therefore a standing case type (1.3, number 24), not a one-off project.

### 1.2 The promise

One public promise, which is also the specification:

> **"You always know your tax bill before it is due. Your books are current up to the last thing you told us, and we ask about anything new within a day. Every deadline is met if you answer and approve by the dates we set. You can ask anything at any hour, and a named person knows you."**

Five parts, each testable:
- **No surprise bill (the headline):** a live estimate of every tax liability, updated as the ledger moves. This is what owners value and what no traditional firm offers [reasoned].
- **Books current to the last fact supplied:** the bank side reconciled within two working days; everything that needs the owner asked about within one working day, one question at a time [conjecture: targets]. From practice, 10–20% of lines in a small company need the owner, and owners answer in batches, late [seen]. No model makes an owner reply. The promise says so, so that the guarantee does not become the main source of disputes.
- **No missed deadline:** for any obligation where the client answered and approved by the date we set.
- **A named person:** every household has one (section 4).
- **Guarantees:** the firm pays penalties and interest caused by its own errors. Many firms already do this [seen, from practice], so it is hygiene, not a selling point. A newer guarantee is possible once error data exists: **if the final bill differs from our estimate by more than a stated margin for a reason we could have known, we credit part of the fee** [conjecture]. That guarantees the thing the client actually buys.

The promise turns year-end work into a maintained condition. A ledger reconciled daily gives about 250 checks a year instead of one [reasoned, step 1 P2].

### 1.3 The work as case types

Inventory A lists 61 client lines and a set of back-office lines. They group into 24 case types. Audit (inventory section J) is left out: it is reserved by law and is a small, separate business [seen, inventory A]. The first draft left out the back-office and client-side lines (K5, K6, L2–L5). They are back in, because they are where deadlines and money are actually lost.

| # | Case type | Inventory lines | Kind | Volume a year at 5,000 clients [conjecture] |
| --- | --- | --- | --- | --- |
| 1 | **Ledger upkeep**: coding, reconciliation, invoices, supplier statements, month-end journals | A1–A4, A7 | Routine | About 2,500 clients kept continuously; tens of thousands of client-months |
| 2 | **Intake: questions to the owner and records capture**. The core product, not a chase | A5, D1, D4, F1 | Routine machinery, human-paced input | About 150,000 single questions; target reply time measured per owner |
| 3 | **VAT return** | B1, B5 | Routine | About 1,500 registrations × 4 = 6,000 |
| 4 | **Payroll run**, including starters, leavers, pensions, construction scheme, and employees' payslip queries | C1–C3, C6, part of C7 | Routine | About 1,200 payrolls, 15,000 runs; several thousand employee queries |
| 5 | **Making Tax Digital quarterly update** | F4 | Routine | Arrives in steps: income over £50,000 from April 2026, over £30,000 from April 2027, over £20,000 from April 2028 [seen, gov.uk]. About 3,000 updates in 2026–27, rising to about 6,400 from 2028–29 |
| 6 | **Year-end accounts production and filing** | D2, D6, D8, D9 | Routine | About 2,500 sets |
| 7 | **Corporation tax return** | E1, E2, E4 | Routine | About 2,500 |
| 8 | **Self-assessment return** | F2, F3, F7 | Routine | About 3,500 |
| 9 | **Company secretarial** | G1–G3, G5 | Routine | About 2,500 confirmations, 3,000 events |
| 10 | **Onboarding and due diligence**: identity, ownership, risk, clearance | K1–K3, G4 | Routine with a judgement edge | About 600 new clients a year plus bought books; 5,000 refreshes |
| 11 | **Payroll year end and benefits** | C4, C5 | Routine with a judgement edge | 1,200 schemes; 1,000 benefit forms |
| 12 | **Clean-up** of messy or neglected books | A6 | Diagnostic | About 300 |
| 13 | **Year-end judgement items**: director's loan account, accruals, stock, work in progress, going concern | D3 | Diagnostic, limited by the client's facts | Inside every set of accounts |
| 14 | **HMRC correspondence and disputes short of enquiry**: codes, penalties, payment plans, VAT queries, 60-day property returns, "nudge" letters, **and HMRC's own errors** (misallocated payments, wrong codes, lost post, stuck repayments, dropped authorisations) | B2, B3, C7, F5, F6 | Diagnostic | About 3,500 items; from practice about a third of the effort is HMRC's errors, not the firm's [seen] |
| 15 | **Management information and forecasts** | H1, H2, H4 | Diagnostic | 500 clients monthly; 300 forecasts |
| 16 | **Everyday questions and remuneration planning** | I1, I2, I4 | Mostly routine (factual questions; arithmetic planning), diagnostic at the edge | About 25,000 questions; 2,500 plans, run every year unprompted |
| 17 | **HMRC enquiries and investigations, R&D and loss claims** | E5, I5 | Residual judgement | About 150 |
| 18 | **Decisions with consequences beyond tax**: selling, restructuring, raising money, distress, redundancy, specialist VAT | B4, I3, H3 | Residual judgement | About 200 projects |
| 19 | **Approval and payment**: the client approves the return or accounts and pays the tax | Spread across D, E, F; not a line in inventory A | **Bottleneck**. Routine machinery, human-paced | About 12,000 approvals; about 9,000 tax payments and payments on account |
| 20 | **Agent authorisation and access**: HMRC agent authorisation per tax, Companies House authority, ledger and bank access | K5 | Routine, but held up by the client and HMRC | About 600 new clients × several taxes; a wave of re-authorisation as each Making Tax Digital cohort joins |
| 21 | **Billing, collection and scope** | L2–L5 | Routine with a judgement edge | 5,000 subscriptions; failed collections; scope changes |
| 22 | **Life events and household splits**: death and probate, divorce, serious illness, emigration, co-directors falling out | Not in inventory A | Residual judgement | About 150–250 a year at 4,000 households [conjecture] |
| 23 | **Leavers and handover out** | K6 | Routine | About 300–500 a year |
| 24 | **Acquisition and migration of bought books** | I6, A6 at scale | Diagnostic | One to three books a year, a few hundred to 1,500 clients each |

Two controls are not case types but run across them:
- **Fraud and impersonation control:** changed bank details in a payroll email, fake HMRC calls to clients, clients inventing invoices for a lender [seen, from practice]. It needs its own agents and envelopes (2.3, 2.6, 3.15).
- **HMRC-statement reconciliation:** the firm keeps its own record of what each client paid and filed, and checks HMRC's account against it. HMRC is treated as a counterparty that makes errors, not as ground truth.

The split, by work rather than count [reasoned, from inventory A's hours, adjusted]:
- **Routine (1–11, 19–21, 23):** about 65% of today's hours.
- **Diagnostic (12–16, 24):** about 22%.
- **Residual judgement (17, 18, 22):** about 13% of hours and a much larger share of what clients value [reasoned].

The client-side types (2, 19, 20, 21) are routine to run and slow to finish. Their limit is the owner's attention, not the agent's ability. That is a different kind of hard from anything in production [reasoned].

---

## 2. The agent enterprise for this service

### 2.1 The constitution, in concrete clauses

Short, and written so agents can cite it. Examples:

1. **Purpose.** Keep each client's financial affairs true, current and compliant, and tell them in plain words what is coming and what they can choose.
2. **The client is the taxpayer.** We act as their agent. We never file, pay or tell a third party anything without a recorded instruction from the client or a standing authority they gave.
3. **Tax positions.** We take a position only where we would expect to defend it successfully. Any position below that bar goes to the judgement desk with the reasoning, and is disclosed to the client in writing. We never take a position that depends on HMRC not looking.
4. **Facts before tax effect.** We record what the owner says a payment was for when it happens, before anyone knows its tax effect. We do not rebuild facts at year end to fit a tax answer. Where we must reconstruct, we say so in the file.
5. **When unsure, say so.** An agent that cannot assess a matter says "cannot assess" and routes it. It does not guess [seen as a practice: LayerX, step 3b].
6. **Deadlines over speed, accuracy over deadlines.** We will file late rather than file something we believe is wrong, and tell the client why that day.
7. **Money.** No agent moves client money. Agents prepare payment files; the client or their bank releases them, except for standing arrangements the client has approved within set limits. Any change of payee bank details is confirmed through a second, known channel before it enters a payment file.
8. **What we will not do.** Regulated investment or pensions advice; insolvency appointments; audit; anything requiring a licence the firm does not hold. We refer.
9. **Errors.** When we find an error that harms a client, we tell them within one working day, fix it, and carry the cost of penalties and interest caused by our error.
10. **Conflicts.** When the people in a household or company stop sharing interests (divorce, a director dispute, an estate), we say so to each of them, stop acting on one person's instruction for the others, and decide who we act for. If we cannot act fairly for both, we act for neither on that matter.
11. **Non-payment.** We do not miss a statutory deadline because fees are unpaid without at least 30 days' written notice. We do not hold records or the position registry hostage when a client leaves.
12. **Suspicion.** Money-laundering concerns go to the reporting officer; agents must not tip off the client [seen as a legal duty].

Clauses 3, 4, 6, 9 and 10 are where the firm's values show. A rival using the same models will differ here.

### 2.2 The shared state

One append-only record of events. Agents read it and write to it through typed actions. They never coordinate by message.

**Entities:** households linked to legal entities; people (owners, directors, employees, executors, former spouses) with roles, consents and **conflict flags**; ledgers, mirrored from the client's ledger platform but held in the firm's own form, so that the firm can change platform; each transaction's source, coding reason and **the owner's stated intent with its date**; documents linked to transactions; obligations with due dates and required inputs; **positions** (every tax judgement, with reasoning, confidence and challenge window); filings and payments; **HMRC's account as HMRC shows it, beside the firm's own record**; forecasts as dated predictions; advice with its facts and stated risks; authorities, standing instructions and agent authorisations per tax; fees, collections and scope; typed cases with their checks and outcomes.

**Events:** transaction or document arrived; question asked; answer received; obligation opened; draft produced; check passed or failed; client approved; filed; accepted or rejected; tax paid; HMRC account mismatch found; letter received; position challenged; forecast scored; payee details changed; life event recorded; conflict flagged; fee collected or failed; client left; error found; playbook changed; breaker tripped.

Four items are new compared with a traditional firm, and they carry the design [reasoned]:
- **The position registry** makes the slow outcome check possible.
- **Forecasts as scored predictions** turn advice into something checkable (step 1, P2).
- **Intent captured at the time of the transaction.** It turns the director's loan account from a year-end reconstruction into a running record (3.5).
- **A platform-independent ledger mirror.** The ledger vendors control the interfaces and are building their own agents (3.19). The firm's state cannot live only inside a rival's product.

### 2.3 Agent roles specific to this service

| Layer | Roles |
| --- | --- |
| **Front door** | **Intake agent**: the core product. It works in the chat channel the owner already uses, asks one question at a time, accepts a photo or a voice note, proposes the likely answer ("Is the £400 to Dave the usual subcontractor payment?"), and learns each owner's patterns. Scored on owner reply time and answers later corrected. Also: client interface (chat, voice, portal, an interface for clients' own agents); intake and typing; the household mapper; an **employee-query agent** that answers payslip questions within a scope the employer sets |
| **Production** | Ledger keeper; obligation watcher; preparers per case type; forecaster; drafting agent for advice; **remuneration planner** that runs every company every year unprompted |
| **Client side** | **Approval and payment agent** (3.13); authorisation agent; billing and collection agent; leaver-handover agent |
| **Counterparties** | HMRC filer; HMRC correspondent; **HMRC-account reconciler**; Companies House filer; bank and open-banking connector; pension-provider connector; ledger-platform connectors (more than one); prior-accountant clearance agent; lender-pack agent |
| **Verification** | Independent recomputer (different code and model); consequence tracker; position auditor; outcome scorer (amendments, enquiries, forecast error, estimate error) |
| **Improvement** | Trace reader; playbook proposer; rule watcher (Budgets, Finance Bills, HMRC manuals, tribunal decisions) |
| **Evaluation** | Test-suite custodian; holdout keeper; shadow-run manager for new models |
| **Operations and commercial** | Billing; compute budget; security; pricing; scope monitor; **migration planner** for bought books |
| **Governance** | Constitution auditor; budget enforcer; circuit breaker; anti-money-laundering monitor; **fraud monitor** (payee changes, unusual payment files, documents that do not match bank evidence, impersonation attempts); **conflict detector** (life events, director disputes) |

### 2.4 Counterparties and how agents deal with them

| Counterparty | Channel today | How agents deal with it |
| --- | --- | --- |
| **HMRC, filing** | Software interfaces for VAT, income tax updates, corporation tax, payroll [seen] | Directly, through the firm's agent credentials |
| **HMRC, everything else** | Web pages that must not be automated; phone; post [seen, inventory A S10] | Agents prepare everything, including replies to formulaic "nudge" letters. A person presses the button, sends, or makes the call |
| **HMRC, as a source of error** | Its own records of payments, codes and authorisations [seen] | Reconcile HMRC's account against the firm's record every month; open a correction case on any difference. The firm does not wait for a client to notice |
| **HMRC, agent authorisation** | Online services; the client must act for each tax [seen] | The authorisation agent pre-fills everything and walks the owner through it in chat, then checks it took effect. Unfinished authorisation is tracked as an obligation with a date |
| **Companies House** | Software filing; identity verification; agent registration [seen] | Directly, within the firm's authorised status |
| **Banks** | Open-banking feeds; lender portals; relationship managers | Feeds read continuously; lender packs sent; negotiation with a person at the bank needs a person or the client |
| **Ledger platforms** | Interfaces; partner pricing; their own assistants [seen] | Connect to more than one; mirror data in the firm's own form. They are suppliers, gatekeepers and rivals at once |
| **Pension providers** | Interfaces [seen] | Directly; the provider's validation is a free consequence check |
| **Clients' employees** | Phone and email to the payroll bureau [seen, from practice] | The employee-query agent answers questions about their own payslip within the employer's scope. It never changes pay without the employer's instruction, and never discusses the employer's affairs |
| **Clients' own agents** | Emerging [conjecture for this segment] | A published interface: obligations, status, estimates, questions outstanding, service levels |
| **Buyers, lenders, insolvency practitioners, lawyers, executors** | People | Agents prepare data rooms, figures and estate summaries; people negotiate |
| **Sellers of practices** | People | Agents run due diligence on the book (3.18); people agree the deal |

### 2.5 Verifiers by case type

Step 1's three checks: rule (conformance), consequence (an outside party's test), outcome (was it right).

| Case type | Rule check | Consequence check | Outcome check | How fast it closes |
| --- | --- | --- | --- | --- |
| Ledger upkeep | Coding rules per client; duplicates; VAT codes | Bank balance agrees; supplier statements agree | Year-end adjustments needed later; client corrections | Hours (bank); month (statements) |
| Intake | Question well formed; one at a time; not already answered | Owner replies | Answer later corrected; year-end reconstruction needed | Days; year end |
| VAT return | Independent recomputation; prior-quarter variance; scheme rules | HMRC accepts; payment posts | HMRC query or assessment; later corrections | Days; outcome within four years |
| Payroll run | Thresholds, codes, statutory pay rules; variance against last run; payee details unchanged or verified | HMRC accepts; bank pays; pension provider accepts | Employee complaint; later correction | Hours to one pay cycle. Fastest outcome signal in the firm |
| Quarterly update | Ledger to update tie-out | HMRC accepts | Final declaration matches the sum of updates | Days; year end |
| Accounts | Tie-outs: ledger, bank, prior year; disclosure rules | Companies House accepts; directors approve | Restatement; lender or buyer challenge | Weeks; years |
| Corporation tax | Independent recomputation; flags (loans to participators, associated companies) | HMRC accepts | Enquiry inside the window; amendments | Weeks; a year or more |
| Self-assessment | Recompute; prior-year income sources present; HMRC data cross-check | HMRC accepts | Enquiry; HMRC's data matching finds missing income | Weeks; one to several years |
| Approval and payment | Request clear; amount and date shown | Client approves; tax paid | Penalties or interest for lateness; estimate error | Days to weeks. Fast, and fully observable |
| HMRC account | Firm's record vs HMRC's | HMRC corrects | Mismatch recurs or not | Weeks to months |
| Management information | Ties to ledger | Client reads and acts | Forecast error, scored monthly | One month |
| Advice | Cites rules; states assumptions | Client chooses | Stated predictions scored; regret; complaints | Months to years |
| Enquiries | Deadlines; evidence complete | HMRC's response | Settlement against the position taken | Months |

Three observations [reasoned]:
- **Payroll and management information close fastest on outcome**, so the engine learns fastest there.
- **Tax returns close fast on consequence but slowly on outcome.** HMRC accepts a wrong return [seen, inventory A B1]. Tax types earn autonomy on rule and consequence checks long before outcome evidence arrives.
- **The client-side case types are the best measured in the firm.** Reply time, approval time and late payment are observed within days. The engine can run many experiments on how to ask (wording, timing, channel, one question or five) and keep what works. Nobody in a traditional firm measures this [reasoned].

### 2.6 Authority envelopes and circuit breakers

**Envelopes** [reasoned; numbers illustrative]:
- **Filing:** only with a recorded client approval for that return, or a standing approval for that type and size.
- **Payment files:** prepared, never released by an agent. Net pay variance above a set bound (say 10% for any employee, 3% in total) blocks the run. Any new or changed payee bank account blocks the run until confirmed through a second, known channel.
- **Contact:** a cap on questions a week, tuned per owner. Employees may be contacted only about their own pay, through a channel the employer approved. No contact with a client's customers or bank without instruction.
- **Positions:** a confidence score below threshold, or a tax effect above a set sum, routes to the judgement desk.
- **Advice:** agents may explain rules, answer factual questions and run remuneration plans with stated assumptions. A recommendation with a stated effect above a set sum, or touching employment, insolvency, investment or a household in conflict, routes to a person.
- **Documents for third parties** (lender packs, income references): only from ledger data that agrees with bank evidence. A client-supplied document that does not agree goes to the reporting officer's queue, not back to the client with a question.
- **Collection:** agents may retry and remind. Stopping work goes to a person, under clause 11.
- **Reach:** a new playbook version serves at most 2% of affected clients in its first cycle, then 10%, then all, with a hold between steps.

**Circuit breakers** halt a case type when any of these leaves its baseline: filing rejections; maker and recomputer disagreeing; payroll variance blocks across many clients in one run; "this is wrong" replies; payee-change attempts; spend per case.

---

## 3. Walking the firm through events

For each event: what agents do, whether it works without a person, and if not, which kind of human need applies. The six kinds: **1 purpose**, **2 definition of good**, **3 answerability**, **4 capability gap**, **5 client demand**, **6 physical world**. Section 7 proposes a seventh: **people required by a counterparty's channel**.

### 3.1 Onboarding a new client with messy books
**Agents** map the household, run identity checks, get clearance from the prior accountant, rebuild the opening position and the director's loan account, find missed obligations, and walk the owner through HMRC agent authorisation for each tax.

**Without a person?** The mechanics, mostly yes [reasoned]. Four points break:
- **Authorisation stalls.** Many clients never complete it [seen, from practice]. The agent can make it easy, but it cannot press the owner's button. Unfinished authorisation is the commonest reason a new client's first deadline is at risk. The named person's first job is often a ten-minute call to get it done. **Kind 5.**
- A non-standard money-laundering risk is a legal decision for the reporting officer. **Kind 3.**
- Old errors, such as years of unreported VAT, raise a disclosure decision. Agents size it. Choosing how to approach HMRC, and persuading a frightened owner, is **kind 4 and kind 5**.
- The owner tells a person things they would not type (section 7.2). **Kind 5, disclosure demand.**

### 3.2 The monthly close
**Agents** code, reconcile, post journals, update tax estimates and the cash forecast, and score last month's forecast. The intake agent asks about each unexplained line within a day, one at a time, with its best guess.

**Without a person?** The production, yes [reasoned]. The bank balance is a hard consequence check. An evaluator governor audits a rotating sample, judged before seeing the agent's reasoning: **kind 2**, as audit. The limit is the owner's replies. Books are current only to the last answer. When an owner goes quiet for weeks, the named person calls. **Kind 5.**

### 3.3 A VAT quarter
**Agents** prepare the return; an independent recomputer on a different model rebuilds it; flags fire for partial exemption, reverse charge and property. The client approves in one tap. The return is filed.

**Without a person?** Yes for a standard trading business [reasoned]. Partial exemption and property stay with the judgement desk for now: **kind 4**, temporary. Registrations and scheme changes happen in HMRC web pages that must not be automated [seen, inventory A S10]. A person presses the button: a **counterparty's rule**.

### 3.4 A Making Tax Digital quarterly update
**Agents** summarise the ledger into HMRC's categories, tie out and submit, and show a running estimate of the year's tax.

**Without a person?** Yes [reasoned]. It is the purest routine case. Three facts shape the rollout [seen, gov.uk]:
- Clients join in three cohorts: income over £50,000 from April 2026, over £30,000 from April 2027, over £20,000 from April 2028.
- There are no penalties or penalty points for late quarterly updates in 2026–27. Penalties still apply to the year-end return and late payment.
- Each cohort needs authorisation for the new tax, so each April brings a wave of case type 20.

So early shadow data comes from a cohort with no penalty pressure, and later cohorts are smaller earners and less digital [reasoned]. Behaviour on late updates measured in 2026–27 will understate compliance once penalties start. The first-contact need is **kind 5**. The case type needs heavy shadow-running through 2028, not people in the loop for ever.

### 3.5 Year-end accounts and corporation tax
**Agents** treat year end as a thirteenth close plus judgement items. They prepare accounts and tax, recompute independently, and flag the director's loan account, associated companies, stock, work in progress, material accruals and going concern. Directors approve; agents file.

**Without a person?** For a simple company with good intake through the year, yes [reasoned]. Outside audit, nothing here needs a licensed signature [seen, inventory A]. What remains:
- **Kind 4, limited by the client, not the model.** The director's loan account is not a calculation. In most firms it is a reconstruction of what the owner meant by each personal payment, done after the event, often to fit the tax answer [seen, from practice]. Stock and work in progress in small firms are estimates. Agents model the effects well. They cannot know the facts.
- **What the design changes.** It moves the question to the day of the payment, when the owner remembers and before the tax effect is known (clause 4). For clients with a full year of intake, the reconstruction becomes a review of answers already given [reasoned]. For bought books and late joiners it does not. So this item shrinks only as fast as clients spend full years on the intake agent: slowly before 2030, faster after [conjecture].
- **Kind 3:** the tax bodies expect review of each tax deliverable [seen, inventory A S9]. The design meets this with an accountable officer who signs for the system and its audit sample (step 1, P6). Section 8 tests whether that holds.

### 3.6 An HMRC enquiry
**Agents** find the challenged judgement in the position registry with its original reasoning and the owner's dated statements, assemble evidence, draft the response and model exposure.

**Without a person?** No [reasoned]:
- **Kind 3:** the firm represents the client to an officer of the state.
- **Kind 4:** negotiating with a human inspector. About 150 a year, never enough to prove autonomy.
- **Kind 5:** the owner is frightened and wants a named person.

Dated intent records make enquiries cheaper to defend: the firm can show what the owner said at the time, not what was rebuilt later [reasoned]. Every result is written back as an outcome against the original position.

### 3.7 A payroll error that reaches staff
**Agents** compute the shortfall, prepare the correcting payment and submission, draft an explanation for the employer, answer affected employees' questions within the employer's scope, and log the cause.

**Without a person?** For a small error inside the envelope, yes [reasoned]. Then:
- Redress beyond the standard (an employee who paid overdraft charges) is **kind 3**.
- The employer, embarrassed in front of staff, often wants a person. **Kind 5.**

Most such errors are late or wrong inputs [seen, from practice]. The remedy is easier change notices confirmed before the run, not more review.

### 3.8 A client in a cash-flow crisis asks whether to make people redundant
**Agents** have probably flagged it weeks earlier. They model options (cost cuts, time to pay with HMRC, invoice finance, reduced hours, redundancy), compute redundancy costs, and flag when directors' duties may shift near insolvency.

**Without a person?** No, and mainly not for capability reasons [reasoned]:
- **Kind 5:** the owner's livelihood and their staff's.
- **Kind 3:** near insolvency, advice has legal consequences. The firm must know when to bring in an insolvency practitioner or employment lawyer.
- **Kind 4:** whether this business will recover is a rare, hard judgement.
- Time-to-pay is often agreed by phone with HMRC. A person makes the call.
- The firm's own fees are now at risk too (3.21). That is a conflict the person must handle openly.

### 3.9 A Budget changes a tax rule mid-year
**Agents:** the rule watcher reads the documents on the day and separates announced, drafted and enacted measures. It drafts playbook changes and new expected answers for the tests, scans every client for effect and date, re-forecasts, re-runs remuneration plans, and drafts messages ranked by effect.

**Without a person?** Mostly [reasoned]:
- **Kind 2:** changing what a correct return looks like is changing the tests. An evaluator governor approves the new expected answers. This is the clearest permanent human job in the firm.
- **Kind 4 and kind 3** where the rule is unclear or not yet law, and clients must be told what to do anyway.

Every affected client hears within days, with their own numbers.

### 3.10 A client wants advice on selling the business
**Agents** build a data room from clean books, model net proceeds under different structures and reliefs, and list what a buyer will find.

**Without a person?** No [reasoned]. Few cases, each different, outcomes years away (**kind 4**). Often the biggest decision of the owner's life (**kind 5**). The firm answers for its tax advice and must refer valuation, legal and investment questions (**kind 3**). Agents do everything but judgement and negotiation, so one expert handles many more sales than today.

### 3.11 A new model release
**Agents** run the suites and holdouts, shadow-run the model on live work without effect, compare error, cost and speed, and promote within reach limits.

**Without a person?** Yes at the current level of autonomy [reasoned]. Raising autonomy on the back of a release is **kind 2**. The verifier must not move to the same model as the maker at the same time, and tax types need longer shadow runs because their outcomes are slow (step 1, P9).

### 3.12 An error repeated across many clients
Say a playbook change applies a payroll threshold from the wrong date across 300 clients, or a misread Budget measure skews 1,200 tax estimates.

**Agents:** the circuit breaker trips and halts the case type. Reach limits turn "who is affected" into a list. Agents compute each effect and prepare corrections.

**Without a person?** Containment yes; resolution no [reasoned]: **kind 3** (someone answers to clients, HMRC, the insurer and the professional body), **kind 1** (redress beyond the constitution), **kind 2** (the tests failed to catch it). Restart, and at what level, is a human decision.

This is step 1's prediction that the decade's scandal will be a correlated error. Reach limits and independent verification matter more here than any other control.

### 3.13 January: returns ready, not approved, tax not paid
The return is ready on 10 January. The client approves on 30 January and pays nothing [seen, from practice]. Multiply by a few thousand.

**Agents** run approval and payment as its own case type:
- **Approve as you go.** Facts are confirmed through the year, so the year-end approval is of a figure the owner has watched for months, not a surprise [reasoned].
- **A tax pot.** The live estimate drives a suggested monthly set-aside into a separate account, under a standing arrangement the client approves. The client's bank moves the money, not the agent [conjecture: needs a bank partner].
- **Staged deadlines** set by the firm well before HMRC's, with reminders tuned per owner from reply history.
- Where the client cannot pay, agents prepare a time-to-pay case early, in December, not in February.

**Without a person?** For most clients, yes [reasoned]. For the owner who does not respond to any channel, the named person calls in the second week of January. **Kind 5.** The firm measures approval-to-deadline days and late-payment interest per client, so it knows whether this works.

### 3.14 HMRC misallocates a payment and issues a penalty notice
**Agents:** the HMRC-account reconciler finds that the client's payment sits against the wrong period or tax. It assembles the evidence (bank record, reference used, HMRC's statement) and drafts the correction request. It holds any action on the penalty and tells the client it is HMRC's error, with the evidence.

**Without a person?** Detection and preparation, yes. Correction mostly needs the HMRC desk: a phone call or a web form agents may not use [seen]. That is the **counterparty's channel**, not a capability gap. From practice, a third of a firm's HMRC desk time goes on HMRC's errors [seen]. The firm should count these and give the totals to HMRC. Volume data is the strongest case for interfaces (section 8).

### 3.15 A payroll email asks to change an employee's bank details
**Agents:** the fraud monitor sees a payee change two days before a run, sent by email from a lookalike domain. Clause 7 and the envelope block the run for that employee until the change is confirmed through a known channel (the employee's own verified contact, or the employer's portal). Agents warn the employer and log the attempt across all clients, because such attempts come in waves.

**Without a person?** Prevention, yes. Agents are better at this than busy people who see one email at a time [reasoned]. Where money has already gone, or a client is the victim of a fake HMRC call, the firm needs a person: reporting, the bank's fraud team, and an upset owner. **Kind 3 and kind 5.**

A related case: a client asks for a lender pack built from invoices that do not appear in the bank feed. The envelope refuses to issue it. The matter goes to the reporting officer, not back to the client as a question, to avoid tipping off. **Kind 3.**

### 3.16 A director dies, or a couple who are both clients divorce
**Agents:** the conflict detector picks up the event (a Companies House filing, a message, a change in bank patterns). Agents freeze filings that needed the director's approval, map who now has authority (executors, the remaining director), compute the estate's and the company's tax positions, and split the household record. In a divorce they flag that two people the firm acts for now have opposed interests.

**Without a person?** No [reasoned]:
- **Kind 5:** bereavement, and a family that now needs a person.
- **Kind 3:** who may instruct the firm is unclear, and confidentiality between former spouses is a duty. Clause 10 decides who the firm acts for. A person applies it.
- **Kind 4:** each case is different and rare.

At 4,000 households, events like these happen every week [reasoned]. They are not rare for the firm, only for each client. That is a steady load on the named people.

### 3.17 A client leaves for another firm
**Agents** assemble the handover: ledger export, the open positions and their challenge windows from the registry, payroll and pension records, authorisations to remove, final fees. They ask why the client is leaving and log the answer as an outcome.

**Without a person?** Yes in most cases [reasoned]. Fees owed or a records dispute (inventory A K6) goes to a person under clause 11. Churn reasons are scored: they are the outcome check on the named-person layer and on pricing.

### 3.18 The firm buys a practice of 800 clients
**Agents** ingest the books before completion. They map clients to segments, re-run the last two years' returns through the independent recomputer, find latent errors, check authorisations and diligence files, and plan migration by ledger platform and deadline.

**Without a person?** No [reasoned]:
- **Kind 1 and kind 4:** whether and at what price to buy, and how warranties cover errors found by the recomputer.
- **Kind 5:** clients trust the retiring partner. Introductions by that partner, in person, keep clients. The 5–15% who leave anyway [seen, from practice] are mostly those who were never introduced.
- **Kind 3:** the reporting officer re-diligences the book.

The design point: the recomputer turns due diligence from a sample of files into a full re-run, and puts a price on the book's hidden errors before signing [reasoned]. Migration is timed away from January.

### 3.19 A ledger vendor launches its own tax agent and changes interface prices
**Agents** measure the effect: which clients sit on that platform, what the new price does to cost, which of the firm's functions the vendor's agent now copies.

**Without a person?** No: this is **kind 1**, strategy. The vendors control interfaces, set prices and are building agents [seen]. That is landscape D's threat, and it starts in 2027, not 2035. The design answer is in the shared state: hold the client's ledger in the firm's own form, connect to more than one platform, and sell what the vendor's agent cannot (the named person, the guarantee, enquiry defence, judgement). Running on one platform at launch is sensible; depending on it is not.

### 3.20 HMRC announces a VAT inspection visit
**Agents** assemble the file: returns, reconciliations, records, positions taken, known weak points. They brief the owner in plain words.

**Without a person?** No. Someone from the firm attends or prepares the owner face to face. **Kind 6 and kind 3.** Rare, but real.

### 3.21 A client stops paying fees
**Agents:** fees are a monthly subscription by direct debit, so there is no year-end bill to argue about and little lock-up. (Inventory A cites a median lock-up of 105 days for practices [seen, inventory A S1].) A failed collection triggers retries and reminders, and checks whether the client is in distress (3.8).

**Without a person?** Mostly [reasoned]. Stopping work before a deadline is a **kind 1** policy applied by a person (clause 11). Where non-payment is a sign of crisis, it becomes 3.8.

### 3.22 The shoebox client and the in-person meeting
Some owners bring a box of paper once a year. Some want an annual meeting in a room [seen, from practice].

**Agents:** a post-and-scanning contractor digitises the box; the intake agent then works through the gaps. The annual meeting is prepared by agents: one page, the owner's numbers, the choices for next year.

**Without a person?** The meeting is **kind 5 and kind 6**. It is sold as part of a tier, not given to everyone. The shoebox is a pricing question: the firm charges for it, or declines the client.

### Summary of the walk

| Event | Without a person? | Kinds of human need |
| --- | --- | --- |
| Onboarding messy books | Mostly | 5 (authorisation, disclosure demand), 3 (non-standard risk), 4 and 5 (old errors) |
| Monthly close | Production yes; replies no | 2 by audit; 5 when the owner goes quiet |
| VAT quarter | Yes, standard cases | 4 (partial exemption, property); HMRC channel |
| Quarterly update | Yes | 5 at first contact |
| Year end and corporation tax | Yes for simple companies with good intake | 4 (facts, limited by the client), 3 (review duty) |
| HMRC enquiry | No | 3, 4, 5 |
| Payroll error | Yes if small | 3 (redress), 5 (embarrassed employer) |
| Cash-flow crisis and redundancy | No | 5, 3, 4 |
| Budget change | Mostly | 2, plus 3 and 4 where unclear |
| Sale of the business | No | 4, 5, 3 |
| Model release | Yes | 2 to raise autonomy |
| Correlated error | Contain yes, resolve no | 3, 1, 2 |
| January approval and payment | Mostly | 5 for owners who do not respond |
| HMRC's own error | Detect yes; correct no | HMRC channel |
| Payee fraud attempt | Prevent yes; aftermath no | 3, 5 |
| Death or divorce | No | 5, 3, 4 |
| Client leaves | Yes | 1 if fees or records are disputed |
| Buying a practice | No | 1, 4, 5, 3 |
| Vendor launches its own agent | No | 1 |
| VAT inspection visit | No | 6, 3 |
| Client stops paying | Mostly | 1 |
| Shoebox and in-person meeting | Partly | 5, 6 |

**Kind 6 is small but not zero.** Post, paper, inspection visits and owners who want a room. It remains the smallest kind in this service.

**Kind 5 is the largest by volume.** The first draft placed it mainly in crisis and advice. After review it sits in ordinary weeks too: authorisation, silent owners, January, bereavement.

---

## 4. The people

### 4.1 Human roles by kind

| Kind | Role in this firm | What they actually do |
| --- | --- | --- |
| **1. Purpose** | Owners and board | Constitution; risk appetite; prices of guarantees; redress beyond policy; capital; acquisitions; platform strategy |
| **2. Definition of good** | **Evaluator governors**, one per family of case types (bookkeeping and VAT; payroll; accounts and corporation tax; personal tax; advice and client side) | Own tests and thresholds; approve new expected answers after a Budget; audit samples; approve autonomy |
| **3. Answerability** | **Accountable officers**: a head of tax practice (registered adviser and agent of record), a reporting officer for money laundering, a person answerable to the professional body and insurer, **each with a named deputy** | Sign for the system, not each output; answer to HMRC, supervisors, insurers and clients. Deputies exist because a suspension or illness of one officer must not stop the firm acting for every client |
| **4. Capability gaps** | **Judgement desk**: enquiry specialists, VAT and property specialists, tax advisers for transactions; playbook authors | Take what agents cannot yet do; every decision recorded as a training case |
| **5. Client demand** | **Client managers**: a named person for every household, about one per 300 households at launch, widening as agents carry more contact. **Client partners** for growing companies, premium clients, crisis and life events | Client managers do no production. They know the household, make the calls agents cannot get answered, handle authorisation and January stragglers, and are the person an owner tells things to. Client partners handle the heavy cases |
| **6. Physical world** | A post-and-scanning contractor; attendance at inspection visits and in-person meetings, by client managers or partners | Mostly outside the firm |
| **7. Counterparty's channel** | **The HMRC desk** | Does what HMRC will not let agents do: web-only forms, phone calls, correcting HMRC's own errors |
| **Running the firm** | **Practice operations**: a practice manager, IT and security operations, collection exceptions | Small, because subscriptions and agents remove most credit control and scheduling |
| **Scaffolding** | Builders (engineers and experts), shadow reviewers, incident responders, **apprentices** | Temporary by design, except apprentices, who become the governors and officers of 2035 |

**Apprentices need a designed route.** Professional training needs logged practical experience across real work [seen]. With production gone, the firm designs it: apprentices act as shadow reviewers of the engine's output, rotate through the judgement desk and the HMRC desk, and shadow client managers. Their review decisions double as evaluation data, so the training pays for part of itself [reasoned].

### 4.2 Headcount sketch for about 5,000 clients and 4,000 households [conjecture]

| Role | 2027 (both landscapes) | 2030 A | 2030 B | 2035 A | 2035 B |
| --- | --- | --- | --- | --- | --- |
| Owners and board (part-time, some also officers) | 3 | 3 | 3 | 2 | 3 |
| Accountable officers and deputies | 3 | 3 | 3 | 3 | 3 |
| Evaluator governors | 5 | 5 | 6 | 3 | 5 |
| Judgement desk | 10 | 6 | 10 | 4 | 7 |
| Client managers (named person per household) | 13 | 10 | 12 | 8 | 11 |
| Client partners (growing, premium, crisis, life events) | 5 | 5 | 6 | 3 | 5 |
| Practice operations | 4 | 3 | 4 | 2 | 3 |
| Builders (engineers and experts) | 10 | 5 | 7 | 2 | 4 |
| Shadow reviewers (2027 includes seasonal cover) | 12 | 2 | 5 | 0 | 2 |
| HMRC desk | 5 | 3 | 4 | 1 | 3 |
| Incident responders (rota from the above, plus) | 1 | 1 | 1 | 0 | 1 |
| Apprentices | 4 | 4 | 4 | 3 | 4 |
| **Total** | **about 75** | **about 50** | **about 65** | **about 31** | **about 51** |

Why the figures moved from the first draft:
- **Shadow reviewers, 8 to 12.** Reviewing every filed tax output (about 6,000 VAT returns, 3,500 personal returns, 2,500 accounts with tax) is over 10,000 hours, mostly in December, January and around common year ends [reasoned, from the review]. Eight people cannot do that in the peak. The revised plan reviews every flagged output and every output for newly acquired clients, and a stratified random sample of about 40% of the rest, with seasonal cover in the first winter. The sample is enough for the measurement in 5.2: a few thousand reviewed cases a year per tax type.
- **Client managers, new: 13.** The 2,000 stable companies had no named person. From practice they will still phone, and many will leave if nobody knows them [seen]. One per 300 households at launch. The ratio is wider than a traditional client manager's (who also does production), and it widens further as agents carry more contact.
- **HMRC desk, 3 to 5 in 2027.** HMRC's own errors and authorisation friction add load.
- **Practice operations, new: 4.** A practice manager, IT and security, collection exceptions.
- **Accountable officers in 2035 A, 2 to 3.** Deputies are a requirement.

**The most uncertain line is client managers.** If owners in landscape A accept an agent as their first contact, and keep a person only for events, one per 800 households is plausible. That takes 2035 A to about 23 people. If owners insist on a person they know, one per 250 holds and 2035 A is about 35 [conjecture]. The design should measure this directly: churn and satisfaction by ratio, in controlled cohorts.

### 4.3 Against a traditional firm

Inventory A's model firm has 30 people for about 1,300 clients [model assumption]. Scaled, a traditional firm serving 5,000 such clients needs **about 110 to 120 people** [reasoned, simple scaling].

| | Traditional, 5,000 clients | Agent-first 2027 | Agent-first 2035 A | Agent-first 2035 B |
| --- | --- | --- | --- | --- |
| People | 110–120 | about 75 | about 31 | about 51 |
| Clients per person | 40–45 | about 67 | about 160 | about 100 |
| Share of people doing production | about 70% | about 25% (reviewers, HMRC desk) | under 5% | about 10% |
| Share in governance, judgement and relationship | about 15% | about 50% | about 75% | about 65% |

The shape changes more than the size. A traditional firm is a pyramid of production with judgement at the top. The agent firm is a senior group around an engine, a layer of named people facing households, and apprentices. The pyramid's middle, where trainees learned, has gone. The new middle is the client manager, and it may become the route into the profession (section 7.2).

---

## 5. 2027 against 2035: removing the scaffolding

### 5.1 What exists at launch

**Start narrow.** Launch with one segment, owner-managed companies plus the director's household, on one ledger platform, with the shared state platform-independent from day one [reasoned, adopting the review]. Add segments and platforms as bought books arrive.

**Run 2027 as measurement.** People review all flagged tax outputs and a stratified sample of the rest. Every reviewer catch and miss is recorded, along with the engine's. A human HMRC desk handles registrations, payment plans, codes, calls and HMRC's errors. People write playbooks; agents propose edits. Builders seed test suites from founding experts' graded cases, design-partner clients and bought books' history where terms allow (step 1, P8). Every household has a named person. The data goes to the insurer and the tax bodies within the first year, not after.

### 5.2 What evidence justifies removing a stage

With no errors in *n* cases, the error rate is below about 3/*n* with 95% confidence [reasoned; a standard result]. To show a rate below 0.5% needs about 600 clean cases. Below 0.1% needs about 3,000.

At 5,000 clients, that is a few months for VAT or payroll, one season for self-assessment, and never for enquiries. **Volume per case type sets the order in which people can leave** [reasoned].

### 5.3 The order, case type by case type [conjecture for timing; reasoned for order]

| Order | Case type | Scaffolding removed | Evidence that would justify it | Plausible date, A / B |
| --- | --- | --- | --- | --- |
| 1 | Intake questions; reminders; billing; approval and payment chasing | Human review of messages | Reply and complaint rates at or better than the human baseline over a season | 2027 / 2027 |
| 2 | Everyday factual questions ("can I claim my phone?", "when is my payment on account?") | Review of answers | Grounded answers agree with a governor panel on a few thousand questions; no rise in complaints | 2027 / 2027–28 |
| 3 | Ledger upkeep and monthly close | Review of every close; replaced by rotating sample | Sampled error rate below the human baseline over 3,000 client-months | 2027–28 / 2028 |
| 4 | Payroll runs, stable employers | Human approval of each run; variance and payee blocks stay | No error reaching staff over a few thousand runs; complaints below baseline. Payroll software is already near-autonomous for these [seen] | 2027–28 / 2028–29 |
| 5 | HMRC correspondence, drafting (nudge letters, simple queries) | Human drafting | Replies accepted by HMRC without follow-up at the human rate | 2027–28 / 2028 |
| 6 | Company secretarial | Review before filing | Registrar acceptance plus no later corrections over 1,000 filings | 2028 / 2028 |
| 7 | Remuneration planning, run for every company every year | Review of each plan | Plans recompute independently; stated savings realised; governors agree on a blind panel. It is arithmetic on known facts; the owner decides | 2028 / 2029 |
| 8 | Quarterly updates | Review of each update | Final declarations match summed updates with explained differences across a full year, measured on the 2027–28 cohort, after penalties start | 2028 / 2029 |
| 9 | VAT returns, standard | Review of each return | No material error in about 3,000 reviewed returns; no HMRC assessment on the cohort | 2028 / 2030 |
| 10 | Payroll, complex (construction scheme, statutory pay, benefits) | Approval of each run | As order 4, on the complex cohort | 2029 / 2031 |
| 11 | Corporation tax, simple companies | Review of each computation | Two seasons; amendments and enquiries no higher than for human work | 2029 / 2032 |
| 12 | Self-assessment, simple | Review of each return | Two seasons; HMRC data-matching finds no more missing income than for human work | 2029 / 2032 |
| 13 | Management information and forecasts | Human commentary | Forecast error at or below the human baseline for a year; owners rate it as useful | 2029 / 2031 |
| 14 | Accounts with judgement items | Review of flagged items | Agent decisions agree with governors on a blind panel at the rate governors agree with each other, **and** the client has a full year of dated intent | 2031 / later |
| 15 | Advice above a set effect | Review | Stated predictions scored over two years; complaint rate; blind panel | 2031 / later |
| 16 | HMRC correspondence, sending and calls | The HMRC desk | **Not evidence but a rule change**: HMRC interfaces or permission for agents (section 8) | Depends on HMRC |
| 17 | Enquiries; transactions; crisis; life events | Not removed | Volume too low to prove; demand for people likely to remain | Shrinks, does not go |

Each step is reversible. A failure moves the case type down a rung without blame (step 3, autonomy as a dial).

Two rules for the whole schedule [reasoned]:
- **Compare against measured human error, not against perfection.** No error rate is known today for any line of a practice [seen, inventory A]. The 2027 measurement is the first time anyone will know what human review catches.
- **Removing a reviewer is not the same as removing review.** Sampling, independent recomputation and outcome scoring stay.

---

## 6. Economics sketch

**Everything in this section is conjecture.** It is arithmetic on assumed numbers, to show the shape.

### 6.1 Today's benchmark

Weighting the segments by typical fees gives about **£1,700 a client** [reasoned, from the review; the first draft used £1,900]. At a margin of about 30% before partners' pay [seen, benchmark], a traditional firm of 5,000 clients earns about £8.5m and costs about £6.0m, almost all people. Clients usually pay their own ledger subscription.

### 6.2 Cost per client in the agent firm

| Cost line | 2027 | 2035 A | 2035 B |
| --- | --- | --- | --- |
| People (loaded cost) | 75 × £75k = £5.6m | 31 × £110k = £3.4m | 51 × £90k = £4.6m |
| Engine: software, tools, data, security | £1.2m | £0.8m | £1.0m |
| Model use and verification compute | £0.4m | £0.3m | £0.4m |
| Ledger platform subscriptions, bundled (about £150 a client after partner terms; retail is £150–£500 [seen]) | £0.75m | £0.5m | £0.7m |
| Insurance (including negligent-advice cover), guarantee reserve, compliance | £0.5m | £0.7m | £0.6m |
| Acquisition and migration (bought books amortised over about ten years; conversion costs; churn replacement) | £1.5m | £0.6m | £0.7m |
| **Total** | **about £10.0m** | **about £6.3m** | **about £8.0m** |
| **Cost per client** | **about £2,000** (£1,690 before acquisition) | **about £1,260** | **about £1,600** |

Notes [reasoned]:
- **The guarantee's real tail is negligent advice, not penalties.** Penalties are small. Claims over advice are covered by indemnity insurance, and the premium is the cost line.
- **2027 costs more than a traditional firm** once acquisition is counted. Scaffolding, a full engine and bought books arrive at once. It is an investment year.
- **The platform line is a strategic cost.** It falls if the firm holds its own ledger or vendors compete for its volume. It rises if one vendor holds the firm captive (3.19).

### 6.3 Prices and models

- **Subscription to a maintained condition**, collected monthly by direct debit, bundling the ledger platform. Illustrative annual prices: sole trader or landlord £500–800; stable company with the director's return £1,500–2,200; growing company with payroll and monthly information £4,000–8,000. Monthly collection removes most lock-up.
- **What the price is for.** The live tax estimate and the named person, not the filing [reasoned, adopting the review]. Filing is what loses value first in landscapes A and D.
- **Estimate guarantee:** credit if the final bill differs from the estimate by more than a stated margin for a reason the firm could have known [conjecture]. Priced from the firm's own estimate-error data. The penalty guarantee is included but not marketed.
- **Premium tier** (£2,000–5,000 extra): a client partner, crisis support, in-person meetings.
- **Projects:** sales, restructuring, enquiry defence, estates. The judgement desk's revenue.
- **Shoebox and clean-up:** charged separately.

### 6.4 The case, and margin under three landscapes

**Lead with capacity, not margin** [reasoned, adopting the review]. Firms are short of people, not clients (inventory A). A traditional firm that wants 3,000 more clients needs about 70 more people it cannot hire. The agent firm needs about a dozen more: client managers, two judgement-desk seats, an HMRC-desk seat. On the 2035 A figures, 8,000 clients cost about £7.9m against revenue of about £13.2m, a margin near 40% [conjecture, arithmetic]. The agent firm's advantage is in its marginal cost per client, not its average.

At 5,000 clients:

| | Traditional firm | Agent firm 2027 | Agent firm, landscape A 2035 | Agent firm, landscape B 2035 | Agent firm, landscape D (price collapse) |
| --- | --- | --- | --- | --- | --- |
| Revenue per client (agent firm includes bundled platform) | £1,700 | £1,850 | £1,650 (filing prices fall; estimate, named person and projects hold) | £1,950 | £600 routine + £500 named person, estimate and accountable layer = £1,100 |
| Cost per client | £1,190 | £2,000 (£1,690 before acquisition) | £1,260 | £1,600 | about £900 |
| Margin | about 30% | about −8% (about +9% before acquisition) | about 24% | about 18% | about 18%, only if the accountable layer sells |
| What the traditional firm's margin does | — | — | Falls sharply as clients compare | Holds; growth capped by hiring | Collapses: routine work was its revenue |

Four points [reasoned, on the conjectured numbers]:
- **At equal size, the agent firm does not beat a good traditional firm's margin in any landscape.** The first draft showed 40% in landscape A. Counting named people, platforms, acquisition and practice operations removes that. The design should not be sold to owners on margin at fixed size.
- **It wins on growth, survival and resilience.** It can add clients cheaply in every landscape. It keeps a margin in A and D where the traditional firm's collapses.
- **In landscape B it is the weaker business at fixed size.** Its case there is capacity and the option on A and D.
- **In landscape D routine compliance is worth little.** Banks, ledger vendors and clients' own agents offer it near cost [conjecture], and the vendor threat starts in 2027. The firm survives on what stays scarce: the named person, the estimate, the guarantee, enquiry defence, crisis and transaction advice, and being the agent HMRC deals with. Price that layer separately from day one.

---

## 7. What this example shows that the general design missed

### 7.1 Where agent-first holds better than expected

1. **Answerability is thinner in law than assumed.** Outside audit, nothing is reserved to a licensed signatory. Directors sign their own accounts; the taxpayer is responsible for their return; anyone may call themselves an accountant [seen, inventory A]. Kind 3 rests mostly on professional guidance and insurance [reasoned].
2. **The physical world is small.** Kind 6 is the smallest kind here: post, paper, inspection visits, owners who want a room.
3. **The statutory calendar is a gift to agents.** Peaks force traditional firms to overstaff. Agents absorb peaks at little extra cost [reasoned].
4. **Counterparties already speak software**, so free consequence checks are plentiful.
5. **The rule watcher is a big lever.** Every affected client hears within days of a Budget, with their own numbers.
6. **Volume per case type is high enough to prove autonomy** in most case types within a few years. Payroll, everyday questions and remuneration planning can move faster than the first draft said.
7. **The client side is the best-measured work in the firm.** Reply time, approval time and late payment close in days. The engine can learn how to ask, which no traditional firm measures [reasoned].
8. **Agents are better than people at fraud prevention.** They see every payee change across every client at once [reasoned].

### 7.2 Where the human layer has to be larger

1. **The client is the bottleneck, not production.** The general design treated missing inputs as an intake problem and approval as a formality. Here, owners' attention limits the whole service: books are current only to the last answer, and January is lost at approval and payment. The intake agent is the core product, and approval and payment is a case type [reasoned, adopting the review].
2. **Disclosure demand.** Owners tell a person things they would not type. That is a variant of kind 5 the general design missed.
3. **A named person for everyone, not only a premium tier.** The general design sold kind 5 as a tier. Here, a cheap named person for every household is needed to get authorisation done, reach silent owners and keep clients after an acquisition. The tier sits on top [reasoned].
4. **The household is the unit, and households break.** Death, divorce and disputes are weekly events at this size. They create conflicts of interest an entity-based design does not see. The general design needs a conflict rule in every constitution where the client is more than one person.
5. **Distress is frequent.** A firm that forecasts well sees more crises earlier, so it needs more crisis people, not fewer [reasoned].
6. **A counterparty's channel creates a seventh kind of human need.** The HMRC desk exists because HMRC forbids automating its web pages [seen], and a third of its work is HMRC's own errors [seen, from practice]. The general design should add: **people required by a counterparty's channel or a counterparty's errors**. Its removal is outside the firm's control.
7. **Outcome checks for tax are slow and mostly absences**, lagging autonomy by four to six years [reasoned].
8. **The training route breaks hardest here.** Trainees learned on the lines that go first. The firm must fund apprentices without production and design their logged experience.

### 7.3 Structural findings

1. **The valuable output is a maintained condition plus scored predictions**, not a set of filings. A firm whose estimates and forecasts are scored can show a track record of judgement [conjecture: the asset that sells the accountable layer in landscape D].
2. **Timing of facts is a design variable.** Asking about a payment on the day it happens, before its tax effect is known, makes year-end judgement smaller and enquiries easier to defend. The general design treated judgement items as a capability gap. Here, part of the gap is when the question is asked [reasoned].
3. **The platform is a counterparty, supplier and rival at once.** The general design treated tools as inputs. Here, the firm's state must not live only inside a vendor's product.
4. **The economics favour growth, not size.** At fixed size the agent firm's margin is no better than a good traditional firm's. Its advantage is marginal cost per extra client, which matters most when the market is short of people.

---

## 8. Stress test: rules, insurance and institutions, applied now

| Fact | Effect on the design |
| --- | --- |
| **HMRC forbids automating its web pages and sign-in; its interfaces are allowed** [seen, inventory A S10] | Keeps the HMRC desk. Route all that is possible through interfaces; batch the rest; count HMRC's errors and press for interfaces with volume data |
| **Agent authorisation is per client, per tax, and needs the client to act** [seen] | Confirms case type 20 and the named person's role in onboarding. Each Making Tax Digital cohort brings a new wave |
| **Making Tax Digital for income tax arrives in three cohorts (2026, 2027, 2028); no penalties for late quarterly updates in 2026–27** [seen, gov.uk] | Volumes step up. Shadow data from 2026–27 understates later compliance; evidence for order 8 is taken from the 2027–28 cohort |
| **Mandatory registration of tax advisers with HMRC**, phased in from 2026 to early 2027, with minimum standards and suspension for failure [seen, gov.uk] | Needs a registered, answerable adviser. A suspension would stop the firm acting for every client at once, so that officer has a deputy and a clean record from day one |
| **The tax bodies' AI guidance (January 2026):** members answer for work "irrespective of the use of AI tools", should treat AI output like a junior's, and ensure submissions can be reviewed [seen, inventory A S9] | Read strictly, it means review of every tax deliverable, which blocks section 5 from order 9 onwards. Keep every output reviewable; argue that sampling plus independent recomputation is appropriate review, using 2027's measured data; if the bodies disagree, tax headcount stays near landscape B |
| **Indemnity insurance:** institute minimums (£2m where fees exceed £800,000); no AI carve-out; insurers starting to ask whether a person reviews important work [seen, inventory A S8, S11] | The guarantee and negligent-advice cover need an insurer that prices sampled review. Offer the error data and a pilot cohort. Failing that, keep guarantees small |
| **Money-laundering duties sit with a named reporting officer; Companies House identity verification and authorised-agent status** [seen, inventory A S15, S16] | Confirms permanent kind 3 roles. Suspicious lender-pack requests go to the officer, not back to the client |
| **Audit, investment and pensions advice, and insolvency appointments are reserved** [seen] | Constitution clause 8; a hard edge in the advice envelope and a referral network |
| **Directors sign their own accounts; taxpayers are responsible for their returns; "accountant" is not protected** [seen, inventory A] | Client approval is a legal step, so approval design matters. Barriers to entry are low: in landscape D rivals include banks and ledger vendors, from 2027 |
| **Confidentiality and data protection**; client data in public AI tools without consent is likely a breach [seen, inventory A S9] | Engagement terms cover AI processing and anonymised outcome use; model contracts exclude training on client data. Employee-query and divorce cases need strict separation of whose data is shown to whom |
| **Professional rules on handover and records when clients leave** [seen as practice, inventory A K6] | Clause 11: no holding records hostage. The position registry extract goes with the client |
| **HMRC's enquiry and discovery windows** run from about a year to many years after filing [reasoned, general knowledge; not checked in this run] | The position registry and intent records are kept for the full window. The guarantee is long-tail |

**What the stress test changes:**
1. **Not the architecture.** Shared state, separated verification, envelopes and reach limits survive.
2. **It slows section 5 for tax case types.** Professional-body expectations and insurers, not capability, are the binding limit on removing review. Ledger, payroll, company secretarial, questions and remuneration planning are less affected.
3. **It confirms the seventh kind:** the HMRC desk, held in place by a counterparty's rule and a counterparty's errors.
4. **It makes the accountable officers central and fragile.** Deputies and a training route are requirements.
5. **It argues for step 3's "firm that writes the standard".** The firm with real error data on sampled review is best placed to persuade the bodies and insurers.

**Where this is weakest.** Every figure is a model figure. The sampling-versus-review question decides tax headcount from 2030. The client-manager ratio decides total headcount more than any other line, and nobody yet knows what owners will accept from an agent.

---

## 9. Review and response

The reviewer is a managing partner writing from practice. Most points were right and are adopted. Where I kept my version, the reason is given.

| # | Reviewer point | What I did |
| --- | --- | --- |
| 1 | The design automates the easy part (production) and under-designs the hard part (getting facts, approval, payment) | **Adopted.** The client side is now the centre: intake agent as core product (2.3), approval and payment as case type 19 (3.13), section 7.2 point 1. I keep production automation as necessary, because it is what makes the live estimate possible and frees people for the client side |
| 2 | "Books reconciled within two days" is really "current to the last thing you told us" | **Adopted.** Promise reworded (1.2) |
| 3 | Director's loan account and stock are facts held by the client; "shrinking" is doubtful by 2030 | **Partly adopted.** Agreed the limit is the client, not the model, and that little shrinks by 2030 for bought books. Kept "shrinks", for a reason the reviewer did not consider: asking about each payment when it happens, before the tax effect is known, turns reconstruction into review (clause 4; 3.5; 7.3 point 2). It shrinks as fast as clients spend full years on the intake agent |
| 4 | Approval is where January goes wrong | **Adopted and pushed further**: approve as you go, a tax pot under a standing arrangement, staged deadlines, early time-to-pay (3.13) |
| 5 | Payroll too cautious; remove approval of standard runs in 2027–28 | **Adopted** for stable employers (order 4). Complex payroll stays later (order 10) because statutory pay and the construction scheme carry more fact risk |
| 6 | Everyday questions can be answered today | **Adopted** for factual questions (order 2, from 2027). Kept one measurement season, because a confident wrong answer about a deadline repeats across thousands of clients |
| 7 | Nudge letters and simple correspondence can be drafted now | **Adopted** (order 5). Sending and calls stay with the HMRC desk |
| 8 | Remuneration planning is arithmetic and should run every year unprompted | **Adopted** (case type 16, order 7, 2028 / 2029) |
| 9 | The penalty guarantee is not a differentiator; the live estimate is | **Adopted** that it is hygiene. **Pushed further**: proposed an estimate guarantee instead (1.2, 6.3) |
| 10 | HMRC as a source of error | **Adopted.** HMRC-account reconciler, event 3.14, and the seventh kind widened to include a counterparty's errors |
| 11 | Authorisation friction | **Adopted.** Case type 20; 3.1; stress test row |
| 12 | Fee collection and lock-up | **Adopted.** Case type 21; event 3.21. Monthly direct debit removes most lock-up, so practice operations stay small |
| 13 | Fraud and impersonation | **Adopted.** Fraud monitor, payee-change rule in clause 7 and the envelope, lender-pack rule, event 3.15 |
| 14 | Life events and disagreeing household members | **Adopted.** Case type 22, clause 10 on conflicts, event 3.16, 7.2 point 4 |
| 15 | Employees as contacts need a rule, not a ban | **Adopted.** Employee-query agent within the employer's scope (2.3, 2.4, 2.6) |
| 16 | Leavers and handover | **Adopted.** Case type 23, clause 11, event 3.17 |
| 17 | Software vendors as counterparties and rivals; landscape D starts in 2027 | **Adopted.** Platform-independent ledger mirror, multiple connectors, event 3.19, cost line, 7.3 point 3 |
| 18 | Physical world understated | **Adopted in part.** Inspection visits and in-person meetings added (3.20, 3.22). Kind 6 remains the smallest kind; the conclusion holds |
| 19 | MTD timing: three cohorts; no late-update penalties in 2026–27 | **Adopted and checked** against gov.uk. Volumes, 3.4, order 8 and the stress test corrected |
| 20 | Eight shadow reviewers cannot cover the 2027 peak | **Adopted.** Stratified sample plus all flagged outputs from day one; 12 reviewers with seasonal cover |
| 21 | Add client managers at one per 250–300 households | **Adopted the role for every household.** Kept a slightly wider ratio (one per 300 at launch, widening to about one per 500 by 2035 A), because these people do no production and agents carry routine contact. Flagged it as the most uncertain line and proposed measuring it in cohorts |
| 22 | Add practice manager, credit control, IT | **Adopted** as practice operations, smaller than a traditional back office for the reason in point 12 |
| 23 | 2035 A at 20 leaves no slack; do not plan below 30 | **Largely adopted**: the revised figure is about 31, with deputies for officers. Kept the view that 20s are possible if owners accept agent-first contact, shown as a sensitivity (4.2), not as the plan |
| 24 | Apprentices need logged experience across real work | **Adopted.** Designed route: reviewers of the engine, rotations on the judgement and HMRC desks, shadowing client managers (4.1) |
| 25 | Baseline nearer £1,700 a client | **Adopted** (6.1) |
| 26 | Acquisition at around one times fees, conversion costs, 5–15% churn | **Adopted.** Cost line, event 3.18, case type 24 |
| 27 | Ledger platform cost of £150–£500 a client | **Adopted** as a bundled cost recovered in price |
| 28 | Guarantee tail is negligent advice, not penalties | **Adopted** in the insurance line |
| 29 | Lead with capacity, not margin | **Adopted and strengthened.** The revised numbers show the agent firm does not beat a good traditional firm's margin at fixed size in any landscape. Its case is marginal cost, growth and survival (6.4) |
| 30 | Start with one segment on one platform | **Adopted for launch** (5.1). Not adopted as a long-term dependence, because of point 17: the state must be platform-independent from day one |
| 31 | Run 2027 as measurement and take data to insurers and the tax bodies early | **Already in the draft; strengthened** with a deadline of the first year (5.1) |
| 32 | Price the live estimate and the named person, not the filing | **Adopted** (6.3), alongside a separately priced accountable layer for landscape D |
