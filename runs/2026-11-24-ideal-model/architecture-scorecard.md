# Architecture scorecard: E1 to E8 across five redesigned services

Claude, 24 November 2026. One author, no sub-agents. It reads the five level 3 redesigns (`level3-accountancy.md`, `level3-lettings.md`, `level3-legal.md`, `level3-claims.md`, `level3-probate.md`). Legal, claims and probate scored themselves; their verdicts are kept. Accountancy and lettings are scored here from their designs. Labels: **[seen]** exists somewhere today, with source; **[reasoned]** follows from logic; **[conjecture]** plausible towards 2035. Points carried from a redesign keep that paper's label.

A caution [reasoned]. Accountancy and lettings produced E1 to E8, so they score well against them. The same author scored the other three, and every verdict moved towards BENDS after review. Treat HOLDS as provisional.

---

## 1. The scorecard

| | Accountancy | Lettings | Legal | Claims | Probate |
| --- | --- | --- | --- | --- | --- |
| **E1 Trusted live record** | **HOLDS.** Owned ledger per household | **HOLDS.** Home record, landlord-owned, open schema | **BENDS.** Half of each contract is the other side's; record holds positions, written for a hostile reader | **BENDS.** Record of the insured risk, shared by opposed parties, graded by provenance | **BENDS.** Holds destinations and liabilities; must outlive its subject and owner |
| **E2 In the money flows** | **HOLDS.** Mandate "beside, not between"; tax paid forward | **HOLDS.** Wallet per home, regulated partner | **BENDS.** Holds no money; sits in the commitment flow instead | **BENDS.** Pays from the insurer's fund, but owned crews make it a payee | **BENDS.** Routes and reserves money; holds it only for attorneys |
| **E3 Standing policies** | **HOLDS.** One-page policy pre-filled from network priors | **HOLDS.** Extends existing spend limits | **BENDS.** Policies must be made, and are overridden; overrides named | **BENDS.** Holds for paying, not for reductions; those need a person | **BENDS.** A will is a policy whose author cannot be asked; test it in life |
| **E4 Conditions, not tasks** | **HOLDS.** "Tax already gone", "safe to spend", checked daily | **HOLDS.** Legal, safe, dry, paid, ready now | **BENDS.** Conditions plus episodic moments | **HOLDS** for instrumented risks, once the product is risk care | **HOLDS.** "Estate routed" in life delivers most of the outcome at death |
| **E5 Priced and guaranteed from pooled data** | **HOLDS.** Certainty priced from estimate-error data, capped; taxpayer stays liable | **HOLDS, at a cost.** Home-by-home underwriting; insurer on the tail from day one; "is it insurance?" unresolved | **BENDS.** Guarantee only own turnaround, price, completeness; no pooled term data | **BENDS.** Pricing on indemnity rewards underpaying; guarantee restoration date, not loss ratio | **BENDS.** Process risk insurable, family risk not |
| **E6 Platform or open standard** | **HOLDS.** Separate platform company | **HOLDS.** Open record standard; flows owned | **BENDS.** Neutral standard body; large buyers run rival envelopes | **BENDS.** Give the protocol to a trade body; be its best user | **BENDS.** Standard needs state push; a dependency, not an asset or hedge |
| **E7 People at the edges** | **HOLDS.** Judgement desk, partners, embedded leads | **BENDS.** Physical edge becomes the core: employed technicians, own turn crew | **HOLDS.** Adds an adversarial edge | **BENDS.** Physical, adversarial and crisis edges are the largest groups | **BENDS.** People at the centre of the experience in crisis |
| **E8 Capability where work happens** | **HOLDS.** Platform for sole traders; embedded leads above | **HOLDS.** In the home, money, tenant's phone, institutions' systems | **BENDS.** Ramp by segment; GC-led clients get a licence, not agents | **BENDS.** Sits in three worlds; the client sits inside the firm through live oversight | **BENDS.** Embed where people are well (employers, banks), not at the deathbed |

**Totals.** Holds 18, bends 22, breaks 0. Accountancy 8 holds. Lettings 7 holds, 1 bends. Legal 1 holds, 7 bend. Claims 1 holds, 7 bend. Probate 1 holds, 7 bend.

Nothing breaks, but in the three new services every element survives only when restated [reasoned]. The bends share causes: opposed parties, contestable inputs, episodic moments, authority that changes hands, and a firm that could profit from its own judgement. Early signs sit in the source designs: accountancy refused to hold money; lettings turned E5 into carrying risk, served a non-paying party (tenants) and faced a conflict (the exit route).

---

## 2. Each element: general, conditional or specific

**E1. General, once restated** [reasoned]. Every service centres on a live record; ownership varies. One aligned owner and a single chokepoint (a ledger): the firm can own it. Many parties relying on it: open, shared, graded by provenance. Disputes possible: written for a hostile reader.
*Restated:* **A shared, live record of the thing, with provenance for every entry, owned by whoever owns the thing, readable by every party with a right to it, written for its most hostile reader, and able to outlive the relationship.**

**E2. General, once restated; holding money is conditional** [reasoned]. The logic is "be where the client's acts take effect": money, commitments in law, destinations in probate. Holding funds needs one aligned principal, a regulated partner and a firm that is not a payee.
*Restated:* **The firm acts in the flow where the client's acts take effect (money, commitments, work, destinations), under a revocable mandate, and never as an unchecked payee.**

**E3. General in form; its source is conditional** [reasoned]. It assumes a policy-holder who can state a policy and be asked again. Founders cannot write one unaided (legal); the dead cannot be asked (probate); reductions hit a party who never set it (claims).
*Restated:* **The firm makes, tests and maintains the client's policy, and acts within it. Overrides are allowed and named. Decisions that harm a party who did not set the policy need a person.**

**E4. General, once restated** [reasoned]. Probate and claims show the strongest form: a condition kept true before the event shrinks the event.
*Restated:* **Sell conditions kept true, and moments made fast; design each condition to shorten its moment.** How much is condition and how much is moment depends on whether the service is continuous or episodic.

**E5. Conditional** [reasoned]. Beyond what the firm controls, a guarantee is insurance and needs capital (lettings, claims, probate). Pooling must be lawful and untraceable; law dropped it. Claims showed a priced outcome can reward harm (underpaying).
*Restated:* **Price and guarantee what the firm controls. Route outcome risk beyond that to a capital partner, priced from the firm's evidence. Check that the revenue unit rises only when the client's outcome improves.**

**E6. General that a standard exists; its owner is conditional** [reasoned]. A ledger has one owner, so accountancy can run a platform company. Bilateral or many-party records need a neutral owner, and then the standard is no hedge against price collapse.
*Restated:* **A shared standard on which the firm is the best user. Owned as a company only where the record has one owner and the network needs a scale the firm cannot reach alone. Otherwise given to, or lobbied for from, a neutral body.**

**E7. General; its shape is a parameter** [reasoned]. Accountancy's edges are judgement and relationship. Lettings and claims add a large physical edge, law an adversarial one, probate a crisis edge.
*Restated:* **Agents produce. People stand where judgement, accountability, physical work, opposition and crisis meet the service. The size of each edge is set by the service, and in crisis people are at the centre of the experience.**

**E8. General in principle; the location is specific** [reasoned]. It fails as worded when the client's world is frozen (probate), owned by a general counsel (legal) or split three ways (claims).
*Restated:* **Capability sits where information is born and decisions are taken, which may be the client's systems, the thing itself, the counterparty's systems, or a third party where the client is calm. Where a regulator holds the client responsible, the client also sits inside the firm through live oversight.**

---

## 3. What the three new services needed that the architecture lacked

| Candidate element | Legal | Claims | Probate | Recurs? |
| --- | --- | --- | --- | --- |
| **Duties to non-paying and opposed parties** (neutrality) | Design for the counterparty; one side only | Neutrality layer; fairness to the policyholder | Neutrality inside one family | **All three, plus lettings' tenants. General** |
| **Controls on the firm itself** (self-dealing, conflicts, inverted incentives) | Spend management that could steer work to itself | Self-dealing; inverted incentive check | No executor capture; house option disclosed | **All five, counting lettings' exit route. General** |
| **Evidence rules**: provenance in, limits on use out | Record as a liability; privilege | Provenance; baseline-use rule | Capacity and coercion evidence | **All three. General where disputes are possible** |
| **A capital boundary** for promises | Dispute funding and insurance | Balance sheet; protected cell | Insurer-backed executor indemnity | **Four of five, with lettings. General wherever outcomes are guaranteed** |
| **Episodic moments and surge capacity** | Moments; deal leads within a day | Physical surge in storms | Death as the moment | **All three. Conditional on episodic demand** |
| **A mandate chain with portable proof of authority** | Who may commit; overrides; investor consents | Delegated authority from capacity providers | Person to attorney to executor; the grant | **Strong in probate, partial in the others. Conditional** |
| **Time beyond the firm**: custody and long tail | Retention limits | Liability claims run for years | Wills kept for decades | **Two of three. Conditional on promise horizon** |
| **Policy-making as work** | Central | Coverage as code | Will tested in life | **Recurs; folded into E3** |
| **Licensing the definition of good** | For GC-led clients | Coverage-as-code sold alone | Not present | **Partial. Conditional on client's own team** |
| **Pace set by the client** | Not present | Not present | Central | **Specific so far; likely in care** |

The pattern [reasoned]. As claims put it, E1 to E8 describe **a firm serving one principal in a cooperative world**. The additions deal with the opposite: many parties, some opposed or lying, authority that moves, and a firm that could profit from what it judges.

---

## 4. The parameters that predict the form

| Parameter | Range across the five | How it changes the design [reasoned] |
| --- | --- | --- |
| **Number and alignment of principals** | One aligned owner (accountancy) to many opposed parties (claims, probate) | One aligned owner: owned record, firm can hold money, platform company possible. Many or opposed: shared record, neutrality layer, standard given to a neutral body |
| **Continuous or episodic** | Daily cash (accountancy) to once in a lifetime (probate) | Continuous: sell conditions. Episodic: sell readiness plus moments, plan surge capacity, acquire clients through others because there is no repeat purchase |
| **Who pays versus who benefits** | Same (accountancy) to split (claims; probate membership free to the person; lettings' tenants) | Split: duties to the beneficiary in the constitution, incentive check on the revenue unit, fairness evidence shown to the party who does not pay |
| **Who controls the outcome** | The firm (tax estimate) to a court, counterparty or family | Firm controls: guarantee it. Others control: guarantee the firm's half only; capital partner for the rest |
| **Client size and in-house capability** | Sole trader to GC-led scale-up or insurer | Small: the firm is the function and holds the record. Large: portable layer in their systems, or a licensed definition of good |
| **Physical intensity and density** | Near nil (legal) to large (lettings, claims) | High: owned field force, density economics, physical edge becomes the core |
| **Honesty of inputs and dispute likelihood** | Honest and calm (accountancy) to fraud and litigation (claims, legal) | Provenance, fraud separated from settlement, record for a hostile reader, evidence-use limits, privilege |
| **Chokepoint structure** | One ledger to commitments spread across many systems | Single: own it. Dispersed: portable layer plus a standard |
| **Horizon of the promise** | Weeks (VAT) to decades (wills, liability) | Long: custody beyond the firm, run-off, slow feedback, capital |
| **Stability of authority and client's state** | Fixed owner, calm, to grief and lost capacity (probate) | Mandate chain, portable proof, a person at the front, pace as policy, safeguarding monitors |
| **Rules on the flow** | Payment rules, client money, privilege | Strict: route and reserve rather than hold; rent regulated rails |

Two parameters predict most bends [reasoned]: **alignment of principals** and **continuous versus episodic**. Accountancy is aligned and continuous and holds everywhere; legal and claims are opposed; probate is episodic with moving authority. Volume sets headcount and platform economics, not the shape.

---

## 5. A restated general architecture

**Core: in every service** [reasoned]. Wording as restated in section 2.
1. **G1 The shared record** (E1).
2. **G2 Acting in the flow, never as an unchecked payee** (E2).
3. **G3 Policy as work** (E3).
4. **G4 Conditions and moments** (E4).
5. **G5 People at the edges, sized by the service** (E7).
6. **G6 Capability where information is born, oversight both ways** (E8).
7. **G7 Duties to every party, and controls on the firm** (new): neutrality to non-paying and opposed parties; no self-dealing; a revenue unit that rises only with the client's outcome.
8. **G8 Evidence rules** (new): provenance in; limits on using evidence against the person who produced it.

**Conditional: with the parameter that switches them on**
- **C1 Priced and guaranteed outcomes** (E5): capital partner *when outcomes depend on others.*
- **C2 The standard** (E6): a platform company *when the record has one owner*; a neutral body *when it has many*.
- **C3 Holding money:** *when one aligned principal, a regulated partner and no payee conflict.* Otherwise route and reserve.
- **C4 Pooled data:** *when lawful and untraceable.*
- **C5 Mandate chain with portable proof of authority:** *when authority changes hands or counterparties need proof before acting.*
- **C6 Custody beyond the firm:** *when the promise outlives the firm's likely life.*
- **C7 Surge capacity:** *when demand is correlated and physically constrained.*
- **C8 Licensed definition of good:** *when the client has its own team and AI.*
- **C9 Pace set by the client:** *when the client is in crisis.*

The first architecture was a firm serving one principal in a cooperative world. The restated one is **a firm that keeps a shared record true, acts where its client's acts take effect, and is built to be trusted by the parties it does not serve** [reasoned].

---

## 6. What remains untested, and the next test

**Untested** [reasoned]:
- **The state as payer.** No design has a public payer setting price.
- **A person as the "thing".** No record yet describes a body and a daily life.
- **People at the centre, every day.** Probate puts them there only in crisis.
- **Forced custody of money across jurisdictions.** All five avoided holding money; none was forced to, and each faced one legal system.
- **Agent-to-agent markets**, assumed by every paper for the 2030s [conjecture], and **the economics**, all conjecture.

**Best next test: home care** [reasoned]. It switches on almost every new and conditional element at once:
- The payer is often a council, the beneficiary a frail person, the family a third party with views [seen, general knowledge, not checked]. That tests G7 hard.
- The record describes a person's daily life: G1 and G8 meet dignity, privacy and safeguarding.
- The physical edge is the product and labour the constraint. G5 may break: people may be the centre, not the edge.
- Authority moves to an attorney as capacity fails (C5). "Safe and well now" is a natural condition (G4), but health declines. Pace and dignity may beat speed (C9).

If the architecture survives home care, it is general. If G5 breaks there, the architecture is a design for **information services with physical edges**, not for care [reasoned].

**Second test: cross-border payroll** [reasoned], as the control case. It is continuous, single-principal and cooperative, so the core should hold. But it forces custody of large sums (C3), many regulators (C2) and guarantees against penalties (C1). If it bends where accountancy held, section 5's conditions are wrongly stated. **Statutory audit** would be the purest test of G7: the payer is the audited company, the beneficiaries are shareholders and the public [reasoned; claims 9.2 predicts this].
