# Handover: designing the AI-native services firm

Written 26 November 2026, for whoever picks this work up next, human or agent. Read this file first, then the files it points to.

## 1. What Ben is trying to do

Ben invests in and helps run services businesses. The aim is to work out how to build a **market-leading AI-native services business**, starting in **2027** and looking ahead to **2035 and beyond**, working "in the real world we actually exist in today".

The questions behind it, from Ben's first prompt:
- **The firm itself:** what the ideal operating model is, and how it would or could be built.
- **Inside the firm:**
  - processes, infrastructure, team, back office and tech stack;
  - the organising principles for people and AI;
  - who needs to be "AI-pilled".
- **Continual self-improvement, or RSI, for a services firm:** what it looks like, what it needs, what would happen. Ben's starting point is that static approaches fail: process mapping such as Marble Cognition, and one-off projects like "let's automate billing".
- **What automating a task needs.** Ben's hypothesis is four things: readable state, a written playbook, a way to write, and a verifier. "Or does it?"
- **Whether to list the 200 things a firm does,** productise them and automate.
- **Commoditisation:** does recursive self-improvement make commodity services work a commodity, and what is left?
- **Variation:** how the design changes by business type (global or local, regulated or not, commodity or high-touch, advice or coordination, small business or enterprise).
- **Investment:** what all this teaches about where to build or invest.

## 2. How Ben wants to work (the most important section)

These steers came after two failed attempts. Hold to them.

1. **Explore and reason forward; don't hide behind evidence.** The field moves fast and evidence is thin, so use inference and conjecture grounded in sound logic. The first run, on 23 November, was rejected because it made everything evidence-bound and committee-ready.
2. **But don't assert without reasoning either.** The second attempt (unit 2, "the world in 2035") was rejected as over-inferred: calls made in one pass with no checking. The standard Ben agreed for any claim the design depends on:
   - the claim;
   - the mechanism, and who gains;
   - what is visible today, and how fast comparable shifts went;
   - the strongest counter-argument;
   - what follows for the design.

   Label claims **[seen]**, **[reasoned]** or **[conjecture]**.
3. **Don't narrow too quickly.** Ben pushed back when the work drilled into warranties, when it treated regulators and courts as starting constraints, and when it started from incumbents. Treat rules, regulators and insurers as facts to design around and as a stress test at the end, not as the starting point.
4. **Redesign, don't automate.** Ben's electricity and Ford point: you rebuild the process around the new power source. Automating today's task list is "level 1" and is already being done, for example by Dwelly. The target is **level 3**: redesign the service and the firm's boundary from the client's outcome. Ben pointed to Pennylane, where client and accountant work in one system, and asked about staff and processes embedded in the client's own systems.
5. **Work in small units, supervised.** Ben asked to do it piecemeal rather than in large unsupervised runs. Show each unit, take the steer, then proceed. Don't swing with the latest comment and lose the original aim. When in doubt, re-read Ben's first prompt (section 1).
6. **Balanced review panels.** An all-practitioner panel pulled towards "sell to incumbents". Mix builders (in the spirit of Linear, Crosby, Pennylane or Dwelly), investors (Conviction-style, roll-up investors in the Elad Gil and General Catalyst style), practitioners and an organisational designer. Reviewers are agents writing in character; never present them as real people. Watch for priming: reviewers given earlier drafts tend to echo them.
7. **Ben likes sharp, decision-changing observations.** For example: "buy books of clients, not companies". Lead with what is non-obvious and name hygiene as hygiene.
8. **Plain English, British spelling, short sentences.**
9. **Ben asked to be told, not to have things incorporated,** when reviewing the library. Don't fold library counter-opinions into the design until asked.

## 3. Where everything is

### Repository
`benjaminthomasphillips-byte/Services-work`, branch `claude/lucid-ramanujan-qaux83`. Commit and push work there. A stop hook asks for untracked files to be committed.

- `prompts/ai-rollup-operating-model.md`: the original orchestration prompt, now superseded. It is kept as a record of what went wrong.
- `runs/2026-11-23-rollup-org/`: the first, evidence-bound run. It is rejected as a direction but useful as raw material:
  - `ledger.md`, an evidence ledger of about 546 rows;
  - `evidence/`, 17 files with row IDs `R-LIB-*` and `R-WEB-*`;
  - `design/inventory-A.md` and `design/inventory-B.md`, work inventories of a 30-person accountancy practice and a 50-person block-management firm.
- `runs/2026-11-24-ideal-model/`: the current work. Key files, in reading order:
  1. `architecture-v1.md`: **the consolidated architecture.** Start here.
  2. `step-4-building-the-firm.md`: **the base design** built on it. Covers the organisation, principles, who needs to be AI-pilled, the engine, back office and infrastructure, the boundary, the build path from 2027 to 2035, and where a first firm looks most promising.
  3. `step-1-the-engine.md`: the self-improving engine.
  4. `step-2-what-is-left.md`: commoditisation, and what stays scarce.
  5. `step-3c-the-electricity-test.md`: levels 1 to 3, the method for designing from scratch, Pennylane, and Dwelly.
  6. `step-3b-the-agent-enterprise.md`: design the firm as pure software, then add people back.
  7. `level3-{accountancy,lettings,legal,claims,probate,homecare,payroll}.md`: seven worked redesigns, each with builder and practitioner reviews (`*-review-*.md`).
  8. `architecture-scorecard.md`: element verdicts across services. Sections 7 and 8 cover home care and payroll.
  9. `blind-score-a.md`, `blind-score-b.md`, `blind-reconciliation.md`: an independent re-score with verdicts stripped out. The blinded inputs are in `blind/`.
  10. `library-review/`: a read-only review of the AI Implementation Library against the design. The `synthesis.md` there was written without the findings slice; read `findings-analyses.md` alongside it.
  11. Superseded but kept: `unit-1-foundations.md`, `unit-2-the-world-in-2035.md` (marked superseded), `step-3-building-the-firm.md`, the `example-*.md` level-1 worked examples, and the panel and counter-review files.

### Notion (Ben's Thoughts Library)
- **Library root:** https://app.notion.com/p/4215f5db20d78154a42dfab8b438005c
- **Rules:** read **"Instructions for the agent"** before acting in the library, and say in the first Log entry that you did: https://app.notion.com/p/4215f5db20d781be8fc2ee0867a155ad. Key rules:
  - keep three voices apart: what the source says, the agent's inference, and Ben's view;
  - never edit a Note;
  - never change a synthesis's Thesis without Ben;
  - log everything, naming failures;
  - ingest outside sources as Source rows.
- **The current work, filed as a Draft synthesis with 16 sub-pages:** https://app.notion.com/p/4225f5db20d781f382dced262125f62a (page id `4225f5db-20d7-81f3-82dc-ed262125f62a`).
- **Log entry for that filing:** https://app.notion.com/p/4235f5db20d7818b86eed9f3f9da5b7b
- **The 23 November evidence-bound draft,** left unchanged, framing superseded: https://app.notion.com/p/4215f5db20d78118b80fc36a3a1e1e06
- **Discovery sweep** (104 outside sources, Ben pointed to it): https://app.notion.com/p/4215f5db20d78195a120f478e5bacda7
- **Data sources:**

  | Name | ID |
  | --- | --- |
  | Sources | `collection://4215f5db-20d7-819e-91af-000b71e89107` |
  | Syntheses | `collection://4215f5db-20d7-81d6-843e-000b9b778527` |
  | Cases | `collection://4215f5db-20d7-818b-9547-000b8b0cbf3f` |
  | Findings | `collection://4215f5db-20d7-8173-8667-000b5a585c02` |
  | Applications | `collection://4215f5db-20d7-8112-b420-000b24df2f68` |
  | Log | `collection://4215f5db-20d7-811c-b866-000b91804f41` |
  | Notes | `collection://4215f5db-20d7-8125-a689-000b041554a8` (empty) |

## 4. Where the thinking stands

**The architecture, in one paragraph** (from `architecture-v1.md`). An AI-native services firm:
- keeps a shared, live record of the thing it serves, with authority to act held in that record;
- acts where its client's acts take effect, in whatever money position its legal role requires, within policies written in layers by those with the right to write them;
- sells conditions kept true and moments made fast, and backs its promises with capital;
- decides for each component whether agents, owned crews or people produce it, and puts named people where judgement, accountability, opposition, crisis or consent meet the service;
- names every party and the principal, and never gains from anyone's loss;
- designs for capacity over time and for the service to survive the firm;
- grows its own next generation of judges;
- runs on an engine that turns every case into a tested improvement, with people owning the definition of good.

**Reach, by component:**

| What the component produces | What the architecture is |
| --- | --- |
| Information, a decision, money or legal status | The whole design |
| A physical change to a thing | The control layer, plus crews and capital |
| A human act, such as care | The support layer only. "People at the edges" broke in home care |

**The parameters that predict the form:**
- the principals: how many, how aligned, and who is principal;
- whether the firm is agent or principal in law;
- who writes the rules;
- continuous or episodic;
- who pays and who benefits;
- who controls the outcome;
- client size;
- what is produced;
- trajectory;
- honesty of inputs;
- horizon.

**Lessons across seven services:**
- Redesign beats automation.
- The bottleneck is usually outside the firm.
- The product changes more than the headcount.
- Risk and capital come back once the firm controls the work.
- The firm must be trusted by parties it doesn't serve.
- In care, labour doesn't compress.
- Judgement has to be manufactured.
- Law is a design variable.

**Open and unresolved:**
- **The review rule:** whether regulators and insurers accept sampling instead of review of every output. It decides headcount everywhere.
- **Retention:** whether a firm keeps its savings. Nothing measures it. Filed deflation in comparable services cuts against it.
- **Reviewer deference:** review may not check anything (library finding L014: 86% adoption of the agent's lean).
- **Effort moved to the client:** moving work to the source may just shift effort onto the client (L004).
- **Unproven:** that the service survives the firm, capital behind outcome promises, and how judgement is grown.
- **All economics and headcounts are conjecture.** All company figures (Dwelly, Pennylane, Crosby) are self-reported.

## 5. What to do next, in agreed order

1. **Retrofitting a messy incumbent with many systems.** Ben said "yes please" to starting this, then asked for this handover first. **This is the next unit.** Material is ready:
   - `library-review/synthesis.md`, section 5: a retrofit sequence assembled from Pluris vendor claims (read-only extraction first; map what people actually do; find leakage between systems; write policy before agents; replay production data; phased cutover). Also new-record-beside-old, past tickets as first tests, ungoverned AI in acquired firms, keeping the veteran experts, and the adoption wall.
   - Library: V002 (mine the ERP event log for a baseline), V008 and N064 (a vendor refusing integration), V006 (capacity-to-P&L).
   - The architecture's level-3 target, and the build-versus-buy paths in step 4, section 8.

   Suggested shape:
   - the incumbent's starting state;
   - what to keep, rebuild or throw away, by architecture element;
   - the sequence and gates from day one;
   - people and adoption;
   - the data and system migration;
   - economics and the losses of the transition;
   - when to retrofit and when to buy the book and rebuild.

   Use the method in section 2, one reviewer pass (balanced), then show Ben.
2. **Where to build or invest,** across the whole map of services, not just the seven. Keep attractiveness, strength of evidence and fit apart, as library analysis A003 does.
3. **A blind test on statutory audit.** None of the seven services shaped it, and it is the purest test of duties to non-paying parties.
4. **Decide with Ben whether to fold in the library review's counter-opinions** (section 4 above), and whether to ingest outside sources as Source rows. The library's instructions require that, and it has not been done.

## 6. Method notes that worked

- **One author per unit,** then a reviewer who attacks it, then a revision with a "review and response" section. Show Ben the revised version.
- **Practitioner and builder pairs per worked example,** told to design around obstacles rather than retreat to automation.
- **Blind scoring.** Strip verdicts before independent scorers read (see `blind/`). One author scoring their own designs drifts.
- **Workflows** (multi-agent scripts) suit parallel reading, reviewing and copying to Notion. Ben opted in. Keep each run scoped to one unit.
- **Subagents sometimes can't write report files.** Have them return text, then save it from the run journal.
- **Copying to Notion:** do it word for word in chunks with `insert_content`, never `replace_content`. Escape `$`, put file names in inline code, then verify headings, table rows and the last line. Container restarts interrupt long runs; resume by checking what exists before appending.

## 7. Cautions

- Ben pasted API keys for Firecrawl and Hyperbrowser into the chat on 23 November. They were never needed and are not recorded anywhere in the repository or Notion. Do not copy them. Suggest Ben rotates them if the transcript is shared.
- Do not edit Ben's Notes, and do not change any existing synthesis's Thesis or status without Ben.
- Do not put model names in commits or repository files.
