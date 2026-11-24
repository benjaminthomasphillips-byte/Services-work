# Review: the agent-first accountancy example, from a managing partner

Review written in character, 24 November 2026, of `example-accountancy.md`. Labels: **[seen]** exists today, mostly from running a practice; **[reasoned]** follows from logic; **[conjecture]** plausible towards 2035. Where I lean on my own practice rather than a source, I say "from practice".

## My verdict in one paragraph

The architecture is sound. The position registry, the independent recomputer and reach limits are the right ideas. Measuring human error before removing people is the best idea in the document. But the example treats production as the hard part. In my firm it is not. The hard part is getting true, complete facts out of owners on time, and getting them to approve and pay. The design automates the part we already find easy. It under-designs the part that causes most missed deadlines, write-offs and complaints.

## 1. Where agents cannot do what the example says

**"Books reconciled within two working days."** The bank side, yes [seen]. Feeds and rules already code most lines in Xero and QuickBooks. The other side is the client: the missing receipt, the £400 transfer to "Dave", the personal card used for fuel, the cash takings never banked. From practice, 10–20% of lines in a small company need the owner, and the owner answers in batches, late [seen]. No model makes an owner reply. The promise is really "current up to the last thing you told us". Say so, or the guarantee clause becomes the main source of disputes.

**Year-end judgement items.** The director's loan account is not a calculation. It is a reconstruction of what the owner meant by each personal payment, done after the event, often to fit the tax answer. Stock and work in progress in small firms are guesses. Agents can model the effects well. They cannot know the facts [reasoned]. I agree with the example's "kind 4", but it calls this "shrinking". I doubt it shrinks much by 2030. The limit is the client, not the model.

**One-tap approval.** It is legally fine. In practice, approval is where January goes wrong. The return is ready on 10 January. The client approves on 30 January and pays nothing [seen, from practice]. The design should treat approval and payment as the bottleneck case type, not as a formality.

## 2. Where it is too cautious

- **Payroll.** For a stable small employer, payroll software is already near-autonomous [seen]. Errors come from late or wrong inputs. Order 6 with dates of 2029–2031 is slow. I would remove human approval of standard runs in 2027–28. Keep the variance blocks.
- **Everyday questions.** Grounded agents can answer most of the 25,000 questions today: "can I claim my phone?", "when is my payment on account?" [reasoned]. The real limit is advice above a set effect, which the example already routes.
- **HMRC "nudge" letters and simple correspondence.** Most are formulaic: crypto, child benefit charge, rental income prompts. Agents can draft replies and gather evidence now. Only the sending and the phone call need the HMRC desk.
- **Remuneration planning.** Salary against dividend, pension contributions and the household's tax bands is arithmetic on known facts. It can run every year for every company, unprompted. Leaving it at "2031 / later" undersells the easiest advice win.
- **The penalty guarantee** is not new. Many firms already pay penalties caused by their own errors [seen, from practice]. It is not a differentiator. The live tax estimate is.

## 3. What it has missed

- **HMRC as a source of error.** Payments misallocated, codes wrong, post lost, repayments stuck, agent authorisations dropped [seen]. A third of my HMRC desk's time goes on HMRC's mistakes, not ours.
- **Authorisation friction.** Every tax for every client needs agent authorisation through HMRC's online services. Many clients never complete it [seen]. Onboarding 600 clients a year will stall here.
- **Fee collection and lock-up.** No case type for clients who do not pay. Collection is a big part of a partner's week.
- **Fraud and impersonation.** Changed bank details in a payroll email, fake HMRC calls, clients inventing invoices for a lender [seen]. If agents prepare payment files, this needs its own control.
- **Life events.** Death and probate, divorce, illness, emigration, a director falling out with a co-director. These are frequent at 5,000 households, and the firm suddenly has two clients who disagree [reasoned].
- **Employees as contacts.** Payroll staff ring the bureau about their payslips. The envelope bans contact with clients' staff. That needs a rule, not a ban.
- **Leavers.** Clients move to other firms. Handing over the ledger, the position registry and authorisations is a case type too.
- **Software vendors as counterparties and rivals.** Ledger platforms control the interfaces, set prices and are building their own agents [seen]. That is the landscape D threat, and it starts in 2027, not 2035.
- **The physical world is understated.** VAT inspection visits, the shoebox client, and owners who want the annual meeting in person [seen, from practice].
- **MTD timing.** Only income over £50,000 is in from April 2026. £30,000 follows in 2027 and £20,000 in 2028, and there are no penalties for late quarterly updates in 2026–27 [seen, gov.uk]. The 6,400 updates a year arrive in steps. Early shadow data will come from the cohort least likely to send records on time.

## 4. Roles and headcount

The 2027 figure of about 50 is tight. Eight shadow reviewers checking every filed tax output: about 6,000 VAT returns, 3,500 personal returns and 2,500 sets of accounts with tax. At realistic review times, that is over 10,000 hours, most of it in December to January and around common year ends [reasoned]. Eight people cannot do it in the peak. Either review samples from day one, or double the reviewers for the first winter.

The bigger gap is a missing layer. The 2,000 stable companies get no named person. From practice, they will still phone, and many will leave if nobody knows them [seen]. I would add a "client manager" role, about one per 250–300 households, as the human front line, paid for by the subscription. Add also a practice manager, credit control and IT. In 2035 landscape A, 20 people for a £8m firm leaves no slack for holidays, illness or one officer's suspension. I would not plan below about 30.

Apprentices: four is right in spirit. But professional training needs logged practical experience across real work [seen]. The firm must design that, likely as reviewers of the engine's work.

## 5. Economics

The baseline is plausible. My own weighting of the segments gives about £1,700 a client, not £1,900 [reasoned, from typical fees]. Margins of about 30% before partners' pay are realistic [seen]. Three gaps:

1. **How the firm gets 5,000 clients.** Realistically by buying practices, at around one times fees [seen, from practice]. Those books come with old habits, desktop software and retiring partners. The conversion cost and churn of 5–15% after a purchase are missing.
2. **Platform cost.** Somebody pays the ledger subscription for every client. That is £150–£500 a year each [seen]. It sits in neither the cost lines nor the prices.
3. **Guarantee cost.** Penalties are small. The real tail is negligent advice claims, which insurance covers and the example does not price.

The point that the agent firm wins on capacity, not margin, in landscape B is right and honest. I would lead with it.

## 6. What I would do if building this

1. Start with one segment: owner-managed companies plus the director's household, on one ledger platform.
2. Make the intake agent the core product: a chat channel the owner already uses, asking one question at a time, with a photo of the receipt. Score it on client reply time.
3. Treat approval and payment as a case type with its own chaser and its own metrics.
4. Run 2027 as measurement. Record human reviewer errors and catches. Take that data to the insurer and the tax bodies early.
5. Keep a named person for every client, but cheap: one per 250–300 households.
6. Build a fraud and authorisation control from day one.
7. Grow by acquisition, with a fixed migration playbook. Expect to lose clients.
8. Price the live tax estimate and the named person, not the filing [conjecture: this is what holds value in landscape D].

The design is closer to buildable than most I have seen. Fix the client side and it gets much closer.

Source checked: [GOV.UK, understanding Making Tax Digital for Income Tax](https://www.gov.uk/guidance/get-ready-for-mtd-an-agent-toolkit/understanding-making-tax-digital-for-income-tax); [GOV.UK, penalties for MTD for Income Tax](https://gov.uk/guidance/penalties-for-making-tax-digital-for-income-tax).
