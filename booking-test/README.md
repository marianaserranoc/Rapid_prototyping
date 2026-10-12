# booking-test — two-version booking page for the reservation test

**What it is:** the page participants saw in the primary test (`evidence-log/experiment-card.md`). It is kept here so anyone can see exactly what was tested.

**Result (11–12 Oct 2026):** 25 people per version. Arm A 16/25 reserved (64%) vs. Arm B 7/25 (28%), +36 pp, one-sided Fisher p = 0.011. Details: `evidence-log/ab-test-results.md`.

**Live links**
- Arm A, no commitment: https://marianaserranoc.github.io/Rapid_prototyping/booking-test/#a
- Arm B, usual 3-class pack: https://marianaserranoc.github.io/Rapid_prototyping/booking-test/#b
- Without `#a` or `#b`, the page shows a team view to preview both versions.

## What each version shows

| | Arm A (`#a`) | Arm B (`#b`) |
|---|---|---|
| Class | Reformer Pilates, all levels · Tue 13 Oct, 11:00–11:50 · Maârif, Casablanca · coach Salma · 4 spots left | Same |
| Offer | **No commitment** · 300 MAD · 1 class · no pack or membership · pay at the studio | **Usual studio terms** · 900 MAD · 3-class discovery pack (300 MAD per class) · valid 1 month · pay at first class |
| Confirmation promise | Spot confirmed within minutes | Same |
| Actions | "Reserve my spot" / "Not for me" | Same |

Only the offer block differs. The studio, Atelier Sable, is fictional. The footer states it is a student test prototype with no online payment.

## How responses are collected
- **Reserve my spot** → first name → a pre-filled WhatsApp message to the team: `I'M RESERVING · Reformer Tue 13/10 11:00 · [name] · ref. S1`
- **Not for me** → reasons ticked (price, having to commit / buy a pack, not sure I'd get a spot, don't know the coach, the time, prefer my gym, other) → `NOT FOR ME · … · reason: … · ref. S2`
- **S1 = Arm A, S2 = Arm B.** The page stores nothing; the WhatsApp messages are the record.
- The team debriefs every person right after their message (no class booked, nothing charged) and asks for a 1-minute voice note on why.

## Ethics and privacy
- No payment details are collected, and no payment is taken.
- Participants are told it was a test immediately after they act.
- Names, numbers, screenshots and voice notes stay in the team's Teams folder, never in this repository. Results here use codes only.

## Files
- `index.html` — the full page (one file, no external services except Google Fonts and WhatsApp's `wa.me` link). The WhatsApp number is set in the `WHATSAPP_NUMBER` line of the script.

**Built with:** Claude (Claude Opus 5.5), 11 Oct 2026, logged in `evidence-log/ai-usage-log.md`.
