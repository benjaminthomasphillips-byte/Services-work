# Review of the level-3 claims redesign, from a builder

Written in character, 24 November 2026, as a founder of an AI-native claims operator. I am reviewing `level3-claims.md`.

Labels:
- **[experience]** is my in-character practitioner judgement. It is a persona's view, not evidence, and should be tested.
- **[seen]** exists somewhere today, with source.
- **[reasoned]** follows from logic.
- **[conjecture]** is plausible towards 2035.

---

## My verdict in one paragraph

The paper gets the core insight right: close the information gap before the loss, not after. But it still treats the claim as the product. In 2035 the product is a home or car that rarely gets damaged and is put right within days when it does. The paper reaches for that, then retreats into a better claims handler. It is also too hopeful about how clients are won, and two of its architecture verdicts are too generous.

---

## 1. It still sells claims handling. Sell an undamaged home.

The paper cuts indemnity by 3% to 5% through faster mitigation, less fraud and more recoveries. Every one of those levers acts after the loss. The biggest lever acts before it: fewer losses. If the firm already runs the leak sensors, the baseline and the first-hour crews, it is a short step to running prevention as well: fixing the failing valve the sensor flagged, not just drying the floor afterwards [reasoned].

So the bolder move is this. **The firm is paid to keep the insured risk intact, and handles claims as the failure case.** Price it per policy-year, as the paper says, but add a fee tied to lower claim frequency, measured against a matched control book. Then E4 stops bending (see section 6). The ongoing promise is "this home is protected and watched", not "no loss waits on us" [reasoned]. How much frequency falls is unknown. Vendor figures exist, but the paper found no independent ones [seen, per the paper]. I would bet frequency falls more than severity does for escape of water [conjecture].

## 2. Indemnity in kind should be the default, not an option

"Fixed-price restoration" is framed as a cheaper way to settle. Take it further. By 2035 a policy should promise restoration to a dated standard, with cash only if the policyholder asks for it. Then the claim no longer has a "quantum" to argue over. There is a job, a date and a quality check signed off by the policyholder [reasoned]. Most of the judgement desk's disputed-quantum work goes with it. The paper still counts 22 to 38 people on that desk in 2035. I think that is too high under landscape A if in-kind restoration is the default [conjecture].

## 3. It is too cautious about cover at the point of sale

Coverage as code is the right idea, but it is used only to spot ambiguity for underwriters. The bolder use is to show the policyholder, at bind, in plain words, what each likely loss would and would not pay. Declines then become predictable rather than surprising [reasoned]. Home claims acceptance of 62% to 71% [seen, per the paper, as reported] reflects surprise as much as fraud. Fix surprise at sale and the decline rate, which the paper rightly says sets the size of the desk, falls. That is a wording-design product the firm can sell to insurers on its own.

Add parametric first-response cash too. When a sensor or flood gauge confirms the event, a fixed sum lands within the hour for emergency costs, before any assessment [conjecture]. That would also cut the credit hire and claims management firms out of the first contact, which the paper wants.

## 4. Winning clients: the wedge is right; the buyer is wrong

MGAs as the first wedge is sound. But in my experience the MGA does not choose its claims administrator on its own. The capacity provider or the Lloyd's syndicate behind it approves, audits and often names the administrator [experience]. So the real first buyer is the **capacity provider and reinsurer**. They want clean, live data and controlled claims across many MGAs. Sell to them once, and get placed into many MGAs [reasoned].

Catastrophe surge as a second wedge is weaker than the paper thinks. Surge is bought from panels by headcount and availability, and it is priced as a commodity. A firm with 60 field technicians loses that contest to the global adjusters [experience]. Better: sell pre-event readiness to reinsurers, meaning a credible event estimate within days. That uses data, not bodies [reasoned].

The 2027 target of about 30,000 claims from two or three MGAs is optimistic. Onboarding, delegated-authority audits and system set-up take six to twelve months each [experience]. I would plan on 8,000 to 15,000 claims [conjecture].

## 5. Scaling is limited by trades, so own them

The paper names restoration capacity as a constraint, then counts only network managers. Speed promises die when the drying firm has no van free. The firm should own regional drying and make-safe crews, buying small firms rather than building them [reasoned]. That changes the economics. Owned crews carry people and vehicles, so the 44% margin under landscape A is too generous. Something like 20% to 28% on a larger revenue base is more believable [conjecture]. The paper's "4% restoration margin" is also too thin for owned capacity and too fat for a pure broker.

## 6. The architecture verdicts

- **E1 BREAKS is too harsh. I would say BENDS.** The paper itself builds a trusted, live, append-only evidence record. It is multi-party, not owned by the client. The element survives if "the client's thing" becomes "the insured risk", recorded under neutral rules [reasoned].
- **E2 HOLDS is too generous. It BENDS.** The paper misses a conflict. If the firm decides the scope of a repair and earns a margin on that repair, it pays itself. The fairness firewall separates settlement from leakage share. It does not separate scope from restoration margin. Fix: scope is set by the engine and the policyholder sees it; restoration margin is paid on the job, not on its size; an independent sample re-scopes completed jobs [reasoned].
- **E3 HOLDS.** Agreed.
- **E4 BENDS is too harsh if the firm runs prevention.** Then the condition is continuous: the risk is watched and protected. HOLDS under my redesign, BENDS under the paper's [reasoned].
- **E5 BENDS.** Agreed, and the capital boundary is the right catch. But the paper stops short. A firm with this data should own a protected cell or partner a reinsurer from 2030 to price restoration guarantees. Otherwise the reinsurer captures the value of its data [conjecture].
- **E6 HOLDS is too generous. It BENDS.** UK shared utilities were mostly formed through trade bodies or under regulatory pressure, not founded by one outsourcer [reasoned, from the paper's own list]. A startup-founded exchange with a capped stake gives the firm little and needs allies it does not have. Treat the exchange as a cause to join, perhaps through a trade body, not a product to found [reasoned].
- **E7 BENDS.** Agreed. But the elastic reserve should be owned crews plus accredited contractors, not just retained adjusters.
- **E8 BENDS.** Agreed.

## 7. What I would keep exactly as written

Asymmetric authority, fraud separation, provenance against AI-made evidence, and the lesson that E1 to E8 assume one principal in a cooperative world [reasoned].

## 8. One thing I would add to the stress test

The policyholder's own agent will shop the claim. By 2035 it may compare offers, threaten the Ombudsman and file a complaint in seconds [conjecture]. The firm's defence is speed and transparency. If the record is open and restoration starts in an hour, the agent has nothing to argue about. Design for that agent as the most demanding user, not as a channel.
