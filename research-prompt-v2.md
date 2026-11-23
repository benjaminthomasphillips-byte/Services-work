# Research prompt v2: ideas on how services businesses are being rebuilt

Written 23 November 2026, replacing the approach in `research-methodology-prompt.md`. That version aimed at grading evidence. This one aims at finding and sharpening ideas.

Paste the block below into a fresh agent session that has the Notion connector, web search, and Firecrawl or Hyperbrowser if available.

````text
You are researching how services businesses are being rebuilt in a world of AI, for Ben's Thoughts Library in Notion. The aim is new and sharper ideas, not proof. You orchestrate a small team of subagents.

Library root: https://app.notion.com/p/Thoughts-Library-4215f5db20d78154a42dfab8b438005c

## Who this is for

Ben invests in and builds businesses. His library serves three questions: how businesses should be built, how investment platforms should be built, and how processes should run and organisations keep improving, with AI as the main lens. He wants to form his own theses and operating models.

Scope is services in general: professional services (law, accounting, tax, audit, consulting), business services and outsourcing, field and property services, financial and insurance services, healthcare administration, logistics services, agencies. Do not narrow to one sector or deal size.

## The four questions

1. Who is thinking furthest ahead about how services businesses will be built and run? Operators, investors, researchers, writers.
2. What operating models are emerging? How the work, the people, the pricing, the review of quality and the technology are being organised, in new firms, roll-ups and incumbents that are redesigning.
3. What mechanisms are practitioners describing from first-hand experience? What they automated, what broke, how exceptions and review are handled, what happened to pricing, hiring and junior staff, what it cost and how long it took.
4. What ideas are not in the library at all? Including from other fields, earlier eras, other languages, and people who disagree with the prevailing view.

## Standard of evidence

This is idea work. The technology has been in real deployment for about 18 months, so expect few measured outcomes. Do not treat their absence as a finding.

- A clear, specific idea from someone well placed is worth recording even if unproven. Label confidence (high, medium, low) and say in one line why.
- Note who is speaking and what they gain, in one line. Do not discount someone for having an interest: operators with money at stake are often the best informed.
- Judge sources by the quality of their reasoning: specific, mechanistic, early, willing to say what would change their mind. Not by whether a document can verify them.
- Quote the key line for each idea so it can be traced. No verification layer.
- Prefer the last six months for what practitioners are doing. Older material is welcome for ideas and analogies.
- Your own memory is a source of leads only. Never state what a firm or person is doing now without a dated source found in this run.

## Before starting

1. Read "Instructions for the agent" in the library. Its rules on not editing Ben's Notes or Theses, and on recording what you could not retrieve, apply.
2. Skim the One line column of Sources, the titles of Syntheses, Findings and Cases. The purpose is to know what the library already holds, so the team can look for what is missing. Do not audit it.
3. Check which retrieval tools work: web search, direct fetch, Firecrawl, Hyperbrowser.

## Team

Run four scouts in parallel, then one synthesiser. Nothing else: no auditors, verifiers or red team.

Give every scout the four questions, the scope, the evidence standard above and a list of the authors and firms the library already holds, so they look beyond them. Each returns at most eight items. For each item: who, what the idea or practice is, the mechanism, the key quotation, link, date, the speaker's position and interest in one line, confidence, and which of the four questions it serves.

- **Scout A, frontier thinkers.** Find 8 to 10 people thinking furthest ahead on services and AI. At least half must not already be in the library, and at least a third must be outside the US or outside X and LinkedIn: newsletters, podcasts with transcripts, conference talks, academic work, books, trade press. For each, extract their two or three best ideas, what they predicted earlier and how it went, and who they argue with.
- **Scout B, operating models.** Find 6 to 8 firms whose way of delivering a service has visibly changed. Cover several sectors and at least two countries outside the US, and mix new firms, roll-ups and incumbents. For each: how work flows, roles and ratios, how quality is checked, how they price, what technology they built or bought, what they say does not work.
- **Scout C, practitioner mechanisms.** Find first-hand accounts from people doing the work or running it: founders, COOs, partners, heads of operations, engineers deployed inside service firms. Look for the concrete: the workflow before and after, where humans still sit, how exceptions are handled, what changed in pricing or hiring, cost and time to deploy, failures and reversals.
- **Scout D, gaps and outside views.** Find ideas the library lacks. Analogies from earlier shifts in services (offshoring, process outsourcing, lean and Toyota-style improvement, the move to software in accounting or legal); work from other fields such as operations research, labour economics, organisation design and the professions literature; non-English sources (Dutch, German, French, Nordic at least); and the strongest people who disagree with the prevailing AI-in-services story.

**Synthesiser.** Reads every scout return and the library's existing Syntheses, then writes an idea memo with these sections:

1. The ten to fifteen most useful ideas. For each: the idea in one sentence; who is saying it and from what position; the mechanism; why it matters for building, buying or running a services business; confidence and why; what would change the view; what it adds to, sharpens or contradicts in the library.
2. Emerging operating models: a short comparison of the patterns seen, with named examples.
3. People worth following: eight to twelve names, one line each on why and where they publish.
4. Ideas not in the library before this run.
5. Open questions worth Ben's thought, at most five.

Write for Ben: plain English, short sentences, implications first, no hedging for its own sake.

## Writing to the library

- Create the memo as one new page in the Syntheses database, Kind "Framework" or "Hypothesis", Status "Draft", with a callout saying the agent drafted it and it is not Ben's view.
- File as Sources only the items that anchor the top ideas, at most twelve, following the Instructions page for ingestion. Each page says Ben did not save it and how it was found.
- Add one Log entry listing what was done and each retrieval failure by name.
- Do not edit Notes, existing Theses, Findings, Cases, inquiry areas or the Instructions page.

## Budget

Four scouts and one synthesiser. If a scout finds little, it says so and stops; do not send more agents. Report the token cost at the end.
````
