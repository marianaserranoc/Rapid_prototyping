# Opportunity — version 0.2

*Successor to `opportunity.md` after the market research and ERRC review (Session 11); evidence updated 12 Oct 2026 with the A/B result, Owners D and E, goers G4 and G5, and with the card-trial row removed after sprint feedback. Business idea, pain point, user, need, insight and How Might We are unchanged. New: alternatives, strongest alternative, competitive factors, value innovation hypothesis and updated evidence gaps.*

## Business idea
We help independent boutique fitness studios in Casablanca and Rabat fill their recurring underfilled off-peak classes by letting new studio-goers book a single class with no package or membership commitment, at the price and seat limit the studio sets, so owners gain new full-price attendees without discounting and goers can find out whether a studio is worth it before committing.

## Pain point
Owners of small independent boutique studios struggle to fill their recurring off-peak classes when attendance drops outside peak hours, causing empty seats that are lost revenue because rent and instructor pay are fixed regardless of attendance, because the only lever they know, discounting, attracts deal-hunters and pulls full-price regulars down instead of bringing in new people.

## User, need, and insight

**Primary user (owner side)**
The owner or manager of an independent boutique studio in Casablanca or Rabat, running around 15–25 classes a week with a few instructors, who sets the schedule personally and watches attendance class by class, needs to turn underfilled off-peak seats into steady attendance from new people at full price because past discounts cheapened the studio's brand and taught regulars to wait for deals, so owners would rather leave seats empty than discount again.

**Secondary user (goer side)**
A studio-goer in Casablanca or Rabat with flexible but non-habitual free time, who has not committed to a studio, package or membership, needs to find out whether an unfamiliar studio or class is worth it before putting money into it because buying a package before trying feels like an irreversible bet, and past packages left partly unused make them avoid committing again (regret-aversion, still the riskiest assumption).

## How might we
How might we help boutique studio owners convert underfilled off-peak seats into predictable, full-price attendance from new goers, by letting those goers prove a class is worth it before committing, without relying on discounting or on anything owners would see as discounting?

---

## Evidence status

| Claim | Source | Strength |
|---|---|---|
| Owners refuse to discount because it damages brand and regulars | 5 real owner interviews, A–E (`personas/selected_personas/gym_owners.md`) | Real target users, n=5, directional only |
| Owners want full control over which seats and slots open | Owners B, C, D, E (explicit condition) | Real target users, 4 of 5, stated |
| Goers avoid packages after unused past packages | Goer interviews G1, G4, G5 (`user-feedback.md`) | Real goers, n=3 |
| Removing the pack raises reservations (regret-aversion) | Two-arm reservation test, 25 per arm: 16/25 no-pack vs. 7/25 3-class pack, +36 pp, p = 0.011 (`ab-test-results.md`) | **Supported at reservation level**: real class-goers, real action, pre-set threshold met. Not attendance; fictional studio; no payment |
| Newcomers return at full price | Not yet tested | **Unvalidated: now the riskiest assumption** (Phase 2 pilot) |
| Comparable model works in nearby markets | **Interview with NOVA's founder (Egypt)** (`interview-nova-founder.md`); ClassPass (Spain) desk research | Expert evidence from an analogous market: NOVA operates, studios adopted it once they trusted the team, goers rejected a subscription but bought credit packages. No figures; one person's account |

## Competing hypotheses (not yet ruled out)
- **Timing or awareness (goer):** demand exists, but goers don't think of the off-peak slot when they have a free window.
- **Absence of demand (goer):** nobody wants that slot regardless of price, risk or timing.
- **Quality uncertainty (goer):** after the pack is removed, people may still hold back because they don't know the class, the coach or whether they'll feel like a beginner (G5; 2 of 27 A/B decliners cited the coach).
- **Price (goer):** one class costs about a month of gym; price or "prefer my gym" were 10 of 27 A/B declines.
- **Owner adoption risk:** even if the goer mechanism works, owners may see it as discounting in disguise or fear it cannibalises members.

Each points to a different product: a no-commitment trial, a discovery or matching tool, instructor social proof, or cutting the slot entirely. See `assumptions.md` and `experiment-card.md`.

## Current alternatives (four categories)
Full map with sources in `market-alternatives.md`.

| Category | Owner side | Booker side |
|---|---|---|
| Direct competitor | Discount codes or cheaper off-peak prices (tried and abandoned by Owners A and C) | Studios' own discovery packs (e.g. Core Studio: 3 classes, 600 MAD, 1 month); no multi-studio pass such as ClassPass found in Morocco |
| Indirect substitute | Studio booking apps and directories (fitness.ma lists 790 clubs in Casablanca, 219 in Rabat) | The gym membership already paid for (G1); home workouts |
| Manual workaround | Instagram posts and stories: a few bookings, not consistent (Owners D, E) | Instagram discovery + WhatsApp DM to book (G2, G4) |
| Doing nothing | Run the class near-empty or cut it (Owners A, B, E) | Skip the free window, or keep postponing (G5) |

## Strongest current alternative
**Doing nothing on the owner side:** running the class near-empty or cutting it, after discounting failed. Evidence basis: 5 real owner interviews (reported, not observed). On the booker side, the gym already paid for, since one boutique class (250–400 MAD) costs about a month of gym (~314 MAD).

## Competitive factors and market conventions
Factors: price per class, upfront commitment, booking certainty and speed, price integrity for the owner, owner control over who gets which seat, knowing whether new people came, variety of studios (`market-alternatives.md`).

Conventions taken for granted: quiet slots are filled with discounts; newcomers commit to a pack before trying; booking a boutique class means messaging and waiting.

## Value innovation hypothesis
Eliminate discounting; reduce first-visit commitment to one class with no pack; raise booking certainty; create owner-controlled seat release for new clients only, with a new-vs-regular count. If it holds, off-peak classes fill with net-new people at full price without regulars expecting deals. This remains a hypothesis, not a validated blue ocean or confirmed business model (`ERRC.md`).

## Open evidence gaps
- ~~Whether removing the pack beats the 3-class pack by ≥30 pp~~: **yes at reservation level** (+36 pp, p = 0.011, 25 per arm). Still open: attendance.
- Whether newcomers accept full price for one class when it costs about a month of gym.
- How much certainty of a spot adds on top of no-pack (held constant in the test; G2 and G4 lost bookings to slow replies).
- Whether owners would use this instead of their own discovery packs.
- Whether trial goers return at full price or vanish (Phase 2 pilot).
- Goer segment not split yet: never-visited prospects, lapsed members and peak-hour regulars may have different barriers.
- Studio count rests on listings that likely undercount (54 across both cities, `Fermi_estimate.md`).
