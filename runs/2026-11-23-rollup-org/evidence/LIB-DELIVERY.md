# LIB-DELIVERY: how work is found, described, handed to AI, checked and signed

Reader: library sub-agent, 23 November 2026. Scope: part 6, Q1 and Q2.

How to read the "Quote" and "Read" lines. Every record below is a Thoughts Library page. I read each page named in full. I did not open any primary source (blog, X post, filing, CIM). Most library pages paraphrase their source. So a quotation is the library record's wording unless marked "source's words", which means the record itself puts the words in quotation marks. "Read: full (record)" means the library page in full, the primary source not at all.

B-records are marked "Imported unverified" in the library. Eight of those used here (B4, B8, B9, B13, B14, B17, B21, B32) cite checkpluris.com as their only source. That is the same promotional origin as the P-cases. They are labelled "Pluris origin" and should carry little weight.

---

### R-LIB-DELIVERY-01
- Claim: One implementer finds the work by mining the ERP event log for every invoice path, and agrees the baseline with finance before building anything.
- Kind: company claim
- Quote: "process-mine every invoice path from ERP event logs (NetSuite, SAP, Oracle, Dynamics); baseline cost per invoice, exceptions, straight-through rate, days to close and DSO and agree them with finance before building"
- Where: N050, https://app.notion.com/4215f5db20d781ada02acb91300cc065 ; source posts dated 30 Oct 2026
- Speaker and interest: Varick COO, an implementer selling paid pilots. Client unnamed.
- Read: full (record)
- Bears on: parts 6, 4, 14; Q1
- Against Ben's starting positions: limits "list the 200 things". The method starts from one function's system log and its exceptions, not from a list of services.

### R-LIB-DELIVERY-02
- Claim: The unit that mattered in that case was the exception and its elapsed time across people, not the task and its minutes.
- Kind: company claim (the worked example is an illustrative composite)
- Quote: "a $48.2k invoice whose PO omitted freight and used units not cases takes 25 minutes of work and 11 days elapsed across five people"; analyst: "copilots shorten the 25 minutes but not the 11 days"
- Where: N050, same page; 30 Oct 2026
- Speaker and interest: Varick COO (vendor); second half is the library analyst
- Read: full (record)
- Bears on: parts 6, 9, 14; Q1, Q2
- Against Ben's starting positions: limits. A task-by-task inventory would record 25 minutes and miss the 11 days.

### R-LIB-DELIVERY-03
- Claim: The same implementer redesigns the process before automating, and builds agents that are mostly fixed code.
- Kind: company claim
- Quote: "build agents ~85% hard-coded with AI only for judgement (reading a vendor email about a short shipment, writing commentary)"; "replace legacy second reviews with auditor-acceptable control checks"
- Where: N050; 30 Oct 2026
- Speaker and interest: Varick COO (vendor)
- Read: full (record)
- Bears on: parts 6, 11, 13; Q1, Q2, Q7
- Against Ben's starting positions: limits "automate as much as you can". Redesign and removal of reviews came first and needed "authority to redesign the process".

### R-LIB-DELIVERY-04
- Claim: Acceptance in that case was shadow running against staff postings, with approval and payment release kept by staff under limits.
- Kind: company claim
- Quote: "shadow mode against staff postings before go-live; approvals and payment release stay with staff under authorisation limits, all agent actions logged for SOX"
- Where: N050; 30 Oct 2026
- Speaker and interest: Varick COO (vendor). Results table (close 18-22 days to 7-9) is unattributed.
- Read: full (record)
- Bears on: parts 6, 3, 13; Q2, Q3
- Against Ben's starting positions: supports "a verifier", and adds two things he does not list: authority limits and an action log.

### R-LIB-DELIVERY-05
- Claim: A fixed quoting workflow that had readable state, written procedure, a way to write and a test set still succeeded on only 22.3% of real requests.
- Kind: company claim (implementer's own figures; success defined differently for the two rates)
- Quote: "synthetic-eval success 92.8% versus 22.3% in production for the fixed RFQ workflow". Analyst: "the production failure of the fixed workflow came from incomplete, ambiguous inputs that a clean synthetic test set did not contain"
- Where: N007, https://app.notion.com/4215f5db20d781bdb215f65724a45efa ; X articles 20 and 27 Jan 2026
- Speaker and interest: Tyler Kim (ndstudio), implementer describing own build for an unnamed ~$20m freight forwarder
- Read: full (record)
- Bears on: parts 6, 10; Q2
- Against Ben's starting positions: contradicts the four as sufficient. That it had "all four" is my reading of the record. What was missing: complete inputs, a test set drawn from real traffic, and a route for vague requests.

### R-LIB-DELIVERY-06
- Claim: The recovery was to let an agent call the workflow steps as tools with an operator present, and to have operators write the SOPs.
- Kind: company claim
- Quote: "the recovery was to make the interaction conversational and let operators supply and encode context. The gain claimed is coverage of cases and cheaper modification, not unattended automation." A001 quotes the source: SOPs "defined what correct meant"
- Where: N007; A001 section 2; Jan 2026
- Speaker and interest: implementer; library analyst for the reading
- Read: full (record)
- Bears on: parts 6, 7, 10; Q1, Q2, Q4
- Against Ben's starting positions: supports "playbooks written per task", with a condition: the people who do the work wrote them. Limits full automation: RFQ time "3-5 min with an operator present".

### R-LIB-DELIVERY-07
- Claim: In the same case operators built their own narrow agents within days once the tools existed.
- Kind: observed result reported by the implementer
- Quote: "DEMONSTRATED: operators built their own narrow agents within days (surcharge calculator, email-history agent, PO extractor, SOP explainer)"
- Where: N007; 27 Jan 2026
- Speaker and interest: implementer
- Read: full (record)
- Bears on: parts 6, 7, 10; Q1, Q4
- Against Ben's starting positions: limits a centrally drawn inventory. The list of work grew from the floor after the first workflow.

### R-LIB-DELIVERY-08
- Claim: Carta described fund-administration work as decision trees drawn by domain experts, one per failure type, which became the agent's prompt.
- Kind: company claim
- Quote: "decision trees drawn by domain experts in Lucidchart are converted to the agent system prompt"; requirements: "fund-admin experts supplying logic for every failure"
- Where: N008, https://app.notion.com/4215f5db20d7813eb689c8e2cc6a65a1 ; First Round Review, 22 Jul 2025
- Speaker and interest: Carta's Director of ML and CPO, in an investor's publication
- Read: full (record)
- Bears on: parts 6, 7; Q1, Q2
- Against Ben's starting positions: supports "playbooks". Unit is the failure type inside one workflow (cash reconciliation, 20,000-25,000 a month), built by "three engineers with the CEO acting as PM".

### R-LIB-DELIVERY-09
- Claim: Carta's agents were in use without a formal verifier; the check was the expert, and the agent mostly suggested.
- Kind: company claim
- Quote: "No formal evaluation loop at time of writing; planned step-level tracking, prompt-edit logging and a baseline test suite"; "agent still mostly suggests rather than completes autonomously at time of writing (July 2025)"
- Where: N008; 22 Jul 2025
- Speaker and interest: Carta executives; savings of "over 3,500 hours a month" are projected, not measured
- Read: full (record)
- Bears on: parts 6, 10; Q2
- Against Ben's starting positions: limits. A case that "worked" without a built verifier, but only as suggestion to a person. No error rate is published.

### R-LIB-DELIVERY-10
- Claim: Deel's platform lets staff describe a workflow in plain language, but every tool is declared by a person with types, a read-only flag, an egress list and injected secrets.
- Kind: company claim (engineering post describes design, not error rates)
- Quote: "Each tool declared once by a person with typed input schema, optional output schema, mandatory read-only flag, network egress allowlist and named secrets injected per call; two-pass write approval (Slack approval by an owner or a policy); credentials never exposed to the model"
- Where: N005, https://app.notion.com/4215f5db20d78106a299c02e30a97497 ; Deel engineering post 30 Sep 2026
- Speaker and interest: Deel, operator describing its own platform, which it now also sells
- Read: full (record)
- Bears on: parts 6, 8, 11, 13; Q2, Q3, Q7
- Against Ben's starting positions: limits. "A way to write" is not one thing: it needs a typed tool, a named owner or policy that approves, and bounded time and fan-out.

### R-LIB-DELIVERY-11
- Claim: Deel scores each run and proposes instruction edits nightly; it publishes no escalation, failure or cost-per-case figure.
- Kind: company claim
- Quote: "outcomes scored as succeeded, blocked or errored; nightly review proposing instruction edits". Source's words: "for work that touches someone's pay, right most of the time isn't right". Not reported: "escalation rate, failure rate, cost per case"
- Where: N005; 30 Sep 2026
- Speaker and interest: Deel; its own figures conflict (100,000 against 250,000 cases a month)
- Read: full (record)
- Bears on: parts 6, 10, 14; Q2, Q4
- Against Ben's starting positions: supports a verifier per action; adds a correction loop. Volume is activity, not outcome.

### R-LIB-DELIVERY-12
- Claim: A lettings group counts human escalations per maintenance task and classes each by cause.
- Kind: company claim
- Quote: "escalation classified by cause (missing information, blocked tool, policy question, judgment)"; "about five human escalations per task at around three minutes each ... against a baseline the firm estimates at about three hours from roughly thirty manual actions. The baseline is assumed, not measured."
- Where: B5, https://app.notion.com/4215f5db20d781ee8092d9f98e6026c6 ; dwelly.group blog, date unknown (figures for August 2026)
- Speaker and interest: the lettings group describing itself; record imported unverified
- Read: full (record)
- Bears on: parts 6, 9; Q1, Q2, Q8
- Against Ben's starting positions: supports "identify edge cases", and gives the classes. Unit is the end-to-end task (a repair case) with about thirty actions, not the single action. Closest held case to reference firm B.

### R-LIB-DELIVERY-13
- Claim: The library's finding is that exceptions are four different kinds of work needing different responses.
- Kind: analyst interpretation
- Quote: "Missing information, unavailable tools, policy boundaries and substantive judgement need different responses; count the whole residual including oversight and repairs." Open question: "Residual composition is rarely published"
- Where: L003, https://app.notion.com/4215f5db20d78178961fcb5b5ff958e0 ; updated 3 Nov 2026
- Speaker and interest: library analyst. Rests on B21, B5, N001, N007, N050, N063; B5 is the only one that publishes the classes.
- Read: full
- Bears on: parts 6, 9; Q1, Q2
- Against Ben's starting positions: supports, and sharpens: an "edge case" is not one category.

### R-LIB-DELIVERY-14
- Claim: An HR-policy engine routes by confidence and sensitivity into answer, draft, or escalate without a draft. (Pluris origin)
- Kind: company claim
- Quote: "routes by confidence and sensitivity, answering some questions, drafting others and escalating sensitive ones without a draft"; "model confidence must be calibrated rather than trusted"
- Where: B21, https://app.notion.com/4215f5db20d7814f970ac720c3c567e6 ; checkpluris.com, date unknown
- Speaker and interest: promotional case study; imported unverified
- Read: full (record)
- Bears on: parts 6, 12; Q1, Q3
- Against Ben's starting positions: not applicable; a second way to class exceptions (by consequence, not cause). No error rate on the auto-answered tier.

### R-LIB-DELIVERY-15
- Claim: In a first-hand build, tasks created from an agent's inference were experienced as noise; the proposed rule is that inference enters as a question.
- Kind: hypothesis (one build, one user, no outcome measure)
- Quote: "Only explicit commitments ... should become tasks; inference should become a one-line question with a daily cap." "The owner's reported split (of 56 tasks, 20 on inference and 8 on imports, experienced as noise) is not verified from files."
- Where: L020, https://app.notion.com/4215f5db20d7814a813eda55e8be146b ; 3 Nov 2026 (rests on N063 / A002)
- Speaker and interest: library analyst on Ben's own build. Limited by N010 and N014, where inferred tasks are reported to work.
- Read: full
- Bears on: parts 6, 9; Q1, Q2
- Against Ben's starting positions: limits. It suggests a fifth requirement: a known trigger and basis for each piece of work.

### R-LIB-DELIVERY-16
- Claim: A holding company found its first deployment took over a year and needed extensive workflow mapping; later firms were reported faster.
- Kind: company claim (founder interview via an automatic transcript)
- Quote: "about 80 percent shared infrastructure by the founder's estimate; extensive workflow mapping, data cleaning and integration; engineers alongside practitioners"; "the first deployment took more than a year; later acquisitions reportedly saw time savings within days"
- Where: B15, https://app.notion.com/4215f5db20d781b395b3d3559ca197c9 ; date unknown
- Speaker and interest: founder of an owner-operator; imported unverified
- Read: full (record)
- Bears on: parts 4, 6, 14; Q1, Q6
- Against Ben's starting positions: supports mapping as a first move, at a cost of a year. Analyst gives three rival explanations for later speed: "platform reuse, cost moved elsewhere, easier later customers".

### R-LIB-DELIVERY-17
- Claim: The accounting roll-up built tax automation one domain at a time; the first domain took six weeks of engineering.
- Kind: company claim
- Quote: "one rental-income domain took about six weeks and substantial engineering oversight to reach 90 percent precision and recall, and the share of returns at 75 percent field completion rose from 25 to 86 percent; later domains were cheaper"
- Where: B3, https://app.notion.com/4215f5db20d78114a953fa5475d9c6b2 ; thriveholdings.com, date unknown
- Speaker and interest: the holding company describing itself; it discloses that OpenAI holds equity in it
- Read: full (record)
- Bears on: parts 6, 10, 14; Q1, Q2, Q6
- Against Ben's starting positions: limits "automate as much as you can". The unit is a domain inside one service (rental income inside a tax return), and each has a build cost.

### R-LIB-DELIVERY-18
- Claim: In that build, practitioner corrections could not be used as they came; they mixed real errors with preferences and stale values.
- Kind: analyst interpretation of a company account
- Quote: "early corrections mixed genuine errors with preferences and values carried forward from a prior year; feedback needs provenance and adjudication before it becomes capability"
- Where: B3; L005, https://app.notion.com/4215f5db20d7816aa61df1ff6d676e97 ("None of the cases reports the error rate of the correction process itself")
- Speaker and interest: library analyst; L005 rests on B3, F013, N005, N007, N063, N070
- Read: full (both records)
- Bears on: parts 6, 10; Q2, Q4
- Against Ben's starting positions: limits. A verifier that is a reviewer's edit needs a known meaning before it can teach anything.

### R-LIB-DELIVERY-19
- Claim: Across about thirty acquired accounting firms, the delivered unit was a return prepared from source documents for a practitioner to review.
- Kind: company claim
- Quote: "7,000 returns in the first season; preparation time down 31 percent on average; accuracy 'up to' 98 percent, which is a maximum, not an average. Company-reported, unaudited." Not disclosed: "review time after preparation, error distribution"
- Where: B2, https://app.notion.com/4215f5db20d7814a985bec89b9e3851f ; current.co news, date unknown
- Speaker and interest: the roll-up describing itself; same organisation as B3, so B2 and B3 are one origin
- Read: full (record)
- Bears on: parts 6, 13, 14; Q1, Q2
- Against Ben's starting positions: not applicable. Closest held case to reference firm A; the signed check stayed local.

### R-LIB-DELIVERY-20
- Claim: An IT-services roll-up has technicians turn their own fixes into runbooks that other acquired firms run; a rival in the same sector allows no autonomous execution.
- Kind: company claim
- Quote: "about 150 agents and 750 skills, roughly 4,000 runs a day, one runbook reused about 300 times"; "half of 'actionable' tickets resolved by the platform ... the actionable population is undefined"; rival: "agents prepare, operators approve, no autonomous execution against client environments"
- Where: B7, https://app.notion.com/4215f5db20d781b19beacdeb792760c9 ; shieldtp.com, date unknown
- Speaker and interest: the holding company describing itself; imported unverified
- Read: full (record)
- Bears on: parts 6, 3, 10; Q1, Q2, Q3
- Against Ben's starting positions: limits a top-down inventory: the playbook list is written by practitioners from tickets as they occur. "neither firm publishes missed escalations ... reversals or material errors".

### R-LIB-DELIVERY-21
- Claim: An accounting platform makes checking a piece of infrastructure: synthetic companies run through the real interfaces, and people review proposals before they reach the books.
- Kind: company claim
- Quote: "synthetic companies driven through real interfaces to reproduce weeks-long onboarding and close states; people review accounting proposals before they affect the books"; "most proposals reportedly pass without edits, with no rate given"
- Where: B16, https://app.notion.com/4215f5db20d78198a1c4e4b8f7913592 ; engineering.integral.de, date unknown
- Speaker and interest: the firm's engineers describing their own system
- Read: full (record)
- Bears on: parts 6, 11; Q2, Q7
- Against Ben's starting positions: supports a verifier; adds that "a single-task benchmark does not represent a multi-week process" (analyst).

### R-LIB-DELIVERY-22
- Claim: A voice-onboarding agent's first design failed because questions were merged to shorten calls; splitting the task fixed it.
- Kind: company claim
- Quote: "The first design merged several questions to shorten calls and lost information on long ones." Requirements: "separate coverage questions, source-linked answers, read-back checks, validated documents, licensed review before submission"
- Where: B18, https://app.notion.com/4215f5db20d781b7b060f5ad8de26dfc ; harperinsure.com engineering post, date unknown
- Speaker and interest: a commercial insurance broker describing itself
- Read: full (record)
- Bears on: parts 6, 13; Q1, Q2
- Against Ben's starting positions: limits. The failure was in how the work was cut up and what was measured (call time), not in a missing one of the four.

### R-LIB-DELIVERY-23
- Claim: Klarna's assistant ran at scale with only proxy checks; the AI share was never rolled back, but the human tier it left behind degraded and was re-specified.
- Kind: company claim in filings, plus analyst interpretation
- Quote: filed "AI share of service chats 62% ... 80% (FY2025)". Source's words (CEO, May 2025): cost had been "too predominant an evaluation factor". Analyst: "Aggregate proxies (chat share, resolution time, internal CSAT) were the only quality signals, so the unmeasured dimension degraded."
- Where: N004, https://app.notion.com/4215f5db20d7818abc90f72ec3b3d28a ; filings 2025-2026
- Speaker and interest: listed company on itself; filings not re-read by the library in that run
- Read: full (record)
- Bears on: parts 6, 7, 9; Q2
- Against Ben's starting positions: limits. It "worked" without an outcome verifier and the cost appeared elsewhere. No escalation or error rate is published.

### R-LIB-DELIVERY-24
- Claim: A resourced private-equity firm reports that multi-step tasks needing modest judgement broke regardless of scaffolding.
- Kind: observed result reported by the owner (no project list, metrics or costs)
- Quote (source's words): "results have been shockingly poor compared to expectations"; processes "often break or become stuck". L009 quotes the scaffolding as "baling wire and duct tape".
- Where: N015, https://app.notion.com/4215f5db20d781ff80acc828064d9136 ; X post 9 Jan 2026, about 2025 work
- Speaker and interest: Brent Beshore, founder, describing own firm's disappointment; nothing to sell
- Read: full (record)
- Bears on: parts 6, 15; Q2, Q6
- Against Ben's starting positions: limits. The record does not say which of the four each project had, so it cannot be scored. The author blames capability. Dated to 2025 models (L019), though L019 itself notes the failure "may not be model-dated".

### R-LIB-DELIVERY-25
- Claim: A ten-person software company delegates almost everything because errors show in minutes and reverse in seconds, with fixed gates on irreversible acts.
- Kind: company claim (founder; change counts, no revenue)
- Quote: "a full test suite every fifteen minutes against live code; thirty-second targeted rollback"; "irreversible outward actions such as payments behind 'dumb, hard-coded' gates"; "about $3.1 million a month on tokens"
- Where: B33, https://app.notion.com/4215f5db20d78177bf7ad605be79464a ; X post, date unknown
- Speaker and interest: founder; among its model vendor's largest customers
- Read: full (record)
- Bears on: parts 6, 8, 14; Q2, Q3
- Against Ben's starting positions: limits. Adds recovery (undo) and a gate on the irreversible. Analyst: unknown "whether the loop can be closed where the state sits in a client's systems ... and outcomes arrive late", which is the services case.

### R-LIB-DELIVERY-26
- Claim: The library holds recovery as helpful but not decisive for how far to delegate.
- Kind: analyst interpretation (status: contested)
- Quote: "Ask which errors become visible, when, who repairs them and what harm occurs first; permissions, economics and organisational choices also matter." Condition: "Operator owns the state and can reverse cheaply."
- Where: L009, https://app.notion.com/4215f5db20d78147b761e607748a3bd9 ; 3 Nov 2026
- Speaker and interest: library analyst; challenged by N015 and N018
- Read: full
- Bears on: parts 6, 3; Q2, Q3
- Against Ben's starting positions: limits; a question to add to the task test.

### R-LIB-DELIVERY-27
- Claim: The library's hypothesis is that what can be checked, and when, should set the control; per-action checking is one control among several.
- Kind: hypothesis
- Quote: "Cases with a per-action check report durable gating; a case measured only by proxies degraded on an unmeasured dimension. This is a hypothesis: records without outcome measures cannot show harm". Conditions: "what establishes adequate performance, what can be checked and when, what remains uncertain, what control is justified at this cost and consequence"
- Where: L015, https://app.notion.com/4215f5db20d7812a8078fe24bc48c2a1 ; 11 Nov 2026
- Speaker and interest: library analyst; limited by N015 ("capability, not checkability, named as the failure")
- Read: full
- Bears on: parts 6, 13; Q2, Q3
- Against Ben's starting positions: supports "a verifier" as central; limits it as a single box. The verifier has a type and a delay.

### R-LIB-DELIVERY-28
- Claim: Test accuracy has not predicted delivery, and the human baseline has errors of its own.
- Kind: analyst interpretation
- Quote: "Human baselines contain hidden errors; controlled-test accuracy and synthetic evals have not predicted deployment performance." Supports include "N002: 99% in controlled tests; retired after nine months" and "N007: 92.8% synthetic versus 22.3% production"
- Where: L006, https://app.notion.com/4215f5db20d7811c9326f550f4c4a35b ; 4 Nov 2026. B1: "evaluation exposed errors in the human baseline". B32 (Pluris origin): 98% screen-reading accuracy was "a feasibility threshold ... not reliable completed work in production"
- Speaker and interest: library analyst. N002 read as a one-line summary only.
- Read: full (L006, B1, B32)
- Bears on: parts 6, 14; Q2
- Against Ben's starting positions: limits. A verifier built on clean test cases is not yet a verifier.

### R-LIB-DELIVERY-29
- Claim: Where document processing was automated for an e-commerce firm, what remained was mostly the checking the client chose to keep.
- Kind: company claim (implementer; customer unnamed)
- Quote: "an 84 percent reduction in operating cost in the first year"; "About two-thirds of the remaining cost is the QA layer the client chose to keep"
- Where: B1, https://app.notion.com/4215f5db20d78150bd46f8785a2a1be0 ; fractional.ai case study, date unknown
- Speaker and interest: Fractional AI, the vendor that built it
- Read: full (record)
- Bears on: parts 6, 14; Q2
- Against Ben's starting positions: not applicable. Analyst: "the size of the retained check is set by the standard and the consequence of error, so it will differ for tax returns or claims".

### R-LIB-DELIVERY-30
- Claim: A regulated AI law firm turned one service into a product by narrowing scope and pricing each step.
- Kind: company claim (prices read on the site); authorisation conditions via trade press
- Quote: site: "a 'polite chaser' at £2.00 and a letter before action at £7.50"; claims up to £10,000. Press: "named solicitors accountable and no case-law proposals permitted"; "defended hearings instructed to a barrister"
- Where: N065, https://app.notion.com/4215f5db20d781759cf5ee9a54cbe5e2 ; site captured 4 Nov 2026
- Speaker and interest: Garfield.Law on itself; "about 600 claims" has no period or denominator
- Read: full (record)
- Bears on: parts 5, 6, 13; Q1, Q8
- Against Ben's starting positions: supports "turn them into products" where the procedure is fixed by rule. Shows the price: the work that does not fit (contested hearings) is handed out.

### R-LIB-DELIVERY-31
- Claim: Another law firm sells contract review by the document with a lawyer reviewing every one; the minutes per document are not published.
- Kind: company claim
- Quote (site's words): "Don't buy hours. Buy outcomes. Fixed rates by the document"; "Human attorneys review all work". Record: "No per-document price, minutes per document, margin or defended-work figures published."
- Where: N067, https://app.notion.com/4215f5db20d781eea5b4fcf4b0f3917a ; site captured 4 Nov 2026
- Speaker and interest: Crosby on itself; venture-funded
- Read: full (record)
- Bears on: parts 5, 6, 13; Q1, Q2
- Against Ben's starting positions: supports the document as a product unit; the verifier is a licensed person on every unit.

### R-LIB-DELIVERY-32
- Claim: A debt collector has a cheap external check on every unit (paid or not), yet most staff are still in operations.
- Kind: company claim (CIM management information; 2025 is a budget)
- Quote: "share of PAID claims handled by the system alone 63% to 81%"; "'AI decision accuracy' 38% (Jan 2025) to 93% (Oct 2025), undefined"; "34.5 FTE (Sep 2025) of which operations ~25"
- Where: N062, https://app.notion.com/4215f5db20d781a6aa0ed11955d067af ; CIM Oct 2025
- Speaker and interest: Debtist management through a sell-side adviser, selling the company
- Read: full (record)
- Bears on: parts 6, 7, 14; Q1, Q2, Q8
- Against Ben's starting positions: limits. A unit with all four still left about 60% of heads in the residual. L015 notes payment checks the result, not conduct.

### R-LIB-DELIVERY-33
- Claim: Two legal cases encode judgement as written rules: a 100-rule lease playbook and six personal skills at a two-lawyer firm; both keep a lawyer reviewing every output.
- Kind: company claim (B8 Pluris origin; N009 first-person)
- Quote: B8: "a 100-rule playbook encodes negotiating positions, fallback language and client-dependent aggressiveness"; "a $25,000 to $100,000 build over six to twelve months"; tested on "one benchmark lease". N009: "attorney review of every output"; "No counts, error rates or revenue figures."
- Where: B8, https://app.notion.com/4215f5db20d781f4bff1d8b595c11140 (date unknown); N009, https://app.notion.com/4215f5db20d781518fccec19d151b719 (27 Feb 2026)
- Speaker and interest: B8 promotional; N009 the managing partner, an enthusiastic adopter
- Read: full (both records)
- Bears on: parts 6, 7, 13; Q1, Q2
- Against Ben's starting positions: supports "playbooks per task". N009 worked with no built verifier and no shared state, at the scale of one person's judgement.

### R-LIB-DELIVERY-34
- Claim: Three cases gained without an agent doing the work at all: explicit rules, a classifier, and a check moved to the originator. (All Pluris origin)
- Kind: company claim
- Quote: B4: "Determinations are attributed to explicit rules." B9: "the team tested a language model and chose an interpretable machine-learning classifier for the core decision". B17: "compliant submissions reportedly rose from about 30 to 95 percent"; requirements "little"
- Where: B4, B9, B17 (pages under https://app.notion.com/, IDs as named); dates unknown
- Speaker and interest: promotional case studies; imported unverified
- Read: full (records)
- Bears on: parts 6, 11; Q1, Q2, Q7
- Against Ben's starting positions: limits. The inventory needs a column for "rules or a sequence change will do". L001: "A lasting integration can create value without an agent reasoning on every transaction"; L004: "check whether effort merely moved to the originator".

### R-LIB-DELIVERY-35
- Claim: Two cases stalled on things outside the four: nobody owned the translation of practice into builds, and legacy data could not be read. (Both Pluris origin)
- Kind: company claim
- Quote: B14: "someone has to translate practice into maintained build-and-test work; tools alone did not suffice in this firm. The claim that this is universally the missing link is not accepted." B13: "employees had already experimented with a general model; a specialist converted legacy output into a usable format"
- Where: B14, B13; dates unknown
- Speaker and interest: B14 a recruiter's case study; B13 promotional
- Read: full (records)
- Bears on: parts 6, 7; Q2, Q6
- Against Ben's starting positions: B13 supports "state an agent can read" as a real gate. B14 limits: a named owner is needed as well.

### R-LIB-DELIVERY-36
- Claim: A001's condition for part 6: narrow work with rules that can be written suits a maintained workflow, and that degrades when inputs are messy.
- Kind: analyst interpretation
- Quote: "Where the task is narrow and the rules can be written down, a maintained workflow with AI interpretation is cheaper and more auditable than either agent arrangement ... Limit: the forwarder's fixed workflow failed in production on vague inputs". Also: "Writes stay single-threaded unless state and permissions are explicit per action."
- Where: A001 section 3, https://app.notion.com/4215f5db20d781688f51e47b90e090c2 ; 30 Oct 2026, addendum 3 Nov 2026
- Speaker and interest: library analyst. Rival explanation stated: "no case of the same work done two ways, and no professional-services firm running (b)".
- Read: full
- Bears on: parts 6, 8, 11; Q2, Q7
- Against Ben's starting positions: limits. Input quality decides the arrangement before the four are even tested.

### R-LIB-DELIVERY-37
- Claim: A001 finds that no arrangement in the library has published an outcome measure.
- Kind: analyst interpretation
- Quote: "None of the arrangements has published an outcome measure. Sierra, Ramp, Block and Uber report adoption and spend ... Spawn reports change counts"
- Where: A001 section 3, point 7; 30 Oct 2026
- Speaker and interest: library analyst
- Read: full
- Bears on: parts 6, 14; Q2
- Against Ben's starting positions: not applicable. It bounds every row above: "worked" means "is in use, by its owner's account".

### R-LIB-DELIVERY-38
- Claim: The library asks that a proposition be tested first against what the customer already buys and what part of the outcome the provider controls.
- Kind: hypothesis (two cases)
- Quote: "An apparent bottleneck in a customer's outcome ... establishes a problem, not demand for a separate provider." Limit: "B5: A lettings group that holds the whole coordination cycle and the landlord relationship controls the outcome it sells"
- Where: L024, https://app.notion.com/4215f5db20d7818a976af9aba06de3c7 ; 4 Nov 2026
- Speaker and interest: library analyst
- Read: full
- Bears on: parts 5, 6; Q1, Q9
- Against Ben's starting positions: limits "turn them into products". An inventory line needs "who controls the outcome".

---

## What this adds up to

All of this section is inference.

On Q1. No held case began with a full list of a firm's services. Each began with one workflow where volume and pain were known (N050, N007, N008, B3, B5), then widened. The one case that reports "extensive workflow mapping" (B15) took over a year. The lists that grew, grew from practitioners: runbooks (B7), SOPs and small agents (N007), decision trees (N008). The unit differs by level: a domain inside a service for building (B3), a case or task with its escalations for running (B5, N062), a document or step for selling (N065, N067). Exceptions are classed two ways: by cause (B5, L003) and by consequence (B21).

On Q2. The four are needed but not enough. N007 arguably had all four and failed on real inputs. N062 has all four and still keeps most heads in the residual. Cases ran without a built verifier (N008, N009, N004) only where a person checked every output, or where harm went unmeasured. The cases add: complete inputs and a trigger with a known basis (N007, L020); authority, limits and a named approver (N005, N050); a class and route for each exception (B5); undo (B33, L009); a test set drawn from real traffic (L006); a correction whose meaning is known (B3, L005); an owner who maintains the playbook (B14, N007); and a first check on whether rules alone will do (B4, B9).

## What is missing

- Any case that started from a complete inventory of a firm's services and reports what happened. None found.
- Any published split of the residual by exception class with numbers. B5 names the classes but not the counts per class.
- Error, reversal or missed-escalation rates for any case. None found (stated outright in B7, N005, N008).
- Any case of the same task run with and without one of the four. None found; A001 says so.
- How an inventory is kept true as work changes. Nothing found beyond N007's weekly SOP edits.
- Volume thresholds that pay for a build (L016 was not on my list; B3 and B8 give only build cost).
- A named owner per automated task as a recorded practice. Only N005's "approval by an owner or a policy".
- Process-mining or work-mapping products as such. Only N050's method.

## Not retrieved

- No primary source behind any record was opened: the X posts, blog posts, filings and the Debtist CIM were read only through the library's pages.
- B-case bodies not read (title and one-line "Work" field only): B6, B10, B11, B12, B19, B20, B22, B23, B24, B26, B27, B28, B29, B30, B31.
- N002 (cited in L006), N001, N010, N014, N018, N063, N070, F013: read only as one-line summaries inside findings pages.
- A002 and A003: not read by me; referred to only where A001 or a finding cites them.
- Source dates for every B-record: the library records "dates unknown".
