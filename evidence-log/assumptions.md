# Assumptions

## Area 1: Goer demand behaviour
*Will goers actually book an off-peak class and come back?*

- Must be true: Goers who could attend an off-peak class avoid booking mainly because paying before they know a studio is worth it feels like an irreversible bet (regret-aversion), not because of timing or awareness
  - Evidence needed: We would need to observe a reservation rate at least 30 percentage points higher (Fisher's exact p < 0.05) for a no-commitment offer (one class, no pack) than for the identical class offered through a 3-class pack, from 40 regular boutique class-goers in Casablanca and Rabat (20 per arm, minimum 15; 25 per arm were reached), under a two-arm reservation test with the same class, studio and price per class (`booking-test/`). Attendance is checked later, in the Phase 2 pilot
- Must be true: Goers who try a class through a no-commitment entry come back at full price, rather than trying once and disappearing
  - Evidence needed: We would need to observe first-time trial attendees booking a second class at full price or buying a standard package within 4–6 weeks, from pilot studio booking records, under no discount
- Must be true: Goers have free time that actually overlaps with studios' off-peak slots
  - Evidence needed: We would need to observe goers reporting at least one weekly free window inside real off-peak class times, from goer interviews matched against actual studio schedules, under their current work or study routine

## Area 2: Owner adoption
*Will owners open their off-peak seats to this?*

- Must be true: Owners see a no-commitment single class, at a price they set, as genuinely different from the discounting they already reject
  - Evidence needed: We would need to observe owners choosing the no-commitment concept over a discount concept when shown both side by side, from real owner interviews in Casablanca and Rabat, under the same class, seat and price conditions
- Must be true: Owners are willing to sell single off-peak classes outside their packages without feeling it undercuts their memberships
  - Evidence needed: We would need to observe owners committing to list at least one recurring off-peak class for a pilot (a commitment, not stated interest), from studio owners we have already interviewed, under their own pricing and seat limits
- Must be true: Owners can release seats within their current manual workflow without admin they cannot absorb
  - Evidence needed: We would need to observe an owner completing a seat-release walk-through with the tools they use today (WhatsApp, spreadsheet or booking software) without needing new staff or software, from a live session with real owners, under a normal working week

## Area 3: Mechanism and economics
*Can this make money for owners and for the venture?*

- Must be true: The mechanism can tell a hesitant but genuine goer apart from someone repeatedly using the cheap entry point
  - Evidence needed: We would need to observe distinct booking patterns (trial then repeat at full price vs. repeated single trials only) in pilot usage data, under a pilot of at least 4 weeks
- Must be true: New bookings come from net-new attendees, not existing members downgrading to the single-class option
  - Evidence needed: We would need to observe existing members' package purchases and attendance staying stable before and after launch, from pilot studio records, under the same season and schedule
- Must be true: The cost of running the mechanism (commission, payouts, any refund guarantee) stays below the incremental revenue it brings each studio
  - Evidence needed: We would need to observe a positive margin per filled seat in a unit economics model built from real studio prices, class sizes and pilot fill rates, under the owners' current cost structure

## Riskiest assumption
**Before the test (11 Oct):** the riskiest assumption was that goers avoid booking mainly out of regret-aversion (Area 1, assumption 1). If it were false, a no-commitment mechanism would solve the wrong problem and owner adoption and economics would no longer matter. Our real evidence was thin: one goer's unused 10-class pack (G1).

**After the test (12 Oct):** the two-arm reservation test met the pre-set bar. **16 of 25 reserved one class with no pack vs. 7 of 25 for the same class as a 3-class pack (+36 pp, one-sided Fisher p = 0.011)**, and "having to commit / buy a pack" was the most common reason for not reserving (10 of 27). Assumption 1.1 is now **supported at reservation level**, though not yet at attendance level.

**New riskiest assumption: 1.2, trial goers come back at full price.** Three reasons:
1. A reservation is cheap; the pilot must show people actually turn up, pay and return.
2. Owners value a newcomer only if they become a regular (Owner D: one-off visitors have "little value"; Owners C, D and E all want new-vs-regular tracking).
3. Price is still a live barrier (10 of 27 declines were price or "prefer my gym"), and it bites hardest on the second, full-price visit.

---

## Why these three areas are MECE
Area 1 asks whether goers want it, Area 2 whether owners will supply seats, and Area 3 whether the exchange between them is economically viable. Each assumption belongs to exactly one side of the marketplace or to the money flowing between them, and together they cover demand, supply and viability.

## Evidence so far (real people only)

| Assumption | What we have | Status |
|---|---|---|
| 1.1 Regret-aversion is the main barrier | **A/B reservation test:** 16/25 vs. 7/25, +36 pp, p = 0.011; "having to commit" the top decline reason (10 of 27) (`ab-test-results.md`). **Interviews:** G1 (unused 10-pack), G4 (unused membership), G5 ("five up front is a different story") | **Supported at reservation level** (n=50, real action, fictional studio, no payment). Rival barriers remain: price (10 of 27 declines), certainty (G2, G4; held constant in the test) |
| 1.2 Trial goers come back | Nothing yet | **Untested: now the riskiest assumption** |
| 1.3 Free time overlaps off-peak | G1, G2, G4 describe unexpected free windows, not matched to schedules. 4 of 27 A/B decliners said the time (Tue 11:00) didn't work | Weak |
| 2.1 Seen as different from discounting | **5 of 5 real owners** reject discounting (A, B, C tried or avoided it; D, E ruled it out). D: "sounds better than a discount" | Directional, n=5, stated |
| 2.2 Willing to sell single classes | A yes, B yes if she controls seats, C yes, D yes (would test on a couple of classes), E "maybe" | **4 of 5** stated interest; **no commitment to a date yet** |
| 2.3 Fits current workflow | Owners insist on choosing seats themselves and on low admin; D and E only use Instagram today | Requirement known, not tested |
| 3.1 Separates genuine goers from gamers | Nothing | Untested |
| 3.2 No cannibalisation | Owners' condition that regulars never see the offer (B, C, D, E) | Requirement known, untested |
| 3.3 Unit economics positive | Fermi estimate of empty seats only (`Fermi_estimate.md`) | Untested |

AI-simulated owner responses in `gym_owners.md` and the illustrative card trials in `oz-trials.md` are excluded because they are not evidence.

## What changed, and what caused it (sprint feedback, 12 Oct)
The feedback asked us to keep examples as examples and only update grounding with what real people told us. This table separates the two.

| Change | Caused by real people? | Source |
|---|---|---|
| 1.1 status: "weak" → **supported at reservation level** | **Yes**: 50 real class-goers' reservations | A/B test |
| Riskiest assumption moved to 1.2 (return at full price) | **Yes** | A/B test; Owner D on one-off visitors |
| Booking certainty logged as a rival barrier; confirmation held constant in the test | **Yes** | G2, G4 |
| Trust-type barriers (not knowing the class, beginner nerves) added as a candidate | **Yes** | G5 |
| 2.1 and 2.2 extended from n=3 to n=5 | **Yes** | Owners D, E |
| "Price, not trust, is the main blocker" (earlier persona file) | **No, it came from an example card trial** | **Withdrawn** |
| "Instant confirmation beat a refund guarantee, 4 of 5 vs. 2 of 5" | **No, example card trial** | **Withdrawn**; certainty now rests on G2 and G4 |
| "Quality uncertainty: one declined WoZ respondent cited the instructor" | **No, example card trial** | **Withdrawn**; replaced by G5's real answer (below) |
| Persona 3 "grounded in Example-G3" | **No, example interview** | **Reverted to hypothesis** (`gym_goers.md`) |

## Candidate assumptions to discuss before the next iteration
- **Not knowing the class (new, real source):** G5 hesitates because Instagram doesn't show what a class is like and she's nervous about being the only beginner; 2 of 27 A/B decliners cited not knowing the coach. Is this a separate Area 1 assumption, or a rival to 1.1?
- **Price on the second visit:** price and "prefer my gym" were 10 of 27 A/B declines. Must be true: newcomers who try one class accept the studio's full price for the next one. This sits inside 1.2 but may need its own test.
- **Owner control over seats:** now a condition for 4 of 5 owners (B, C, D, E). This could become an explicit Area 2 assumption rather than sitting inside 2.3.
- **Team credibility (from the NOVA founder interview):** owners trust a new platform only when its team has visible credibility in the fitness world and long-term commitment. Evidence needed: owners agree to a pilot more often when an instructor or studio insider joins the outreach (`interview-nova-founder.md`).
- **Recurring vs. one-off commitment (same source):** NOVA's subscription failed but credit packages sold, which suggested only *recurring* commitment was the barrier. **Our test points the other way for first visits:** even a one-off 3-class pack cut reservations from 64% to 28%. A likely reason is that NOVA's credits work across many studios, while our pack locks the newcomer into one studio they don't know yet. Worth asking Aly in the follow-up.
