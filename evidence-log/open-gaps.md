# Open Gaps and Experimental Limitations Log

> **Status:** Critical synthesis and methodological risk control document.
> **Project:** Off-peak capacity for independent boutique fitness studios in Casablanca and Rabat, Morocco.
> **Last reviewed:** 11 Oct 2026, before the Phase 1 gate.

This document gathers the business-model contradictions, experimental limitations and unvalidated gaps found so far. Each must be resolved, or consciously accepted, before committing to product development.

---

## Gap tracker

| # | Gap | Severity | Status | Next action | Linked to |
|---|---|---|---|---|---|
| 1 | Trial-then-vanish vs. trial-then-convert | High | Open | 4–6 week follow-up of pilot trial goers | `assumptions.md` 1.2, 3.1 |
| 2 | No result yet for the two-arm primary test | Critical | Running 11–13 Oct (reservations) | Log results in `experiment-card.md`; attendance moves to the Phase 2 pilot | `experiment-card.md`, `booking-test/` |
| 3 | No concurrent control in the card trials | Medium | Addressed by design | Primary test is two-arm; card trials kept as pre-test signals only | `oz-trials.md` |
| 4 | **Booking certainty vs. commitment risk** | High | **New, partly addressed** | Instant confirmation held constant in both arms of the primary test | `oz-trials.md` Persona 2 |
| 5 | Financial risk vs. instructor and quality trust | High | Open | Add an instructor-familiarity question to the post-test debrief | `oz-trials.md` Persona 1 |
| 6 | Undifferentiated goer segment | Medium | Open | Record segment (new, lapsed, current) for every test participant | `opportunity.md` |
| 7 | Modality and geography baseline | Medium | Open | Count real studios on Google Maps; record modality and capacity of each pilot studio in Phase 2 | `Fermi_estimate` |
| 8 | Acute push vs. learned resignation (owners) | Medium | Partly addressed | 3 real owners all rejected discounting but said yes to trying; check for resignation in 2–5 more interviews | `JTBD.md`, `gym_owners.md` |
| 9 | Owner operational bandwidth and control | High | Open | Seat-release walk-through with a real owner using their current tools | `assumptions.md` 2.3 |
| 10 | Owner sample below threshold | Medium | **New** | 3 of the 5–8 owners needed; 2–5 more interviews | `experiment-card.md` Layer 1 |
| 11 | AI-simulated responses in evidence files | Medium | **New, addressed** | Kept labelled and excluded from all counts | `gym_owners.md`, `ai-usage-log.md` |

---

## 1. Central contradiction: the one-off "sampler" vs. owner retention needs

There is an unresolved tension between what motivates the goer and what the owner needs to stay viable.

| Lens | Goer perspective | Owner perspective |
| :--- | :--- | :--- |
| **Primary motivation** | **A one-off patch:** attends another studio because their usual class was full or cancelled, to keep today's routine without committing. | **Predictability and retention:** needs recurring attendance to cover fixed monthly costs (rent and instructor pay). |
| **Behavioural outcome** | No reason to return weekly unless the same schedule clash happens again. | Wants to avoid "class tourists" who take cheap drop-in slots and never become full-price members. |

### Business model risk: trial-then-vanish vs. trial-then-convert
- **The vulnerability:** if the no-commitment offer only attracts people who come once and disappear, the model becomes a discounter or ClassPass-style aggregator. Owners resist aggregators because they devalue the brand, frustrate full-paying regulars and erode margins without building community.
- **Evidence status:** **unvalidated.** The card trials ([oz-trials.md](personas/selected_personas/oz-trials.md)) measured single-booking intent only. In the Persona 3 trial, 3 of 5 who would book said they'd "probably come back", but that is stated intent, not behaviour.
- **Required next test:** a 4–6 week follow-up of pilot trial goers, tracking whether each one books a second class at full price, buys a package, or vanishes. This is now the Measurable target in [goals.md](goals.md): at least 30% rebook at full price within 6 weeks.

---

## 2. Experimental design limitations

### A. No concurrent control in the card trials
- **Limitation:** the Persona 1 price test in [oz-trials.md](personas/selected_personas/oz-trials.md) had no control arm. The belief that goers reject 10-class packs came from one interview (G1 bought a 10-pack, used 5–6 classes and resolved never to prepay again). The card itself showed one gym-equivalent price, and 5 of 8 said they would book.
- **Resolution:** the primary test in [experiment-card.md](experiment-card.md) is now two-arm (no commitment vs. normal commitment) on the same class, price and visibility. The card trials are reported as pre-test signals, not evidence for the hypothesis.

### B. Primary test not yet run
- **Limitation:** the two-arm test (real class-goers in Casablanca and Rabat, large gap between arms) had no results logged, and the original recruitment deadline of 23 Sep passed with no contacts recorded.
- **Current status:** running 11–13 Oct 2026 as a reservation test through a two-version booking page (`booking-test/`). It measures reservations, not attendance, because the team cannot verify who shows up; attendance moves to the Phase 2 pilot with a real studio. Sample raised to 20 per arm (minimum 15) so a 30 pp gap is meaningful; if fewer than 15 per arm are reached, the result is reported as partial with the real n.

---

## 3. Open validation gaps

### Gap 4 (new): booking certainty vs. commitment risk
- **Context:** in the Persona 2 trial ([oz-trials.md](personas/selected_personas/oz-trials.md)), instant confirmation got 4 of 5 "I'd book it", while a refund guarantee got 2 of 5. Those who skipped the refund card said they worried about not knowing whether they had a place, not about losing money.
- **Why it matters:** this partly contradicts the riskiest assumption. If certainty matters more than risk removal, the product is an instant-booking tool, not a no-commitment trial.
- **What we did:** the primary test now holds instant confirmation constant in both arms, so only commitment risk differs. This rival hypothesis is logged in [assumptions.md](assumptions.md).

### Gap 5: financial risk vs. instructor and quality trust
- **Context:** in the Persona 1 card trial, one of the three who declined cited not knowing the instructor.
- **Open question:** is the main barrier financial commitment or quality uncertainty? These lead to different products: payment mechanics vs. instructor discovery and social proof.
- **Next action:** ask every primary-test participant in the debrief whether knowing the instructor would have changed their decision.

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
- **Evidence so far:** all 3 real owners ([gym_owners.md](personas/selected_personas/gym_owners.md)) rejected discounting but said they would try the concept. That suggests interest rather than resignation, but n=3 and stated intent only.

### Gap 9: operational bandwidth and owner control
- **Context:** real owner interviews ([gym_owners.md](personas/selected_personas/gym_owners.md)) stress full control over which seats open and no extra admin. Owner B made seat control a condition of saying yes.
- **Open question:** how can a solo operator release spare seats in real time without manual WhatsApp exchanges or disrupting their current scheduling tools?
- **Next action:** a seat-release walk-through with one real owner using the tools they use today. This is also the first input for the Stage 2 feature specification.

### Gap 10 (new): owner sample below threshold
- **Context:** Layer 1 in [experiment-card.md](experiment-card.md) needs 5–8 owners; 3 have been interviewed.
- **Next action:** 2–5 more owner interviews before Session 16. Until then, owner adoption is reported as directional only.

### Gap 11 (new): AI-simulated responses in evidence files
- **Context:** [gym_owners.md](personas/selected_personas/gym_owners.md) adds 2 AI-simulated responses per owner persona to 1 real response each.
- **Resolution:** simulated responses stay clearly labelled, are excluded from every count in [assumptions.md](assumptions.md) and [experiment-card.md](experiment-card.md), and are logged in [ai-usage-log.md](ai-usage-log.md).
