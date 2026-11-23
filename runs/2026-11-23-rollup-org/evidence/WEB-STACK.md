# WEB-STACK: the technology stack and back office of firms running services work on agents

Outside web research, done 23 November 2026. Scope: Q7, parts 11 and 12, with spill into parts 8, 10 and 14.

How to read "Read". Pages were fetched and passed through an extraction step that returned quotations. "Part" means I saw the extracted passages, not every line of the page. "Summary only" means I saw a search summary or a secondary account and not the source itself. Quotations are as returned by the extraction; where one is a heading or was shortened, the row says so. The Klarna filing was downloaded and the quoted passages were read directly in the filing text.

One warning for the whole file. Almost no services roll-up has published an architecture account. The detailed layer-by-layer accounts come from large technology companies (Uber, Cloudflare, Block, Pinterest) and from model vendors describing their own offices. They show what the layers are and what they take. They do not show what a 30-person firm runs.

## A. Roll-ups and AI-native services firms

### R-WEB-STACK-01
- Claim: The tax system built for Thrive Holdings' accounting firms has an improvement loop in which practitioner corrections are logged, grouped, turned into evaluation targets, and a coding agent proposes a fix as a pull request.
- Kind: company claim
- Quote: "Every intervention feeds the product's improvement loop by recording exactly what Tax AI proposed"; "Codex can then help investigate, propose changes, validate them against targeted and regression evals"
- Where: https://openai.com/index/building-self-improving-tax-agents-with-codex/ (27 May 2026)
- Speaker and interest: Two Thrive Holdings engineers and two OpenAI staff. Operator and its model vendor writing together; OpenAI holds equity in Thrive Holdings and is selling Codex.
- Read: part
- Bears on: parts 6, 10, 11; Q2, Q4, Q7
- Against Ben's starting positions: supports "orgs constantly self improving"; adds a fifth requirement to his four (a logged correction signal). Note the loop improves software, by engineers' approval, not the firm's own playbooks.

### R-WEB-STACK-02
- Claim: In that loop engineers approve every change and unclear cases leave the loop; automation covers a bounded extraction and mapping layer only.
- Kind: company claim
- Quote: Engineers "remain responsible for architecture, product decisions, and shipping"; ambiguous cases "route back to the product team instead of being forced through the loop."
- Where: same post, 27 May 2026
- Speaker and interest: as R-01
- Read: part
- Bears on: parts 3, 8, 10; Q3, Q4
- Against Ben's starting positions: limits. The published "self-improving" case is human-gated at the change step and narrow in scope.

### R-WEB-STACK-03
- Claim: Reported pilot results are 7,000 returns, field completion rising over six weeks, about a third less preparation time and about 50% more throughput; none is independently checked and the accuracy figures differ between accounts.
- Kind: company claim
- Quote: "At launch, only a quarter of returns were at 75% correct field completion, but within six weeks, 86% hit that mark." Also "drafts returns with up to 97% accuracy" (as extracted). TechCrunch later reported "processed more than 7,000 tax returns at 98% accuracy."
- Where: OpenAI post above (27 May 2026); https://techcrunch.com/2026/08/12/openai-backed-thrive-holdings-raises-2b-to-bring-ai-to-the-enterprise/ (12 August 2026)
- Speaker and interest: Operator and vendor; TechCrunch repeating the company during a fund-raise. One origin, not two pieces of evidence.
- Read: part
- Bears on: parts 6, 14; Q2, Q7
- Against Ben's starting positions: not applicable. "Up to 97%" is a peak; 86% of returns at 75% of fields is the more modest stated result. The post does not say which tax software is written to or who signs.

### R-WEB-STACK-04
- Claim: Extending the system to one harder schedule (rental property) took about six weeks of engineer and practitioner time.
- Kind: company claim
- Quote: Automating rental-property returns "required six weeks of engineering and practitioner review to reach 90% precision and recall." "The work created reusable patterns that made it easier to extend Tax AI to other complex tax schedules."
- Where: https://openai.com/index/forward-deployed-engineering-means/ (22 October 2026)
- Speaker and interest: OpenAI, describing its own paid deployment service.
- Read: part
- Bears on: parts 6, 14; Q1, Q6, Q7
- Against Ben's starting positions: limits "list the 200 things and automate". One sub-type of one service cost six weeks. Head count is not given.

### R-WEB-STACK-05
- Claim: The only published figure on cost falling from first deployment to second comes from a semiconductor customer, not a services firm.
- Kind: company claim
- Quote: "We were able to remove roughly 90% of the custom code from each project." "In one August 2026 example, the initial deployment took two months. Extending the solution to a second team took one day." "In mid-2025, we had around 15 FDEs working with a large semiconductor customer on 10+ use cases."
- Where: same OpenAI post, 22 October 2026
- Speaker and interest: vendor
- Read: part
- Bears on: parts 4, 11, 14; Q6, Q7
- Against Ben's starting positions: not applicable. This is the shape of the number A003 asks for (latest against first) but from another industry and a second team in the same customer.

### R-WEB-STACK-06
- Claim: Thrive Holdings rents its model research capacity: OpenAI staff sit inside its companies, and Thrive's own engineers come from software start-ups.
- Kind: company claim
- Quote: "OpenAI will embed research, product, and engineering teams inside Thrive Holdings' companies"; "Thrive Holdings has built out a product and engineering team with veterans of startups including Harvey and Ramp"
- Where: https://openai.com/index/thrive-holdings (1 December 2025); https://www.newcomer.co/p/inside-the-vc-roll-up-craze-that (18 December 2025, mostly paywalled)
- Speaker and interest: OpenAI (vendor and shareholder); Newcomer (journalist, Madeline Renbarger)
- Read: part (Newcomer: visible portion only)
- Bears on: parts 2, 7, 11; Q6, Q7
- Against Ben's starting positions: not applicable. Shows a build-with-vendor route that depends on a vendor's equity interest.

### R-WEB-STACK-07
- Claim: Thrive's scale by August 2026 was over 70 businesses, with the accounting arm at over 50 firms; engineering head count is not disclosed.
- Kind: company claim
- Quote: "surpassed 70 businesses on Thrive Holdings' platforms"; "more than 50 firms and more than 2,000 professionals"; Shield "sped up help desk resolution times by 36x."
- Where: TechCrunch, 12 August 2026 (URL in R-03)
- Speaker and interest: journalist reporting company statements at a $2bn raise
- Read: part
- Bears on: parts 4, 11, 12; Q6, Q7
- Against Ben's starting positions: not applicable. "36x" has no stated baseline or method.

### R-WEB-STACK-08
- Claim: Long Lake says one platform, Nexus, runs across all its companies; its investor's account gives activity figures and no architecture, head count or cost.
- Kind: company claim (relayed by an investor)
- Quote: Long Lake "has completed 40 acquisitions and built a proprietary AI platform, Nexus, deployed across every company it owns." "Top-performing HOA managers are reclaiming over 65 hours per month." "We believe the early results support the thesis."
- Where: https://www.generalcatalyst.com/stories/manufacturing-outliers-long-lake (28 September 2026)
- Speaker and interest: General Catalyst partners; investor with a position.
- Read: part
- Bears on: parts 11, 14; Q7
- Against Ben's starting positions: not applicable. Hours reclaimed by "top-performing" managers is activity, and a selected group. A statement that "roughly 80% of the infrastructure is shared across the verticals" appeared only in a search summary of an interview; I did not read its source.

### R-WEB-STACK-09
- Claim: Shield (Thrive's IT-services arm) runs an internal platform called Forge; the claimed results concern one managed-services firm.
- Kind: company claim
- Quote: "Forge, an internal AI platform designed to automate MSP service delivery." "Shield says Forge can resolve over half of tickets stuck in the queue." "one MSP using the platform has reduced technician ticket-resolution time by roughly 70%."
- Where: https://www.channelinsider.com/video/ai-msps-beyond-support-tickets/ (29 September 2026)
- Speaker and interest: trade journalist (Victoria Durgin) relaying Shield
- Read: part (video transcript)
- Bears on: parts 11, 12; Q7, Q8
- Against Ben's starting positions: not applicable. Nothing on the ticketing or remote-management systems underneath, or on what is shared.

### R-WEB-STACK-10
- Claim: Lawhive, a UK and US law firm that buys firms, says it built its own agent system and is hiring practitioners to write acceptance criteria and evaluation sets per matter type.
- Kind: company claim (job advertisement)
- Quote: "we've built our own agentic operating system for legal services." "Turn that knowledge into product requirements, workflows and acceptance criteria that engineers can build against." "Build evaluation sets from real matter types and judge output quality as a practitioner would." "$190K – $270K / year"
- Where: https://jobgether.com/offer/6af3e1b71b1a9ee7d6628e65-legal-engineer (listing dated 11 November 2026; a job-board copy, not Lawhive's own page)
- Speaker and interest: employer recruiting
- Read: part
- Bears on: parts 7, 10, 11; Q2, Q6, Q7
- Against Ben's starting positions: supports the verifier leg of his four. Gives one real price for the role that writes playbooks and evaluation sets: a "first Legal Engineer" per practice area at $190–270K.

### R-WEB-STACK-11
- Claim: Ascend, a private-equity-backed US accounting platform, is reported to have a 30-person AI team working beside its accountants.
- Kind: company claim
- Quote: "they have a 30-person AI team that's working alongside their CPAs" (search summary of the podcast page; the transcript did not load). From the page itself only: AI "may well require rethinking the entire structure of the accounting firm"
- Where: https://www.accountingtoday.com/podcast/the-ai-native-firm (19 October 2026)
- Speaker and interest: David Wurtzbacher, Ascend's founder and chief executive, interviewed by a trade editor
- Read: summary only for the 30 figure
- Bears on: parts 7, 11, 14; Q6, Q7
- Against Ben's starting positions: not applicable. The one head-count figure found for a centre team at an accounting consolidator; unverified.

### R-WEB-STACK-12
- Claim: A holding company of new-built AI services firms shares back-end software and operations across them and claims small teams suffice.
- Kind: company claim
- Quote: "sharing back-end software and operations with the rest of Infinity's portfolio"; launched "with $17 million in investment and 8 subsidiary startups"; "a combined $7.1 million in annualized revenue"; "You don't need a team of 500 people anymore, you need a team of five people, or 10"
- Where: https://www.upstartsmedia.com/p/infinity-new-holdco-ai-services (27 May 2025)
- Speaker and interest: journalist (Alex Konrad) quoting Infinity's chief executive and its lead investor
- Read: part
- Bears on: parts 2, 12, 14; Q7, Q9
- Against Ben's starting positions: not applicable. Build-from-new vehicle. Eighteen months old; no later figures found.

### R-WEB-STACK-13
- Claim: In UK mid-tier accountancy, most firms have an AI strategy and few trust their workforce's readiness; about half are private-equity backed.
- Kind: observed result (survey by a professional body; self-reported by firms)
- Quote: "only 17% expressing confidence in this area." "Nearly half of responding firms are now PE-backed." (86% with a technology strategy that includes AI, and 68% expecting fewer early-career roles, were given in the extraction as figures, not quotations.)
- Where: https://www.icaew.com/insights/viewpoints-on-the-news/2026/may-2026/mid-tier-firms-focused-on-ai-and-consolidation (22 May 2026)
- Speaker and interest: ICAEW, the professional body and regulator of its members
- Read: part (article body; the underlying research report was not read)
- Bears on: parts 1, 7, 11; Q6, Q8
- Against Ben's starting positions: limits any assumption that UK targets arrive with a stack. The article says nothing on tools, spend or build against buy.

## B. Permissions, identity and audit

### R-WEB-STACK-14
- Claim: Uber built its own gateway between agents and internal services; every tool is off until its owning team reviews and enables it.
- Kind: company claim (engineering account by the operator)
- Quote: "is currently hosting over 800 MCP servers and over 5000 tools"; "Every MCP server and tool starts in a disabled state and must be explicitly reviewed and enabled by the owning team."; "discovery doesn't imply exposure."
- Where: https://www.uber.com/blog/designing-mcp-gateway/ (1 October 2026)
- Speaker and interest: three Uber engineers describing their own system; no product to sell
- Read: part
- Bears on: parts 3, 8, 11; Q3, Q7
- Against Ben's starting positions: adds to his four: "authority and limits on action" is a built layer with named owners. Team size and cost are not stated.

### R-WEB-STACK-15
- Claim: At Uber the gateway strips personal data from tool responses and treats a change to a tool's description as a change needing the owner's approval.
- Kind: company claim
- Quote: "MCP Gateway also does out-of-the-box redaction for any PII or sensitive data from the tool responses." "Every change to the tool description triggers a config change diff, which must be approved by server owners." "If you're building agentic systems at scale, the hardest part isn't the AI."
- Where: as R-14
- Speaker and interest: as R-14
- Read: part
- Bears on: parts 3, 10, 13; Q3, Q4, Q7
- Against Ben's starting positions: supports change control on procedures (Q3). The post does not describe audit logs.

### R-WEB-STACK-16
- Claim: Cloudflare has a central team running a shared platform for agent tool servers, with access policy, login records, per-employee token limits and detection of unapproved servers.
- Kind: company claim (operator who also sells the components)
- Quote: "This team built a shared MCP platform inside our monorepo"; "Our administrators can see who logged into what MCP portal"; "to enforce cost controls (by limiting the number of tokens each employee can burn through)"; "to find remote MCP servers that are not being accessed via an MCP server portal"
- Where: https://blog.cloudflare.com/enterprise-mcp (14 April 2026)
- Speaker and interest: Cloudflare staff; the stack is built from products Cloudflare sells, so this is also marketing
- Read: part
- Bears on: parts 8, 11, 12, 13; Q7
- Against Ben's starting positions: not applicable. Shows that this layer can be bought. Team size not disclosed.

### R-WEB-STACK-17
- Claim: Block wrote all its internal tool servers itself and restricts which models may call which tools and which data categories the agent may touch.
- Kind: company claim
- Quote: "all MCP servers used internally are authored by our own engineers." "MCP allows us to define which models can invoke which tools"; "we restrict Goose from being used with certain categories of sensitive data, in line with internal policies." "Most employees report saving 50–75% of their time on common tasks"
- Where: https://goose-docs.ai/blog/2025/04/21/mcp-in-enterprise (21 April 2025)
- Speaker and interest: Angie Jones, Block's head of developer relations, promoting Block's open-source agent
- Read: part
- Bears on: parts 8, 11, 13; Q3, Q7
- Against Ben's starting positions: not applicable. The time saving is self-reported activity. Nineteen months old.

### R-WEB-STACK-18
- Claim: Pinterest is reported to run a central registry of approved tool servers with two layers of authorisation and limits on high-privilege actions.
- Kind: company claim (seen through secondary summaries)
- Quote: "high-privilege actions (e.g., modifying production DAGs) are restricted to approved teams"; "MCP tools are saving on the order of 7,000 hours per month." (both as given in search summaries)
- Where: https://medium.com/pinterest-engineering/building-an-mcp-ecosystem-at-pinterest-d881eb4c16f1 (19 March 2026; returned 403)
- Speaker and interest: Pinterest engineer (Tan Wang), per the summaries
- Read: summary only
- Bears on: parts 8, 11; Q3, Q7
- Against Ben's starting positions: not applicable. Shares no origin with Uber or Cloudflare; a third independent firm choosing registry-plus-gateway. Hours saved is activity.

### R-WEB-STACK-19
- Claim: Operators advise a registry of every agent, an owner per agent, separate identities, a review before release and a rule for retiring agents; one firm takes six to eight weeks per agent.
- Kind: company claim (several operators quoted by a journalist)
- Quote: Fujifilm Biotechnologies: "from idea to release is typically six to eight weeks." "Agents can drift from the guardrails that you set up for them." DaVita: "We assess compliance, cybersecurity, governance and business value before broader adoption." Consultant: "Treat an agent like a product with an owner, not a project with an end date."; "Forgotten agents with live credentials are a real risk."
- Where: https://www.cio.com/article/4246026/as-employees-build-ai-agents-cios-manage-the-lifecycle.html (11 November 2026)
- Speaker and interest: chief information officers describing their own firms; one consultant (Hylaine) who sells this advice. DaVita is said to have "more than 10,000 agents"; Fujifilm about 50 builders among 5,000 eligible staff.
- Read: part
- Bears on: parts 3, 8, 9; Q3, Q7
- Against Ben's starting positions: supports adding a named owner and a retirement rule to his four.

## C. Verifiers, review queue and the correction signal

### R-WEB-STACK-20
- Claim: Ramp's expense agent decides most approvals alone, sits under hard-coded limits, and falls back to the old human process when unsure.
- Kind: company claim (vendor describing its own product in use at itself and customers)
- Quote: "Since enabling the policy agent at Ramp, we've seen more than 65% of approvals be fully handled by the agent." "We layer deterministic rules on top: dollar limits, vendor blocklists, category restrictions." "When the agent isn't sure, we fall back to the pre-agent escalation process users are accustomed to."
- Where: https://engineering.ramp.com/post/how-to-build-agents-users-can-trust (date not shown on the page as retrieved)
- Speaker and interest: Ramp engineering; sells the product
- Read: part
- Bears on: parts 3, 6, 8, 12; Q2, Q3, Q7
- Against Ben's starting positions: bears on the L014 against N076 dispute: this is limits-and-budgets with review only on suspicion, not approval at each step. The 65% figure is from Ramp's own use.

### R-WEB-STACK-21
- Claim: Ramp found that a user's correction cannot be taken as the right answer without checking.
- Kind: company claim (a design lesson from an operator-vendor)
- Quote: "Every user-flagged error should be a candidate for your evals." "If we always took the user's action as the ground truth, the LLM could have been too lenient."
- Where: as R-20
- Speaker and interest: as R-20
- Read: part
- Bears on: parts 6, 10; Q2, Q4
- Against Ben's starting positions: limits a simple "learn from corrections" loop. Matches the Thrive post's point that corrections include "expected workflow noise" (R-02). Two independent operators.

## D. The back office: finance, legal, HR, IT

### R-WEB-STACK-22
- Claim: Anthropic's finance team uses packaged skills for reconciliations and commentary as a first pass, with people editing; the account names no formal control.
- Kind: company claim (vendor describing its own office)
- Quote: "GL-to-subledger and bank reconciliations, with breaks classified and reviewer commentary drafted as a first pass."; "free up 10 to 20 hours a week for higher-impact work."; "the team spends their time on judgment and making the call, not on the first draft."
- Where: https://claude.com/blog/how-anthropics-finance-team-uses-claude-to-shape-the-narrative-behind-the-numbers (22 May 2026)
- Speaker and interest: Alice Fong, Anthropic corporate finance; the firm sells the tool
- Read: part
- Bears on: part 12; Q7
- Against Ben's starting positions: supports the back office as a proving ground in a weak sense. Hours freed is activity; no close-time or error figure is given.

### R-WEB-STACK-23
- Claim: Anthropic's legal playbooks are plain text files a lawyer wrote in an afternoon, and the firm itself says the tool is not proprietary.
- Kind: company claim
- Quote: "The plugin is markdown files that tell Claude how Anthropic's legal team thinks about risk." The team "built the Legal plugin in an afternoon." It is public because "there's nothing proprietary about it." Finance: "connecting Claude Cowork to the data warehouse via MCP and asking ad-hoc questions against live data"
- Where: https://claude.com/resources/guides/deploying-claude-across-your-organization/how-anthropic-teams-use-cowork (undated; footer 2026)
- Speaker and interest: vendor guide
- Read: part
- Bears on: parts 5, 10, 11, 12; Q5, Q7
- Against Ben's starting positions: supports Chroma's objection that back-office automation can be rented by any owner; the firm-specific part is the playbook content. Bears on Q5: the playbook format is not the scarce thing.

### R-WEB-STACK-24
- Claim: Anthropic's legal team reports one turnaround figure and keeps lawyers on final judgement.
- Kind: company claim
- Quote: "turnaround dropped from two to three days down to 24 hours." "Use AI for the first pass, triage, and drafting, not final judgment." "I still read the blog post. I'm still reviewing the work."
- Where: https://claude.com/blog/how-anthropic-uses-claude-legal (8 December 2025)
- Speaker and interest: Mark Pike, associate general counsel at the vendor
- Read: part
- Bears on: parts 12, 13; Q3, Q7
- Against Ben's starting positions: not applicable. The page does not address privilege. Same origin as R-22 and R-23: one firm.

### R-WEB-STACK-25
- Claim: Klarna's filing gives the most checkable account of a support function moved to an agent, with the estimating method stated.
- Kind: company claim in a regulatory filing (carries liability for misstatement; not an audited operating metric)
- Quote: "Our AI assistant handled 80% of customer service chats in the year ended December 31, 2025, according to our service chat log data, doing the work equivalent of over 850 full-time agents (estimated based on the average monthly reduction in chat and telephone conversations handled by full-time agents in 2025 following the launch of our AI assistant), and in 2025 delivered approximately $59 million in cost savings."
- Where: Klarna Group plc Form 20-F for FY2025, https://www.sec.gov/Archives/edgar/data/2003292/000200329226000007/klar-20251231.htm (filed 2026; exact date not checked)
- Speaker and interest: issuer to its investors
- Read: part (passages read directly in the filing)
- Bears on: parts 12, 14; Q7
- Against Ben's starting positions: not applicable. Satisfaction is "according to internal consumer satisfaction surveys". Press reports that Klarna returned to hiring human agents in 2025 were seen only in search summaries.

### R-WEB-STACK-26
- Claim: Klarna attributes part of its gain to cutting bought software and suppliers and to an internal knowledge assistant across its systems.
- Kind: company claim in a regulatory filing
- Quote: "We also reduced or canceled contracts with over 1,700 suppliers following our AI adoption and standardization"; "we operate an internal knowledge chatbot, which we call Kiki, that helps employees find information in real time across internal systems."; "Our average annual revenue per employee at period end has increased from approximately $344,000 in 2022 to approximately $1,240,000 in the year ended December 31, 2025."
- Where: as R-25
- Speaker and interest: as R-25
- Read: part
- Bears on: parts 11, 12, 14; Q7
- Against Ben's starting positions: not applicable. Revenue per employee also reflects revenue growth and a hiring freeze; the filing does not separate these. Klarna is a software company with its own engineers, not a model for a 30-person practice.

### R-WEB-STACK-27
- Claim: A field study of small and mid-sized firms using one vendor's AI bookkeeping software found faster monthly close and more detailed ledgers, and found accountants following the software when it was unsure.
- Kind: observed result (academic; data from a software vendor's customers)
- Quote: "A 7.5 day reduction in monthly close time." "A 12% increase in general ledger granularity (a measure of reporting detail)." "When AI suggests diverging categories for uncertain transactions, accountants tend to still follow AI's suggestions"
- Where: MIT Sloan write-up of Choi and Xie, "Human + AI in Accounting", https://mitsloan.mit.edu/ideas-made-to-matter/how-generative-ai-can-make-accountants-more-productive (5 August 2025). Sample: "79 small and midsize firms", 277 accountants surveyed.
- Speaker and interest: academics (Stanford, MIT); the university's write-up; the vendor partner is unnamed
- Read: summary only (the paper itself was not read)
- Bears on: parts 6, 12, 14; Q2, Q7
- Against Ben's starting positions: supports the back office and bookkeeping as checkable first ground; limits reliance on a human reviewer as the verifier, since reviewers deferred to the tool. Pre-agent generation of tools.

### R-WEB-STACK-28
- Claim: Ramp's finance-close product records each agent session and stores recurring work as reusable skills; its public account gives no accuracy or close-time figure.
- Kind: company claim (vendor marketing; one line from Ramp's own controller)
- Quote: "Stack records every plan, source, action, and handoff in a Session Audit Log." "Agents propose plans, ask questions, and route work to relevant reviewers within your existing processes." Ramp's controller: it "posted depreciation directly to NetSuite without issue."
- Where: https://ramp.com/blog/how-finance-teams-use-ramp-stack (31 August 2026)
- Speaker and interest: Ramp product marketing
- Read: part
- Bears on: parts 11, 12; Q7
- Against Ben's starting positions: supports Chroma's objection: the close with audit log, skills and review routing is a product "more than 1,000 businesses" are said to rent.

### R-WEB-STACK-29
- Claim: IBM's widely cited HR case (an agent handling 94% of routine HR questions, about 200 roles replaced) was not confirmed against a primary source in this run.
- Kind: company claim (as relayed by the press)
- Quote: "Our total employment has actually gone up" (Arvind Krishna, as quoted in search summaries of a Wall Street Journal interview)
- Where: e.g. https://www.entrepreneur.com/business-news/ibm-ceo-ai-replaced-hundreds-of-human-resources-staff/491341 (May 2025)
- Speaker and interest: IBM's chief executive; IBM sells the HR agent product
- Read: summary only
- Bears on: part 12; Q7
- Against Ben's starting positions: not applicable. Included so the ledger does not treat it as established.

## E. Cost control

### R-WEB-STACK-30
- Claim: Uber spent its 2026 AI budget in the first months of the year and responded with engineering measures.
- Kind: company claim (chief technology officer, via journalist)
- Quote: Uber "blew through its budget for the technology in just the first few months of the year." Naga: "because we've treated efficiency as an engineering problem rather than a budget problem." Uber's president, on the link between AI and product output: "That link is not there yet".
- Where: https://fortune.com/2026/08/07/uber-ai-spending-tokenmaxxing-is-over-cto/ (7 August 2026)
- Speaker and interest: journalist (Sasha Rogelberg) quoting Uber executives. Levers named: prompt caching, a changed default model, and showing engineers their own cost per hour.
- Read: part
- Bears on: parts 9, 11, 14; Q7
- Against Ben's starting positions: not applicable. A firm that encouraged maximum use and ranked staff by it had no outcome link to show.

### R-WEB-STACK-31
- Claim: Most large firms an analyst spoke to cap spend per employee, at very different levels, and change the default model to control cost.
- Kind: analyst interpretation (interviews with over 50 firms; mostly engineering staff)
- Quote: Uber "imposed a $1,500/month/employee limit"; two others "cap employees at $250 and $500 a month, respectively"; "Most employees have a $200/month budget by default"; one firm "switched the default Claude model for all staff from Opus to Sonnet". Ramp card data, as cited: "99th percentile customers spend almost $90,000/yr per employee," and "the median Ramp customer spending just $136."
- Where: https://newsletter.semianalysis.com/p/tokenbudgeting-our-conversations (30 June 2026; paywalled after the opening)
- Speaker and interest: SemiAnalysis, a research firm selling subscriptions
- Read: part (free portion)
- Bears on: parts 9, 14; Q7
- Against Ben's starting positions: not applicable. Gives a planning range for part 14. These are software and industrial firms; no figure for a services practice was found.

### R-WEB-STACK-32
- Claim: Spend on tokens across one card provider's customers rose thirteen-fold in a year and is spiky.
- Kind: observed result (the provider's own transaction data, method not described)
- Quote: businesses' "average monthly token spend 13x'd from January 2025 to January 2026."; "AI costs spike 50% or more about one in every four months for the biggest spenders."; there is "not yet a proven, standardized way for companies to measure AI ROI today."
- Where: https://ramp.com/leading-indicators/the-tokenmaxxing-comedown-companies-grapple-with-the-ai-fomo-premium (3 June 2026)
- Speaker and interest: Ramp, which sells spend controls
- Read: part
- Bears on: part 14; Q7
- Against Ben's starting positions: not applicable. A budget line that can jump 50% in a month needs a cap and an owner before it needs optimising.

## What this adds up to

Inference, not source statement.

1. The layers Ben lists are real and separately visible in operator accounts, but the fullest accounts come from technology companies with hundreds of engineers. No services roll-up has published its architecture. Long Lake, Thrive, Shield and Lawhive name a platform and give results; none gives head count, cost per firm, or what sits on top of the acquired firm's existing systems.
2. Permissions and audit converge on one pattern in three unrelated firms (Uber, Cloudflare, Pinterest): a registry, a gateway, tools off by default, an owner per tool. This layer can now be bought. It should be shared across a group.
3. The improvement loop that exists in public (Thrive and OpenAI) is engineers improving software from logged corrections, with a human approving each change. It is not a firm rewriting its own playbooks. Two operators independently say raw corrections are noisy and cannot be taken as truth.
4. The back office is where rented products are strongest (close, expenses, HR questions). That supports Chroma's objection. The firm-specific asset is the playbook content and the evaluation set, and one vendor calls its own playbook format not proprietary.
5. Cost control is a cap, a default model and visibility. Published per-head figures run from $200 to $2,000 a month in engineering-heavy firms; nothing exists for a practice.

## What is missing

- Any architecture account from an AI roll-up, with people and cost. Looked for: Long Lake, Thrive, Crete or Current, Shield, Titan, Ascend, Lawhive, Crosby, Affinia.
- Engineering cost of the latest firm against the first, for any services group. Only a semiconductor example (R-05).
- Systems of record: which practice-management, tax, ticketing or property systems these groups keep, replace or write to. Nothing found.
- Capture of meetings, email and screens by a named services operator. Only vendor pages and a student project.
- The human review queue as a built thing: staffing, sampling rate, override rate. Nothing beyond R-20.
- A named controller's before-and-after close time with agents. Only vendor testimonials.
- HR, IT and compliance back-office cases with a stated method, other than Klarna support.
- UK mid-tier or consolidator stack detail. ICAEW gives attitudes only.
- What is shared across a group, in an operator's own words, beyond "one platform".

## Not retrieved

- Klarna press release, businesswire.com/news/home/20260219313357 (403). The 20-F was read instead.
- Pinterest Engineering, "Building an MCP Ecosystem at Pinterest" (403); secondary summaries only.
- AccountingWeb, "From consolidation to controllability: the operating system problem in PE" (403).
- Lawhive press release of 18 March 2026 on its US acquisition team (403).
- Accounting Today podcast transcript with Ascend's chief executive (page loaded without the transcript).
- Ascend engineering job advertisement on Greenhouse (redirected to a jobs index).
- Newcomer, "Inside the VC roll-up craze" (paywalled after the opening).
- SemiAnalysis "TokenBudgeting" company-by-company summary (paywalled).
- MIT Sloan capstone poster on Level Agency (PDF returned as unreadable binary).
- Choi and Xie's paper itself (only the MIT Sloan write-up was read).
- The interview behind Long Lake's "80% of the infrastructure is shared" (search summary only; source not identified).
- IBM primary material on AskHR; Moderna 2026 update; Crosby's own engineering material; Affinia or RedBird material on "RedBird X"; ICAEW's underlying mid-tier research report; Digits and Pilot primary pages (seen in search summaries only, not used as rows).
- Long Lake job advertisements (search found none).
