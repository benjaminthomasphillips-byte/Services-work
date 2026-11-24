# Review of the level 3 accountancy redesign: a platform builder's view

Written in character by Claude, 24 November 2026, as the founder of a European shared accounting platform used by accounting firms and small businesses. Labels: **[seen]** exists today, with source; **[reasoned]** follows from logic; **[conjecture]** plausible towards 2035; **[experience]** what a builder in this role would say from practice. The persona is a role, so read [experience] as informed judgement, not testimony.

---

## My verdict

This is the best draft I have seen that starts from the gap between where facts are born and where they are used. "Close the gap and the work stops existing" is right. But the draft still pictures one firm reading other people's systems after the event. It closes the gap by watching faster. I would close it by being where the transaction is made. That changes the boundary choice, the distribution plan and the size of the prize.

## 1. The source is the transaction, not the bank feed

The draft says information is "born" in the bank account. It is not. By the time money moves, the meaning is gone. That is why the draft needs policies, one-tap questions and an anomaly agent. They are repairs for data that arrived without meaning [reasoned].

Meaning is born when the invoice, quote, payslip or rent demand is created. If the platform issues the invoice, the payment request and the receipt, each carries its VAT, category, counterparty and purpose from birth. The bank payment then only confirms it. Nothing needs classifying [reasoned].

Europe already works this way in places. Italy has cleared every B2B invoice through its central exchange since 2019 [seen, Agenzia delle Entrate]. France starts mandatory e-invoicing through approved platforms from September 2026 [seen, French tax authority]. The UK follows in April 2029 [seen, draft section 9]. In my experience the bank feed is the fallback for whatever escaped structure, not the backbone [experience].

**What I would build:** the invoicing, bill-pay and request-to-pay rails first, with the bank feed as the check. Aim for most of a Core client's transactions to be structured at birth by 2032 [conjecture].

## 2. "Do not build a ledger" is the wrong lesson

The draft rents ledgers and owns a "canonical financial state" above them. But that state is a ledger. It has entries, accounts, positions and an audit trail. Owning it while also syncing to several vendors' ledgers recreates the two-record problem the draft itself condemns [reasoned].

I have watched integration layers lose. Every vendor change breaks a sync. Every gap becomes a reconciliation. The vendor can switch off the interface when you start to compete [experience].

Ledgers are cheap to build in 2026. The hard part is not the ledger. It is the shared workspace where the owner and the accountant act on the same entries at the same time. That is what makes the platform hard to leave [experience]. So: own one ledger, open its data model, and let others read and write to it. Do not sit on top of three.

## 3. The unit of design is too small

The draft designs a 5,000-client firm and counts heads to one decimal place. A platform thinks in networks. Hundreds of thousands of businesses on one data model is where the real gains are [reasoned]:

- **Shared counterparty knowledge.** When one business codes a supplier, every business that pays that supplier inherits it. Most "policies" become network defaults the owner just confirms [reasoned].
- **Both sides of the trade.** When buyer and seller are on the same network, an invoice is one record seen twice. The VAT on each side agrees by construction [reasoned].
- **Priors for new clients.** A new bakery starts with the policies, cash cycle and tax profile of 4,000 bakeries. The partner's "best-spent hour" falls to ten minutes of confirming [conjecture].

The single firm is still useful. It should be the reference customer of the platform, not the whole design.

## 4. Distribution runs through accountants, not around them

The draft buys books, partners with banks and wins MTD cohorts directly. That is the slowest route. In practice, small businesses pick software their accountant tells them to use [experience]. The fastest channel is the 20,000-plus accountancy practices in the UK [seen, professional body membership data, approximate].

So I would give the platform to firms, free or cheap, and let them bring their clients. The draft's own firm runs on it, competes on the accountable layer, and the platform earns on every firm. Offering the layer to others is in the draft, but not until 2031 [seen, draft 9.5]. I would do it in 2027. Distribution compounds; late platforms do not catch up [reasoned].

## 5. Tax at source should move into the rails

"Pay as you trade" is good. But the draft has the firm computing and sweeping. By 2035, the bolder design splits VAT and provisional income tax at the moment of payment, as a rail feature. Several EU states use split payment for VAT already, including Italy and Poland [seen, EU VAT practice]. The EU's VAT in the Digital Age package moves the Union to real-time digital reporting [seen, Council adoption, 2025].

A platform with certified status can carry that split for every business on it [conjecture]. The firm then stops being a tax collector and becomes the party that certifies the split is right. That is where the draft's "accountability" margin should sit.

## 6. The verified record is the biggest product, and it is underplayed

The draft lists it fifth. I would put it first. A record that is complete, structured at birth and verified daily is worth more to lenders, insurers and the state than any filing [reasoned].

Two uses matter. **Credit:** underwriting from live, verified data, priced on facts instead of two-year-old accounts [conjecture]. **Trusted status with the tax authority:** the Netherlands has run "horizontal monitoring", a co-operative compliance scheme including for intermediaries, for years [seen, Dutch tax administration]. A UK version for platform-certified records would mean fewer enquiries and faster refunds [conjecture]. The draft's rule against commissions is right. Charge the lender a flat data fee, or let the client keep the saving.

## 7. Where the draft is still too cautious

- **Returns.** It keeps a one-tap confirmation of each return in 2035. With rails-level reporting, the return disappears. The owner confirms the year's position, not a form [conjecture].
- **Mandates.** It assumes owners resist money permissions. My experience is the reverse once the benefit is visible: owners hand over bill-pay quickly when the money stays in their own account [experience].
- **Agents.** It treats clients' agents as a 2031 interface. By the early 2030s, the counterparty on many transactions will be a machine. Build for agent-to-agent invoicing and settlement from the start [conjecture].

## 8. Where it is right, and I would not change it

The firm sits beside the owner's money, not between. Profit leaves filing. The household, not the company, is the client. Certainty priced from error data. The forced moments of MTD and e-invoicing as the wedge. All sound [reasoned].

---

## What I would build, in one paragraph

A shared ledger where owner, accountant and agents act on the same entries. Invoicing, payment and bill-pay rails, so data is born structured. A network that turns one business's knowledge into everyone's default. A certified record that lenders and the tax authority can rely on. A free platform for accounting firms, with my own firm as the reference customer selling the accountable layer. The 2027 wedge stays MTD. The 2035 prize is being the record the economy trusts [conjecture].
