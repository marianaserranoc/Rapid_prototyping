# Roadmap — version 0.1

*Behaviours here, tasks in each feature's `plan.md`. Phase 0 and 1 in detail, later phases in outline. Each phase ends in validation, and a failed validation can stop or redirect the roadmap.*

## Phase 0 — Prove the barrier (now to Session 15)
**Behaviour:** a new goer opens a booking page for one off-peak class at full price and reserves a spot without buying a pack (or declines and says why).
**Built with:** a static two-version booking page on GitHub Pages (`booking-test/`), WhatsApp and a spreadsheet, run by the team. Attendance is not measured in this phase.
**Must pass:**
- Two-arm reservation test run with real class-goers (20 per arm, minimum 15) and results logged (`experiment-card.md`)
- Outcome read against the pre-set threshold (≥30 pp with p < 0.05 supports, under 15 pp counts against)
- Go / change / stop decision recorded at the Phase 1 gate

**Result (12 Oct): passed.** 25 per arm; Arm A 16/25 vs. Arm B 7/25, +36 pp, one-sided Fisher p = 0.011 (`evidence-log/ab-test-results.md`). Decision: continue to Phase 1.

**If it had failed:** commitment isn't the barrier. The decline reasons pick the pivot: price, certainty of a spot, or trust in the coach (`experiment-card.md`, decision rule).

## Phase 1 — First Working Skeleton: off-peak seat booking (Sessions 16–21)
**Behaviour:** an owner releases chosen off-peak seats; a new goer books one from a link with no package; the place is confirmed instantly; the studio marks who attended; the owner sees how many attendees were new.
**Feature spec:** `specs/2026-10-12-off-peak-seat-booking/`
**Must pass:** every check in that feature's `validation.md`, including no double bookings, regulars never seeing the offer, and one end-to-end run with a real owner.

## Phase 2 — First structured testing round (Sessions 22–23)
**Behaviour:** 2–3 pilot studios release real off-peak seats for two weeks; goers book through the skeleton. **Attendance and return visits are measured across studios.**
**Candidate studios:** Owners D and E, who both said they'd try it on a couple of classes (`user-feedback.md`). Phase 0 left two questions for this phase: do people who reserve actually attend and pay, and is price a barrier on the second visit?
**Must pass:** at least 2 extra attendees per released class on average; reservations convert to attendance; owners keep releasing seats after week one.

## Phase 3 — Harden and measure (Sessions 24–26)
**Outline:** no-show handling, reminders, privacy review, accessibility check, and repeat checks after every change.
**Must pass:** no regressions on Phase 1 checks; a risk review signed off.

## Phase 4 — Second testing round and return rate (Sessions 27–28)
**Outline:** measure whether trial goers book again at full price.
**Must pass:** at least 30% of trial goers rebook at full price. *Only about 5 weeks run from Session 22 to Session 28, so the 6-week return window in `goals.md` will be reported as partial at the Phase 2 gate.*

## Later (not before evidence)
Online payment, more studios and cities, owner self-service onboarding, revenue model (commission per filled seat vs. monthly fee). Each needs its own evidence first.

