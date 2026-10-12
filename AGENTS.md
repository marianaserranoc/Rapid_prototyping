# AGENTS.md — rules for every AI agent in this repository

Read this file first in every session, then read the files it points to. If anything here conflicts with a request, stop and ask the team.

## 1. What this project is
A prototype that lets independent boutique studios in Casablanca and Rabat release chosen off-peak seats, at full price, to first-time visitors who book one class with no package and get an instant confirmation. The full intent is in `specs/mission.md`.

## 2. Read before you act
| Task | Read first |
|---|---|
| Any code | `specs/mission.md`, `specs/tech-stack.md`, the current feature folder in `specs/` |
| A new feature | `specs/roadmap.md`, then write `requirements.md`, `plan.md`, `validation.md` in a new `specs/YYYY-MM-DD-<feature>/` folder **before** code |
| Evidence or strategy files | The relevant file in `evidence-log/` and `evidence-log/open-gaps.md` |
| Persona rehearsal | `agents/persona-agent.md` |

## 3. Build rules
- **Specs before code.** Build only what the current `requirements.md` asks for. If something seems missing, propose a change to the spec; do not add it silently.
- **Validation first.** A task is done only when its checks in `validation.md` pass. Never weaken a check to make it pass.
- **No discounts, ever.** Never add promo codes, dynamic pricing, price suggestions or any price lower than the one the owner enters.
- **Owners stay in control.** Only the owner releases or withdraws seats. Never release, reprice or re-target seats automatically.
- **Regulars never see the offer.** Treat the member-list check as critical. Any change near it must rerun validation check D3.
- **No AI in the core flow.** Booking, seat counts, confirmation, prices and offer visibility are deterministic rules (`specs/tech-stack.md`, AI Fit Decision).
- **Minimal personal data.** First name and phone number only. Never log, print, commit or show one person's data to another.
- **No secrets in Git.** Keys, tokens and `.env` files stay out of the repository.
- **Small commits.** One requirement per commit, with the requirement number in the message (e.g. `R5: block bookings when seats run out`).
- **Record unknowns as TBD.** Don't guess a tool, a number or a user behaviour; write TBD and say what would decide it.

## 4. Evidence rules
- **Real users validate; AI explores.** Never present AI-generated, AI-simulated or Persona Agent output as user evidence.
- **Label every claim** as REPORTED, OBSERVED, STATED INTENT, DESK or HYPOTHESIS, consistent with `evidence-log/user-feedback.md`.
- **Don't invent** participants, quotes, numbers, dates, sources or model versions. If something is missing, say so.
- **Keep contradictions visible.** Don't smooth over evidence that weakens the riskiest assumption.

## 5. Logging
After any meaningful AI-assisted episode (code generated or reviewed, a spec drafted, evidence synthesised), propose a row for `evidence-log/ai-usage-log.md` using its six columns:
`Date | Tool & version | Stage/ Step | Use | Output used | Student's decisions`
Show the row to the team and write it only after they approve it.

## 6. Where things live
- `evidence-log/` — what we know and what supports it
- `specs/` — what we build and how we verify it
- `agents/` — rehearsal agents
- `prototype/` — the artifact being tested
- `downloads/` — the AI helper prompts used in the course
