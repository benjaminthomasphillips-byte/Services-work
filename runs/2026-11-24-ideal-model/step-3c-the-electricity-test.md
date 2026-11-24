# Step 3c. The electricity test: redesigning services from scratch rather than automating today's work

Draft by Claude, 24 November 2026, after Ben's challenge that the worked examples were still too narrow. It uses two sources Ben pointed to: Pennylane's model in French accountancy, and a 23 November 2026 report on Dwelly's agents. Both were read for this step, and the figures in them are the companies' own unless stated otherwise.

Labels:
- **[seen]** exists today;
- **[reasoned]** follows from logic;
- **[conjecture]** a plausible extension towards 2035.

## 1. What went wrong in the worked examples

Both examples began from today's inventory of work: 87 lines in an accountancy practice and 123 in a lettings firm. They then asked which of those lines agents could do. That is the factory owner putting an electric motor where the steam engine stood and keeping the shafts and belts. The work got cheaper, but its shape stayed the same.

The proof that it was too narrow came from Dwelly, as reported on 23 November 2026 [seen; company figures, not independently checked]:
- **Size today:** 300 staff run 20 agencies and more than 17,000 properties. That is about 88 people per 5,000 homes, close to the 81 the agent-first lettings example estimated for 2027.
- **How much is automated:** agents already complete about 55% of the steps in letting a home without a person, with a target of 85% by early 2027.
- **Manual work:** touches per letting fell from 28 to 13, with a target of five.
- **Capacity:** a negotiator who handled 350 properties now handles about 700, with a target above 1,000.

So the "agent-first" example was roughly where an AI roll-up already is in 2026. Dwelly is doing it by automating the existing lettings process, step by step, very fast. That is valuable, but it is still the motor in the old factory.

## 2. What electricity actually teaches

Factories first replaced their central steam engine with a central electric motor, still driving every machine through shafts and belts. Productivity barely moved. The gains came decades later, when factories were rebuilt around a motor at each machine ("unit drive"). Plants became single-storey, laid out by the flow of work rather than around the drive shaft, and whole jobs, such as maintaining the belting, disappeared (general knowledge; Paul David's work on the dynamo is the classic account).

Translated to services, there are three levels of change:

| Level | What changes | Services example |
| --- | --- | --- |
| **1. Swap the power source** | The same tasks, done by agents | Dwelly: the same lettings steps, 55% done by agents [seen] |
| **2. Redesign the process** | Tasks disappear because information is created where and when it is needed | Pennylane: the transaction is the unit of work, and bookkeeping becomes a side effect of running the business [seen] |
| **3. Redesign the service and the firm's boundary** | The firm's capability lives where the client's work happens. The service becomes a continuous condition. The firm is a layer inside the client's world, not an office the client sends things to | Partly seen in shared systems. Mostly [conjecture] |

The electricity equivalent of a motor at every machine is intelligence at the point of work: in the client's bank and invoices, in the building, in the tenant's phone, in the counterparty's interface. It is not intelligence in a central office that processes what clients send in.

## 3. How to design from scratch

A procedure, in order [reasoned]:

1. **Start from the client's outcome and the client's world, not the firm's tasks.** What does the client want to be true, continuously?
2. **Find where the information is born and where decisions are taken.** Put the firm's capability there.
3. **Delete the tasks that exist only because information was in the wrong place, at the wrong time or in the wrong form.** Collecting, re-keying, chasing, reconciling and preparing for a deadline are often consequences of distance, not of the work itself.
4. **Delete the waits that exist because of how authority and money are arranged.** Replace approvals with standing policies, and replace chasing with contract terms, floats and defaults.
5. **Then put people where the outcome genuinely needs a person** (step 3b's kinds of need).
6. **Then decide the firm's boundary:** what lives in the client's systems, what in the firm, what with counterparties, and who owns the platform underneath.

The worked examples did step 5 and part of step 4. They skipped 1 to 3, and 6.

---

## 4. Accountancy, redesigned from scratch

### The outcome
The owner of a small business wants to:
- always know where they stand;
- never be surprised by tax or cash;
- pay the right tax without effort;
- make good decisions at the moments that matter;
- spend no time on bookkeeping.

### Where information is born
In the business's own money flows: bank payments, card spend, invoices issued and received, payroll, sales platforms. Pennylane's design starts here [seen, company pages]:
- the client and the accounting firm work in the same system, with different permissions;
- bank transactions arrive continuously;
- invoices come in by e-invoicing or by each client's own email address;
- the firm's rules apply first, then AI suggestions, then the client's input.

Pennylane says 63% of invoices and transactions need no manual action to be entered, and 84% of reconciliations come from AI suggestions [company claims]. Most of that comes from where the data originates, not from clever models.

France made e-invoicing mandatory from 1 September 2026 [seen, company page]. That puts invoice data in digital form at the source by law. The UK has been moving towards e-invoicing too, but I have not checked its timetable.

### What disappears
- **Bookkeeping as a job.** Every transaction is classified when it happens. If the classification is unclear, the question goes to the owner at the moment of payment, when the answer is known, rather than months later. The accountancy example found that the owner, not production, was the bottleneck. Moving to the point of work dissolves most of that bottleneck, because there is far less to ask later.
- **Year-end as a project.** Statutory accounts and the tax computation are produced from a ledger that is always closed. People's judgement concentrates on a few genuine choices.
- **VAT preparation and quarterly updates as work.** They are computed continuously, and filing is a confirmation.
- **Chasing records.** There is nothing to chase if records are created where the money moves.

### What appears
- **A live position:**
  - cash;
  - tax owed to date, held in a "tax pot";
  - profit;
  - a forecast.
- **Answers and advice at the moment of decision.** "Can I afford to hire?" "Should I take a dividend now?" "What does this contract do to my VAT?" The firm's agent sits in the owner's chat, and a named person is available when the stakes are real.
- **Financial operations, not just records.** Paying suppliers, invoicing customers, chasing late payers and managing cash. The firm runs the client's finance function rather than reporting on it.

### Where the firm's people and agents sit
- **Inside the client's systems,** not in an office that receives documents. The firm's agents are in the client's bank feeds, invoicing, payroll and chat.
- **Embedded people.**
  - For smaller clients: a named finance partner who works in the client's channel and system.
  - For larger clients: a fractional finance lead who is part of the client's team, perhaps on site some days.
- **The client's system is the firm's factory floor.**

### The boundary choice
| Option | What it means | Examples |
| --- | --- | --- |
| **The firm owns the platform** | The firm is software plus licence plus people: one integrated stack | Digits claims agents automate most bookkeeping, and sells to firms [seen, vendor claim]; Pennylane ran its own accounting firm and is selling it [seen] |
| **The firm builds on a platform** | Use Pennylane, Xero or similar; differentiate on service, advice and the firm's own agents on top | Pennylane firms. One claims 5,000 client files from three offices [seen, company testimonial] |
| **The firm is a portable agent layer** | Its agents plug into whichever ledger and bank the client uses, through open interfaces | Pennylane opened access for outside AI assistants in August 2026 [seen]; most of this option is [conjecture] |

Pennylane chose to be the platform and promised never to sell accounting services, so that firms become its distribution [seen, firm charter]. That is a deliberate choice of boundary. It also shows what the 2035 contest in accountancy may be about: whoever holds the shared system where client and firm work together.

### What this does to the design
- **The unit of work** is the transaction or event at the source, not the case.
- **The measure** is the share of the client's financial life handled as a side effect, not the number of cases done.
- **The firm's product** is a continuous finance function with advice and accountability, not "accounts and returns".
- **The people needed:**
  - governors of the rules;
  - exception handlers;
  - advisers at the moments that matter;
  - named partners;
  - accountable officers.
- **The question of headcount changes.** It is no longer "how many people for 5,000 clients". It is "how many clients per accountable person when the work is a by-product". Today's best platform-based firms already claim thousands of files for small teams [seen, unverified].

---

## 5. Lettings, redesigned from scratch

### The outcomes
- **The landlord:** rent arrives, the property stays compliant and in good order, there is no hassle, and the asset's value is protected.
- **The tenant:** a home that works, fair treatment and quick fixes.

### Where information is born
- **In the building:** damp, leaks, boiler faults, smoke alarms, door access, energy use.
- **In the tenant's life:** identity, income and payments.
- **In the landlord's choices:** policies, spending limits, attitude to risk.
- **In counterparties' systems:** deposit schemes, councils, certificate registers, contractors.

### What disappears
- **Most of the 28 touches in a letting** [reasoned]:
  - Identity and income are checked at the source, through open banking and digital identity, instead of by collecting documents.
  - Viewings are self-guided, with smart access.
  - Contracts are standard and signed digitally.
  - Deposit or deposit-replacement is automatic.
  - Move-in uses a guided video inventory by the tenant.

  The goal is not five touches; it is zero touches for the standard letting, with people only for exceptions.
- **Inspections and compliance as visits and chasing.** Sensors and digital certificate feeds make compliance a continuously monitored condition. Damp becomes a live signal rather than a twelve-month outcome. The lettings example found sensors make slow outcomes fast.
- **Repair triage as phone calls.** A sensor alert or tenant video triggers dispatch within the landlord's standing policy, to a network contractor. Payment follows evidence of completion.
- **Landlord approvals.** The landlord sets the policy once: spending limits by type of repair, tenant criteria, rent strategy, a float. The firm acts within it.

### What appears
- **The property as an instrumented, managed asset** with a live record of condition, compliance, income and costs.
- **Predictive maintenance,** and evidence that supports the asset's value.
- **For tenants,** an interface (later, their own agent) that gets things fixed without chasing.

### Where the firm's capability sits
- In the building: sensors, locks and telemetry.
- In the landlord's portfolio dashboard and policy settings.
- In the tenant's phone.
- In the contractor network's dispatch and payment.

The office becomes a small control room, plus people in the field.

### Dwelly against this design
Dwelly is taking the fast route at level 1:
- it buys agencies;
- it keeps landlord relationships with people;
- it automates the existing process step by step, while also improving outcomes it can measure.

Dwelly reports offer to signed agreement falling from 19 days to about 11, and fall-throughs from 14% to 9% [seen, company figures].

That route wins the clients and the data quickly. Level 3 needs changes that may sit badly with acquired agencies: instrumenting buildings, standing landlord policies, new contracts with contractors and tenants, a different role for negotiators.

So the competitive question for 2035 is who reaches level 3 first:
- **the roll-up,** which has the clients but a process built to be automated;
- **the clean-sheet builder,** which has the design but no clients.

This is the familiar pattern in which incumbents automate the old process well, and a redesign arrives from someone not tied to it [reasoned].

---

## 6. Staff and processes inside the client's world

Ben asked about staff or processes integrated into the client, on site or in their systems. There are four forms, which can be combined:

| Form | What it is | Where it fits |
| --- | --- | --- |
| **Shared system** | Firm and client work in the same software in real time, with different permissions | Accountancy now (Pennylane, Xero) [seen]; lettings through landlord and tenant portals |
| **Agents inside the client's tools** | The firm's agents connect to the client's bank, ledger, chat, property systems and sensors through open interfaces | Becoming possible now [seen, early]; normal by the 2030s [conjecture] |
| **Embedded people** | A named person who works in the client's channel and, for larger clients, sits with the client's team some days a week | Fractional finance leads, outsourced in-house legal and property operations [seen in parts] |
| **The firm runs the client's function** | The client's finance or property operations are the firm's operation, on the client's side of the line | Outsourced finance functions and build-to-rent operators [seen]; with agents, viable for small clients [conjecture] |

What this changes [reasoned]:
- **Intake largely disappears.** The firm is already where the information is born. The worked examples' biggest bottleneck, getting facts from clients and outsiders, shrinks.
- **The boundary between firm and client moves.** "Send us your documents" becomes "we live where your work happens". That raises switching costs and deepens trust. It also raises questions of data rights and of who controls the system.
- **The relationship becomes continuous.** A firm present daily in the client's finances or building is involved in decisions before they are made.
- **Platform ownership becomes the strategic question.** If the firm lives inside the client's systems, whoever owns those systems has power over the firm. Pennylane resolved that by being the platform and never selling the service. Digits chose to own the ledger. Dwelly chose to own the agencies.

---

## 7. What this changes in the overall design

| Earlier assumption | After the electricity test |
| --- | --- |
| The unit of work is a case that comes in | The unit is an event at its source: a transaction, a sensor reading, a decision |
| The firm processes what clients send | The firm lives where the client's work happens |
| Measure: cases closed with no human touch | Measure: the share of the client's affairs handled as a side effect; touches per outcome designed towards zero |
| People at the boundaries with clients and outsiders | Fewer boundaries to staff, because more information is born inside the shared system. People concentrate on judgement, advice at moments that matter, relationships and accountability |
| The firm's boundary is the firm | The firm's boundary is a choice: own the platform, build on one, or be a portable layer |
| Teams organised around types of work | Teams organised around the client's world: their finance function, their portfolio of buildings |
| An agent-first roll-up as the bold option | An agent-first roll-up is level 1. The bold option is level 3 |

---

## 8. Where this is weakest

- **Level 3 depends on clients adopting shared and instrumented systems:**
  - bank feeds;
  - e-invoicing;
  - open banking;
  - sensors in rental homes;
  - landlords setting standing policies.

  Adoption by small clients is historically slow, so the clean-sheet design may run ahead of its market.
- **Counterparties must provide interfaces.** HMRC does not allow automation of its web pages, and councils, deposit schemes and contractors vary widely.
- **Platform dependence cuts both ways.** Building on Pennylane or Xero is fast but cedes power. Building a platform is slow and capital-hungry; Pennylane raised about €360 million [seen, press].
- **All figures for Dwelly and Pennylane are company claims.** No independent evidence on headcount or outcomes was found.
- **The UK e-invoicing timetable is not checked.**

---

## 9. What to do next

- **Redo the two worked examples at level 3.** Start from the client's outcome and the point where information is born. Treat the boundary choice explicitly. Show what the firm, its people and its economics look like when most of today's 87 and 123 lines simply do not exist.
- **Add level 3 to the base design** in step 3, with the boundary choice as one of the main choices.
