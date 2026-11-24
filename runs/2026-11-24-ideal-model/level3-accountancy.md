# Level 3: accountancy, tax and finance for small UK businesses, redesigned from scratch

Draft by Claude, 24 November 2026. Revised the same day after two reviews: a platform builder pushing it further and a practitioner testing it against practice (section 11). It follows the six-step procedure in step 3c, the kinds of human need in step 3b and the engine in step 1, and sets itself against the level 1 worked example (`example-accountancy.md`). Labels: **[seen]** exists somewhere today, with its source; **[reasoned]** follows from logic; **[conjecture]** plausible towards 2035. Every volume, price and headcount is a model figure for argument. Today's rules are treated as facts to design around and applied as a stress test in section 10.

---

## The answer in brief

1. **Accountancy exists because of a gap.** Economic events happen in one place and time. They are turned into numbers, tax and decisions somewhere else, months later. Most of today's work is the cost of crossing that gap: collecting, re-keying, chasing, reconciling, preparing for deadlines [reasoned].
2. **Close the gap at the point where meaning is born, not where money moves.** A bank payment carries an amount and a name. Its meaning (VAT, category, purpose, counterparty) is born earlier, when the invoice, quote, payslip or rent demand is made. If the service issues those, nothing needs classifying. The bank feed becomes the check, not the backbone [reasoned].
3. **Then the work does not get cheaper. It stops existing.** Tax is a function of structured transactions, a few facts and a few choices. So tax can be known continuously, and moved out of reach as it arises. Filing becomes a confirmation of a position the owner has watched all year [reasoned].
4. **The product is a set of continuous conditions:** I know where I stand; my tax has already left; my bills and invoices run themselves; I hear before a big decision, not after it; my record is trusted by lenders and HMRC. The firm sells those conditions, plus a person who answers for them.
5. **The boundary: own the record, the network and the accountability; rent the rails.** One ledger, owned, with an open data model, which is the client's canonical record. Invoicing, bill-pay and request-to-pay built on it, so data is born structured. A network across many businesses, so one owner's knowledge becomes everyone's default. Payment rails, banking and filing channels are rented [reasoned].
6. **Two entities, not one.** A platform company runs the ledger, rails and network, and is offered to other accountancy firms. The firm sells the accountable layer and is the platform's reference customer. The firm gets scale it could not reach alone; the platform gets a customer that proves it [reasoned].
7. **The organisation** is a governing core, a judgement desk, pooled partners for sole traders, named partners for companies, embedded finance leads for growing companies, and a deliberate training route. At 5,000 clients the firm's core is about 34 people in 2035 in landscape A and 48 in B, close to level 1's 31 and 51. Total headcount is higher, about 63 and 78, because the firm sells a finance function [conjecture].
8. **Profit leaves filing,** which will be near free by the early 2030s. It sits in the finance function for growing companies, priced against a part-time finance director; in certainty, priced from the firm's own error data from year one; and, on the platform side, in a record the economy trusts [conjecture, following step 1, P3].
9. **The design is built for owners as they are.** They raid visible tax pots in bad months, ignore prompts after a quarter, think in stories rather than policies, and phone about everything. So tax leaves the account rather than sitting in it, questions are rationed by value, and the paperwork of ordinary life is part of the service [reasoned, from the practitioner review].
10. **The wedge is the forced moment.** Making Tax Digital brings sole traders and landlords over £30,000 in from April 2027 and over £20,000 from April 2028 [seen, gov.uk]. Mandatory VAT e-invoicing starts in April 2029 [seen, government announcement]. Each forces owners to change how they keep records. That is when they will accept a different service.

---

## 1. The client's outcome, segment by segment

The outcome: the owner always knows where they stand, is never surprised by tax or cash, pays the right tax with no effort, makes good decisions at the moments that matter, can prove their position to anyone in minutes, and spends no time on bookkeeping.

Each of these is a condition, not a deliverable. It is either true right now or not. So the first design choice is that **the firm sells states of the world, maintained continuously**, not outputs delivered on dates [reasoned].

The same 5,000 clients as the level 1 example, for comparison [conjecture: the mix]:

| Segment | Clients | What they want to be continuously true | What they least want to do |
| --- | --- | --- | --- |
| **Sole traders and partnerships** | 1,000 | "The money in my account is mine to spend. Tax is already gone." "I get paid on time." | Keep records. Think about tax |
| **Landlords** | 1,000 | "I know what each property really earns after tax and finance costs." "Selling or incorporating will not surprise me." | Collect letting-agent statements. Work out what is allowable |
| **Owner-managed companies, stable** (1–10 staff) | 2,000, plus 500 linked personal returns | "I know what I can safely take out, and how." "Payroll and VAT just happen." "Company and household are planned together." | Answer questions about old transactions. Approve what they do not understand |
| **Growing companies** (10–50 staff) | 500 | "I have a finance function I could show an investor tomorrow." "I know my runway and act before it bites." | Hire a finance director they cannot afford or find |

Four points follow [reasoned]. **The real client is a household with a business attached**, which matters more now the firm acts on money. **Segments differ by decision value, not compliance volume**: a sole trader wants tax to vanish, a growing company wants a finance function; these are different products. **No segment wants an accountant.** They want the conditions; an accountant was the only way to get them while information was in the wrong place. **But every segment wants someone to ring.** Owners ring their accountant about mortgage references, SA302s, student finance, child benefit, grant forms and council letters [seen, practitioner review]. That demand is real, builds trust, and is part of the outcome, not noise around it.

---

## 2. Where information is born and decisions are taken

### 2.1 Information

| Information | Where it is born | Where today's firm meets it | By 2035 |
| --- | --- | --- | --- |
| **What a sale or purchase is** (VAT, category, counterparty, purpose) | The invoice, quote, order, payslip or rent demand, when it is made | Photos, PDFs, forwarded emails, or guessed from a bank line | Born structured on the platform's own invoicing, bill-pay and payroll, or received as a structured e-invoice [reasoned]. Italy has cleared B2B invoices centrally since 2019 [seen, Agenzia delle Entrate, via builder review]. UK VAT e-invoicing from April 2029 over Peppol [seen, government announcement; adviser summaries] |
| **Money in and out** | The bank account and card, at payment | Weeks later, via feeds or statements | Read as it happens, as a **check** that the structured record is complete, and as the fallback for what escaped structure [seen: open banking feeds today; reasoned: the role] |
| **What an unstructured payment was for** | The owner's head, at payment | At year end, reconstructed, often to fit the tax answer [seen, level 1 example 3.5] | Covered by a network default or the owner's policy; the rest asked, rarely, ranked by tax value [reasoned] |
| **How others classify the same counterparty** | Thousands of other businesses paying the same supplier | Nowhere: each firm and each client codes it again | Shared, aggregated and anonymised across the network, so a new client inherits it [reasoned] |
| **Rent and property costs** | The tenant's payment; the letting agent's system | An annual statement, late and messy [seen, practitioner review] | Read from the letting platform and rent account, through partnerships [reasoned; lettings roll-ups already run these systems, step 3c] |
| **The owner's intentions and appetite** | The owner | A meeting once a year | Written once as standing policies, starting from network priors, revised when life changes [reasoned] |

### 2.2 Decisions

The decisions that matter are few and predictable: extraction, hiring, buying, borrowing, VAT registration, incorporation, pricing, selling, raising money, closing.

Today the accountant learns of most of them after they are taken, when they appear in the books [seen, from practice in the level 1 review]. **The redesign puts the firm at the moment before the decision**, where its knowledge is worth most [reasoned]. Where the firm issues the quote or the purchase order, it is there by construction.

### 2.3 The design rule

Put the firm's capability at four points: **at the birth of the transaction**, where meaning is created; **in the money flow**, where completeness is checked; **in the owner's channel**, where intentions are spoken; **at the decision moment**, where advice has value. Everything else today's firm does exists because it was not at those points [reasoned].

---

## 3. What disappears, and why

### 3.1 The mechanisms

Step 3c deletes tasks caused by distance and waits caused by how authority and money are arranged. Here there are eight mechanisms [reasoned]:

| Mechanism | What it replaces | Why it works |
| --- | --- | --- |
| **Structure at birth** | Coding, bookkeeping, most questions | An invoice issued or received on the platform carries its VAT, category and counterparty. There is nothing to classify later |
| **One record, checked against the bank** | Reconciliation | There is one ledger. The bank feed confirms it; a gap is an exception, not a routine. Reconciliation was the cost of keeping two records |
| **Network defaults** | Most of the owner's coding decisions | When thousands of businesses class a supplier one way, a new client starts there and only confirms [reasoned] |
| **Standing policies** | Repeating questions | "Builders' merchant payments are materials. Anything to my sister's company is a loan." One answer covers hundreds of transactions. Expect 60–80% removal, not 90% (7.5) |
| **Ask rarely, by value, with safe defaults** | Year-end reconstruction | A small monthly budget of questions, ranked by tax at stake. Unanswered items fall to the treatment safest for the owner in an enquiry, which usually costs a little tax. Prompts decay within a quarter, so the design does not depend on them [seen, practitioner review: decay] |
| **Tax leaves as it arises** | January; payment chasing; the raided pot | Tax is moved out of the owner's reach, not just set aside: paid forward to HMRC where HMRC accepts it, otherwise held in a notice pot. Later, split at the payment rail (4.2) |
| **Confirm the year, not each form** | Approval of each return as a project | The owner approves a method once and confirms the year's position once. Returns are derived from it. Where law needs a declaration, that one sitting gives it |
| **Structured exchange** | Correspondence; misallocations; nudge letters | The firm makes the payments, with correct references. Data sent to HMRC matches what HMRC holds |

**Bookkeeping disappears as a job** because nobody keeps books. The books are the transactions as they were born, checked against the bank. **Year end disappears as a project** because the ledger is never open. **January disappears as a peak** because there is no stock of unpaid, unapproved tax waiting for it. The practitioner review confirms the cause: bank feeds cut bookkeeping hours, but January stayed because the tax stock still built up [seen, practitioner review].

### 3.2 Today's work, line by line

The level 1 example grouped today's work into 24 case types; the practitioner review adds a 25th. "Side effect" means the output still exists but nobody, human or agent, does it as a task.

| # | Level 1 case type | Fate at level 3 | Why | Who or what does what remains |
| --- | --- | --- | --- | --- |
| 1 | Ledger upkeep | **Disappears** | Structured at birth; one record; bank as check | Ledger; anomaly agent |
| 2 | Intake: questions to the owner | **Mostly disappears**: about 150,000 a year falls to 25,000–45,000 [conjecture] | Structure, network defaults and policies answer most; the rest rationed by value | Client's finance agent |
| 3 | VAT return | **Side effect** | VAT on each structured invoice; e-invoices from 2029 | Tax engine; recomputer; the year's confirmation |
| 4 | Payroll run | **Side effect for the routine; exceptions remain** | Pay follows contracts and time data. Starters, leavers, statutory sick and parental pay, attachment orders, auto-enrolment and the sudden bonus do not [seen, practitioner review] | Payroll engine; payroll exceptions on the judgement desk |
| 5 | MTD quarterly update | **Side effect** | A summary of an always-current ledger | Tax engine |
| 6 | Year-end accounts | **Side effect, plus a residue of judgement** | Extract from a closed ledger; stock, work in progress, accruals, and the lease and revenue judgements in FRS 102 from 2026 remain [seen, general knowledge, via practitioner review] | Tax engine; judgement desk; director confirms |
| 7 | Corporation tax | **Side effect** | Liability computed and paid forward monthly | Tax engine; recomputer |
| 8 | Self-assessment | **Side effect** | Business figures live; HMRC pre-fill for the rest; tax already paid forward | Tax engine; household agent |
| 9 | Company secretarial | **Side effect** | Events come from the share register, payroll and identity records | Secretarial agent |
| 10 | Onboarding and due diligence | **Remains, shrunk** | Digital identity and bank data do most | Onboarding agent; reporting officer for non-standard risk |
| 11 | Payroll year end and benefits | **Disappears** | Real-time submission; payrolled benefits | Payroll engine |
| 12 | Clean-up of messy books | **Remains, at the door only** | Once per arriving client | Migration agent; judgement desk for disclosure |
| 13 | Year-end judgement items | **Mostly moves to the moment** | The director's loan account becomes a running record; accruals become policies | Policy engine; residue to the judgement desk |
| 14 | HMRC correspondence | **Shrinks sharply** | No misallocated payments; fewer mismatches; later, trusted status | HMRC desk for HMRC's own errors |
| 15 | Management information and forecasts | **Becomes a condition** | Position always live; forecasts daily and scored | Forecast agent; embedded lead with the owner |
| 16 | Everyday questions and remuneration planning | **Transformed** | Answers at once; extraction a running optimisation under policy | Finance agent; partner above a set effect |
| 17 | Enquiries, R&D and loss claims | **Remains; cheaper to defend** | Structured records and dated positions are the defence. HMRC tests substance, not timestamps, so the record helps but does not decide [reasoned, from practitioner review] | Judgement desk; accountable officer |
| 18 | Decisions beyond tax (sale, raise, distress) | **Remains and grows** | The firm sees them coming, so joins more of them, earlier | Named partner or embedded lead; judgement desk |
| 19 | Approval and payment | **Disappears** | Method and year confirmed once; tax leaves as it arises | Mandate agent; partner for owners who refuse a mandate |
| 20 | Agent authorisation | **Remains** (HMRC rule), once at the door | The client must act for each tax [seen] | Onboarding agent; partner calls if stuck |
| 21 | Billing and collection | **Side effect** | Subscription collected under the same mandate | Operations agent |
| 22 | Life events and household splits | **Remains** | People, conflict and grief | Named partner or pooled team; judgement desk; officer |
| 23 | Leavers and handover | **Shrinks** | The client owns a portable record in an open format | Operations agent |
| 24 | Acquisition and migration of books | **Remains, as one growth engine** | Bought clients arrive at level 1 | Migration agent; owners; partners for introductions |
| 25 | **Everyday household paperwork** (mortgage references, SA302s and tax year overviews, student finance, child benefit, grant forms, council letters) [new, from practitioner review] | **Mostly a side effect of the verified record** | A lender or agency reads a certified view with consent; overviews come from HMRC data the firm already holds | Finance agent; pooled team or partner for the odd ones |
| — | Fraud control | **Grows** | The firm now initiates payments, so it is in the fraud chain | Fraud monitor; payee rules (7.1) |
| — | HMRC account reconciliation | **Shrinks** | The firm made the payments | Reconciliation agent |

**The count.** Of 25 case types, nine disappear or become pure side effects; three become side effects with a human residue (payroll, accounts, paperwork); six remain but shrink; two are transformed into conditions or live answers (management information, everyday questions); five remain mostly human: enquiries, decisions beyond tax, life events, acquisition, and authorisation (by HMRC's rule). One, decisions beyond tax, grows [reasoned].

**What changed from level 1.** The level 1 example spent most of its design on getting facts from owners and getting them to approve and pay (case types 2 and 19). At level 3 both mostly vanish. The bottleneck was not solved. It was designed out, mainly by moving the firm to where transactions are made.

---

## 4. What appears that did not exist before

### 4.1 New continuous conditions

| Condition | What the owner sees | What makes it true |
| --- | --- | --- |
| **"Safe to spend"** | One number: balance, minus tax owed and not yet paid forward, minus committed bills, minus the owner's chosen buffer | Structured record; continuous tax; known payables |
| **"Tax already gone"** | Tax paid forward to HMRC, or in a notice pot, against the live liability, for every tax | Sweeps on each receipt; scheduled payments forward. True in bad months as well as good, because the money is out of easy reach [reasoned, from practitioner review] |
| **"Books closed today"** | No open item older than a day | Structure at birth; network defaults; policies |
| **"Record trusted"** | A verified record any lender, landlord, insurer, buyer or agency can read in minutes, with consent | The firm certifies daily that the record agrees with bank and counterparty evidence |
| **"No decision taken blind"** | A short message before a big payment or commitment | Decision detectors (4.3) |
| **"Paid on time"** | Debtors chased and collected within policy | Invoices issued on the platform with payment requests; receivables agent |

Each gives a daily check. Step 1's P2 said checkability is a design choice. Here every condition is checked every day, so the engine learns far faster than the level 1 firm could [reasoned].

### 4.2 New products

In order of strategic weight. Revenue weight differs and is in section 8.

1. **The verified record, and trusted status built on it.** A record that is structured at birth, checked daily against the bank and certified by an accountable firm is worth more to lenders, insurers and the state than any filing [reasoned, from builder review]. Three uses. **Credit**: underwriting from live verified data instead of two-year-old accounts [conjecture]. **Everyday paperwork**: the mortgage reference or income proof becomes a consented read, not a letter (case type 25). **Trusted status with HMRC**: the Netherlands has run "horizontal monitoring" since 2005, including a track through tax service providers for small and medium firms, on a voluntary basis without a specific statute [seen, Chambers guide; Dutch tax administration reports]. A UK version for certified records would mean fewer enquiries, pre-agreed treatments and faster refunds [conjecture]. The firm pursues it from 2028 (9.5). Lenders pay a flat data fee, or the client keeps the saving. Never a commission.
2. **Tax leaves as it arises ("pay as you trade").** PAYE did this for employees in the 1940s [seen, general knowledge]. The self-employed never got it, because nobody sat in their money flow. It comes in three steps, each more "gone" than the last [reasoned]:
   - **2027: pay forward.** A share of each receipt is swept and then paid forward to HMRC. For self-assessment, HMRC's Budget Payment Plan already takes weekly or monthly direct debits towards the next bill [seen, gov.uk]. Its limits: HMRC pays no interest on it, and the owner can stop it at any time [seen, gov.uk; adviser summary]. So the firm sets it to match the live estimate, and stopping it needs a conversation with the partner, not a tap. VAT and PAYE amounts, due within weeks, sit in a pot.
   - **2028: the notice pot.** Where paying forward is not available, the pot is a notice account in the client's name, so a withdrawal takes days and triggers a call [conjecture: whether bank partners offer business notice accounts with sweep interfaces].
   - **2030s: split at the rail.** When customers pay through the platform's payment requests, the VAT and provisional income tax are split off at the moment of payment, as a rail feature. Split payment exists today in narrow forms: Italy applies it to supplies to public bodies [seen, Italian VAT law Art. 17-ter; EY, June 2025], and the EU's VAT in the Digital Age package moves towards real-time reporting [seen, Council adoption, 2025, via builder review]. The firm then stops being the collector and becomes the party that **certifies the split is right** [conjecture].
3. **The owner's financial policy.** One page: buffer, payment terms, how recurring payments are classed, how much to take out and how, what needs approval, what the firm may pay without asking. It is the client's equivalent of the firm's constitution (step 3b). It starts pre-filled from the network: a new bakery begins with the defaults of bakeries like it, and the owner confirms or changes them [reasoned, from builder review]. Setting it takes perhaps twenty minutes, not an hour. It removes the repeating questions; it does not remove the hard ones (7.5).
4. **A running finance function.** Bills paid on policy, invoices issued and chased, payroll, cash. For growing companies, a monthly board pack, a covenant watch and a senior person in the room.
5. **Certainty, from year one.** A guarantee that the final bill will be within a stated margin of the live estimate, for reasons the firm could have known, capped in the first year. Fee protection insurance is sold widely today [seen, via practitioner review], so the form is familiar. It is the clearest sales message the firm has [reasoned]. Later, **tax smoothing**: a fixed monthly payment, with differences covered within limits [conjecture; priced from the firm's estimate-error data, as step 1, P3 proposes].
6. **The household plan and desk.** Company and personal affairs planned together and continuously: extraction, pensions, the spouse, property, the eventual sale. And the household's paperwork handled, priced into the tier rather than refused or billed by the letter.

### 4.3 New decisions supported

| Moment | Detected by | What the owner hears |
| --- | --- | --- |
| Receipts approach the VAT threshold | Rolling turnover | "You cross the threshold in about six weeks. Here are your options and what each costs." |
| A large purchase is about to go through | A purchase order or quote on the platform, or in chat | "Buying the van before 31 March brings £X of relief forward. Leasing costs £Y more over four years." |
| A director moves money to themselves | Payment to a personal account | "This overdraws your loan account. A dividend instead costs £Z less. Shall I prepare it?" |
| A landlord's mortgage rate resets | Rent and mortgage flows | "Property 3 now loses money after tax. Hold, sell or refinance: here are the numbers." |
| The owner tries to stop paying tax forward | Change to the payment plan or a notice withdrawal | "That leaves £X of January tax unfunded. Here is what else could give this month." |

### 4.4 New data

- **Structured transactions at birth**, across many businesses: the raw material for network defaults and for the verified record.
- **Positions dated before their tax effect**: supporting evidence in an enquiry, not proof.
- **Scored forecasts** for every client, every month: a track record of judgement.
- **Estimate error by cause**: the data that prices certainty.
- **Behaviour data**: pot withdrawals, prompt reply rates, policy changes. The things the practitioner says break designs [seen, practitioner review], measured instead of assumed.
- **Decision outcomes**: what the owner chose and what followed. Step 1 said slow outcome signals are the hardest to get. This design produces them as a by-product [reasoned].

---

## 5. Where the firm's capability sits, by segment

Of step 3c's four forms, the mix should follow decision value and the client's appetite for a person [reasoned]:

| Segment | Platform and agents | People | Firm runs the function | Why |
| --- | --- | --- | --- | --- |
| **Sole traders** | **Core**: invoicing and payment requests, bank check, tax paid forward, rare questions | **A pooled team**, not a named partner: fast answers, life events, decisions. Said plainly at sale [reasoned, from practitioner review] | Tax only | Low decision value; high value from tax vanishing; owners value a fast answer over a name [seen, practitioner review] |
| **Landlords** | **Core**: rent account, letting-platform feeds, mortgage data | Pooled team; partner for portfolio decisions | Tax and property accounts | Information is born at letting agents, so partner with them |
| **Stable companies** | **Core**: invoicing, bill-pay, payroll, bank, cards, mandate for bills and tax | A named partner in the owner's chat, about 1 per 400–550 at maturity | **Yes**: payables, receivables, payroll, tax | Extraction and the loan account are continuous decisions |
| **Growing companies** | Plus lender, investor and banking interfaces | **An embedded finance lead**: daily in the channel, on site some days, at the board. About 1 per 8–12 companies | **Fully** | High, continuous decision value. Board meetings, investor calls and bad weeks do not compress [seen, practitioner review] |

All four work on one shared ledger: client, firm and agents act on the same entries at the same time. **Choosing the form is choosing the price point.** The platform is cheap and removes the tax problem for everyone. Embedded people are costly and pay only where decisions are large [reasoned].

**One rule across segments.** The firm sits *beside* the owner's money, never *between* the owner and it. The client's bank holds the funds, or HMRC does once tax is paid forward. The firm holds a mandate the owner can revoke. Granting is easy; stopping tax payments has deliberate friction; stopping bill-pay does not. That keeps the firm out of client-money rules, keeps interest with the client, and makes trust easier to give [reasoned; regulatory reading in section 10].

---

## 6. The boundary choice

### 6.1 The recommendation: own the record, the network and the accountability; rent the rails

The first draft said "do not build a ledger" and proposed a canonical state above several vendors' ledgers. The builder review showed the flaw: that state *is* a ledger. Syncing it with three vendors recreates the two-record problem the design condemns, and every vendor change breaks a sync [reasoned; experience, builder review]. What is costly is not the ledger as a data structure. It is the shared workspace, the rails around it and the distribution (Pennylane raised about €360m mostly for those [seen, step 3c]). So the revised stance, layer by layer, still follows step 1's P3: the fast, checkable layers become cheap; the slow, accountable ones keep the margin [reasoned].

| Layer | Who offers it near free by the 2030s | Stance |
| --- | --- | --- |
| **The ledger: one record per household** | Vendors and banks offer ledgers free [seen: FreeAgent is owned by NatWest and free to its business customers; general knowledge, not checked] | **Own one, with an open data model.** Others read and write to it. Read clients' old ledgers only during migration |
| **Transaction rails**: invoicing, bill-pay, payment requests, payroll, Peppol access | Vendors; accredited e-invoicing providers from 2029 | **Own the product** that makes data born structured. **Rent** the payment rails and, at first, Peppol access |
| **Network knowledge**: counterparty coding, priors, error statistics | Nobody: it needs many businesses on one data model | **Own.** The compounding asset |
| Filing | Vendors; possibly HMRC itself | **Build thin** |
| **The money mandate** | Banks, for their own customers only | **Own the relationship; rent the rails** from a regulated payments partner |
| **Accountability**: licence, insurance, guarantee, named person, certification | Nobody easily | **Own.** The margin is here |
| **Trusted status** with HMRC and lenders | Nobody yet | **Own**; earned from data |
| **Decisions at the moment** | Banks and vendors will try, but will not carry the consequence | **Own** |

### 6.2 Two entities

A 5,000-client firm cannot make a network. Shared counterparty knowledge, both sides of a trade on one record, and priors for new clients need hundreds of thousands of businesses [reasoned, from builder review]. Small businesses mostly use the software their accountant chooses [experience, builder review], and there are tens of thousands of UK practices [seen, approximate, via builder review]. So distribution runs through accountants.

**The design** [reasoned]:
- **The platform company** runs the ledger, rails, network, money layer and evaluation harness. It sells to accountancy firms, cheaply at first, priced per business.
- **The firm** sells the accountable layer and the finance function. It is the platform's first and reference customer.
- **Separation rules.** Other firms' client data is never visible to the firm. Network knowledge is aggregated and anonymised; supplier categories are shared, amounts and identities are not. The platform takes no fee that depends on which firm a business chooses.
- **Phasing.** The structuring layer (ledger, invoicing, network defaults) goes to other firms in 2027–28. The money layer and certification go to them only once proven on the firm's own clients, from about 2030. A continuous tax engine wrong in public across many firms would cost more than a late start [reasoned].

**The channel conflict** is real: other firms may not want a platform whose sister firm competes with them. Two answers. The firm competes on the accountable layer that most practices also sell, so the platform must be the better tool regardless [reasoned]. And the platform can be governed or later owned apart from the firm, as the shareholders choose [conjecture].

### 6.3 Who else is in the picture

| Player | What they are doing | How the firm and platform stand |
| --- | --- | --- |
| **Banks** | Free software, tax pots, invoicing [seen in part, general knowledge] | **Partner for distribution and rails; carry the risk they will not.** Banks do not want tax-error risk [reasoned, practitioner review]. Offer Clear white-labelled, with the firm carrying that risk, from 2027 talks and a 2028 pilot |
| **Ledger vendors** | Building agents [seen: Xero's JAX, company claims]; controlling interfaces | **Rival at the platform level.** Read their data during migration; never depend on their interfaces for the live record |
| **Accountancy firms and roll-ups** | Buying practices; automating at level 1 | **Customers of the platform and competitors of the firm.** They bring clients; the firm wins on the accountable layer |
| **Lettings roll-ups** (Dwelly and others) | Run rent flows and landlord relationships [seen, step 3c] | **Partner.** They hold landlord information at birth; offer them the tax layer |
| **HMRC** | Target of 90% digital interactions by 2029–30, 78% in 2025–26; agent services lag [seen: HMRC roadmap and 2026 update; ICAEW] | **Data partner, then trusted counterparty.** Show paid-forward tax and clean data across thousands of clients; seek a pre-cleared status from 2028 |
| **Lenders and insurers** | Want verified small-business data | Read the verified record for a flat fee, or the client keeps the saving. Never a commission that bends advice |
| **Clients' own agents** | By the early 2030s, a counterparty on many invoices will be software [conjecture] | Build agent-to-agent invoicing and settlement into the rails from the start. E-invoices over Peppol are already machine to machine [reasoned] |

**The 2035 contest** [reasoned]. It is about **whose record the economy trusts, and who holds the owner's mandate at the moment of decision.** A bank holds the money but not trust for advice. A vendor holds a ledger but not the consequence. A roll-up holds relationships but an old process. The platform aims to hold the record; the firm aims to hold the mandate, the decision and the accountability.

---

## 7. The organisation that follows

### 7.1 The agent architecture

One shared state, as step 3b requires. Its centre is not a case list but **each household's ledger**: transactions as born, policies, positions, forecasts, obligations, mandates, people.

| Layer | Agents |
| --- | --- |
| **Per client** | **The client's finance agent**: one orchestrator per household, acting within the owner's policy; issues invoices and payment requests, raises decision moments, asks its rationed questions, answers in chat, handles household paperwork |
| **Shared engines** | Continuous tax engine; independent recomputer on different code and model; policy engine; network-defaults engine; forecaster; payroll and property engines |
| **Money** | Mandate agent (pay-forward, sweeps, bills within policy); receivables agent; payee verification |
| **Counterparties** | HMRC, Companies House, banks, Peppol, letting platforms, lenders, other firms on the platform, clients' agents |
| **Verification and evaluation** | Condition monitors; scorers for estimates, forecasts and decision outcomes; behaviour monitors (withdrawals, reply rates, feed breaks); test suites; model-release harness (step 1) |
| **Governance** | Constitution auditor; fraud monitor; conflict detector; data-separation monitor for the network; **a circuit breaker on money movement, separate from the one on filings** |

**Three new constitution clauses**, added to level 1's twelve [reasoned]:
- **Money.** The firm moves money only under a revocable mandate, within the owner's written policy. It pays only payees that arrive through a structured invoice or pass confirmation of payee, and a payee new to the client is first paid by the owner, in their own bank. Funds stay in the client's account or go to HMRC. Interest is the client's.
- **The record.** The client's record belongs to the client and leaves with them, in an open format, on request. The firm takes no payment from a lender, insurer or provider that depends on what the client chooses.
- **The network.** What one client teaches the network is shared only in aggregate and without identities or amounts.

### 7.2 The people, by kind of need

| Kind of need (step 3b, plus level 1's seventh) | Role | What they do |
| --- | --- | --- |
| **1. Purpose** | Owners and board | Constitution; risk appetite; prices of certainty; capital; partners and acquisitions; the relationship with the platform |
| **2. Definition of good** | **Standard-setters** by family: continuous tax; money movement and fraud; payroll; advice; **training** | Own tests and thresholds; decide when a condition counts as true; audit samples |
| **3. Answerability** | Accountable officers with deputies: head of tax, reporting officer, **head of payments**, **head of certification** | Sign for the system; answer to HMRC, supervisors, the payments partner, insurers, lenders who rely on the record, clients |
| **4. Capability gaps** | Judgement desk | Enquiries, unusual VAT and property, payroll exceptions, year-end judgements, disclosure at onboarding, hard decision moments |
| **5. Client demand** | **Pooled team** for Clear; **named partners** for Core; **embedded finance leads** for Function | Pooled team: fast answers, life events, paperwork. Partners: first policies, owners who stop paying forward, big decisions. Leads: weekly with the owner, at the board, on site some days |
| **6. Physical world** | Scanning contractor; inspection visits | Small |
| **7. A counterparty's channel** | HMRC desk | HMRC's errors and web-only steps, shrinking with trusted status and better agent services |
| **Scaffolding** | Firm builders and evaluators; shadow reviewers; **trainees** | The platform's engineers sit in the platform company, not here |

**How people work.** Nobody prepares anything. Partners and leads work from the live state, in the client's channel; the system sets their week (decision moments, owners who have stopped paying forward, quiet owners, policies due, life events). Standard-setters work from condition failures and samples, not files.

**The training route** [reasoned, from practitioner review]. Today's judges learned by preparing accounts and getting them wrong under review. If agents prepare everything, that school closes, and the judgement desk has no successors by the early 2030s. So the firm builds a different school:
- **Blind cases.** Trainees work real past cases from the raw record without seeing the answer, then compare with the recomputer, the reviewer and what HMRC later did.
- **Building the tests.** Every trainee writes test cases for the engines. To break an engine you must understand the rule.
- **Shadowing the recomputer.** When engine and recomputer disagree, a trainee resolves it first, under a standard-setter.
- **A small book of exceptions.** From the second year, each trainee owns real exceptions for a few dozen clients under supervision.
- **Rotation** through the judgement desk, payroll exceptions and an embedded lead's companies.

Whether this counts as practical experience for ACA and ACCA is a question for the bodies, raised in 2027 [conjecture: their answer]. Trainees are counted in the core and kept at about six a year even in landscape A. They are the cost of having judges in 2035.

### 7.3 Operating rhythm

- **Continuous:** transactions structured, bank checked, tax recomputed and paid forward, decision moments, condition monitoring.
- **Daily:** exceptions cleared; condition failures and the money breaker reviewed.
- **Weekly:** leads with each growing company; standard-setters review drift; playbook releases within reach limits.
- **Monthly:** forecasts scored; a short position letter to every owner; board packs; behaviour review (withdrawals, reply rates, feed breaks).
- **Annually:** the year's confirmation, and a policy review with every owner, in one sitting.

There is no January peak. There is a Budget peak, which agents absorb [reasoned].

### 7.4 Headcount for 5,000 clients [conjecture]

Four assumptions carry the numbers. **First, not every client is at source at once**: 30% in 2027; 70% (A) or 55% (B) in 2030; 95% (A) or 85% (B) in 2035. **Second, policies and network defaults remove 70–80% of questions in A and 60–70% in B**, not 90% (7.5). **Third, growing companies taking Function** rise from 150 in 2027 to 300–350 by 2035, with leads at 1:8 rising to 1:12, not 1:25. **Fourth, platform engineers are counted in the platform company**, whose cost reaches the firm as a fee (8.2).

| Role | 2027 | 2030 A | 2030 B | 2035 A | 2035 B |
| --- | --- | --- | --- | --- | --- |
| Owners and board | 3 | 3 | 3 | 2 | 3 |
| Accountable officers and deputies | 4 | 4 | 4 | 4 | 4 |
| Standard-setters | 5 | 5 | 5 | 4 | 5 |
| Judgement desk | 9 | 7 | 9 | 6 | 9 |
| Named partners (Core) | 10 | 6 | 8 | 4 | 6 |
| Pooled team (Clear and household) | 4 | 3 | 4 | 3 | 4 |
| HMRC desk | 4 | 2 | 3 | 1 | 2 |
| Shadow reviewers | 8 | 2 | 5 | 0 | 2 |
| Firm builders and evaluators | 6 | 4 | 5 | 3 | 4 |
| Operations and fraud desk | 4 | 3 | 3 | 2 | 3 |
| Trainees | 6 | 6 | 6 | 5 | 6 |
| **Core subtotal** | **63** | **45** | **55** | **34** | **48** |
| Embedded finance leads | 19 (150 cos., 1:8) | 28 (280, 1:10) | 28 (250, 1:9) | 29 (350, 1:12) | 30 (300, 1:10) |
| **Total, firm** | **82** | **73** | **83** | **63** | **78** |
| *Platform company, for comparison* | *about 20* | *about 45* | *about 40* | *60–90, serving many firms* | *50–70* |

| | Traditional | Level 1, 2027 | Level 1, 2035 A / B | **Level 3, 2027** | **Level 3, 2035 A / B** |
| --- | --- | --- | --- | --- | --- |
| People in the firm | 110–120 | 75 | 31 / 51 | 82 | 63 / 78 |
| Of which compliance and client core | about 110 | 75 | 31 / 51 | 63 | **34 / 48** |
| Of which selling a finance function | few | 0 | 0 / 0 | 19 | 29 / 30 |
| Questions to owners a year | many, unmeasured | about 150,000 | lower | about 110,000 | **about 25,000 / 45,000** |
| Peak | January | January | January, smaller | January, smaller | **none** / Budget |

**What the revision changed.** The first draft had a 2035 A core of 24. The practitioner's corrections (harder exceptions, fewer questions removed, a training route, a fraud desk) take it to 34. The builder's moves (structure at birth, network defaults) keep it from going higher. Leads roughly double, because the ratio is now realistic. The core is no smaller than level 1's. The difference is what it sells, and that its work does not come back.

### 7.5 What drives the numbers

1. **The share of clients at source.** Every client still on old processes costs level 1 headcount. Adoption, not capability, sets the 2027–2030 numbers [reasoned].
2. **How much is born structured.** Each point of transactions structured at birth removes questions that no policy can. The target is most of a Core client's transactions by 2032 [conjecture, from builder review].
3. **The policy and network effect.** Policies handle the easy, repeating 70%; bank rules in today's ledgers already do much of that [seen, practitioner review]. The hard cases are mixed Amazon orders, personal cards used for fuel, cash takings, and a payment to a brother-in-law that is part loan and part wages. Structure helps some (itemised invoices); network defaults help few. So partner ratios sit at 400–550, not 1,000 [conjecture].
4. **Lead ratio and price.** At 1:8–12 the Function tier pays only if priced against a part-time finance director (8.1).
5. **The review rule.** If professional bodies and insurers accept sampling plus independent recomputation, shadow reviewers go by 2030. If not, the 2035 B core holds even in landscape A (section 10).
6. **HMRC's channels and trusted status** set the HMRC desk and part of the judgement desk.

**The honest point.** In 2027 level 3 needs more people than level 1. Its advantage is that the work it removes does not come back, and what it sells is worth more [reasoned].

---

## 8. Economics

**All of this section is conjecture**: arithmetic on assumed numbers, to show the shape. Baseline from the level 1 example: a traditional firm earns about £1,700 a client, £8.5m at 5,000 clients, at about 30% margin.

### 8.1 What is sold, and how it is priced

| Tier | For | Includes | Illustrative price, 2027 |
| --- | --- | --- | --- |
| **Clear** | Sole traders, landlords, linked individuals | Tax paid forward; returns as side effects; safe-to-spend; decision moments by agent; pooled team; household paperwork; capped estimate guarantee | £550–800 a year; linked individual £300 |
| **Core** | Stable companies with the director's household | Clear, plus invoicing, bills, payroll and tax run under policy; continuous extraction planning; named partner | £1,800–2,600 a year |
| **Function** | Growing companies, 10–25 staff | Core, plus the full finance function, an embedded lead, board pack, lender work | £18,000–28,000 a year |
| **Function Plus** | Investor-backed or 25–50 staff | Function, plus investor reporting, raise and covenant work, more of the lead's time | £30,000–50,000 a year [from practitioner review] |
| **Certainty** | All | Capped estimate guarantee in the price from year one; smoothing later | Smoothing 1–2% of tax smoothed |
| **Record** | Lenders, insurers, with client consent | Read of the verified record | Flat fee per read; never a commission |
| **Projects and arrival** | All | Sale, raise, enquiry defence, estates; clean-up and onboarding | Fixed fees |

**Pricing logic** [reasoned]. Price the condition and the person, never the filing. Filing will be close to free, so a price tied to it decays. A condition holds its value as long as rivals cannot make it as true. The Function tiers are priced against the real alternative, a part-time finance director, not against an accountant's fee.

### 8.2 The firm: revenue, cost and margin at 5,000 clients

2027 revenue: Clear about £1.45m (2,000 at about £650, plus 500 linked individuals at £300); Core about £4.2m (2,000 × £2,100); Function and Plus about £3.6m (150 at an average of £24,000); other growing companies on an enhanced Core about £1.75m (350 × £5,000). **About £11.0m, or £2,200 a client.**

| | 2027 | 2035 A (capability compounds) | 2035 B (plateau) | D (price collapse) |
| --- | --- | --- | --- | --- |
| Prices assumed | As 8.1 | Clear £400; Core £1,600; Function average £26,000 × 350 | Clear £600; Core £2,000; Function average £28,000 × 300 | Clear £150; Core £900; Function average £20,000 × 300 |
| **Revenue** (incl. record fees, smoothing) | £11.0m | £14.3m | £15.1m | £8.8m |
| Core people (loaded, about £85,000) | £5.0m (63) | £2.9m (34) | £4.1m (48) | £3.1m (about 36) |
| Embedded leads (loaded, £140,000–150,000) | £2.7m (19) | £4.4m (29) | £4.5m (30) | £4.5m (30) |
| Platform: build share in 2027, per-client fee later | £2.5m | £0.6m | £0.8m | £0.4m |
| Model use and verification | £0.4m | £0.3m | £0.4m | £0.3m |
| Banking, payments and feed partners | £0.6m | £0.3m | £0.5m | £0.2m |
| Insurance (including payment-error and crime cover), guarantee reserve, compliance | £0.8m | £0.9m | £0.8m | £0.8m |
| Acquisition and migration | £1.5m | £0.5m | £0.6m | £0.3m |
| **Cost** | £13.5m | £9.9m | £11.7m | £9.6m |
| **Margin, level 3 firm** | **about −23%** (+13% before platform build and acquisition) | **about 31%** | **about 22%** | **about −9%** at this mix |
| Margin, level 1 example | about −8% | 24% | 18% | 18%, if the accountable layer sells |

### 8.3 The platform company, in outline [conjecture]

- **2027–29:** an investment, funded as one. It costs £3–5m a year; most of it is the firm's share above until other firms join.
- **2035 A:** perhaps 1,000–2,000 firms and 150,000–300,000 businesses, a few per cent of UK businesses, at £5–10 a business a month. Revenue of roughly £10–35m, plus record fees.
- **Why it matters for the firm.** It is the hedge against landscape D. A price collapse in services is a volume gain for a platform priced per business [reasoned].

### 8.4 What the numbers say [reasoned, on conjectured numbers]

- **2027 is a deeper investment year** than in the first draft and than level 1, because the firm now pays for a ledger and rails as well as the money layer, and runs realistic lead ratios.
- **In landscape A** the firm beats level 1 at fixed size, and its revenue grows rather than shrinks, because Function is priced against a finance director.
- **In landscape B** prices hold and the firm sells a bigger product to the same clients.
- **In landscape D** the firm alone loses money at this mix. It survives by changing mix (Clear sold through a bank at volume, with the pooled team only for events; Function grows) and because the platform gains. Firm and platform together are better placed than level 1, but not safe.

### 8.5 Where the profit comes from

1. **The finance function for growing companies,** the largest source. Agents do the work; one lead serves 8–12 companies, priced against a part-time finance director.
2. **Certainty priced from data,** from year one, capped. The firm knows its estimate error by cause and prices guarantees better than anyone without that data (step 1, P3).
3. **The trusted record:** record fees, and the cheaper enquiries and faster refunds that trusted status brings.
4. **Decisions at the moment.** Not priced per decision, but the reason owners stay and move up a tier.
5. **Low marginal cost at source** (perhaps £60–100 a sole trader by 2035 A), which pays only with distribution at volume.

**Not from:** filings, interest on clients' money, or lender commissions. The first decays. The other two would undermine the trust the mandate depends on [reasoned].

---

## 9. How it is built from 2027

### 9.1 What exists to use today

- **Budget Payment Plan**: weekly or monthly direct debits towards the next self-assessment bill; needs the previous bill paid; no interest paid; the taxpayer can stop it [seen, gov.uk; adviser summary].
- **Commercial variable recurring payments**: Wave 1 live from 2 June 2026 under the UK Payments Initiative scheme; most volume still sweeping [seen: FCA statement on the scheme's launch; vendor summaries; date not checked against the scheme itself].
- **Paying HMRC by bank-initiated transfer:** available [seen, general knowledge, not checked in this run].
- **Making Tax Digital interfaces** for VAT and income tax; income tax cohorts from April 2026, 2027 and 2028 [seen, gov.uk, via level 1].
- **Companies House identity verification and software filing** [seen, via level 1].
- **Mandatory B2B e-invoicing** for VAT from 1 April 2029 over Peppol; roadmap published autumn 2026 [seen].
- **Examples abroad:** Italian central invoice clearance since 2019; French mandatory e-invoicing from September 2026; Italian split payment for public-body supplies; Dutch horizontal monitoring through tax service providers [seen; sources in the reviews and at the end].
- **Mandatory reimbursement of authorised push payment fraud** since October 2024 [seen, via practitioner review], which sets who carries a payment-fraud loss.

### 9.2 What must be built

1. **The ledger**, one per household, with an open data model and a shared workspace where owner, firm and agents act on the same entries.
2. **The transaction rails**: invoicing, payment requests, bill-pay, payroll, Peppol access, built for agent counterparties from the start.
3. **The network-defaults engine**, with the separation rules in 6.2.
4. **The policy engine**: owner policies in plain words, pre-filled from the network, compiled into rules agents cite.
5. **The continuous tax engine** across all taxes, with an independent recomputer. The hardest single build: it must be right every day, not once a year.
6. **The money layer**: pay-forward, sweeps, payments, payee rules, its own circuit breaker, on a regulated partner's rails.
7. **The question budget**: rationed, ranked by value, with safe defaults.
8. **Decision detectors**, each with a test suite of past cases.
9. **The verified record** and interfaces for lenders, agencies and HMRC.
10. **The evaluation harness**: condition monitors, behaviour monitors, scorers for estimates, forecasts and decision outcomes (step 1).
11. **The training school** (7.2).

### 9.3 The first wedge

**Tax paid forward for sole traders and landlords entering Making Tax Digital, with invoicing on the platform** [reasoned].

- **Why this segment.** From April 2027 everyone with qualifying income over £30,000 must keep digital records and send quarterly updates; from April 2028, over £20,000 [seen, gov.uk]. Each cohort is forced to change. The product removes the new burden and adds what they never had: tax already gone, and money in the account that is theirs to spend.
- **Why it proves the design.** It needs the hardest parts (the record, the tax engine, money movement) on the simplest client: one person, one account. And it works today: the Budget Payment Plan carries the pay-forward without waiting for commercial VRP to widen.
- **Certainty from day one.** A capped guarantee is the sales message.
- **Landlords through partners.** Lettings roll-ups and platforms hold the rent flows.
- **The weakness.** Low revenue per client. The wedge proves the machine; it does not pay for the firm.

**Two moves run alongside.** Buy one or two books of owner-managed companies in 2027 and move them to Core over two to three years: revenue, test-suite history, and growing companies for Function. And give the structuring layer to a handful of other firms as design partners, so the network starts growing in year one.

### 9.4 What would make clients adopt it

- **A forced moment:** MTD cohorts and e-invoicing.
- **Visible money:** "safe to spend" and "tax already gone" are understood at once. Accounts are not.
- **Less effort from week one:** twenty minutes confirming network defaults, then a few questions a month at most.
- **Their accountant recommends it:** most owners use what their accountant chooses [experience, builder review].
- **A guarantee** on the estimate.
- **A person** for first-year trust: named for companies, a fast pooled team for sole traders.
- **Distribution where owners already are:** their accountant, their bank, their letting agent.

### 9.5 The sequence to 2035 [conjecture for dates]

| Period | Main moves | Clients at source |
| --- | --- | --- |
| **Before the wedge** | Settle insurance cover for payment errors, and liability terms with the payments partner (10.2) | — |
| **2027** | Build ledger, rails, tax engine and pay-forward. Launch Clear for the April 2027 cohort with a capped guarantee. Buy one or two company books. First design-partner firms on the structuring layer. Review or sample all filings. Talks with a bank on white-labelled Clear. Raise the training route with ACA and ACCA bodies | about 30% |
| **2028** | Core for bought companies. Network defaults live. Notice pots. Bank pilot. Approach HMRC on a trusted status for certified records | about 45% |
| **2029** | E-invoicing: payables and receivables born structured for VAT-registered clients. Function scaled. Platform opened to firms generally | about 60% |
| **2030** | Sampling replaces review where bodies and insurers accept it. Money layer offered to other firms. Smoothing piloted. Verified record used by first lenders | about 70% (A) |
| **2031–33** | Split at the rail for payments through the platform. Trusted status in operation, if granted. Own payments authorisation if volume justifies it | 80–90% |
| **2034–35** | Data exchange with HMRC replaces returns for certified clients, if allowed. The owner confirms a year, not forms. The firm is a finance function with an accountable core; the platform is a record others rely on | about 95% (A) |

---

## 10. What would make this wrong, and the stress test

### 10.1 What would make this wrong

1. **Owners will not let tax leave.** If they stop the pay-forward and drain notice pots in bad months, "tax already gone" fails when it matters. Measure withdrawals by month, with and without the Budget Payment Plan route [reasoned, from practitioner review].
2. **Owners grant mandates but not trust.** The builder expects quick uptake of bill-pay; the practitioner expects revocation. Measure both, separately [reasoned].
3. **Structure at birth stays low.** If most transactions still arrive unstructured, questions return, partner ratios fall towards level 1's 300, and the firm is a good level 2 firm [conjecture].
4. **The network does not form.** If other firms will not join a platform with a competing sister firm, the network effects never arrive. Then the firm is a well-designed firm with a costly ledger [reasoned].
5. **Banks or vendors take the bottom tier.** A bank with a tax pot, free software and a licensed advice partner could offer Clear at zero: landscape D, early. The answer is the top tiers and the platform [reasoned].
6. **HMRC collects at source itself.** Good for owners. The tax layer goes; the firm survives through Function, decisions and certification [conjecture].
7. **A money-movement failure.** One fraud or error moving many clients' money would end trust. The money breaker, payee rules and reach limits matter more than any filing control [reasoned].
8. **Growing companies prefer their own hire,** shrinking the main profit source [conjecture].
9. **Capability stalls below continuous accuracy.** If the tax engine needs heavy review, costs stay near level 1 [reasoned].
10. **The judges run out.** If the training route does not produce judgement, the desk cannot be staffed in the 2030s [reasoned, from practitioner review].

### 10.2 The stress test, applied now

| Fact | Effect on the design |
| --- | --- |
| **Moving others' money needs authorisation** as a payment institution or an agent of one [seen, general knowledge of UK payment services regulation] | Use a regulated partner's rails from 2027. Funds stay in the client's account or go to HMRC. Seek authorisation only at volume |
| **Commercial VRP is new**: Wave 1 live June 2026; most volume still sweeping [seen, scheme summaries] | The wedge does not need it: the Budget Payment Plan and sweeps to the client's own pot carry pay-forward today |
| **The Budget Payment Plan can be stopped by the taxpayer and earns no interest** [seen, gov.uk; adviser summary] | Friction is in the service, not the scheme: stopping it is a conversation. Interest lost is the price of certainty; say so |
| **Mandatory reimbursement for authorised push payment fraud since October 2024** [seen]; **professional indemnity cover may answer for advice but not payment errors** [seen, practitioner: insurers ask about scope] | Settle liability with the payments partner and buy specific cover before the wedge. New payees are paid first by the owner; the firm pays only structured or confirmed payees |
| **Holding client money triggers professional client-money rules** [seen, general knowledge] | Do not hold it. A pot in the client's name avoids the rules |
| **The taxpayer remains liable for their tax** [seen] | Certainty is a guarantee or credit, not a transfer of liability. Smoothing needs an insurer or reserve, and may count as insurance; take advice first |
| **HMRC forbids automating its web pages; interfaces are allowed** [seen, level 1] | The HMRC desk stays until agent services improve or trusted status arrives |
| **Professional bodies: members answer for work "irrespective of the use of AI tools"; submissions should be reviewable** [seen, level 1] | Level 3 helps the argument: every output is a side effect of a state checked daily. If the bodies insist on per-output review, the 2035 B core holds in landscape A |
| **Training needs practical experience** under ACA and ACCA rules [seen, general knowledge] | Design the training route with the bodies from 2027, so blind cases and exception books count |
| **Directors sign their accounts; taxpayers file their returns** [seen] | One annual sitting gives every declaration the law needs. The forms are derived; the declaration remains until law changes |
| **Client confidentiality and data protection** [seen, general knowledge] | Network knowledge shared only in aggregate, without identities or amounts; a separation monitor checks it |
| **Split payment exists only in narrow forms** (e.g. Italy, public-body supplies) [seen] | Split at the rail is a 2030s option on the platform's own payment requests, not a dependency |
| **E-invoicing from 2029 covers VAT-registered business trade only** [seen] | Small sole traders and consumer sales use the platform's own invoices and payment requests, with the bank as fallback |
| **Small firms took about fifteen years to adopt cloud accounting** [general knowledge, step 1] | Adoption will lag the design. The plan assumes 30% at source in 2027. Distribution through accountants is the fastest route |
| **Banks, vendors and roll-ups move first** [seen in part] | The firm cannot outspend them. It must out-design them in the accountable layer, and the platform must reach firms early |

### 10.3 What the stress test changes

1. **Not the design.** Structure at birth, one record, network defaults, pay-forward, the accountable core and the verified record all survive today's rules.
2. **Tax leaves through HMRC's own plan first;** split at the rail waits for the platform's payment volume.
3. **Human declarations stay,** given once a year on a position the owner has watched all year.
4. **The review rule decides headcount,** as level 1 found.
5. **Insurance and payment liability come first,** before the first payment is made.
6. **Trust in money movement and owner behaviour decide adoption.** That is where the first year's evidence should go.

**Where this is weakest.** Every figure is conjecture. Five numbers decide whether the design works, and nobody knows them yet: how many owners keep paying forward in bad months; how many questions structure, network and policy remove; how fast prompt replies decay; how often feeds break; and whether other firms will join the platform. The first four can be measured in the wedge's first six months, and the fifth in the first year of design partners. That is the reason to start there.

---

## 11. Review and response

**B** = builder review; **P** = practitioner review.

| # | Point | What I did |
| --- | --- | --- |
| B1 | The source is the transaction, not the bank feed | **Taken.** "Structure at birth" is the first mechanism; the platform owns invoicing, bill-pay, payment requests and payroll; the bank feed is the check and fallback (2.1, 3.1, 6.1) |
| B2 | "Do not build a ledger" is the wrong lesson | **Taken.** The canonical state was a ledger in disguise. Now: own one ledger with an open data model; read old ledgers only during migration (6.1) |
| B3 | The unit of design is too small; think in networks | **Taken.** Network defaults, both sides of a trade, priors for new clients (3.1, 4.2). Network knowledge is owned and governed by a new constitution clause (7.1) |
| B4 | Distribute through accountants, from 2027 | **Taken, phased.** Two entities; the firm is the reference customer. Structuring layer to design-partner firms in 2027–28; money layer and certification only once proven, from 2030 (6.2) |
| B5 | Tax at source should move into the rails | **Taken as the third step** of pay-forward, for the 2030s; the firm becomes the certifier of the split. Split payment exists only in narrow forms today, so it is not a dependency (4.2, 10.2) |
| B6 | The verified record is the biggest product | **Taken strategically.** Now first among new products, with credit, paperwork and trusted status. Revenue still comes mostly from Function, and the text says so (4.2, 8.5) |
| B7a | Returns disappear | **Taken in substance.** The owner confirms a year, not forms. A declaration stays where law needs one (3.1, 10.2) |
| B7b | Owners hand over mandates readily | **Partly taken; see conflict 1** |
| B7c | Build for agent counterparties from the start | **Taken.** In the rails from 2027, not 2031 (6.3, 9.2) |
| B8 | What to keep: beside not between; profit leaves filing; household; priced certainty; forced moments | **Kept** |
| P1 | A revocable pot is not "tax already gone"; owners raid pots | **Taken.** Tax now leaves: paid forward to HMRC through the Budget Payment Plan from 2027, notice pots from 2028, split at the rail later. Stopping is a conversation, not a tap (4.2, 5) |
| P2 | One hour of policy will not remove 90% of questions; model 60–75% | **Taken, with a builder offset.** 60–70% (B) to 70–80% (A), the top end only with structure and network. Partner ratios 400–550, not 600–1,000 (7.5) |
| P3 | Moment questions decay | **Taken.** A question budget, ranked by tax value, with defaults safe for the owner. Dated answers help an enquiry but do not decide it (3.1, 3.2) |
| P4 | "Side effect" undersells the exceptions; judgement desk too thin | **Taken.** Payroll and accounts now carry a human residue; judgement desk 6 / 9 in 2035, not 3 / 6 (3.2, 7.4) |
| P5 | Lead ratio 1:15–25 is too high; raise the price | **Taken.** Leads at 1:8–12; Function Plus at £30,000–50,000. Leads roughly double; revenue rises more (7.4, 8.1) |
| P6 | Partners field everything else | **Taken.** New case type 25; mostly a side effect of the verified record; priced into Clear and Core (3.2, 4.2) |
| P7 | Money movement changes the firm's risk class | **Taken.** Payee rules in the constitution; payment-error and crime cover; liability terms settled before the wedge; fraud desk in headcount (7.1, 9.5, 10.2) |
| P8 | Who trains the judges? | **Taken.** A training school: blind cases, test-writing, recomputer shadowing, exception books, rotation. Trainees held at about six a year (7.2) |
| P9 | Pursue HMRC trusted status from 2028 | **Taken**, combined with the builder's horizontal-monitoring point (4.2, 9.5) |
| P10 | Certainty can launch in year one | **Taken.** Capped guarantee from 2027 as the main sales message (4.2, 9.3) |
| P11 | Pool the sole-trader partner | **Taken.** A pooled team for Clear, said plainly (5, 7.2) |
| P12 | Banks will not carry tax-error risk; offer to carry it earlier | **Taken.** Bank talks in 2027, pilot in 2028 (6.3, 9.5) |
| P13 | Test first: withdrawals, policy effect, reply decay, feed breakage, insurer terms | **Taken** into the evidence plan (10.1, 10.3) |

**Where the reviewers conflicted, and which way I went.**

1. **Will owners give money permissions?** The builder says owners hand over bill-pay quickly once the money stays in their account. The practitioner says owners raid tax pots in bad months. **Both, because these are different acts.** Bill-pay has a visible benefit, so granting is easy. Leaving tax alone has an invisible benefit, so withdrawal is the risk. So: easy to grant, friction to withdraw, and tax moved out of the account rather than ring-fenced in it. Each measured separately.
2. **How much does policy-setting remove?** The builder says network priors cut the partner's hour to ten minutes. The practitioner says policies remove 60–75% at best. **Both, again on different things.** Priors cut the time to set a policy; they do not touch the hard cases that drive questions. I took the builder on setup time and the practitioner on removal rate.
3. **How big, and how fast, to go?** The builder wants a platform for all firms from 2027. The practitioner's points (exceptions, liability, a hard tax engine) argue against exposing an unproven money layer widely. **I went with the builder on structure and the practitioner on money**: the structuring layer to firms from 2027–28, the money layer and certification only from 2030.
4. **How lean is the 2035 core?** The builder's moves push it down; the practitioner expects nearer 40. **The arithmetic lands at 34 in A and 48 in B.** The builder is right that structure removes work no policy can. The practitioner is right that exceptions, fraud control and training need people.
5. **Do returns disappear?** The builder says yes; today's law requires declarations. **The task disappears and the declaration stays**, given once a year on the whole position, until law changes.

---

## Sources checked in this run

- E-invoicing from April 2029: EY Global Tax News, 3 December 2025; gov.uk consultation response on electronic invoicing; OpenText and Edicom summaries of the 2026 roadmap.
- Commercial VRP: FCA statement on the UK Payments Initiative scheme launch; Plaid summary, June 2026; TrueLayer, "What does 2026 hold for VRP?".
- Budget Payment Plan: gov.uk, "Pay your Self Assessment tax bill: pay weekly or monthly"; LITRG, "Self assessment tax payments".
- Italian split payment: EY Global Tax News, 27 June 2025 (scope narrowed from July 2025; EU authorisation to 30 June 2026, extension not confirmed in this run).
- Dutch horizontal monitoring: Chambers, Tax Controversy 2026, Netherlands; Belastingdienst, "Tax supervision made to measure"; Meijburg summary.
- Xero JAX: Xero media release, September 2025.
- Pennylane: company site; no UK launch found.
- HMRC transformation roadmap and 2026 update (gov.uk); ICAEW summaries, July 2025 and July 2026.
- Not checked in this run, taken from the reviews: French e-invoicing timetable; Italian invoice clearance since 2019; EU VAT in the Digital Age adoption; APP fraud reimbursement from October 2024; number of UK practices; FRS 102 changes from 2026.
