# Goals

## Product Goal (long-term outcome)
- **Specific:** Run a no-commitment single-class booking mechanism with independent boutique fitness studios in Casablanca and Rabat, letting new goers book recurring off-peak classes at the price and seat limit each studio sets, without packages, memberships or discounts.
- **Measurable:** At each pilot studio, fill on average at least 2 of the empty seats per off-peak class compared with its pre-pilot baseline, with at least 30% of first-time trial goers booking again at full price or buying a package within 6 weeks, and no drop in existing members' package purchases. *(Targets proposed by the team, to be revisited once baselines are measured.)*
- **Achievable:** Start with 2–3 pilot studios that already fit the owner profile (independent, 15–25 classes a week), coordinated manually through WhatsApp and a shared booking sheet before any software is built.
- **Relevant:** Addresses the owner pain in `opportunity.md` (empty seats are lost revenue; discounting backfires) and tests the full assumption map in `assumptions.md`: goer demand (Area 1), owner adoption (Area 2) and economics (Area 3).
- **Time-bound:** Pilot live by Session 22 (first structured testing round) and results consolidated for the Phase 2 gate at Session 28 (1 Dec 2026).

## Sprint Goal (this cycle)
- **Specific:** Learn whether removing commitment risk (no package required, explicit no-obligation guarantee) produces a meaningfully higher off-peak booking-and-attendance rate than an identical, equally visible offer with normal commitment terms. This tests the riskiest assumption: goer regret-aversion, not timing or awareness, keeps off-peak seats empty (Area 1, assumption 1).
- **Measurable:** Gap in booking-and-attendance rate between Arm A (no commitment) and Arm B (normal commitment). Threshold set before testing: a gap of at least 40 percentage points supports the assumption; a gap under 20 points counts against it; anything in between is inconclusive and triggers a larger second round. See `experiment-card.md`.
- **Achievable:** A manual two-arm Wizard of Oz test with 10 regular boutique class attendees in Casablanca and Rabat (5 per arm), recruited through our Moroccan contact's WhatsApp network as set out in `recruitment.md`, plus the owner interviews already completed (`personas/selected_personas/gym_owners.md`). No software development.
- **Relevant:** Separates the regret-aversion hypothesis from the competing timing/awareness, absence-of-demand and quality-uncertainty hypotheses before any engineering investment. If it fails, the product goal above is withdrawn rather than built.
- **Time-bound:** Both arms run 11–13 Oct 2026, results logged in `experiment-card.md` before Group Project I on 13 Oct. If fewer than 5 people per arm are reached, the partial result is reported as such and the test is completed before Session 16 (First Working Skeleton kickoff).

---

## How these goals connect to the rest of the Venture Skeleton

| Step | File | What it says |
|---|---|---|
| Opportunity | `opportunity.md` | Owners lose money on empty off-peak seats; discounting backfires |
| Riskiest assumption | `assumptions.md` | Goers avoid booking out of regret-aversion |
| Sprint Goal | this file | Test that assumption with a two-arm WoZ test by 13 Oct |
| Experiment | `experiment-card.md` | Method, metric, threshold and decision rule |
| Decision | `experiment-card.md` results | Continue to pilot, pivot to a discovery or trust mechanism, or stop |
| Product Goal | this file | Only pursued if the sprint result supports the assumption |
