# User Feedback — real-user evidence log

**Purpose:** one place for every piece of feedback from real people, what it supports or weakens, and what it changed. Detailed notes stay in `personas/selected_personas/`.
**Updated:** 11 Oct 2026.

**Rules for this file**
- Only real people. AI-simulated responses (`gym_owners.md`, `personas/hypothetical/ai-persona-*`) are rehearsal and are **not listed here**.
- Stated intent ("I'd book it") is labelled as such and never counted as behaviour.
- Use initials or codes only. No names, phone numbers or screenshots of private messages.

---

## 1. Participants

| Code | Side | Method | Date | Location | Fit to target user | Detail file |
|---|---|---|---|---|---|---|
| G1 | Goer | Interview | [to add] | [to confirm] | Partial: gym member who occasionally tries boutique classes | `gym_goers.md` Persona 1 |
| G2 | Goer | Interview | [to add] | [to confirm] | Good: no fixed studio, unpredictable schedule | `gym_goers.md` Persona 2 |
| G3 | Goer | Interview, with live walk-through | [to add] | [to confirm] | Good: no fixed studio, moves between studios | `gym_goers.md` Persona 3 (labelled "Example-G3" in that file) |
| Owner A | Owner | In-person visit | [to add] | [to confirm] | Good: sets schedule, watches bookings | `gym_owners.md` |
| Owner B | Owner | Phone call | [to add] | [to confirm] | Good | `gym_owners.md` |
| Owner C | Owner | In-person visit | [to add] | [to confirm] | Good | `gym_owners.md` |
| Trial P1 (8 people) | Goer | Card trial, one at a time | [to add] | [to confirm] | Partial: friends-of-friends with gym memberships | `oz-trials.md` |
| Trial P2 (10 people, 5 per card) | Goer | Card trial, two cards | [to add] | [to confirm] | Partial: convenience sample | `oz-trials.md` |
| Trial P3 (7 people) | Goer | Card trial | [to add] | [to confirm] | Partial: convenience sample | `oz-trials.md` |
| Expert: Aly Shourbagui | Founder of NOVA (Egypt), analogous platform | Interview | [to add] | Egypt | Expert, not a target user: evidence on owner adoption and go-to-market | `interview-nova-founder.md` |

**To complete before submission:** dates, and whether each person is in Casablanca or Rabat. The rubric scores participant fit, so any participant outside Morocco should be marked as a proxy.

---

## 2. What real people told us

### Owners (n=3)

| Feedback | Who | Type | Supports or weakens |
|---|---|---|---|
| Names a specific quiet slot: Tue 11:00, about 3 of 10 | A | REPORTED | Supports the pain point: recurring, specific, measurable |
| Names a specific quiet slot: Fri 12:30, 2–3 of 8 | C | REPORTED | Supports the pain point |
| Tried a discount: few returned and regulars objected | A | REPORTED | Supports "discounting backfires" |
| Tried a discount once; regulars asked why, so stopped | C | REPORTED | Supports "discounting backfires" |
| Avoids discounting because regulars notice and expect the same | B | REPORTED | Supports |
| Cut a class after months of low attendance | A | REPORTED | Supports a real push; shows "exit" as the current alternative |
| Ran a 2-person class rather than disappoint a regular | B | REPORTED | Supports "doing nothing" as the current alternative |
| Full-price refund vs. discount: different, worth testing, wants to see it work first | A | STATED INTENT | Supports Create move; owners need proof |
| Would accept a third party only if she controls the seats and it doesn't look like a discount | B | STATED INTENT | **Changes the design:** owner control is a requirement |
| Open to it if seats are hers to choose and for new customers only; would want new-vs-existing tracking but won't build it | C | STATED INTENT | **Changes the design:** new clients only; tracking is part of the product |

### Expert: founder of NOVA, Egypt (n=1)

| Feedback | Type | Supports or weakens |
|---|---|---|
| Studios had seen similar ideas before that never came to anything | REPORTED (expert) | Supports owner scepticism as a real adoption barrier |
| Studios trusted NOVA because a co-founder is an instructor and the team was visibly committed | REPORTED (expert) | **New factor:** team credibility drives owner adoption |
| Owners understood the win-win easily | REPORTED (expert) | Supports the two-sided value hypothesis |
| A credit subscription failed at first because people were sceptical; credit packages worked | REPORTED (expert) | **Mixed:** recurring commitment puts people off, but prepaid packs were accepted |
| Influencer marketing and word of mouth drove growth | REPORTED (expert) | Supports trust and social proof as adoption levers |

### Goers (n=2 interviews + 3 card trials)

| Feedback | Who | Type | Supports or weakens |
|---|---|---|---|
| Had a free morning that matched a class, didn't book, went to the gym | G1 | REPORTED | **Changes the JTBD trigger** to "unexpected free window" |
| Didn't want a package before knowing the place; single class felt expensive vs. the gym already paid for | G1 | REPORTED | Supports regret-aversion **and** a price barrier |
| Bought a 10-pack, used 5–6, now avoids prepaying | G1 | REPORTED | Supports regret-aversion |
| The instructor is the main reason to return | G1 | REPORTED | Opens a separate quality/instructor lever |
| Meeting cancelled → saw a studio's story → sent a DM → no quick reply → gave up | G2 | REPORTED episode | **Weakens the riskiest assumption:** she gave up over certainty, not risk |
| Single class at gym-equivalent price: 5 of 8 would book; 2 decliners preferred the paid gym, 1 didn't know the instructor | Trial P1 | STATED INTENT | Price is a fixable barrier; instructor trust is a second lever |
| Instant confirmation 4 of 5 vs. refund guarantee 2 of 5; refund decliners wanted certainty of a place | Trial P2 | STATED INTENT | **Weakens the riskiest assumption** |
| Trial class: 5 of 7 would book; 3 of those 5 would probably return | Trial P3 | STATED INTENT | Supports appeal of a trial; return is intent only |

---

## 3. What the feedback changed

| Decision | Before | After | Triggered by |
|---|---|---|---|
| Primary test design | Compared commitment terms only | Instant confirmation held constant in both arms so certainty can't explain the result | G2, Trial P2 |
| Owner offer | A trial mechanism for any goer | Seats chosen by the owner, offered to **new clients only**, with new-vs-regular tracking | Owners B, C |
| JTBD trigger | Usual class full or cancelled | Unexpected free window | G1, G2 |
| Price in the test | Not fixed | Full studio price in both arms, to separate price from commitment | G1, Trial P1 |
| Riskiest assumption status | Working hypothesis | **Contested**, with booking certainty as a named rival | G2, Trial P2 |
| Owner outreach | The offer alone would convince owners | Involve a respected instructor or studio insider in outreach; address "why will this one last?" up front | NOVA founder |
| Phase 2 acquisition | Not defined | Test influencer and referral channels for goers | NOVA founder |

---

## 4. Primary test results (two-arm reservation test)
*Running 11–13 Oct 2026 through `booking-test/`. Fill from `experiment-card.md` once replies are in.*

| | Arm A (no commitment) | Arm B (normal terms) |
|---|---|---|
| Link sent to | | |
| Reserved ("I'M RESERVING" message) | | |
| Declined ("NOT FOR ME" message) | | |
| No reply | | |
| Top decline reasons | | |
| Voice notes received | | |

**Result against threshold:** [≥30 pp with p < 0.05 / 15–29 pp / under 15 pp] · n per arm: [ ]
**Decision:** [continue / change / stop]

---

## 5. What we still don't know
- Whether anyone **actually attends** (the reservation test stops at reserving; attendance is tested in the Phase 2 pilot).
- Whether trial goers come back at full price.
- Whether owners' answers hold beyond these three, and whether they'd choose this over their own discovery packs.
- Whether the goer participants are in our target cities.
