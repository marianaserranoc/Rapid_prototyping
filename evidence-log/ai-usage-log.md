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
