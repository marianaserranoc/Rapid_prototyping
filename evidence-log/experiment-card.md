# Experiment Card

## How this card evolved
Earlier versions were replaced, not deleted from our thinking. Each change was triggered by something specific. Details of each step are in `ai-usage-log.md` and `pivot-log.md`; earlier file versions are in the repository's commit history.

| Version | What we planned to test | Method and threshold | Why we changed it |
|---|---|---|---|
| v1 | Goers have elastic routines and will move to off-peak slots given a non-price nudge (priority access + social matching) | Concierge: manual WhatsApp nudges to 5 people; ≥3 of 5 book and attend | The insight moved from timing to regret-aversion; a single group also couldn't tell which explanation caused a positive result |
| v2 | Goers avoid off-peak classes out of regret-aversion | Single-group Wizard of Oz with a low-commitment offer | One group can't separate regret-aversion from timing or awareness |
| v3 | Same, with a control | Two groups (low-commitment vs. normal terms, same visibility), 5 each; book-and-attend gap ≥40 pp; plus three supporting layers | Real goer G2 gave up on a booking because nobody replied to her DM quickly, so booking certainty could explain any gap. *(An earlier version of this row cited a card trial; that trial was an illustrative example, not real data, and is no longer used as evidence. See `oz-trials.md`.)* |
| v4 | Same, controlling for certainty | Instant confirmation promised in both groups | The team can't verify who attends a class this week |
| v5 | Same | Two-version booking page (`booking-test/`), 5 per arm; reservation-rate gap ≥40 pp; decline reasons pick the pivot | With 5 per arm, one person moves the result by 20 pp, so even a 40 pp gap could be chance |
| v6 | Same | Same page, 20 per arm (minimum 15, recruit 25); gap ≥30 pp with Fisher's exact p < 0.05 | Ran 11–12 Oct 2026. A second real goer (Youssef, Rabat, 12 Oct) described the same slow-DM drop-out as G2, which confirmed that holding confirmation constant was the right control |
| **Result** | — | **25 per arm. Arm A 16/25 (64%), Arm B 7/25 (28%), gap +36 pp, one-sided Fisher p = 0.011** | **Threshold met: Supports. Decision: Continue to the Phase 2 pilot (attendance and return)** |

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
- **Confirmation:** the same "spot confirmed within minutes" promise in both arms, so booking certainty cannot explain a difference (G2 and Youssef both dropped out over slow replies; see pre-test signals below).
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
Only real people count here. The card trials in `personas/selected_personas/oz-trials.md` were an **illustrative example** of the method and are **not evidence**, so they no longer appear in this table (sprint feedback, 12 Oct).

| Who (real) | What they told us | What it suggested for the test design |
|---|---|---|
| G1 (goer, interview) | Bought a 10-pack and used 5–6; won't prepay before knowing a studio; one class felt expensive next to her paid gym | Commitment **and** price are both possible barriers, so the test keeps price per class identical (300 MAD) in both arms |
| G2 (goer, interview) | Meeting cancelled → studio's Instagram story → DM → no quick reply → gave up | **Certainty of a spot is a rival explanation**, so instant confirmation is promised in both arms |
| Youssef (goer, Rabat, 12 Oct) | Same pattern as G2: DM, no reply for ~40 min, gave up. Says instant confirmation matters more than no pack | Second real case for the certainty rival; confirmation stays constant |
| Goer interviewed by Khaled (12 Oct) | Has never bought a pack; "five classes up front is a different story"; would "probably" book one class at full price if a friend invited her | Supports the commitment barrier in her own words; adds beginner nerves and "Instagram doesn't show the class" as trust-type barriers |

**What this meant before the test:** two of four real goers (G2, Youssef) dropped out over slow confirmation, not commitment. That is why both arms promise the same "confirmed within minutes", so certainty cannot explain a difference between them. The rival is also logged in `assumptions.md`.

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
| Owner D (interviewed by Khaled, 12 Oct; `Khaled-gym-owner-interview.md`) | Recorded call | Yes: "sounds better than a discount" | Yes, conditionally: he picks the classes and seats, regulars don't see a deal, he learns whether newcomers return. Willing to test on "a couple of classes" |
| Owner E, Karim (Rabat, yoga and mobility, interviewed by Yassin, 12 Oct; `gym-owner-rabat-yassin-interview.md`) | Zoom | Yes: refuses to lower prices because regulars would expect it | **"Maybe"**, only if he chooses the class and number of spots and regulars never see it |

**4 of 5 real owners (80%) distinguish the offer from discounting and say they would offer it; the fifth says "maybe".** This clears the ≥60% bar on the minimum sample of 5, but it is **stated willingness only**: no owner has yet committed a specific class on a specific date, which is our bar for adoption (`test-brief.md` §4). The same three conditions came up in 4 of 5 interviews: the owner chooses the seats, regulars never see the offer, and the owner can see who is new.
**Next:** ask Owners D and E (both open to a trial, and E agreed to a WhatsApp follow-up) to commit one real off-peak class for the Phase 2 pilot. Owner D's city and studio type are still to be confirmed. The AI-simulated owner responses in `gym_owners.md` are excluded because they are not evidence.

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
Four real goer interviews (G1, G2, Youssef, and the goer interviewed by Khaled). Barriers outside our original three hypotheses:
- **Booking certainty** (G2, Youssef): two interviews. This met the "2 or more" trigger, so the primary test was redesigned and instant confirmation is now held constant in both arms.
- **Beginner nerves and not knowing what the class is like** (Khaled's goer: "uncomfortable if everyone already knows what they're doing"; "Instagram doesn't show the experience"): one interview. Not controlled in the test; logged in `open-gaps.md` Gap 5.

*An earlier version listed "not knowing the instructor" from a card trial. That trial was illustrative, not real, so it has been removed as evidence.*

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
- **Status:** open gap for conversion. **Comparison after the test:** Arm A's 64% reservation rate is not a dramatic outlier next to the US benchmark (paid intro offers converting at 50–60%), but the two measure different steps (reserving a fictional class vs. paying for a real one), so this counts as **plausible, not confirmed**. The Phase 2 pilot is where attendance and paid conversion get measured for real.

---

## Results and decision (primary test)
**Ran:** 11–12 Oct 2026 through `booking-test/`. **Recruited:** 25 per arm (above the 20-per-arm target). Per-participant log (codes only): `ab-test-results.md`. Raw WhatsApp messages and voice notes stay in the team's Teams folder.

| | Arm A: 1 class, no pack | Arm B: 3-class pack | Gap |
|---|---|---|---|
| Links sent | 25 | 25 | |
| Reserved ("I'M RESERVING") | **16** | **7** | |
| Did not reserve | 9 | 18 | |
| Reservation rate | **64%** | **28%** | **+36 pp** |
| Fisher's exact p (one-sided) | | | **0.011** |

**Why people did not reserve** (27 non-reservers, main reason each, both arms together):

| Reason | Arm A | Arm B | Total | Rival it speaks to |
|---|---|---|---|---|
| Having to commit / buy a pack | 0 | 10 | 10 | Our assumption (regret-aversion) |
| Price | 3 | 2 | 5 | Price rival |
| Prefer my gym | 3 | 2 | 5 | Price rival (already-paid alternative) |
| The time | 2 | 2 | 4 | No demand for that slot |
| Don't know the coach | 1 | 1 | 2 | Trust rival |
| Not sure I'd get a spot | 0 | 1 | 1 | Certainty rival (held constant by design) |
| **Total** | **9** | **18** | **27** | |

All 10 commitment declines came from Arm B, the only arm with a pack. Price and gym declines appear in both arms at similar levels (A 6, B 4). Voice notes: 29 of 50. Quotes: [team to add 2–3 short lines, word for word, from real voice notes].

**Outcome against threshold:** **Supports.** The gap (+36 pp) is above the 30 pp bar and p = 0.011 is below 0.05, both set before the test.

**Decision:** **CONTINUE.** Keep one class with no pack as the core newcomer offer. Next is the Phase 2 pilot: 2–3 real studios (starting with Owners D and E, who were open to a trial), real off-peak classes, measuring **attendance and return at full price** (`specs/roadmap.md`).

**How to read it honestly**
- **What it shows:** with price per class, studio, coach, time and confirmation held the same, removing the pack more than doubled reservations. "Having to commit / buy a pack" was also the most common reason for not reserving. Both point the same way: commitment is a real barrier.
- **What it doesn't settle:**
  - **Price is still in play, but it doesn't explain the gap.** "Price" and "prefer my gym" (10 of 27) appear in both arms at similar levels (A 6, B 4), while all 10 commitment declines are in Arm B. Price is a separate, steady barrier; the pilot must check whether people who reserved actually pay 300 MAD and come.
  - **Commitment and upfront cash move together.** Arm B asked for 900 MAD up front vs. 300 MAD, so we can't separate "won't commit to three classes" from "won't pay 900 MAD at once". Either way, the no-pack offer removes both.
  - **Certainty wasn't tested.** Only 1 person cited it, but that was by design: both arms promised instant confirmation. Real goers G2 and Youssef still show slow DMs lose bookings, so instant confirmation stays in the product (ERRC Raise).
  - **Reservation is not attendance**, the studio was fictional, nothing was paid, and participants came from the team's networks with alternating, not random, assignment.

**What would change our mind:** in the Phase 2 pilot, if newcomers who reserve a no-pack seat mostly don't turn up and pay the full price (roadmap: "reservations convert to attendance"), or fewer than 30% rebook at full price (Phase 4), then a reservation was cheap talk and commitment was not the whole barrier. We would then revisit price first, since it was the second most common reason (`pivot-log.md` §3).

---

## How the layers relate
- **Primary test** checks the mechanism itself: does removing commitment risk change real booking behaviour.
- **Layer 1** checks a separate risk, owner adoption, that no goer test can substitute for.
- **Layer 2** checks whether the primary test is asking the right question; it caused one redesign (confirmation held constant).
- **Layer 3** checks whether the result could plausibly hold at market level.

None of these alone shows the venture will work. Together they cover mechanism, adoption, sample validity and market plausibility, which is the most a Phase 1 validation can realistically deliver before building starts.
