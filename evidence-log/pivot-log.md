# Pivot Log — how evidence changed our decisions

**Purpose:** one place showing the loop the course asks for: test → feedback → decision → pivot. Every row names the evidence that caused the change.
**Updated:** 12 Oct 2026 (A/B result, sprint feedback, 4 new real interviews).

---

## 1. Pivots so far

| # | What we believed | What showed us otherwise | What we changed | Evidence type |
|---|---|---|---|---|
| 1 | The venture would start in Egypt | [team to add the reason] | Moved the market to Morocco (Casablanca and Rabat) | [team to add] |
| 2 | Owners' problem is timing: off-peak classes sit at the wrong hour | Cross-review flagged the claim as unsupported; it couldn't be told apart from "nobody wants that slot" | Moved the riskiest assumption to the goer side: people won't commit before trying | AI critique, then team decision (`ai-usage-log.md`) |
| 3 | A single-group test would prove the assumption | A positive result couldn't separate commitment from timing or awareness | Two-group test: no-package vs. normal terms, same class | Team reasoning (`experiment-card.md`) |
| 4 | Any goer could get the trial offer | Owners B and C would only take part if they choose the seats and regulars never see the offer | **New clients only, owner picks the seats**; became the ERRC Create move | Real owner interviews (`user-feedback.md`) |
| 5 | Commitment is the main goer barrier | G2 gave up on a booking because nobody replied to her DM quickly (confirmed on 12 Oct by G4, who did the same). *An earlier version also cited a card trial (4 of 5 vs. 2 of 5); that trial was an illustrative example and was removed after sprint feedback.* | Instant confirmation held equal in both test groups; "certainty of a spot" named as a rival explanation | Real goer interviews (G2, G4) |
| 6 | The job starts when someone's usual class is full or cancelled | G1 and G2 both describe an unexpected free window instead | JTBD trigger changed to "unexpected free window" | Real goer interviews (`JTBD.md`) |
| 7 | One boutique class is a cheap way to try a studio | Desk research: one class (250–400 MAD) costs about a month of gym (~314 MAD) | Price added as a rival explanation; test uses full price in both groups so price can't explain a gap | Desk research (`market-alternatives.md`) |
| 8 | The test would measure attendance | The team can't verify who shows up at a studio this week | Test measures reservations through a booking page; attendance moves to the Phase 2 pilot | Practical constraint (`experiment-card.md`) |
| 9 | 5 people per group would be enough | One person changes the result by 20 pp, so even a 40 pp gap could be chance | 20 per group (minimum 15); threshold lowered to 30 pp with a significance check | Team reasoning, Fisher's exact test (`experiment-card.md`) |
| 10 | Card trials and "Example-G3" counted as pre-test evidence | Sprint feedback (12 Oct): they were illustrative examples, not real people. "Keep examples as examples" | Relabelled as examples in `oz-trials.md`; every claim that rested on them withdrawn or re-grounded in real interviews; Persona 3 reverted to hypothesis | Course feedback; evidence discipline |
| 11 | The goer job has one trigger: an unexpected free window | G5 has been postponing a **friend's invitation** to reformer for months: a different way into the same job | JTBD now has two circumstances: free window (G1, G2, G4) and friend's invitation (G5); friend-referral added as a Phase 2 channel | Real goer interview (G5) |
| 12 | Owners want more bookings | Owner D: a one-off visitor has "little value"; a newcomer who becomes a regular does. C, D and E all want to see who is new | Owner-facing metric is **newcomers who return**, not bookings; new-vs-regular tracking is core to Phase 1 | Real owner interviews (C, D, E) |
| 13 | Regret-aversion is the riskiest assumption | A/B test: 16/25 no-pack vs. 7/25 3-class pack, +36 pp, p = 0.011 | **Continue.** 1.1 supported at reservation level; riskiest assumption moves to 1.2 (trial goers return at full price) | Real behaviour, 50 class-goers (`ab-test-results.md`) |
| 10 | Owners would judge us on the offer alone | NOVA's founder: studios had seen similar ideas fail and only trusted NOVA because a co-founder is an instructor and the team was committed | Owner outreach will include a respected instructor or studio insider; team credibility added as a candidate assumption | Expert interview (`interview-nova-founder.md`) |
| 11 | Any prepayment is the barrier for goers | NOVA's subscription failed, but credit packages sold | We now distinguish recurring commitment (subscription) from a one-off pack; the Arm B result is read with this in mind | Expert interview (`interview-nova-founder.md`) |

---

## 2. Five Whys — why are off-peak seats empty?

| Why? | Answer | Source |
|---|---|---|
| 1. Why is Owner A's Tuesday 11:00 class at about 3 of 10? | Her regulars are at work at that time | Owner A (interview) |
| 2. Why doesn't she fill it with other people? | New people don't come without a low-risk reason to try | Hypothesis |
| 3. Why don't new people try? | They'd have to buy a pack first, aren't sure they'll get a spot, or find one class expensive next to their gym | G1, G2, G4, G5, price research; A/B test (pack was the top decline reason) |
| 4. Why don't studios just sell cheaper single classes? | It looks like a discount; regulars notice and want the same deal | Owners A–E |
| 5. Why is that a dead end today? | There's no way to sell a full-price single seat to newcomers only without regulars seeing it | **Root cause** |

The root cause is what the product addresses (`ERRC.md`, Create move). Steps 2 and 3 are the parts the reservation test checked: removing the pack lifted reservations by 36 pp (`ab-test-results.md`).

---

## 3. Pivots decided in advance (reservation test)

Written before results come in, so the evidence picks the direction, not us. Full rules in `experiment-card.md`.

| If the result is… | And the decline reasons say… | We will… |
|---|---|---|
| A reserves ≥30 pp more than B (p < 0.05) | — | **Continue:** pilot with 2–3 real studios and measure attendance and return |
| Gap under 15 pp | Mostly price or "prefer my gym" | **Pivot on price:** explore a new-clients-only first-visit price with owners |
| Gap under 15 pp | Mostly "not sure I'd get a spot" | **Pivot to certainty:** instant booking for studios' existing classes |
| Gap under 15 pp | Mostly "don't know the coach" | **Pivot to trust:** coach profiles, class videos, reviews |
| Almost no one reserves in either group | — | **Change the slot** and rerun before concluding |
| Gap of 15–29 pp, or ≥30 pp without p < 0.05 | — | **Extend** with 10 more people per group, then decide |

## 4. Result and decision
*Filled in 12 Oct 2026. Full table: `ab-test-results.md`.*

| | |
|---|---|
| Result | Arm A: **16 of 25** reserved (64%) · Arm B: **7 of 25** reserved (28%) · Gap: **+36 pp** · Fisher's p (one-sided): **0.011** |
| Top decline reasons | Having to commit / buy a pack 10 (all Arm B) · price 5 · prefer my gym 5 · the time 4 · don't know the coach 2 · not sure I'd get a spot 1 (27 non-reservers). Price and gym appear in both arms (A 6, B 4) |
| Branch triggered | **First row: A reserves ≥30 pp more than B with p < 0.05 → Continue.** None of the pivot branches fired |
| Decision | **Continue.** Keep one class with no pack as the newcomer offer. Phase 2 pilot with 2–3 real studios (Owners D and E approached first), real off-peak classes, measuring attendance and return at full price |
| What would change our mind next | Newcomers who reserve in the pilot mostly don't turn up and pay, or fewer than 30% rebook at full price. Then we'd take the **price branch** first, because price and "prefer my gym" were 10 of 27 declines, as many as commitment |
