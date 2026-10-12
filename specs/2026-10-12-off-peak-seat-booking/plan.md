# Plan — Off-peak seat booking (version 0.1)

*Tasks, in order. Each task names the requirement it serves. Build only what the requirements ask for.*

## Data the feature needs

| Record | Fields | Used by |
|---|---|---|
| Studio | name, address, owner phone, cancellation rule | R1, R4, R6 |
| Member list | studio, phone number | R2 |
| Released class | studio, date, start time, class type, instructor, price, seats released, status (open / full / withdrawn) | R1, R3, R5 |
| Booking | released class, goer first name, goer phone, booked at, confirmed at, status (booked / cancelled / attended / no-show) | R3–R8 |

Phone numbers are personal data: store only what's listed, never show one goer's number to another, and delete after the pilot (`tech-stack.md`).

## Tasks

| # | Task | Serves | Done when |
|---|---|---|---|
| 0 | Choose the build tool and data storage at Session 16; record the choice in `tech-stack.md` | — | `tech-stack.md` has no TBD for build tool or storage |
| 1 | Create the four records above with sample data for one studio | All | Sample studio, 3 members, 2 released classes exist |
| 2 | Owner screen: release seats for a class at a price they enter; withdraw unbooked seats | R1 | Owner releases and withdraws seats on a phone in under 2 minutes |
| 3 | Goer entry: phone number check against the member list | R2 | Member numbers are blocked from booking; new numbers continue |
| 4 | Goer booking page: class details, full price, cancellation rule, name + phone, one confirm tap | R3, R6 | Booking completes with no package or payment step |
| 5 | Seat counting that blocks bookings once seats run out | R5 | Two people booking the last seat at once: exactly one succeeds |
| 6 | Confirmation on screen and by message | R4 | Message arrives within 1 minute in a real test |
| 7 | Attendance marking after the class | R7 | Owner marks each booking from a phone |
| 8 | Weekly summary per released class | R8 | Numbers match a hand count from the bookings |
| 9 | Run every check in `validation.md`; fix and rerun until all pass | All | `validation.md` Definition of Done met |
| 10 | One end-to-end run with the pilot owner, observed | All | Notes added to `evidence-log/user-feedback.md` |

## Order and dependencies
Tasks 1 → 2 → 3 → 4 → 5 → 6 must come in order (each needs the previous one). Tasks 7 and 8 can run in parallel after task 4. Task 9 comes after all others; task 10 only after task 9 passes.

## AI use while building
A coding agent may write the code from this plan. Every agent session reads `AGENTS.md` and `specs/` first. Each meaningful AI-assisted episode is logged in `evidence-log/ai-usage-log.md`.
