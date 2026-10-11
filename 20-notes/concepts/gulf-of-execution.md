---
type: concept
first_seen: week-01
source: "Norman, The Design of Everyday Things (Ch. 2)"
tags: [concept, week/01, norman]
---

# Gulf of Execution

## Definition (my own words, ≤ 3 sentences)
The Gulf of Execution is the psychological gap between the user's intended goal/plan (the Behavioral stage) and the physical actions the system allows them to perform. It answers the user's silent question: *"How do I operate this device to achieve my intention?"* A designer's primary job is to bridge or eliminate this gulf using clear signifiers, affordances, constraints, and mappings.

---

## What causes the Gulf of Execution?
- **Missing or deceptive signifiers**: The user does not know which affordance to manipulate (e.g., a flat push-door that looks like it needs to be pulled).
- **Complex action mapping**: The required input does not naturally correspond to the intended output (e.g., four stove burner knobs arranged in a single row for four square burners).
- **Excessive cognitive translation**: The user has to convert a simple intention (*"heat food for 2 minutes"*) into a complex ritual (pressing `Power Level`, `100%`, `Time Cook`, `0-2-0-0`, `Start`).

---

## Example
- **Good example**: A light switch or sliding dimmer next to a lamp, or a prominent, well-labeled primary CTA button on a checkout page. The user forms an intention and instantly knows what physical/digital action triggers it.
- **Bad example / violation**: A microwave where heating a cup of milk requires consulting a cryptic numerical code list hidden on the inside frame of the door.

---

## How Designers Bridge the Gulf
1. **Strong [[signifier|Signifiers]]**: Clearly show *where* and *how* to touch, click, or turn.
2. **Natural Mappings**: Match controls spatially to the items being controlled.
3. **Constraints**: Prevent invalid physical or digital actions before they happen.
4. **Feedforward**: Let the user preview what will happen before committing the action.

---

## Why it matters for software engineers
When engineers build forms, CLI commands, or APIs, they often design around database models rather than user intentions. If a user wants to "cancel a subscription" but has to navigate through `Account Settings → Billing → Invoices → Preferences → Edit Tier → Downgrade`, the huge Gulf of Execution frustrates the user and generates customer support tickets.

---

## Related concepts
- [[seven-stages-of-action]]
- [[gulf-of-evaluation]]
- [[signifier]]
- [[affordance]]
