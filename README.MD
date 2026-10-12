# Daba

**Full-price off-peak seats for independent boutique studios in Casablanca and Rabat.**
Rapid Prototyping with AI · IE University · Team: [names]

---

## Working Backwards: press-release opener
*A future customer story we are testing, not a claim about today. Quotes are illustrative.*

### Boutique studios in Casablanca fill their quiet classes without a single discount
*Studio owners choose which off-peak seats to open to first-time visitors, at their normal price; newcomers get a confirmed place in seconds with no package to buy.*

**CASABLANCA, March 2027.** Daba today launched a simple way for independent yoga, pilates and boxing studios to fill the classes that run half-empty every week, without lowering their prices or upsetting their regulars.

**The problem.** Every studio has a class like Tuesday at 11:00: rent and instructor pay are fixed, but three people turn up to a room for ten. Discounts bring deal-hunters and make regulars ask why they pay more. Meanwhile, people with a free morning scroll past a studio's story, send a message, wait for a reply, and go to the gym instead.

**The solution.** Owners pick the seats they want to fill. First-time visitors see the class, book one session at the studio's normal price with no pack or membership, and get a confirmed place straight away. Regulars never see the offer.

**How it works.** The owner releases seats from their phone. A newcomer opens a link, enters a name and number, taps once, and is booked. After class, the owner sees how many attendees were new.

> "I stopped discounting because my regulars noticed. Now I open two seats on Tuesday mornings to new people at my normal price, and I can see who comes back." — *Studio owner, Maârif (illustrative)*

> "My meeting got cancelled, I booked a reformer class in a minute and paid at the door." — *Goer, Casablanca (illustrative)*

**What would prove this wrong:** if newcomers don't book more without a package than with one, if they won't pay full price for a single class, or if they never come back. See `evidence-log/ERRC.md` and `evidence-log/experiment-card.md`.

---

## Where we are (12 Oct 2026)

| | Status |
|---|---|
| **Riskiest assumption (tested)** | Goers avoid booking because committing before trying feels like a bad bet (regret-aversion) |
| **Result** | Two-arm reservation test, 11–12 Oct, 25 people per version: **one class with no pack 16/25 (64%) vs. the same class through a 3-class pack 7/25 (28%)**, +36 pp, one-sided Fisher p = 0.011. The bar was set before the test (≥30 pp and p < 0.05), and it was met (`evidence-log/ab-test-results.md`) |
| **Decision at the Phase 1 gate** | **Continue.** Build the First Working Skeleton; pilot with 2–3 real studios and measure attendance and return at full price |
| **Real evidence** | 6 owner interviews (5 of 6 reject discounting; most would release seats if they choose them and regulars never see it); 7 goer interviews (pack avoidance, including a Casablanca Hyrox athlete turned away by a monthly-only box; two lost bookings to slow DM replies; one friend-invitation path; one proxy for whom price is the barrier); the A/B test; 1 expert interview (NOVA, Egypt) |
| **New riskiest assumption** | Trial goers come back at full price. Owners only value newcomers who return, and price was cited in 10 of 27 declines |
| **What could still make us narrow, pivot or stop** | People reserve but don't turn up or pay (reservations were cheap talk); trial goers never return (we'd be a discounter in disguise); no owner commits a real class |
| **Fixed after sprint feedback** | Illustrative card trials and "Example-G3" relabelled as examples and removed from all evidence; JTBD now has two circumstances, with Pull and Anxiety marked as hypotheses; persona selection explained (`evidence-log/personas/persona-selection.md`) |

---

## One coherent strategic chain

| Decision | Current one-liner | Source of truth |
|---|---|---|
| Target user | Owners of independent boutique studios in Casablanca and Rabat with a recurring underfilled off-peak class | `evidence-log/opportunity.md` |
| Job to Be Done | Fill named quiet slots with new people at normal price, choosing which seats are offered | `evidence-log/JTBD.md` |
| Strongest alternative | Run the class near-empty or cut it (owners); the gym already paid for (goers) | `evidence-log/market-alternatives.md` |
| ERRC direction | Eliminate discounting; reduce first-visit commitment to one class; raise booking certainty; create owner-controlled seat release for new clients only | `evidence-log/ERRC.md` |
| Value hypothesis | Full-price, no-package single classes for newcomers fill at least 2 empty seats per off-peak class without hurting regulars' purchases | `evidence-log/ERRC.md` |
| Evidence status | Riskiest assumption supported at reservation level (A/B test); attendance and return untested; not a validated market or business model | `evidence-log/user-feedback.md`, `evidence-log/ab-test-results.md` |
| Next evidence | Phase 2 pilot: attendance, payment and return at full price with Owners D and E; a seat-release walk-through | `evidence-log/experiment-card.md`, `specs/roadmap.md` |

---

## Repository map — three layers of truth

```
.
├── README.md                  ← you are here
├── AGENTS.md                  ← rules every coding agent follows
├── agents/
│   └── persona-agent.md       ← rehearsal with synthetic personas (never evidence)
├── specs/                     ← what we build, under which constraints
│   ├── mission.md
│   ├── tech-stack.md
│   ├── roadmap.md
│   └── 2026-10-12-off-peak-seat-booking/
│       ├── requirements.md
│       ├── plan.md
│       └── validation.md
├── booking-test/              ← two-version booking page used in the reservation test
├── test-brief.md              ← one-page brief of the test and interviews
├── downloads/                 ← AI helper prompts used
├── evidence-log/              ← what we know, and what supports it
│   ├── opportunity.md   goals.md   assumptions.md   experiment-card.md
│   ├── recruitment.md   JTBD.md    ERRC.md          user-feedback.md
│   ├── market-alternatives.md   Fermi_estimate.md   open-gaps.md
│   ├── interview-nova-founder.md   opportunity-v02.md
│   ├── ab-test-results.md       ← A/B reservation test: results and per-participant log
│   ├── interviews/
│   │   ├── README.md              ← index: every real interview, its code, transcript and recording
│   │   ├── transcriptions/        ← one report per interview (owners D, E, F; goers G4–G8)
│   │   └── audio-video/           ← the recordings
│   ├── pivot-log.md             ← how evidence changed our decisions
│   ├── size-of-the-prize.md     ← what empty seats are worth, from our own owner data
│   ├── blue-ocean.md            ← where we stop competing on price; what's hard to copy
│   ├── build-decision.md        ← go/no-go: what we build first, what we won't, kill criteria
│   ├── ai-usage-log.md
│   └── personas/
│       ├── persona-selection.md   ← why these personas, and the fate of the other 12 candidates
│       ├── selected_personas/     ← gym_goers, gym_owners, interview questions, oz-trials (example only)
│       └── hypothetical/          ← candidates not selected, kept for traceability
├── trial_1/                   ← first versions of opportunity, assumptions and goals (kept to show the evolution)
├── Venture_Skeleton _v0/      ← first skeleton page
└── prototype/
    └── prototype-v0.pdf
```

- **Evidence** (`evidence-log/`, Sessions 3–11): what do we know, and what supports it?
- **Constitution and feature spec** (`specs/`, Sessions 12–13): what we build next, and how we verify it.
- **Agent context** (`AGENTS.md`, `agents/`, Session 13): how AI agents work in this repo.

## How to use this repository
- **People:** start with this README, then `evidence-log/build-decision.md` (are we ready to build?), `evidence-log/blue-ocean.md` and `evidence-log/user-feedback.md`.
- **Coding agents:** read `AGENTS.md`, then `specs/`, before writing anything.
- **Persona rehearsal:** follow `agents/persona-agent.md`. Synthetic answers create questions, not evidence.

All AI assistance is logged in `evidence-log/ai-usage-log.md`.
