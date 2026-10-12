# Persona Selection: from 12 candidates to the personas we use

**Updated:** 12 Oct 2026, in response to sprint feedback on personas ("explain why the critical profiles were chosen").
**Selected personas:** `selected_personas/gym_goers.md`, `selected_personas/gym_owners.md`
**Candidates not selected:** `hypothetical/` (kept for traceability, never cited as evidence)

---

## 1. How we did it

Each team member drafted persona hypotheses with AI help before and after the first interviews (`ai-usage-log.md`). That gave us **12 candidate files**: 7 goer profiles and 6 owner profiles. `Yacine_Personas.md` holds one of each, so it counts towards both sides.

We kept a candidate only if it passed all three tests:

| Test | Question we asked | Why it matters |
|---|---|---|
| **1. Grounded** | Does at least one real person we interviewed behave this way, in a specific recent episode? | Personas built on no one are fiction; the course asks for behaviour, not demographics |
| **2. Decision-relevant** | Does this persona's barrier change what we test or build? | A persona that doesn't change a decision is decoration |
| **3. Distinct** | Is its behaviour different from the personas already kept, or would merging lose nothing? | Fewer, sharper personas are easier to test against |

Named demographic profiles (age, job, name) were not a reason to keep a persona. Where a candidate was mostly demographic, we kept only its behavioural part.

## 2. What happened to each candidate

### Goer side

| Candidate file | Archetype | Grounded? | Fate | Reason |
|---|---|---|---|---|
| `ai-persona-Khaled-01.md` | Package-Wary Tryer | Yes: G1 (unused 10-pack, went to the gym instead) | **Selected → Persona 1** | Its barrier, not prepaying before knowing a studio, is our riskiest assumption itself. Since then also grounded by G5 |
| `persona-goer-yassin-01.md` | Uncommitted Last-Minute Booker | Yes: G2 (DM, no quick reply, gave up) | **Selected → Persona 2** | Its barrier, certainty of a spot, is the strongest rival explanation. It changed the test: confirmation was held constant in both arms. Since then also grounded by G4 |
| `Karimuser.md` | Unanchored Sampler | No grounded anchors (the file says so itself) | **Selected as Persona 3, then reverted to hypothesis (12 Oct)**; first real anchor from G6 (13 Oct) | It was briefly marked "grounded" via "Example-G3" and an example card trial, neither of which is real. It stays as a hypothesis because multi-studio samplers would be a different business, but nothing rests on it |
| `LeenGoer.md` | Unprompted Free-Window | Partly: 1 episode from G1 | **Merged** into Persona 1 and the JTBD trigger | Same person (G1) and same episode as Persona 1. Its insight, that the free window passes by default, became JTBD Circumstance A, so a separate persona added nothing |
| `persona-hypothesis-goer.md` | Group-Chat Explorer (tries studios with friends via group chats) | Not at the time. **Partly revived by G5** on 12 Oct (a friend inviting her to reformer) | **Merged** into JTBD Circumstance B (friend's invitation) | G5's path in is through a friend, which this candidate predicted. But G5's barriers (pack, nerves, gym already paid) are Persona 1's, so it's a second way into Persona 1, not a new persona. We'd split it out if more friend-led bookers appear in the pilot |
| `Mariana.md` | Gambler-Averse Regular (treats an unfamiliar class as a bet and skips) | No evidence base | **Dropped as a persona; its idea kept** as the regret-aversion hypothesis | The "booking feels like a bet" idea became the riskiest assumption we tested. But it describes **regulars** avoiding unfamiliar slots, and our offer is for **newcomers only** (owners' condition), so the profile is outside the target |
| `Yacine_Personas.md`, Persona 2 | Ghita, 28, freelance brand strategist | No: a named, demographic profile | **Dropped** | Its behaviour (flexible schedule, discovers on Instagram) is covered by Persona 2, which is grounded in two real people |

### Owner side

| Candidate file | Archetype | Grounded? | Fate | Reason |
|---|---|---|---|---|
| `ai-persona-Khaled-02.md` | Price-Integrity Protector | Yes: Owner A | **Selected → Owner Persona 1** | Refusing discounts is the reason our offer must be full price (ERRC Eliminate). Since then also grounded by Owner D |
| `persona-owner-yassin-02.md` | Capacity-Protective Studio Owner | Yes: Owner B | **Selected → Owner Persona 2** | Control over seats is her condition for saying yes, which became ERRC Create. Since then also grounded by Owner E (Karim) |
| `KarimOwner.md` | Manual Patcher | Not at the time; later matched by Owner C | **Selected → Owner Persona 3** | Owner C's wish to see who is new, without building it herself, became the new-vs-regular report. Owners D and E want the same |
| `LeenOwner.md` | Admin-Stretched Operator (bookings by hand on WhatsApp) | Partly: 1 owner interview | **Merged** into Owner Persona 3 and `open-gaps.md` Gap 9 | Same pain as the Manual Patcher (manual admin, no tracking). Kept as an open question: can owners release seats without new admin? |
| `persona-hypothesis-burned-gatekeeper.md` | Burned Gatekeeper (discounting went badly, watches attendance, wants control) | Its traits were later confirmed one by one by real owners | **Merged** into Owner Personas 1 and 2 | Every trait it predicted showed up in real owners, but split across the two personas we'd already grounded. As a separate persona it would duplicate them |
| `Yacine_Personas.md`, Persona 1 | Salma, 36, owner of Studio Nour | No: a named, demographic profile | **Dropped** | Its behaviour is covered by Owner Persona 1 |

**Summary:** 12 files → **6 selected** (3 goer, 3 owner), **5 merged**, **3 dropped** (Yacine's file counts once on each side). After sprint feedback, **5 of the 6 are grounded in real people** and 1 (Unanchored Sampler) is back to a hypothesis.

## 3. Why these are the critical profiles

Each selected persona maps to one decision in the venture. That's what makes them critical, not that they are the most common type:

| Persona | The decision it drives | Where you can see it |
|---|---|---|
| Goer 1: Package-Wary Tryer | **No pack** for newcomers (ERRC Reduce), the variable tested in the A/B test | `experiment-card.md`; result 16/25 vs. 7/25 |
| Goer 2: Last-Minute Booker | **Instant confirmation** (ERRC Raise), held constant in the test | `experiment-card.md` controls; `specs/tech-stack.md` |
| Owner 1: Price-Integrity Protector | **Full price, no discounts** (ERRC Eliminate) | `ERRC.md`; 5 of 6 owners |
| Owner 2: Capacity-Protective Owner | **The owner chooses the seats** (ERRC Create) | `specs/.../requirements.md` R1 |
| Owner 3: Manual Patcher | **New-vs-regular report**; seat release in one message | `specs/.../requirements.md`; `open-gaps.md` Gap 9 |
| Goer 3: Unanchored Sampler (hypothesis) | None yet; would matter if we widened to multi-studio passes | `gym_goers.md` |

## 4. How the personas changed with real evidence

| Date | Change | Caused by |
|---|---|---|
| Persona sessions | 12 AI-assisted candidates drafted by the team | Persona exercise (`ai-usage-log.md`) |
| After first interviews | 6 selected using the three tests above; others merged or dropped | G1, G2, Owners A–C |
| 11 Oct | Persona 3 marked "grounded" | ⚠ An example interview and example card trial, **not real people** |
| **12 Oct** | Persona 3 **reverted to hypothesis**; card-trial claims removed from Personas 1 and 2 | Sprint feedback ("keep examples as examples") |
| **12 Oct** | Persona 1 gains G5; Persona 2 gains G4; Owner Personas 1 and 2 gain Owners D and E | New real interviews (Khaled, Yassin) |
| **12 Oct** | Persona 1's barrier confirmed at group level | A/B reservation test (+36 pp for no pack) |
| **12 Oct** | The "Group-Chat Explorer" idea partly revived as JTBD Circumstance B | G5 (friend's invitation) |
| **13 Oct** | Persona 1 gains G7 (habit) and G8 (Casablanca; turned away by a monthly-only box) | New real interviews (Sofía, Leen) |
| **13 Oct** | Persona 3 gets its first real anchor (wants variety; finds single classes too expensive). Still a hypothesis at n=1 | G6 (Mariana's interview) |

## 5. What would make us change the selection
- **Add a persona** if 2 or more pilot bookers arrive through a friend and behave differently from Persona 1 (a separate Group-Chat Explorer).
- **Ground or drop Persona 3** after 1–2 interviews with people who rotate between studios.
- **Add a non-gym-member goer** if the pilot shows people without a gym behave differently (all our grounded goers who mention a gym are members).
