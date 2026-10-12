# Open Gaps and Experimental Limitations Log

> **Status:** Critical synthesis and methodological risk control document.
> **Project:** Off-peak capacity for independent boutique fitness studios in Casablanca and Rabat, Morocco.
> **Last reviewed:** 12 Oct 2026, after the A/B test result and sprint feedback.

This document gathers the business-model contradictions, experimental limitations and unvalidated gaps found so far. Each must be resolved, or consciously accepted, before committing to product development.

---

## Gap tracker

| # | Gap | Severity | Status | Next action | Linked to |
|---|---|---|---|---|---|
| 1 | Trial-then-vanish vs. trial-then-convert | **Critical** | Open: **now the riskiest assumption** | Phase 2 pilot: track attendance, payment and a second full-price booking for every newcomer | `assumptions.md` 1.2, 3.1 |
| 2 | No result yet for the two-arm primary test | Critical | **Closed 12 Oct**: 16/25 vs. 7/25, +36 pp, p = 0.011 (Supports) | Attendance moves to the Phase 2 pilot | `ab-test-results.md`, `experiment-card.md` |
| 3 | No concurrent control in the card trials | — | **Closed: the card trials were illustrative examples, not evidence** (sprint feedback) | Nothing; the real test had a control arm | `oz-trials.md` |
| 4 | Booking certainty vs. commitment risk | High | Partly addressed | Commitment: answered at reservation level (A/B). Certainty: kept in the product (G2, G4); measure confirmation time vs. drop-outs in the pilot | `JTBD.md`, G2, G4 |
| 5 | Commitment vs. trust in the class (coach, beginner comfort, "what is it like?") | High | Open, **re-grounded in real evidence** | Test a short class video and coach profile on the pilot booking page; ask pilot bookers whether it mattered | G5; 2 of 27 A/B declines |
| 6 | Undifferentiated goer segment | Medium | Open | Record segment (new, lapsed, current) and gym membership for every pilot participant | `opportunity.md` |
| 7 | Modality and geography baseline | Medium | Open | Count real studios on Google Maps; record modality and capacity of each pilot studio | `Fermi_estimate.md` |
| 8 | Acute push vs. learned resignation (owners) | Medium | Partly addressed | 5 of 6 owners reject discounting; 5 of 6 open to the offer. Test whether any commits a real class | `JTBD.md`, `gym_owners.md` |
| 9 | Owner operational bandwidth and control | High | Open | Seat-release walk-through with Owner D or E using their current tools | `assumptions.md` 2.3 |
| 10 | Owner sample below threshold | Medium | **Partly closed**: 5 of the 5–8 owners | 1–3 more interviews; first commitments to a date | `experiment-card.md` Layer 1 |
| 11 | AI-simulated responses in evidence files | Medium | Addressed | Kept labelled and excluded from all counts | `gym_owners.md`, `ai-usage-log.md` |
| 12 | **Examples counted as evidence** | High | **New, addressed 12 Oct** | Card trials and Example-G3 relabelled; every dependent claim withdrawn or re-grounded (`assumptions.md`, "What changed") | `oz-trials.md`, `gym_goers.md` |
| 13 | **Price vs. commitment not fully separated** | High | **New, partly addressed**; G6 (13 Oct) names price as her main barrier | Split by arm: all 10 commitment declines in Arm B; price/gym in both arms (A 6, B 4). Still, Arm B asked for 900 MAD up front, so "won't commit" and "won't pay 900 at once" move together. Watch second-visit price in the pilot | `ab-test-results.md` |
| 14 | **Verify interview reports against recordings** | Medium | **Closed 13 Oct**: all recorded reports match their audio (`interviews/README.md`) | G4's episode closely mirrors G2's, and Owner E's quiet slot matches Owner C's (Fri 12:30, 2–3 of 8). Check both reports against the audio and log word-for-word quotes | `interviews/transcriptions/gym_goer_yassin_interview.md`, `interviews/transcriptions/gym-owner-rabat-yassin-interview.md` |

---

## 1. Central contradiction: the one-off "sampler" vs. owner retention needs

There is an unresolved tension between what motivates the goer and what the owner needs to stay viable.

| Lens | Goer perspective | Owner perspective |
| :--- | :--- | :--- |
| **Primary motivation** | **A one-off try:** uses an unexpected free window (G1, G2, G4) or finally accepts a friend's invitation (G5) to try a class without committing to a pack. | **Predictability and retention:** needs recurring attendance to cover fixed monthly costs (rent and instructor pay). |
| **Behavioural outcome** | No reason to return weekly unless the same schedule clash happens again. | Wants to avoid "class tourists" who take cheap drop-in slots and never become full-price members. |

### Business model risk: trial-then-vanish vs. trial-then-convert
- **The vulnerability:** if the no-commitment offer only attracts people who come once and disappear, the model becomes a discounter or ClassPass-style aggregator. Owners resist aggregators because they devalue the brand, frustrate full-paying regulars and erode margins without building community.
- **Evidence status:** **unvalidated, and now the riskiest assumption.** The A/B test showed newcomers reserve far more readily without a pack (64% vs. 28%), but it says nothing about whether they come back. Owner D was explicit: a one-off visitor has little value; a newcomer who becomes a regular is valuable. *(An earlier version cited a card trial's "3 of 5 would come back"; that was an illustrative example and has been removed.)*
- **Required next test:** a 4–6 week follow-up of pilot trial goers, tracking whether each one books a second class at full price, buys a package, or vanishes. This is now the Measurable target in [goals.md](goals.md): at least 30% rebook at full price within 6 weeks.

---

## 2. Experimental design limitations

### A. No concurrent control in the card trials (closed)
- The card trials in [oz-trials.md](personas/selected_personas/oz-trials.md) were an illustrative example, not real data, so this limitation no longer applies to our evidence. The real primary test had a same-page control arm.

### B. Primary test (closed 12 Oct)
- **Result:** 25 per arm. Arm A (no pack) 16/25, Arm B (3-class pack) 7/25, +36 pp, one-sided Fisher p = 0.011: above the pre-set bar ([ab-test-results.md](ab-test-results.md)).
- **Limits that remain:** reservations, not attendance; fictional studio; no payment; participants from the team's networks; alternating, not random, assignment; commitment and upfront cash not separated (Gap 13).

---

## 3. Open validation gaps

### Gap 4: booking certainty vs. commitment risk
- **Real evidence:** G2 and G4 both lost a booking because nobody replied to their DM quickly; G4 says instant confirmation matters more to him than not buying a pack. *(The card trial previously cited here was an illustrative example and has been removed.)*
- **What we did:** the A/B test held instant confirmation constant in both arms, so its +36 pp gap is about commitment, not certainty. Only 1 of 27 decliners cited certainty, as expected when it's promised in both arms.
- **Still open:** how much certainty adds on top of no-pack. **Next:** in the pilot, log time-to-confirmation and drop-outs.

### Gap 5: commitment vs. trust in the class
- **Real evidence:** G5 hesitates because Instagram doesn't show what the class is like, and she's nervous about being the only beginner; G1 says the instructor is the main reason to return; 2 of 27 A/B decliners said they didn't know the coach. *(The earlier card-trial evidence for this gap was an illustrative example and has been removed.)*
- **Open question:** does trust in the class block people *after* the pack is removed? These lead to different features: payment terms vs. class videos, coach profiles and bringing a friend.
- **Next action:** add a short class video and coach profile to the pilot booking page, and ask every pilot booker whether it mattered.

### Gap 6: undifferentiated goer segment
- **Context:** [opportunity.md](opportunity.md) still treats the goer as one segment.
- **Open question:** barriers likely differ across:
  1. *Net-new prospects:* never visited the studio (high trust barrier).
  2. *Lapsed members:* attended before but stopped (a specific dropout reason).
  3. *Current peak-hour regulars:* active members who avoid off-peak slots (schedule rigidity or habit).
- **Next action:** record each participant's segment in the [recruitment.md](recruitment.md) log so results can be split later, even if the sample is too small to compare now.

### Gap 7: modality and geography baseline
- **Context:** the opportunity assumes the same studio economics across disciplines and cities.
- **Open questions:**
  - Low-capacity, high-touch formats (reformer pilates, 6–10 beds) have very different margins from high-capacity ones (HIIT or spin, 25+ spots).
  - The market size in [Fermi_estimate](Fermi_estimate) relies on an unverified 1 boutique studio per 50,000 residents in Casablanca and Rabat.
- **Next action:** anchor the Fermi estimate with a real count of boutique studios from Google Maps; record each pilot studio's modality and capacity in Phase 2. The reservation test uses reformer pilates (8 reformers), so its result speaks to that modality only.

### Gap 8: acute push vs. learned resignation (owners)
- **Context:** [JTBD.md](JTBD.md) frames the owner's pain as an urgent push.
- **Open question:** after repeated failures with discounting, have owners accepted empty off-peak classes as normal? If so, adoption means overcoming deep scepticism, not just offering a better tool.
- **New (expert evidence):** NOVA's founder said Egyptian studios had seen similar ideas before that never came to anything, and only trusted NOVA because a co-founder is an instructor and the team was visibly committed ([interview-nova-founder.md](interview-nova-founder.md)). So owner scepticism is real, but it can be overcome by credibility, not only by a better offer.
- **Evidence so far:** all 5 real owners ([gym_owners.md](personas/selected_personas/gym_owners.md)) reject discounting; 4 say they would try the concept and Owner E says "maybe". Owner E's case is closest to resignation: he keeps a 2-of-8 class running for 2 regulars and has only tried Instagram posts. Still stated intent only; the real test is whether an owner commits a class to the pilot.

### Gap 9: operational bandwidth and owner control
- **Context:** real owner interviews ([gym_owners.md](personas/selected_personas/gym_owners.md)) stress full control over which seats open and no extra admin. Owners B, C, D and E made seat control a condition of saying yes; Owner E: if an app filled his class without him, he isn't interested.
- **Open question:** how can a solo operator release spare seats in real time without manual WhatsApp exchanges or disrupting their current scheduling tools?
- **Next action:** a seat-release walk-through with Owner D or E using the tools they use today. This is also the first input for the feature specification.

### Gap 10: owner sample below threshold
- **Context:** Layer 1 in [experiment-card.md](experiment-card.md) needs 5–8 owners; 5 have now been interviewed (Owners D and E added 12 Oct). 4 of 5 clear the stated-willingness bar.
- **Next action:** 1–3 more interviews, and above all a commitment to a real class on a real date. Until then, owner adoption is reported as directional only.

### Gap 11: AI-simulated responses in evidence files
- **Context:** [gym_owners.md](personas/selected_personas/gym_owners.md) adds 2 AI-simulated responses per owner persona to 1 real response each.
- **Resolution:** simulated responses stay clearly labelled, are excluded from every count in [assumptions.md](assumptions.md) and [experiment-card.md](experiment-card.md), and are logged in [ai-usage-log.md](ai-usage-log.md).

### Gap 12 (new): examples counted as evidence
- **Context:** sprint feedback (12 Oct) pointed out that the card trials and "Example-G3" were illustrative examples, yet several files used them as grounding.
- **Resolution:** `oz-trials.md` now opens with an "illustrative example, not evidence" notice; every dependent claim is withdrawn or re-grounded in real interviews and the A/B test; Persona 3 is back to a hypothesis. The full list of changes is in [assumptions.md](assumptions.md), "What changed, and what caused it".

### Gap 13 (new): price vs. commitment not fully separated
- **Context:** both arms charged 300 MAD per class, but Arm B asked for 900 MAD up front. "Having to commit" (10) and "price / prefer my gym" (10) were equally common reasons for not reserving.
- **Real interview (13 Oct):** G6 says one Pilates class at full price is "very expensive" and she'd only try it if cheaper as a trial ([mariana-interviews.md](interviews/transcriptions/mariana-interviews.md)). This is the clearest real case for the price rival.
- **Split by arm (done):** all 10 commitment declines are in Arm B; price and gym declines appear in both arms (A 6, B 4), so price is a steady barrier that doesn't explain the gap ([ab-test-results.md](ab-test-results.md)).
- **Next action:** in the pilot, check whether newcomers accept full price on their **second** visit, and offer a 3-class pack at 300 MAD paid per visit to separate commitment from upfront cash.

### Gap 14 (new): verify interview reports against recordings
- **Context:** the reports for G4 and Owner E were written from audio. G4's episode is almost identical to G2's (cancelled meeting → Instagram story → DM → no reply → gave up), and Owner E's quiet slot matches Owner C's (Fri 12:30, 2–3 of 8).
- **Why it matters:** similar stories are possible, but evaluators will check. A report that drifts towards earlier notes would weaken the evidence.
- **Resolved (13 Oct):** every recorded interview was transcribed automatically and compared with its report. G4's and Owner E's reports match their recordings almost word for word, so the similarity to G2 and Owner C is a real coincidence, not drift. Next step: add 2–3 timestamped quotes to each report.
