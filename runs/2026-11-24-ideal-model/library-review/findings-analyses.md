# The AI Implementation Library against the design: findings, analyses and applications

Claude, 24 November 2026. A reading report only. Nothing in the design or in Notion was changed.

## What was read

- In full: all 24 Findings (L001 to L024), including the "discovery sweep" sections added on 24 November; A001 and A002; A003 (about 132,000 characters, read in six slices to the end, appendices included); V001 to V008. Design files read: architecture-v1.md and step-4-building-the-firm.md in full, step-1-the-engine.md skimmed.
- Not read: the underlying case pages (N, B, F and P records). I know them only from the one-line summaries inside the findings. So I have not checked any case's Review status, including whether it was "imported unverified".
- How to weigh it. A finding is "an interpretation, not a fact" (its own migration note). Ten findings are Hypothesis or Design consideration, and two (L002, L009) are Contested. Every sweep addition says "All self-reported unless stated". V001, and part of L015, rest on P069, a Pluris record: unchecked promotional material. The Applications are proposals, not evidence.
- Labels used below: claim (what a company or vendor says), observed (a measured or filed result, or a research study), hypothesis, proposal, and my inference.
- What the design already uses. It already cites L014 and L022. Through the earlier evidence ledger it also uses the freight-forwarder result (92.8% against 22.3%) and LayerX's "cannot assess".

## How each finding bears on the design

| Finding (status) | Part of the design | Verdict |
| --- | --- | --- |
| L001 (Supported) | G5, and step 4 §6.2 agent runtime | Qualifies. Lasting value can come without "an agent reasoning on every transaction". Maintenance cost is unpriced. |
| L002 (Contested) | G1, the record | Supports. Context is definitions, sources and maintained state, not documents. |
| L003 (Supported) | The engine's correction sorting; principle 10 | Supports, and adds "count the whole residual including oversight and repairs". |
| L004 (Supported) | G6, C12; lesson 2 | Qualifies. Moving work to the source may shift effort to the originator. "No case measures the originator's added effort." |
| L005 (Supported) | The engine: "corrections sorted by what they mean" | Supports, and gives the categories. |
| L006 (Supported) | Test suites; §8 stop rules | Supports. Controlled accuracy has not predicted deployment. |
| L007 (Supported) | Builders layer; 2027 build path | Supports. The complementary work is larger than the build. |
| L008 (Supported) | §2.1 layers; independent evaluation; §7 boundary | Supports separating the roles. |
| L009 (Contested) | The autonomy dial | Qualifies. Feedback and recovery "do not determine it alone". |
| L010 (Supported) | G4, conditions as coverage | Qualifies. More coverage is worth something only if it changes action. |
| L011 (Supported) | §7 boundary; build, rent or open | Supports hybrids. |
| L012 (Supported) | G8 adversaries | Supports, and extends. Institutions also change the rules. |
| L013 (Supported) | G5 sizing; G9; lesson 6 | Supports. The residual human tier is "a different job". |
| L014 (Hypothesis) | G5 named person; the review rule | Challenges. Already cited, but not acted on. |
| L015 (Hypothesis) | Step 1 P2; the autonomy dial | Supports. Part of its basis is P069 (Pluris). |
| L016 (Design consideration) | §8 losses in early years | Supports. Adoption effort is a missing cost line. |
| L017 (Supported) | §5 measures | Supports. Two of the design's measures lean towards activity. |
| L018 (Hypothesis) | G13; step 1 P3; §6 margins | Challenges the economics. |
| L019 (Hypothesis) | The model harness | Supports. A002 limits it. |
| L020 (Hypothesis) | G12, G3, the front-door agent | Specifies a mechanism. |
| L021 (Hypothesis) | G6; step 1 P10 | Qualifies "capability where information is born". |
| L022 (Hypothesis) | Step 1 P10 | Supports. Already used. |
| L023 (Hypothesis) | §6.2 infrastructure cost | Qualifies. The recurring cost is reading and reconciling, or authorisation at company scale. |
| L024 (Hypothesis) | Step 4 §1 steps 1 and 2; G13; §9 | Challenges the order of the design steps. |

## 1. Useful material the design does not yet use

Agent arrangements (A001). Step 4 §2.1 and step 3b fill the organisation chart with agent positions. A001 compares three arrangements: one assistant with tools; several workers over shared state; and maintained workflows with occasional AI. It finds:
- "coordination through conversation between agents fails at scale". MAST is cited for "41-87% failure rates" in open-source frameworks.
- Sierra's role-specific agents failed because "the most important work happens across teams" (N012, claim).
- Writes stay single-threaded unless "state and permissions are explicit per action". The design's "one orchestrator per case that alone writes to it" matches this.
- Parallel readers "need a shared output schema and keys" (A002 addendum, observed in one build). The design does not have this rule.
- Rival explanation: "no professional-services firm" runs arrangement (b), workers over shared state.

My inference: the design's many agent positions should be checked against condition 5 before they multiply.

Current state against history (A002, X9). G1 says entries are "added to, never edited". A002 found that "appended handovers recreate the contradictions the system exists to remove". It adopted "properties hold the current value and a change log holds history". A002 itself names the rival: "append-only logs with a generated current view work as well". My inference: G1 needs a specified current-state view, written down as part of the element.

Constraint location (A003 §2). G4 promises "moments made fast". A003 adds a test: where the delay sits with counterparties or scarce capacity, a faster provider "cannot be credited with removing that constraint without an additional mechanism". Its example is conveyancing's "123 days". The architecture's lesson 2 says the bottleneck is outside the firm. A003 says a firm can claim the outcome only if it holds a coordinating contract or platform, and never where the shortage is clinicians, surveyors or contractors. This bears directly on claims, home care and probate.

Pricing bases and how much of a saving is kept (A003 §3). A003 lists seven bases: time, per unit, multi-year contract, subscription, statutory fee (capped or uncapped), third-party paid, and outcome share. Each has its own failure routes. The design sells conditions and moments but does not say which basis each sits on. Step 1 §4 states the conclusion; A003 gives the per-basis mechanics to back it.

Ways to build and grow (A003 §5). Three points the design does not use:
- A003 proposes a hybrid (proposal): buy one firm as the operating platform, then serve other firms "under a mandate on their own systems".
- "The number to ask for is the engineering and adoption cost of the most recent firm against the first." This would make a clear gate in step 4 §8.
- A003's four-way classification of propositions: standalone start-up, acquisition and improvement, product extension, or a feature too small to matter.

Baselines and permission for a retrofit. Step 4 §10 lists retrofitting an incumbent as still to do. Three records bear on it:
- V002 (proposal): mine a year of ERP event logs for exceptions per month, elapsed days and straight-through rate, and "stop if exceptions are under ~100/month".
- V008 and N064: an incumbent software vendor can withhold an integration. The implementer is quoted at "EUR 200k plus 10-15 percent SLA" (claim).
- A003 cites antitrust suits over auto-dealer software.

G6 assumes the firm can get into clients' systems; these records say access can be refused.

Model failures as dated records (V004, L019). Keep a dated "graveyard" of failed uses and re-test it at each major model release. This fits the model harness in step 4 §6.2.

Turning saved time into money (V006, proposal). Before go-live, write three lines: hours freed and in which role; what they will be spent on, with a named owner; and which P&L measure moves, and by when. G5 says "where people produce, agents exist to return their time" but names no way to turn that time into results.

Buyers that automate (V007). Step 1 §5 expects clients' agents to compare firms. V007 adds the effect on price: where a service can be specified, automated procurement compresses margin. Where accountability is part of what is bought, the automation "stops at the specification". This bears on C8 and on pricing.

## 2. Counter-opinions and challenges

1. Nobody has measured how much of a saving a firm keeps. This cuts against the margins in architecture §6, against G13, and against step 1 P3. Strength: strong.
   - L018: "Does any held case show margin retained versus passed through?" None does.
   - A003 calls retention its "weakest premise". It cites filed figures (observed): RWS "adjusted PBT -43 percent"; WPP "revenue -8.1 percent"; Indian IT "10 to 15 percent pricing pass-through".
   - A third party (Vold, in L018) says bolt-on value is "competed away to customers within 18 months".
   - N130 (observed, a hospital's own evaluation): freed time became more throughput only "where the structure of the service allowed"; elsewhere it went to "unpaid hours".

   The design's margins (31%, 45%, 50%) are labelled conjecture. The library gives no basis for them under any pricing basis.

2. The review rule assumes the reviewer judges independently. This cuts against G5 sizing and step 4 §4. Strength: moderate.
   - L014: experts "adopted an agent's lean 86% of the time". That figure is a summary of a study the library has not read.
   - N121 (claim): about 1,300 applications screened "in about two hours", about 5.5 seconds each.
   - Woods, cited in L014: "AI explanation did not improve joint performance".
   - L014 says the remedies are "proposed, not tested".

   The design treats the choice between sampling and reviewing every output as the main unknown for headcount. The library suggests a third: whether either kind of review checks anything.

3. The design starts from the client's outcome, not from what the client already buys. This cuts against step 4 §1 steps 1 and 2, and §9. Strength: moderate.
   - L024: an apparent bottleneck "establishes a problem, not demand for a separate provider".
   - A003's two worked candidates came out as "an improvement inside an existing business" rather than standalone firms: an Awaab's Law repair desk, which ended up as an improvement inside a contractor, and AI-drafted imaging reports, which ended up as an "unproven incremental economic advantage".
   - Exception desks "leave the shortlist" because "no sufficiently distinct or attractive standalone proposition" was found.

   That cuts against step 1 P3's "sell the judgement desk to clients", and against standalone claims and home-care firms.

4. The agent org chart. Strength: moderate. Most of the evidence is self-reported.
   - SaaStr was "cut back from close to 30 because overlapping agents gave conflicting answers" (N086, in L002).
   - Sierra's role-specific agents failed (N012).
   - Garicano, cited in L008: "A lab cannot be the designer, monitor, investigator and judge". This supports the design's independent evaluation function.

5. Deterministic code rather than agents. This cuts against G5's default "agents for information, decisions, money and status". Strength: mild to moderate.
   - Neil Kelly had AI write about 30 scheduled programs, "with no model guessing in the live path" (N083, claim).
   - Stripe: "writing code to deterministically accomplish small decisions we can anticipate" (N090).

   My inference: the producer of a component could often be agent-written deterministic code, which is a fourth option alongside agents, crews and people.

6. Selling coverage. This cuts against G4. Strength: moderate. It bears on the statutory-audit blind test.
   - A003 strand B: full-population audit tools have been "available since 2016, partially adopted, no quality metric, fees not visibly moved".
   - L010: whether wider coverage "changed decisions is unmeasured".

7. Buying books of clients. This cuts against step 4 §8, "Buy books of clients" for accountancy. Strength: moderate.
   - A003 records "a record year of practice acquisitions in 2025, 177 private-equity investments and 875 roll-ups counted over a decade", and concludes: "assume the sellers already know".
   - N129 (observed, research on manufacturing plants): AI adoption "causes significant short-run productivity losses". At older plants, roughly half of that loss is explained by dropping lean management practices.

8. Institutions change the rules against the firm. This bears on G8 and on reform-dependent designs (probate, legal). Strength: mild to moderate.
   - A003: a "£250 fee cut representative complaints to the Financial Ombudsman from 37,100 to 4,300 in a year". A003 notes this is confounded by a separate pause.
   - N079 (claim, anonymous): refund fraud "crept up 4x" after customers "learned how to phrase requests"; the agent was withdrawn after three months.

   G8 anticipates adversaries who learn. The library adds that regulators price induced volume away "within months".

9. Autonomy set by evidence alone. Strength: mild.
   - L009 (Contested): permissions, economics and organisational choices also decide how far work is delegated.
   - Garicano: "colluding agents may hide" errors.

10. Where information is born. This cuts against G6. Strength: mild.
    - L021: commitments made on calls "appear only as later consequences, or not at all".
    - One build (observed): "101 past calendar entries in 31 days against 11 recorded notes in 45 days".

    In legal, probate and care, much is born in conversation.

## 3. Specificity the records offer

- Correction categories (engine). L005: "factual error, preference, task objective and obsolete carried-forward values". A002's owner made corrections of four kinds: "fact, classification, preference, requirement". L005 also warns: "agreement with a reviewer is not proof of better customer outcomes".
- Exception categories (principle 10, step 1 P5).
  - L003: missing information, unavailable tools, policy boundaries, substantive judgement.
  - N094 (vendor): informational, personalised data, action. Informational queries resolve at "90%+", while Fin is "struggling with ... action-based requests".
  - N100: seven request categories, one workflow each.
- A closed list of actions for each agent position (G12, step 4 §2.3).
  - N084: "consult a file, request a document, answer on documented contract terms", with everything else escalated "with context gathered".
  - N078 Talentsconnect: "about a week's onboarding, a performance phase and retirement after three to six months, graded permissions (read or draft, none may send)", and an ROI "checked by a controller". Agent management was given to HR. The design cites Talentsconnect, but not these details.
- Staged autonomy sequences (the autonomy dial; step 4 §6.3).
  - N085: run in parallel with manual work, then automate the simple cases, then "supervised full automation over 18 months".
  - N086: "supervised for three deals before we let it go autonomous on the fourth".
  - Deel: a "two-pass write gate" and a mandatory read-only flag.
  - Spawn: "30-second targeted rollback", with tests every 15 minutes (A001).
  - Stripe: "at most two CI rounds before a human reviews".
  - Intercom: 19.2% of pull requests auto-approved, "86% of them 20 lines or fewer". My inference: autonomy can be scaled to the size of the change.
- Validating the evaluator (evaluation function). N115: seed known-good and known-weak ideas and check that they score as expected. N114: AI output must "pass identical evaluation thresholds" to human work.
- Where commitments come from (G12, G3). L020 and A002 X3:
  - Classify each commitment by basis: the principal's own explicit commitment, another party's explicit commitment, an inference, or a third-party offer.
  - Inferences enter as "a one-line question with a daily cap". The review proposed three a day.
- Measures (step 4 §5).
  - Lemonade's three tests (N138, CEO's proposal): customer growth divided by headcount growth; the loss adjustment expense ratio; gross profit per exposure. These suit claims.
  - Two of the design's own measures, "share handled as a side effect" and "time to adopt a new model", are activity measures in L017's terms.
- Compute cost (step 4 §6.2: 5–10% of payroll early on).
  - Cars24: token spend at "8.88% of the corporate salary bill (2.17% two quarters earlier)" (N080, claim).
  - LayerX: about "¥300,000 per person per month" (N098).
  - Multi-agent research runs at "about 15x the tokens of chat" (A001).
- Returning gains to staff (step 1 P10). LayerX pays "a larger pay pool (up to 10%) and bonuses of up to six months" (N097, claim).
- Separating clients' data (step 4 §6.1 Security). Sierra's gateway inherits each user's access, tags every response for customer and sensitivity, and blocks cross-customer access. It took "about 1.5 engineers" (A001, N046).
- Lettings conditions (G4, G11). Awaab's Law (A003, N068):
  - investigate within "ten working days" and make emergencies safe "within 24 hours";
  - the clock starts when "any part of the landlord or its agent becomes aware";
  - records of access attempts form "the statutory defence".
- Sizing expert review (G5). Measure "total expert time ... including verification and correction". AI drafting cut documentation time by "29.4 seconds, 15.5 percent" on radiographs, which is not total expert time (N069).
- The residual job (G9, the judgement desk). HelloPrint (N133, studied by TNO):
  - customer-service staff fell from about 100 to 20;
  - onboarding now takes "two to three months";
  - first-time resolution was about 62% against 51% a year earlier;
  - satisfaction was 3.45 for the AI against 3.75 for staff.
- Economic discipline (§6 margins, §8 stop rules).
  - A003's bridge: "do not count a freed hour twice, revenue as profit, gross hours as cash, acquisition-led growth as AI uplift".
  - Its price test sets three scenarios side by side: rivals adopting, the programme as dated cash flows, and failed implementation.
- Tying financials to source (V001, resting on P069, which is Pluris and unchecked). Rebuild the P&L from source "with rows that must tie to zero".

## 4. Gaps: questions the design raises that the library cannot answer

- The review rule. No regulator or insurer in the library accepts sampling. The closest is the SRA accepting Garfield's "supervision design" (observed). Toyota (N134) aims to check "all evidence in audits instead of a sample", which suggests AI may make reviewing every output cheap rather than settle the question.
- Capital and backed promises (G13). Nothing on insurers or capital partners pricing an AI firm's guarantees.
- The service surviving the firm (G10). Only A002's "restore not rehearsed and relations do not survive export".
- Succession of judgement (G9). N131 shows skill formation inhibited in a one-hour experiment. There is no case of a route to judgement that a professional body accepts.
- Parties the firm does not serve (G7), and conflicts. No outcome data at all.
- Physical work and human acts. The home-care analogue is "unverified". No crew or care case.
- Limiting the blast radius and correlated error. No case.
- Evaluator incentives, and pooled data (C4). No case of either.
- Mandate against ownership. "Not available anywhere" (A003 investigation 5).
- Economics of AI-native firms. Crosby's and Garfield's economics are unpublished; Garfield reports only "about 600 claims". The library has no measured case of a new firm passing its cold start.
- Who keeps the saving. Unmeasured. A003's proposed "retention ledger" from filed accounts has not been done.
