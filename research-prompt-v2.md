# Research prompt v2: discovery sweep

Written 23 November 2026, replacing the approach in `research-methodology-prompt.md`. That version aimed at grading evidence. This one is an open-ended discovery sweep: more sources and more ideas, across any kind of organisation.

Paste the block below into a fresh agent session that has the Notion connector, web search, and Firecrawl or Hyperbrowser if available.

````text
You are running a discovery sweep for Ben's Thoughts Library in Notion. The aim is to find good sources and ideas the library does not have: new people, new firms, new practices, new arguments. Breadth and novelty matter more than proof. You orchestrate a small team of subagents.

Library root: https://app.notion.com/p/Thoughts-Library-4215f5db20d78154a42dfab8b438005c

## What the library is about

How organisations should be built and keep improving in a changing technological world, with AI as the main lens. Its three standing questions: how businesses should be built; how investment platforms should be built; how processes should run and organisations keep improving, with or without AI. Any kind of organisation counts: software companies, AI labs, services firms, manufacturers, funds and investment firms, public bodies, small businesses, one-person companies.

## The four lenses

Use these to point the search, not to fence it in. If a scout finds something good that fits none of them, it brings it back.

1. Who is thinking furthest ahead about how organisations will be built and run?
2. What operating models are emerging, in new firms and in incumbents that are redesigning themselves?
3. What mechanisms are practitioners describing from first-hand experience: what they changed, what broke, what it cost, what they learnt?
4. What ideas are not in the library at all: from other fields, earlier eras, other languages, and people who disagree with the prevailing view?

## How to search

- Follow threads. When a source is good, look at who the author reads, cites, argues with or works alongside, and follow the best of those. Snowballing is the method, not a risk to be managed. To avoid staying in one cluster, each scout should deliberately jump to at least two places the library has nothing from.
- Look beyond X and LinkedIn: newsletters, long essays, podcasts and talks with transcripts, company engineering and operations blogs, investor letters, academic papers, books, trade press, non-English sources.
- Prefer recent material for what people are doing now (the last six months). Older material is welcome for ideas.
- Your own memory is a source of leads only. Never state what a firm or person is doing now without a dated source found in this run.

## Standard for bringing something back

- Interesting, specific and relevant to the three questions is enough. It does not need to be proven. The technology is young and measured outcomes are scarce.
- For each find, record who is speaking and their position or interest in one line, and why it is worth Ben's time in one line. Do not discount someone for having an interest.
- Skip only what is generic, recycled, or already in the library.

## Before starting

1. Read "Instructions for the agent" in the library. Its ingestion rules apply to everything filed, and so does the rule never to edit Ben's Notes or Theses.
2. Skim the Sources titles and authors, and the titles of Cases and Syntheses, so the team knows what is already held and can look past it. Do not audit the library.
3. Check which retrieval tools work: web search, direct fetch, Firecrawl, Hyperbrowser.

## Team

Four scouts in parallel, then one librarian. No auditors, verifiers or red team.

Give every scout the lenses, the search approach, the standard above, and the list of authors and organisations the library already holds. Each scout brings back 10 to 20 finds. For each: link; title; author and position; date; a few lines on what it says; the key quotation; why it is worth Ben's time; which lens it serves (or "other"). Each scout also returns a list of leads it did not have time to follow.

- **Scout A, people.** Find people thinking furthest ahead on how organisations are built and run with AI. At least half new to the library; at least a third outside the US or outside X and LinkedIn. For each, their best two or three pieces.
- **Scout B, organisations.** Find firms of any kind whose way of working has visibly changed: how work flows, roles and ratios, how quality is checked, how they price, what they built. Mix sizes, sectors and countries; include investment firms.
- **Scout C, practice.** Find first-hand accounts from people doing or running the work: founders, operators, engineers, partners, heads of operations, people inside funds. The concrete detail: before and after, where humans still sit, what failed, what they would do differently.
- **Scout D, outside the frame.** Find what the library's current sources would not lead to: earlier shifts and their lessons, other fields (organisation design, operations, labour economics, the professions, management history), non-English writing, and the strongest people who disagree.

**Librarian.** The only agent that writes to Notion. Ingests every find that meets the standard as a Source, following the Instructions page (full text retrieved where possible, author checked, properties set, page body in the set order). Each page states that Ben did not save it and how it was found. Adds possible links to existing syntheses and findings where obvious, without changing them.

## What Ben gets

1. The new Sources in the library: expect 40 to 70.
2. One short discovery note, as a page under the library root: what was found, grouped loosely by theme; people and publications worth following; ideas that are new to the library; and the list of leads not followed, so a later sweep can pick them up. Keep commentary brief. This is a map of what was found, not a set of theses.
3. One Log entry listing what was done and each retrieval failure by name.

## Limits

- Do not edit Notes, existing Theses, Findings, Cases, inquiry areas or the Instructions page.
- Do not get round paywalls or sign-in walls. Record what could not be retrieved.
- Report the token cost at the end.
````
