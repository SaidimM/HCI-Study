---
type: concept
first_seen: week-01
source: "Norman, The Design of Everyday Things (Ch. 1 & 2); Miller (1968)"
tags: [concept, week/01, norman, feedback, latency]
---

# Feedback

> *"Feedback—sending back information about what action has been done and what result has been accomplished—is a well-known concept in the science of control and information theory."* — Don Norman

![[feedback-latency.svg]]

---

## 1. Definition (my own words, ≤ 3 sentences)
Feedback is the immediate sensory return of information to the user confirming that an action was received, what effect it produced, and what state the system is currently in. It bridges the [[gulf-of-evaluation]] by converting invisible machine state changes into perceivable visual, auditory, or tactile signals. Without timely and proportionate feedback, users experience uncertainty, duplicate inputs, and self-blame.

---

## 2. Quantitative Cognitive Latency Limits

In human-computer interaction, "immediate" is strictly quantified by neurobiology and attention spans (Robert Miller 1968, Card/Moran/Newell 1983, Jakob Nielsen):

```
0 ms ───────[ 100 ms ]─────────────────[ 1.0 s ]───────────────────────[ 10.0 s ]───► ∞
                │                         │                                │
         VISCERAL / DIRECT         BEHAVIORAL FLOW                  ATTENTION LOSS
       Immediate causality;       Noticeable pause, but            Mind wanders; user
       feels instantaneous        train of thought is              switches tasks.
       (haptic click, keydown,    unbroken (page load,             Progress indicator
        direct slider drag)        simple search query)            or notify mandatory!
```

```
┌────────────────────────────────────────────────────────────────────────┐
│                        THE 3 RESPONSE-TIME LIMITS                      │
├────────────────────┬──────────────────┬────────────────────────────────┤
│ Threshold          │ Human Experience │ Interaction Requirement        │
├────────────────────┼──────────────────┼────────────────────────────────┤
│ **0.1 s (100 ms)** │ Instantaneous    │ Direct manipulation; no lag.   │
│ **1.0 s**          │ Thinking flow    │ Uninterrupted task context.    │
│ **10.0 s**         │ Attention lost   │ Percent bar or background job. │
└────────────────────┴──────────────────┴────────────────────────────────┘
```

---

## 3. Feedforward vs. Feedback

```
                    ┌───────────────────────────────┐
                    │     USER GOAL / INTENTION     │
                    └───────────────┬───────────────┘
                                    │
                  ┌─────────────────┴─────────────────┐
                  ▼                                   ▼
          [ FEEDFORWARD ]                       [ FEEDBACK ]
          (Before Action)                       (After Action)
          • "What *will* happen?"               • "What *just* happened?"
          • Hover button highlight              • Mechanical tactile click
          • Drag snap-to guidelines             • Loading spinner / progress
          • Ghost drop-target container         • Audio success chime
          • Cursor shape shift (grab/pointer)   • "Message Sent" toast banner
```

- **Feedforward:** Signals what to expect *before* committing the motor act, narrowing the [[gulf-of-execution]].
- **Feedback:** Communicates the outcome *after* the motor act, narrowing the [[gulf-of-evaluation]].

---

## 4. The 4 Cardinal Laws of Good Feedback

<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(220px, 1fr)); gap: 14px; margin: 16px 0;">

<div style="border: 1px solid #38bdf8; border-radius: 8px; padding: 14px; background: rgba(56,189,248,0.05);">
  <h4 style="margin: 0 0 8px 0; color: #7dd3fc;">1. Immediate (&lt;100ms)</h4>
  <p>Even if backend execution takes 5 seconds, sensory acknowledgment of the touch/click must fire within 100ms so the user knows the button registered.</p>
</div>

<div style="border: 1px solid #10b981; border-radius: 8px; padding: 14px; background: rgba(16,185,129,0.05);">
  <h4 style="margin: 0 0 8px 0; color: #34d399;">2. Informative</h4>
  <p>Feedback must explain <em>what occurred</em> in human terms. A flashing red LED or cryptic code (<code>Error 0x80070005</code>) provides zero diagnostic value.</p>
</div>

<div style="border: 1px solid #f59e0b; border-radius: 8px; padding: 14px; background: rgba(245,158,11,0.05);">
  <h4 style="margin: 0 0 8px 0; color: #fbbf24;">3. Proportionate</h4>
  <p>Minor, routine actions require subtle sensory cues (quiet click). Destructive or rare actions require salient, unignorable feedback (modal confirmation).</p>
</div>

<div style="border: 1px solid #ef4444; border-radius: 8px; padding: 14px; background: rgba(239,68,68,0.05);">
  <h4 style="margin: 0 0 8px 0; color: #f87171;">4. Restrained</h4>
  <p>Avoid excessive noise. Over-announcing every trivial system event leads directly to human habituation and dangerous <strong>Alarm Fatigue</strong>.</p>
</div>

</div>

---

## 5. The Pathology of Feedback Overload: Alarm Fatigue

```
┌────────────────────────────────────────────────────────────────────────┐
│                     THE FEEDBACK DESIGN SPECTRUM                       │
├────────────────────┬─────────────────────────────┬─────────────────────┤
│   ZERO FEEDBACK    │      OPTIMAL FEEDBACK       │    ALARM FATIGUE    │
├────────────────────┼─────────────────────────────┼─────────────────────┤
│ User is blind;     │ Salient, proportional cues; │ System screams 24/7;│
│ repeated clicks,   │ timely, unobtrusive         │ humans habituate &  │
│ anxious guesswork. │ reassurance.                │ silence all alerts. │
└────────────────────┴─────────────────────────────┴─────────────────────┘
```

When systems produce too much non-critical feedback (e.g., constant chirps in hospital Intensive Care Units, incessant lane-departure chimes in modern cars), the human brain naturally tunes out the auditory channel. 
- In medicine, **Alarm Fatigue** is recognized by the FDA as a leading cause of patient death—nurses silence or ignore monitors after hundreds of false alarms.
- In nuclear engineering, the **Three Mile Island** disaster was exacerbated by over 100 simultaneous blinking alarm annunciators, completely blinding operators to the true root cause.

---

## 6. Why it matters for software engineers
Engineers frequently build forms and asynchronous workflows with broken feedback loops:
- **The Frozen Button Slip:** A user clicks "Submit Order", but the button remains visually static while waiting for a 2-second Stripe API response. The user assumes the click missed and clicks three more times, submitting duplicate transactions.
- **The Optimistic UI Remedy:** Instantly render the expected success state (<100ms) while the background network request resolves, reverting gracefully only if a server error occurs.
- Designing feedback means treating **state visibility** as a first-class architectural requirement, not a cosmetic after-thought.

---

## Related concepts
- [[gulf-of-evaluation]]
- [[gulf-of-execution]]
- [[seven-stages-of-action]]
- [[signifier]]
- [[Conceptual Model, System Image and Real usage]]