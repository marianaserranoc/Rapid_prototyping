# Requirements — Off-peak seat booking (version 0.1)

**Feature:** an owner releases chosen off-peak seats to new clients; a new goer books one with no package and gets an instant confirmation; the studio marks attendance; the owner sees new vs. regular attendees.
**Roadmap phase:** Phase 1, First Working Skeleton (Sessions 16–21).
**Tests these assumptions:** 1.1 regret-aversion, 2.1 seen as different from discounting, 2.3 fits owner workflow (`assumptions.md`).

## Why this feature first
It is the thinnest flow that touches both sides of the market and every ERRC move: full price (Eliminate), one class with no package (Reduce), instant confirmation (Raise), and owner-controlled seats for new clients only (Create).

---

## User stories and acceptance criteria

### R1 — Owner releases seats
*As an owner, I want to choose which off-peak seats to release, so that I stay in control of my schedule.*
- Owner selects a class (day, time, type, instructor) and a number of seats.
- Price is the studio's normal single-class price, entered by the owner; the system never suggests or applies a lower price.
- Owner can withdraw unbooked seats at any time.
- **Source:** Owners B, C (control as a condition).

### R2 — Offer is shown only to new clients
*As an owner, I want regulars not to see this offer, so that it never looks like a discount.*
- A goer enters a phone number before seeing booking options.
- If that number is on the studio's list of current members, the goer is told the class is for first-time visitors and is not shown the booking button.
- Owner can add or remove numbers from the member list.
- **Source:** Owner C ("if regulars can see or get the same offer, it feels like a discount"); Owners D and E (regulars must never see it as a special deal).

### R3 — Goer books one class with no package
*As a goer with a free window, I want to book one class without buying a pack, so that I can try the studio first.*
- Goer sees class, time, studio, instructor name and full price.
- Booking needs first name and phone number only, plus one tap to confirm.
- No package, membership or payment is requested. Payment is made at the studio.
- **Source:** G1, G4, G5 (avoid prepaying a pack); A/B reservation test (no pack: 16/25 reserved vs. 7/25 with a 3-class pack); `tech-stack.md`.

### R4 — Instant confirmation
*As a goer, I want to know straight away that I have a place, so that I can plan around it.*
- Confirmation is shown on screen and sent by message within 1 minute of booking.
- Confirmation includes studio address, time and cancellation terms.
- **Source:** G2's and G4's abandoned DM bookings.

### R5 — No overbooking
- Bookings for a class can never exceed the seats the owner released.
- When the last seat is taken, the class shows as full immediately.

### R6 — Cancellation terms are stated, not hidden
- The goer sees the cancellation rule before confirming. *Default to decide with the pilot owner, e.g. free cancellation up to 3 hours before.*
- **Source:** cancellation penalties are part of the commitment barrier (`Fermi_estimate.md`).

### R7 — Studio marks attendance
- After the class, the owner or staff marks each booking as attended or no-show, from a phone.

### R8 — Owner sees new vs. regular attendees
- A weekly summary per released class shows seats released, booked, attended, and how many attendees were new.
- **Source:** Owners C, D and E want this and none track it today; Owner D values a newcomer only if they come back.

---

## Out of scope for this feature
- Online payment, refunds or deposits
- Any discount, promo code or dynamic price
- Multiple studios in one booking flow, credits or subscriptions
- Reminders and automated no-show follow-up (Phase 3)
- Any AI in booking, pricing or offer visibility (`tech-stack.md`, AI Fit Decision)

## Open questions
- Interface language: French only, or French and Arabic?
- Who maintains the member list in R2: the owner, or a one-time import from the studio's booking tool?
- Cancellation default (R6): agree with the pilot owner.
