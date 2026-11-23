# LIB-IMPROVE-TECH: evidence from the Thoughts Library on the improvement system, technology and data, and the back office

Parts 10, 11, 12. Questions Q4 and Q7. Read on 23 November 2026. Read-only; nothing in Notion was changed.

**How to read the rows.** For Sources (Blomfield, Chase, Smith, Stockton, june, DeepSeek Harness, Armstrong, Suh, Jansson, Notion, Relivs, Collison, Anthropic) I read the library page in full, including the captured text; "Read" says how much of the original that capture holds. For Cases (B and N numbers) I read the library's case record in full, not the underlying web source. Quotes from case records are the record's wording of the source unless shown in inner quotation marks. Every figure below is self-reported unless marked otherwise. None of the cases is independently verified.

Page links: all records are at `https://app.notion.com/p/<id>`; the id is given in each Where line.

## Rows

### R-LIB-IMPROVE-TECH-01
- Claim: Blomfield proposes a five-part loop: sensors, a policy layer, deterministic tools, a quality gate, and a learning step.
- Kind: proposal
- Quote: "a quality gate like that might be evals, deterministic checks, safety filters, human review for high risk stuff, and then a learning mechanism"
- Where: Source "Tom Blomfield (shared by Linas Beliūnas)", 4215f5db20d781fabe71d4969b6eef3c. Talk undated, at least six months older than the post that shared it.
- Speaker and interest: Y Combinator partner describing YC's own tools and its portfolio; YC gains if founders believe small teams suffice. He calls the talk "pretty conceptual and high level".
- Read: part (machine transcript excerpts of a 13-minute talk; video not watched)
- Bears on: 10, 8; Q4, Q3
- Against Ben's starting positions: supports "orgs constantly self improving" as a design; limits Ben's four requirements (adds a policy layer and a learning step)

### R-LIB-IMPROVE-TECH-02
- Claim: At YC a monitoring agent reads every staff query, writes a fix overnight, and a second agent reviews and merges it; no human approval, rollback or measured outcome is described.
- Kind: company claim
- Quote: "put in a merge request [...] Have an agent review it and merge it and deploy it so when a human comes the next day to ask the same query, it will now succeed."
- Where: same record as R-01
- Speaker and interest: as R-01. Internal knowledge tool at an investor, where a wrong answer is cheap.
- Read: part
- Bears on: 10; Q4
- Against Ben's starting positions: supports that a loop can run; limits it to low-stakes internal queries

### R-LIB-IMPROVE-TECH-03
- Claim: The same speaker says nobody has a firm that improves itself in every function, and his second example is a manual where new advice is merged or dropped.
- Kind: company claim
- Quote: "I'm not sure anyone has a truly self improving company in every function." And: "Every new piece of advice we give, it's compared with the existing user manual and either incorporated or thrown away."
- Where: same record as R-01
- Speaker and interest: as R-01. "Dramatically better" is his judgement; no test described.
- Read: part
- Bears on: 10, 15; Q4
- Against Ben's starting positions: limits "constantly self improving" (the strongest advocate concedes no whole-firm case)

### R-LIB-IMPROVE-TECH-04
- Claim: LangChain separates the agent that flags a knowledge gap from a background curator agent that fixes it, and advises starting from one workflow.
- Kind: company claim (design) with a proposal
- Quote: "Asking agents - who are mainly trying to accomplish their own goals - to properly update and maintain this knowledge will cause it to become unruly and full of contradictions." And: "Start with one recurring workflow, inspect where agents struggle, and close that loop."
- Where: Source "Harrison Chase: build a knowledge factory", 4215f5db20d7814ebe98dc4f000659f2, 21 Nov 2026
- Speaker and interest: vendor and operator; the article ends "please reach out, we can help!". No results given. Who checks the curator, and how stale knowledge is retired, is not said.
- Read: part (first part of the article captured; the rest cut)
- Bears on: 10, 11, 6; Q4, Q1, Q7
- Against Ben's starting positions: supports continual improvement; contradicts "list out the 200 things" as the first move ("The goal isn’t to document everything before agents can start working")

### R-LIB-IMPROVE-TECH-05
- Claim: Deel scores each run, has a nightly review propose instruction edits, and sends every write through a two-pass approval.
- Kind: company claim
- Quote: "outcomes scored as succeeded, blocked or errored; nightly review proposing instruction edits"; design standard quoted from Deel: "for work that touches someone's pay, right most of the time isn't right"
- Where: N005, 4215f5db20d78106a299c02e30a97497. Engineering post 30 Sep 2026.
- Speaker and interest: Deel, which also sells the platform. Claimed expense automation "from 78% (prior rules-based) to 90%". Not reported: "escalation rate, failure rate, cost per case". Its own sources conflict (100,000 against 250,000 cases a month).
- Read: full record; source not opened
- Bears on: 10, 12, 8; Q4, Q7
- Against Ben's starting positions: supports a self-improving back office in outline; who approves an instruction edit and how it is undone are not stated

### R-LIB-IMPROVE-TECH-06
- Claim: Sierra's role-per-agent design failed and was collapsed into one agent built by a six-person team; its nightly self-reflection is experimental and outcomes are unmeasured.
- Kind: company claim
- Quote: "nightly self-reflection proposing skill improvements (experimental)"; the author says the company has "no good way yet to measure whether deals close faster or issues resolve first time"
- Where: N012, 4215f5db20d781d08b31f8c41658dce5, post of 9 Jul 2026
- Speaker and interest: Sierra engineer; Sierra sells agents. 75,000+ sessions and 70% of PRs are activity, as the author says.
- Read: full record; source not opened
- Bears on: 10, 11, 8; Q4, Q7
- Against Ben's starting positions: limits (a well-resourced AI vendor cannot yet show the loop works); supports one agent over many (A001)

### R-LIB-IMPROVE-TECH-07
- Claim: One tax domain took about six weeks and heavy engineering oversight, and early practitioner corrections mixed real errors with preferences and stale values.
- Kind: company claim, with the library analyst's interpretation
- Quote: "one rental-income domain took about six weeks and substantial engineering oversight to reach 90 percent precision and recall"; "practitioner corrections interpreted before being used as evaluation data"
- Where: B3, 4215f5db20d78114a953fa5475d9c6b2, source undated (Thrive Holdings)
- Speaker and interest: a holding company that owns accounting firms; OpenAI holds equity in it. "later domains were cheaper", with no figure. Maintenance cost unreported.
- Read: full record; source not opened. Record is "Imported unverified".
- Bears on: 10, 14, 6; Q4, Q6
- Against Ben's starting positions: limits (a correction is not a signal until someone adjudicates it); gives the only per-domain build time in the library

### R-LIB-IMPROVE-TECH-08
- Claim: Integral's development agents propose pull requests, not direct changes, and are tested on synthetic companies run through real interfaces.
- Kind: company claim
- Quote: "development agents propose pull requests rather than pushing to main; synthetic companies driven through real interfaces to reproduce weeks-long onboarding and close states"
- Where: B16, 4215f5db20d78198a1c4e4b8f7913592, source undated
- Speaker and interest: an accounting, tax and payroll service describing its own engineering. "most proposals reportedly pass without edits, with no rate given".
- Read: full record; source not opened. "Imported unverified".
- Bears on: 10, 11; Q4, Q7
- Against Ben's starting positions: supports (a verifier as infrastructure); adds a test bed as a stack layer Ben does not list

### R-LIB-IMPROVE-TECH-09
- Claim: Spawn lets agents change live systems with no pull requests, relying on tests every fifteen minutes, thirty-second rollback and hard-coded gates on irreversible actions.
- Kind: company claim
- Quote: "1,055 of 123,548 changes reverted over a year (0.9 percent)"; "about \$3.1 million a month on tokens plus the compute bill is the complete cost, with no revenue or baseline stated"
- Where: B33, 4215f5db20d78177bf7ad605be79464a, post of 28 Oct 2026
- Speaker and interest: founder of a ten-person games company; says it is among one model vendor's largest customers. Judges are built from "two years of recorded decisions".
- Read: full record; source not opened. "Imported unverified".
- Bears on: 10, 11, 14; Q4, Q3, Q7
- Against Ben's starting positions: supports the loop where errors show in minutes and undo takes seconds; limits it for client work where "outcomes arrive late" (the record's own caveat)

### R-LIB-IMPROVE-TECH-10
- Claim: Fintool gates every change to its agents on an evaluation set and says context preparation was most of the work.
- Kind: company claim
- Quote: "~2,000 eval cases including adversarial grounding; PRs blocked if eval score drops more than 5%"; "parsing pipeline described as 80% of the work"
- Where: N017, 4215f5db20d7815193f5d5b7e10e64f0, post of 24 Jan 2026
- Speaker and interest: founder promoting a product. "No customer outcomes or error rates in production."
- Read: full record; source not opened
- Bears on: 10, 11; Q4, Q7
- Against Ben's starting positions: supports the verifier requirement; a regression gate is the nearest thing in the library to an approval rule for changes

### R-LIB-IMPROVE-TECH-11
- Claim: A fixed quoting workflow passed its synthetic tests and failed in production; recovery came from operators writing the instructions.
- Kind: company claim
- Quote: "synthetic-eval success 92.8% versus 22.3% in production for the fixed RFQ workflow"; "operators built their own narrow agents within days"
- Where: N007, 4215f5db20d781bdb215f65724a45efa, posts of 20 and 27 Jan 2026
- Speaker and interest: the implementer; client unnamed. No post-agent success rate reported.
- Read: full record; source not opened
- Bears on: 10, 6; Q4, Q2
- Against Ben's starting positions: contradicts the four-requirements test as sufficient (state, playbook, write path and an evaluator all existed and it still failed on vague inputs)

### R-LIB-IMPROVE-TECH-12
- Claim: Varick agrees baseline measures with finance before building, keeps agents mostly deterministic, and runs them in shadow against staff postings before go-live.
- Kind: company claim
- Quote: "build agents ~85% hard-coded with AI only for judgement"; "close 18-22 days to 7-9; [...] cost per invoice \$13 to \$6" (one unnamed rollout, against its own pilot baseline)
- Where: N050, 4215f5db20d781ada02acb91300cc065, posts of 30 Oct 2026
- Speaker and interest: implementer selling paid pilots; client unnamed; figures unaudited. "client owns them at month 6".
- Read: full record; source not opened
- Bears on: 12, 10, 11, 14; Q4, Q7
- Against Ben's starting positions: supports the back office as the proving ground; shows how to know a loop works (elapsed time and exceptions, not logins)

### R-LIB-IMPROVE-TECH-13
- Claim: Chroma proposes keeping a register of failed uses and re-testing it with each better model; nobody is reported to have done it.
- Kind: proposal
- Quote: "keep a graveyard of failed use cases with reasons and re-test it when a better model arrives"; the record adds "no evidence the graveyard practice has been used or measured"
- Where: N053, 4215f5db20d781688c6fdb41d481cdcb, Oct 2026
- Speaker and interest: investor white paper; promotional.
- Read: full record; source not opened
- Bears on: 10, 15; Q4
- Against Ben's starting positions: supports; it is the only library item on the "models get better" loop as a routine

### R-LIB-IMPROVE-TECH-14
- Claim: Applied Compute retrains customer models from production traces, and the reward design is where "correct" gets defined.
- Kind: company claim
- Quote: "continual improvement from production traces (online RL, self-distillation, A/B release)"; cost per cell "54.8% lower than Claude Sonnet 5" on the vendor's own benchmark
- Where: N070, 4215f5db20d781438ea8f78a0111e79a, announcement of 2 Nov 2026
- Speaker and interest: vendor; benchmarks built by the vendor. The record notes "there is no services-firm case".
- Read: full record; source not opened
- Bears on: 10, 11; Q4, Q7
- Against Ben's starting positions: limits (works on high-volume, machine-gradable calls; named customers are software firms)

### R-LIB-IMPROVE-TECH-15
- Claim: Collison lets any user submit a change that an agent implements with no review, and doubts it scales beyond personal tools.
- Kind: observed result (first-hand, anecdotal)
- Quote: "an agent that yolo implements whatever is submitted"; "Does it become unmaintainable after a while?"; "Can software designed this way be secure and reliable?"
- Where: Source "Patrick Collison: an improvements box", 4215f5db20d78137b5e8eaa33a2328ea, 31 Oct 2026; also case N057
- Speaker and interest: Stripe CEO on his personal apps; no product promoted.
- Read: full
- Bears on: 10, 3; Q4
- Against Ben's starting positions: supports who should propose (the person who feels the friction); limits ungated change to settings with no shared users or controls

### R-LIB-IMPROVE-TECH-18
- Claim: Coinbase's CEO says his agents' output still needs major changes and taxes the reviewers; a shared store of lessons is his hoped-for remedy.
- Kind: company claim (the problem) and hypothesis (the remedy)
- Quote: "many of the PRs still require major changes, and create a heavy tax on the team to review and modify"; "the number of required edits should decrease over time"
- Where: Source "Brian Armstrong", 4215f5db20d781a3be86c5c3ce6b09d4, 20 Nov 2026
- Speaker and interest: operator admitting a cost. The "Brain" is not defined; no figures.
- Read: part (post text only; diagram and clip not captured)
- Bears on: 10, 9; Q4
- Against Ben's starting positions: limits (the review burden lands on other people before any loop pays back)

### R-LIB-IMPROVE-TECH-21
- Claim: The library's finding is that a correction must be classed before it is learned from, and no case reports how often the correction process is itself wrong.
- Kind: analyst interpretation
- Quote: "Separate factual error, preference, task objective and obsolete carried-forward values; agreement with a reviewer is not proof of better customer outcomes." Open question: "None of the cases reports the error rate of the correction process itself."
- Where: L005, 4215f5db20d7816aa61df1ff6d676e97, status "Supported by reports", updated 4 Nov 2026
- Speaker and interest: library analyst, from B3, N005, N007, N063, N070, F013.
- Read: full
- Bears on: 10; Q4, Q2
- Against Ben's starting positions: limits (a correction signal with known meaning is a fifth requirement)

### R-LIB-IMPROVE-TECH-22
- Claim: In Scribe's test a wiki alone helped the model, recordings helped more, and results fell only when the wiki was added on top of recordings.
- Kind: observed result (vendor's own small test)
- Quote: "Adding either the wiki or the recordings improved its performance by more than half, but the workflow recordings beat the wiki on every measure we scored." Caveat: "this is one experiment, run on one model and graded by that same model."
- Where: Source "Jennifer Smith (Scribe)", 4215f5db20d7818f9a10f01acad08ff4, 19 Nov 2026
- Speaker and interest: CEO of a firm that sells workflow recording; the winning condition is her product. Thirty tasks, no numbers beyond "more than half".
- Read: part (excerpts of a fully retrieved article)
- Bears on: 11, 10, 6; Q4, Q7, Q1
- Against Ben's starting positions: limits "full context" (more stored context is not the same as knowing what matters); does not show a wiki makes agents worse

### R-LIB-IMPROVE-TECH-23
- Claim: Stockton says the binding work is organisational: taking people off daily work to write down procedures nobody has described.
- Kind: analyst interpretation (a consultant's opinion), same origin as R-22
- Quote: "You have to decide it's worth the time to step away from the day-to-day work, in order to build these types of assets"
- Where: Source "Matt Stockton", 4215f5db20d781078fdcfe94e3617c80, 21 Nov 2026. Rests on the Scribe article; counts with R-22 as one piece of evidence on the test.
- Speaker and interest: AI consultant paid for this kind of work. His summary of the test ("adding access to the wiki degraded performance") overstates it.
- Read: full
- Bears on: 10, 7; Q4, Q1
- Against Ben's starting positions: supports that the improvement system is a management decision, not a tool

### R-LIB-IMPROVE-TECH-24
- Claim: Anthropic's report says unlogged work is discouraged, not that everything is logged, and records the cost of stale records and of attention.
- Kind: observed result (a company's study of itself)
- Quote: "Private work, in unlogged meetings and direct messages, is invisible, confusing and discouraged in an AI-heavy workplace." Also: "reading all the output of their Claude agents would take half their work week."
- Where: Source "Anthropic: how employment is changing inside Anthropic", 4215f5db20d781439531d0c04eb041aa, undated
- Speaker and interest: four Anthropic researchers on their own employer, which sells the agents. A stale document "meant agents kept bringing requests for t-shirts and mugs".
- Read: part (excerpts of a fully retrieved report)
- Bears on: 10, 9, 11; Q4, Q3
- Against Ben's starting positions: limits "full context" (pressure, not total capture; a software firm with no client confidentiality)

### R-LIB-IMPROVE-TECH-25
- Claim: In the one first-hand build, mail and calendar missed the commitments made on calls, so the owner's word was the main source.
- Kind: observed result (one user) with a hypothesis drawn from it
- Quote: "101 past calendar entries in 31 days against 11 recorded notes in 45 days; transcript scope granted but unused"
- Where: L021, 4215f5db20d781ae9bcae92ef3aeef15 (Hypothesis); A002 lesson X5; case N063. 3 Nov 2026.
- Speaker and interest: library analyst reading the owner's own build; one user, one firm, no outcome measured.
- Read: full
- Bears on: 10, 11; Q4, Q7
- Against Ben's starting positions: limits "full context" (capture is bounded by the channel; consent and confidentiality rules are named as a condition, not examined)

### R-LIB-IMPROVE-TECH-26
- Claim: Records that people must enter by hand were abandoned in the held build; records made as a by-product of work survived.
- Kind: hypothesis, supported by one build and reports
- Quote: "A removed CRM and four abandoned task lists in one owner's workspace follow this pattern." And: "agent entry moves the cost to the agent's reading rather than removing it"
- Where: L022, 4215f5db20d781629e4fc19cbd8e0d92 (Hypothesis), updated 11 Nov 2026; A002 lesson X6
- Speaker and interest: library analyst; forward-untested. Limit: N049, "A mandate can force entry".
- Read: full
- Bears on: 11, 10, 7; Q4, Q7
- Against Ben's starting positions: limits any design that asks staff to feed the context store

### R-LIB-IMPROVE-TECH-27
- Claim: The asset in the build was maintained state with identities; the failure was layered handovers that held several answers to one question.
- Kind: observed result (one build, two reviews)
- Quote: "One current-state record per fact, with history separate; appended handovers recreate the contradictions the system exists to remove"
- Where: A002 lesson X9 and section 3, 4215f5db20d7819bb2eeec0067167077, 3 Nov 2026; L002 (status "Contested"), 4215f5db20d781e0b5c6e89724ff5301
- Speaker and interest: library analyst. A002's own rival reading: "the contradictions came from several agents writing in one day, not from the append style."
- Read: full
- Bears on: 11; Q7
- Against Ben's starting positions: supports "state an agent can read" and tightens it; sits against june's proposal of an append-only event log (source read, no row)

### R-LIB-IMPROVE-TECH-28
- Claim: Pulling data became cheap after the first capture; reading it against state recurred every run; no token, money or owner-time figure was recorded.
- Kind: observed result (untimed) and hypothesis
- Quote: "Tokens, money, owner minutes | Not recorded anywhere"; "the 40-minute run went mostly on 11 full reads and about 50 record changes (split untimed)"
- Where: A002 section 2; L023, 4215f5db20d78197a8d5fcdc1dc37f23 (Hypothesis), 3 Nov 2026
- Speaker and interest: library analyst. Challenged by N046: at company scale the access layer was most of the work.
- Read: full
- Bears on: 11, 14; Q7
- Against Ben's starting positions: not applicable to a stated position; shows the cost-control layer was absent in the only first-hand build

### R-LIB-IMPROVE-TECH-29
- Claim: The first-hand build ran with three of Ben's four requirements; the verifier was the owner, and the write gate was a rule the agent followed, not code.
- Kind: observed result (one build)
- Quote: "Verifier per kind | Not built. Twelve regression cases are specified"; "a rule followed by an agent is not a gate tested against an adversarial case"
- Where: A002 section 3, 4215f5db20d7819bb2eeec0067167077
- Speaker and interest: library analyst; the owner commissioned and corrected the build. "The playbooks were written by agents and reviewers, not derived from the owner's corrections".
- Read: full
- Bears on: 10, 6; Q2, Q4
- Against Ben's starting positions: limits (usable state was produced without a verifier at low volume; no improvement loop ran)

### R-LIB-IMPROVE-TECH-30
- Claim: Sierra's shared connection layer took about one and a half engineers over months, and the hard part was permissions, tenancy tagging and audit.
- Kind: company claim
- Quote: "About 1.5 engineers over months; existing identity platform"; "Legal and compliance sign-off depended on the access-control and audit system."
- Where: N046, 4215f5db20d781839f87e407f9950eee; engineer's diary and a WorkOS post of 11 Sep 2026
- Speaker and interest: Sierra engineer; WorkOS sells identity products. Also: coding agents "cheat" in self-verification. The official Sierra post was read only through a third party.
- Read: full record; source not opened
- Bears on: 11, 13; Q7
- Against Ben's starting positions: not applicable; the library's one people-cost figure for the permissions and audit layer (build, on an identity system already owned)

### R-LIB-IMPROVE-TECH-31
- Claim: Ramp reports a \$1.5m token bill in one week and answers it with a cost meter per project and a model router.
- Kind: company claim
- Quote: "one week in May 2026 cost \$1.5m in tokens"; "moving Ramp's own work onto the router cut the bill 30% 'overnight'"; "323 employees made 6,500+ edits to what Glass knows"
- Where: N013, 4215f5db20d78148b08ee9b3ca30c8b4, post of 13 Oct 2026
- Speaker and interest: co-founder's launch post for a product; no method for any figure.
- Read: full record; source not opened
- Bears on: 11, 14; Q7
- Against Ben's starting positions: not applicable; shows cost control is a layer to design from day one

### R-LIB-IMPROVE-TECH-32
- Claim: Block spent about nine months building one open-source agent, grades autonomy by how checkable the task is, and its users discard bad sessions instead of correcting them.
- Kind: company claim
- Quote: "About nine months of internal development before release"; "users discard bad sessions rather than correct them"
- Where: N047, 4215f5db20d781e0aed5dff69ed1f758; Fortune 6 Mar 2026 and a 2025 team interview
- Speaker and interest: executives speaking in a layoff context; the 40% productivity figure has no method.
- Read: full record; source not opened
- Bears on: 11, 10; Q7, Q4
- Against Ben's starting positions: limits the loop (if people discard and retry, no correction is captured)

### R-LIB-IMPROVE-TECH-33
- Claim: Long Lake says most of its platform is shared across sectors but each firm still needs data clean-up and engineers on site for about two years.
- Kind: company claim
- Quote: "about 80% of the infrastructure is shared across verticals"; engineers "'in your office for the next 2 years'"; "The first acquisitions took over a year to show business outcomes"
- Where: N071, 4215f5db20d781b8a9afd7d3207ffaa2, interview of 11 May 2026
- Speaker and interest: CEO on a podcast hosted by one of his investors; unaudited; overlaps N059, N060, N072.
- Read: full record; source not opened
- Bears on: 11, 4, 14; Q7, Q6
- Against Ben's starting positions: supports a shared platform; limits it (the per-firm cost is people, for years)

### R-LIB-IMPROVE-TECH-34
- Claim: Bonsai stopped automating around clients' software after a vendor blocked it, and now replaces the system of record at a stated price.
- Kind: company claim (management on a call, and marketing)
- Quote: "a TMS vendor refused to allow order-entry automation"; "a EUR 200k project takes about one person at roughly 70% margin"; Cabooter paid "EUR 52k one-off plus EUR 750 a month"
- Where: N064, 4215f5db20d7819eb97df2dfdb4a1ada, call notes 3 Nov 2026, updated 11 Nov 2026
- Speaker and interest: implementer pitching to the owner's firm; savings are "calculated", not measured; its own figures conflict.
- Read: full record; sources not opened
- Bears on: 11, 5; Q7
- Against Ben's starting positions: not applicable; adds a buy-or-replace decision on systems of record, and the risk that an incumbent vendor withholds the write path

### R-LIB-IMPROVE-TECH-36
- Claim: A former Long Lake founding-team member says storing company memory is easy, the hard part is deciding what to remember, and each firm's process is bespoke.
- Kind: hypothesis (forecast and opinion)
- Quote: "Company brain: I don't think is particularly hard [...] They can just be markdown files." And: "Every company within a vertical shares the same 'noun' of 'review XYZ,' but the process by which each company evaluates and understands the information is bespoke."
- Where: Source "John Suh", 4215f5db20d7812db43ddc7f94f8e1c4, 21 Nov 2026
- Speaker and interest: building an unnamed product; expects "an independent company will own this product layer". No deployment or results. Replies dispute him: "Permissions are a nightmare and obligatory."
- Read: full
- Bears on: 11, 10; Q7, Q1
- Against Ben's starting positions: limits "turn them into products" across firms (bespoke process per firm); supports buying the context store cheaply

### R-LIB-IMPROVE-TECH-38
- Claim: Notion advises syncing everything into one governed store with a few linked databases and renting the model.
- Kind: proposal (vendor guide)
- Quote: "Rent the intelligence. Own the context."; "directly granting agents access to dozens of sources adds complexity, multiplies possible points of failure, and is exponentially harder to govern"
- Where: Source "Notion: A New Shape for Work", 4215f5db20d781ce99bae6223227a92c, undated
- Speaker and interest: the vendor of the store it recommends; says so. No evidence in the captured part.
- Read: part (about 56% captured; the sections on shared agents, governance and starting were not)
- Bears on: 11; Q7
- Against Ben's starting positions: supports a shared context store; R-22 is the direct objection

### R-LIB-IMPROVE-TECH-39
- Claim: DeepSeek's design puts one light router in front of isolated workers, filters events with fixed rules before any model call, adds an outside watchdog, and leaves security unsolved.
- Kind: proposal, with a small synthetic test
- Quote: "Deterministic policies remove noise before any large model is called"; "Unless security and privacy are handled well, a Super-agent can only work within a very small, trusted scope."; results are "indicative only"
- Where: Source "DeepSeek Harness", 4215f5db20d7816199ecf93a5d7263e7, 1 Nov 2026
- Speaker and interest: the product team; machine-translated; the test simulated work with a timer. "With the neutral prompt, the model did not call a subagent in any of the 5 runs."
- Read: part (excerpts of a fully retrieved article)
- Bears on: 11, 8, 13, 9; Q7, Q3
- Against Ben's starting positions: not applicable; adds triggers, a watchdog and a cap on interruptions ("a cap of 100 words per reply") as layers

### R-LIB-IMPROVE-TECH-40
- Claim: An investor essay claims finance teams now build their own agents and that the leanest aim for finance at 2% of headcount.
- Kind: company claim, second-hand
- Quote: "Anthropic finance maintains 70+ skills treated as production code"; "leanest teams target finance at 2% of headcount versus ~5%"; "Second-hand claims about named teams; no method."
- Where: N042, 4215f5db20d7813fa1b6fa850119fd38, 8 Oct 2026
- Speaker and interest: a16z partner promoting portfolio companies; unverified.
- Read: full record; source not opened
- Bears on: 12, 7; Q7
- Against Ben's starting positions: supports the back office as the place to start; the only headcount target in the library for it, and unverified

## Loop anatomy (from the rows above)

"Not stated" means the record I read does not say.

| Case | Proposes | Tests | Approves | Undo | Outcome measured |
| --- | --- | --- | --- | --- | --- |
| YC (R-02) | monitoring agent | not stated | a second agent | not stated | none |
| LangChain (R-04) | working agents flag; curator edits | not stated | not stated | not stated | none |
| Deel (R-05) | nightly review | run scoring | not stated for edits; owner or policy for writes | not stated | 78% to 90% claimed, no error rate |
| Sierra (R-06) | nightly self-reflection | not stated | not stated | not stated | none, by its own account |
| Thrive (R-07) | practitioner corrections, interpreted | benchmark | engineers | not stated | precision, recall, completion (claimed) |
| Integral (R-08) | development agents | synthetic companies | people (pull request) | version control implied | no rate given |
| Spawn (R-09) | agents | suite every 15 minutes | judges; person for held cases | 30-second rollback | 0.9% reverts; no revenue |
| Fintool (R-10) | engineers | ~2,000 eval cases | automatic gate | pull request blocked | none in production |
| Varick (R-12) | implementer | shadow mode | staff keep approvals | not stated | close days, cost per invoice (claimed) |
| Collison (R-15) | any user | none | none | not stated | count of changes |
| First-hand build (R-29) | owner and reviewers | none built | owner | change log; restore not rehearsed | none |

## What this adds up to

**Inference, mine.** The library holds many designs for a self-improving loop and no measured one in a services firm. Proposing is cheap and well covered. Testing exists only where a machine can check the work (code, ledgers, graded calls). Approval of a change to a procedure is almost never described. Undo is described once, at Spawn. Outcome is measured nowhere independently. So Ben's "static" criticism is fair as an aim, but the evidence supports a narrower design: a loop per workflow, with a regression set, a named approver for instruction changes, a rollback, and a baseline agreed first (Varick, Fintool, Integral). Three things recur as missing requirements beyond Ben's four: a classed correction signal (L005), a separate curator (Chase), and attention to review the output (Armstrong, Anthropic).

On the stack, the costs that appear are people, not software: about 1.5 engineers for permissions and audit, six for a company agent, six weeks per tax domain, engineers on site for two years. Storage looks cheap to buy. Permissions, evaluation sets, per-firm data clean-up and cost metering look like the work. The back office is the only place with baseline-style numbers, and all are vendor claims.

## What is missing

- Any loop with an independent measure of whether changes made the work better.
- Who may approve a change to a procedure, and any record of a bad change being caught and reversed in a services setting.
- Money cost of a stack for a firm of 30 to 50 people. The figures held are from software companies.
- Build against buy for the review queue, the evaluation sets and the improvement loop. Nothing found.
- What clients, staff and the law permit to be recorded. Named as a condition in L021 and absent elsewhere.
- Back office as a whole (HR, legal, compliance, IT, deal integration). Only finance and payroll appear.
- Chroma's "any owner can rent it" objection was not in my reading list. N023 (Artifact AI, a bought agent layer over existing ledgers, marketing claims only) bears on it indirectly.
- Read and given no row, to stay near the length limit: N027 (Claude Code team habits; "No measurements"), N033 (PostHog on loops; cost omitted), N023, the Jansson post (one person's skills database that the agent edits; no check described), the june post (a company's state as an append-only event log; no working example) and the Relivs post (a relayed talk; only the chapter title "one bad memory can poison your entire agent fleet" was captured, so it is unverified). Row numbers therefore have gaps.
- B10 (a P&L assistant, "100 percent accuracy reported for a pilot of unknown size") and B12 (a connector builder, "about ten times faster") were read and given no row. B10 rests on a Pluris page (checkpluris.com), so it is unchecked promotional material.

## Not retrieved

- The underlying web sources of every B and N case. I read the library's records only.
- The Blomfield talk video and its date and venue.
- The second part of Chase's "How to build a knowledge factory".
- The last 44% of Notion's "A New Shape for Work".
- The video behind the Relivs post, and its speaker's name.
- Brian Armstrong's workflow diagram and the David Senra clip.
- Full text of the Scribe, DeepSeek Harness and Anthropic originals beyond the library's stored excerpts.
- The build files behind A002 (`OBSERVATIONS.md`, the run notes), which sit on Ben's drive.
- The official Sierra post on its gateway (the library read it through WorkOS).
