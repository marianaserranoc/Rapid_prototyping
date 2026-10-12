# Tech Stack — version 0.1

*Evidence backs each need; the team chooses each tool. Not knowing yet is a decision to record, not hide.*

## Choices

| Layer | Current choice | Why (evidence or decision) | Status |
|---|---|---|---|
| Phase 0 test | A static two-version booking page on GitHub Pages (`booking-test/`), sending reservations to WhatsApp; one shared spreadsheet (Microsoft 365) to count them | Test the riskiest assumption before building anything (`experiment-card.md`) | **Done**: 16/25 vs. 7/25 (`ab-test-results.md`) |
| Goer surface | Mobile web page opened from a WhatsApp or Instagram link; no app to install | Goers discover on Instagram and book by DM (G2, G4); the A/B test ran on exactly this kind of page and 23 of 50 people reserved through it | **Decided** |
| Owner surface | Owner releases seats by WhatsApp message or a one-screen web form | Owners are solo operators who won't take on new admin; they check bookings on their phone (Owner A); Owner E refuses any app that fills his class without him | Decided: WhatsApp first. **TBD:** web form in Phase 1 |
| Build tool for the First Working Skeleton | One of Lovable, Bolt, v0, or VS Code with a coding agent | Course tools; pick by which produces a working booking flow fastest that the team can still read and change | **TBD** — decide at Session 16 |
| Data storage | A hosted database with row-level access (Supabase is the course default) | Need bookings, released seats and attendance in one place | **TBD** — decide with the build tool |
| Hosting | The build tool's hosting or GitHub Pages | Free; enough for a pilot | **TBD** |
| Payments | None. Goers pay at the studio, as they do today | Handling money adds legal and trust risk the test doesn't need | **Decided** |
| Confirmation | Instant message to the goer (WhatsApp in Phase 0, automatic in Phase 1) | Certainty of a place is a named barrier: G2 and G4 both gave up when a DM went unanswered | **Decided** |
| Interface language | French first; Arabic | Not yet asked of users | **TBD** — ask in next interviews |
| Personal data | First name and phone number only; consent at booking; deleted after the pilot | Morocco's personal-data law (Law 09-08, overseen by the CNDP) | Decided: minimise. **TBD:** confirm obligations |

## AI Fit Decision — where AI belongs and where it does not

| Step | Who does it | Why |
|---|---|---|
| Releasing seats, setting price and seat limit | **Owner (person)** | Owner control is a condition of adoption (Owners B, C, D, E) |
| Showing the offer only to new clients | **Code (rule)** | Must be exact: a regular seeing the offer turns it into a visible discount (Owners C, D, E) |
| Booking, seat count, confirmation | **Code (rule)** | Must never double-book or guess; deterministic and testable |
| Marking attendance | **Owner or studio staff (person)** | Only the studio knows who walked in |
| New vs. regular report | **Code (rule)** | A count, not a judgement |
| Drafting outreach and reminder messages | **AI, reviewed by a person** | Saves team time; a person approves every message before sending |
| Summarising interview notes and open feedback | **AI, verified against the notes** | Logged in `ai-usage-log.md` |
| Rehearsing persona reactions | **AI (Persona Agent)** | Rehearsal only, never evidence (`agents/persona-agent.md`) |

**Rule:** AI never touches price, seat release, booking, or who sees an offer. In the prototype, those are rules or people.

## Run rules
- One repository; specs in `specs/` are the source of truth for what gets built.
- No keys, tokens or phone numbers in Git; use the build tool's secret settings and keep `.env` out of the repo.
- Commit small, with a message saying which requirement it serves.
- Every phase ends with the checks in that feature's `validation.md` passing.
