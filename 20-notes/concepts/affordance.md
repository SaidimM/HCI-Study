---
type: concept
first_seen: week-01
source: "Norman, DOET (Ch. 1); J.J. Gibson (1979)"
tags: [concept, week/01, norman, gibson, affordance]
---

# Affordance

*What an object makes possible for a particular agent; whether you can see it is a separate question.*

> [!abstract] At a glance
> **What:** A relationship between an object's properties and an agent's capabilities.
> **Why:** It separates what is *possible* from what is *visible*, so we can diagnose design failures.
> **See it:** Clear glass affords light but not passage; the decal is the signifier.

## Definition (my own words, ≤ 3 sentences)
An affordance is the fundamental relationship between the physical properties of an object/environment and the physical capabilities of an interacting agent (human or animal). It defines what actions are physically possible, regardless of whether the agent perceives them or not. Affordances determine what *can* be done, but they do not specify *how* or *where* to do it—that is the role of a [[signifier]].

---

> [!warning] Correction · 2026-10-18
> The earlier version called Gibson's affordances "purely objective". Both Gibson and Norman (2013) treat them as **relational**. The real difference: Gibson cares whether the possibility *exists*; Norman cares whether it can be *perceived and discovered*.

---

## Gibson vs. Norman: The Foundational Difference
- **J.J. Gibson (Ecological Psychology, 1979):** Coined the term. An affordance is a *relationship* between an animal and its environment. It exists whether or not it is perceived, but it is always defined relative to the animal. Gibson said it is neither purely objective nor purely subjective: it "cuts across the dichotomy of subjective-objective."
- **Don Norman (HCI / Cognitive Design, 1988/2013):** Also treats affordances as relational (2013). His contribution is the design question: an affordance that cannot be perceived is useless. Norman emphasized **Perceived Affordances** and later clarified that designers rarely create new physical affordances; designers create [[signifier|signifiers]] to make affordances visible.

---

## Examples

### 1. The Relational Nature (Human vs. Cat)
A smartphone's physical properties interact differently depending on the agent:
- For a **human**, it affords one-handed gripping, touchscreen tapping, and voice communication.
- For a **domestic cat**, it affords swatting, resting on for warmth, or knocking off a table. It does *not* afford calling, because the cat lacks the physical and cognitive apparatus.

### 2. The Glass Door & Safety Decals (Actual vs. Perceived)
- **Actual Affordance:** A sheet of clear plate glass affords light transmission, but *blocks* physical passage.
- **Perceived Affordance without Signifier:** Because it is transparent, humans perceive empty space that affords walking through, leading to collisions.
- **The Redesign (Building Code Mandate):** Safety regulations in many places require frosted stickers or logos at about eye level (exact height varies by jurisdiction; verify before citing a number). The sticker is a **signifier** that signals the presence of a solid physical barrier and indicates the swing/push area.

---

## Why it matters for software engineers
In software and web development, physical affordances are fixed: a monitor or touchscreen is a flat plane of glass that affords touching anywhere. On a screen, **you cannot build physical affordances—you design [[signifier|signifiers]] that represent virtual capabilities**. Misunderstanding this leads engineers to assume a UI is "naturally intuitive" when it actually just lacks the signifiers needed for users to discover features.

---

## Related concepts
- [[signifier]]
- [[gulf-of-execution]]
- [[seven-stages-of-action]]
- [[feedback]]
