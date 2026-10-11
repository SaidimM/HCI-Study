---
type: concept
first_seen: week-01
source: "Norman, The Design of Everyday Things (Ch. 2)"
tags: [concept, week/01, norman]
---

# Seven Stages of Action

## Definition (my own words, ≤ 3 sentences)
Human action is a continuous feedback loop that starts with a high-level goal, executes across physical reality, and evaluates the outcome against expectations. The cycle consists of one goal stage, three stages of execution (Plan, Specify, Perform), and three stages of evaluation (Perceive, Interpret, Compare). When we are novice or encountering failure, these stages operate consciously and reflectively; when fluent, execution and evaluation slip into fast, automatic subconscious routines.

```
                  ┌───────── [ GOAL ] ─────────┐
                  │   Reflective / Conscious   │
                  ▼                            │
        [ PLAN (Intention) ]                   │
       Behavioral / Conscious                  │
                  ▼                            ▲
             [ SPECIFY ]                  [ COMPARE ]
       Behavioral / Subconscious     Reflective / Conscious
                  ▼                            ▲
             [ PERFORM ]                  [ INTERPRET ]
        Visceral / Motor Act         Reflective / Subconscious
                  ▼                            ▲
       ══════════════════════════════════════════════════════════
         GULF OF EXECUTION               GULF OF EVALUATION
       ══════════════════════════════════════════════════════════
                  ▼                            │
                  └──────► [ WORLD / STATE ] ──┘
                             (Physical Object)
                                     │
                                [ PERCEIVE ]
                              Visceral Sensory
```

---

## The 7 Stages (Walkthrough: Heating Food in a Microwave)

| Stage | Level of Processing | Mindset | Microwave Example |
|---|---|---|---|
| **1. Goal** | Reflective | Subconscious → Conscious | *"I feel hungry and need to satisfy my hunger."* |
| **2. Plan (Intention)** | Behavioral | Conscious | *"I will warm up some food to eat."* |
| **3. Specify** | Behavioral | Subconscious / Conscious | *"I will use the microwave in the kitchen for 2 minutes."* |
| **4. Perform** | Visceral (Motor) | Subconscious (if fluent) | Open door, insert bowl, shut door, turn the timer knob. |
| **5. Perceive** | Visceral (Sensory) | Subconscious | Look at the microwave: the interior light is OFF, no hum sound. |
| **6. Interpret** | Reflective | Subconscious → Conscious | *"The microwave isn't running; maybe the wall plug is loose."* |
| **7. Compare** | Reflective | Conscious | *"The food is still ice cold, and I'm still hungry. Goal not met."* |

---

## Subconscious vs. Conscious Processing
- **Subconscious**: Extremely fast, automatic, parallel, and handles skilled habits without mental strain—but prone to routine slips and blind spots.
- **Conscious**: Slow, deliberate, sequential, logical, and reflective—activated when facing novel situations, errors, or unexpected breakdowns.
- **Fluency shift**: First-time users move step-by-step through every single stage consciously. Expert users collapse Specify, Perform, Perceive, and Interpret into subconscious muscle memory until an unexpected failure breaks the loop.

---

## False Blame & Learned Helplessness
When users make an error during the 7 stages, they instinctively **blame themselves** (*"I must be dumb, I clicked the wrong button"*). In reality, the flaw is almost always in the **system design**—either the interface failed to signpost what to do (Gulf of Execution) or failed to show what happened (Gulf of Evaluation). Good design shoulders the blame so the user doesn't have to.

---

## Why it matters for software engineers
Engineers often test systems purely by checking if the backend executes the happy path, ignoring the cognitive journey. Understanding the 7 stages allows developers to diagnose the exact breakdown point: did the user fail to translate their goal into API-triggerable actions (Execution), or did the system fail to communicate state changes through immediate, comprehensible UI state (Evaluation)?

---

## Related concepts
- [[gulf-of-execution]]
- [[gulf-of-evaluation]]
- [[affordance]]
- [[signifier]]
- [[feedback]]
