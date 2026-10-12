# Validation — Off-peak seat booking (version 0.1)

*Written before building. The feature is done only when every check below passes. Repeatable proof beats a plausible demo.*

## 1. Deterministic checks (rules that must always hold)
Run on the fixed reference data (task 1 in `plan.md`) after every change.

| # | Check | Expected result | Requirement |
|---|---|---|---|
| D1 | Book more seats than released | Extra booking refused; class shows full | R5 |
| D2 | Two goers book the last seat at the same moment | Exactly one booking succeeds | R5 |
| D3 | A member's phone number tries to book | No booking button; first-visit message shown | R2 |
| D4 | A new phone number books | Booking succeeds, no payment or package step | R2, R3 |
| D5 | Price shown to the goer | Equals the owner's entered price exactly; no discount anywhere | R1 |
| D6 | Owner withdraws seats with one already booked | Booked seat kept; only unbooked seats withdrawn | R1 |
| D7 | Confirmation content | Contains studio address, class time and cancellation rule | R4, R6 |
| D8 | Weekly summary | Released, booked, attended and "new" counts match a hand count | R8 |
| D9 | One goer's data visible to another goer | Never | Privacy |
| D10 | Keys, tokens or phone numbers in the repository | None found | Run rules |

## 2. Timed checks (measured on a real phone)
| # | Check | Pass |
|---|---|---|
| T1 | Confirmation message arrives after booking | Within 1 minute, 5 out of 5 attempts |
| T2 | Owner releases seats for a class | Under 2 minutes, first try, without help |
| T3 | New goer books from link to confirmation | Under 1 minute |

## 3. Agentic cases
None in this feature. Booking, seat counts, offer visibility and prices are rules only (`tech-stack.md`, AI Fit Decision). If any AI step is added later, it gets its own cases here with fixed settings and repeated runs.

## 4. Real-user check
| Check | Pass | Fail → next move |
|---|---|---|
| Pilot owner releases seats for one real off-peak class without help | Owner completes it and says they would do it again next week | Simplify release to a single WhatsApp message |
| Owner reviews the weekly summary | Owner can say how many attendees were new without asking us | Redesign the summary |
| At least 3 new goers book through the skeleton for the pilot owner's class, and the owner marks who came | 3 or more bookings, attendance recorded for each | Check whether the drop is at the link, the booking or the class. This is the first attendance data; Phase 2 measures it at scale |

Results go into `evidence-log/user-feedback.md`.

## 5. What must be trusted
- **No overbooking** (D1, D2): one failure would break owner trust immediately.
- **Regulars never see the offer** (D3): the whole "not a discount" promise depends on it.
- **Full price only** (D5): owners rejected discounting.

## Definition of Done
- All D checks pass on the reference data and again after the last change.
- All T checks pass on a real phone.
- One real-owner run completed and logged.
- `requirements.md` open questions answered or moved to the next feature.
- AI-assisted work for this feature logged in `ai-usage-log.md`.
