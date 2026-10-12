# A/B Reservation Test — results log

**Test:** two-version booking page (`booking-test/`), Reformer Pilates at the fictional studio Atelier Sable, Tue 13 Oct 11:00. Arm A = 300 MAD, 1 class, no pack (ref. S1). Arm B = 900 MAD, 3-class pack (ref. S2). Design, threshold and decision rule: `experiment-card.md`.
**Ran:** 11–12 Oct 2026, after the page went live · **Recruited:** 25 per arm through the team's Moroccan contacts (`recruitment.md`). Exact send times are in the WhatsApp log; they are not reproduced here.
**Source of truth:** the WhatsApp messages received on the test number (each ends in ref. S1 or S2) and the voice notes. They stay in the team's Teams folder; this file uses codes only.

---

## 1. Summary

| | Arm A (S1) | Arm B (S2) |
|---|---|---|
| Links sent | 25 | 25 |
| Reserved | 16 | 7 |
| Did not reserve | 9 | 18 |
| Reservation rate | 64% | 28% |

**Gap:** +36 percentage points · **Fisher's exact test, one-sided:** p = 0.011 (odds ratio 4.6) · **Pre-set bar:** ≥30 pp and p < 0.05 → **met (Supports)**.

**Reasons for not reserving** (27 people, main reason each):

| Reason ticked or said | Total | Arm A | Arm B |
|---|---|---|---|
| Having to commit / buy a pack | 10 | 0 | 10 |
| Price | 5 | 3 | 2 |
| Prefer my gym | 5 | 3 | 2 |
| The time | 4 | 2 | 2 |
| Don't know the coach | 2 | 1 | 1 |
| Not sure I'd get a spot | 1 | 0 | 1 |
| **Total** | **27** | **9** | **18** |

**What the split shows:** all 10 "having to commit" declines came from Arm B, the only arm with a pack. Price and gym declines are spread across both arms (A 6, B 4), so price is a real barrier, but it doesn't explain the gap between arms.

**Voice notes received:** 29 of 50 (Arm A 15, Arm B 14). Audio stays in Teams.

## 2. Voice-note quotes (word for word, anonymised)
Only lines a participant actually said. No AI paraphrases.
- [code, arm, reserved Y/N]: "…"
- [code, arm, reserved Y/N]: "…"
- [code, arm, reserved Y/N]: "…"

## 3. How the numbers were checked
- p-value computed with `scipy.stats.fisher_exact([[16, 9], [7, 18]], alternative="greater")` → 0.0111. Two-sided p = 0.022.
- The team's results summary was formatted with ChatGPT; the counts above come from the team's WhatsApp log. Quotes are not taken from the AI summary (`ai-usage-log.md`).

## 4. Per-participant log
One row per person, from the WhatsApp log (codes only; order as logged). Totals match section 1: Arm A 16 reserved of 25, Arm B 7 of 25.

| Code | Arm | Reserved (Y/N) | Main reason if not |
|---|---|---|---|
| A01 | A (S1) | Y | — |
| A02 | A (S1) | Y | — |
| A03 | A (S1) | N | Price |
| A04 | A (S1) | Y | — |
| A05 | A (S1) | Y | — |
| A06 | A (S1) | N | Prefer my gym |
| A07 | A (S1) | Y | — |
| A08 | A (S1) | Y | — |
| A09 | A (S1) | N | The time |
| A10 | A (S1) | Y | — |
| A11 | A (S1) | Y | — |
| A12 | A (S1) | N | Price |
| A13 | A (S1) | Y | — |
| A14 | A (S1) | N | Prefer my gym |
| A15 | A (S1) | Y | — |
| A16 | A (S1) | Y | — |
| A17 | A (S1) | N | The time |
| A18 | A (S1) | Y | — |
| A19 | A (S1) | N | Don't know the coach |
| A20 | A (S1) | Y | — |
| A21 | A (S1) | Y | — |
| A22 | A (S1) | N | Prefer my gym |
| A23 | A (S1) | Y | — |
| A24 | A (S1) | N | Price |
| A25 | A (S1) | Y | — |
| B01 | B (S2) | N | Having to commit / buy a pack |
| B02 | B (S2) | N | Having to commit / buy a pack |
| B03 | B (S2) | Y | — |
| B04 | B (S2) | N | Price |
| B05 | B (S2) | N | Having to commit / buy a pack |
| B06 | B (S2) | N | Prefer my gym |
| B07 | B (S2) | Y | — |
| B08 | B (S2) | N | Having to commit / buy a pack |
| B09 | B (S2) | N | The time |
| B10 | B (S2) | N | Having to commit / buy a pack |
| B11 | B (S2) | Y | — |
| B12 | B (S2) | N | Don't know the coach |
| B13 | B (S2) | N | Having to commit / buy a pack |
| B14 | B (S2) | N | Prefer my gym |
| B15 | B (S2) | Y | — |
| B16 | B (S2) | N | Having to commit / buy a pack |
| B17 | B (S2) | N | Price |
| B18 | B (S2) | N | Having to commit / buy a pack |
| B19 | B (S2) | Y | — |
| B20 | B (S2) | N | Not sure I'd get a spot |
| B21 | B (S2) | N | Having to commit / buy a pack |
| B22 | B (S2) | Y | — |
| B23 | B (S2) | N | The time |
| B24 | B (S2) | N | Having to commit / buy a pack |
| B25 | B (S2) | Y | — |
