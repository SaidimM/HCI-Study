---
type: concept
first_seen: week-01
source: "Norman, The Design of Everyday Things (Ch. 1)"
tags: [concept, week/01, norman, signifier]
---

# Signifier

## Definition (my own words, ≤ 3 sentences)
A signifier is any perceivable signal, mark, or physical trace that communicates the presence of an [[affordance]] or the state of a system to an agent. While an affordance determines what actions are physically possible, a signifier specifies **what** action can be taken, **where** that action should take place, **how** it should be performed, and **what state** the system is currently in. Signifiers can be deliberately designed or naturally emergent from use.

---

## The Four Questions a Signifier Answers

| Dimension | Question Answered | Everyday & UI Example |
|---|---|---|
| **What** | What action is possible? | A foot pedal on a trash can signifies foot actuation opens the lid (saving dirty hand contact). |
| **Where** | Where should the action take place? | A chrome push-plate on a door or a dual-flush button on a toilet tank signifies the exact physical contact target. |
| **How** | How should it be performed? | An Android **BottomSheet grabber** (a thin, grayish-black oval strip) indicates up/down dragging, reinforced by a quick introductory peek/bounce animation (**Animated Feedforward**). |
| **State** | What state is the system in? | An unread notification badge, a glowing kettle LED, or a locked indicator on a deadbolt. |

---

## Deliberate vs. Accidental Signifiers

1. **Deliberate Signifiers:** Explicitly crafted by designers to bridge the [[gulf-of-execution]] and [[gulf-of-evaluation]] (e.g., icons, labels, textured grips, audio chimes).
2. **Accidental / Incidental Signifiers:** Physical traces left by previous users or the environment that convey actionable meaning without deliberate design:
   - **Desire Paths:** Worn dirt tracks through grass signifying the shortest, preferred walking route.
   - **Fingerprint Smudges:** Smudges on touchscreens or glass doors indicating where previous people touched or pushed.
   - **Auditory Clues:** Whistling steam from a kettle indicating boiling water.

---

## Strong vs. Weak Signifiers (Norman's Rule)

> *"A door that needs a sign that says 'PUSH' or 'PULL' is a confession of design failure."* — Don Norman

- **Strong Signifiers (Visceral & Behavioral):** Convey meaning through intrinsic geometry, physical affordances, and spatial mapping (e.g., a flat plate that can only be pushed, a handle contoured for grasping). Operates subconsciously without reading.
- **Weak Signifiers (Reflective):** Rely on external text, labels, or manuals (e.g., stickers reading "PULL"). They force conscious cognitive translation and fail when language, lighting, or attention is compromised.

---

## The Screen Reality: Why Norman Apologized
In the 1988 edition of *The Design of Everyday Things*, Norman used "affordance" loosely, leading software engineers to declare: *"I designed an affordance for this button."*

In the 2013 revised edition, Norman explicitly corrected this:
- On a glass touch display, the **physical affordances are fixed**—the glass affords tapping, sliding, and pinching anywhere across its surface.
- A button drawn on a screen **has no physical affordance**; it is entirely a **signifier** signaling an underlying virtual capability.
- **The Flat Design Trap:** When designers stripped away drop shadows, borders, and bevels (e.g., early iOS 7), they removed critical signifiers, drastically widening the [[gulf-of-execution]] because users could no longer distinguish interactive elements from static labels.

---

## Why it matters for software engineers
Engineers frequently build powerful APIs and UI controls without intuitive signifiers, expecting users to "just know" or read documentation. If users struggle to locate where to click, guess whether an item is draggable, or miss destructive actions, the fault lies in missing or deceptive signifiers. Clear signifiers make virtual affordances discoverable.

---

## Related concepts
- [[affordance]]
- [[gulf-of-execution]]
- [[gulf-of-evaluation]]
- [[feedback]]
- [[seven-stages-of-action]]
