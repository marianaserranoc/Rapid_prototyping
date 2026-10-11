# Experiment Card

## How this card evolved
Earlier versions were replaced, not deleted from our thinking. Each change was triggered by something specific. Details of each step are in `ai-usage-log.md` and `pivot-log.md`; earlier file versions are in the repository's commit history.

| Version | What we planned to test | Method and threshold | Why we changed it |
|---|---|---|---|
| v1 | Goers have elastic routines and will move to off-peak slots given a non-price nudge (priority access + social matching) | Concierge: manual WhatsApp nudges to 5 people; ≥3 of 5 book and attend | The insight moved from timing to regret-aversion; a single group also couldn't tell which explanation caused a positive result |
| v2 | Goers avoid off-peak classes out of regret-aversion | Single-group Wizard of Oz with a low-commitment offer | One group can't separate regret-aversion from timing or awareness |
| v3 | Same, with a control | Two groups (low-commitment vs. normal terms, same visibility), 5 each; book-and-attend gap ≥40 pp; plus three supporting layers | Persona 2 card trial: instant confirmation beat a refund guarantee (4 of 5 vs. 2 of 5), so certainty could explain any gap |
| v4 | Same, controlling for certainty | Instant confirmation promised in both groups | The team can't verify who attends a class this week |
| v5 | Same | Two-version booking page (`booking-test/`), 5 per arm; reservation-rate gap ≥40 pp; decline reasons pick the pivot | With 5 per arm, one person moves the result by 20 pp, so even a 40 pp gap could be chance |
| **v6 (current)** | **Same** | **Same page, 20 per arm (minimum 15); gap ≥30 pp with Fisher's exact p < 0.05** | — |

## Primary Test: Wizard of Oz (Area 1 — goer regret-aversion)

### Hypothesis
Among studio-goers who have not committed to a studio or off-peak slot, removing commitment risk (one class, no package required) will produce a meaningfully higher **reservation rate** for an off-peak class than the identical class offered through the studio's usual 3-class pack. Both arms see the same class, studio, coach, price per class (300 MAD), seats left and promise of instant confirmation, so the only difference is commitment.

### Method
Run a fake-door Wizard of Oz test with **40 regular boutique class-goers in Casablanca and Rabat (20 per arm, minimum 15)**, recruited through our Moroccan contacts' WhatsApp networks (`recruitment.md`). Each person receives a link to a booking page (`booking-test/`, live at https://marianaserranoc.github.io/Rapid_prototyping/booking-test/) for a Reformer Pilates class at a fictional studio, Atelier Sable (Maârif, Tue 11:00).

- **Arm A (`#a`):** 300 MAD for 1 class, no pack or membership, pay at the studio.
- **Arm B (`#b`):** the same class through the studio's usual 3-class discovery pack, 900 MAD (300 MAD per class), valid 1 month.

A reservation means the person entered their first name and sent the pre-filled WhatsApp message ("I'M RESERVING … ref. S1/S2"). Declining sends "NOT FOR ME … reason: …" with the reasons they ticked. Immediately after each message, the team explains it was a student test, no class was booked and nothing will be charged, and asks for a 1-minute voice note on why. **Attendance is not measured in this round**; it moves to the Phase 2 pilot (`specs/roadmap.md`).

Controls written before running:
- **Assignment:** alternate A/B in the order contacts are received, logged in the results table before the message is sent.
- **Page:** both arms use the same page (`booking-test/index.html`); only the offer block differs. The reference code (S1 = A, S2 = B) is hidden in the message so participants don't see their arm.
- **Confirmation:** the same "spot confirmed within minutes" promise in both arms, so booking certainty cannot explain a difference (see pre-test signals below).
- **Transparency:** the page footer says it is a student test prototype with no online payment. Each participant is debriefed right after sending their message; no payment is ever taken.
- **Denominator:** the team logs who received link A and who received link B before sending, because the page cannot record visits.

### Metric
**Reservation rate per arm** = reservation messages received ÷ people sent that arm's link, plus the gap between arms (Arm A minus Arm B). Secondary: the reasons ticked in "Not for me" messages and stated in voice notes, counted by category (price, commitment/pack, certainty of a spot, coach, timing, prefers gym).

### Threshold
Set before testing:
- **Supports the assumption:** with 20 people per arm, Arm A's reservation rate is at least **30 percentage points** higher than Arm B's (e.g. Arm A ≥9 of 20, Arm B ≤3 of 20) **and** a one-sided Fisher's exact test gives p < 0.05. If only 15–19 per arm are reached, the same test applies, which means a gap of about 40 pp (e.g. ≥9 of 15 vs. ≤3 of 15).
- **Counts against it:** gap under **15 points**.
- **Inconclusive:** gap of 15–29 points, or ≥30 points without p < 0.05.

*Why these numbers:* with 5 per arm, one person changed the result by 20 pp, so a 40 pp gap could happen by chance. With 20 per arm, a 30 pp gap is unlikely to be chance (Fisher's exact test, one-sided, p < 0.05), so the threshold can be lower and still mean something.

### Evidence strength
MEDIUM-LOW — real target users in Morocco taking a real action (reserving and sending a message), with a same-page control isolating commitment. Weaker than attendance: a reservation costs nothing, and the studio is fictional. 20 per arm is enough to detect a large gap (about 30 pp), not a small one; recruiting through personal networks limits how far it generalises.

### Decision rule
Written before the test. The "Not for me" reasons and voice notes decide **which** pivot, so each branch names the evidence that picks it.

- **Supports (≥30 pp, p < 0.05):** CONTINUE. Keep the no-package single class as the core offer. Next: 2–3 pilot studios from the owner interviews, real off-peak classes, and measure **attendance and return at full price** (Phase 2, before Session 22).
- **Against (<15 pp), most decliners tick "price" or "prefer my gym":** PIVOT ON PRICE. Commitment isn't the barrier; the 300 MAD class is. Next: owner interviews on whether a lower first-visit price can avoid looking like a discount to regulars (new clients only).
- **Against (<15 pp), most decliners tick "not sure I'd get a spot":** PIVOT TO CERTAINTY. Build an instant-booking tool for studios' existing classes instead of a no-commitment offer.
- **Against (<15 pp), most decliners tick "I don't know the coach":** PIVOT TO TRUST. Test instructor profiles, short class videos or reviews before booking.
- **Against (<15 pp), almost nobody reserves in either arm:** CHANGE THE SLOT. Treat absence of demand for that time as likely; rerun with a different time before concluding.
- **Inconclusive (15–29 pp, or ≥30 pp without p < 0.05):** EXTEND. Send the links to 10 more people per arm, recompute once, then decide.

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
Partly done (`Fermi_estimate.md`, `market-alternatives.md`):
- **Found:** prices (250–400 MAD per reformer class; about 314 MAD for a month of gym in Casablanca), studio counts (43 in Casablanca, 11 in Rabat, likely undercounted), and that no multi-studio pass such as ClassPass appears to operate in Morocco.
- **Not found:** any Moroccan figure for trial-to-membership conversion. The only benchmark is unattributed US industry data (paid intro offers converting at 50–60%, free trials under 20%), so it is indicative only.
- **Status:** open gap for conversion; the reservation result will be compared against the US benchmark with that caveat.

---

## Results and decision (primary test)

| # | Arm | Link sent (date) | Reserved (Y/N) | Reasons if not | Voice note (Y/N) |
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
| 11 | A | | | | |
| 12 | B | | | | |
| 13 | A | | | | |
| 14 | B | | | | |
| 15 | A | | | | |
| 16 | B | | | | |
| 17 | A | | | | |
| 18 | B | | | | |
| 19 | A | | | | |
| 20 | B | | | | |
| 21 | A | | | | |
| 22 | B | | | | |
| 23 | A | | | | |
| 24 | B | | | | |
| 25 | A | | | | |
| 26 | B | | | | |
| 27 | A | | | | |
| 28 | B | | | | |
| 29 | A | | | | |
| 30 | B | | | | |
| 31 | A | | | | |
| 32 | B | | | | |
| 33 | A | | | | |
| 34 | B | | | | |
| 35 | A | | | | |
| 36 | B | | | | |
| 37 | A | | | | |
| 38 | B | | | | |
| 39 | A | | | | |
| 40 | B | | | | |

| | Arm A | Arm B | Gap |
|---|---|---|---|
| Links sent | | | |
| Reserved | | | |
| Reservation rate | | | |
| Fisher's exact p (one-sided) | | | |

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
