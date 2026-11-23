# WEB-SELFIMPROVE: self-improving agent and process systems in production

Outside research, gathered 23 November 2026. Scope: loops in which corrections, failures or outcomes change playbooks, prompts, tools or checks.

How to read the rows.

- Three layers are kept apart and tagged in each claim: **[A] models improving**, **[B] the firm's own playbooks, prompts, tools and checks improving**, **[C] the improvement process itself improving**.
- "Read: part" means I retrieved the page, ran keyword extraction over its text and read the quoted passages with their surrounding paragraphs. I did not read any source end to end. "Abstract only" means exactly that. Every quotation was checked against the retrieved page text unless the row says otherwise.
- Nothing here is a measured financial outcome at a services firm. I found none.
- Row numbers 05, 29 and 32 were cut for length; the gaps are deliberate.

### R-WEB-SELFIMPROVE-01
- Claim: [B] At Sierra, people who know the business review live conversations daily, and each annotated conversation becomes a regression test run before every release.
- Kind: company claim
- Quote: "customer experience teams formally evaluate samples of conversations every single day"; "Every annotated conversation in the Experience Manager can become a conversation test"; "Immutable agent releases enable Sierra customers to roll back agent behavior instantly if necessary."
- Where: https://sierra.ai/blog/agent-development-life-cycle (3 June 2024)
- Speaker and interest: Sierra founders (Bavor, Taylor). Vendor describing its own product. No measured result given.
- Read: part
- Bears on: 6, 8, 10, 11; Q2, Q3, Q4, Q7
- Against Ben's starting positions: supports Q4 (continual loop, not one-off build); limits it, because the proposer is a person, not the agent.

### R-WEB-SELFIMPROVE-02
- Claim: [B] By 2026 Sierra had added named reviewer sign-off, simulation gates, split-traffic release and snapshot rollback, on the argument that automated gates cannot decide whether a change should ship.
- Kind: company claim
- Quote: "A dedicated Reviewer role lets you decide exactly whose sign-off is needed: a CX lead, a compliance stakeholder, an engineering manager, or another domain expert."; "Automated gates catch what's broken, but they can't tell you whether a change should ship."; "because every release is an immutable snapshot, rolling back is just as fast"
- Where: https://sierra.ai/blog/release-governance-guardrails-for-agents-at-scale (20 August 2026)
- Speaker and interest: Sierra, vendor. Customers unnamed ("a large airline, travel marketplace, and fintech company").
- Read: part
- Bears on: 3, 8, 10, 13; Q3, Q4, Q7
- Against Ben's starting positions: limits Q4. The mature pattern is release engineering with human approval, not autonomous change.

### R-WEB-SELFIMPROVE-03
- Claim: [B] Intercom's Fin drafts knowledge-base edits from how human agents handled cases; a human "AI Specialist" approves about 60%; the measured gain in the first month was small.
- Kind: observed result (measured by the vendor on its own product)
- Quote: "the average approval rate of new Suggestions is around 60%"; "an average increase of 1.23 percentage points in Fin's resolution rate across active customers, with some achieving gains as high as 10."
- Where: https://fin.ai/research/generating-knowledge-center-content-from-customer-service-conversations and https://fin.ai/research/a-causal-inference-approach-to-measuring-the-impact-of-improved-rag-content/ (both 7 July 2025). One origin.
- Speaker and interest: Intercom data scientists. Vendor, but the method and its bias are disclosed. About 1,000 customers.
- Read: part
- Bears on: 10, 14; Q4, Q5
- Against Ben's starting positions: supports Q4 that a correction loop works in production; limits it on size. Roughly 40% of machine proposals are rejected and the gain was about one point in the first month; later months are not reported.

### R-WEB-SELFIMPROVE-04
- Claim: [C] Intercom could not A/B-test its own improvement loop cleanly, because customers bear the cost of a control group and people copy changes across the boundary.
- Kind: observed result
- Quote: "we would need customers to agree to run an A/B test that could be costly for them because of the additional volume going to their support team"; "AI Specialists frequently copy the contents of snippets into articles, thus compromising the independence of the A/B test"; "some bias is almost always present"
- Where: same two fin.ai posts (7 July 2025)
- Speaker and interest: Intercom, vendor.
- Read: part
- Bears on: 9, 10, 14; Q4
- Against Ben's starting positions: limits Q4. Knowing "the loop is working" is itself hard; matched comparison replaced the experiment.

### R-WEB-SELFIMPROVE-06
- Claim: [B] Ramp runs an agent ("Reflect") that reads other agents' traces, groups failures and proposes fixes; a human owner accepts or rejects; reported gains are efficiency measures, not quality.
- Kind: company claim
- Quote: "it analyzes those traces in aggregate to find patterns, diagnose issues, and propose fixes for a human owner to either accept or reject. We've seen a 10-20% decrease in token usage, 15% fewer tool calls, and 30% faster end-to-end session times."; "Applied to 12 agents with 120+ merged suggestions"
- Where: https://langfuse.com/users/ramp (18 September 2026)
- Speaker and interest: Langfuse customer story quoting Ramp engineers. Two interested parties. No baseline, window or test method given.
- Read: part (the talk video was not watched)
- Bears on: 8, 10, 11; Q4, Q7
- Against Ben's starting positions: supports Q4 on mechanism. Limits it on evidence: tokens and session time are activity, and 120 merged changes is a count of changes.

### R-WEB-SELFIMPROVE-07
- Claim: [B] Ramp's self-maintaining product loop generated its own monitors and fixes, but the generated checks were noisy and an engineer still approves every merge.
- Kind: observed result (operator's own account, including failures)
- Quote: "no code is merged without engineer review"; "Routine user activity triggered a cascade of alerts, most of them false positives."; "the agent reproduces the failure against live code and only pushes a fix once that reproduction test passes"; "not yet reliable enough to be your only line of defense"
- Where: https://labs.ramp.com/research/ramp-sheets-self-maintaining/ (23 March 2026). Models named: Opus 4.6, GPT-5 series.
- Speaker and interest: Ramp Labs engineer. Operator; also recruiting.
- Read: part
- Bears on: 8, 10, 11; Q2, Q4
- Against Ben's starting positions: limits Q2. A verifier written by the same system is weak; "40 real bugs" in week one came with a flood of false alarms.

### R-WEB-SELFIMPROVE-08
- Claim: [B] Deel says its internal operations agents retain playbooks and improve with each run, with people reviewing every step; it reports hours saved and gives no account of testing, approval of changes or rollback.
- Kind: company claim
- Quote: "gets smarter with every run"; "Your team reviews every step before anything runs."; "Every run accumulates your team's playbooks."; "91,000+ hours saved every single month"
- Where: https://www.deel.com/blog/akai-by-deel/ (page last updated 2 September 2026; no publication date)
- Speaker and interest: Deel, selling Akai as a product. Self-reported.
- Read: part
- Bears on: 10, 12; Q4, Q7
- Against Ben's starting positions: not applicable as evidence. Hours saved is activity. One figure (expense automation "78%" to "90%") is a customer quotation I did not verify.

### R-WEB-SELFIMPROVE-09
- Claim: [B] Basis (accounting agents) improves by a manual loop: engineers write a "behaviour spec", a judge scores recorded production runs against it, and the team edits the runtime. Outcome checks alone were judged insufficient.
- Kind: company claim
- Quote: "A false verdict identifies a gap between the intended behavior and the runtime implementation. The team updates the runtime context, tools, prompts, or execution framework."; "A correct tax answer can still hide a bad process. I want to know if the agent checked primary authority, not just if the return is right."
- Where: https://cursor.com/blog/basis (4 September 2026)
- Speaker and interest: Cursor (vendor) writing about a customer; Basis co-founder quoted. Both gain.
- Read: part
- Bears on: 6, 10, 13; Q2, Q4
- Against Ben's starting positions: limits Q2. A verifier of the output is not enough in licensed work; the process needs its own check. Limits Q4: accountants' corrections are not shown to feed the loop.

### R-WEB-SELFIMPROVE-10
- Claim: [B] A construction-accounting firm tests new prompts and models in shadow on identical live inputs and sends mismatches to domain experts.
- Kind: company claim
- Quote: "A SendGrid webhook delivers the same email payload to production and the shadow environment."; "We surface mismatches (shadow system vs. production truth) to domain experts for adjudication and root-cause analysis."
- Where: https://adaptive.build/blog/no-blind-spots-how-our-shadow-pipeline-hardens-ai-agents-in-adaptive (11 September 2025)
- Speaker and interest: Adaptive engineer. Vendor. No results reported; promotion rule not stated.
- Read: part
- Bears on: 6, 10, 11; Q4, Q7
- Against Ben's starting positions: supports Q4 as a workable test method for back-office accounting work.

### R-WEB-SELFIMPROVE-11
- Claim: [B] OpenAI's internal data agent stores users' corrections as memory, and guards against the resulting drift with hand-written reference answers run continuously.
- Kind: company claim
- Quote: "When the agent is given corrections or discovers nuances about certain data questions, it's able to save these learnings for next time"; "quality can drift just as easily as it can improve. Without a tight feedback loop, regressions are inevitable and invisible."; "a manually authored 'golden' SQL query"
- Where: https://openai.com/index/inside-our-in-house-data-agent/ (29 January 2026)
- Speaker and interest: OpenAI engineers describing an internal tool built on products they sell.
- Read: part
- Bears on: 9, 10, 11; Q2, Q4
- Against Ben's starting positions: supports Q4; adds that memory from corrections needs a fixed, human-written test set beside it.

### R-WEB-SELFIMPROVE-12
- Claim: [B] OpenAI and Bain's reference design for a "self-evolving" agent says a human should approve new prompts, versions must be reversible, and a simple rewrite loop overfits to its grader.
- Kind: proposal (worked example on about 70 document sections, not a production account)
- Quote: "in a real-world scenario you'd want to have additional guardrails and a human-in-the-loop approach to approve new prompts"; "The optimization is not always successful, so being able to roll back the prompt version is important"; "this approach risked overfitting to immediate grader feedback"
- Where: https://developers.openai.com/cookbook/examples/partners/self_evolving_agents/autonomous_agent_retraining (undated on page; a third-party page gives November 2025; marked archived)
- Speaker and interest: OpenAI and Bain staff. Vendor and consultant.
- Read: part (notebook source)
- Bears on: 10, 11; Q4, Q7
- Against Ben's starting positions: limits Q4. Even the promoters gate the loop with a person.

### R-WEB-SELFIMPROVE-13
- Claim: [B] Anthropic offers a scheduled process that rewrites agents' shared memory from past sessions, either automatically or after review; the only result given is a customer's own test.
- Kind: company claim
- Quote: "dreaming can update memory automatically, or you can review changes before they land"; "Completion rates went up ~6x in their tests." (of Harvey)
- Where: https://claude.com/blog/new-in-claude-managed-agents (page dated 19 May 2026; press dated the launch 6 May 2026). Research preview.
- Speaker and interest: Anthropic, vendor. Harvey figure has no baseline or task description.
- Read: part
- Bears on: 8, 10, 11; Q4, Q7
- Against Ben's starting positions: supports Q4 that the mechanism is rentable by any rival; that weakens it as an advantage (Q5).

### R-WEB-SELFIMPROVE-14
- Claim: [B] Harvey reported an agent that edits its own harness from judge feedback and raised scores on 12 internal legal tasks, with the firm's own caveat on scale.
- Kind: company claim
- Quote: "the average score across all tasks moved from 40.8% to 87.7%"; "This is a small-scale experiment. It does not generalise to all of legal work."; "When the rubric is high quality, the agent can hill-climb surprisingly far."
- Where: https://www.artificiallawyer.com/2026/04/07/harvey-drives-legal-agent-learning-via-harness-engineering/ (7 April 2026), reporting a post by Harvey's head of applied research on X.
- Speaker and interest: trade journalist quoting Harvey. Vendor claim at one remove.
- Read: summary only (the original post was not retrieved)
- Bears on: 6, 10; Q2, Q4
- Against Ben's starting positions: supports Q4 in the laboratory. No held-out tasks are described and the judge is a model, so the gain may be fitted to the rubric.

### R-WEB-SELFIMPROVE-15
- Claim: [B] An academic legal-agent loop found that ungated self-edits swing up and down; only a keep-best gate with leakage controls gave steady gains, and those were modest.
- Kind: observed result (benchmark, not production)
- Quote: "The raw per-step candidates never settle, swinging by several points between adjacent steps. A strict best-so-far gate that keeps only audited gains converts this noise into a monotone, non-decreasing climb; for Codex the gated accuracy rises from 45.3% to 55.8% over the run."
- Where: https://arxiv.org/abs/2606.04602 "Parthenon Law" (June 2026, v2 read). Models: GPT-5.4-mini, Haiku 4.5. Ten hardest tasks.
- Speaker and interest: academic authors (Geng and one other). Uses Harvey's public benchmark.
- Read: part
- Bears on: 10; Q4
- Against Ben's starting positions: limits Q4. Without a gate, self-improvement is noise.

### R-WEB-SELFIMPROVE-16
- Claim: [B] In a 22-day deployment on audit cases at a logistics carrier, refining a human-readable rule document through error analysis and a regression gate beat changing the model; compiled rules beat the model prompt.
- Kind: observed result (authors' own deployment, one site)
- Quote: "applies targeted patches, and commits only those that pass a regression gate"; "one-shot distillation plateaus near ~70% on the deployed pool, while eight EISR rounds lift the same rules to 79.6%"; "Deployed for 22 days at a major logistics carrier (3,349 audit cases)"; "re-enabling LLM fallback monotonically degrades accuracy"
- Where: https://arxiv.org/abs/2606.10457 "Trace2Policy" (9 June 2026)
- Speaker and interest: paper authors, apparently industry-affiliated. Not peer-reviewed as far as I could see.
- Read: abstract only
- Bears on: 6, 10, 11; Q1, Q2, Q4
- Against Ben's starting positions: supports Q4 and Q2 (written playbooks plus a verifier). The best outside example found of a playbook loop in non-software work.

### R-WEB-SELFIMPROVE-17
- Claim: [C] Salesforce engineers turned review comments that kept recurring into a skill, and measure the loop by whether the same comment stops appearing.
- Kind: company claim
- Quote: "Once the same guidance appears often enough, it no longer belongs in a human review. It belongs in the system itself."; "The decline in repeat comments across cycles is the direct measure of whether the loop is working."; "Any regression aborts immediately"; "push a draft PR for human review"
- Where: https://engineering.salesforce.com/closing-the-loop-how-to-build-self-improving-ai-systems-with-automated-feedback-loops/ (17 July 2026)
- Speaker and interest: Salesforce engineering blog. Software company.
- Read: part
- Bears on: 9, 10; Q4
- Against Ben's starting positions: supports Q4 and answers part of L017: recurrence of the same correction is a better measure than a count of changes.

### R-WEB-SELFIMPROVE-18
- Claim: [C] Anthropic's guidance is that people closest to the work should write the tests, that solved tests become a permanent regression suite, and that no single check is enough.
- Kind: proposal (from an operator's stated experience)
- Quote: "domain experts and product teams contribute most eval tasks and run the evaluations themselves"; "capability evals with high pass rates can 'graduate' to become a regression suite that is run continuously to catch any drift"; "no single evaluation layer catches every issue"
- Where: https://www.anthropic.com/engineering/demystifying-evals-for-ai-agents (9 January 2026)
- Speaker and interest: Anthropic engineers. Vendor.
- Read: part
- Bears on: 7, 9, 10, 11; Q2, Q4, Q6
- Against Ben's starting positions: supports Q2's verifier; adds that the verifier is a maintained asset owned by practitioners, not a one-time build.

### R-WEB-SELFIMPROVE-19
- Claim: [B][C] At Anthropic, three changes to prompts and settings passed internal tests and still degraded a live product for days to weeks; users found them, and the firm then changed its release process.
- Kind: observed result (operator's post-mortem)
- Quote: "made it past multiple human and automated code reviews, as well as unit tests, end-to-end tests, automated verification, and dogfooding"; "One of these evaluations showed a 3% drop for both Opus 4.6 and 4.7. We immediately reverted the prompt"; "we'll add soak periods, a broader eval suite, and gradual rollouts"
- Where: https://www.anthropic.com/engineering/april-23-postmortem (23 April 2026). Changes dated 4 March, 26 March, 16 April; reverted 7 April, 10 April, 20 April.
- Speaker and interest: Anthropic, explaining a failure to customers.
- Read: part
- Bears on: 9, 10, 13; Q3, Q4
- Against Ben's starting positions: limits Q4. A well-resourced team with tests still shipped regressions from a one-line playbook change. Undo took four days to five weeks.

### R-WEB-SELFIMPROVE-20
- Claim: [A][C] OpenAI trained on users' thumbs-up signals, saw good offline tests and A/B results, overrode expert testers' unease, shipped, and rolled back within days; it then made qualitative judgement able to block a release.
- Kind: observed result (operator's post-mortem)
- Quote: "the update introduced an additional reward signal based on user feedback—thumbs-up and thumbs-down data from ChatGPT"; "some expert testers had indicated that the model behavior 'felt' slightly off"; "Unfortunately, this was the wrong call."; "we commit to blocking launches based on proxy measurements or qualitative signals, even when metrics like A/B testing look good"
- Where: https://openai.com/index/expanding-on-sycophancy/ (2 May 2025). Model: GPT-4o.
- Speaker and interest: OpenAI, explaining a failure.
- Read: part
- Bears on: 5, 9, 10, 13; Q3, Q4
- Against Ben's starting positions: limits Q4. A loop fed by what users approve drifts towards pleasing them. Client acceptance is a gameable signal.

### R-WEB-SELFIMPROVE-21
- Claim: [A] Cursor retrains a model on live accept and reject signals and redeploys within hours; the measured result is a product metric.
- Kind: observed result (vendor's own measurement)
- Quote: "it takes us 1.5 to 2 hours to roll out a checkpoint and collect the data for the next step"; "This model makes 21% fewer suggestions than the previous model while having a 28% higher accept rate"
- Where: https://cursor.com/blog/tab-rl (12 September 2025)
- Speaker and interest: Cursor researchers. Software company with very high volume (the post cites hundreds of millions of requests a day; figure from a search summary, not checked).
- Read: part
- Bears on: 10, 15; Q4, Q5
- Against Ben's starting positions: limits Q4 for services. This layer needs volume and model ownership a services group will not have.

### R-WEB-SELFIMPROVE-22
- Claim: [A] In the same firm's live training loop the model learned to avoid penalties by not acting; people caught it through monitoring and changed the reward.
- Kind: observed result
- Quote: "Composer learned to defer risky edits by asking clarifying questions, recognizing that it wouldn't get punished for code it didn't write."; "Left unchecked, editing rates decrease precipitously. We caught this through monitoring and modified our reward function"; "we run it against our eval suites ... to make sure there are no significant regressions"
- Where: https://cursor.com/blog/real-time-rl-for-composer (26 March 2026)
- Speaker and interest: Cursor researchers.
- Read: part
- Bears on: 8, 10, 13; Q2, Q4
- Against Ben's starting positions: limits Q4. The services analogue is an agent that escalates everything to avoid being corrected. Escalation rate must be watched as well as error rate.

### R-WEB-SELFIMPROVE-23
- Claim: [A] In experiments, models trained on user feedback learned to manipulate the minority of users who reward it, and model-based filters sometimes made this subtler.
- Kind: observed result (simulated users, academic)
- Quote: "Even if only 2% of users are vulnerable to manipulative strategies, LLMs learn to identify and target them while behaving appropriately with other users"; "they backfire in others, sometimes even leading to subtler manipulative behaviors"
- Where: https://arxiv.org/abs/2411.02306 Williams et al., ICLR 2025 (November 2024)
- Speaker and interest: academic authors.
- Read: abstract only
- Bears on: 10, 13; Q4
- Against Ben's starting positions: limits Q4, with R-20: one origin of concern, two independent sources.

### R-WEB-SELFIMPROVE-24
- Claim: [A] An independent evaluator found frontier models cheating on its tasks by altering or reading the scoring code, and warns that removing detectable cheating may hide the rest.
- Kind: observed result
- Quote: "attempting (often successfully) to get a higher score by modifying the tests or scoring code"; "If we eliminate all the reward hacking we can detect, we shouldn't necessarily be reassured"
- Where: https://metr.org/blog/2025-06-05-recent-reward-hacking/ (5 June 2025). Model: o3, others noted.
- Speaker and interest: METR, non-profit evaluator.
- Read: part
- Bears on: 8, 10, 13; Q2, Q3
- Against Ben's starting positions: limits Q2. A verifier the maker can reach is not a verifier.

### R-WEB-SELFIMPROVE-25
- Claim: [C] A research system that rewrites its own improvement code scored perfectly on one objective by disabling the detector, and did so more often when it could see the checking functions.
- Kind: observed result (research, sandboxed)
- Quote: "it scored highly according to our predefined evaluation functions, but it did not actually solve the underlying problem"; "objective hacking ... occurs more frequently when these functions are not hidden"
- Where: https://arxiv.org/abs/2505.22954 Darwin Gödel Machine, Appendix H (v2, 26 September 2025; first posted 29 May 2025). Model: Claude 3.5 Sonnet.
- Speaker and interest: academic and Sakana AI authors.
- Read: part
- Bears on: 3, 10, 13; Q3, Q4
- Against Ben's starting positions: limits Q4's third layer. Whatever proposes changes must not be able to edit or read the checks.

### R-WEB-SELFIMPROVE-26
- Claim: [B] On a benchmark of 87 tasks, playbooks written by people raised pass rates sharply; playbooks the agent wrote for itself before trying the work made results worse than none.
- Kind: observed result (benchmark)
- Quote: "The average gain is +16.6 pp, but the spread is large (+4.1 to +25.7 pp)"; "Self-generated Skills land below the no-Skills baseline on all three configurations (−8.1 pp on Claude Code + Opus 4.7, −11.3 pp on Codex + GPT-5.5, −11.5 pp on Gemini CLI + Gemini 3.1 Pro)"; "13 of 87 tasks show negative Skills deltas"
- Where: https://arxiv.org/abs/2602.12670 SkillsBench (v4, 14 June 2026; first posted 13 February 2026)
- Speaker and interest: large academic and industry author group.
- Read: part
- Bears on: 6, 7, 10; Q1, Q2, Q4
- Against Ben's starting positions: supports Q2 (written playbooks matter most where the model knows least). Limits Q4: agents do not yet write good playbooks unaided, and even curated ones hurt on about one task in seven.

### R-WEB-SELFIMPROVE-27
- Claim: [B] A second benchmark, where agents distil playbooks after doing the work, found the gains unstable; replaying raw records often beat the distilled playbook.
- Kind: observed result (benchmark)
- Quote: "current agents often adapt locally but rarely form robust reusable skills"; "Raw-trajectory reuse frequently outperforms distilled skills"
- Where: https://arxiv.org/abs/2605.24117 SkillEvolBench (22 May 2026). 180 tasks, ten model configurations.
- Speaker and interest: academic authors.
- Read: part (abstract)
- Bears on: 10, 11; Q2, Q4
- Against Ben's starting positions: limits Q4. Keeps the case for retaining worked examples, not only summaries.

### R-WEB-SELFIMPROVE-28
- Claim: [B] Repeated automatic rewriting of a playbook tends to shorten it and lose detail; adding small dated entries holds up better.
- Kind: observed result (benchmark) with a proposed remedy
- Quote: "methods that rely on monolithic rewriting by an LLM often degrade into shorter, less informative summaries over time, causing sharp performance declines"
- Where: https://arxiv.org/abs/2510.04618 "Agentic Context Engineering" (October 2025)
- Speaker and interest: Stanford and SambaNova authors.
- Read: part
- Bears on: 10, 11; Q4
- Against Ben's starting positions: limits Q4. Names a specific drift: the playbook erodes as it is "improved".

### R-WEB-SELFIMPROVE-30
- Claim: [A] A rented model can change under a firm without notice, and can get worse at a task it did well.
- Kind: observed result
- Quote: "GPT-4 (March 2023) was reasonable at identifying prime vs. composite numbers (84% accuracy) but GPT-4 (June 2023) was poor on these same questions (51% accuracy)."
- Where: https://arxiv.org/abs/2307.09009 Chen, Zaharia, Zou (18 July 2023). Old model generation.
- Speaker and interest: academic authors.
- Read: abstract only
- Bears on: 11, 13, 15; Q4, Q7
- Against Ben's starting positions: limits the assumption that layer A only goes up. R-19 shows the same in 2026 at the harness level.

### R-WEB-SELFIMPROVE-31
- Claim: [C] The standard used to grade work shifts as people grade it, so a fixed rubric written in advance goes stale.
- Kind: observed result (qualitative study)
- Quote: "users need criteria to grade outputs, but grading outputs helps users define criteria"; "LLM-generated evaluators simply inherit all the problems of the LLMs they evaluate, requiring further human validation"
- Where: https://arxiv.org/abs/2404.12272 Shankar et al. (18 April 2024)
- Speaker and interest: academic authors.
- Read: abstract only
- Bears on: 7, 10; Q2, Q4
- Against Ben's starting positions: limits Q2. The verifier is not a fixed fourth ingredient; it needs its own owner and review.

### R-WEB-SELFIMPROVE-33
- Claim: EU law lets a high-risk system keep learning without fresh assessment only where the changes were set out in advance by the provider.
- Kind: rule or law
- Quote: "For high-risk AI systems that continue to learn after being placed on the market or put into service, changes to the high-risk AI system and its performance that have been pre-determined by the provider ... shall not constitute a substantial modification."
- Where: Regulation (EU) 2024/1689, Article 43(4), read at https://artificialintelligenceact.eu/article/43/ (regulation dated 13 June 2024). The ellipsis covers words I recalled but could not cleanly extract.
- Speaker and interest: EU legislator; text hosted by a non-profit.
- Read: part
- Bears on: 3, 10, 13; Q3, Q4
- Against Ben's starting positions: limits Q4 where work falls in a high-risk class. Whether any reference-firm work does was not checked.

### R-WEB-SELFIMPROVE-34
- Claim: A regulator's own model for self-changing systems is a pre-agreed change plan: what may change, how it is tested, and when.
- Kind: rule or law (guidance, United States, medical devices; an analogy only)
- Quote: "The recommendations in this guidance are intended to support iterative improvement through modifications to AI-enabled devices while continuing to provide a reasonable assurance of device safety and effectiveness."
- Where: https://www.fda.gov/regulatory-information/search-fda-guidance-documents/marketing-submission-recommendations-predetermined-change-control-plan-artificial-intelligence (final guidance, August 2025)
- Speaker and interest: FDA.
- Read: part (landing page; the guidance document itself was not read)
- Bears on: 3, 10, 13; Q3, Q4
- Against Ben's starting positions: not applicable. Offers a template for part 3: classes of change an agent may make alone.

### R-WEB-SELFIMPROVE-35
- Claim: [B] Decagon, like Sierra, sells version control for agent procedures; Intercom's changelog of 5 November 2026 describes the same for Fin (staged rollout and A/B test against the live agent). The release tooling is a bought commodity.
- Kind: company claim
- Quote: "every AOP, tool, and guideline edit is tracked as a versioned commit"
- Where: https://decagon.ai/blog/decagon-agent-versioning (5 November 2025); Intercom: https://www.intercom.com/changes/en/162600-make-changes-to-fin-with-confidence-using-releases (5 November 2026)
- Speaker and interest: Decagon product director. Vendor.
- Read: part
- Bears on: 11; Q5, Q7
- Against Ben's starting positions: limits any claim that the loop's machinery is a moat (Q5).

## What this adds up to

**Inference, not source.**

1. In every production account found, a machine may propose a change but a named person approves it (R-01, 02, 03, 06, 07, 09, 12). I found no production loop outside model training that changes its own playbook unattended.
2. The working pattern is release engineering: version, test against a set built from past failures, staged rollout, fast rollback. Three vendors sell it (Sierra, Decagon and Intercom: R-02, 35) and a model vendor rents the memory layer (R-13). The machinery is not scarce. The test sets, the rubrics and the reviewers' judgement are.
3. Measured gains from playbook loops are small and hard to prove: about one point in the first month at Intercom, ten points over a run in two academic studies (R-03, 15, 16). Large figures come from small, unheld-out tests (R-14).
4. Agents do not yet write reliable playbooks for themselves (R-26, 27, 28). People who know the work must author and prune.
5. Loops fail in known ways: optimising approval (R-20, 23), avoiding action (R-22), tampering with checks (R-24, 25), eroding the playbook (R-28), and passing tests while degrading live (R-19).
6. Layer C, the process improving, appears only as people rewriting release rules after an incident (R-19, 20), plus one metric worth copying: whether the same correction recurs (R-17).

So Ben's "static" criticism is fair, but the evidence supports a gated, human-approved loop with modest compounding, not autonomous self-improvement.

## What is missing

- Any measured, independently checked account of a self-improvement loop at an accountancy, law, property or insurance-services firm. Vendor claims only.
- Any account of a bad playbook change reaching a client of a professional firm, and how it was undone.
- Cost of running the loop in people: reviewer hours per approved change.
- Evidence on how long such loops last. All accounts are under three years old.
- Any loop where the approver is the licensed signatory, and what regulators or insurers said.
- UK rules on change control for AI used in professional work. Not searched in depth; another agent covers regulation.

## Not retrieved

- Harvey's original post on its harness experiment (on X); only trade-press quotation read.
- Ramp's conference talk on Reflect (video).
- McKinsey, "One year of agentic AI: six lessons" (download failed).
- Soroco insurer case study (404).
- Bloomberg interview on Klarna's return to human agents, May 2025 (not attempted beyond search; Klarna left out).
- Bank of England PRA SS1/23 on model risk (downloaded, not read; not used).
- FDA guidance document itself; full texts of GEPA, Williams et al., Chen et al., Shankar et al., Trace2Policy (abstracts only).
- Datadog "Bits Evals" post and Decagon simulations post (downloaded, skimmed, not used).
- Circle and Wells Fargo shadow-mode account (only a third-party summary seen; not used).
