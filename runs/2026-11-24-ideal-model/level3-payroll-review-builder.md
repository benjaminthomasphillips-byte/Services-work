# Review of the level-3 payroll redesign, from a builder

Written in character, 24 November 2026, as a founder of a global employer-of-record (EOR) and payroll platform. I am reviewing `level3-payroll.md`.

Labels:
- **[experience]** is my in-character operator judgement. It is a persona's view, not evidence, and should be tested.
- **[seen]** exists somewhere today, with source.
- **[reasoned]** follows from logic.
- **[conjecture]** is plausible towards 2035.

---

## My verdict in one paragraph

The paper is right that nobody wants a payroll run, and right that the EOR is a principal, not an agent. But it misdescribes how our money moves, treats EOR as lawful almost everywhere when much of Europe and Latin America regulates it as labour leasing, and still sells a better monthly payroll. Its control result is stated too kindly: the money assumption does not bend, it breaks.

---

## 1. The money is described wrongly

**Our EOR invoice is revenue, not client money** [experience]. The client pays us for a service whose price includes the salary. Once paid, it is our money, and we owe the wages ourselves. So the "trust per country" in section 6.3 is a choice we could make, not a legal default. It may also change the money's legal character and pull us into safeguarding rules. Licences bite elsewhere: on paying contractors for clients, and on wallets and cards that hold workers' balances [experience]. The paper never mentions contractors, though they are a large share of workers on platforms like ours.

**"Debit the client on payday morning" means we finance payroll** [reasoned]. A US client cannot pay a Polish employee in złoty on instant rails. Our Polish entity pays from a Polish account, so we must fund it first and collect later. Just-in-time for the client is credit from us. Say so, and price it as credit.

**The real balances are accruals, not two-week float** [experience]. Thirteenth-month pay, holiday pay and severance build up for months in many countries. Either we bill them monthly and hold them, or we carry the credit risk. That is where "no float income" truly bites.

**The float sum is overstated** [reasoned]. Under the paper's own design we hold nothing for own-entity clients. Only EOR flows, about 40% of $12.6bn, are held. Two weeks of that at 3% is about $6m, not $15m. In landscape D that lifts margin by roughly four or five points, not thirteen. The temptation is real but smaller, so the "commercial bet" in section 10.2 is cheaper than claimed.

## 2. EOR is labour leasing in much of the world

Germany is not the exception. In France, for-profit supply of labour is prohibited in principle, and EOR is lawful mainly through *portage salarial*, with criminal penalties for directors otherwise [seen, Addleshaw Goddard and Deloitte Avocats, 2026]. Mexico banned personnel subcontracting in 2021, allowing only registered specialised services [seen, Littler, EY, PwC]. Spain, Italy, Poland and the Netherlands run temp-agency regimes with licences, caps or equal-treatment rules [experience; not checked here]. The paper "owns" France in 2027 and Mexico by 2030 as EOR countries. That is unsafe as written [reasoned].

So the dial is not a feature. It is the lawful form of the business. And conversion is a transfer of employment, with consultation and continuity of service, not a record "carrying across" [experience].

## 3. Entities are harder than a fixed cost line

"Owned entity" often means a legal entity we own, with a local bureau running payroll and an accountant filing its returns [experience]. Banks de-risk accounts with large cross-border payroll flows. Many countries need statutory audits and transfer-pricing files. Rented directors carry personal liability for unpaid social contributions in some countries, including criminal liability in Germany [experience; not checked here]. They sign only if our money controls are visibly strong. That makes treasury a recruiting tool for directors, not just a desk.

## 4. Where it still automates today's payroll

- **Payday survives.** Continuous pay is computed, then released monthly. Bolder: the employee chooses cadence, currency and rail, within law [conjecture].
- **"A lawful start in 72 hours" is today, not 2035** [experience]. In established countries we already onboard in days. The real gates are visas, background checks and bank accounts.
- **The wage guarantee restates the law.** As legal employer we already owe wages until lawful termination [reasoned]. The gap employees actually face is **our** failure, not the client's.
- **The wedge is the incumbents' core.** Firms of 50 to 500 in several countries are exactly what Deel, Remote and Rippling sell to [experience]. HR systems are not a neutral channel; several now sell EOR themselves.

## 5. The bolder moves

1. **Make the worker a client.** *Portage salarial* already lets a worker bring their own employer [seen, sources above]. By 2035 a mobile professional could hold one lasting employment, with pension, benefits and seniority, across many clients. Clients buy work; the person owns the relationship [conjecture]. This turns G1's portable record into the product.
2. **Make location a pay event.** People will live in several countries a year. Tax residency, social-security cover and permanent-establishment exposure should follow each day's location, computed live. Mobility, not gross-to-net, is the hard and valuable problem [reasoned].
3. **Guarantee against our own failure.** An independent trustee for payroll balances, a named successor employer in every owned country, and published solvency [reasoned].
4. **Open the rule packs.** Licensing earns $6–12m and invites conflict. Co-maintain them with authorities. Our edge is accountability, not code [reasoned].

## 6. The architecture verdicts

| # | Paper | Mine | Why |
| --- | --- | --- | --- |
| **G2** | Bends | **Breaks** for EOR | The element means "sit beside the money". The fix reverses it. Rewording a reversal as a bend hides a break [reasoned] |
| **C3** | Bends | **Breaks as a conditional** | For an EOR, holding money is the business, every day. Home care set the precedent: C7 and C9 broke as conditionals for the same reason [reasoned] |
| **G7** | Holds | **Bends** | Duties are ranked. When a client wants someone gone tomorrow in a protected country, the employee's rights beat our paying client. That is daily work, and no earlier design had it [experience] |
| **G9** | Holds | **Bends** | G9 concerns the workforce that delivers the service. EOR staff are the client's workforce. "The workforce is the product" stretches the meaning [reasoned] |
| **C2** | Holds | **Bends** | Forty national schemas are not a neutral standard. Our data model becomes the de facto cross-border one [reasoned] |
| **C11** | Not switched on | **Switched on** | A good EOR is meant to end in conversion. Its trajectory is planned decline [reasoned] |

**My tally:** holds 18, bends 3, breaks 2. The paper says 21, 2, 0.

**Is the control result honest?** Not quite. The diagnosis, a missing "agent or principal" parameter, is right and useful [reasoned]. But "nearly clean" is the wrong headline. One author designed, scored and interpreted it, and the generous verdicts sit exactly where the firm owes duties against its paying client. Better: *the information core holds; the money and loyalty assumptions break where the firm is principal in law.*

---

**Sources checked:** Littler, EY and PwC alerts on Mexico's 2021 subcontracting reform; Addleshaw Goddard (September 2026) and Deloitte Société d'Avocats on EOR and *portage salarial* in France; Remote's published pricing pages ($599 to $699 per employee-month, varying by region), which support the paper's "around $600". Everything marked [experience] is unchecked.
