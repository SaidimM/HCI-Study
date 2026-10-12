---
type: concept
first_seen: week-01
source: "Norman, DOET (Ch. 1); J.J. Gibson (1979)"
tags: [concept, week/01, norman, gibson, affordance]
---

# Affordance

## Definition (my own words, ≤ 3 sentences)
An affordance is the fundamental relationship between the physical properties of an object/environment and the physical capabilities of an interacting agent (human or animal). It defines what actions are physically possible, regardless of whether the agent perceives them or not. Affordances determine what *can* be done, but they do not specify *how* or *where* to do it—that is the role of a [[signifier]].

---

## Gibson vs. Norman: The Foundational Difference
- **J.J. Gibson (Ecological Psychology, 1979):** Coined the term. Affordances are purely objective, physical relationships. They exist independent of experience, culture, or perception.
- **Don Norman (HCI / Cognitive Design, 1988/2013):** In design, an affordance that cannot be perceived is useless. Norman emphasized **Perceived Affordances** and later clarified that designers rarely create new physical affordances; designers create [[signifier|signifiers]] to make affordances visible.

---

## Examples

### 1. The Relational Nature (Human vs. Cat)
A smartphone's physical properties interact differently depending on the agent:
- For a **human**, it affords one-handed gripping, touchscreen tapping, and voice communication.
- For a **domestic cat**, it affords swatting, resting on for warmth, or knocking off a table. It does *not* afford calling, because the cat lacks the physical and cognitive apparatus.

### 2. The Glass Door & Safety Decals (Actual vs. Perceived)
- **Actual Affordance:** A sheet of clear plate glass affords light transmission, but *blocks* physical passage.
- **Perceived Affordance without Signifier:** Because it is transparent, humans perceive empty space that affords walking through, leading to collisions.
- **The Redesign (Building Code Mandate):** Safety regulations require frosted stickers or logos at eye level (~1.4m). The sticker is a **signifier** that signals the presence of a solid physical barrier and indicates the swing/push area.

---

## Why it matters for software engineers
In software and web development, physical affordances are fixed: a monitor or touchscreen is a flat plane of glass that affords touching anywhere. On a screen, **you cannot build physical affordances—you design [[signifier|signifiers]] that represent virtual capabilities**. Misunderstanding this leads engineers to assume a UI is "naturally intuitive" when it actually just lacks the signifiers needed for users to discover features.

---

## Related concepts
- [[signifier]]
- [[gulf-of-execution]]
- [[seven-stages-of-action]]
- [[feedback]]
