# Counter-review: an actuary's view

**Reviewer:** Fellow of the Institute and Faculty of Actuaries. I priced professional indemnity and specialty liability at a Lloyd's syndicate and now advise on model risk and AI liability. I have not checked any figure in this review against a source in this pass. Where I give one, it is from memory and I say so.

---

## Where I start

Both papers come to the same idea: **run the fast, high-volume work as a data source, then use that data to price and carry the risk in the slow, high-margin layer** (step 1, P3; step 2, Q4). That is my industry's ground, so I will spend most of this review on it. In short, the direction is right, but the mechanism is described the wrong way round. The authors think the advantage is pricing risk from your own error data. In my experience, your own error data is the last thing a capacity provider will let you price from, and it is not where the margin sits.

## What they get right

Several things here are better than most AI-services decks I see.

- **Step 1, P1: conformance is not quality.** This is the most important sentence in either paper. In reserving we call it the difference between a model that reproduces last year's triangle and a model that is right. A suite of past cases tells you the new process agrees with the old one. It tells you nothing about the claims that have not been reported yet.
- **Step 1, P7: "no enquiry" is weak evidence.** That is exactly right. An absence of claims is not proof of no loss. It is incurred-but-not-reported (IBNR) business until the tail has run off.
- **Step 1, §6, point 5: the decade's scandal will be a correlated error.** I agree, and I would put it more strongly. It is the risk that decides whether the guarantee business can exist at all (see below).
- **Step 2, Q4: risk-bearing alone earns roughly the cost of capital, and the margin is in the bundle.** Broadly right. Title insurance is a fair example: from memory, its loss ratios are in single figures, and the money is in search and distribution.
- **Step 2, Q9: risk margin is valued nearer book value.** Correct. An investor should take this seriously, because it cuts against the step 1 instinct to warrant everything.

## Where it does not survive contact with my market

**1. "Guarantees priced from the firm's own error data" (step 1, P3; step 2, Q4).**

The paper assumes the operator's data gives it a pricing edge. Credibility theory says otherwise, for three reasons.

- **The losses that matter are rare and severe, and they report late.** A tax-accuracy guarantee or a building-compliance warranty is long-tail liability. Claims emerge over three to seven years, sometimes longer. A firm that starts in 2027 will not have a developed loss triangle for its first underwriting years until the early 2030s. Until then, its "error data" measures frequency of detected slips, not severity of real loss. In PI the two are very weakly related: a handful of large claims drives the result.
- **It is your own data about your own work.** Every underwriter I worked with discounts a submission built on the insured's own loss data and its own models. That is not snobbery. The party that controls the work also controls what gets recorded as an error. The paper's own P6 (the improver must not grade itself) applies with full force at the firm level. Lloyd's capacity providers will want independent audit, peer benchmarks and a long record before they credit any of it.
- **Small volume gives little credibility.** Even a large AI-native firm will have thin experience per case type for years. It will be blended with market data, and the market data sits with HMRC, the PI insurers and the brokers. The authors say this in P7 ("tax authorities, insurers and software vendors see the same outcomes across far larger populations"), but they do not follow it through to P3.

What would change: treat own-data pricing as a 2032-onward option, and price the guarantee from market data plus independent assurance until then.

**2. "Only the operator can drive the error rate down, so only it can price the risk below a pure insurer" (step 2, Q4).**

This confuses expected loss with price. For a correlated book, the premium is set mostly by the **capital charge for the tail** and by reinsurance cost, not by mean frequency. An engine that lowers the average error rate while putting thousands of clients on one playbook can *raise* the capital you need, because one bad release becomes a single event across the whole book. In Lloyd's terms it is an aggregation, or "clash", exposure. The paper's correlated-error point and its guarantee strategy are in tension, and the paper does not join them up.

The precedent I would put in front of an investor is the US monoline bond insurers. From memory, they guaranteed correlated credit risk, were priced on benign recent experience, and most were broken in 2007–08. A guarantee business built on one engine is a monoline.

What would change: put accumulation management at the centre of the design, not in the hygiene list. That means caps on clients per playbook version, named event definitions, and an event excess-of-loss reinsurance programme from day one.

**3. "Take on the enquiry if one comes" is presented as new.**

It is not. Tax investigation (fee protection) insurance has been sold by UK accountancy practices for at least two decades. The practice usually acts as an introducer or appointed representative, and the cover is underwritten by a specialist insurer. My understanding is that it is a commission line for the practice and a low-loss-ratio product for the insurer. So the slow, high-margin layer the paper wants to build is already an existing, distribution-led insurance product. The margin in it went to whoever owned the client relationship, not to whoever carried the risk. That supports Q4's conclusion, but it undermines the idea that a warranty is a new source of advantage.

**4. Regulation is treated as a counter-argument. It is the gating item.**

Step 1 lists "regulators may not let a services firm warrant outcomes" as a counter-argument. In the UK it is close to settled law. A promise to pay money, or to provide a benefit, on an uncertain event in return for consideration is very likely an insurance contract. Carrying it on without authorisation is a criminal offence under the Financial Services and Markets Act. Insurance distribution rules, the Consumer Duty and the FCA's fair-value work then apply to anything sold to consumers or small firms. From memory, the FCA has been pressing hard on poor-value add-on products such as GAP insurance.

A service guarantee therefore has three realistic routes:

- **A pure performance warranty with no money benefit.** We fix it free. This is not insurance, and it is limited.
- **An insurance product the firm distributes.** This needs FCA authorisation or appointed-representative status.
- **A captive or protected cell** that holds the risk behind a fronting insurer. This takes capital, a regulator and years.

None of these is a design detail. Each one decides what the firm is.

**5. The paper misses the cheapest route to the bundle: be the MGA, not the balance sheet.**

The structure my market already uses is the managing general agent, or Lloyd's coverholder. It owns the data, the underwriting and the claims control. It earns commission and profit share. It borrows capacity from syndicates or insurers, who hold the capital. The MGA is valued nearer to software and distribution. The capital provider is valued near book. That is exactly the split Q9 wants, and it already exists. The historical example of "risk bundled with control of the work" is Hartford Steam Boiler. From memory, it inspected and insured boilers from the 1860s, and its edge was the inspection, not the balance sheet. Note one point, though: it inspected *other people's* boilers. An inspector independent of the operator is what made the bundle credible to buyers.

**6. The insurance market is moving against AI-produced work, not towards it.**

The papers assume someone will cover the firm. My reading of the market in 2025–26, which I have not checked here, is that PI and general-liability carriers are moving to exclude or sub-limit AI-related loss. This follows the "silent cyber" playbook the PRA and Lloyd's forced through after about 2017. If that continues, an AI-native firm will struggle to buy its *own* PI on standard terms, before it even thinks about selling guarantees.

Specialist AI-performance cover does exist. From memory, Munich Re has written AI performance guarantees for several years, and newer MGAs have launched AI-warranty products with Lloyd's capacity. It is priced on independent model testing. The papers do not cover the firm's own insurability at all. For an investor, that is a first-year cost and a possible block on growth.

**7. "The licensed signatory signs for the system, and regulators have not yet accepted it" (step 1, P6).**

They have, in my profession, for decades. The Lloyd's Statement of Actuarial Opinion, the actuarial function holder under Solvency II, and the with-profits actuary all sign for models, assumptions and processes, not individual outputs. These roles are governed by professional standards such as the FRC's technical actuarial standards. The PRA's model risk principles for banks (SS1/23, effective 2024 from memory) set out inventory, independent validation, tiering and senior-manager accountability. That is very close to the paper's "people govern the evaluator". The authors should borrow this ready-made governance rather than invent it. It would also make the firm legible to insurers and regulators straight away.

## What they miss entirely

- **The firm's own insurability** (point 6).
- **Reserving.** Any warranty business has to hold reserves for claims not yet reported. Those reserves need an actuarial opinion and will tie up capital before profit appears. Running a services firm with a growing guarantee book is running a small insurer, and its cash profile is very different.
- **Adverse selection.** If the firm offers guarantees, the clients who buy them will be the ones who know their affairs are messiest. Self-improving or not, the engine cannot see what the client hides.
- **Moral hazard on the client side.** A guaranteed client takes less care with inputs. The paper says incomplete client inputs are the main cause of failure (step 1, §5). A guarantee makes that worse unless the contract makes the client warrant their inputs.

## My own industry in 2035

I am guessing here. Routine actuarial production will largely be automated: data cleansing, reserving runs, pricing refreshes and regulatory reporting. That fits the paper's "routine execution" tier, and it is already well under way with software vendors. The value will sit in three places:

- **Statutory sign-off roles,** which regulation protects. These fit "residual judgement" and are protected by liability, as the paper says.
- **Independent model validation and AI assurance.** I expect this to become a large, regulated function across insurance, banking and anyone warranting AI-produced work.
- **Underwriting AI risk itself.**

The framework would predict the first two correctly. It would miss the third, because it assumes the operator carries the risk. I expect the operator to be a customer of the risk market, and the independent assurer to be the gatekeeper. That is the paper's own Q3, transplanted into insurance.

## What I would back

1. **An independent AI-assurance and rating firm** for AI-produced professional work. It would test, monitor and certify operators, and sell the results to insurers, regulators and clients' agents. This is Q3's "trusted checker". It is separate from any operator, for exactly the conflict reason the paper gives.
2. **An MGA or coverholder** that writes PI and performance cover for AI-native services firms. Its capacity would come from Lloyd's. Its underwriting edge would come from live telemetry agreed as a condition of cover, including holdout performance, change logs and exception rates, which are the very diligence tests in step 1, §6. The operator's data becomes valuable as a condition of cover verified by someone else, not as the operator's private pricing basis.
3. **If the investor insists on an operator,** it should distribute insurance from day one (appointed-representative status, then authorisation) and leave the capital to others. A captive for its own PI comes later, once it has five years of developed experience.

## What would change my mind

I would change my view if a capacity provider credited a firm's own error data in the price of a long-tail guarantee within its first three years, without independent audit. I have not seen that happen. I would be glad to be shown it.
