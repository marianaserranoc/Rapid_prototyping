# Size of the Prize — what empty off-peak seats are worth

**Question:** how much money sits in empty off-peak seats, and how much of it could Daba realistically help studios recover?
**Built from:** our own owner interviews (data no one else has), the Fermi estimate (`Fermi_estimate.md`) and the A/B reservation test (`ab-test-results.md`). Every number is labelled: **OURS** (from our interviews or test), **DESK** (public sources), or **ASSUME** (to be replaced with pilot data).

---

## 1. One quiet class, from what owners told us

| Owner | Quietest class | Seats filled | Empty seats | Empty value per class (at 300 MAD) | Source |
|---|---|---|---|---|---|
| A | Tue 11:00 | ~3 of 10 | ~7 | ~2,100 MAD | OURS |
| C | Fri 12:30 | 2–3 of 8 | 5–6 | 1,500–1,800 MAD | OURS |
| D | Weekday 11:00 and lunch | 3–4 of 8 | 4–5 | 1,200–1,500 MAD | OURS |
| E | Fri 12:30 | 2 (sometimes 3) of 8 | 5–6 | 1,500–1,800 MAD | OURS |
| *F (proxy, outside Morocco)* | *7, 8, 9 am* | *~1/5 of capacity* | *~80% empty* | *—* | *OURS, proxy* |

**Reading:** the quietest classes of the four owners who gave numbers (A, C, D, E) run at **about 30% full**, leaving **4–7 empty seats**. At 300 MAD (DESK: 250–400 MAD per reformer class), that's **1,200–2,100 MAD of unsold capacity per class, every week**, with the instructor paid anyway (A, D, E, F said so).

*Caveat:* owners named their **quietest** class, not their average off-peak class, so this is the top of the range.

## 2. All boutique studios in Casablanca and Rabat

| Input | Fermi base case | With our owner data | Status |
|---|---|---|---|
| Studios | 54 (43 Casablanca, 11 Rabat) | 54 | DESK, counted listings (likely an undercount) |
| Classes per studio per week | 20 | 20 | ASSUME |
| Off-peak share | 35% → 7 off-peak classes per studio | 35% | ASSUME |
| Empty seats per off-peak class | 4 | **4–6** (owners' quiet classes have 4–7) | ASSUME → partly OURS |
| Price per seat | 300 MAD | 300 MAD | DESK |
| **Empty seats per week** | **≈ 1,510** | **≈ 1,510–2,270** | DERIVED |
| **Unsold capacity per week** | **≈ 450,000 MAD** | **≈ 450,000–680,000 MAD** | DERIVED |
| **Per year (× 52)** | **≈ 23.5 M MAD** | **≈ 23.5–35 M MAD** | DERIVED |

This is the **total pool** of empty off-peak capacity, not revenue Daba can capture.

## 3. What one studio could recover

Product goal (`goals.md`): fill **2 extra seats per off-peak class**.

| | Per week | Per month (≈ 4.3 weeks) | Status |
|---|---|---|---|
| Off-peak classes | 7 | 30 | ASSUME (20 × 35%) |
| Extra seats filled (2 per class) | 14 | 60 | Target, not yet measured |
| **Extra revenue to the studio (at 300 MAD)** | **4,200 MAD** | **≈ 18,000 MAD** | DERIVED |
| Daba's share, *if* 15% commission per filled seat | 630 MAD | ≈ 2,700 MAD | **ASSUME**: the revenue model isn't decided (`specs/roadmap.md`, "Later") |

**Why owners might pay:** the studio keeps 85% of seats it was already paying an instructor to run empty. Nothing is discounted, so regulars see no reason to ask for a lower price (Owners A–E).

## 4. What Daba could realistically reach

| Scenario | Studios using Daba | Seats filled per week | Studio revenue per week | Daba revenue per year (at 15%, assumed) |
|---|---|---|---|---|
| Phase 2 pilot | 2–3 (starting with Owners D, E) | 28–42 | 8,400–12,600 MAD | — (learning, not earning) |
| Year 1 target | 10 (≈ 1 in 5 counted studios) | 140 | 42,000 MAD | ≈ 330,000 MAD |
| Both cities, mature | 25 (≈ half of counted studios) | 350 | 105,000 MAD | ≈ 820,000 MAD |

**Honest read:** in Casablanca and Rabat alone, this is a **solopreneur-scale business**, not a unicorn. The prize grows by:
- **More cities:** Marrakech, Tangier, and Salé/Témara around Rabat. The Fermi count covers the two city centres only.
- **More formats:** functional and Hyrox training (G8 in Casablanca couldn't book a single session; NOVA's founder named a Hyrox boom in Egypt), plus spin, barre and boxing, none of which are in the studio count.
- **The funnel signal:** in the A/B test, **64%** of people offered a no-pack class reserved, vs. **28%** with a pack. The Phase 2 pilot measures how many reservations turn into attendance. That rate decides how many people each released seat has to reach.

## 5. What would shrink the prize
- **Reservations don't turn into attendance.** Then the 64% is a ceiling, not a funnel.
- **Price.** 10 of 27 A/B decliners cited price or their gym, and proxy G6 says full price stops her.
- **Studios do it themselves.** Core Studio already sells a 3-class discovery pack. If studios add their own single-class option, Daba's value has to be **reach to new people and new-vs-regular tracking**, not the offer alone (`blue-ocean.md`).

## 6. Numbers to replace first
| Number | Replace with | When |
|---|---|---|
| Empty seats per off-peak class | One week of real attendance from Owners D and E | Phase 2 pilot |
| Off-peak share (35%) | The pilot studios' real timetables | Before Session 16 |
| 15% commission | What owners say is fair (`test-brief.md` §4, Q7) | Next owner conversations |
| 54 studios | A Google Maps count, without duplicates | Before Session 16 |
