# Experiment Card — Supporting Layers (alongside the Wizard of Oz behavioral test)

These three additions don't replace the Wizard of Oz test on Area 1 (goer regret-aversion) — they cover questions that test can't answer: owner adoption, whether the proxy sample resembles the real target population, and whether the result would even be plausible at market scale.

---

## Layer 1: Owner-side Interviews (Area 2 — owner adoption)

### Hypothesis
Independent boutique studio owners will perceive a low-commitment, risk-reduced off-peak trial mechanism as meaningfully different from a discount — and will be willing to offer it — rather than dismissing it as "discounting with extra steps."

### Method
Run an Interview (problem evidence) with 5–8 independent boutique studio owners (matching the USER profile: 15–25 classes/week, few instructors, owner sets the schedule) by presenting the low-commitment trial concept alongside a discount concept side by side, asking them to react to and distinguish between the two, and describe what they've already tried for off-peak slots and why it fell short.

### Metric
Count of owners who, in their own words, describe the trial concept as distinct from discounting and state willingness to offer it, out of total owners interviewed.

### Threshold
Clears if at least 5 of 8 interviewed owners (≥60%) both distinguish the concept from discounting and state willingness to offer it.

### Evidence strength
LOW-MEDIUM — real target users (actual studio owners, not proxies), but stated intent rather than observed adoption behavior; captures perception and willingness-to-consider, not follow-through if actually offered the mechanism.

### Decision rule
- **If threshold met (≥5 of 8):** CONTINUE — owner adoption is plausible; proceed to test the goer-side mechanism (Wizard of Oz) with real partner studios rather than proxies, since owners have shown willingness to host it.
- **If threshold missed (<5 of 8):** CHANGE — redesign the mechanism's framing or structure (e.g., different guarantee terms, different revenue-sharing model) and re-interview a fresh group, since adoption is the harder gate than goer behavior if owners won't offer it regardless of goer demand.
- **If ambiguous (e.g., owners distinguish it but hesitate on willingness, or vice versa):** CHANGE — follow up with the hesitant subset specifically to isolate whether the blocker is perception (still looks like a discount) or a separate concern (revenue risk, operational burden) not yet addressed.

---

## Layer 2: Goer-side Interviews (proxy-sample sanity check)

### Hypothesis
The proxy testers used in the Wizard of Oz test resemble real target studio-goers closely enough that their booking/attendance behavior is informative — i.e., no major factor specific to real studio-goers is missing from the test design.

### Method
Run a small set of Interviews (problem evidence) with 4–6 people matching the actual USER profile (studio-goers with flexible, non-habitual time who haven't committed to a studio/off-peak slot), conducted before or alongside the Wizard of Oz test, asking about their actual recent behavior around off-peak slots and any reason they wouldn't book one that the current hypothesis hasn't accounted for.

### Metric
Count of interviews surfacing a previously unconsidered barrier (a factor not covered by regret-aversion, timing/awareness, or absence-of-demand), out of total interviewed.

### Threshold
Clears (i.e., proxy sample is sound enough to proceed) if 0–1 of 4–6 interviews surface a genuinely new, unaddressed barrier. 2 or more triggers a redesign before running the main test.

### Evidence strength
MEDIUM — real target users, but stated recollection of past behavior/reasoning rather than observed behavior; useful for catching blind spots, not for validating the hypothesis itself.

### Decision rule
- **If threshold met (0–1 new barriers surfaced):** CONTINUE — proceed with the Wizard of Oz test as designed, using the existing proxy sample.
- **If threshold missed (2+ new barriers surfaced):** CHANGE — revise the Wizard of Oz test design (hypothesis, method, or both) to account for the newly surfaced factor(s) before running it, since the current design may be testing the wrong thing entirely.
- **Ambiguous branch:** not applicable — this is a simple count against a pre-set line.

---

## Layer 3: Market Research (generalization sanity check)

### Hypothesis
Existing data on studio churn/trial-conversion rates or Morocco fitness/wellness spending behavior will show that a regret-aversion/low-commitment dynamic is plausible at the market level — i.e., the proxy sample's behavior in the Wizard of Oz test is not wildly out of step with how the real market behaves.

### Method
Conduct a Technical spike–style desk research pass (not a live experiment with users): gather any available secondary data — studio-side churn/trial-conversion figures if a partner studio will share them, or published research/reports on Morocco's fitness and wellness spending habits — and compare general patterns (e.g., typical trial-to-membership conversion rates) against what the Wizard of Oz test produces.

### Metric
A qualitative fit assessment: whether the Wizard of Oz test's observed booking/attendance rate falls within a plausible range of whatever comparable published or studio-shared conversion benchmarks exist, rather than being a specific number to hit.

### Threshold
Clears if at least one credible data source is found and the Wizard of Oz result is not a dramatic outlier (e.g., not 10x higher or lower) relative to it. If no comparable data can be found at all, this layer is marked an open gap rather than forced to a conclusion.

### Evidence strength
LOW — secondary, aggregate data, not primary evidence about this specific mechanism; useful only as a rough plausibility check, not as confirmation or disconfirmation of the hypothesis.

### Decision rule
- **If threshold met (data found, result plausible):** CONTINUE — treat the Wizard of Oz result as reasonably credible pending the larger in-market test.
- **If threshold missed (data found, result is a dramatic outlier):** CHANGE — treat the Wizard of Oz result with more skepticism and prioritize running the larger, real-studio version sooner rather than scaling confidently on the proxy result alone.
- **If no data available at all:** mark as an open gap — proceed with the other layers' conclusions, but flag generalization confidence as unresolved rather than assumed.

---

## How the layers relate
- **Wizard of Oz (main test)** — tests the mechanism itself (does regret-aversion respond to risk removal), with real behavior but a small proxy sample.
- **Layer 1 (owner interviews)** — tests a completely separate risk (adoption) that no behavioral test on goers can substitute for.
- **Layer 2 (goer interviews)** — doesn't test the hypothesis; it checks whether the main test's sample and design are even asking the right question.
- **Layer 3 (market research)** — doesn't test the hypothesis either; it's a rough plausibility check on whether the main test's result could generalize.

None of these four pieces alone is sufficient to "know it will work" — together they cover mechanism, adoption, sample validity, and rough market plausibility, which is the most a Session 5–stage validation effort can realistically deliver before any building starts.
