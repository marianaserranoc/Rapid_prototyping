# Build Decision — are we ready to build Daba?

**Decision (13 Oct 2026): GO, narrowly.** Build only the First Working Skeleton in `specs/2026-10-12-off-peak-seat-booking/`. Nothing else is built until the Phase 2 pilot shows that reservations turn into attendance.

---

## 1. What we had to know before building, and what we know now

| Gate question | Answer | Evidence | Confidence |
|---|---|---|---|
| Is the owner's pain real and recurring? | **Yes** | 4 owners (A, C, D, E) name a specific quiet class at about 30% full, paying the instructor anyway (A, C, D, E) | Medium: n=4, reported |
| Do owners reject the current fix (discounting)? | **Yes** | 5 of 5 owners A–E (proxy F excluded) | Medium: stated |
| Does removing the pack change what newcomers do? | **Yes, at reservation level** | A/B test: 64% vs. 28%, +36 pp, p = 0.011, n=50, threshold set before testing | Medium: real action, but reservation ≠ attendance |
| Would owners use it? | **Probably** | Owners A–E: 4 say yes and 1 says maybe, under conditions we can build | Low: no owner has committed a real class yet |
| Do newcomers come back at full price? | **Unknown** | Not tested | None: **now the riskiest assumption** |
| Is the prize worth it? | **Yes, at solopreneur scale** | ≈ 4,200 MAD a week of extra revenue per studio if 2 seats per off-peak class fill (`size-of-the-prize.md`) | Low: assumptions in the chain |

**Why GO now:** the assumption that could have killed the idea (commitment as the barrier) survived a real test with a bar set in advance. The next risks (attendance, return) **can only be measured with something real people can book and owners can run**, so a minimal build is the cheapest next test, not a premature one.

## 2. What we build first (Sessions 16–21)
Only what the pilot needs to measure attendance and return:

| Build | Why | Requirement |
|---|---|---|
| Owner releases chosen seats (one WhatsApp message or one form) | Owner control is a condition for 4 of 5 owners | R1 |
| Offer visible to newcomers only | Regulars must never see it (C, D, E) | R2 |
| One class, no pack, full price, pay at the studio | The variable the A/B test validated | R3 |
| Confirmation within 1 minute | Slow replies lose bookings (G2, G4) | R4 |
| No overbooking; clear cancellation terms | Trust for owners and goers | R5, R6 |
| Studio marks attendance | **The thing we still need to learn** | R7 |
| New-vs-regular report for the owner | What owners value and nobody tracks | R8 |

## 3. What we will not build yet
| Not now | Why not |
|---|---|
| Online payments | Adds legal and trust risk the pilot doesn't need; goers pay at the studio |
| Credits, subscriptions, multi-studio passes | NOVA's subscription failed at first; credits make us an aggregator, which owners distrust |
| Discounts or dynamic pricing | Contradicts the Eliminate move and every condition owners A–E set |
| A native app | Goers book from Instagram and WhatsApp links; a mobile web page is enough |
| Owner self-service onboarding, more cities | Not before 2–3 pilot studios work by hand |

## 4. Budget: why it's worth the time and tokens
- **Scope:** about 8 requirements, one booking flow, one owner view, built with a course tool (Lovable, Bolt, v0 or a coding agent; decided at Session 16).
- **Reuse:** the A/B booking page (`booking-test/`) already proves the goer screen works on a phone.
- **Cap:** if the skeleton isn't usable end to end by Session 21, we run the pilot by hand (WhatsApp plus a shared sheet) instead of building more.

## 5. What would stop us (kill and pivot criteria)
| If, in the Phase 2 pilot… | Then |
|---|---|
| No owner releases a real seat on a real date | **Stop building**; rework the owner offer (trust, insider outreach, NOVA's lesson) |
| Newcomers reserve but mostly don't turn up | **Pivot on price or certainty** (decline reasons pick which) |
| Fewer than 30% of trial goers rebook at full price (Phase 4) | **Rethink the model**: owners won't pay for one-off visitors (Owner D) |
| Owners only want reach, not the rules | **Narrow** to a newcomer-acquisition channel for studios |

## 6. Would anyone invest?
Not yet, and we'd say so. What an early backer would see: a real pain owners can put a number on; a behaviour change of +36 pp at the same price; owners asking for exactly the rules we'd build; and a clear next proof point (attendance and return in 2–3 studios within two weeks). What they'd wait for: **one owner committing a real class**, and **newcomers who come back**.
