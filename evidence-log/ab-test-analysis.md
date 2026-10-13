# A/B Test — deeper analysis: how much should we trust +36 pp?

**Data:** `ab-test-results.md` (Arm A, no pack: 16/25 reserved; Arm B, 3-class pack: 7/25). **Pre-set rule:** ≥30 pp and one-sided Fisher p < 0.05 (`experiment-card.md`). Everything below was computed in Python (scipy, statsmodels) from those counts only. Nothing here changes the decision; it shows how sure we can be.

---

## 1. The headline, with uncertainty

| | Arm A (no pack) | Arm B (3-class pack) |
|---|---|---|
| Reserved | 16 of 25 | 7 of 25 |
| Rate | 64% | 28% |
| 95% interval (Wilson) | 45%–80% | 14%–48% |

| Measure | Value | Plain reading |
|---|---|---|
| Gap | **+36 pp** | Removing the pack more than doubled reservations |
| 95% interval for the gap (Newcombe) | **+8 pp to +57 pp** | Almost certainly positive; the true size could be modest or large |
| Relative lift | **2.3×** | No-pack people reserved 2.3 times as often |
| Fisher's exact, one-sided | **p = 0.011** | Under the pre-set 0.05 |
| Bayesian check (flat priors) | **P(A beats B) = 99%**; P(gap ≥ 30 pp) = 61%; P(gap ≥ 15 pp) = 92% | A beating B is near-certain. That the gap is **at least** 30 pp is only about 60% likely |

**Honest reading:** we are confident that removing the pack helps. We are **not** confident about **how much**. The pre-set rule was met, but a repeat of the test could plausibly land anywhere from about +10 to +55 pp.

## 2. How fragile is the result?

| If… | One-sided p | Still passes? |
|---|---|---|
| As observed | 0.011 | Yes |
| 1 Arm A reserver had declined | 0.023 | Yes |
| 2 Arm A reservers had declined | 0.042 | Yes, just |
| **3 Arm A reservers had declined** | **0.074** | **No** |
| 3 more Arm B people had reserved | 0.078 | No |

**Fragility index = 3.** Three people answering differently would have made the result inconclusive. That's normal for n = 50, but it's why the Phase 2 pilot must replicate the effect with real attendance before we scale anything (`specs/roadmap.md`, Phase 2; kill criteria in `build-decision.md` §5).

**Power:** if the true rates really are 64% and 28%, a 25-per-arm test would meet our rule about **68%** of the time. The test was big enough to detect a large effect, not a small one, as the experiment card said in advance.

## 3. What the decline reasons add

| Reason | Arm A (9 decliners) | Arm B (18 decliners) | Reading |
|---|---|---|---|
| Having to commit / buy a pack | 0 | **10** | Appears **only** where there was a pack: the mechanism behaves as predicted |
| Price + prefer my gym | 6 of 25 (24%) | 4 of 25 (16%) | Same in both arms (Fisher p = 0.73): price is a **steady background barrier**, not the cause of the gap |
| The time | 2 | 2 | Same in both arms: Tue 11:00 lost a few people either way |
| Don't know the coach | 1 | 1 | Minor in both |
| Not sure I'd get a spot | 0 | 1 | Minor, as expected when both arms promised confirmation |

**Strongest single piece of evidence in the repo:** the commitment reason is **0 in A and 10 in B**, while every other reason is flat across arms. The gap comes from the one thing we changed.

## 4. Threats to validity, and how serious each is

| Threat | Why it matters | How serious | What would fix it |
|---|---|---|---|
| Reservation ≠ attendance | A reservation cost nothing | **High** | Phase 2 pilot measures attendance and payment |
| Upfront cash and commitment move together | Arm B asked for 900 MAD up front vs. 300 MAD | Medium | Pilot variant: 3-class pack paid per visit |
| Alternating, not random, assignment | Order of contact could correlate with type of person | Low–medium | Randomise with a coin flip or a script next time |
| Personal networks | Friends of the team may be keener than strangers | Medium (affects both arms equally, so the **gap** is less affected than the **levels**) | Recruit through studios' own Instagram in the pilot |
| Fictional studio | No brand, reviews or location trust | Low for the gap (same in both arms) | Real studios in the pilot |
| Only one class and time | Tue 11:00 reformer only | Medium for generalising | Pilot covers several off-peak slots and two formats |

## 5. What this means for the presentation
- Say **"more than doubled"** and **"almost certainly positive"**, not "36% proven".
- Show the **0 vs. 10** commitment reasons: it's the clearest visual you have.
- Be first to say **"three people could have flipped it"**. That's why the next step is a pilot, not a scale-up.

*Reproduce:* `scipy.stats.fisher_exact([[16, 9], [7, 18]], alternative="greater")`; `statsmodels.stats.proportion.confint_proportions_2indep(16, 25, 7, 25, method="newcomb")`.
