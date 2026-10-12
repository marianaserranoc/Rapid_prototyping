# Fermi Estimate — Underfilled Off-Peak Seats per Week (Casablanca & Rabat)

**What this answers:** roughly how many off-peak class seats go unfilled each week across boutique fitness studios in Casablanca and Rabat, what they are worth, and how many a single pilot studio could offer.

**Format:** known anchors, several assumptions, one derived number you can challenge — the same structure as the course's piano-tuner example. **Version 2 (11 Oct 2026):** the population and studio-count assumptions from version 1 have been replaced with sourced figures.

---

## Assumption chain

| Step | Input | Status | Value used | Source |
|---|---|---|---|---|
| 1 | Casablanca population | **KNOWN** | 3,218,036 | 2024 census (RGPH, HCP), city |
| 1 | Rabat population | **KNOWN** | 515,619 | 2024 census (RGPH, HCP), city |
| 2 | Boutique studios, Casablanca | **COUNTED** | 43 (18 yoga, 13 pilates, 12 boxing) | poidata.io listings, Aug 2025 |
| 2 | Boutique studios, Rabat | **COUNTED** | 11 (8 yoga, 1 pilates, 2 boxing) | poidata.io listings, Aug 2025 |
| 3 | Classes per studio per week | ASSUME | 20 | Owner profile in `opportunity.md` (15–25); not published by studios |
| 4 | Off-peak share of classes | ASSUME | 35% | Not published; see benchmark note below |
| 5 | Empty seats per off-peak class | ASSUME, cross-checked | 4 | ≈ 10-seat class at 60% off-peak fill; see note |
| 6 | Price per seat | **OBSERVED** | 300 MAD | Studio price lists and press, 2025–26 |
| 7 | **Result (Casablanca)** | DERIVED | 43 × 20 × 0.35 × 4 = **≈ 1,200 seats/week** | |
| 7 | **Result (Rabat)** | DERIVED | 11 × 20 × 0.35 × 4 = **≈ 310 seats/week** | |
| 7 | **Result (both cities)** | DERIVED | **≈ 1,510 seats/week ≈ 450,000 MAD/week of unsold class capacity** | |

## How each number was reached

- **Population.** 2024 census figures for the cities themselves. Version 1 used 3.7M and 0.6M, which overstated both. Wider areas are much larger (Rabat with Salé and Témara is about 1.76M), so if the venture later covers Salé and Témara, the studio count must widen too.
- **Studio count.** Listings counted by category (yoga studio, pilates studio, boxing gym) on poidata.io, data as of Aug 2025. This replaces the version 1 guess of 1 studio per 50,000 people. The implied ratio is **1 per 75,000 in Casablanca and 1 per 47,000 in Rabat** (1 per 69,000 combined), so version 1 was close for Rabat but overstated Casablanca by about 70%.
  - *Likely an undercount:* searching the web found at least eight pilates studios in Casablanca by name (Core Studio, 10Studio Pilates, High Studio, Encore Pilates, The Pilates Studio, Tri Pilates, Rise Studio and Eleven Studio, which is opening soon). Spin, barre and HIIT studios aren't counted at all.
  - *Possibly double-counted:* a studio offering yoga and pilates may appear in both categories.
  - poidata does not disclose its method, so treat this as a floor to be checked on Google Maps.
- **Classes per week (20).** Studio websites show opening hours (e.g. Monday–Friday 8:00–21:00 or 21:30, shorter weekends) but not timetables, which load inside booking apps. Opening hours that long can fit 20 classes, so 20 is plausible but unverified.
- **Off-peak share (35%).** Not published for Morocco. US boutique data (Mariana Tek, 236 studios) ranks 5–6 pm, 7–8 pm and 6–7 am as the busiest starts and 2 pm as the least attended, which fits a midday off-peak window. No percentage is available, so this stays an assumption.
- **Empty seats (4).** Reformer studios describe "small groups" and a "limited number of reformers", typically 6–12 machines. At about 10 seats and 60% off-peak fill, 4 seats are empty. Industry KPI write-ups cite 70% as a profitability floor for average fill, and give one example of a 40% off-peak "ghost town", but these figures are unattributed. Still an assumption, to be replaced with one week of real attendance from a pilot studio (Phase 2).
- **Price per seat (300 MAD).** Core Studio sells reformer classes at 260–300 MAD each in packs and mat classes at about 220 MAD. Rise Studio lists a reformer class at 350 MAD. Le360 (Jan 2026) reports 250–400 MAD per reformer session in Morocco.

---

## Sensitivity: how much does each assumption move the answer?

Both cities combined, seats per week. The base case is in **bold**.

| Studios | Basis | Off-peak 25% · 2 empty | Off-peak 35% · 4 empty | Off-peak 45% · 6 empty |
|---|---|---|---|---|
| 37 | 1 per 100,000 people | 370 | 1,040 | 2,000 |
| **54** | **Counted listings** | **540** | **1,510** | **2,920** |
| 108 | Listings undercount by half | 1,080 | 3,020 | 5,830 |

**Reading it:** the plausible range is about 370 to 5,800 empty seats a week. The studio count now rests on data rather than a guess, so the biggest remaining uncertainty is off-peak share and empty seats per class. Those two can only be measured inside a real studio.

---

## What this means for one pilot studio

| | Seats per week | Value per week (at 300 MAD) |
|---|---|---|
| Empty off-peak seats (20 × 35% × 4) | 28 | 8,400 MAD |
| Product Goal: fill 2 of 4 per class (`goals.md`) | 14 | 4,200 MAD |

With 2–3 pilot studios, that is about 30–40 extra bookings a week, enough to see within 6 weeks whether trial goers come back.

---

## What the research changed beyond the numbers

- **Studios already sell low-commitment entry.** Core Studio offers a "Discovery pack" of 3 reformer classes for 600 MAD, valid one month, alongside 10–50-class carnets and 3–12-month subscriptions. Our venture is therefore not competing with "no trial option". It competes with trial packs the studio already controls. This belongs in `opportunity.md` as an existing alternative, and is a question for the owner interviews: why don't discovery packs already fill off-peak classes?
- **Cancellation rules are part of the commitment barrier.** Studios require cancelling 3–24 hours ahead or losing the class (10Studio: 24 hours; Core Studio: 3 hours in its FAQ, with longer windows mentioned elsewhere). This is a concrete form of the regret-aversion our riskiest assumption describes.
- **Pilates is the growth segment.** Le360 describes reformer studios "springing up like mushrooms" across Morocco, and US data shows pilates is the most common boutique modality (about 1 in 3 studios). This supports focusing the reservation test and the first pilot on reformer pilates (`open-gaps.md`, Gap 7).

---

## Still to replace with counts

| Step | How to check | When |
|---|---|---|
| 2. Studio count | Search Google Maps for "pilates", "yoga", "reformer", "boxing", "spin" in each city; remove chain gyms and duplicates | Before Session 16 |
| 3. Classes per week | Read 5 studios' timetables in their booking apps (e.g. Core Studio's app) | Before Session 16 |
| 4–5. Off-peak share and empty seats | One week of class-by-class attendance from a pilot studio | Phase 2 pilot (Sessions 22–23) |

## The number you can challenge

The studio count is now sourced, so the weakest link is **empty seats per off-peak class**. It multiplies the result directly and comes from no Moroccan data at all. One week of attendance from a pilot studio replaces it. Our three owners already give a first hint: their quiet classes run at about 3 of 10 and 2–3 of 8, so 5–7 empty seats, above our assumption of 4.

---

## Sources
- Population: 2024 census (RGPH, Haut-Commissariat au Plan), via [City Population — Morocco cities](https://www.citypopulation.de/en/morocco/cities/)
- Studio counts: [poidata.io — Yoga studios in Morocco](https://poidata.io/report/yoga-studio/morocco), [Pilates studios](https://poidata.io/report/pilates-studio/morocco), [Boxing gyms](https://poidata.io/report/boxing-gym/morocco), data as of Aug 2025
- Studio pricing and policies: [Core Studio — Tarifs](https://corestudio.ma/tarifs/), [Rise Studio](https://risestudiocasablanca.setmore.com/), [10Studio Pilates](https://www.10studiopilates.com/), [High Studio](https://highstudio.ma/), [Encore Pilates](https://www.encorepilates.ma/), [Eleven Studio](https://www.elevenstudio.casa/en)
- Market price range: [Le360 — Le Pilates Reformer, la nouvelle star de la remise en forme (Jan 2026)](https://fr.le360.ma/lifestyle/le-pilates-reformer-la-nouvelle-star-de-la-remise-en-forme_N4XSWT2BURGWRDC2W5HRIXOG3E/)
- Time-of-day attendance: [Mariana Tek — Trends in Boutique Fitness: Northeast Metro Region](https://www.marianatek.com/resources/northeast-regional-data-report/)
- Fill-rate benchmarks (unattributed, indicative only): [PulseRevOps — KPIs for boutique fitness studios](https://pulserevops.com/industry-kpis/ik0410)
