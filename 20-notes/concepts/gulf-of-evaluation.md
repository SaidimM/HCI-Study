---
type: concept
first_seen: week-01
source: "Norman, The Design of Everyday Things (Ch. 2)"
tags: [concept, week/01, norman]
---

# Gulf of Evaluation

## Definition (my own words, ≤ 3 sentences)
The Gulf of Evaluation is the psychological gap between the physical state of the object and the user's perception and interpretation of that state. It reflects the mental effort required to answer: *"What state is the system in now, and did my action work?"* When a system provides immediate, understandable sensory feedback, this gulf is narrow.

---

## What causes the Gulf of Evaluation?
- **Delayed or absent feedback**: The user presses a button, but nothing lights up, vibrates, or sounds for several seconds.
- **Uninterpretable feedback**: System lights flash or cryptic error messages appear (e.g., `Error 0x80070005`) that provide zero clue as to whether the goal was fulfilled.
- **Mismatch between conceptual model and system image**: The system has changed its internal state, but its outward appearance gives no sensory sign of that change.

---

## Example
- **Good example**: 
  - In a microwave: as soon as the door closes and the knob turns, the interior lamp illuminates, a mechanical hum starts, and the turntable begins rotating. The user instantly knows the system is working.
  - In software: a checkout button transforms into a spinner, followed immediately by a distinct green checkmark and "Payment Confirmed" notification.
- **Bad example / violation**: 
  - A pedestrian crossing button with no LED or audio indicator. Pedestrians repeatedly press it multiple times wondering if their press registered.
  - A form submit button that freezes without any loading spinner, prompting users to double-click and submit duplicate transactions.

---

## How Designers Bridge the Gulf
1. **Immediate [[feedback|Feedback]]**: Acknowledge every interaction within 100ms.
2. **Explanatory Sensory Cues**: Use visual, auditory, and haptic modalities matched to human sensory perception (Visceral level).
3. **Transparent System Status**: Explicitly state system health and current progress, keeping the user's mental model in sync with reality.

---

## The Danger of User Self-Blame
When evaluation fails, users frequently accuse themselves: *"Did I press it wrong? Am I clumsy?"* Good design accepts that this is fundamentally an evaluation design failure: the system failed to communicate its status to human perception.

---

## Why it matters for software engineers
In distributed systems, asynchronous jobs, and frontend UI states, engineers must prioritize UI responsiveness. If an optimistic update fails or an API call takes 2 seconds with no loading skeleton/spinner, users will think the page is broken or frozen. Designing for the Gulf of Evaluation means making internal states transparently observable.

---

## Related concepts
- [[seven-stages-of-action]]
- [[gulf-of-execution]]
- [[feedback]]
- [[Conceptual Model, System Image and Real usage]]
