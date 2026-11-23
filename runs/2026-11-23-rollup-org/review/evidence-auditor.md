# Evidence audit of draft v1

Reviewer: evidence auditor. 23 November 2026. Audited: `design/draft-v1.md` against `ledger.md`, the seventeen files in `evidence/`, `inventory-A.md` and `inventory-B.md`, with spot checks in the three rival designs.

## Verdict

The draft is careful with quotations and careless in a smaller number of summary sentences. Every quoted passage I checked is in the row or inventory the draft cites, word for word, and none of the three known corrections is repeated. The problems are of a different kind: about twenty-five sentences tagged [source says] are really the draft's, the ledger's or a researcher's reading, and a handful of them carry weight. The most serious are in the thesis and the worked example: "the check was most of the cost that remained" rests on two vendor case studies, one of which does not say it; "the tax guidance reads as review of each tax deliverable" is an inventory author's reading of a document a third read, and it fixes firm A's control; the worked-example scores come from a ten-item test, not the thirteen-item test with hard gates that the draft publishes; and "only the audit opinion is reserved by law" is tagged as sourced when the inventory marks it as inferred and unchecked. None of these reverses the design. Several would change how confident the thesis may sound, and two (the tax-review reading and the re-scoring) should be settled before the worked example is relied on.

## What I checked, and what share

| What | In the draft | Checked | How |
| --- | --- | --- | --- |
| Quoted passages in the body (above the Sources section) | about 125 | all | Matched by script against the evidence rows and inventories, then against the row actually cited on that line |
| Evidence rows cited by ID | 185 distinct | all 185 | Read each row's claim, kind, quote, speaker and read-depth against every sentence that cites it |
| Sentences tagged [source says] | 87 | all 87 | Read against the cited row, inventory passage or ledger section |
| Inventory figures and quotations | about 50 | about 45 | Looked up in the inventory text; arithmetic re-done where the draft derives a number |
| References to ledger sections, findings and questions | about 20 | about 15 | Read the ledger passage |
| Statements about the three rival designs | about 40 | 6 | Spot checks only (centre sizes, the mandate quotation, the 10 to 15% figure) |
| Sources table (URLs against rows) | 109 URLs | 109 by script | 104 match the cited row; the other 5 sit on "same source as" rows and look right |

Overall I checked about nine in ten of the tagged claims, numbers and quotations. Not checked: most of what the draft says the rival designs propose, and any primary source. Like the draft's author, I read evidence rows, not the documents behind them, so a quotation that is wrong in the evidence file would pass this audit.

## Objections, ranked by how much they matter

Line numbers are lines of `draft-v1.md`.

### A. Would change what the thesis or the worked example may claim

**1. "Where automation worked, the check was most of the cost that remained."** Thesis point 4, line 21; repeated in spirit at Part 14 ("the main residual cost").
- Tagged [source says], citing R-LIB-DELIVERY-29 and R-WEB-MAPPING-06.
- R-LIB-DELIVERY-29 is a vendor (Fractional AI) on an unnamed customer: "About two-thirds of the remaining cost is the QA layer the client chose to keep". Kind: company claim.
- R-WEB-MAPPING-06 is Marble's case study. It says human time fell from 14 hours to 6 and "a specialist approves every response". That the remaining six hours are the check is the researcher's reading, marked "[inferred]" in the row. The row gives no split.
- So: two company claims, one of them an inference, presented as an observed pattern.
- Fix: "Two vendor case studies point the same way: one says two-thirds of remaining cost was the retained check (self-reported, customer unnamed); in the other, human time fell less than processing time while a person approved everything (the split is not given). [inferred] The check is likely to be the main residual cost."

**2. "The tax bodies' guidance reads as review of each tax deliverable."** Thesis, weakest premise, line 27; Part 8, line 500; Part 13, line 643.
- Tagged [source says] (inventory A, S9). The words are the inventory author's, in a "Still open" list (inventory A line 97), about a document "about a third read".
- What the inventory quotes from the guidance: AI output should be "reviewed with appropriate scepticism", and where software "can be configured to make human review optional" the member should ensure "the data and the submission can be subject to an appropriate review". "Can be subject to" is not plainly "each one must be".
- This reading fixes the control at firm A ("every filed return is reviewed by a person") and is one of four props of the weakest premise.
- Fix: tag as "[inferred, the inventory author's reading of a guidance document read in part]", quote the two passages, and make the professional body's answer an explicit output of experiment 1. Keep the cautious planning assumption; do not present it as a rule.

**3. The worked-example scores were made with a ten-item test, not the test the draft publishes.** Part 6 lines 339 ("the thirteen scores") and 357 to 381; Part 4 line 268; the Scores table, lines 755 to 764.
- Both inventories score ten items ("All ten items met", inventory A line 307; "scored on the ten items", inventory B line 409). The draft's test has thirteen items and five hard gates, and a different status rule.
- The status shares (8%, 52%, 26%, 15%; 6%, 49%, 23%, 22%) and "met on 14 of 87" are therefore not results of the draft's test. Inventory A also says item 7 "sorted nothing as scored" and should be re-scored; the draft's question C does that, but no line has been re-scored.
- Fix: say under the Scores table that the figures are from the inventories' ten-item version, that items 11 to 13 and the gate rule were not applied, and that shares could move. Or re-score.

**4. "At firm A only the audit opinion is reserved by law."** Line 142, tagged [source says]; relied on at line 43 ("both reference firms are less protected by licence than the word suggests") and line 764.
- Inventory A marks the whole passage "[inferred, general knowledge of UK law … not checked against statute in this run]". The draft adds "not checked against a primary source" only for firm B.
- The draft admits this in its weaknesses list (line 895), but the tag in the body is still wrong.
- Fix: retag as "[inferred by the inventory author; unchecked]" for both firms. "About 12 signatures and under 5% of hours" is correct arithmetic on model hours (2,200 of 49,010).

**5. "Every production loop has a machine proposing and a named person approving."** Thesis point 5, line 22.
- The ledger says a machine "may propose" (Part 10). R-WEB-SELFIMPROVE-01 says of Sierra that "the proposer is a person, not the agent". The ledger also records one ungated production account, Spawn (Q4, contradictions; self-reported).
- Fix: "In every production account but one, a named person approves a change; in several the proposal also comes from a person. The exception is Spawn (self-reported; software; reversible in seconds)."

**6. The freight-forwarder case is carried too far.** Line 122 and line 126.
- "A workflow with state, procedure, a write path and a test set scored '92.8% versus 22.3% in production'" (R-LIB-DELIVERY-05). The row says: "That it had 'all four' is my reading of the record", and "success defined differently for the two rates".
- The draft keeps "implementer's own figures" and drops both caveats, then uses the case twice: against the full inventory and against the four requirements as sufficient.
- Fix: add "by the researcher's reading it had all four; the two rates use different definitions of success".

### B. Wrong or overstated against the row

**7. "Cases ran without a built verifier only as suggestions to a person who checked everything, at low volume" (R-LIB-DELIVERY-09/33).** Line 126.
- Carta (R-LIB-DELIVERY-09) is not low volume: R-LIB-DELIVERY-08 gives cash reconciliation at 20,000 to 25,000 a month. Only the two-lawyer firm in R-LIB-DELIVERY-33 is small.
- R-LIB-DELIVERY-33 also rests partly on B8, one of the Pluris promotional cases the ledger lists as unchecked.
- Fix: drop "at low volume", or apply it to the law-firm case only; mark B8 as promotional.

**8. "Every lasting acquirer ties sellers in for one to three years or more" (R-WEB-OWNERSHIP-22/30; R-WEB-PRECEDENTS-20).** Line 209. Copied from ledger line 110.
- Three firms, not every one: Brown & Brown, Knights, Gallagher. Constellation, Berkshire, Danaher and Halma are not shown.
- Brown & Brown and Gallagher rows describe earn-outs measured over one to three years, which is a payment term, not a requirement to stay. Brown & Brown's key staff "are not prohibited from competing with us". Only Knights ties payment to "continued employment".
- The draft elsewhere rejects earn-outs on the firm's results, so these precedents support less of its own seller design than the sentence implies.
- Fix: "Three listed acquirers defer part of the price over one to three years; one of them ties it to the seller staying."

**9. Outsourcer margins.** Line 694 and line 863.
- "12.6% to 15.4% operating margins (Concentrix, Teleperformance, Accenture)" mixes three measures: Concentrix non-GAAP operating margin (12.6%), Teleperformance recurring EBITA margin (13.6%), Accenture operating margin (15.4%). Two of the three come from results releases, not filings.
- Line 863 says "Listed outsourcers earn 10 to 15%" with no citation. It is copied from `design-mandate.md`, and no cited row gives a figure as low as 10% (the lowest is Concentrix's 11.8% for one quarter).
- Fix: name each measure; change line 863 to the same range and cite the rows.

**10. "Agent management rose 'from 10% … to 22%' of sessions."** Line 542 (R-WEB-GOVERNANCE-15).
- The quoted figure is for "meta-work"; the source says "much of this rise" was agent management. The row's own claim line makes the same slip.
- The next sentence, "Agents do not reduce management time", is an inference from one software firm that tripled in size (R-WEB-GOVERNANCE-16 gives that caveat). It sits in a [source says] paragraph.
- Fix: "meta-work, much of it agent management, rose from 10% to 22%"; tag the conclusion [inferred].

**11. "22% of hours physical."** Line 816.
- 22% is the whole "leave with people" share at firm B (18,410 hours). Physical presence is 8,300 of 84,740 hours, about 10% (inventory B section 3.3). Line 761 has it right.
- Fix: "about 10% of hours need physical presence; 22% stay with people".

**12. "RSM Tenon, Slater and Gordon and Ince failed after debt-funded or over-priced buying."** Line 82.
- RSM Tenon and Slater and Gordon: supported (the latter from an encyclopaedia summary, "summary only").
- Ince: R-WEB-OWNERSHIP-31 records the purchase and the administration with no cause; R-WEB-OWNERSHIP-32 says the regulator's page "gives no reason and no amount".
- Fix: take Ince out of the causal sentence, or say "collapsed; cause not in the evidence". Mark the Slater and Gordon and Ince rows as second-hand.

**13. "Danaher mandates its system."** Line 109.
- R-WEB-PRECEDENTS-04, which the draft cites elsewhere, quotes Danaher: "Not every operating company has to implement every tool." The row's reading is "limits a full, uniform roll-out".
- This matters because chain 5 takes "Danaher's form for the management system" as the precedent for a mandated method.
- Also: the quotations come from executives speaking to a magazine, through an extraction tool, "quotes not re-checked against raw text". "Company accounts" at lines 109, 136 and 571 reads like financial accounts. Say "the company's own telling".
- Fix: "Danaher mandates the core (training, a plan in 100 days, a monthly review) and lets firms choose among the tools."

**14. Concentrix's goodwill write-off used as an AI warning.** Line 725.
- The quotation is exact, but the row says the charge was "primarily resulting from the trading range for the Company's stock price" and "not to a stated loss of clients".
- Fix: add "attributed by the company to its share price".

**15. "Fixed fees to small payers hold it until renewal (R-WEB-COMMERCIAL-04)."** Line 170, tagged [source says].
- The row is Accenture's chief executive on enterprise clients. "Fixed price lets the supplier keep a saving until renewal" is the researcher's inference; nothing in it is about small payers. The draft's "untested for small-business clients" understates this: it is unevidenced.
- Fix: retag [inferred].

### C. Long Lake, and other self-reported material not marked

**16. Long Lake rows used without the self-reported label.**
- Line 292: "Long Lake's pace of about ten deals in under five months (R-WEB-ROLLUPS-07)". This is the researcher's subtraction of a journalist's count (about 30, May) from Long Lake's own (40, September). R-LIB-STRUCTURE-11 notes the count is itself inconsistent ("'40th' … '35th'"). Fix: "implied by two counts that do not agree; self-reported".
- Line 314: "Freed capacity is not profit until someone sells it (R-LIB-FAILURES-16)" is Long Lake's founding partner's thesis (kind: proposal; "no outcome data"). Fix: attribute it.
- Line 437: "'net adding jobs', as Long Lake does (R-WEB-ROLLUPS-04/25)". The speaker in the row is General Catalyst, its investor; the words are not in R-WEB-ROLLUPS-25. Fix: "as its investor says of it (R-WEB-ROLLUPS-04)".
- Lines 15, 122, 290 and 411 are labelled correctly.

**17. Other company claims stated flat under [source says].**
- Line 477: "Sierra tried an agent per role, found it failed" (R-LIB-GOVERNANCE-17/18; an engineer on his own tool, "summary only", no outcome measure).
- Line 500: "Ramp's agent decides most approvals under hard-coded limits" (R-WEB-STACK-20; 65%, Ramp on its own product).
- Line 269: "One vendor refused" a write path (R-LIB-IMPROVE-TECH-34; an implementer's pitch; "its own figures conflict").
- Line 347: "Implementers redesign first" (R-LIB-DELIVERY-03). One implementer, Varick, describing itself. Copied from ledger line 218.
- Line 23: the semiconductor second-team figure (R-WEB-STACK-05) is OpenAI describing its own paid service, and falls in the ledger's Thrive-with-OpenAI origin group.
- Line 542: "Danaher cut its measures from 150 to eight" is Danaher's telling.
- Line 597: "About 1.5 engineers over months" (R-LIB-IMPROVE-TECH-30) drops the row's condition: built on "an identity system already owned".
- Fix for each: add "by its own account" or the equivalent.

### D. One origin counted more than once

**18. Ciridae counted twice.** Line 455: "every hard case failed below the top (R-LIB-PEOPLE-15/16; R-LIB-FAILURES-09)".
- R-LIB-PEOPLE-15 and R-LIB-FAILURES-09 are the same case (N016; the ledger lists them as one origin). R-LIB-PEOPLE-16 is a recruiter's promotional claim that the analyst "did not accept".
- So "every hard case" is one implementer's marketing story and one recruiter's. Fix: "in the two accounts on file, both promotional, the failure was below the top".

**19. The insurer evidence is one law firm's article.** Lines 27, 88, 487, 634, 643.
- R-WEB-LAW-25 and inventory A's S11 are the same Browne Jacobson article of February 2026. With R-WEB-LAW-24 (DAC Beachcroft) the whole insurer side is two law firms' commentary.
- R-WEB-LAW-25's question is about "AI-generated legal outputs before submission to courts or clients"; the draft applies it to accountants and property managers without saying so. (S11 does have questions aimed at accountants; cite those instead.)
- Fix: "one law firm advising insurers suggests they ask …"; note the shared origin.

**20. Chain 5 rests on two operators' letters.** Lines 107 to 112.
- Six row citations, two origins (Constellation; Danaher), plus Berkshire in the thesis. The draft's list of shared origins at line 79 names Long Lake, Thrive, Chroma, Dwelly and Anthropic but not these.
- Fix: add Constellation, Danaher and the CMA vets inquiry to the line 79 list.

**21. "Three unrelated firms" for the gateway pattern (R-WEB-STACK-14/16/18).** Line 608.
- The origins are separate. But the Pinterest row was "seen through secondary summaries" (the page returned 403), and Cloudflare sells the components it describes.
- Fix: "three firms' own accounts, one read only as a search summary".

### E. Tagged [source says] but really inference (smaller cases)

- Line 21 and line 27: "faster preparation with unchanged review only moves the queue to managers (inventory A section 3)". The inventory tags this "[inferred]".
- Line 453: "trainees learn on the lines handed over first". "[inferred]" in inventory A. The 2,300 hours is a model assumption, correctly called "model hours".
- Line 502: "Records people must enter by hand die (R-LIB-GOVERNANCE-31)". The row's kind is "hypothesis".
- Line 169: "Nobody has shown an owner keeping an AI saving (R-LIB-ECONOMICS-01/08)". The rows say the library holds no measured case. "Nobody" is wider than the source.
- Line 170: "Enterprise buyers claim the saving through procurement (R-WEB-COMMERCIAL-15/18)". The rows give two executives saying they will, two banks' lower spend, and a law firm's list of terms to negotiate. Stated intent, not an observed result.
- Line 122: "The one account of extensive mapping first took over a year (R-LIB-DELIVERY-16)" is used against mapping. The row reads it as "supports mapping as a first move, at a cost of a year", and says later firms were "reportedly" faster. Say both.
- Line 94: the KPMG study (R-WEB-PEOPLE-17) compared juniors working with an agent against the agent alone. It did not test sign-off. Using it for "sign-off is not an independent check" is the researcher's inference.
- Line 451: "Usage rewards drove cost at Uber and fear at Proton". Uber had a leaderboard; Proton had a mandate with tracking, from anonymous staff in an outlet with "a declared stance". Neither row describes rewards.
- Line 620: "the acquirers that failed could not see their cash". One case, Wind River (R-WEB-PRECEDENTS-33).
- Line 132: Marble "presents capture as switched on by employees at team level". The row says employees install it and analysis is grouped by team. Two different things run together.

### F. Numbers with no source, or with the derivation missing

- Line 267: diligence takes "about a week on the floor, then two to four more". "About a week" is inventory B's own unevidenced estimate; inventory A says of the same cost "I have no measured cost for that and will not guess one". "Two to four more" has no source. Mark both as design choices.
- Line 681: five firms' "combined revenue is perhaps £12m to £17m". Five of firm A is £11m to £14m; five of firm B is £15m to £20m. The mix behind £12m to £17m is not stated.
- Line 863: "10 to 15%" (see objection 9).
- Line 571: "Every AI-era loop on file is under three years old". It is in the ledger (line 426) but carries no citation in the draft.
- Line 173: "46% of surveyed UK mid-tier firms" (R-WEB-PRECEDENTS-26). Correct, but the row says the sample size was "not confirmed" (the previous edition had 36 firms) and the answers are the firms' own.
- Line 173 files the Dwelly operating account under "Block management". It is lettings maintenance, as lines 31 and 816 say.
- Design numbers that are declared as choices and need no source: the centre sizes, 12 to 18 months for the resident, three-year seller terms, four-year unit holding. These are fine as labelled.

### G. The three known corrections

None is repeated.
- Anthropic and logging: the draft does not say Anthropic logs everything. Its only uses of the employment report are the meeting and meta-work figures (see objection 10).
- The Scribe test: not cited. The draft makes no claim that a wiki made an agent worse.
- Long Lake: four of seven uses carry "self-reported"; three do not (objection 16).
- Blomfield: named only as one side of a dispute at line 502. No Blomfield figure is used.
- Spawn: cited at lines 485, 491, 492 and 716 with no figures, and line 716 is marked "one firm's founder". Acceptable. Principle 9 ("every change can be undone") cites R-LIB-IMPROVE-TECH-09 as an origin; add "self-reported" there.

## What checked out

- All quoted passages match the cited rows. I found no altered or merged quotation.
- Sample sizes and dates the draft adds in brackets are in the rows: 50 analysts; 79 firms; 523 juniors; 1,000 clients; o3; GPT-5.4-mini and Haiku 4.5 on ten tasks; "late 2025"; the 2027 ICAEW result.
- Inventory figures match: 87 and 123 lines; the status shares; 14 of 87 and 37 of 123; 1,300 hours inside HMRC's web pages; 8,300 physical hours; the 850, 2,000, 1,500 and about 11,000 hour case sizes; fee, margin, lock-up and insurance figures; "about four" things to build; "about ten of 123" productisable lines.
- Derived figures are right: £0.6m to £1.0m profit before partners' pay; "half of juniors … did no better" (25.8% plus 24.1%); "under 5% of hours" for audit.
- The ledger references (findings 1 and 10; sections 1, 3 and 5; Parts 2, 3, 5, 8, 9 and 14; Q1 to Q3) say what the draft says they say.
- The draft's own statements of what it did not read are accurate and prominent.

## A note on where the faults come from

About a third of the overstated sentences are copied from the ledger (objections 5, 8, 16 first item, 17 fourth item, and "enterprise buyers claim" in section E). Fixing the draft alone will leave them in the ledger for the next reader. The same goes for the slip in R-WEB-GOVERNANCE-15's claim line.
