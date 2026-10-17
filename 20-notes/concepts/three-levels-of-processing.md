---
type: concept
first_seen: week-01
source: "Norman, The Design of Everyday Things (Ch. 2)"
tags: [concept, week/01, norman, cognitive-psychology]
---

# Three Levels of Processing

*We react to design at three levels: gut feeling, skilled use, and reflective meaning.*

> [!abstract] At a glance
> **What:** Visceral, Behavioral and Reflective processing (Norman).
> **Why:** Good design must work at all three, not just the functional one.
> **See it:** A phone that looks gorgeous, responds fluently and makes its owner proud.

## Definition (my own words, ≤ 3 sentences)
Human cognition processes experiences at three neurological levels: **Visceral**, **Behavioral**, and **Reflective**. Visceral is pre-conscious and biological (how things look and feel); Behavioral is subconscious and habit-driven (how things perform and respond); Reflective is the only conscious level, governing interpretation, storytelling, self-image, and long-term memory. Great design must address all three layers in balance.

```
┌────────────────────────────────────────────────────────┐
│                      REFLECTIVE                        │
│   Conscious · Reasoning · Self-Image · Narrative       │
│   "Was this worth $1,200? What does this say about me?"│
└──────────────────────────▲─────────────────────────────┘
                           │
┌──────────────────────────┴─────────────────────────────┐
│                      BEHAVIORAL                        │
│   Subconscious · Learned Skills · Usability & Muscle   │
│   "Swiping up to unlock, blind typing, smooth flow"    │
└──────────────────────────▲─────────────────────────────┘
                           │
┌──────────────────────────┴─────────────────────────────┐
│                       VISCERAL                         │
│   Subconscious · Biological Affect · Immediate Senses  │
│   "Cold titanium frame, crisp button click, gorgeous"  │
└────────────────────────────────────────────────────────┘
```

> [!warning] Correction · 2026-10-18
> Two refinements. (1) "Universal across cultures" is too strong: Reinecke & Gajos (2014) found real cultural differences in visual preferences. An open research question for the visual design track (see `10-data/visual-design/curriculum.md`). (2) The upward arrows are misleading: Norman says influence flows **both ways**. Reflective judgments (brand, price) can change how something feels visceral-ly, and gut feeling colors reflection.

---

## Detailed Breakdown

### 1. Visceral Level (Appearance & Immediate Sensation)
- **Nature:** Pre-reflective, biological, largely shared across people (though aesthetic preferences also vary with culture and experience).
- **Triggered by:** Sight, sound, touch, smell, balance.
- **Design focus:** Aesthetics, material feel, sensory delight, physical responsiveness.
- **Example:** The satisfying magnetic *thud* of a luxury car door closing; the tactile resistance of a machined aluminum volume knob.

### 2. Behavioral Level (Use & Tactile Fluency)
- **Nature:** Subconscious, learned habits, motor schemas.
- **Triggered by:** Operating controls, typing, navigating, driving.
- **Design focus:** Usability, feedback immediacy, natural mappings, low cognitive load.
- **Example:** Blindly reaching for the turn signal while driving, or typing on a smartphone keyboard without consciously spelling each letter. When feedback is instantaneous and predictable, user experiences effortless "flow".

### 3. Reflective Level (Meaning & Personal Identity)
- **Nature:** **The ONLY conscious level.** Slow, deliberative, narrative-building.
- **Triggered by:** Post-action evaluation, pride, embarrassment, long-term memory.
- **Design focus:** Brand affinity, emotional satisfaction, justification of cost, prestige.
- **Example:** Wearing a mechanical watch that is less accurate than a digital quartz watch because of its heritage and personal pride.

---

## Why it matters for software engineers
Engineers are trained to optimize almost entirely for the **Behavioral** level (does the feature function efficiently?). But if the **Visceral** layer feels cheap, sluggish, or clunky, users form an immediate negative bias. And if the **Reflective** layer leaves users feeling anxious, judged, or stupid (e.g., intimidating terminal errors or deceptive subscription cancellation flows), they will hate the software even if the backend is technically flawless.

---

## Related concepts
- [[seven-stages-of-action]]
- [[slips-vs-mistakes]]
- [[feedback]]
- [[gulf-of-execution]]
- [[gulf-of-evaluation]]
