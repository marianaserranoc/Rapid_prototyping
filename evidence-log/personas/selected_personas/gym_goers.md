## Persona 1: The Package-Wary Tryer

**Grounding status:** Grounded — interview G1, gap closed with WoZ trial (example)

### Behavioural archetype
A person who already pays for a default way to train (a gym membership) and occasionally tries boutique classes when a free window appears, but will not prepay a package before knowing a studio, weighing a single class against their already-paid default.

### Evidence boundary (final)

| Claim | Evidence status | Basis |
|---|---|---|
| Has a gym membership, trains 3–4×/week | REPORTED | G1 Q1–Q3 |
| Found the studio via a friend's IG post, messaged on WhatsApp | REPORTED | G1 Q4 |
| Free morning matched a slot; didn't book, went to gym instead | REPORTED | G1 Q4–Q5 |
| Didn't want a package before knowing the place | REPORTED | G1 Q6 |
| Single class felt expensive vs. the gym already paid for | REPORTED | G1 Q6 |
| Bought a 10-pack, used 5–6; now avoids prepaying | REPORTED | G1 Q9 |
| Instructor is the main reason to return | REPORTED (stated) | G1 Q10 |
| Price (not trust) was the primary blocker | SUPPORTED | oz-trial-persona1.md — 55% conversion when price matched gym-equivalent rate, holding trust constant |
| A gym-equivalent single-class price meaningfully increases booking | SUPPORTED |oz-trial-persona1.md, n=20, threshold met |
| This holds for non-gym-holders too | UNKNOWN | Trial only reached self-identified gym members — new gap, carried forward |

**Gap-closing summary:** the original open question ("was it commitment risk or price-vs-gym?") is resolved toward **price**, for this persona and this trial. New gap opened: untested for people without an existing gym membership to compare against.

---

## Persona 2: The Uncommitted Last-Minute Booker

**Grounding status:** Grounded — interview G2, gap closed with WoZ trial (example)

### Behavioural archetype
A young professional with an unpredictable schedule who discovers boutique fitness at short notice but hasn't committed to a studio, and — per the closed trial below — is driven more by booking friction than by regret-aversion.

### Evidence boundary (final)

| Claim | Evidence status | Basis |
|---|---|---|
| Unpredictable schedule; discovers free time at short notice | REPORTED | G2, direct quote |
| Uses Instagram to discover, DM/WhatsApp to book | REPORTED | G2, direct quote |
| Cancelled meeting → IG story → DM → no quick reply → abandoned | REPORTED | G2, recalled episode |
| Booking friction contributed to abandonment | SUPPORTED | Demonstrated by the episode itself |
| Stated main concern is wasting money, not price | REPORTED | G2, stated framing |
| Booking friction is the *dominant* factor, more than regret-aversion | SUPPORTED | oz-trial-persona2.md — Arm A (instant confirm) 64% vs. Arm B (refund guarantee) 38%, 26-point gap clears the pre-committed 15-point threshold |
| Combining instant confirmation + refund guarantee outperforms either alone | UNKNOWN | Not tested — natural next trial arm |

**Gap-closing summary:** original HYPOTHESIS ("regret/uncertainty-aversion is the dominant driver") is **downgraded** — the trial points to friction as primary, risk-aversion as secondary. This is a genuine reversal of the pre-trial assumption, not just a confirmation, and is worth flagging as the most important finding in this file: the cheapest fix (faster booking) may matter more than the mechanism the team originally set out to build (a refund guarantee).

---

## Persona 3: The Unanchored Sampler

**Grounding status:** Grounded — interview Example-G3, corroborated by WoZ trial (example). Previously hypothesis-only.

### Behavioural archetype
A studio-goer with flexible, non-habitual time and no fixed studio commitment. Hesitation centers specifically on package-vs-drop-in pricing at the booking step, not general distrust — and a low-commitment offer measurably increases both booking and short-term return rate.

### Evidence boundary (final)

| Claim | Evidence status | Basis |
|---|---|---|
| No fixed studio/package; moves between studios | REPORTED |G3 Q1 |
| Hesitates specifically at pack-vs-drop-in price, not distrust of the class | REPORTED, corroborated | Example-G3 Q4, observed in Q6 walk-through |
| Acceptable friction ceiling: phone number + one-tap confirm | REPORTED | G3 Q7 |
| A full-price-refund offer increases completed bookings for this slot | SUPPORTED | oz-trial.md — 15 bookings over 3 weeks vs. lower historical baseline |
| A meaningful share of trial bookers return within 21 days (47% vs. ~15% baseline) | SUPPORTED | oz-trial.md, pre-committed 40% threshold met |
| This generalizes beyond one studio/slot | HYPOTHESIS | n=15, one location |
| Whether returning bookers were new or already-regulars switching slots (cannibalization) | UNKNOWN | Not instrumented — new gap |

**Gap-closing summary:** "regret-aversion vs. timing/awareness vs. absence-of-demand" resolved toward pricing-at-the-booking-step. New gap opened: cannibalization, not yet measurable from goer-side data alone — needs owner-side booking records to check.

---

## Cross-persona synthesis (what closing all three gaps together tells you)

Three independent trials converge on the same headline: **across all three personas, price-and-friction at the booking moment outweighed the regret-aversion story the team started with.** Persona 1's trial isolated price; Persona 2's trial isolated friction vs. risk and friction won; Persona 3's trial confirmed price-at-checkout as the specific hesitation point. None of the three trials found strong evidence that fear of a *bad class experience* was the primary blocker — which was the original shared assumption across all three persona docs before any interview or trial ran.

**This is the most important thing to model for "the rest" reading this example:** the value of closing a validation gap isn't that it proves your original idea right — here, it mostly didn't. It's that you now know which lever (price visibility, booking speed) actually moves behavior, versus the one you originally planned to build (a trust/regret mechanism). A gap-closing exercise that just confirms the starting hypothesis every time should itself be treated with suspicion.

## Open gaps carried forward (not a failure state — expected)

| Gap | Owner |
|---|---|
| Does price-matching work for non-gym-holders? (Persona 1) | Goer-side, next trial |
| Does instant-confirm + refund guarantee combined outperform either alone? (Persona 2) | Goer-side, next trial |
| Are Persona 3's returning bookers new customers or regulars switching slots? (cannibalization) | Needs owner-side booking data — see owner persona files |

