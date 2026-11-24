# Unit 1. Foundations: what a services firm is for, and the right metaphor

Draft by Claude, 24 November 2026. Design by inference. Library records are used as inspiration and named where they shaped a point; nothing here is a claim that it has been shown to work.

## 1. What a services firm actually sells

Strip a services firm to first principles and it sells five things, bundled:

1. **Capacity.** Hours of work the client cannot or will not do.
2. **Know-how.** Knowing how the work is done well, including the exceptions.
3. **Accountability.** A named, licensed, insured party who carries the consequence if it is wrong.
4. **Coordination.** Moving other parties (tax authorities, contractors, courts, counterparties) to get an outcome.
5. **Trust.** Someone the client can call, who knows them, and whom they believe.

The firm's familiar shape is the pyramid, leverage ratios, the billable hour, the partnership and the apprenticeship. That shape is not a law of services. It is the answer to one constraint: trained expert humans were scarce, slow to make and the only way to deliver items 1 and 2. Choudary calls professional services "a locked system built around four constraints". The library's discovery sweep holds his piece.

AI removes that constraint for capacity and for most codified know-how. Their marginal cost heads towards compute plus checking. The other three do not get cheaper in the same way. Accountability still needs a liable party. Coordination still runs at the speed of other parties. Trust still has to be earned. A fourth scarce thing appears that the old firm never managed: **the rate at which the firm's know-how improves**.

So the ideal firm is not the old firm with fewer people. It is a different machine, organised around what is now scarce:

| Old firm is organised around | New firm is organised around |
| --- | --- |
| Rationing scarce expert hours | Producing outcomes at near-zero marginal cost |
| Leverage: juniors do volume, partners sign | Agents do volume; people sit at signature, judgement on the hard cases, relationship, and teaching the system |
| Know-how in heads, passed on by apprenticeship | Know-how as versioned, executable playbooks, verifiers and a corpus of solved cases |
| Billing hours | Selling outcomes and maintained conditions |
| Improvement by individual experience, slowly | Improvement as a designed, weekly loop the firm runs on itself |
| Quality by review of each person's work | Quality by verifiers built into the line, plus independent audit |

## 2. Is the factory metaphor helpful or harmful?

Both. It is the right metaphor for one lesson and the wrong one for several others.

### Where it helps

- **Redesign around the new power source; don't bolt it on.** The best historical parallel is electrification rather than Ford himself. Factories first swapped the steam engine for one big electric motor driving the same shafts and belts, and saw little gain. The gain came decades later, when factories were rebuilt around a motor at every machine: single-storey plants, flow laid out by the work rather than by the drive shaft. Ivan Zhao (Notion), in the discovery sweep, says firms are "still swapping out the waterwheel". This is the core of your Ford point: the Model T plant was designed for the new way of producing, not adapted from the old one.
- **The line is designed before production starts.** Work flows through defined stations, with typed inputs and outputs and parts that fit anywhere. In services this means typed tasks with defined inputs, playbooks and checks, so a case can move between agents and people without being re-explained.
- **Quality built in, not inspected at the end.** This is Toyota more than Ford. Jidoka means a machine stops itself on an abnormality; andon means anyone can stop the line. Remo Jansen applies this to agents. Toyota's own quality AI checks every document rather than a sample.
- **Price cuts expand the market.** The Model T was cheap enough to create buyers who never had a car. A003 names the same effect: "cases and customers that were uneconomic becoming viable". An AI-native firm should expect most of its growth from clients who never bought the service before, not from taking share.

### Where it harms

- **Ford's line was rigid.** "Any colour so long as it's black." The changeover to the Model A shut the plant for months. An AI-native firm's line has to change weekly and get better with every model release, without a rebuild. A fixed line is the wrong picture.
- **Fordism deskilled the worker.** In the new services firm the people who remain are the most skilled, and their judgement is what teaches the system. A factory picture that treats people as interchangeable station staff will drive out exactly the people the firm needs. Gerlach's "AI knowledge trap" in the sweep: cut the experts and the models degrade unseen.
- **A factory makes one standard product.** Much of the value in services is tailoring. AI makes mass customisation cheap, so the firm does not have to choose between standard and bespoke the way Ford did.
- **In a factory the customer is outside.** In services the client is a co-producer: they hold the records, the context and the decisions. Counterparties also act on the work. The "line" runs partly inside other organisations.
- **A factory optimises a fixed process; this firm must optimise its own improvement.** The scarce asset is the rate of learning, which the factory picture leaves out entirely.

### A better set of metaphors, each for its own job

- **Electrification, for the transition.** Rebuild around the new source of power; don't bolt it on. This is also the lens for the retrofit unit.
- **A codebase, for what the firm is.** Playbooks are code, verifiers are tests, past cases are the test suite, improvements are commits, rollout is continuous deployment, and a bad change is rolled back. I think this is the most useful single picture: the firm's know-how becomes something you can version, test, diff, deploy and improve. Call it the compiled firm.
- **Toyota, for the culture of improvement.** Everyone improves the work daily, anyone can stop the line, and problems are surfaced, not hidden. McElheran and colleagues, in the sweep, find that about half of old plants' early AI productivity loss came from dropping lean routines.
- **A teaching hospital, for the people.** Triage, protocols for the common cases, specialists on the hard tail, and trainees learning on real cases under supervision. It fits the judgement desk and answers the junior-pipeline problem.
- **Autopilot levels, for agent autonomy.** Graded levels of delegation, with clear handover rules, earned by record.

**Recommendation:** keep "factory" only as shorthand for the transition lesson and for designed flow. Make the codebase the model of the firm and Toyota the model of its culture. Say this explicitly whenever the design is presented, because "factory" invites the wrong instincts in partners and staff: rigid lines, deskilling and standard-only products.

## 3. Design axioms for the ideal model

These carry into every later unit.

1. **Design for the capability of 2028, not 2026.** Assume models get better and cheaper every six to twelve months. A good design improves automatically with each model, by running the test suite on the new model and promoting tasks up the autonomy ladder. A design that needs rebuilding each time is wrong.
2. **Work is born on the line.** In a firm built new, the work happens inside the system, so the record is a by-product and nothing needs watching (L022). Retrofit tools such as Marble Cognition have to watch people because the work happens outside the system. A native firm never has that problem. This is the strongest argument for building new.
3. **People sit at the scarce points.** These are the signature, judgement on the hard tail, the relationship, and teaching the system. Everything else defaults to agents, and the burden of proof sits on keeping a person in the loop. Signature and relationship are the exceptions, where the burden runs the other way.
4. **The asset is the compiled know-how.** That means the playbooks, the verifiers, the test suite of solved cases and the exception corpus. It is what the firm owns, protects and improves, and the thing a buyer would pay for.
5. **The rate of improvement is the master measure.** Track how fast exception rates, the cost per case and the error rate fall, week on week.
6. **Verification is the core craft.** Making the work is cheap. Showing it is right, independently of the maker, is the expensive part and the firm's main engineering effort (L014, L015).
7. **Sell outcomes and maintained conditions, not hours.** Let price fall to grow the market. Capture value through volume, scope and owning the client's live records ("state").
8. **Own the client's state where possible.** The firm that holds the client's live ledger, compliance record or case file becomes the client's operating system and is hard to replace.
9. **Accountability is designed, not assumed.** A named person signs, with a verification system they can actually rely on, and an approval that is not a rubber stamp.

## 4. Proposed units

1. **Foundations.** This unit.
2. **The work system.** Products and cases; the task contract (your four requirements plus what is missing); autonomy levels and how a task is promoted; verification; state and context; how a case flows; exceptions.
3. **The self-improving firm.** The improvement loops (case, line, firm, model upgrade); what a recursively self-improving services firm needs; what would actually happen as it compounds; failure modes such as drift, gaming the measures, correlated errors and skill atrophy.
4. **People, agents and organisation.** Roles, shape and numbers; pay, including paying for teaching the system; juniors; agents as staff; decision rights; the organising principles for people and agents; who needs to be AI-pilled.
5. **The commercial model and the stack.** Pricing, maintained conditions, market expansion, and what is left when the work is a commodity. Also the technology stack and the back office.
6. **Building it from scratch.** The Crosby and Garfield path, from founding team to scale, and where acquisitions fit: buying books of clients and licences to move onto the line.
7. **Retrofitting the messy incumbent.** A firm with several systems, tacit know-how and partners with interests. What is required to reach the ideal state, the sequence, what to throw away, and how much of the old firm survives.
8. **Variation and where to invest.** How the design changes by type of business, and the most promising places to build or invest.

Each unit is one short document. You review it before the next one starts. At the end they are assembled into one page in the library.
