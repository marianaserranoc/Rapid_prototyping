# Pre-mortem — it's December 2027 and Daba has failed. Why?

**Method:** imagine the venture has already failed, then work backwards to the most likely causes. Each cause links to the evidence we have **today**, the earliest signal that it's happening, and what we'd do. This is team reasoning from the evidence log, not new data. Open questions stay visible, as the course asks.

| # | How Daba died | Likelihood today | Evidence today | Earliest warning signal | What we'd do |
|---|---|---|---|---|---|
| 1 | **People reserved but didn't show up.** Reservations were free, so the 64% was cheap talk | **High** | A/B measured reservations only; fragility index 3 (`ab-test-analysis.md`) | Phase 2 attendance under 40% | Reminders plus a small refundable deposit; if still low, pivot on price |
| 2 | **Newcomers came once and vanished.** Owners stopped releasing seats | **High** | Owner D: one-off visitors have "little value"; return untested | Return under 15% at Session 28 | Add a "second class" nudge at full price; if it fails, rethink the model |
| 3 | **Price, not commitment, was the real ceiling** | Medium | Price/gym in 10 of 27 declines, flat across arms; proxy G6 | No-shows citing price; low second-visit rate | First-visit price set by the owner for newcomers only (owners must agree it isn't a "discount") |
| 4 | **Owners never committed a real class** | Medium | All owner evidence is "I would"; none dated | Owners D and E don't name a date within a week | Bring an instructor or studio insider into outreach (NOVA's lesson); offer to run it fully by hand |
| 5 | **Studios copied it themselves** with their own single-class option | Medium | Core Studio already sells discovery packs; the app is easy to copy (`blue-ocean.md`) | A pilot owner asks "why not just do this myself?" | Make reach to new people and the new-vs-regular report the product, not the offer |
| 6 | **Regulars found out** and asked for the same deal | Low–medium | B, C, D, E made invisibility a condition | Any regular asking about it in the pilot (guardrail) | Stop; tighten newcomer checks against member lists |
| 7 | **Too small to matter** | Medium | Solopreneur scale in two cities (`size-of-the-prize.md`) | Fewer than 10 studios interested after the pilot | Widen to more cities (Marrakech, Tangier, Salé/Témara) and formats (Hyrox, functional, spin) |
| 8 | **The admin was too much** for solo owners | Medium | Owners run everything by hand on WhatsApp; LeenOwner candidate persona | Owners skip releasing seats in week 2 | Seat release in one WhatsApp message; we do the rest |
| 9 | **An aggregator arrived** (ClassPass-style) with credits and discounts | Low (none found in Morocco) | Desk research | A launch announcement | Compete on owner control and full price, which aggregators don't offer |

## What this changes now
- Risks 1 and 2 are why `build-decision.md` is **GO, narrowly** and why `experiment-card-phase2.md` measures attendance and return before anything else.
- Risk 4 is the cheapest to reduce today: ask Owners D and E for a **date**.
- Risk 5 is why `blue-ocean.md` says the moat can't be the code.
