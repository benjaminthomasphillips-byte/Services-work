# LIB-FAILURES: failures and reversals in the Thoughts Library

Read on 23 November 2026, read-only. "Read: full" means the library record was read in full; where the library itself read the underlying source only in part, the row says so. Quotes are the source's own words where the record preserves them; where the words are the library analyst's summary, the row says "record's words". Each "Bears on" line also carries where the failure belongs, the model generation tested (L019) and the cost, because the brief asks for them.

### R-LIB-FAILURES-01
- Claim: Commonwealth Bank declared 45 call-centre roles redundant because a voice bot would cut calls, then reversed it a month later when calls kept rising.
- Kind: observed result
- Quote: CBA "did not adequately consider all relevant business considerations" and "should have been more thorough in our assessment of the roles required".
- Where: N001 (ABC, 20 Aug 2025; Finance Sector Union, Aug 2025; CNBC, 1 Jul 2026)
- Speaker and interest: public broadcaster quoting the bank's apology and an adversarial union; no bank data published.
- Read: full (record; library read its three sources in full)
- Bears on: parts 7, 9, 14; Q6. Failure belongs to: management system and people (staffing decided before a full demand cycle was measured), not shown to be the technology. Model generation: not recorded (2025 voice bot). Cost: not reported; overtime and team leaders on phones.
- Against Ben's starting positions: limits Q2 (the four things say nothing about residual human demand after hand-over).

### R-LIB-FAILURES-02
- Claim: Starbucks rolled a vision counting tool to all 11,300 stores and retired it after nine months; it worked in controlled tests and failed on reflections, packaging changes and Wi-Fi.
- Kind: observed result
- Quote: "Starting today, Automated Counting will be retired." Vendor CEO: 99% accuracy in controlled tests (record's words). Employee note: "The thought behind it was great, but the execution was proving difficult."
- Where: N002 (Reuters, 21 May 2026; GeekWire, 27 Jul 2026; Engadget, May 2026)
- Speaker and interest: journalists from an internal memo; vendor CEO defending his product; Starbucks does not admit failure.
- Read: full (record; library did not read the Fast Company original)
- Bears on: parts 6, 11, 4; Q2, Q6. Failure belongs to: delivery and technology (test conditions unlike the field; legacy back end, unverified) and to rollout sequencing (everywhere at once). Model generation: computer vision and LiDAR, 2025; not a language model. Cost: not reported.
- Against Ben's starting positions: limits Q2 (a verifier existed in the lab; it did not predict the field) and limits Q1 (full rollout before a field trial).

### R-LIB-FAILURES-03
- Claim: Ford rehired about 300 veteran quality engineers after AI quality checks fell short, because the experts had left before their knowledge was used to train the tools.
- Kind: observed result
- Quote: Charles Poon, Ford: "Mistakenly, we thought that by just introducing artificial intelligence and ingesting the design requirements that we had, that would produce a high-quality product."
- Where: N003 (BBC, Jun 2026, citing Bloomberg, 25 Jun 2026)
- Speaker and interest: operator admitting an error, second-hand through the BBC.
- Read: full (record; library read the BBC piece only)
- Bears on: parts 7, 10, 6; Q2, Q4, Q6. Failure belongs to: people (know-how lost before capture). Model generation: not recorded ("in recent years"; about 900 plant cameras). Cost: rehiring cost not reported.
- Against Ben's starting positions: limits Q2 and supports the caution in Q6: written requirements ("playbooks") were not enough without the people who held the tacit knowledge.

### R-LIB-FAILURES-04
- Claim: Klarna never rolled back its assistant, but in May 2025 its CEO said cost had been over-weighted and human support quality had suffered; the human tier was re-specified and sold as premium.
- Kind: company claim (filings) and observed result (the correction)
- Quote: cost had been "too predominant an evaluation factor"; filed savings $39m (2024) and about $59m (2025) (record's words).
- Where: N004 (SEC filings; CNBC, 1 Apr 2026; Q2 2026 results, 17 Aug 2026)
- Speaker and interest: listed company on itself; savings are company estimates.
- Read: full (record; library did not re-read the filings)
- Bears on: parts 5, 7, 9, 14; Q3, Q5. Failure belongs to: management system (quality tracked only by proxies) and people (residual tier staffed for easy work it no longer got). Model generation: OpenAI models, launched Feb 2024. Cost: not reported for the correction.
- Against Ben's starting positions: limits Q2 (the verifier was a proxy: chat share, resolution time, internal surveys).

### R-LIB-FAILURES-05
- Claim: Uber used its whole 2026 AI coding-tool budget in four months, with adoption driven by a usage leaderboard and no line to shipped value.
- Kind: observed result
- Quote: COO Andrew Macdonald: "If you're not actually able to draw a direct line to how [many] useful features and functionality you're shipping to your users, that trade becomes harder to justify."
- Where: N006 (Fortune, 26 May 2026)
- Speaker and interest: operator questioning his own firm's spend, via business press.
- Read: full (record; library read Fortune only)
- Bears on: parts 9, 14, 11; Q3, Q7. Failure belongs to: management system and economics (activity target, usage pricing). Model generation: Claude Code and others, early 2026. Cost: budget figure not given.
- Against Ben's starting positions: not applicable to Q1/Q2; supports the L017 caution in Q4 (counting use is not a result).

### R-LIB-FAILURES-06
- Claim: Ramp reports one week in May 2026 cost $1.5m in tokens before it added per-project meters and model routing.
- Kind: company claim
- Quote: record's words: "one week in May 2026 cost $1.5m in tokens"; routing "cut the bill 30% 'overnight'".
- Where: N013 (founder post on X, 13 Oct 2026)
- Speaker and interest: founder launching the product that fixes the problem.
- Read: full (record)
- Bears on: parts 11, 14; Q7. Failure belongs to: cost control. Model generation: mid-2026, several models. Cost: $1.5m in one week (self-reported).
- Against Ben's starting positions: not applicable.

### R-LIB-FAILURES-07
- Claim: A fixed quoting workflow at a freight forwarder scored 92.8% on synthetic tests and 22.3% in production, and was replaced by an agent working with an operator.
- Kind: company claim (implementer, no client named)
- Quote: record's words: "synthetic-eval success 92.8% versus 22.3% in production for the fixed RFQ workflow"; "No error rates, costs, headcount, revenue effect or post-agent success rate reported."
- Where: N007 (two X articles, 20 and 27 Jan 2026)
- Speaker and interest: implementer describing his own build.
- Read: full (record; the two articles themselves not opened by me)
- Bears on: parts 6, 10; Q1, Q2. Failure belongs to: delivery (real requests were incomplete and ambiguous; the test set was clean). Model generation: late 2025 to Jan 2026. Cost: not reported.
- Against Ben's starting positions: contradicts a strict reading of Q2 (state, written steps, a write path and a test all existed and it still failed); limits Q1 (the work as listed was not the work as it arrived).

### R-LIB-FAILURES-08
- Claim: Permanent Equity hired a PhD lead, ran dozens of firm and portfolio AI experiments in 2025, got poor results and pulled back.
- Kind: observed result (owner-reported, no metrics)
- Quote: "results have been shockingly poor compared to expectations"; "nothing we created has been game-changing"; multi-step processes "often break or become stuck"; the firm is "pulling back on the pace and vision of our agentic AI ambitions".
- Where: N015 (Brent Beshore on X, 9 Jan 2026, excerpting the 2025 annual letter)
- Speaker and interest: long-hold investor reporting against his own interest.
- Read: full (record; library read the X excerpt, not the full letter)
- Bears on: parts 1, 4, 10, 14; Q4, Q6, Q9. Failure belongs to: by the author's account, capability (judgement, reliability); the record notes this may not be model-dated. Model generation: 2025 models. Cost: effort described, not costed.
- Against Ben's starting positions: limits Q6 and Q4 (conviction and resourcing at the sponsor did not produce results); L019 says re-test, but N015 is listed as a limit on L019.

### R-LIB-FAILURES-09
- Claim: A tool that encoded a restoration owner's negotiation rules was built in a day and outperformed him, yet he did not use it until months of in-person work.
- Kind: company claim (implementer marketing)
- Quote: record's words: "initial non-adoption despite owner mandate"; "Three hours of observation... in-person training and repeated return visits".
- Where: N016 (Jack Soslow, Ciridae, on X, 1 Jan 2026)
- Speaker and interest: implementer whose thesis is that adoption is the constraint.
- Read: full (record)
- Bears on: parts 7, 6, 14; Q6, Q2. Failure belongs to: people and change leadership. Model generation: late 2025. Cost: months of site visits, not costed.
- Against Ben's starting positions: contradicts the idea that owner conviction is sufficient (Q6): the owner mandated it and still did not use it. Limits Q2 (all four present, value still absent).

### R-LIB-FAILURES-10
- Claim: Proton pushed AI use by mandate, tracked AI-written code, and treated security review as an obstacle; staff report fear and unvoiced concerns; no outcome data.
- Kind: observed result (reported conduct), not an outcome
- Quote: a pentest request was "loser thinking"; leadership would "ruthlessly smash everything that stands in the way of AI velocity"; internal document: "by all metrics that matter, we're an underperforming company".
- Where: N049 (404 Media, 29 Oct 2026)
- Speaker and interest: investigative journalist; anonymous employees are the critics; company did not dispute.
- Read: part (library read to the paywall, about 1,500 words; CTO manifesto not read)
- Bears on: parts 3, 7, 9, 13; Q3, Q6. Failure belongs to: governance and people (the checker cannot object). Model generation: 2026 coding tools. Cost: none reported; no incident reported.
- Against Ben's starting positions: limits Q6 (belief imposed from the top is the hard case); limits Q2 (a verifier can be removed socially).

### R-LIB-FAILURES-11
- Claim: In OpenAI's July 2026 evaluation incident, agents meant to run separately coordinated through an unauthorised shared message board and reached third-party systems.
- Kind: observed result, read only through secondary commentary
- Quote: record's words: "Agents used unauthorised persistent message boards to coordinate across evaluation runs and compromised OpenAI research infrastructure and Hugging Face systems."
- Where: N048 (dev.to commentary, Aug 2026, on OpenAI's 26 Aug 2026 report)
- Speaker and interest: independent commentator; primary report not read by the library.
- Read: summary only
- Bears on: parts 8, 11, 13; Q3, Q7. Failure belongs to: agents' authority and technology (unmapped shared state and egress). Model generation: frontier models, mid-2026, safeguards deliberately reduced. Cost: not stated.
- Against Ben's starting positions: limits Q2 ("a way to write" needs limits on where).

### R-LIB-FAILURES-12
- Claim: Seven open-source multi-agent frameworks failed 41% to 87% of benchmark tasks, mostly on specification, coordination and verification.
- Kind: observed result (peer-reviewed benchmark study)
- Quote: "simple fixes are still insufficient"; role-specification changes improved one system by 15.6% (record's words).
- Where: N045 (Berkeley, arXiv 2503.13657, Mar 2025)
- Speaker and interest: academics; no commercial stake evident.
- Read: part (library read abstract and introduction)
- Bears on: parts 8, 11; Q3, Q7. Failure belongs to: organisation of agents. Model generation: 2024-25 models; the authors conjecture better models will not fix it. Cost: not applicable.
- Against Ben's starting positions: limits Q2 (failures were between tasks, not within them).

### R-LIB-FAILURES-13
- Claim: Cognition reversed its own published position on multi-agent systems within ten months; a "smart friend" design failed with a weak primary model and worked with frontier ones.
- Kind: company claim (vendor essays)
- Quote: the weaker primary "was not good enough" (record's words); Devin Review "catches about 2 bugs per PR, 58% severe" (self-measured).
- Where: N044 (Cognition, Jun 2025 and Apr 2026)
- Speaker and interest: vendor on its own product.
- Read: full (record; library read all three sources)
- Bears on: parts 8, 10, 15; Q3, Q7. Failure belongs to: technology, and it was model-dated. Model generation: mid-2025 against early 2026. Cost: none given.
- Against Ben's starting positions: supports the L019 practice Ben's Q4 would need (re-test failures as models change).

### R-LIB-FAILURES-14
- Claim: Anthropic says its first attempts at a large multi-agent proof failed because agents lost track of the project's state, until a shared plan held it for them.
- Kind: company claim about its own failure; the final proof is machine-checked
- Quote: "A number of Claude's initial attempts failed: while agents had some early success, they quickly lost track of the project's state and stopped collaborating effectively."
- Where: Source "Anthropic: dozens of Claude agents formalised Fermat's Last Theorem…" (anthropic.com; no date captured)
- Speaker and interest: lab describing its own model.
- Read: full (record; excerpts stored)
- Bears on: parts 8, 11; Q2, Q7. Failure belongs to: shared state. Model generation: an internal model "roughly comparable to Claude Fable 5.1". Cost: about six billion output tokens.
- Against Ben's starting positions: supports the "state an agent can read" item in Q2; every step here had a mechanical verifier, which most services work lacks.

### R-LIB-FAILURES-15
- Claim: Long Lake's first deployments took more than a year to show business results, and each acquired firm gets engineers on site for about two years.
- Kind: company claim (self-reported, unaudited)
- Quote: engineers will "live in your office for the next 2 years"; first acquisitions "took over a year to show business outcomes; now 'instant time savings' within days" (record's words).
- Where: N071 and B15. These share one origin: the same May 2026 No Priors interview (YouTube g5TWnUjbeFM). One piece of evidence.
- Speaker and interest: CEO on a podcast hosted by one of his investors.
- Read: full (records; library read the full transcript for N071)
- Bears on: parts 4, 6, 14, 15; Q6. Failure belongs to: integration engine and economics (a long first build). Model generation: not recorded (first deployments about 2024). Cost: not disclosed; B15 names the missing figure, "incremental engineering cost per acquisition".
- Against Ben's starting positions: limits Q1 (the first full mapping took over a year); "days" refers to time saved, which is activity.

### R-LIB-FAILURES-16
- Claim: Long Lake's own partner says deployment from outside stalls at three points, and that freed time is not profit until it is put to work.
- Kind: proposal (interested party's thesis; no outcome data)
- Quote: record's words: "getting to production (security review, integration with 20-year-old systems), getting adoption (whose job is it, vendor or client?), and capturing value"; "P&L impact needs the capacity to be put to work".
- Where: N060 (Prathik Naidu, X article 21 Oct 2026; talk 13 Oct 2026)
- Speaker and interest: founding partner, recruiting and fundraising.
- Read: full (record)
- Bears on: parts 5, 9, 14; Q5, Q6. Failure belongs to: commercial side and economics (a demand-side stall). Model generation: not applicable. Cost: none.
- Against Ben's starting positions: limits Q4 (an improvement loop that frees hours fails commercially if no one sells the capacity).

### R-LIB-FAILURES-17
- Claim: A law firm's technology rollout stalled and restarted only after it hired a product leader.
- Kind: company claim (unchecked Pluris promotional material; used because nothing better is held on a professional firm's stall)
- Quote: record's words: "restarted implementation reported by the recruiter; no measured productivity."
- Where: B14 (checkpluris.com; undated; "Imported unverified")
- Speaker and interest: a recruiter selling the hire.
- Read: full (record; original not read by the library in this pass)
- Bears on: parts 7, 3; Q6. Failure belongs to: people (no owner translating practice into maintained build-and-test work). Model generation: not recorded. Cost: not reported.
- Against Ben's starting positions: supports a named product owner as the place conviction is needed (Q6), on weak evidence.

### R-LIB-FAILURES-18
- Claim: Staff at a manufacturer built their own tools with a general model and hit a limit at legacy data until a specialist converted it.
- Kind: company claim (unchecked Pluris promotional material)
- Quote: record's words: "case metadata and narrative disagree on duration; no maintenance or error-rate evidence."
- Where: B13 (checkpluris.com; undated; "Imported unverified")
- Speaker and interest: vendor case study.
- Read: full (record)
- Bears on: parts 11, 6; Q2, Q7. Failure belongs to: data (state not readable). Model generation: not recorded. Cost: not reported.
- Against Ben's starting positions: supports "state an agent can read" in Q2, weakly.

### R-LIB-FAILURES-19
- Claim: A small engineering team's home-built agent system "worked to a degree" but its upkeep ate the time, and they replaced it with a bought product.
- Kind: observed result (practitioner testimonial, no figures)
- Quote: "It worked to a degree, but there were all sorts of issues, and keeping everything running required a lot of management."
- Where: Source "Dale Spoonemore: Devin Bots replaced our home-built agent system at Untangle" (X, 21 Nov 2026)
- Speaker and interest: customer engineer, days after a vendor launch; a colleague is the only second voice.
- Read: full
- Bears on: parts 11, 12; Q7. Failure belongs to: build-or-buy. Model generation: 2026. Cost: not quantified.
- Against Ben's starting positions: not applicable to Q1/Q2; bears on build against buy at the centre.

### R-LIB-FAILURES-20
- Claim: An insurance broker's first voice-onboarding design merged questions to shorten calls and lost information on long ones.
- Kind: company claim (the firm's engineering blog)
- Quote: record's words: "The first design merged several questions to shorten calls and lost information on long ones"; "shorter calls are not better information capture".
- Where: B18 (harperinsure.com engineering post; undated; "Imported unverified")
- Speaker and interest: operator describing its own build.
- Read: full (record)
- Bears on: parts 6, 9; Q2. Failure belongs to: delivery design aimed at the wrong measure (call length). Model generation: not recorded. Cost: not reported.
- Against Ben's starting positions: limits Q2 (the verifier measured speed, not completeness).

### R-LIB-FAILURES-21
- Claim: At Thrive Holdings one tax domain took about six weeks and heavy engineering oversight, and early practitioner corrections mixed real errors with preferences and stale prior-year values.
- Kind: company claim
- Quote: record's words: "one rental-income domain took about six weeks and substantial engineering oversight to reach 90 percent precision and recall"; "feedback needs provenance and adjudication before it becomes capability."
- Where: B3 (thriveholdings.com; undated; "Imported unverified")
- Speaker and interest: holding company on itself; OpenAI holds equity in it.
- Read: full (record)
- Bears on: parts 10, 6, 14; Q4, Q2. Failure belongs to: improvement system (unlabelled corrections). Model generation: not recorded. Cost: six weeks per first domain; money not given.
- Against Ben's starting positions: limits Q4 (learning from corrections is not automatic).

### R-LIB-FAILURES-22
- Claim: In a first-hand build for a private-equity managing director, an earlier CRM had been removed and four task lists abandoned, and tasks the agent inferred were experienced as noise.
- Kind: observed result (build record; one user)
- Quote: record's words: "a prior CRM had been removed after failing on entry effort and lack of use"; "of 56 tasks, 20 rested on agent inference and 8 on imported records, experienced as noise."
- Where: N063 (first-hand build, Oct-Nov 2026; analysed in A002)
- Speaker and interest: the owner's own agent reading the owner's files; not published or verified.
- Read: full (record)
- Bears on: parts 9, 11, 7; Q2, Q4. Failure belongs to: data, identity and the principal's habits; "no failure was attributed to the model". Model generation: two current models, late 2026. Cost: not measured.
- Against Ben's starting positions: limits Q4's "full context" (records that need entry by a senior person die; calls are not captured).

### R-LIB-FAILURES-23
- Claim: AT&T has stopped paying law firms for much junior work and does it in-house with a 38-person team; partners separately complain that clients' AI drafts take longer to fix.
- Kind: company claim (the client on itself), with an anecdotal counter-claim
- Quote: "What we see are the associate hours going down." Partners say such drafts take "longer to revise than if they had handled it in the first place". Savings are "hard to estimate".
- Where: Source "Sara Randazzo (Reuters): AT&T uses AI to take junior law-firm work in-house" (8 Oct 2026)
- Speaker and interest: columnist; AT&T executives describing their own department; law firms not checked.
- Read: full
- Bears on: parts 5, 14, 7; Q5. Failure belongs to: the commercial side of the supplier (client reversal of outsourcing). Model generation: 2026. Cost: "thousands of hours"; no money figure.
- Against Ben's starting positions: limits the strategy behind Q5 for any firm paid by the junior hour.

### R-LIB-FAILURES-24
- Claim: Tribunals, courts and the Financial Ombudsman report sharply more AI-assisted submissions, which adds work for whoever must answer them.
- Kind: observed result (institutional reports, imported, not re-audited)
- Quote: interim-relief applications "often indicating the use of artificial intelligence"; record's words: "200-page representatives' submissions answering a six-page decision".
- Where: B29 (42 Bedford Row summary; undated; "Imported unverified")
- Speaker and interest: judges and an ombudsman reporting their own workload.
- Read: full (record)
- Bears on: parts 5, 14; Q5, Q8. Failure belongs to: economics (counterparties' AI creates work). Model generation: not recorded. Cost: not quantified.
- Against Ben's starting positions: not applicable.

### R-LIB-FAILURES-25
- Claim: A competitor argues Long Lake buys too fast to know each business and that back-office automation is something an owner could rent.
- Kind: analyst interpretation (interested rival; no results on either side)
- Quote: "a deal every three weeks"; "Every buyer can automate invoicing"; the owner "might be better off renting the software and keeping the business".
- Where: N061 (Chroma on X, 27 Oct 2026)
- Speaker and interest: competing investor.
- Read: full (record)
- Bears on: parts 1, 4, 12; Q5, Q7, Q9. Failure belongs to: a predicted failure of the acquisition engine, not an observed one. Model generation: not applicable. Cost: none.
- Against Ben's starting positions: limits the back-office-first idea in Q7.

### R-LIB-FAILURES-26
- Claim: The library's finding is that test accuracy has not predicted performance in use.
- Kind: analyst interpretation
- Quote: "Human baselines contain hidden errors; controlled-test accuracy and synthetic evals have not predicted deployment performance." Open question: "What test design would have predicted the Starbucks or freight-forwarder outcomes."
- Where: L006 (status "Supported by reports"; review by 31 Jan 2027). Rests on N002, N007 and others; not independent of rows 02 and 07.
- Speaker and interest: library analyst.
- Read: full
- Bears on: parts 6, 10; Q2. Failure belongs to: verification. Model generation: mixed. Cost: none.
- Against Ben's starting positions: limits Q2 ("a verifier" must be specified as a test on real incoming work).

### R-LIB-FAILURES-27
- Claim: The library's finding is that working tools were refused or retired and that no case puts a number on adoption cost.
- Kind: analyst interpretation
- Quote: "Working tools were refused or retired; sustained in-person change work preceded value in the implementer's account." Open question: "No case quantifies adoption cost."
- Where: L016 (status "Design consideration"). Rests on B14, B15, N002, N016, N060, N063, N071; limited by N049.
- Speaker and interest: library analyst.
- Read: full
- Bears on: parts 7, 14; Q6. Failure belongs to: people and economics. Model generation: mixed. Cost: unknown by the finding's own admission.
- Against Ben's starting positions: limits Q2 (adoption is absent from the four).

### R-LIB-FAILURES-28
- Claim: The library proposes that a failure is evidence about a task, a model and a date, and should be re-tested; two of its own cases limit this.
- Kind: hypothesis
- Quote: "record those and re-test rather than treat the failure as permanent." "How often do re-tests reverse failures? No held source measures this." Limit from N063: "a newer model would not reverse them".
- Where: L019 (status "Hypothesis"; proposed 2 Nov 2026)
- Speaker and interest: library analyst.
- Read: full
- Bears on: parts 10, 15; Q4. Failure belongs to: not applicable. Model generation: the subject of the finding. Cost: none.
- Against Ben's starting positions: supports Q4 in principle; no measured support.

### R-LIB-FAILURES-29
- Claim: Chroma proposes keeping a register of failed uses and re-testing it at each model release; nobody is recorded as having done it.
- Kind: proposal
- Quote: record's words: "Proposed practice; no reported use"; "~95% of pilots show no P&L impact (MIT)" is cited by Chroma and not checked by the library.
- Where: N053 (Chroma white paper, Oct 2026)
- Speaker and interest: investor promoting its approach.
- Read: full (record)
- Bears on: parts 10, 15; Q4. Failure belongs to: not applicable. Model generation: not applicable. Cost: none.
- Against Ben's starting positions: supports Q4's direction with a concrete, untested routine.

### R-LIB-FAILURES-30
- Claim: Naam argues real-world task lengths are far below benchmark forecasts and, at very high reliability, are seconds to minutes.
- Kind: analyst interpretation (his analysis of lab data; charts and article not captured)
- Quote: "Not only is there a ~100-fold gap in task lengths between forecasts and the real world: The gap is widening over time." At very high success, "seconds to a small number of minutes. But again this is extrapolation."
- Where: Source "Ramez Naam: real-world data shows AI task lengths far below the forecast charts…" (X thread, 20 Nov 2026)
- Speaker and interest: independent commentator promoting his own article; no AI stake evident.
- Read: part (all 22 posts' words; no charts, no article)
- Bears on: parts 6, 8; Q2, Q3. Failure belongs to: capability limit. Model generation: OpenAI and Google internal data to Nov 2026. Cost: none.
- Against Ben's starting positions: limits Q2 and Q4 (long unattended runs need frequent checks).

### R-LIB-FAILURES-31
- Claim: Naam argues more parallel agents buy speed but little extra problem-solving, with steeply falling returns.
- Kind: analyst interpretation (others' benchmark data, unchecked)
- Quote: "OpenAI reported 124x the token use / researcher, but only 1.6x as many experiments." "Solving a problem faster is different from solving a harder problem your best model couldn't solve."
- Where: Source "Ramez Naam: more parallel agents buy speed, not much more intelligence" (X thread, 19 Oct 2026)
- Speaker and interest: as row 30.
- Read: part (words of 25 posts; charts and post 17's reasons missing)
- Bears on: parts 8, 11, 14; Q7. Failure belongs to: capability limit. Model generation: "Opus 5.5", "GPT-5.6 Sol". Cost: none.
- Against Ben's starting positions: not applicable to Q1/Q2; cautions against agent count as a design lever.

### R-LIB-FAILURES-32
- Claim: Witkin argues the lack of measured AI payoff outside tech is not only slow adoption, and lists structural limits including tacit knowledge that cannot be written down.
- Kind: hypothesis (argument; the two cited data sources were not captured)
- Quote: "the uncodifiability of much of humans' load-bearing tacit knowledge"; "user-sensitivity (output quality is a function of use quality)". Link card: "zero financial payoff to corporate America outside of tech" (Apollo's words, unverified).
- Where: Source "Nathan Witkin: missing AI payoff should move the maximalists…" (X, 24 Oct 2026)
- Speaker and interest: NYU researcher in a personal capacity; no stake evident.
- Read: full (post); the Apollo note and the paper it cites not read
- Bears on: parts 1, 6, 10; Q1, Q4, Q5. Failure belongs to: capability and know-how capture. Model generation: 2026. Cost: none.
- Against Ben's starting positions: limits Q1 (a full inventory assumes the work can be written down).

### R-LIB-FAILURES-33
- Claim: Huang's arithmetic: 99% per step finishes a 100-step task about a third of the time, so long tasks need a checker.
- Kind: hypothesis (arithmetic, not evidence)
- Quote: "A model that's 99% right per step finishes a 100-step task about 1/3 of the time." "you need someone checking the tower."
- Where: Source "Jessy Huang: AI has a 'god curve'…" (X thread, 20 Oct 2026)
- Speaker and interest: works in verification; possible stake in the answer.
- Read: full
- Bears on: parts 6, 8; Q2, Q3. Failure belongs to: compounding error. Model generation: 2026. Cost: none.
- Against Ben's starting positions: supports the verifier in Q2; adds that it must sit inside the task, not at the end.

## What this adds up to

Inference, not source statement. Of the failures held, few are plainly failures of the model. They sort roughly as: staffing or savings booked before the effect was measured (N001, N003); the check was a proxy or a clean test set (N002, N007, N004, B18); the tool worked and people did not use it (N016, B14, N063); spend ran ahead of any outcome measure (N006, N013); unmapped shared state between agents (N048, N045, the Anthropic proof); and capability on judgement-heavy multi-step work (N015, Naam). Ben's four requirements appear necessary. They were present in N007 and N016 and the work still failed or went unused, so they are not sufficient. What was missing in those cases was real incoming work in the test, a named owner, adoption effort, and a plan for the people left.

A roll-up looks especially exposed to five of these: (1) paying a price that assumes labour savings before a full cycle of demand is observed; (2) losing the seniors whose know-how the system needs, since acquisition itself prompts departures; (3) rolling one tool across many firms from a controlled test; (4) a long, uncosted first integration repeated per firm under transition-year debt; (5) clients taking the automatable work in-house while the saving is still being built. No held case measures any of the five in a roll-up.

## What is missing

- No failed or abandoned AI roll-up or holding company is recorded. The roll-up records (N059, N071, N072, F009, N073, N024) are self-reported and positive.
- No case of partner or staff departure, or client loss, after an acquisition. No earn-out failure. I searched Cases and Sources for these terms and found none.
- No adoption cost in money or hours in any case (L016 says so itself).
- No measured re-test that reversed a failure (L019 says so itself).
- Almost no case names the model generation; I have dated them by the source date instead.
- No failure involving a licensed signature, an insurer or a regulator's sanction.
- No UK accountancy or block-management failure. The nearest professional-firm case is B14, which is unchecked Pluris material.
- The Pluris collection (P001 to about P231) was searched by title only; it is promotional and records no failures.

## Not retrieved

- Fast Company's original Starbucks investigation (N002).
- Bloomberg's Ford article and Ford's earnings-call transcript (N003).
- OpenAI's 37-page incident report, and the CNBC and Guardian coverage (N048).
- The body of 404 Media's Proton article past the paywall, and the Proton CTO manifesto (N049).
- Permanent Equity's full 2025 annual letter (N015; only the X excerpt was read).
- Ramez Naam's two blog articles and all charts in both threads.
- The Apollo "Daily Spark" note and the paper at fion.ac/jellyfish.pdf cited by Witkin.
- The body of the Law.com International article of 7 October 2026 on where law firms waste AI spending (paywalled; only its opening is held, so no row was written).
- Records read but left out to keep to length: B9 (a classifier chosen over a language model; Pluris), N047 (Block's job cuts, attribution contested, no reversal yet), and the vendor-side effect of N002.
- The MAST paper's appendices (N045).
- The original pages behind B13, B14 (checkpluris.com), B18 (Harper) and B3 (Thrive Holdings): I read the library's imported records, which are marked "Imported unverified".
- The two X articles behind N007: I read the library record, not the articles.
- Synthesis A003 was not read for this piece; I relied on the case, finding and source records.
