# Review of step 2 draft: "If the engine works, what becomes a commodity, and what is left?"

Reviewer, 24 November 2026. Single reviewer. Cited rows checked against `runs/2026-11-23-rollup-org/evidence/` and `ledger.md`. General-knowledge comparisons judged from my own knowledge; where I offer replacements they are also general knowledge and should be marked as such.

---

## Verdict

The draft is well organised but argues less than it appears to. Its spine (Q1's four conditions, the scarce-goods list, the barbell, the five-to-ten-year window) is largely the earlier run's ledger Q5 and row R-LIB-ECONOMICS-33 restated in cleaner prose, plus standard economics (price elasticity, aggregation, hollowing of the middle). The one idea presented as the big new force, credence goods closing from the buyer's side, is misapplied. It treats routine filings as credence goods when they are mostly experience goods. It says opacity premiums vanish while keeping "judgement nobody can verify", which is an opacity premium, as a source of margin. And it ignores that a client who relies on its own AI to check the work has moved the credence problem to whoever supplies that AI rather than removed it. Its headline claim that buyer-side checking "erodes margins faster and further" than falling costs has no mechanism comparing the two and rests on one vendor survey. The question the client most needs answered is who captures the surplus once the engine works. The draft barely asks it. Model providers, insurers, buyer-side agents, the professionals themselves and the state are absent or appear only as counter-arguments. The state's absence also contradicts step 1's P3, which named the state as a place where checkable services become free. The design section then contradicts itself: price near cost now, but use a window in which the routine tier "still pays"; own the client's live records, but those records already sit with the software vendors that Q4 names as the threat. Fix the credence argument, add a surplus-capture section, and resolve section 3. The rest is tidying.

---

## Objections, ranked by how much they should change the draft

### 1. The credence-goods framing is misapplied and contradicts the draft's own list of scarce goods
**Section:** The answer in brief, point 2; Q2; Q5 ("judgement where nobody can verify"); section 3.4.

**Problem.**
- **Wrong goods.** A credence good is one whose quality the buyer cannot judge even after buying (Darby and Karni). Most routine compliance work is not like that. A filing is accepted or rejected, a penalty arrives or it does not, the books reconcile or they do not. These are experience goods, and largely the "consequence" checks of step 1's P1. The credence element in professional services sits in diagnosis and advice: was the work needed, was the tax position the best one available, was the settlement good. So whatever opacity premium there is lies mostly in the judgement tier, not the routine tier the draft says AI will commoditise.
- **Self-contradiction.** Q2 says "premiums based on opacity disappear, and premiums based on demonstrable outcomes survive". Q5 and section 3.2 then keep "judgement where nobody, human or machine, can verify the answer" as a margin layer. Margin on judgement that cannot be verified is, by definition, an opacity premium. Section 3.4 ("make the record provable") cannot apply to that layer either: step 1's P7 says many outcome labels are absences.
- **Misreads where the rent comes from.** In the economics, credence problems show up mainly as over-treatment, under-treatment and over-charging by the expert who both diagnoses and treats. Competition often turns them into excess volume rather than high unit margins (Dulleck and Kerschbamer's survey is the standard reference). Professional margins have rested at least as much on licensing barriers and leverage as on opacity. If AI narrows the gap, the first casualty may be unnecessary work, which cuts billed volume. That runs against Q3's claim that advice demand expands.
- **What the client's AI actually checks.** It checks an output against rules and market norms. That is step 1's *conformance* check, which step 1 says "measures agreement with past experts, not whether the work got better". The draft gives the buyer's AI a power that step 1 denies the firm's own engine.

**Fix.** Separate three things: (a) routine, experience-good work, where AI cuts cost and the gain passes through via Q1; (b) diagnostic and credence work, where buyer-side AI chiefly reduces over-treatment and so cuts volume; (c) residual credence, which survives and still carries a premium based on trust. Then say explicitly that the judgement desk's margin is a credence premium, and say what protects it: licence, reputation, liability. Drop "provable record" for the judgement tier, or say what proxy would stand in for proof.

### 2. "Erodes margins faster and further than supplier costs falling" is assertion presented as inference, and credence migrates rather than disappears
**Section:** The answer in brief, point 2; Q2.

**Problem.**
- The brief states it as fact. The body tiers Q2 as "mechanism; bet on how fast", and its own counter-argument says "most clients won't bother to check". Nothing compares the size of the two forces.
- The evidence is one vendor survey from TaxDome, which sells practice software. Sample method is not stated (R-WEB-COMMERCIAL-25). The row says clients *used* AI to review work. It does not say they found errors, switched, or paid less. The same row reports that 53% of clients would pay *more* for faster service, which the draft leaves out.
- Translation, the draft's own comparison, cuts the other way. Buyers usually cannot judge a translation into a language they do not read, yet prices fell (R-WEB-COMMERCIAL-12). They fell because buyers accepted "good enough" substitutes, not because buyers could verify quality. Commoditisation does not need the information gap to close.
- **Missing counter-argument, and the most interesting point available here.** A client who checks work with its own AI must trust that AI. Credence does not vanish; it moves to the verifier. Whoever supplies the client's checking agent (a model provider, the accounting software, a bank, a comparison platform) inherits the trust rent. That ties Q2 directly to Q4 and is far less obvious than "AI closes the gap". A second missing counter: suppliers will game whatever benchmarks the client's agent reads. Published track records are self-reported unless someone audits them, and that auditor becomes another intermediary.

**Fix.** Drop "faster and further" from the brief, or give a mechanism and a reason to compare the two forces. Re-tier the buyer-side force as a bet for anything beyond routine work. Add the migration of credence to the verifier as a premise or as a part of Q4.

### 3. "Accountability stays scarce" is the load-bearing claim and is the least defended
**Section:** Brief point 4; section 1 table; Q2 counter-argument; Q5 row 1; section 5, third bullet.

**Problem.**
- **Carrying risk is not obviously a premium business.** Selling the consequence is underwriting. In competitive insurance markets underwriting earns roughly the cost of capital, so combined ratios hover near 100% (general knowledge). A premium exists only with better information than other capital (step 1's P3 data argument) or a licence that rations entry. The first is contestable by insurers, who see more outcomes (step 1, P7). The second is a regulatory rent, and it is politically exposed once AI makes the underlying work cheap.
- **The precedents point the other way.** Liability is already moving from the professional to the system's maker:
  - autonomous diabetic-retinopathy screening cleared in the US in 2018, where the vendor, not a reading clinician, carries the liability;
  - certified autopilots, where nobody signs each landing;
  - the EU's revised Product Liability Directive, which brings software, including AI, within strict producer liability.

  All three are general knowledge, to be checked. US title insurance is an older and closer case. It largely replaced lawyers' title opinions as the way accountability for property title was carried, so the consequence moved from the professional's signature to an insurer's balance sheet (general knowledge).
- **Step 1 undermines it.** Step 1's P6 has the licensed signatory "sign for the system as well as the output". If one signatory can cover a system serving thousands of clients, the number of signatures needed collapses. The large stock of licensed professionals then makes the licence abundant, not scarce. The draft's own design accelerates the very shift that section 5 lists as a risk.
- **"Regulators require a named person" overstates R-WEB-LAW-16.** The SRA notice says solicitors remain accountable for AI-assisted work. The same row notes "no rule requires approval at each step".

**Fix.** Re-tier accountability as scarce from mechanism to bet beyond about 2030. Add the underwriting economics and the product-liability path as the strongest counter-argument. Say which version of accountability the design is betting on: a licence rationing entry, an information advantage in pricing risk, or a balance sheet. Each has a different winner.

### 4. The state as provider is missing, which contradicts step 1
**Section:** Q3 (mandated services); Q4; section 3.3.

**Problem.** Step 1's P3 says the quickest-to-check services become "cheap or free inside banks, software and the state". Step 2 drops the state entirely. Yet mandated services are where the state both sets the requirement and can most easily supply it. Examples from general knowledge:
- pre-filled tax returns in the Nordic countries and Estonia removed most of the preparation market;
- the US IRS piloted a free Direct File service before withdrawing it, which shows the US preparer market's persistence is partly political;
- Making Tax Digital routes filing through software connected to the tax authority's systems, which arguably shifts value to software vendors rather than adding work for firms. The draft lists MTD only as adding scope.

The draft's "standing" (gateways, registry access) is also being opened to software through APIs, not rationed to firms.

**Fix.** Add a premise: in mandated services the end state may be provision by the state or by a vendor at zero price. The question is then which jurisdictions and services, and on what timetable. Make "does the state or a mandated platform own the point of need?" a step 3 parameter. Re-read MTD as a channel shift, not a scope gain.

### 5. Who captures the surplus is not analysed
**Section:** Missing; partly Q4.

**Problem.** Each premise names "who gains" in one line, but there is no account of how the surplus divides among:
- **model providers**, which supply every firm's capacity, so their prices set its cost floor, and which are moving downstream into services themselves;
- **distribution owners** (Q4 covers these);
- **buyer-side agents and comparison platforms**;
- **insurers**;
- **the scarce professionals themselves** (objection 10);
- **clients**;
- **the state**.

N055 (OpenAI's deployment company and acquisition of Tomoro) is filed under "point of need". It is really evidence of a model provider entering services directly, which is a different threat. Q4 also assumes a buyer's agent behaves like a distributor that takes a share. A buyer-side agent may act for the buyer, paid by subscription, and squeeze suppliers rather than tax them. Comparison sites and buyers' brokers are the two templates, and they divide the surplus very differently.

**Fix.** Add a short section, possibly a table: for each scarce layer and the commodity tier, who could capture the surplus, by what mechanism, and what the firm must own to keep a share. Re-file N055. Split Q4's "client's own agent" into an agent acting as distributor and an agent acting for the buyer.

### 6. Section 3's recommendations contradict each other and the premises
**Section:** Section 3, items 1, 3 and 5; Q4 "What follows"; Q6.

**Problem.**
- **Near-cost pricing against the window.** Item 1 says to price the commodity tier near cost deliberately. Item 5 and Q6 say to design for a five-to-ten-year window in which the routine tier "still pays" and to use it to fund the scarce layers. Pricing near cost from 2027 gives up the window. Where Q1's conditions are absent, it also gives away a gain Q1 says suppliers can keep. Penetration pricing to buy share is a coherent strategy, but it is a capital decision for the investor and must be argued as one.
- **Loss leaders against unbundling.** Q2 imagines clients' agents comparing each layer against benchmarks. That world is hostile to loss leaders: the agent takes the cheap tier and buys accountability wherever it is cheapest. The draft needs a reason the bundle holds.
- **White label against owning the client.** Q4 lists "be the accountable partner behind a distribution owner" as a valid choice. Item 1 depends on owning the relationship and the live records. A white-label partner has neither.
- **Who owns the live state.** Q4 calls holding the client's live state "the main defence". But the ledger already lives in the accounting software, the cash in the bank and the case file in the practice-management system: the same distribution owners Q4 fears. A services firm owns the live state only if it is, or controls, the software. Say so, or drop the claim.

**Fix.** Pick a strategy per region, or state the condition under which each applies. Make the pricing choice explicit as an investment decision: when to price at cost, funded by what, until when. Add the condition that makes a bundle survive agent-led unbundling, such as liability tied to execution or switching costs in the record.

### 7. Q3 confuses demand elasticity with pass-through
**Section:** Brief point 3; Q3.

**Problem.**
- The claim that in mandated services "demand barely grows… so the saving goes to clients" does not follow. Elasticity of *market* demand decides whether volume grows. How a cost saving divides between supplier and client is decided by competition (Q1's conditions). Inelastic demand, if anything, *raises* a supplier's pricing power. The defensible version: when price falls in a mandated market, the revenue pool shrinks, because volume is fixed. In a discretionary market it may grow. That is a statement about the size of the market, not about who gets the saving.
- "The low-cost leader captures the expansion" needs an argument for scale economies in serving the new demand. Otherwise many entrants share it.
- **Evidence shows supply, not demand.** Garfield's £2 chaser (R-LIB-DELIVERY-30) shows a price, not that demand expanded. The row says "about 600 claims" has no period or base. "Makes a £300 debt worth pursuing" is the author's inference. Q3 also lacks the agreed "visible today" and "how fast" elements.
- **Missing counter.** The draft's own adversarial evidence belongs here. R-LIB-ECONOMICS-37 shows institutions damping machine-generated volume within months: complaints to the Financial Ombudsman fell about 30% after a fee for professional representatives. Discretionary expansion in contested matters will be throttled by courts, ombudsmen and counterparties' own agents.

**Fix.** Restate Q3 as a claim about the size of the revenue pool. Move pass-through to Q1. Add institutional throttling as the strongest counter. Mark the demand-expansion claim as a bet until there is volume evidence.

### 8. Q1's evidence is stretched, and the right unit is the buyer, not the service
**Section:** Brief point 1; Q1.

**Problem.**
- **Law.** "US law firm rates rose" is offered as suppliers keeping the AI gain. But hourly rates rising while hours fall is compatible with bills falling. The cited report itself says "AI… has not yet made its way to pricing". Rate rises in 2025 and 2026 are confounded by strong demand. The same report (R-WEB-COMMERCIAL-13 row note) says clients moved work to cheaper firms and in-house. So condition 4 was present, and the gain passed through in volume, not rate.
- **Cases filed as "price or volume fell".** TCS (R-WEB-COMMERCIAL-05) is IT services, not translation, and its margin *rose* while revenue fell. Teleperformance (R-WEB-COMMERCIAL-07) held margin by cutting overhead and restructuring. Suppliers kept margin by cutting their own cost even where the conditions were present. That is a third pattern Q1 lacks. TCS's "expansion in scope" is a fourth: pass-through by giving more work for the same price, not a lower price.
- **Audit on both sides.** Audit appears under "conditions present" (KPMG cutting its auditor's fee by about 14%, R-WEB-COMMERCIAL-01) and under "conditions absent" (audit fees unmoved, R-LIB-ECONOMICS-29). The difference is the buyer: KPMG is a Big Four firm that could judge and do the work itself. So the four conditions are properties of buyer segments, not services. That is a genuinely useful finding the draft walks past. Note also that R-LIB-ECONOMICS-29 is an analyst's reading of regulator text the analyst did not read.
- **Slogan.** "Decided by the market, not the technology" overstates. Condition 4, doing the work yourself, is precisely technology.

**Fix.** Re-tier the pattern from trend to mechanism with thin support. Add pass-through via scope and via volume, and margin kept through cost-cutting. Map buyer segments, not services, on the conditions. Soften the slogan.

### 9. The general-knowledge comparisons are roughly accurate but support different conclusions
**Section:** Brief point 5; Q1; Q6.

**Problem.**
- **Travel agents.** A fifteen-year decline from the mid-1990s and survival in complex and luxury travel is about right. But the decisive blow was the airlines, as distribution owners, cutting agents' commissions to zero between about 1995 and 2002, not online booking alone. Corporate travel management consolidated and grew. That supports Q4, not the barbell's timing.
- **US tax preparers.** "About half still pay a preparer" is about right; it has been in the 50 to 60% range. The persistence owes much to complexity, refund products and industry lobbying against free government filing. Much of the "assisted tier" is itself a low-cost national chain, so it is a commodity, not a trusted premium. Countries with pre-filled returns show the opposite end state (objection 4).
- **Translation.** Price pressure over about a decade is roughly fair. But volumes grew strongly over the same period, and the mechanism was "good enough" substitution (objection 2).

Better comparables, also general knowledge and to be checked:
- **US brokerage commissions:** deregulated in 1975, reaching zero around 2019. Value moved to order flow, asset gathering and advice, and advisory fees of about 1% proved sticky. The pace was decades, not years.
- **Robo-advice:** captured mostly by incumbents with distribution, not by start-ups.
- **UK insurance comparison sites:** prices became comparable, yet insurers exploited inert customers through price-walking for about fifteen years until the FCA banned it in 2022. This directly tests "clients' agents will compare".
- **Title insurance:** accountability moved to insurers. It stays high-margin because buyers are referred rather than shop, which is a credence and point-of-need story at once.

**Fix.** Keep the three comparisons but state what each actually shows. Add brokerage and comparison sites at least; they bear directly on Q1, Q2 and Q4.

### 10. The scarce human layer, and who keeps its rent, are not addressed
**Section:** Q5; section 3.2.

**Problem.**
- **For an investor, scarcity matters only if the firm can capture it.** Several of the Q5 goods belong to individuals: trust in a crisis, unwritten judgement, relationships with counterparties. In law partnerships and investment banks such rents go to the people, not to outside owners.
- **The labour market moves in two phases** the draft does not see:
  - **2027 to the early 2030s:** the squeezed middle releases many experienced professionals. Judgement-tier talent is cheap and plentiful.
  - **Mid-2030s onward:** the junior tier that used to train them is gone, so judgement becomes genuinely scarce and expensive. Step 1's §6 says the remaining work concentrates on the hardest cases, but neither step follows that through to supply.

  The design implication is not obvious and is useful. Hire the judgement layer during the squeeze. Build the training pipeline the market will stop providing. Expect the 2035 scarce layer to bargain hard.

**Fix.** Split Q5 into three groups: goods the firm can own (records, standing, capital, outcome data, licences held by the entity); goods that accrue to individuals (judgement, crisis trust, relationships); and goods that accrue to institutions. Add the two-phase labour argument, tiered as mechanism.

### 11. Valuation and international competition are absent
**Section:** Missing; bears on section 3.

**Problem.**
- **Valuation.** The client is an investor and this is a buy-and-build context. If the margin moves to carrying consequence, the firm starts to look like an insurer. It would then need regulated capital and be valued nearer to book value than on a multiple of software-like earnings. If the routine tier is priced at cost, acquired firms' revenue shrinks on a schedule. Roll-up targets in the squeezed middle are buying the part of the barbell that goes. None of this is said.
- **International competition.** Capacity becomes location-free, which ends the offshore labour arbitrage the Indian IT firms, TCS among them, were built on. Those firms will push into the scarce layers, while licences, standing and court access stay national. That protects a domestic firm and also caps its scale to one jurisdiction at a time. The models themselves come from a handful of non-UK providers.

**Fix.** Add a short section on what the barbell does to valuation: the multiple for each tier, the capital needed to carry consequence, and how the window should be priced into acquisition multiples. Add a paragraph on jurisdiction as both moat and ceiling, and on offshore providers moving up.

### 12. Much of the draft is standard thinking, and several premises fall short of the agreed format
**Section:** Throughout.

**Problem.**

*Standard thinking, presented with more weight than it carries:*
- The barbell and the hollowed-out middle (a long-standing theme in writing on the professions, e.g. Maister; Susskind and Susskind).
- AI democratising expertise and eroding the professions' information advantage. This is the Susskinds' 2015 thesis in all but name.
- Margin moving to the point of need (aggregation theory).
- Mandated against discretionary, which is introductory elasticity.
- The scarce-goods list, which is R-LIB-ECONOMICS-33 ("distribution, trust, records, regulatory authorisation and adoption pace") restated.
- Q1, which is the ledger's Q5 "assumption to design on" with two conditions added.

*Genuinely non-obvious, or nearly so, and under-developed:*
- The client's own agent as a possible point of need.
- Commodity volume as the data source for pricing the scarce layers. This is mostly step 1's P3.
- The points the draft walks past: that audit shows the conditions belong to buyers; that credence migrates to the verifier; that liability is moving to system makers; the two-phase labour market.

*Format gaps against the agreed standard:*
- Q3 lacks "visible today" and "how fast".
- Q5's table has no evidence and no "who gains" per row.
- Q6 lacks "who gains".
- Q4's "visible today" rests on unit 2, which step 1 says is superseded, and on a misfiled N055.

*Citation stretches:*
- R-LIB-ECONOMICS-37 is cited for an arms race in Q5. The row's own reading is that institutions price the extra volume away within months, which is the counter-argument. "Alloway" does not appear in the row.
- R-LIB-ECONOMICS-33 and R-WEB-STACK-23 show that playbooks are quick to copy, not that "public rules and practice guides are in the models".
- R-WEB-LAW-16 is stretched, as noted in objection 3.

**Fix.** Lead the brief with the non-obvious points and compress the standard ones to a line each, credited. Fill the missing elements of the format or say why they cannot be filled. Correct the citations.

---

## Smaller points

- Section 1 lists "Standing" as scarce because "institutions admit few, slowly". Tax authorities and Companies House already admit software vendors through APIs. Standing is being granted to software, not rationed to firms.
- "Design for a window of roughly five to ten years" from 2027 ends between 2032 and 2037, so the routine tier may already be gone by 2035. Say which end the design assumes.
- R-LIB-ECONOMICS-16 records a check date of "8 Oct 2028". It is probably a typo for 2026 in the evidence file. It does not affect the draft but should be fixed at source.
- The section 4 parameters should include "who supplies the client's verifier", "can the state or a mandated platform provide it free?" and "can liability sit with a system's maker?", following objections 2, 4 and 3.
