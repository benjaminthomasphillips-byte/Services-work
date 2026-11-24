# Level 3. Probate and estate administration in England and Wales, redesigned from scratch

Revised draft by Claude, 24 November 2026, after two reviews: a builder of an online wills and probate service (`level3-probate-review-builder.md`) and a senior private client solicitor (`level3-probate-review-practitioner.md`). One author, no sub-agents. A stress test of the architecture that came out of `level3-accountancy.md` and `level3-lettings.md` ([element] to [element]). It follows the six-step procedure in `step-3c-the-electricity-test.md` and the kinds of human need in `step-3b-the-agent-enterprise.md`. Today's rules and institutions are facts to design around; they are applied in full only in section 10. A few facts were checked on 24 November 2026; sources are at the end. What changed after review, and why, is in section 11.

Labels:
- **[seen]** exists somewhere today, with source;
- **[reasoned]** follows from logic;
- **[conjecture]** plausible towards 2035.

Where a reviewer's practice experience is the only support for a claim, it is marked **[seen, practitioner review]** or **[builder review]**. That is practitioner judgement, not a checked source.

Every volume, price and headcount is a model figure for argument.

---

## The answer in brief

Level 1 asks: "how do agents run a probate department?" This paper asks: "what would a family buy if nobody had ever built a probate practice?"

1. **Estate administration exists because of a gap at death.** One person knew where everything was, what it was worth, what was owed and what they wanted. At death that knowledge vanishes, authority passes to people who lack it, and institutions freeze everything until someone proves who may act. Most of today's work is rebuilding a dead person's financial life from the outside, by letter, months later [reasoned].
2. **The grant is a proof token, not a piece of work.** It exists to tell a bank, a registrar or the Land Registry: "pay this person; you will not have to pay twice". Anything that gives the same assurance can do its job [reasoned].
3. **So the target is not a faster probate. It is an estate that mostly does not need one.** During life, give every asset a destination that works at death without a grant (nominations, pension wishes, policies in trust, payable-on-death instructions where offered), carrying a reserve for tax and debts. Test the will while the person is alive, so they resolve its ambiguities themselves. The readiness score measures one thing: **the share of the estate that will reach the right people within a fortnight of death, net of what is owed** [reasoned].
4. **For what still needs authority, replace or pre-empt the token.** In the near term, an insurer-backed indemnity lets a partner bank release money before the grant for low-risk member estates. Towards 2035, argue for two changes in law: statutory nominations for ordinary accounts and investments, and **a will proved in life**, which some US states already allow [seen; conjecture for England and Wales].
5. **Sell two things, paid for by different people.** During life, a condition, **"if I died tonight, my family would be paid in weeks and nobody would fight"**, free to the person and paid for by employers, banks, pension schemes and charities. After death, a guaranteed outcome: **settled by a date, at a fixed price, with the executors carrying no personal liability for process errors**. A named person guards the family's time and peace [reasoned].
6. **The hardest design problems are authority and the principal.** The client who chose the firm dies. Authority passes to executors the firm may never have met, who are free to go elsewhere, acting for beneficiaries whose interests differ. Every counterparty waits for a court token before it acts. And the firm's promise, made in 2027, may fall due in 2055. The architecture has no element for any of this [reasoned].
7. **Headcount.** At about 12,000 estates, 1 million living members and 200,000 attorney accounts a year by 2035, the firm needs about 215 people in landscape A and 320 in B, against about 900 for traditional firms doing the same estates. Of these, about 170 in A work on estates; the rest serve attorneys and will-making. The human share stays higher than in accountancy, because grief, capacity, family conflict and houses do not compress [conjecture].
8. **The architecture test.** [element] holds. [element], [element], [element], [element], [element], [element] and [element] bend. None breaks. The architecture needs four new elements: **a mandate chain with proof the world accepts**, **many-party neutrality inside one family**, **custody across decades**, and **pace set by the client** (section 9).

---

## 1. The client's outcome, segment by segment

### 1.1 What each party wants to be true

| Party | What they want true | When | Measure |
| --- | --- | --- | --- |
| **The living person** | "My affairs are in order. If I die or lose capacity, the people I chose can act at once. My wishes will be followed and understood. My family will not fight" | Continuously, for decades | Readiness score: share of the estate pre-routed net of reserves; will tested and current; powers registered; wishes recorded with reasons |
| **The bereaved family** | "We were not burdened. Money for the funeral and the household was there. We decided only what mattered. Nothing went wrong" | At death and for the weeks after | Family hours spent; days to first payment; decisions asked of the family; complaints |
| **Executors** | "I carry no personal liability. Someone competent is doing it. I chose them" | From death to discharge, and years after | Claims against executors (target nil); executors who keep the firm after death |
| **Beneficiaries** | "I know what I will receive and when. It is fair. I am paid on time" | From death to distribution | Days to first and final payment; disputes raised |
| **Counterparties** (banks, registrars, HMRC) | "We paid the right person and will not pay twice" | At death | Releases made without a grant; losses on those releases (target nil) |

Three points follow [reasoned]. First, **the outcome has two phases with different shapes**. During life it is a condition, held for decades. After death it is a finite project with a hard end. Pre-routing moves work from the second phase into the first, where it is cheap and the person can still be asked. Second, **"quickly" is not quite the outcome.** Families want control of pace. Some want everything done in a fortnight. Others cannot face the house for six months. The design makes speed available, not imposed. Third, **counterparties are parties with an outcome too**. They freeze accounts to protect themselves. Give them the protection another way and they stop freezing.

### 1.2 The segments

About 571,000 people died in England and Wales in 2025 [seen, ONS]. Roughly half of estates need a grant; the rest are small or jointly held and pass without one [seen, general knowledge; proportion not checked]. About half of adults have no will [seen, general knowledge; not checked], so most estates of people who are not members are intestate. Administrators under an intestacy have no authority at all until the grant [seen, practitioner review; general law].

| Segment | Share of deaths [conjecture, approximate] | What they want | What they get |
| --- | --- | --- | --- |
| **Small and joint estates, no grant** | about 45% | "Close it all, in days" | Automated settlement; a guide on call; often paid for by a bank partner |
| **Standard estates with a home** | about 40% | "Sell or transfer the house, share it fairly" | Fixed price with guarantee; a named guide; the house option |
| **Taxable estates** | about 6%, perhaps 10% once pensions count from April 2027 [reasoned from seen changes] | "Right tax, no personal risk" | Plus tax desk; tax known and reserved in life |
| **Complex or contested**: farm, business, trusts, blended families | about 7% | "Keep the business and the family together" | Senior adviser leads; mediation first |
| **The living** | Adults over 50; anyone at a life event; anyone whose parent has just died | "Sort it once; keep it current" | Readiness membership, free to them |
| **Attorneys and donors** | Growing with dementia | "Run Mum's money safely, and prove it" | The attorney's account: a main product, not an add-on |

**The real client is the household across two generations.** The parent buys readiness; the children receive the settlement; the children then become members. Today's market sells wills with no plan for what follows, and probate to strangers in shock [reasoned].

---

## 2. Where information is born and decisions are taken

### 2.1 Today

| Information | Where it is born | Where today's firm meets it |
| --- | --- | --- |
| **What the person owns, and its value at death** | Banks, pension schemes, Land Registry, platforms, insurers, online accounts | After death, by letter to each institution, from paperwork found in a drawer; valuation letters take weeks each |
| **What the person owes, including contingent claims** | Lenders, councils, utilities, HMRC, DWP, care providers, personal guarantees | By notification, waiting for claims, and a statutory notice. DWP benefit overpayment checks routinely hold up distribution for months [seen, practitioner review] |
| **Who gets what, and why** | The will, made years before; the person's head | The will is found in a drawer or a will bank. The reasons are found nowhere |
| **Where each asset goes at death** | Mostly nowhere: only pension wishes, life policies in trust and joint ownership carry a destination | Discovered asset by asset |
| **Lifetime gifts** | Bank records | Reconstructed from seven years of statements |
| **That the person has died** | The medical examiner; then the registrar | The family phones the firm, days or weeks later |
| **Who may act** | The will, then the grant | Every counterparty waits for the grant above its small-estate limit [seen, practitioner review] |

### 2.2 Decisions

The decisions are few: who acts; keep or sell the house; how to use the reliefs; when to distribute; whether to vary the will; whether to settle a claim. Today lay executors take most of them late and without data. Some are missed entirely, such as a deed of variation within two years [seen, general knowledge]. The most important decisions of all, where each asset goes and how the will reads in an awkward case, are best taken by the person while alive. Today almost nobody asks them [reasoned].

### 2.3 By 2035

Most of the information is born in systems that will be digital and readable with consent [reasoned, from seen trends]:
- **Pensions.** Pension dashboards connect all schemes to one finder service [seen: connection deadlines through 2026; public launch date not checked]. From 6 April 2027 schemes must tell personal representatives the value of benefits within four weeks of being told of a death [seen, HMRC technical note].
- **Money.** Open banking gives live balances during life with consent [seen]. Notification at death is partly shared: Tell Us Once for the state; the Death Notification Service for about 43 financial firms [seen, Which?].
- **The grant.** Digital probate applications average about four to five weeks to grant; paper takes about 16 [seen, ICAEW reports of HMCTS data, 2026].
- **Tax.** Where a full inheritance tax account is needed, the probate application waits for HMRC's code, normally within about 20 working days of the return or payment [seen, GOV.UK]. Excepted estates, which are most estates, skip this [seen, GOV.UK].
- **Land.** Title and price data are digital [seen].
- **The will.** Electronic wills are recommended by the Law Commission, with a draft bill (May 2025), but not enacted [seen].
- **Lasting powers.** Made online but still printed to register; a fully online service is being built under the Powers of Attorney Act 2023 [seen, GOV.UK].
- **Liabilities.** These are the weak point. Assets announce themselves; debts and contingent claims do not. The state's own data (DWP benefits, council tax) is readable in principle but not offered to anyone with consent today [reasoned].

**The design rule** [reasoned]: put the firm's capability at five points. **During life, in the person's accounts**, so the estate is known and pre-routed before death. **During life, in the will**, so its ambiguities are settled by its author. **At the moment of death**, as the first party told, by the person's own prior instruction. **At the decision moments**, with the family, with data. **In the money**, so that payments, reserves and accounts happen where the money moves.

---

## 3. What disappears, what becomes a side effect, what remains

### 3.1 The mechanisms [reasoned]

| Mechanism | What it replaces | Why it works |
| --- | --- | --- |
| **The estate pre-routed in life** | Asset collection; much of the grant's purpose; most distribution | Every asset carries a named destination that works at death without a grant: pension wishes, policies in trust, nominations and payable-on-death instructions where institutions offer them. At death most money moves directly, net of a reserve |
| **The liability record and reserve** | Waiting blind for creditors | Liabilities and contingent claims are recorded in life with consent (benefits, care contracts, guarantees, loans, tax). Each pre-routed asset releases net of its share of a reserve sized from the record. The reserve sits in the estate wallet until liabilities clear |
| **The will drafted as rules and tested in life** | Interpretation after death; construction disputes | One source, two renderings. The will is held as structured rules; the legal text is rendered from them and checked by a lawyer; the signed text governs. The rules are run against scenarios while the person lives: "your son dies before you; your house is sold before you die; your estate halves". The person chooses each answer, and the will is amended to say it |
| **Pre-authorised notification** | The family phoning institutions | The person instructs in life: "when I die, tell these firms, and offer my executors this firm" |
| **The indemnified release** | Waiting for the grant to collect money | For low-risk member estates, a rated insurer indemnifies the partner bank for releasing funds before the grant to the executors' estate wallet, on the firm's verified record of the will, the executors and the death |
| **The estate wallet** | Cheques; client account; reconciliations; estate accounts | One account in the executors' name at a regulated partner. The accounts are its history |
| **The safe share** | A year's wait for beneficiaries | Pays early the part of each entitlement that survives any plausible claim, tax bill or debt. Insurance covers process risks; family-provision risk is held back, not insured |
| **Executors' policies, set once** | Case-by-case approvals | "Sell the house unless a beneficiary wants it at valuation. Pay legacies at once" |
| **A view every beneficiary can see** | Letters, chasing, suspicion | Ledger, timeline and reasons are visible, so silence does not breed mistrust |

Two limits on pre-routing, built in [reasoned, with seen law]:
- **It does not escape what is owed.** Pension death benefits fall into inheritance tax from April 2027 with personal representatives liable [seen, HMRC technical note]. Family provision claims can reach nominated property and the deceased's share of joint property [seen, Inheritance (Provision for Family and Dependants) Act 1975, ss.8–9]. So every destination carries a reserve, and the reserve is the design, not a footnote.
- **Not every route is safe.** Joint ownership hands control and sometimes beneficial ownership to the joint holder, invites abuse and can be treated as a gift. Trusts of the family home carry tax traps if the person still lives there. The firm prefers nominations and payable-on-death instructions, which change nothing in life, and uses joint ownership or trusts only on advice [reasoned; seen, general knowledge].

### 3.2 Today's main work, line by line

| # | Today's work | Fate at level 3 | Why | What does what remains |
| --- | --- | --- | --- | --- |
| 1 | Taking instructions; finding the will | **Shrinks to a conversation about wishes and pace** | Facts and the tested will already in the record | Guide |
| 2 | Registering the death | **Remains with the family** (the informant's legal duty) | The firm books it; Tell Us Once follows | Family |
| 3 | Notifying institutions; finding assets | **Side effect; mostly disappears** | Pre-authorised notice; estate compiled in life; residual search only | Notification and asset agents |
| 4 | Finding liabilities | **Shrinks; remains as a wait** | Known liabilities in the record; DWP and late creditors still take weeks | Liability agent; reserve; insurance for the residue |
| 5 | Date-of-death valuations | **Side effect for money; remains for house and chattels** | Balances read at the date; a surveyor where tax turns on it | Valuation agent; RICS valuer |
| 6 | Inheritance tax return | **Side effect, with judgement left** | Estimate and reserve ran in life. Reliefs, gifts and pension tax need judgement | Tax engine; tax desk |
| 7 | Paying tax before the grant | **The wait disappears** | Direct payment from banks, released pension funds or bridging | Wallet agent; lending partner |
| 8 | Probate application | **Side effect, signed by an authorised person; often not needed for members** | A reserved activity [seen, Legal Services Act 2007] | Accountable officer |
| 9 | Waiting for the grant | **Remains for cold estates; blocks little for members** | Pre-routing and indemnified release; sale preparation in parallel | Registry agent |
| 10 | Collecting assets; notices; administration tax; estate accounts | **Side effects** | Money flows to destinations or the wallet; its history is the accounts | Wallet and tax agents; officer signs |
| 11 | Clearing and selling the house | **Remains: physical and emotional; with a new option** | Keys, empty-home insurance, the family choosing what to keep; a priced option to take or sell at valuation | Property coordinator; field partners |
| 12 | Distribution | **Mostly happens at death through destinations; residue computed** | Safe share early; final under policy | Wallet agent; officer approves final |
| 13 | Answering calls from family and beneficiaries | **Disappears as chasing; remains as care** | Everyone sees the same live view | Guide |
| 14 | Disputes | **Somewhat fewer, earlier, mediated** | Reasons recorded and will tested in life; transparency after death; caveats still possible | Mediator; partner litigators |
| 15 | Wills and lasting powers | **Drafting becomes rule-setting and testing; signing stays physical** | Two witnesses in person [seen, Wills Act 1837] | Will adviser; mobile witness network |
| 16 | Will storage | **Becomes custody, a lasting obligation** | See section 9 | Custody service |
| 17 | Digital life: photos, subscriptions, social accounts, crypto | **New, mostly agent work** | High volume, low skill, hated by families | Digital estate agent; guide on call |

About half of today's work becomes a side effect or disappears for a member; much less for a cold intestate estate. That is less than in accountancy, because death has a house, a legal clock, a grieving family and a signature in ink [reasoned].

### 3.3 The timeline that results [conjecture, 2035, standard estate with a house]

The first draft had one timeline. It was wrong for taxable estates and too smooth on liabilities. It now splits three ways.

| | Today (typical) | Ready member, excepted estate | Ready member, taxable estate | Cold estate, no will |
| --- | --- | --- | --- | --- |
| Funeral and household money | 1–4 weeks | Same day, through destinations | Same day | Days: banks pay funeral invoices directly [seen, general knowledge] |
| Assets known | 2–4 months | Hours | Hours | 2–4 weeks |
| Liabilities known, including DWP | Months | 4–8 weeks | 4–8 weeks | 2–3 months |
| Pre-routed money reaches beneficiaries, net of reserve | Not applicable | 1–2 weeks | 1–2 weeks | None |
| Probate applied for | 3–6 months | 1–2 weeks, or not needed | 6–8 weeks: return filed in 2–3 weeks, then HMRC's code [seen, GOV.UK] | 6–10 weeks |
| Grant | 4–16 weeks after application [seen] | 1–2 weeks | 1–2 weeks | 2–4 weeks |
| Safe share of residue paid | 9–12 months | 4–8 weeks | 3–4 months | 4–6 months |
| House sold or taken | 6–12 months | Weeks if a beneficiary takes it at valuation; else 2–4 months, unless the family chooses later | Same | 4–8 months |
| Final distribution | 9–15 months | 4–7 months (claims window runs) | 6–9 months | 9–12 months |

The headline is not the end date. It is that **for a ready member most money reaches beneficiaries in a fortnight, without a grant**, and **the family is asked to decide perhaps five things**. For a cold estate the gain is smaller: months, not weeks. That gap is the reason to be a member, and the children see it.

---

## 4. What appears that did not exist before

### 4.1 New products

1. **Readiness membership, free to the person.** A live estate and liability record, the will tested and kept current, destinations set for each asset, a running tax estimate and reserve, and a readiness score. Updated by life events the firm can see, not by an annual letter. Paid for by employers, banks, pension schemes and charities, who each have a lasting reason to pay [reasoned].
2. **The settlement guarantee.** A fixed price, dates for first and final payment, and **an indemnity for the executors** covering process errors, missing beneficiaries and late creditors, backed by an insurer. Family-provision risk is handled by holding back, not by cover. Executors keep control and carry no personal risk for the firm's work [reasoned].
3. **Executor support, never executor capture.** The family are executors with the firm doing the work. The firm acts as professional executor only where no one will, and never names itself sole executor in a will it drafts. Executors may leave at any time with the whole record exported. The guarantee is why they stay [reasoned].
4. **Pay-out in weeks.** Pre-routed destinations first, then the safe share, then bridging at cost plus a shown margin. Not the steep discounts some inheritance advance firms take [seen: such firms exist; rates not checked].
5. **The attorney's account.** A wallet with spending rules, an audit trail, alerts to a second attorney or a safeguarding officer, and the attorney's accounts as a side effect. Attorney abuse is a daily safeguarding concern [seen, practitioner review]. It is the family's way in at the moment they are already worried, and it carries the mandate chain from person to attorney to executor. By 2035 it may be the largest product by members [conjecture].
6. **The wishes record.** The person's own recorded explanation of why the estate is split as it is, shared after death as they chose. It persuades families more often than it persuades judges: in *Ilott v The Blue Cross* [2017] UKSC 17 a mother's letter of reasons did not prevent an award to her daughter [seen]. So its job is to prevent the dispute, not to win it.
7. **The house option.** An independent RICS valuation; any beneficiary may take the house at that value; otherwise a neutral partner offers a guaranteed purchase at a shown discount, or the family sells on the open market. Every fee is shown. A transparent, priced option is not a commission [reasoned].
8. **Digital estate closure.** Photos saved, subscriptions cancelled, accounts memorialised or closed, crypto found. A cheap first product for non-members [reasoned].
9. **The will proved in life** (from when the law allows). A court validates the member's will while they live, on the firm's capacity evidence; death triggers only identity and death checks [conjecture for England and Wales; seen in several US states].

### 4.2 New continuous conditions

- **The estate is routed**: share of value with a working destination, net of reserve.
- **The liabilities are known**: share of expected debts and contingent claims recorded.
- **The will is tested**: no untested scenario among the standard set; no life event since the last test unhandled.
- **Tax is not a surprise**: the inheritance tax estimate is within a stated band, and the reserve covers it.
- **Capacity evidence exists**: each will and power has a contemporary record of capacity and of the absence of pressure.
- **Someone can act tomorrow**: powers registered, attorneys briefed, executors verified, access arranged.

### 4.3 New data

Pooled across estates [reasoned]: time and cost by estate type (prices fixed fees); late-claim and late-creditor rates (prices the guarantee and sizes reserves); dispute risk factors such as a second marriage, an estranged child, a cohabitant or a carer child living in the house (tells the living person where a conversation, a provision or a gift now prevents a claim later); house exceptions such as subsidence, sitting tenants or an occupying sibling (priced before the guarantee); losses on indemnified releases (tells banks what the grant is really protecting them from); and which institutions are slow at death, which, published, becomes pressure [conjecture].

---

## 5. Where the firm's capability sits, and the boundary

### 5.1 By segment

The client's "world" is unusual here. During life it is the person's accounts, their will and their family. At death it is a kitchen table, a phone full of messages and twenty institutions that have frozen everything [reasoned].

| Segment | Agents and record | People | Where it sits |
| --- | --- | --- | --- |
| **Living members** | Linked to accounts by consent; destinations; will tests; prompts at life events | Will advisers; mobile signing and capacity network | In the person's accounts; in an employer's, bank's or pension provider's app |
| **Attorneys** | Wallet, rules and alerts | Safeguarding officer on exceptions | In the attorney's phone and the donor's bank |
| **Small estates** | Full automation | A guide on call | Inside the bank's bereavement flow |
| **Standard estates** | Estate agent; wallet; property workflow | Named guide; officer signs; property coordinator | In the family's phones; at the house |
| **Taxable, complex, contested** | Plus tax engine and evidence pack | Tax and senior advisers; mediators | With the family's other advisers, on a shared record |

**Embedded capability means something different here.** Nobody wants a person from the firm in their home at the worst moment, uninvited. And the first draft's idea of embedding in hospices and care homes fails twice: it looks like referral-farming at the deathbed, and care homes are often creditors of the estate [builder and practitioner reviews; reasoned]. The firm embeds instead **where people are well and already thinking about money**: employers' benefits, banks, pension schemes, charities' legacy programmes. And it is present at death **because the person chose it in life**, and told the institutions so.

### 5.2 The boundary choice

| Option | For this firm | Verdict |
| --- | --- | --- |
| **Own the platform** | A closed estate record and wallet | A record no bank or registry reads is worthless at death [reasoned] |
| **Build on a platform** | Legal case-management software | Built for files and letters; no live link to assets, no wallet [reasoned] |
| **Portable agent layer** | Agents in any bank's or provider's systems | Right for partners; owns nothing that lasts decades |
| **Open schema; owned custody, member relationship, guarantee and people** | Publish the estate record schema; contribute to a standard others lead; own the rest | **Chosen** |

**The recommendation** [reasoned]: **publish an open estate record schema and export everything in it**, so that executors, rival firms and the family's own AI can read it. **Contribute to, do not try to lead,** the shared standard. A shared UK finance standard tends to need a regulator's or the state's push; open banking needed a competition order [seen, CMA 2017]. UK Finance, the Death Notification Service and government hold this ground [seen]. The firm's role is to prove the schema works and lobby for it. **Own** what others cannot easily do: custody of wills and records for decades, the member relationship, the guarantee priced from pooled data, and the people. **Rent** banking rails, identity, insurance capacity, lending and the field network.

Why not own the platform, as the accountancy design does? Because the decisive moment is death, and at death the counterparties are dozens of institutions. A schema they can all read beats a platform they must join [reasoned]. And a firm that dies before its members needs their records to survive it (section 9.2).

### 5.3 Who else is in the picture

| Player | What they hold | How the firm stands |
| --- | --- | --- |
| **Solicitors and their will banks** | Stored wills; local trust; percentage fees [seen, general knowledge] | **Partner for contested work.** Buy will banks only cheaply: a will stored in 2004 belongs to someone who has moved twice; conversion is low [builder review] |
| **Consumer will-and-probate firms** (Farewill, owned by the funeral group Dignity [seen, TechCrunch]; Co-op Legal Services) | Brand; volume; funeral links; charity will schemes | **Rivals at level 1–2.** The funeral link is strong but conflicted; stay neutral of funerals |
| **Charities** | Free-will schemes funded by hoped-for legacies [seen, general knowledge] | **Main acquisition channel for wills.** Payment never buys a nudge: the gift prompt is neutral and the person's choice is recorded |
| **Employers** | Workforces in their fifties; benefits budgets | **Distribution partner** for readiness and attorney accounts |
| **Banks** | The money; bereavement teams; their own executor services [seen, practitioner review] | **Partner and rival.** Readiness for customers; small estates inside the bank's flow; indemnified release. They want fewer frozen accounts, because grieving customers leave [conjecture] |
| **Pension providers and advisers** | From 2027, a duty to inform personal representatives; members' attention | **Partners from 2028.** Slow to sign; expect 18 months [builder review] |
| **HMRC, HMCTS, OPG, Land Registry, DWP** | Rules, grant, powers, liabilities | Build to their channels; seek trusted-filer status; ask for consented liability reads |
| **The family's own AI** | A capable assistant in every executor's phone by about 2030 [conjecture] | Give it the schema; sell what it cannot: liability, money, signatures, care, custody |

The 2035 contest is between **whoever is told first at death and trusted to act**: the bank, the funeral group or a neutral firm the person chose in life. The firm's answer is to be chosen in life, and to be chosen again by the executors because of the guarantee [reasoned].

---

## 6. The organisation

### 6.1 The agent architecture

| Agent | One per | Sole writer of | Job |
| --- | --- | --- | --- |
| **Person agent** | Living member | Estate and liability record; destinations; readiness | Keep links live; spot life events; keep the tax estimate and reserve; run will tests; flag pressure or capacity concerns to people |
| **Attorney wallet agent** | Donor | The donor's spending rules and audit trail | Enforce rules; alert on anomalies; produce attorney's accounts |
| **Estate agent** | Estate | Plan and state | Orchestrate from death to discharge; ask the family only what policy does not cover |
| **Wallet agent** | Estate | The money | Collect, reserve, pay, distribute, produce accounts |
| **Asset, liability, tax, property and digital agents** | Institution; estate; house | Their cases | Notify, value, close; find and clear debts; compute and file tax; run clearance and sale; close digital life |
| **Beneficiary agents** | Beneficiary | That person's view | Explain what they get and when; never see others' private data |
| **Counterparty agents** | Registry, HMRC, OPG, DWP, partner banks | Their cases | File, watch for caveats, answer, present proof of authority |
| **Verifiers, safeguarding, governance** | Output type; firm | Nothing | Recompute on other models; check rules against the signed will; watch for coercion and fraud; budgets, limits, breakers |

Constitution clauses specific to this service [reasoned]:
1. **The person's wishes rule, within the law.** Not the executors' convenience, not the firm's, not the payer's.
2. **Every beneficiary is owed the truth.** The firm acts for the executors, but no beneficiary is misled or kept in the dark about their own entitlement.
3. **Pace belongs to the family.** Speed is offered, never pressed. No nudges to sell the house.
4. **No commission from funerals, house sales or advances** that could bend advice; every priced option and fee is shown. A payer of membership, such as a charity, buys no influence over the will.
5. **The signed will governs.** Rules never stand apart from it; any difference stops distribution.
6. **Executors choose.** The firm never makes itself hard to leave.
7. **Custody outlives the firm.** Records and wills are held so that they survive the firm's failure.
8. **When in doubt about capacity or pressure, stop and send a person.**

### 6.2 The people, by kind of need

| Kind of need | Roles | Notes |
| --- | --- | --- |
| **1. Purpose** | Owners and board, with an independent member for families | |
| **2. Definition of good** | Head of estates law; tax lead; actuary and underwriting lead; safeguarding lead; family experience lead | The family experience lead owns tests for tone, pace and burden, not only correctness |
| **3. Answerability** | Accountable officers authorised for probate; client money officer; data officer | They sign grant applications, estate accounts and rule-to-will checks |
| **4. Capability gaps** | Judgement desk: reliefs, trusts, overseas assets, insolvent estates, ambiguous wills, intestacy, liabilities | Shrinks with capability, slowly, because cases are varied |
| **5. Client demand for a person** | **Bereavement guides**, one named per estate; will advisers for complex lives | Families want a person, but most want one decisive conversation and reliable updates, not hours of contact [seen, practitioner review]. Time is available, not budgeted for all |
| **6. The physical world** | Property coordinators; mobile witness and capacity network; clearance, keys, valuers and estate agents as partners | Mostly outside the firm |
| **7. Conflict** | Mediators; dispute lead; partner litigators | Permanent; a family dispute is not a capability gap |
| **Scaffolding** | Builders; human checkers; trainees | Checkers go as evidence allows; pension tax checked by people longest |

### 6.3 Rhythm

Deaths arrive daily, with a winter peak [seen, general knowledge]. **Daily:** each new death gets a guide within hours and a first call when the family is ready; destinations release; caveat searches run. **Weekly:** estates past promised dates; disputes forming; liability checks outstanding. **Quarterly:** the actuary reprices the guarantee and reserve rules; model releases go through the test harness. **At each Budget:** every member's tax estimate, reserve and will test set are recomputed overnight.

### 6.4 Headcount sketch [conjecture]

Volume assumed: 2027, 600 cold estates and a few thousand members through charity wills; 2030, 4,000 estates, 250,000 members and 40,000 attorney accounts; 2035, 12,000 estates (about 2% of deaths, about 55% from members), 1 million members, 200,000 attorney accounts and about 60,000 wills and powers made or changed a year. Guide hours budgeted at about 15 per estate in 2027 and 6 (A) to 9 (B) by 2035: about 4 for a ready member, 10 for a cold estate.

| Role | 2027 | 2030 A | 2030 B | 2035 A | 2035 B |
| --- | --- | --- | --- | --- | --- |
| Owners, board, accountable officers | 6 | 9 | 10 | 14 | 20 |
| Standard-setters (law, tax, actuary, safeguarding, experience) | 5 | 7 | 8 | 8 | 9 |
| Judgement desk (including intestacy and liabilities) | 6 | 14 | 20 | 20 | 36 |
| Bereavement guides | 7 | 25 | 34 | 55 | 83 |
| Tax desk | 2 | 6 | 9 | 10 | 16 |
| Property coordinators | 3 | 9 | 13 | 16 | 26 |
| Mediators and dispute lead | 1 | 5 | 6 | 12 | 15 |
| Will advisers (complex) | 3 | 10 | 14 | 25 | 38 |
| Safeguarding and attorney exceptions | 1 | 7 | 9 | 20 | 28 |
| Builders | 14 | 14 | 18 | 10 | 16 |
| Human checkers (scaffolding) | 5 | 5 | 9 | 0 | 6 |
| Partnerships and distribution | 3 | 7 | 7 | 10 | 10 |
| Operations, complaints, client money | 3 | 6 | 7 | 8 | 10 |
| Trainees | 2 | 5 | 5 | 8 | 8 |
| **Inside the firm** | **61** | **129** | **169** | **216** | **321** |
| *Outside: witness and capacity network, valuers, clearance, estate agents* | *partners* | *partners* | *partners* | *partners* | *partners* |

| Traditional firms at the same estate volume [conjecture] | 2027 | 2030 | 2035 |
| --- | --- | --- | --- |
| Estates (about 50 fee-earner hours each, 1,300 hours a year, plus support at 1:1) | about 45 | about 300 | about 900 (including wills) |
| **Level 3** | 61 | 129 / 169 | 216 / 321 |

### 6.5 What drives the numbers [reasoned]

1. **Warm against cold estates.** A pre-routed member's estate is mostly settled before anyone opens a file; a stranger's intestate estate is not. Cold estates are the volume until about 2032 and fund the firm. In 2027 level 3 needs more people than a traditional firm, because of builders and cold estates.
2. **Guide hours per estate.** Cut after review: families can have more, but most do not use it. Still the largest line.
3. **The attorney's account.** With will advisers, it adds about 45–65 people by 2035, mainly safeguarding and advice to the living. Without them, the estate side is about 170 in A, not far from the builder's estimate of 150.
4. **The review rule.** If insurers and regulators accept sampling plus independent recomputation for grant applications and accounts, checkers go. If not, the B column holds in A.
5. **Dispute rate.** If the wishes record, will testing and transparency cut disputes by about a quarter, as the practitioner expects, mediators stay near the figures above. The first draft's halving was too hopeful.
6. **Physical work sits outside.** Counting partners' people would add perhaps 100–200 full-time equivalents by 2035; traditional firms also outsource most of it.

**The honest point.** The ratio to traditional (about 1:4 in A, 1:2.8 in B) is less dramatic than in accountancy. The human core here is care, conflict and capacity, which do not compress. The gain is mostly in what families experience: a fortnight not a year, five decisions not fifty letters, no personal risk.

---

## 7. Economics [conjecture throughout]

### 7.1 What is sold and how it is priced

Baseline: traditional probate fees are often £3,000–£15,000, or 1–5% of the estate; bank executor services often charge a percentage with a minimum [seen, general knowledge; not checked]. Probate application fees are £300 for estates over £5,000 (reported to rise to £526) [seen in part; not checked].

| Product | For | Paid by | Price, 2027 |
| --- | --- | --- | --- |
| **Readiness** | Living members | Employer, bank, pension provider or charity | Free to the person; £15–30 a year per member to the payer |
| **Will and powers** | Members | Charity scheme or the person | Charity-funded for simple; £400–1,200 for complex wills with trusts |
| **Small estate settlement** | No grant | Bank partner or family | £300–600 |
| **Standard settlement with guarantee** | Grant, home, no tax | Estate | £2,500–3,500 fixed for cold; £1,200–2,000 for members |
| **Taxable settlement** | IHT estates | Estate | £5,000–12,000 fixed by band |
| **Complex** | Business, farm, trusts | Estate | Fixed quote from the record |
| **House exceptions** | Subsidence, tenants, hoarding, an occupying relative | Estate | Priced from the record before the guarantee is given |
| **House option, digital closure** | Estates that choose them | Estate | Shown fees |
| **Pay-out in weeks** | Beneficiaries who choose bridging | Beneficiary | Cost of funds plus a shown margin |
| **Attorney's account** | Attorneys | Donor | £4–6 a month |
| **Professional executor** | Where no family member will act | Estate | Fixed, plus an annual fee for trusts |

**Pricing logic** [reasoned]. Never a percentage of the estate: it bears no relation to work and families resent it. Price the guarantee and the person. Price the messy house as an exception, or the clean estates pay for it and leave. Members get a lower settlement price because their estate is cheaper to settle. The membership is paid by someone with a lasting reason: a charity's legacy income, an employer's benefits budget, a bank's or pension provider's retention.

### 7.2 Revenue, cost and margin

| | 2027 | 2035 A | 2035 B | 2035 D (price collapse) |
| --- | --- | --- | --- | --- |
| Estates | 600 | 12,000 | 12,000 | 12,000 |
| Average settlement fee | £3,800 | £2,400 | £2,900 | £1,000 |
| Settlement revenue | £2.3m | £28.8m | £34.8m | £12.0m |
| Members (paid by partners; average £15 a year) | £0.1m | £15.0m | £15.0m | £8.0m (at £8) |
| Attorney's accounts | £0.0m | £10.0m | £10.0m | £6.0m |
| Wills and powers | £0.3m | £6.0m | £6.0m | £3.0m |
| House option and digital closure fees | £0.1m | £3.0m | £3.0m | £2.0m |
| Bridging margin | £0.1m | £3.0m | £3.0m | £2.0m |
| **Revenue** | **£2.9m** | **£65.8m** | **£71.8m** | **£33.0m** |
| People (loaded £75,000–78,000) | £4.6m | £16.2m | £25.0m | £14.3m (cut to about 190) |
| Model use and verification | £0.2m | £1.5m | £2.0m | £1.2m |
| Insurance for the guarantee and indemnified releases | £0.2m | £3.0m | £3.6m | £3.0m |
| Banking, identity, data and partner fees | £0.3m | £3.5m | £3.5m | £3.0m |
| Custody and compliance | £0.2m | £1.5m | £1.5m | £1.5m |
| Acquisition (charity and employer partnerships, distribution) | £1.0m | £7.0m | £7.0m | £5.0m |
| **Cost** | **£6.5m** | **£32.7m** | **£42.6m** | **£28.0m** |
| **Margin** | **about −125%** | **about 50%** | **about 41%** | **about 15%** |

### 7.3 What the numbers say

- **The early years are deep losses**, because the asset is a membership book whose payoff comes when members die. Cold estates carry the firm until about 2032 [reasoned].
- **Pre-routing cuts the firm's own fee per estate**, and that is the point. The average settlement fee falls from the first draft's £3,000 to £2,400 in A. Revenue moves to partner-paid membership and attorney accounts, which recur [reasoned].
- **In D the firm now survives**, because about half its revenue no longer depends on settlement work. If families' own AI can do probate, the firm sells custody, attorney safeguarding, liability cover, the guide and the member book. The first draft lost money in D; this one makes a thin margin [conjecture].

### 7.4 Where profit comes from

1. **Warm estates.** A member's estate costs perhaps a third of a cold one to settle; that gap is margin.
2. **Recurring revenue during life**: partner-paid membership and attorney accounts.
3. **The guarantee**, priced from pooled late-claim, valuation and process-error data.
4. **The children.** Every settlement puts the firm in front of three to five adult children at the one moment they think about their own wills [builder review]. It is the cheapest acquisition there is.

**Not from:** percentages of estates, funeral commissions, house-sale kickbacks or influence sold to payers. Each would destroy the trust that membership needs [reasoned].

---

## 8. How it is built from 2027

### 8.1 The first wedge: standard cold estates, pension-aware from day one

The first draft led with a pension product sold through pension providers. Both reviewers liked the timing; the builder warned it pulls a young firm into the heaviest liability with an untested engine, through slow partners. The redesign keeps the timing and changes the channel [reasoned].

From 6 April 2027, unused pension funds and death benefits fall into the estate for inheritance tax, and **personal representatives are liable** for reporting and paying it, with beneficiaries jointly liable once benefits vest [seen, Finance Act 2026; HMRC technical note]. Schemes must report values within four weeks; personal representatives can direct schemes to withhold and pay [seen]. So **every estate with a pension after April 2027 needs pension handling**, whoever its channel. The wedge cannot avoid pensions; it can avoid selling them first.

The wedge [reasoned]:
- **Product:** a fixed-price standard settlement with executor indemnity, sold direct, with pension tax handled inside each estate and checked by people. Plus digital closure as a cheap entry product.
- **Channel:** direct, and through charities' free-will schemes for the living.
- **Then, from 2028:** a "pension-aware settlement" sold through pension providers and advisers, once the tax engine has a record across a few hundred real estates.
- **Why now:** pension inheritance tax is new, the liability is personal and frightening, and nobody has built for it.

The second pressure point is the April 2026 relief changes for farms and businesses: a £2.5m allowance for 100% relief, 50% above it [seen, GOV.UK]. Families with farms and companies need their estate known, routed and planned in life.

### 8.2 Adoption

Readiness is hard to sell: people avoid thinking about death, and about half of adults have no will [seen, general knowledge; not checked]. People do not pay monthly for a thing they want to forget; they act once, at a trigger [builder review]. So [reasoned]:
- **Make it free to the person**, paid by employers, banks, pension schemes and charities.
- **Make the children the engine.** Every settlement ends with an offer to each adult child: your own readiness, free, and your parents' if still living.
- **Enter through the attorney's account.** When a parent's capacity starts to fail, the family is already engaged and worried. The account protects the parent now, and pre-routes the estate later.
- **Sell at life events**: retirement, a diagnosis, a house sale, a pension drawn.

### 8.3 Sequence [conjecture for dates]

| Period | Moves |
| --- | --- |
| **2027** | Licensed as an alternative business structure with authorised probate practitioners. Estate wallet with a bank partner. Executor indemnity with an insurer. 600 cold standard estates sold direct, pension-aware. Charity will scheme. Digital closure |
| **2028–29** | Pension-aware settlement through one provider. Attorney's account launched. Employer distribution. Publish the estate record schema. Indemnified release pilot with one bank for member estates. HMRC and registry channels in use |
| **2030–31** | Destinations for members wherever institutions offer them; lobby for statutory nominations and consented DWP liability reads. Seek trusted-filer status. Contribute to whatever shared estate standard the state or UK Finance leads. If electronic wills are enacted, move members to them |
| **2032–35** | Most estates warm. Ready members paid mostly within a fortnight. Argue for a will proved in life, using a decade of capacity evidence. The attorney's account becomes a main product as dementia rises |

---

## 10. What would make this design wrong, and the stress test

### 10.1 What would make this design wrong

1. **People will not prepare for death**, even free. If readiness stays below a few per cent of older adults, most estates stay cold and the firm is a good level 2 probate firm with a wallet [reasoned].
2. **Institutions will not offer destinations.** If banks and platforms do not offer payable-on-death instructions or nominations, and the law does not add them, pre-routing stops at pensions and policies, and the grant stays central [reasoned].
3. **Banks or funeral groups capture the moment of death**, are told first and offer settlement free. The firm becomes their supplier [reasoned].
4. **The family's own AI does probate well and free** (landscape D). Only liability, care, custody and safeguarding remain worth paying for [conjecture].
5. **Insurers will not back indemnified releases or the executor indemnity** at an acceptable cost until years of data exist [reasoned].
6. **A correlated error**: one misreading of pension tax repeated across a thousand estates, with executors personally liable [reasoned].
7. **Pre-routing is abused**: a coerced change of destination moves an older person's money with no court in the way [reasoned].
8. **Disputes do not fall** despite will testing, wishes records and transparency [reasoned].

### 10.2 The stress test against today's rules and institutions

| Fact | Effect on the design |
| --- | --- |
| **Probate activities are reserved** under the Legal Services Act 2007; will writing is not [seen] | Authorised persons sign grant applications; licensed body from day one. The firm holds will writing to the regulated standard to protect validity |
| **Wills must be signed and witnessed in person** [seen, Wills Act 1837]; temporary video witnessing ended in January 2024 [seen, general knowledge]; electronic wills recommended but not enacted [seen, Law Commission 2025] | A mobile signing and capacity network is needed until reform. The rules and the text come from one source; the signed will governs |
| **Executors have authority from death, but counterparties ask for the grant above small-estate limits; administrators have none until the grant** [seen, practitioner review] | The wallet does not fill early by itself. Pre-routing avoids the grant; indemnified release pre-empts it for members; cold intestate estates wait |
| **A full inheritance tax account means waiting for HMRC's code, normally within about 20 working days, before applying for probate**; excepted estates skip this [seen, GOV.UK] | Timeline split by tax status (section 3.3). Taxable estates are six to eight weeks from death to application at best |
| **Inheritance tax is generally due before the grant**, with interest from the end of the sixth month [seen, general knowledge] | Direct payment from banks; released pension funds; bridging through a regulated lender; the tax reserve held in life as a known figure |
| **Pensions enter the estate from April 2027**; personal representatives liable; schemes report within four weeks [seen] | Pension handling in every estate from day one, checked by people; sold through providers only from 2028 |
| **Family provision claims** can be brought within six months of the grant and can reach nominated and joint property [seen, Inheritance (Provision for Family and Dependants) Act 1975, ss.4, 8–9] | Pre-routing does not escape them. Early payment is the safe share; family risk is held back, not insured |
| **Anyone can enter a caveat**, for a small fee, blocking the grant for six months, renewable [seen, practitioner review] | Daily caveat searches; mediation at once. A will proved in life would blunt this |
| **Creditor protection** depends on statutory notices and a waiting period [seen, Trustee Act 1925, s.27]; DWP overpayment checks take months [seen, practitioner review] | Notices issued as a side effect; liability reserve; insurance for the late-creditor residue |
| **Professional executor appointments** have a poor reputation where will writers used them to lock in fees [seen, practitioner review]; a wish that a firm act is not binding [seen, practitioner review] | The firm never names itself sole executor; executors may leave with the full record; the guarantee is the reason to stay |
| **Client money rules** for regulated firms are strict and under review [seen, SRA] | Hold no client money. Wallets are in the executors' or attorney's name at a bank partner; the firm has a mandate |
| **Grant times**: digital about five weeks; paper about sixteen [seen, ICAEW reports of HMCTS data] | Digital only; parallel work makes the wait mostly harmless |
| **Data protection** covers living people; the deceased's data largely falls outside UK GDPR, beneficiaries' does not [seen, general knowledge] | Consent in life governs; after death each beneficiary sees only their entitlement |
| **Bridging and advances** are credit [seen, general knowledge] | Through an FCA-authorised partner at shown prices |
| **Lifetime validation of wills** exists in several US states: North Dakota (1977), Ohio (1978), Arkansas (1979), Alaska (2010) and others since [seen, ACTEC Foundation; Porter Wright, 2021]. No such route in England and Wales [seen, general knowledge] | A 2030s law reform target, argued from the firm's capacity evidence; not in the plan before then |
| **Statutory nominations** in England and Wales are narrow, limited to small sums in certain societies [seen, general knowledge; not checked] | Destinations rely on what institutions offer voluntarily until the law widens them |
| **Adoption**: about half of adults have no will [seen, general knowledge] | Free to the person; children and attorney accounts as the way in |

### 10.3 What the stress test changes

1. **Not the core design.** The record in life, destinations, the tested will, the wallet, the guarantee and the guide survive today's rules.
2. **The grant moves from the critical path to the edge, for members only.** For cold intestate estates it stays on the path; that is why they cost more and why membership matters.
3. **The legal clocks become floors**, bridged with destinations, reserves and the safe share rather than removed.
4. **The ink signature stays on the critical path for wills** until electronic wills are law, so a field network stays in the plan.
5. **Law reform is part of the product plan**, not a hope: statutory nominations, consented liability reads, a will proved in life. Each removes a wait that no amount of agent capability can.

**Where this is weakest.** Every figure is conjecture. Five unknowns decide whether it works: whether people will join readiness in numbers, even free; whether institutions will offer destinations; whether insurers will back indemnified releases; whether a shared estate standard forms under someone else's lead; and whether disputes fall at all. The first and third can be tested within two years.

---

## Sources checked in this run

- Deaths: ONS, *Death registration summary statistics, England and Wales: 2025* (570,988 deaths).
- Grant times: ICAEW regulatory news, *HMCTS update for probate firms*, June and October 2026; MoJ quarterly Family Court statistics, Q1 2026.
- Inheritance tax account and probate timing: GOV.UK, *How to value an estate for Inheritance Tax and report its value* and *Applying for probate: before you apply* (wait for HMRC's code; excepted estates may apply at once); HMRC trusts and estates newsletter, December 2021 (allow 20 working days).
- Pensions and inheritance tax from April 2027: GOV.UK policy paper and HMRC technical note on inheritance tax on pensions; ICAEW, May 2026; Farrer & Co; Shoosmiths on Royal Assent of Finance Act 2026.
- Agricultural and business property relief: GOV.UK press release, 23 December 2025 (£2.5m allowance); HMRC manual IHTM25510.
- Wills reform: Law Commission, *Modernising Wills Law* (Law Com No 419), May 2025, with draft Bill.
- Lasting powers: GOV.UK guidance (make online, print to register); Gazette notice on the move to a fully online service.
- Death Notification Service: UK Finance launch release (2018); Which? on coverage (about 43 firms).
- Farewill: TechCrunch, October 2024, on acquisition by Dignity.
- Ante-mortem probate in US states: ACTEC Foundation podcasts on ante-mortem probate; Porter Wright, *Probate & Property*, March/April 2021 (list of states); Financial Advisor magazine on Alaska's 2010 statute.
- *Ilott v The Blue Cross* [2017] UKSC 17; Inheritance (Provision for Family and Dependants) Act 1975, ss.8–9 (stated from general knowledge of the statute; text not re-checked).
- Open banking: CMA retail banking market investigation order, 2017 (general knowledge).
- Stated as general knowledge or reviewer experience and not checked: share of estates needing a grant; traditional fee levels; share of adults without a will; inheritance advance pricing; video witnessing end date; statutory nomination limits; caveat fees and duration; bank small-estate practice; DWP overpayment delays; charity free-will schemes.
