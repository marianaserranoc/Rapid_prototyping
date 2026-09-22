## Persona 1: The Package-Wary Tryer

**Grounding status:** Grounded — interview G1, gap closed with WoZ trial 

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
| Price (not trust) was the primary blocker | SUPPORTED (stated preference) | oz-trials.md, Persona 1 — shown a gym-equivalent-price card, 5 of 8 gym-holders said they'd book; the 3 who said no mostly cited the gym being already-paid, one cited not knowing the instructor |
| A gym-equivalent single-class price makes booking more likely | SUPPORTED (stated preference) | oz-trials.md, Persona 1 — 5/8 said yes on the card |
| This holds for non-gym-holders too | UNKNOWN | Only tested on self-identified gym members — new gap, carried forward |
| Trust/instructor familiarity may be a second, separate lever | UNKNOWN | One respondent's stated reason for declining — not designed into the card, so not properly tested |

**Gap-closing summary:** the original open question ("was it commitment risk or price-vs-gym?") leans toward **price**, based on stated responses to one card. New gap opened: one respondent's answer hinted trust/instructor-familiarity matters too, but the card wasn't built to test that separately.

---

## Persona 2: The Uncommitted Last-Minute Booker

**Grounding status:** Grounded — interview G2, gap closed with WoZ trial 

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
| Booking friction/certainty leans as the bigger factor, more than regret-aversion | SUPPORTED (stated preference) | oz-trials.md, Persona 2 — Card A (instant confirm) 4 of 5 said they'd book vs. Card B (refund guarantee) 2 of 5; those who declined Card B mostly said they wanted certainty the booking existed, not that they feared losing money |
| Combining instant confirmation + refund guarantee outperforms either alone | UNKNOWN | Not tested — natural next round |

**Gap-closing summary:** original HYPOTHESIS ("regret/uncertainty-aversion is the dominant driver") is **downgraded, not disproven** — a 4/5-vs-2/5 result on stated intent, with reasons pointing to certainty over financial risk. Worth flagging as the file's most useful finding: the cheapest fix (a visibly confirmed booking) may matter more than the mechanism the team originally set out to build (a refund guarantee) — though this is what people *said* they'd do, not what they actually did, and needs a bigger round before betting engineering time on it.

---

## Persona 3: The Unanchored Sampler

**Grounding status:** Grounded — interview Example-G3, corroborated by WoZ trial. Previously hypothesis-only.

### Behavioural archetype
A studio-goer with flexible, non-habitual time and no fixed studio commitment. Hesitation centers specifically on package-vs-drop-in pricing at the booking step, not general distrust — and a low-commitment offer measurably increases both booking and short-term return rate.

### Evidence boundary (final)

| Claim | Evidence status | Basis |
|---|---|---|
| No fixed studio/package; moves between studios | REPORTED | Example-G3 Q1 |
| Hesitates specifically at pack-vs-drop-in price, not distrust of the class | REPORTED, corroborated | Example-G3 Q4, observed in Q6 walk-through |
| Acceptable friction ceiling: phone number + one-tap confirm | REPORTED | Example-G3 Q7 |
| A full-price-refund offer increases stated willingness to book this slot | SUPPORTED (stated preference) | oz-trials.md, Persona 3 — 5 of 7 said they'd book when shown the card |
| Of those, a meaningful share say they'd return within 2 weeks | SUPPORTED (stated intent only) | oz-trials.md, Persona 3 — 3 of 5 who'd book also said they'd likely return; nobody in this test actually booked or returned for real |
| This generalizes beyond one studio/slot | HYPOTHESIS | n=7, stated preference only, one recruiting pool |
| How far the offer's terms (e.g., the 2-week return window) can tighten before it stops converting | UNKNOWN | Card tested whether the offer appeals at all, not its sensitivity to its own terms |
| Whether stated return intent matches actual return behavior | UNKNOWN | This method only captures what people say they'd do — needs a real, even manually-run booking to check |
| Whether returning bookers would be new or already-regulars switching slots (cannibalization) | UNKNOWN | Not instrumented — new gap |

**Gap-closing summary:** "regret-aversion vs. timing/awareness vs. absence-of-demand" leans toward pricing-at-the-booking-step, based on stated responses to one card. New gap opened: this whole round only measures intent, not behavior — the next step is making the offer real, even manually, to see if people follow through.

---

## Cross-persona synthesis (what closing all three gaps together tells you)

Three small card-based tests point the same direction: **across all three personas, price and booking certainty at the decision moment outweighed the regret-aversion story the team started with.** Persona 1's card isolated price; Persona 2's cards isolated certainty vs. risk-reduction, and certainty led; Persona 3's card showed the offer moving stated willingness to book. None of the three tests found strong evidence that fear of a *bad class experience* was the primary blocker — which was the original shared assumption across all three persona docs before any interview or test ran. Every sample here is tiny (5–8 people per test, one conversation each), so this is a shared directional lean, not a settled finding.

One limitation applies to all three and is worth stating plainly rather than glossing over: **this entire round measures what people say they'd do, not what they actually do.** Nobody in any of these tests booked a real class or came back for a second one — they looked at a card and answered a question. That's the right first move (fast, cheap, no engineering), but it's a weaker signal than real behavior, and the responsible next step is making at least one of these ideas bookable for real — even manually — before treating any of these leans as settled.

**This is the most important thing to model for "the rest" reading this example:** the value of closing a validation gap isn't that it proves your original idea right — here, it mostly didn't. It's that you now know which lever (price visibility, booking speed) actually moves behavior, versus the one you originally planned to build (a trust/regret mechanism). A gap-closing exercise that just confirms the starting hypothesis every time should itself be treated with suspicion.

## Open gaps carried forward (not a failure state — expected)

| Gap | Owner |
|---|---|
| Does price-matching work for non-gym-holders? (Persona 1) | Goer-side, next round |
| Does trust/instructor-familiarity matter as a separate lever from price? (Persona 1) | Goer-side, needs its own card design |
| Does instant-confirm + refund guarantee combined outperform either alone? (Persona 2) | Goer-side, next round |
| Does stated return intent match real return behavior? (Persona 3) | Needs a real, even manually-run booking — the single biggest open question across all three personas |
| Are Persona 3's stated "would return" bookers likely to be new customers or regulars switching slots? (cannibalization) | Needs owner-side booking data — see owner persona files |
