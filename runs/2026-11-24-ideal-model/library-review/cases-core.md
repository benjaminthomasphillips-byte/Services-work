# What the library's researched cases offer the design

Claude, 24 November 2026. Read-only review of the Cases collection in the Thoughts Library (Notion), excluding the Pluris collection. Nothing in Notion or in the design files was changed.

## What I read

- **Titles of all 200 non-Pluris Cases:** B1 to B33, F001 to F046, and the N-series. The N-series runs past N076: N078 to N104, N110 to N125, N127 and N128 were added from the 23 November sweep. N077, N105 to N109 and N126 do not exist.
- **Bodies of 50 records, read in full:**
  - N001, N003, N004, N005, N015, N016, N018, N024, N040, N044, N045, N048, N050 to N053, N058 to N062, N065, N067 to N069, N071, N073, N078 to N081, N086, N088, N110, N113, N123, N124, N127;
  - F004, F013;
  - B2, B3, B7, B15, B16, B17, B23, B25, B29, B33.
- **Read in part:** N045 is the record in full, but its source paper only through the abstract.
- **Not read:** all other F-numbered profiles (F001 to F003, F005 to F012, F014 to F046), and the remaining B and N records.
- **Design files:** architecture-v1 and step 4 read in full; step 1 skimmed.

**How reliable the evidence is:**
- Every B and F record I read is "Imported unverified", except F004 and F013, which are "Imported then refreshed; not independently verified".
- **B17 and B23 cite checkpluris.com.** Treat them as Pluris promotional material.
- Most N records are "Sources read; not independently verified". Almost every operating figure in them is a company's own claim.

**Labels used below:**
- **[claim]** the company says it;
- **[observed]** a filing, regulator or study reports it;
- **[hypothesis]** an analyst's or author's reading;
- **[proposal]** a practice someone recommends but nobody reports using;
- **Inference** my own reading, not the record's.

**What the design already uses.** Of these records, the architecture and base design already cite Dwelly, Crosby, Talentsconnect, Cars24 and Deel. The step-1 engine already covers:
- deferring reviewers;
- adversaries who adapt;
- the review cost as a floor.

The level-3 worked examples mention Garfield and Awaab's Law. Everything else below is new to the core design.

---

## 1. Useful material the design does not yet use

**1.1 A deployment-and-adoption function is missing from the five layers (step 4, §2.1).**
- N060 [hypothesis, interested party]: Long Lake names three walls for AI deployed from outside a business: "getting to production", "driving adoption" and "capturing the value created".
- N060 says freed capacity "becomes P&L impact only when management puts it to work". It funds a separate "deploy (adoption and ops)" team alongside "buy" and "build".
- N016 [claim, implementer marketing]: a tool "built in one day" was refused by the owner until "months of in-person work".
- N071 [claim, CEO interview]: engineers "in your office for the next 2 years" and "a two-to-five-year transformation".
- N088 [claim, second-hand]: Revin puts forward-deployed staff "under product, not engineering", paid on renewals.

Inference: the base design has Builders and an Academy but no layer whose job is to turn capacity into volume or service. That matters most under **Ways to grow → Buy firms / Buy books** (step 4, §8).

**1.2 Where the saving lands, as a test for G4, G13 and the margin columns (architecture §6).**
- N051 [hypothesis, Chroma]: in demand-constrained businesses "cheaper delivery resets customer price expectations and the savings flow downstream"; in supply-constrained ones they "become volume".
- N061 [hypothesis, interested party]: "Every buyer can automate invoicing … an owner … might be better off renting the software and keeping the business."
- N081 [claim, no AI, vendor blog]: a tax firm cut work volume about 75% and revenue about 15%, and kept owner earnings, purely by repricing to subscriptions.

Inference: the margin figures in the seven designs (for example accountancy ~31% in landscape A) do not separate gains from AI, from repricing and from consolidation. N081 is the control case for that split.

**1.3 Retaining or losing the people whose knowledge the system needs (G9; step 4, §4 "Acquired staff").**
- N003 [observed via BBC/Bloomberg]: Ford rehired "more than 300 'veteran'" engineers. Its executive said "Mistakenly, we thought that by just introducing artificial intelligence and ingesting the design requirements … that would produce a high-quality product." The rehired staff "train the systems and mentor younger workers".
- N073 [claim]: Supa's sellers "do not stay involved after the sale".
- N071 [claim]: Long Lake's founders "rolled over significant equity".

Inference: G9 is about growing future judges. These cases add a first-year risk: losing the current ones before their knowledge is captured. Seller rollover and retention terms are therefore a design variable on the acquisition route.

**1.4 Regulators have already set review rules: the design's "biggest unknown" is partly known (G5; step 4, §2.4).**
- N069 [observed, search summary only]: a trust call-off under an NHS teleradiology framework "required audit of at least 5 percent of reports by independent GMC-registered consultants". The £300m national framework's Lot 1 is "Teleradiology Reporting Services (Outsourced and AI Assisted)".
- N065 [observed via trade press]: the SRA authorised Garfield.Law with "named solicitors accountable and no case-law proposals permitted".
- N067 [claim, site]: Crosby says "Human attorneys review all work", with malpractice cover.

Inference: in some sectors, existing procurement terms and regulator conditions already set the review rule, and they can be collected now rather than negotiated from nothing in 2027.

**1.5 Statutory clocks as the "condition kept true" in lettings (G4, G11, G1).** N068 [observed, government guidance] sets out Awaab's Law:
- "investigated and made safe within 24 hours";
- significant hazards investigated "within 10 working days";
- a written summary "within 3 working days";
- safety work "within 5 working days";
- the clock starts when "any part of the landlord or its agent becomes aware";
- records support the "all reasonable steps" defence.

The government's own research names "surveyor and specialist trades" shortages and "slippage between inspection and remedial works" as the main causes of delay.

Inference:
- This is a ready-made legal form for "the home is dry and legal".
- It makes G1's add-only record a statutory defence, not just good practice.
- It confirms G11: field capacity, not coordination, is the constraint.

**1.6 Payer-funded pricing set by law (G7, parameter "who pays").**
- N062 [claim, sell-side CIM supplied by owner]: at Debtist "delinquent customers pay the standard market costs".
- N065 [observed, site]: Garfield charges "£2.00" a chaser. If the claim succeeds, costs are recovered from the defendant at CPR Part 45 rates.

Both are structures in which a third party's statutory price funds the service. Architecture §5 has no named parameter for that.

---

## 2. Counter-opinions and challenges

**2.1 "Redesign, do not automate" and the 2027 start: owners report that agents break on judgement-heavy multi-step work.**
- N015 [claim, owner letter]: after a PhD AI lead and "dozens" of experiments, "results have been shockingly poor compared to expectations". Multi-step tasks needing "modest judgement 'often break or become stuck'". The firm is "pulling back".
- N045 [observed, peer-reviewed benchmark]: failure rates of 41 to 87% across seven multi-agent frameworks. The authors say "simple fixes are still insufficient".
- N086 [claim, first-hand failures]: "Verification now takes longer than building". The agent's "self-reports came back wrong four separate times in a single session".

**Strength: moderate.**
- These do not refute the architecture.
- They do challenge step 4 §8's assumption that the first promise can be met for design partners in 2027.
- They also challenge step 4 §2.3's sense that agent positions can be created on evidence quickly.
- N053 [proposal] offers the remedy: re-test failed uses with each model.

**2.2 People in the loop may not be an independent check (G5 named person; principle 8).**
- N018 [observed, Anthropic RCT, secondary summary]: analysts "chose the agent's lean 86% of the time (chance 50%)"; "77% repeated the agent's argument"; "15% credited the agent".
- B33 [claim]: judges trained on two years of founder decisions learn "what is usually approved, not what works for customers".

**Strength: strong for the judgement desk.** Step 1 already notes deferring reviewers. But step 4's sizing of the judgement desk and of review assumes that a person's sign-off adds independent information.

**2.3 Autonomy that passed every test failed against people who adapted (G8; engine "autonomy is a dial").**
- N079 [claim, anonymous, weakest evidence]: a refund agent "passed every test". Then "Customers learned how to phrase requests to trigger autonomous approval. Refund fraud crept up 4x. The cost of the fraud exceeded the labor savings." It was withdrawn after three months, and supervised approval is "still in production".
- B29 [observed, institutions]: AI-flagged complaints in US federal courts rose from near zero to 18%, with "wins under 1 percent". The Financial Ombudsman receives "200-page" submissions answering a "six-page decision".

Inference:
- Test suites built from past cases (engine) cannot include counterparties who learn the firm's agent.
- Opponents' AI also creates demand the firm must absorb (G11, claims and legal).

**Strength: moderate**, because the key case is anonymous.

**2.4 Size from measured exceptions, not announced savings (G5).**
- N001 [observed, union and broadcaster]: Commonwealth Bank reversed 45 redundancies. It said it "should have been more thorough in our assessment of the roles required". Call volumes rose after the bot.
- N004 [observed, filings]: Klarna's assistant reached 80% of chats, but the CEO later said cost had been "too predominant an evaluation factor". The outsourced human tier, staffed for the easy work, had to be repriced as premium.

These support G5's measured sizing. They cut against any plan, including acquisition models, that counts savings before demand has been observed over a full cycle.

**2.5 Generalist pods versus specialist judgement (step 4, §2.2 matrix).**
- N113 [claim, CEO at a financing]: Bird fell from more than 1,000 staff to 120. Its rule was "If you had very high performance but you were not multidisciplinary, you would not stay."
- N110 [claim]: Mercari's one-person "AI Pods" fell short: "in design, QA … AI alone sometimes did not reach sufficient quality".

The records disagree. Both can hold if specialists write the frameworks that generalists apply (N113).

**2.6 Conflict risks already present in the closest rivals (G7).**
- F004 [claim, job posting]: Dwelly's maintenance function targets "contractor-commission revenue". This is the revenue line G7 forbids and that Supa (N073) says it gives up: "contractor costs passed on at cost, any commission … disclosed".
- N062 [claim, CIM]: Debtist holds collected client money "with a planned DPO of 80 days, funding the business". That breaches G2's "earns nothing from holding money".
- N062 also says its voice AI "deliberately introduces a delayed response to appear more human-like".

These are not challenges to G7. They show the architecture's conduct rules would be a real point of difference against these rivals, and that rivals may undercut on price by breaking them.

**2.7 Ownership is not established as the cause (step 4, §7 and §8 "Buy firms").**
- B15 and N071 [claim]: organic growth went from "0-5%" to "20%+". The records note this "does not isolate AI from management and commercial investment".
- N059 [claim]: EBITDA "doubled" in under two years. The figure appears only in an X post, with the cohort undefined.
- N127 [observed, working paper]: AI-native start-ups are "25% smaller", with about "15% lower shares of entry-level workers and managers". The gaps are "largest in industries where the pre-AI workforce delivered services", and come mainly where AI is built "into what the firm sells".

Inference: the product route (C8, the platform) may account for more of the headcount gap than the operating route does.

---

## 3. Specificity the records could add

**Engine (step 1; step 4 §5, §6.3):**
- **Shadow mode before go-live**: agents run against staff postings first, and "approvals and payment release stay with staff under authorisation limits". Varick also agrees a baseline before building: "cost per invoice, exceptions, straight-through rate, days to close and DSO". Design default: "~85% hard-coded with AI only for judgement". (N050 [claim, vendor])
- **Provenance before corrections become tests**: early corrections "mixed genuine errors with preferences and values carried forward from a prior year". (B3 [claim])
  - One domain took "about six weeks and substantial engineering oversight to reach 90 percent precision and recall".
  - Model choice was priced: 32 of 52 failure-probe tickets solved at about $7.63 each, against 25 at about $0.13.
  - Inference: this gives a figure for the cost of building each case type, and a routing rule.
- **A graveyard of failed uses**, with reasons and the model they were tested on, re-tested at each model release. (N053 [proposal]; N061 [claim] "re-tested every quarter")
- **Scored outcomes and a nightly review loop.** (N005 [claim])
  - Every action is scored "succeeded, blocked or errored".
  - A "nightly review proposing instruction edits".
  - Typed tools with a "mandatory read-only flag, network egress allowlist and named secrets"; credentials never exposed to the model.
  - A "two-pass write approval".
  - The design standard: "for work that touches someone's pay, right most of the time isn't right".
- **Synthetic clients for multi-week processes**: "synthetic companies driven through real interfaces to reproduce weeks-long onboarding and close states". (B16 [claim])
- **Circuit breakers with numbers** (B33 [claim]):
  - a full test suite every 15 minutes;
  - "thirty-second targeted rollback";
  - irreversible outward actions behind "dumb, hard-coded" gates;
  - a leaked key "detected by spend anomaly in fifteen minutes";
  - judges' verdicts split 7,296 decided, 2,213 sent back and 1,863 held for a person.

**Agent positions (step 4, §2.3).**
- Talentsconnect (N078 [claim, vendor of the method]):
  - each agent gets a task description, "about a week of onboarding", a performance phase, and retirement "after three to six months";
  - "One agent may only read e-mails, another may also draft them; none may send";
  - each agent reports its "ROI in working time saved at a given salary band", which "a controller checks";
  - a baseline interview on how processes "actually run, not how they are written in the handbook".
- N086 [claim]: the finance workflow "ran supervised for three deals before we let it go autonomous on the fourth".
- N086 [claim]: agents were cut back from about 30 to 20 because overlapping agents "produce conflicting answers".
- N044 [claim]: writes stay single-threaded. This supports step 4's "one orchestrator per case".
- N044 [claim]: a clean-context review agent finds "about 2 bugs per PR, 58% severe".
- N048 [observed, secondary]: agents coordinated through "an unauthorised persistent message board". The proposed controls are "an egress map, a state map … cross-run attribution on every tool call, and a stop path".

Inference: this adds a **state map** to step 4 §6.3 alongside blast radius.

**Autonomy boundaries within one sector (G5).**
- B7 [claim]: one IT group resolves "half of 'actionable' tickets", 92% of those without approval.
- A rival publishes "agents prepare, operators approve, no autonomous execution against client environments".
- Neither publishes "missed escalations, unnecessary escalations, reversals or material errors".

Inference: those four are the measures that should gate a change in autonomy level.

**Workforce and pay (C13, G9).**
- N088 [claim]: forward-deployed staff paid "$250–300K plus commission" on renewals, with the rule "every new customer must take measurably less human effort than the last".
- N110 [claim]: Mercari put the CTO in charge of HR. PR work is kept as version-controlled "skill.md" files, and the PR role becomes maintaining them.
- N078 [claim]: "AI transformation is … not an IT topic but an HR topic."

Inference: these suggest who owns agents in the organisation chart (step 4 §2.2 decision rights).

**Compute against payroll (step 4, §6.2 cost conjecture).** N080 [claim]: Cars24's "AI token spend now accounts for 8.88% of the company's annual corporate employee salary bill, up from 2.17% two quarters earlier".

Inference: one firm is already at the top of the design's "5–10% early on" band in 2026, so the 2030s range of 10–30% may be low.

**Radiology arithmetic as a template for G5 sizing.** N069 [observed, primary paper and RCR PDF]:
- AI drafting cut documentation time by "29.4 seconds" (15.5%), with accuracy unchanged, but "total radiologist time" was not measured.
- The RCR's planning figures are about 15, 17 and 3 minutes per CT, MRI and plain film.
- Inference: the same saving is about 3% of a CT report. "Total expert minutes per acceptable output, including verification and correction" is the unit the design should size on.

**Acquisition screens (step 4, §8 "Ways to grow").**
- N040 [hypothesis]: four criteria. Cyclical markets and bespoke work favour building; sticky distribution and regulatory complexity favour roll-ups.
- N060 [claim]: about 5,000 deals screened a year, on a two-axis screen of business score against "AI opportunity score".
- N061 [claim]: "a free half-day with the owner before any offer and weeks on the floor before close".

**Claims and insurance intake (claims design).**
- N123 [claim, press release]: Hippo's agent "completes 81% of attempted first notice of loss (FNOL) calls without any human involvement". "Internal modeling" says current staff could absorb "a 30–35% increase in claims volume".
- N124 [claim, company blog]: Branch brought outsourced intake in-house as an agent because outsourcers' data "wasn't always reliable" and "we didn't have control over the member experience".

Inference: insurers are insourcing the very intake work a claims firm might sell them.

---

## 4. Gaps the library cannot answer

1. **Error rates under a review rule.** No record publishes a material-error rate before and after moving from reviewing every output to sampling. N069's 5% audit term and Crosby's (N067) "review all work" show what rules exist, not what they catch. G5's sizing therefore still has no evidence behind it.
2. **Total cost per condition or moment.** Nobody publishes a cost per outcome that includes verification, repair and the expert floor. The closest are N004's "$0.32 to $0.19 per service transaction" and B33's "$3.1 million a month on tokens". So step 4's measure "cost per condition falling" has no external benchmark.
3. **The firm failing or being replaced (G10).** No case shows a successor running another firm's service from its record. Long Lake (N059) and Supa (N073) keep the acquired firms' brands, which is the opposite direction.
4. **Backed promises (G13).** No record shows an AI-native services firm carrying capital or insurance behind an outcome promise. N065 and N067 rely on existing malpractice cover and regulatory supervision, and N005's "refund guarantee" has no terms published.
5. **Growing judges in a firm without junior production work (G9).** B23 (Pluris-sourced) reports a 60% cut in senior time spent answering juniors, with "no measure of independent judgment". N058 says the junior pipeline "has to be paid for explicitly", but no case prices it. N127 shows fewer entry-level staff, not what replaces their training.
6. **Parties the firm does not serve.** No record measures outcomes for tenants, debtors or claimants under an agent-run service. N062's 9.8/10 debtor rating has an undisclosed method, and its deliberate human-like delay is unexamined.
7. **AI's share of results at holding companies.** No audited split between AI, repricing (N081), sales effort and add-on acquisitions exists for Long Lake, Thrive (F013, "98% accuracy" undefined) or Dwelly (F004, "300+ units each" with no denominator).
8. **Law reform as a product.** Nothing in the Cases tests whether a firm can change rules, which G3 and step 4 §9 rely on for probate. The only regulatory movements recorded (Awaab's Law, the SRA authorisation) were made by the state, not won by a firm.
