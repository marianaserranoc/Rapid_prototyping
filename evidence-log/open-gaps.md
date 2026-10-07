# Open Gaps and Experimental Limitations Log

> **Status:** Critical synthesis and methodological risk control document.  
> **Project:** Off-peak capacity optimization for independent boutique fitness studios in Morocco.

This document compiles the core business model contradictions, experimental limitations, and unvalidated empirical gaps (*Open Gaps*) identified throughout the project that must be resolved prior to committing to product development or software engineering.

---

## 1. Central Contradiction: The One-Off "Sampler" vs. Owner Retention Needs

There is an unresolved structural tension between what motivates the studio-goer and what the studio owner requires for viable business economics:

| Lens | Goer Perspective (*Student*) | Owner Perspective (*Studio Owner*) |
| :--- | :--- | :--- |
| **Primary Motivation** | **A one-off patch:** Attends another studio purely because their usual class was full or cancelled. Seeks to preserve their workout routine today without making any ongoing commitment. | **Predictability & retention:** Needs recurring attendance to reliably cover fixed monthly overhead (studio lease and instructor wages). |
| **Behavioral Outcome** | Has no organic intent to return weekly unless the exact same schedule mismatch reoccurs in their calendar. | Wants to avoid "class tourists" taking advantage of cheap drop-in slots without ever converting into full-price members. |

### Business Model Risk: *Trial-then-Vanish* vs. *Trial-then-Convert*
* **The Vulnerability:** If the low-commitment mechanism merely attracts users who attend once and disappear (*trial-then-vanish*), the model degenerates into a discounter or ClassPass-style aggregator. Studio owners actively resist aggregators because they devalue the studio brand, frustrate full-paying regulars, and erode margins without building local community.
* **Evidence Grounding Status:** **Unvalidated.** Current Wizard of Oz trials ([oz-trials.md](file:///Users/sofia/Desktop/Rapid%20Prototyping/evidence-log:/PERSONAS/oz-trials.md)) measured only single-instance booking intent. They did **not track repeat attendance or conversion rates over time**.
* **Required Next Test:** Run a 4–6 week longitudinal follow-up tracking whether first-time trial attendees subsequently purchase a standard package, book a second class at full price, or vanish permanently.

---

## 2. Experimental Design Limitations in Prior Testing

### A. Absence of a Direct A/B Test (10-Class Pack vs. Single Drop-in)
* **Limitation Identified:** In the price-vs-commitment test documented in [oz-trials.md](file:///Users/sofia/Desktop/Rapid%20Prototyping/evidence-log:/PERSONAS/oz-trials.md) (Persona 1), **no simultaneous A/B control arm was executed**.
* **Evidence Source:** The assumption that studio-goers reject 10-class packages was drawn solely from past qualitative interview recollections (G1 recalled buying a 10-pack, utilizing only 5–6 classes, and resolving never to prepay again). The actual card test presented only a single gym-equivalent price point (5 of 8 agreed to book).
* **Required Action:** Run a true concurrent two-arm test on matched cohorts (Arm A: Single class with zero commitment; Arm B: Standard 10-class package) to quantify the exact booking rate delta under identical visibility conditions.

### B. Unexecuted Primary Test in Morocco ([recruitment.md](file:///Users/sofia/Desktop/Rapid%20Prototyping/evidence-log:/recruitment.md))
* **Limitation Identified:** The primary behavioral experiment defined in [experiment-card.md](file:///Users/sofia/Desktop/Rapid%20Prototyping/evidence-log:/experiment-card.md) (10 real target attendees in Casablanca and Rabat testing for a $\ge 40$ percentage-point booking gap) **has no completed empirical results logged in this repository**.
* **Current Status:** [recruitment.md](file:///Users/sofia/Desktop/Rapid%20Prototyping/evidence-log:/recruitment.md) defines only the recruitment criteria and outreach timeline targeting September 23. Existing WoZ trial data reflects preliminary proxy tester runs, not the target Moroccan cohort.

---

## 3. Additional Open Validation Gaps

### Gap 1: Financial Risk vs. Instructor & Quality Trust
* **Context:** In [oz-trials.md](file:///Users/sofia/Desktop/Rapid%20Prototyping/evidence-log:/PERSONAS/oz-trials.md), among respondents who declined the gym-equivalent single-class card, one explicitly cited **not knowing the instructor** as the primary blocker.
* **Open Question:** Is the dominant booking barrier financial commitment (package cost), or is it quality uncertainty regarding the instructor and class environment? These point to fundamentally different product interventions (payment mechanics vs. instructor discovery and social proof).

### Gap 2: Undifferentiated Goer Segmentation
* **Context:** In [opportunity.md](file:///Users/sofia/Desktop/Rapid%20Prototyping/evidence-log:/opportunity.md), the "goer" is treated as a monolithic segment.
* **Open Question:** The dynamics differ dramatically across three distinct groups:
  1. *Net-new prospective goers:* Have never visited the studio before (high trust barrier).
  2. *Lapsed members:* Previously attended but churned (past experience, specific dropout reason).
  3. *Current peak-hour regulars:* Active members who currently avoid off-peak slots (schedule rigidity vs. habit).

### Gap 3: Modality Variance and Geographic Baseline
* **Context:** The opportunity assumes uniform boutique studio economics across disciplines and locations.
* **Open Question:**
  * Low-capacity, high-touch modalities (e.g., Reformer Pilates with 6–10 beds) operate under completely different margin structures than high-capacity disciplines (e.g., HIIT or spin with 25+ spots).
  * The market size calculation ([Fermi_estimate.txt](file:///Users/sofia/Desktop/Rapid%20Prototyping/evidence-log:/Fermi_estimate.txt)) relies on an unverified ratio of 1 boutique studio per 50,000 residents in Casablanca and Rabat.

### Gap 4: Acute Push vs. Learned Resignation on the Owner Side
* **Context:** In [JTBD.md](file:///Users/sofia/Desktop/Rapid%20Prototyping/evidence-log:/JTBD.md), the owner's pain is framed as an active, urgent push.
* **Open Question:** Following repeated past failures with discounting, have owners normalized empty off-peak classes into learned helplessness? If so, the hurdle to adoption is not just showing a better tool, but overcoming deep skepticism that off-peak slots can be filled at all without brand damage.

### Gap 5: Operational Bandwidth and Owner Control
* **Context:** Real owner interviews in [gym_owners.md](file:///Users/sofia/Desktop/Rapid%20Prototyping/evidence-log:/PERSONAS/gym_owners.md) emphasize that owners insist on absolute discretion over which slots/seats are opened and reject administrative overhead.
* **Open Question:** The exact operational workflow has not yet been designed: how can solo operators release surplus inventory in real-time without managing manual WhatsApp exchanges or disrupting their existing scheduling tools?
