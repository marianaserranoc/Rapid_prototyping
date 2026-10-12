# Test Brief — reservation A/B test and interviews

*Use this to brief teammates, or paste it into an AI assistant. Every number under "Scenarios" is a planned reading of a possible outcome, written before the test. The real result is in §2 "What happened".*

---

## 1. Project context (one minute)

**Course:** Rapid Prototyping with AI, IE University. Group Project I on 13–15 Oct 2026 grades evidence from real users and how it changes our decisions.

**Venture:** independent boutique fitness studios in Casablanca and Rabat (yoga, pilates, reformer, boxing) have recurring off-peak classes that run half empty. Rent and instructor pay are fixed, so every empty seat is lost money. Owners have tried discounts, but discounts attract deal-hunters and upset regulars (5 real owner interviews).

**Our idea:** owners release chosen off-peak seats **at full price, to new clients only**; newcomers book **one class with no pack or membership** and get a **confirmed spot within minutes**.

**Riskiest assumption:** newcomers avoid booking mainly because buying a pack before trying a studio feels like a bad bet (**regret-aversion**), not because of price, timing or uncertainty about getting a spot.

**Why it was contested before the test:**
- G2 and G4 each abandoned a booking because nobody replied quickly (certainty, not risk).
- One boutique class (250–400 MAD) costs about a month of gym (~314 MAD), so price may be the barrier.
- NOVA's founder (Egypt) says a subscription failed but **credit packs sold**, so people may only reject *recurring* commitment.

---

## 2. The A/B reservation test

### What it is
A fake-door test: a real-looking booking page for a class that doesn't exist, used to see whether people take a real action (reserving), not just say they would.

| | Arm A — no commitment | Arm B — usual studio terms |
|---|---|---|
| Link | `marianaserranoc.github.io/Rapid_prototyping/booking-test/#a` | same page, `#b` |
| Class | Reformer Pilates, Tue 13 Oct 11:00, fictional studio "Atelier Sable", Maârif, 4 spots left | same |
| Offer | **300 MAD, 1 class, no pack** | **900 MAD, 3-class discovery pack** (300 MAD/class, valid 1 month) |
| Confirmation promise | Spot confirmed within minutes | same |
| Only difference | | **Commitment** (price per class is identical) |

### How it runs
1. Recruit 25 people per arm (target **20 per arm completed, minimum 15**), regular boutique class-goers in Casablanca and Rabat, via three channels: Moroccan classmate's network, other Moroccan IE students' contacts, and referrals.
2. Alternate A/B in order of contact and **log the arm before sending**.
3. Each person taps **Reserve my spot** (enters first name) or **Not for me** (ticks reasons: price · having to commit/buy a pack · not sure I'd get a spot · don't know the coach · the time · prefer my gym · other).
4. The page sends a pre-filled WhatsApp message to +34 674 868 222 ending in **ref. S1 (A)** or **ref. S2 (B)**.
5. The team replies straight away: it was a student test, nothing was booked or charged, and could they send a **1-minute voice note** on why they said yes or no.
6. Anyone who doesn't reply counts as "did not reserve".

### Metric and rule (set before testing)
- **Reservation rate** per arm = reservations ÷ links sent.
- **Supports:** A is **≥30 pp** above B **and** Fisher's exact test (one-sided) p < 0.05. At 20 per arm that means roughly A ≥9/20 vs. B ≤3/20; at 15 per arm, about a 40 pp gap.
- **Against:** gap **under 15 pp**.
- **Inconclusive:** 15–29 pp, or ≥30 pp without p < 0.05 → send to 10 more per arm, then decide.

### Scenarios and how we would read them

| Scenario | Example pattern (20 per arm) | How we'd read it | Decision |
|---|---|---|---|
| **Ideal for our idea** | A 10/20 (50%), B 2/20 (10%), gap 40 pp, p < 0.05; B decliners mostly tick "having to commit / buy a pack" | Removing the pack drives reservations: regret-aversion holds | **Continue:** pilot with 2–3 real studios, measure attendance and return at full price |
| **Plausible: packs are fine** (fits NOVA's experience) | A 7/20, B 5/20, gap 10 pp | One-off packs aren't the barrier; only subscriptions might be | **Pivot:** decline reasons pick the direction (below) |
| **Plausible: certainty is the barrier** (fits G2 and G4) | Small gap; decliners in both arms mostly tick "not sure I'd get a spot" | Commitment isn't the issue; speed and certainty of booking are | **Pivot to certainty:** instant booking for studios' existing classes |
| **Plausible: price is the barrier** (fits "one class ≈ a month of gym") | Low reservations in both arms; most tick "price" or "prefer my gym" | 300 MAD for one class is too much next to a paid gym | **Pivot on price:** test a new-clients-only first-visit price with owners |
| **Plausible: trust is the barrier** (fits NOVA's influencer/word-of-mouth point) | Small gap; many tick "don't know the coach" | People need social proof before trying | **Pivot to trust:** coach profiles, short videos, reviews, influencer and referral channels |
| **No demand for that slot** | Almost no one reserves in either arm | Tuesday 11:00 may just be the wrong time | **Change the slot** and rerun |
| **In between** | A 8/20, B 4/20, gap 20 pp | Direction looks right, but it could be chance | **Extend:** 10 more per arm, then decide |

*Honest expectation (written before the test):* given G2 and NOVA's experience, a **small gap** with certainty or price as the top reasons is at least as likely as the ideal result. Either outcome is useful: the pivot branches are written in advance.

### What happened (11–12 Oct 2026)
25 per arm. **Arm A 16/25 (64%) vs. Arm B 7/25 (28%), +36 pp, one-sided Fisher p = 0.011.** This matches the **"Ideal for our idea"** row: **Continue.** Decline reasons (27): having to commit / buy a pack 10, price 5, prefer my gym 5, time 4, coach 2, certainty 1. Price plus gym equals commitment, so price is the first thing to watch in the pilot. Full log: `evidence-log/ab-test-results.md`.

### Limits to state when presenting
- A reservation is not attendance; the studio is fictional; nothing was paid.
- Participants come from a few personal networks, and assignment isn't random.
- Detects a large gap (~30 pp), not a small one.

---

## 3. Voice notes (debrief after every reply)

### Questions (asked in this order, no suggested answers)
1. Why did you say yes or no?
2. Was it the price, having to commit, not being sure you'd get a spot, or not knowing the coach? *(each separately)*
3. Do you already pay for a gym or a pack somewhere?
4. *(If they reserved)* What would make you go back at the normal price?

### What we listen for

| Signal in what they say | Supports | Weakens |
|---|---|---|
| Talks about not wanting to buy a pack, wasting money on unused classes, "I'd want to try first" | Regret-aversion (our idea) | — |
| Talks about not knowing if they'd really get in, wanting a quick answer | Certainty rival | Regret-aversion |
| Compares to their gym or says it's expensive | Price rival | Regret-aversion |
| Mentions the coach, reviews, a friend who goes, Instagram | Trust / social-proof rival | — |
| Says subscriptions put them off but a pack is fine | NOVA's finding (recurring vs. one-off) | "Any prepayment is the barrier" |
| Says the time doesn't work | No demand for that slot | — |

**How to log:** one row per person in the tracker (code, arm, reserved Y/N, reasons ticked, voice note Y/N, main theme). Quote 2–3 short anonymised lines in `user-feedback.md`; keep audio in Teams, never in GitHub.

---

## 4. Owner interviews (Owners D and E done 12 Oct; 1–3 more)

### Questions
1. Which is your quietest class, and how many people usually come?
2. What have you tried to fill it, and what happened?
3. *(Show the no-pack offer next to a discount)* How are these different for you, if at all?
4. Would you release 2 seats in that class next week to new clients only, at your normal price? What would stop you?
5. Do you sell a discovery or trial pack? Does it bring people to off-peak classes?
6. Show me how you manage bookings today. *(Watch; don't help.)*
7. If someone brought you new clients, what fee would feel fair?
8. *(From NOVA)* Have you seen platforms like this before? What would make you trust a new one?

### Scenarios

| Scenario | What we'd hear | How we'd read it | Decision |
|---|---|---|---|
| **Ideal** | Names a specific quiet class; says discounts backfired; agrees to release seats **on a date**; can release them in minutes | Owner adoption is real (not just polite interest) | Recruit as a Phase 2 pilot studio |
| **Plausible: interested but sceptical** | "Sounds good, I've seen apps like this before, let's see" (NOVA's point) | Credibility, not the offer, is the barrier | Bring an instructor or studio insider into the next conversation; come back with proof |
| **Plausible: discovery packs already work** | "My trial pack already fills it" | Our closest competitor is good enough for this owner | Ask why off-peak specifically stays empty; may narrow to studios without trial packs |
| **Plausible: control or admin is the blocker** | "Only if I choose the seats" / "I don't have time for another tool" | Matches Owners B and C | Keep seat release to one WhatsApp message; owner always chooses |
| **Against** | "It's a discount in disguise" or no interest at all | ERRC Eliminate/Create moves don't convince | Rework the owner offer before building anything |

**Rule:** only a commitment to a date counts as adoption evidence. "Maybe" is logged as interest.

---

## 5. Expert interview (done): NOVA founder, Egypt
- Studios had seen similar ideas fail; they trusted NOVA because a co-founder is an instructor and the team was committed; the win-win was easy to understand.
- A credit **subscription** failed at first; credit **packs** worked.
- Influencer marketing and word of mouth drove growth.
- Launched at the right moment: a pilates and Hyrox boom in Egypt.
- *Expert evidence from an analogous market, not our target users. One person, no figures.*

---

## 6. After results come in
Update, in this order:
1. `experiment-card.md` (results table, outcome, decision)
2. `user-feedback.md` (counts, reasons, quotes)
3. `pivot-log.md` §4 (which branch was triggered)
4. `README.md` (decision line)
5. `ai-usage-log.md` (if AI helped analyse)

**Prompt for an AI assistant, once you have real data:**
> Here is our test brief and our real results [paste tracker: code, arm, reserved, reasons, voice-note themes]. Compute the reservation rate per arm, the gap and a one-sided Fisher's exact p-value. Say which pre-written scenario and decision branch the results match, and list the top decline reasons per arm. Use only the data provided; flag anything missing instead of estimating it.
