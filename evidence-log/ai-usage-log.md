## Pass 1 — Collaborative drafting (Claude, this conversation)

**Tool used:** Claude
**Purpose:** Draft and sharpen the Opportunity Frame fields (Pain point, User, Need, Insight, How Might We) for the studio off-peak capacity idea.

## What I drafted first, then AI challenged:

**Pain point (v1):** AI flagged that "off-peak students under-capacity" conflated who/what was under capacity, that it was missing the actual cost to the studio, and that "discounting is temporary" was diagnosing the wrong root cause (should be structural — discounting changes who shows up, not when)
**USER (v1):** AI pushed for narrower specifics — size, business model, whether it's a chain vs. independent studio — rather than "fitness studios" broadly
**NEED:** minor wording fixes only (typos, tightened phrasing)

## What I accepted vs. revised:

Rewrote Pain point twice based on feedback before landing on a version naming the specific cost driver (fixed costs: rent + instructor pay)
Narrowed USER to: independent boutique studio owner/manager, 15–25 classes/week, sets their own schedule

## Pass 2 — Independent critical review (fresh AI chat)

**Tool used:** [fill in which AI you used]
**Purpose:** Independently critique the Pass 1 Opportunity Frame fields for specificity, evidence, and internal consistency — without context on how they were built.

### What it flagged

- **USER** is specific on operational size (class count, instructor count) but silent on modality (yoga/pilates vs. CrossFit/HIIT) and geography — both likely shape *why* a slot is off-peak in the first place
- **NEED** functionally restates the HOW MIGHT WE rather than describing owners' actual attempted workarounds and why they fall short — not yet falsifiable by an interview
- **INSIGHT** ("timing mismatch, not pricing") is the riskiest, least-supported claim in the frame — written as a settled conclusion, but there's no way yet to rule out the competing explanation that off-peak demand is simply absent rather than mistimed. These imply different products.
- **Internal inconsistency:** the PAIN POINT's cost-structure justification (fixed costs → any seat filled is a win) actually argues *for* discounting, not against it. The real case against discounting is a demand-composition argument (cannibalizing full-price attendees vs. recruiting net-new ones) — a separate claim that needs owner evidence, not cost-structure logic
- **HOW MIGHT WE** assumes the owner's core complaint is attendance/headcount, not margin or instructor retention — worth confirming

### What I accepted vs. still open

- **Accepted and fixed:** split the PAIN POINT into its two separate claims (cost-structure fact vs. demand-composition claim)
- **Accepted, reframed rather than fixed:** INSIGHT is now explicitly marked as an unvalidated, riskiest assumption (not a conclusion) — becomes the target for the Session 5 riskiest-assumption test in `experiment-card.md`
- **Flagged as open gaps** (not resolved, since no real owner interview exists yet): USER's modality/geography narrowness, NEED restating the HMW, HOW MIGHT WE's attendance-vs-margin assumption

## Pass 1 — Assumption mapping (Claude, this conversation, quick mode)

**Tool used:** Claude
**Purpose:** Brainstorm and cluster assumptions underlying the studio off-peak opportunity, and identify the riskiest one, using the venture-assumption thinking partner exercise (quick mode).

### What I drafted, then AI challenged
- Two early assumptions ("studios need free spots," "studios want to pay for another platform") were flagged as too vague/unfinished to test — pushed to identify the actual underlying claim
- "Digital booking gets adopted" was flagged as bundling two separate claims (studio-side and student-side adoption) that could fail independently — not yet split, kept as an open gap
- Accidentally pasted in a set of Nova-related (consumer-side/subscription) assumptions mid-brainstorm — caught before clustering, discarded to keep the file consistent with the studio-side `opportunity.md`
- "Studios keep availability updated in real time" was flagged as sitting ambiguously between Area 2 (trust/adoption) and Area 3 (technical feasibility) — placed in Area 3 as a judgment call

### What I accepted vs. revised
- Sharpened the elastic-routines assumption to name specific mechanisms (incentives, dynamic pricing, algorithmic nudges) rather than leaving it generic
- Considered adding an instructor-alignment area during the exhaustive check, decided it was a stretch, and set it aside rather than forcing a fourth area
- Confirmed 3 areas as mutually exclusive and collectively exhaustive after both checks

### Riskiest assumption and reasoning
Selected "target consumers have elastic routines and will shift given a nudge/incentive" over "studios will pay for a platform fee," because the pricing-model risk has a viable pivot (subscription → transaction commission) while the behavior-elasticity risk has no fallback — if false, the core value proposition doesn't exist.

**Note:** quick mode was run first; a full-mode re-run was planned for deeper coverage before moving to `experiment-card.md`.

## Pass 1.1 — Assumption Mapping & Load-Bearing Stress Test (Gemini, this conversation)

* **Tool used:** Gemini
* **Purpose:** Expand, simplify, and stress-test assumptions across Demand, Studio Adoption, and Feasibility, then isolate the single load-bearing (riskiest) assumption to lock Stage C.
* **What I drafted/requested, then AI challenged & refined:**
  * **Operational Gap Evaluation:** AI proposed adding an instructor-alignment assumption (#8) regarding pay and room-density pushback. I challenged this as an over-engineered stretch for an early-stage MVP where instructors follow owner directives, dropping it from the core list.
  * **Feasibility Gap Isolation (#7):** Identified real-time schedule management (studios keeping availability updated to prevent double-bookings) as the second core technical assumption under Area 3.
  * **Forced-Choice Load-Bearing Test:** AI forced a direct call between Assumption #4 (student routine elasticity) and Assumption #2 (studios paying platform fees) to determine which failure kills the venture vs. forces a minor pivot.
* **What I accepted vs. revised:**
  * **Accepted:** Plain-language framings for Area 2 and Area 3, and the inclusion of real-time availability updating as #7.
  * **Rejected:** Adding Assumption #8 (instructor compliance), keeping the scope focused strictly on student behavior and owner switching friction.
  * **Locked:** Stage C locked with Assumption #4 as the core pillar.
* **Riskiest assumption and reasoning:**
  * **Assumption #4 selected:** *"Target consumers have elastic routines and will shift given the right nudge/incentive."* Reasoning: If student routines are behaviorally locked to peak hours, no amount of dynamic pricing or software polish can create off-peak demand (the core idea dies). In contrast, if studio payment willingness (#2) fails, the business model can simply pivot from a SaaS fee to a commission-on-booking model.

## Pass 1 — Goal setting (Claude, this conversation)

**Tool used:** Claude
**Purpose:** Draft and sharpen the Product Goal and Sprint Goal, building on the confirmed Opportunity Frame and riskiest assumption (#4: elastic routines/nudges).

### What I drafted first, then AI challenged
- Product Goal (v1) included "high-margin revenue" and "price-conscious students... affordable, flexible access" — AI flagged that margin wasn't established anywhere in PAIN POINT/NEED (attendance/utilization was), and that the student-pricing language reintroduced consumer-side framing (echoing the earlier Nova mix-up) despite the USER being the studio owner throughout
- Revised Product Goal dropped the student-pricing angle and reframed around "net-new attendees" and "protecting margins/brand value" — consistent with the studio-side USER and the demand-composition argument already established in `opportunity.md`

### What I accepted vs. flagged as minor
- Accepted: Sprint Goal's explicit "non-price timing nudge" phrasing, which correctly operationalizes Assumption #4 and keeps it distinct from a discount-based test (avoids contaminating the "timing, not pricing" INSIGHT)
- Flagged, not resolved: "brand value" in the Product Goal is a new concept not previously validated anywhere in `opportunity.md` or `assumptions.md` — noted as a minor addition, not blocking

## Pass 1.1 — Goals Definition & Load-Bearing Sprint Alignment (Gemini, this conversation)

* **Tool used:** Gemini (working off previous context and critique from Claude)
* **Purpose:** Sharpen the long-term Product Goal and Stage D Sprint Goal, ensuring tight alignment with the locked riskiest assumption (#4) and the updated Opportunity Frame.
* **What we discussed, challenged & stress-tested:**
  * **The Discounting Trap:** When Gemini initially drafted a product goal mentioning "dynamic discounts" and "affordable access," we challenged this against the core Pain Point in the Opportunity Frame. Discounting cannibalizes full-price regulars rather than shifting schedules. We debated whether the venture is a "discount marketplace" or a "schedule-matching engine."
  * **Aligning with Claude’s earlier flags:** Gemini raised Claude’s previous point that timing mismatches and total absence of demand require two completely different solutions. If the core problem is timing, the goal must prove users shift schedules due to non-price nudges (e.g., priority access, accountability mechanisms) rather than just cheap tickets.
  * **Isolating the Sprint Goal:** We pushed to ensure the Sprint Goal wasn't a vague product milestone, but a direct, binary test of Assumption #4—measuring actual student routine elasticity before building any real software.
* **What was accepted vs. revised:**
  * **Revised:** Stripped all references to price-slashing from the Product Goal, refocusing it entirely on margin-protected yield management and schedule matching for studio owners.
  * **Accepted:** Defined the Sprint Goal around behavioral schedule shifts, explicitly isolating whether non-price incentives can move users into off-peak slots.
* **Locked Deliverables:**
  * **Product Goal:** Build an automated schedule-matching platform for independent boutique studios that systematically fills recurring off-peak capacity with net-new attendees while protecting studio margins and brand value.
  * **Sprint Goal:** Prove whether target consumers will behaviorally alter their daily routines to attend an off-peak class slot when given a non-price timing nudge or matching mechanism (validating Assumption #4).
