# Experiment Card

## Primary Test: Wizard of Oz (Area 1 — goer regret-aversion)

### Hypothesis
Among studio-goers who have not committed to a studio or off-peak slot, removing commitment risk (no package required, explicit no-obligation guarantee) will produce a meaningfully higher booking-and-attendance rate for an off-peak slot than the identical slot with normal commitment terms. Both arms get the same visibility and the same instant booking confirmation, so the only difference is commitment risk.

### Method
Run a Wizard of Oz test with 10 regular boutique class attendees in Casablanca and Rabat (5 per arm), recruited through our Moroccan contact's WhatsApp network (`recruitment.md`), by sending each person the same message about the same real off-peak class at the same price. Arm A adds one sentence: no package required and a full refund if they don't like the class. Arm B states standard booking and payment terms. Bookings are confirmed instantly by a team member in both arms, and attendance is confirmed with the studio after the class.

Controls written before running:
- **Assignment:** alternate A/B in the order contacts are received, logged in the results table before the message is sent.
- **Script:** identical wording except the single commitment sentence. Both scripts are saved in `experiment-scripts.md`.
- **Confirmation:** instant reply in both arms, so booking certainty cannot explain a difference (see pre-test signals below).
- **Consent:** participants are told afterwards that the booking was coordinated by students for a course project; no payment is taken without their knowledge.

### Metric
Booking rate and attendance rate per arm, recorded separately, plus the gap between arms (Arm A minus Arm B) on book-and-attend.

### Threshold
Set before testing:
- **Supports the assumption:** Arm A's book-and-attend rate is at least 40 percentage points higher than Arm B's (e.g. Arm A ≥3 of 5, Arm B ≤1 of 5).
- **Counts against it:** gap under 20 points.
- **Inconclusive:** gap of 20–39 points, or high booking with low attendance in Arm A.

### Evidence strength
MEDIUM — real target users in Morocco and real booking behaviour, with a same-visibility, same-confirmation control isolating commitment risk. Limited by 5 per arm and a single recruiting network.

### Decision rule
- **Supports (≥40 pp):** CONTINUE. Recruit 2–3 pilot studios from the owner interviews and run a 10-per-arm version on their real off-peak classes before Session 22.
- **Against, both arms book well (<20 pp):** CHANGE. Commitment risk isn't the barrier; pivot towards a discovery or instant-booking mechanism.
- **Against, both arms book poorly (<20 pp):** CHANGE. Treat absence of demand for that slot as more likely; test a different slot or time before concluding.
- **Inconclusive (20–39 pp):** CHANGE. Run one more round of 5 per arm, varying only the strength of the guarantee.

---

## Pre-test signals already collected
Three card-based Wizard of Oz trials were run before the primary test (`personas/selected_personas/oz-trials.md`). They measured stated intent ("would you book this?"), not real bookings, and used friends-of-friends rather than the Moroccan target cohort.

| Trial | Cards | Result | What it suggests |
|---|---|---|---|
| Persona 1: Package-Wary Tryer | Single class at gym-equivalent price, no package | 5 of 8 would book | Price is a fixable barrier; 1 skip cited not knowing the instructor |
| Persona 2: Last-Minute Booker | A: instant confirmation vs. B: refund guarantee | A: 4 of 5, B: 2 of 5 | **Certainty of getting in mattered more than removing financial risk** |
| Persona 3: Unanchored Sampler | Single trial class | 5 of 7 would book; 3 of those 5 would probably return | Offer is appealing; return intent untested in practice |

**This partly contradicts our riskiest assumption.** In Persona 2's trial, the refund guarantee (risk removal) did worse than instant confirmation, and the people who skipped it said they were worried about not knowing whether they had a place, not about losing money. That points to booking friction and certainty, not regret-aversion. The primary test now holds instant confirmation constant in both arms, so this rival explanation cannot drive the result. The rival hypothesis is also logged in `assumptions.md`.

---

# Supporting Layers

These don't replace the primary test. They cover questions it can't answer: owner adoption, whether our goer sample asks the right question, and whether the result is plausible at market level.

## Layer 1: Owner-side Interviews (Area 2 — owner adoption)

### Hypothesis
Independent boutique studio owners will see a no-commitment single-class offer, at their own price and seat limit, as meaningfully different from a discount and will be willing to offer it.

### Method
Run interviews with 5–8 independent boutique studio owners in Casablanca and Rabat (15–25 classes a week, owner sets the schedule) by showing the no-commitment concept next to a discount concept, asking them to distinguish the two and to describe what they have already tried for off-peak classes and why it fell short.

### Metric
Number of owners who, in their own words, distinguish the concept from discounting and say they would offer it, out of all owners interviewed.

### Threshold
At least 5 of 8 owners (≥60%) both distinguish it from discounting and say they would offer it.

### Evidence strength
LOW-MEDIUM — real target users, but stated willingness rather than observed adoption.

### Decision rule
- **Met (≥5 of 8):** CONTINUE. Ask the willing owners to commit one real off-peak class to the pilot.
- **Missed (<5 of 8):** CHANGE. Redesign the framing or revenue model (guarantee terms, revenue share) and re-interview a new group.
- **Mixed (distinguish it but hesitate, or the reverse):** CHANGE. Follow up with the hesitant owners to find whether the blocker is perception or a separate concern such as revenue risk or admin load.

### Results so far (`personas/selected_personas/gym_owners.md`)

| Owner | Method | Distinguishes from discounting | Would offer it |
|---|---|---|---|
| Owner A | In person | Yes | Yes |
| Owner B | Phone | Yes | Yes, if they control which seats open |
| Owner C | In person | Yes | Yes |

**3 of 3 real owners so far, against a target sample of 5–8.** Not yet enough to clear the threshold; 2 to 5 more interviews are needed. The AI-simulated owner responses in `gym_owners.md` are excluded because they are not evidence.

## Layer 2: Goer-side Interviews (sample sanity check)

### Hypothesis
The people recruited for the primary test resemble real target goers closely enough that no major barrier specific to real goers is missing from the test design.

### Method
Run interviews with 4–6 people matching the goer USER profile before the primary test, asking about their recent behaviour around off-peak classes and any reason they wouldn't book that our hypotheses don't cover.

### Metric
Number of interviews that surface a barrier not covered by regret-aversion, timing/awareness or absence of demand.

### Threshold
Sound enough to proceed if 0–1 interviews surface a new barrier; 2 or more triggers a redesign before the primary test.

### Evidence strength
MEDIUM — real target users, but recollection rather than observed behaviour.

### Decision rule
- **Met (0–1 new barriers):** CONTINUE with the primary test as designed.
- **Missed (2+ new barriers):** CHANGE the primary test's hypothesis, method, or both first.

### Results so far
Two barriers outside our original three hypotheses have already appeared in goer interviews and trials: **booking certainty** (Persona 2) and **not knowing the instructor** (Persona 1). That meets the "2 or more" trigger, so the primary test was redesigned: instant confirmation is now held constant in both arms. Instructor familiarity is not controlled and is logged as an open question.

## Layer 3: Market Research (plausibility check)

### Hypothesis
Available data on trial-to-membership conversion or fitness spending in Morocco will show the primary test's result is not wildly out of line with how the real market behaves.

### Method
Desk research: published reports on Morocco's fitness and wellness market, plus any trial-conversion figures a partner studio is willing to share, compared against the primary test's result.

### Metric
Whether the primary test's rate falls within a plausible range of comparable benchmarks.

### Threshold
At least one credible source found and the result not a dramatic outlier (e.g. not 10× higher or lower). If no data exists, this layer is marked an open gap.

### Evidence strength
LOW — secondary aggregate data, a rough plausibility check only.

### Decision rule
- **Plausible:** CONTINUE, treating the primary result as credible pending the pilot.
- **Outlier:** CHANGE, treating the result sceptically and moving the real-studio pilot earlier.
- **No data:** mark as an open gap and flag generalisation confidence as unresolved.

### Results so far
Not started.

---

## Results and decision (primary test)

| # | Arm | Contacted (date) | Booked | Attended | Notes |
|---|---|---|---|---|---|
| 1 | A | | | | |
| 2 | B | | | | |
| 3 | A | | | | |
| 4 | B | | | | |
| 5 | A | | | | |
| 6 | B | | | | |
| 7 | A | | | | |
| 8 | B | | | | |
| 9 | A | | | | |
| 10 | B | | | | |

| | Arm A | Arm B | Gap |
|---|---|---|---|
| Book-and-attend rate | | | |

**Outcome against threshold:** [Supports / Against / Inconclusive]
**Decision:** [Continue / Change / Stop], following the decision rule above
**What would change our mind:** [the single result that would reverse this decision]

---

## How the layers relate
- **Primary test** checks the mechanism itself: does removing commitment risk change real booking behaviour.
- **Layer 1** checks a separate risk, owner adoption, that no goer test can substitute for.
- **Layer 2** checks whether the primary test is asking the right question; it already caused one redesign.
- **Layer 3** checks whether the result could plausibly hold at market level.

None of these alone shows the venture will work. Together they cover mechanism, adoption, sample validity and market plausibility, which is the most a Phase 1 validation can realistically deliver before building starts.
