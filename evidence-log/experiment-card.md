# Experiment Card

## Hypothesis
Peak-only boutique fitness users will book and attend at least one off-peak class within 7 days when shown a short list of available off-peak options (not just one suggested slot), delivered via a non-monetary nudge.


## Method
Run a Concierge experiment with peak-only boutique fitness users by manually reaching out via WhatsApp/DM with a short, personalized list of available off-peak options (e.g., 2-3 classes across different times/studios), framed as a non-monetary nudge (priority access or social accountability matching), and manually coordinating their booking, to observe whether users actually book and attend at least one off-peak class within 7 days.

## Metric
Measure booking rate as the count of users who book an off-peak class slot within 7 days of receiving the nudge, out of total users contacted.

## Threshold
The test clears the threshold if at least 3 out of 5 contacted users (≥60%) book an off-peak class slot within 7 days of direct concierge outreach via WhatsApp/DM.

## Evidence strength
MEDIUM — the test observes real booking and attendance behavior (not just stated interest), but relies partly on proxy users outside Morocco and a small sample size (5 people), which limits how confidently the result generalizes to the actual target market.

## Decision rule
- **If threshold met (≥ 3 of 5 book):** CONTINUE by running a 10-user version of this test using a real studio's actual schedule, to check whether the effect holds at a larger scale and whether the studio can keep up with real bookings (Assumption #7), before writing any code.
- **If threshold missed (< 3 of 5 book):** CHANGE by re-running the test with a small group, offering a discount instead of a non-price nudge, to determine whether demand is purely price-sensitive rather than schedule-elastic, or structurally absent regardless of offer.
- **If ambiguous (e.g., exactly 2 of 5 book, or a user books but doesn't show up):** CHANGE by running one more 5-user round that isolates priority access from social accountability matching, to evaluate whether either nudge works independently.

## Intentional exclusions

To keep this test minimal and code-free, the following were deliberately excluded from Experiment Card v0:

- Studio-side real-time calendar/API integration
- Payment processing
- Dynamic pricing or automated discounting logic
- A custom mobile or web app — outreach and booking are done manually via WhatsApp
- Automated matching algorithms — nudges (priority access, social matching) are manually selected and sent per user
- Real-time availability tracking — the "available" options listed are manually curated by us for each message, not pulled from any live schedule or system

Ready to add this as a new section at the end of experiment-card.md. Want to move on to
