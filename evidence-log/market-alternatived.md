# Market Alternatives — what owners and goers use instead

**Purpose:** map what our users would choose instead of us, using the course's four categories, and decide what each one means for the product. Supporting output for `ERRC.md`.
**Researched:** 11 Oct 2026. **Rule used:** for each alternative, market evidence (what exists) is kept separate from target-user behaviour (what our users actually do). If behaviour is unknown, it is labelled a hypothesis or gap.

**Evidence labels:** OBSERVED (seen in a real episode), REPORTED (said in an interview), DESK (public source), HYPOTHESIS (not yet evidenced).

---

## Bound the decision
- **Market:** independent boutique fitness studios (yoga, pilates, reformer, boxing) in Casablanca (pop. 3.2M) and Rabat (0.5M). About 54 listed studios, likely an undercount (`Fermi_estimate.md`).
- **Price level:** a single boutique class costs **250–400 MAD**, while an average monthly gym membership in Casablanca is **about 314 MAD**. **One boutique class costs roughly a month of gym.**
- **Decision this map informs:** what to compete on, what to leave alone, and which test comes first.

---

## Alternatives map

### Goer side

| Alternative | Category | Simple test | Target-user behaviour | Compare on | Evidence so far and gaps | So what? |
|---|---|---|---|---|---|---|
| Studio's own discovery pack (e.g. Core Studio: 3 reformer classes, 600 MAD, 1 month) | **Direct competitor** | Same user, same job? Yes: a low-commitment way to try one studio | HYPOTHESIS — no goer mentioned using one | Price per class, commitment length, booking certainty | DESK: Core Studio price list. GAP: how many studios offer one; do goers know about them? | Our offer is narrower (one class, off-peak only) and must win on certainty and no prepayment, not on price |
| Multi-studio class passes (ClassPass-style) | **Direct competitor** | Same job, different route | HYPOTHESIS — not available | Variety, price, credits | DESK: ClassPass's coverage page doesn't list Morocco (Nov 2025); no local equivalent found. GAP: a local pass may exist that we missed | No dominant aggregator in Morocco: room for a first mover, but also no proof goers want one |
| Gym membership already paid for | **Indirect substitute** | Same progress (a workout), different route | REPORTED: G1 has a gym membership, trains 3–4×/week, and went to the gym instead of booking the class | Sunk cost, certainty, effort | REPORTED G1; DESK: gym ≈ 314 MAD/month. 2 of 3 decliners in the Persona 1 trial said they'd rather use the already-paid gym | The real competitor for a free window. A single class must feel worth the price of a month of gym |
| Home workout, run, or nothing | **Indirect substitute / doing nothing** | Same progress at zero cost | HYPOTHESIS — implied by G1's fallback | Cost, effort, habit | No direct evidence | Zero-cost default; only certainty and low effort can beat it |
| Instagram discovery + WhatsApp DM to book | **Manual workaround** | User assembles it themselves | OBSERVED: G2 saw a studio's Instagram story, sent a DM, got no quick reply and gave up | Speed of confirmation, effort | REPORTED G2; Persona 2 trial: instant confirmation 4 of 5 vs. refund guarantee 2 of 5 | **The friction we can remove most cheaply:** confirm the place instantly |

### Owner side

| Alternative | Category | Simple test | Target-user behaviour | Compare on | Evidence so far and gaps | So what? |
|---|---|---|---|---|---|---|
| Discount codes or cheaper off-peak prices | **Direct competitor** (own lever) | Same job: fill the slot | REPORTED: Owners A and C tried discounts and stopped; regulars objected or asked why. Owner B avoids discounting | Fill rate, price integrity, regular reaction | REPORTED (3 owners) | Owners have rejected it. Anything that looks like a discount fails at the gate |
| Studio booking software (e.g. studio apps, Setmore) and directories (fitness.ma: 790 clubs listed in Casablanca, 219 in Rabat; free trial sessions at partner clubs) | **Indirect substitute** | Same progress (bookings), different route | HYPOTHESIS — owners did not mention them as a fix for off-peak | Reach to new goers, cost, control | DESK: fitness.ma, Core Studio app, Rise Studio on Setmore. GAP: do they bring net-new goers to specific off-peak slots? | Don't replace their booking tool. Sit beside it and send them new people for chosen seats |
| Asking regulars, social posts, WhatsApp blasts | **Manual workaround** | Owner assembles it | REPORTED (version 1 JTBD, team interpretation); not confirmed by the 3 owners | Effort, reach, consistency | GAP: not asked directly | Ask in the next owner interviews how much time this takes |
| Run the class near-empty, or cut it | **Doing nothing** | Accept the pain | REPORTED: Owner B ran a 2-person class rather than disappoint a regular; Owner A cut a class after months | Lost revenue, regular loyalty | REPORTED (2 owners) | The strongest current alternative: free, familiar, fully controlled. Our offer must be almost as effortless |

---

## Strongest current alternative
- **Goer side:** the already-paid gym membership, plus giving up when a DM booking stalls.
- **Owner side:** running the class near-empty or cutting it, after discounting failed.

**Evidence basis:** REPORTED and OBSERVED behaviour from 2 goer interviews and 3 owner interviews, plus card trials (stated intent). Small samples, directional only.

---

## Opportunity stress test (four lenses, three findings kept)

| Lens | Finding | Implication for the prototype |
|---|---|---|
| **Entry** | Low barrier: studios already sell discovery packs and could add a "single off-peak class" button themselves | Our value can't be the offer alone; it must be **reach to new goers + instant confirmation + new-vs-regular tracking**, which a solo owner won't build (Owner C) |
| **Substitution** | For goers, one class ≈ a month of gym, so the gym wins on price | Test whether goers accept full studio price for one off-peak class, or whether the price itself, not commitment, is the barrier (Persona 1: "price is the fixable part") |
| **Dependencies** | Depends on owners releasing seats and on WhatsApp/Instagram as the booking channel | Manual WhatsApp flow first; keep owners in control of which seats go out |
| Major shifts | ClassPass or a regional aggregator entering Morocco would change the field | Not kept: no sign of entry; revisit at the Phase 2 gate |

---

## Strategic bets to test

| Hypothesis | Method | Metric | Threshold | Decision rule |
|---|---|---|---|---|
| **Removing commitment risk beats normal terms** (priority test) | Two-arm WoZ test (`experiment-card.md`) | Book-and-attend gap between arms | ≥40 pp | Met: keep. Under 20 pp: pivot to an instant-booking tool |
| Instant confirmation beats the DM workaround | Hold constant in the primary test; measure time from message to confirmation | Abandonment before confirming | PROPOSED ≤1 of 10 abandon | Missed: simplify the booking step before anything else |
| Owners prefer our offer to their own discovery pack for off-peak slots | Next owner interviews: show both side by side | Owners who would use ours for off-peak | PROPOSED ≥3 of 5 | Missed: help owners promote their own discovery packs instead |
| Goers pay full studio price for one class | Primary test uses full price in both arms | Bookings at full price | PROPOSED ≥3 of 10 book | Missed: price, not commitment, is the barrier; rethink with owners |

---

## Sources
- [Core Studio — Tarifs](https://corestudio.ma/tarifs/) (discovery packs, carnets, subscriptions)
- [Rise Studio booking page](https://risestudiocasablanca.setmore.com/) (350 MAD reformer class)
- [Le360, Jan 2026](https://fr.le360.ma/lifestyle/le-pilates-reformer-la-nouvelle-star-de-la-remise-en-forme_N4XSWT2BURGWRDC2W5HRIXOG3E/) (250–400 MAD per reformer session)
- [Combien-coute.net — gym membership in Casablanca](https://www.combien-coute.net/fitness/maroc/casablanca/) (≈ 314 MAD/month, Numbeo-based)
- [ClassPass — Where can I use ClassPass?](https://help.classpass.com/hc/en-us/articles/204992155-Where-can-I-use-ClassPass-) (no Morocco listing, Nov 2025)
- [Fitness.ma](https://fitness.ma/) (directory: 790 clubs in Casablanca, 219 in Rabat; free trial sessions)
- [Hespress, Mar 2023, citing Ken Research](https://www.hespress.com/1146670-1146670.html) (specialised pilates, cycling and yoga studios spreading in Casablanca, Rabat, Marrakech)
- Interviews and trials: `personas/selected_personas/gym_goers.md`, `gym_owners.md`, `oz-trials.md`
