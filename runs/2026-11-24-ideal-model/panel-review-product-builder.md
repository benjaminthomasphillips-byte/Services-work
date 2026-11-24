# Panel review: a founder and design-led product builder

*Role: co-founder of a small, highly regarded software company known for craft, small senior teams, opinionated products and quality as strategy. Not a named real person. Reviewing "Step 3. How we would build an AI-native services firm", draft of 24 November 2026.*

I mark what I know from building software companies as **[experience]** and what I am guessing about services and about 2035 as **[conjecture]**.

---

## My verdict in a paragraph

The bones are right, and some of the instincts are better than I expected from a services document. The four-hour promise, the build-versus-rent table, the back office as the engine's first client, independent quality, and "nobody is paid on volume they also check" are all things I would keep. But the draft does what it says it won't: it reads like an organisation chart for a good firm, not a point of view on a great one. It has ten design choices and no refusals. It treats the portal as the product just as clients' agents are about to make portals irrelevant. It splits the firm into pods without noticing that pods will produce five different client experiences. And it is quiet on the bold commercial question for 2035: whether the firm sells work, or sells a guarantee that the work is right. Mostly I would change emphasis, not structure. Fewer functions, one owner of taste, a product built API-first, and a firm prepared to stand behind its output with its own balance sheet.

---

## Where it is wrong or naive

**1. Pods will fragment the product. [experience]** Conway's law is not optional. Give five pods five case types, an engineer each and the freedom to "decide inside their type of work", and within eighteen months you will have five intake flows, five status vocabularies and five ways of explaining a fee. Every company I know that organised around autonomous squads without a single owner of the experience shipped a patchwork. The draft names "one person who owns the client experience" in the founding team, then loses that person when it describes the grown firm: the centre has Platform, Quality, Talent, Commercial and Back office, but no Design. Make the client surface (portal, API, language, notifications) a single product owned centrally by a small design and product group with a veto. Pods should build on it, as they build on the platform, not beside it.

**2. "The client experience is the product" is right for 2027 and wrong for 2032. [conjecture, from experience of how interfaces die]** Section 4 is a table of portal virtues. In landscape C, which the draft itself rates as plausible, the client's agent is the user. Nobody admires the status page; the agent reads a feed. What survives is reliability, speed, being right, being accountable, and a clean, well-documented interface: developer experience for machines. So build API-first from day one. The portal should be the first client of the firm's own API, the same discipline the draft already applies to the back office. Calling the agent interface "conjecture on timing" is too cautious. It costs almost nothing to build the portal that way in 2027 and a great deal to retrofit in 2031.

**3. Agents "on the organisation chart" is a metaphor that will mislead. [experience]** Agents are software. They need versioning, rollback, tests, owners, budgets and logs, which the draft rightly lists. They do not need onboarding, performance reviews or retirement parties. Dressing them up as staff makes people anxious and puts their management in an HR frame, when what it needs is release engineering. Keep the accountability and drop the anthropomorphism. Every agent should be a versioned deployment with a named human owner.

**4. The rhythm table is process dressed as momentum. [experience]** Daily, weekly, monthly, quarterly and per-release reviews are five standing rituals. At my company the cadence is simple: short build cycles, a written update, and the rule that quality problems jump the queue. The draft's best operating idea is buried in principle 6: every exception is a lesson. Turn it into a hard rule, the services equivalent of a zero-bug policy. Every classified exception gets an owner and is fixed within one cycle, or it is consciously accepted in writing. That single rule will do more than the five meetings.

**5. Hiring experienced people from squeezed mid-sized firms is a culture risk. [experience by analogy]** When we hired people from large incumbents, the ones who struggled weren't short of skill. They brought habits: meetings as work, polish over shipping, escalation over ownership. Billable-hour culture is a stronger habit than most. Hire them, but through paid work trials on real cases, and in small numbers per pod. The draft says "experts with taste" but never says how you test for taste. A trial is the only test I trust.

## What is too generic

**6. There are no refusals. [experience]** Opinionated products are defined by what they won't do. The ten choices would fit any well-run modern firm. Write the "no" list, publish it and keep to it: no hourly billing, ever; no bespoke workflows for a big client; no custom portals or white-labelling in the first five years; no case types the engine cannot measure; no growth in a pod that breaks its service level. The deadliest trap for a craft company is the large customer who wants it done their way. Professional firms have said yes to that customer for a century. Saying no is the moat.

**7. Talent density needs a number. [experience, with a conjecture]** "Small and senior" is said, not designed. Set a headcount ceiling or a revenue-per-person floor, and make every hire above the line a founder decision. A hard ceiling forces automation honestly. In landscape A, a firm with a few hundred people serving a market that incumbents staff with tens of thousands is the prize. The firm should commit to that shape in advance, not hope to discover it in 2033.

## What it fails to anticipate, 2027 to 2035

**8. The firm should sell a guarantee, not work. [conjecture, grounded in step 1]** Step 1 says the profit sits in the slow-to-check layers: accountability, the hard tail, outcomes that show late. The natural product is warranted work. Fixed price, plus a stated promise that if we are wrong, we pay. Underwrite it with the outcome data the engine already collects. Start with a captive or a partner insurer, and by 2032 consider holding the risk yourself. A firm that turns its track record into a priced guarantee has a moat that rented models cannot copy. It is also exactly what a client's agent will look for when comparing suppliers by machine. The draft mentions insurance only as a constraint in its weaknesses section, never as a product.

Other bold moves it does not consider:

- **The ideal service is invisible.** The draft's "subscription to a maintained condition" is its most forward-looking phrase, and it is buried in a table. Push it: by 2035 the best experience is no interaction at all. Books are always closed. Compliance is always met. The client hears from the firm only when a decision needs a human. Measure the firm on how rarely clients need to contact it.
- **Publish a changelog to clients.** No professional firm tells clients what improved this week. A public changelog makes the engine visible, builds trust and keeps the firm honest. It costs almost nothing.
- **Open the playbooks.** Publishing part of the method, as some software companies publish how they work, sets the standard for the category, recruits the right experts and costs little: the advantage is the engine and the data, not the text. **[conjecture]**
- **Own the licence.** Where regulation allows, holding the regulated permission itself, and later offering it to the experts on a platform, is the stronger version of the "platform" end form.
- **The real competitor is the software incumbent.** By 2030 the accounting-software and legal-research giants will bundle "done for you" services. The firm's answer is to be the accountable party they cannot be without becoming regulated firms. This deserves a section, not a line. **[conjecture]**
- **Taste concentrated, not distributed.** In a world of abundant generated output, the scarce thing is the judgement about what good looks like. The firm's identity should rest on a small number of named principals whose standards are visible. That is closer to a great studio than a partnership.

## The strongest ideas, to keep

- The single public promise that incumbents cannot match without rebuilding. It is the spec, the marketing and the quality bar at once. This is exactly how good products start.
- Rent the intelligence; own the learning. The build-versus-buy table is clear and correct.
- The back office running on the engine from the first month.
- Quality independent of the pods and reporting to the board. "The maker never checks its own work." "Nobody is paid on volume they also check."
- Autonomy as a dial that can be turned down without disgrace.
- A burden of proof on complexity, and anyone can stop the line.
- Pay for contribution to playbooks and tests, judged by peers rather than usage counts.
- Testing the design against three landscapes, with the warning that the economics differ greatly between them.

## What I would do differently

I would found it as a product company that happens to hold a licence. One design and product owner with a veto over everything the client or the client's agent touches. An API first and the portal built on top of it. A published "no" list. A headcount ceiling. A zero-exception-debt rule in place of most of the meetings. By year three, a warranted, fixed-price product that turns the engine's track record into a guarantee. I would back the team whose founders show taste in the first week of design-partner work, not the one with the best org chart. The draft is close to describing that firm. It needs to be braver about what that firm refuses, and about what it is prepared to promise.
