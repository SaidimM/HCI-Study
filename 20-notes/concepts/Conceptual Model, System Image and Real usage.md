---
type: concept
first_seen: week-01
source: "Norman, The Design of Everyday Things (Ch. 1 & 2)"
tags: [concept, week/01, norman, mental-models, system-image]
---

# Conceptual Models & The System Image

> *"The designer’s conceptual model must match the user’s conceptual model. But the designer never talks directly to the user—everything is communicated through the System Image."* — Don Norman

![[conceptual-model-triad.svg]]

---

## 1. Definition (my own words, ≤ 3 sentences)
A **Conceptual Model** (or mental model) is an internal cognitive simulation of how a tool, device, or system works, enabling a person to predict actions and outcomes. Don Norman divides this into the **Design Model** (the engineer's conceptual model) and the **User's Model** (the user's mental model). Because creators cannot stand next to users, communication happens exclusively through the physical artifact, interfaces, and feedback—known collectively as the **System Image**.

---

## 2. Core Architecture: Norman's Asymmetric Triad

```
      [ DESIGNER ]                        [ USER ]
           │                                 ▲
    (Design Model)                     (User's Model)
           │                                 │
           └────────► [ SYSTEM IMAGE ] ──────┘
             (Physical Device / UI / Docs / Feedback)
```

```
┌────────────────────────────────────────────────────────────────────────┐
│                        THE LAW OF THE TRIAD                            │
├────────────────────────────────────────────────────────────────────────┤
│ 1. The Designer CANNOT talk to the User.                               │
│ 2. The User forms their entire mental model SOLELY from interacting     │
│    with the SYSTEM IMAGE (plus prior habits & metaphors).              │
│ 3. If the System Image fails to communicate the Design Model, the user │
│    creates a flawed model → resulting in systemic MISTAKES.            │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 3. The Three Pillars of the Triad

<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(260px, 1fr)); gap: 14px; margin: 16px 0;">

<div style="border: 1px solid #8b5cf6; border-radius: 8px; padding: 14px; background: rgba(139,92,246,0.05);">
  <h4 style="margin: 0 0 8px 0; color: #a78bfa;">1. The Design Model</h4>
  <p>The creator's deep theoretical conception of the product: schemas, state machines, mechanical linkages, and logic. The designer knows *why* every piece exists and how they relate.</p>
</div>

<div style="border: 1px solid #38bdf8; border-radius: 8px; padding: 14px; background: rgba(56,189,248,0.05);">
  <h4 style="margin: 0 0 8px 0; color: #7dd3fc;">2. The System Image</h4>
  <p>The <strong>only physical reality</strong> that exists in the world. It includes the industrial body, screen layout, button signifiers, error dialogues, audible hums, and instructions.</p>
</div>

<div style="border: 1px solid #10b981; border-radius: 8px; padding: 14px; background: rgba(16,185,129,0.05);">
  <h4 style="margin: 0 0 8px 0; color: #34d399;">3. The User's Model</h4>
  <p>The internal simulation developed in the user's mind through perception and experimentation. It guides all planning, execution, and evaluation in the [[seven-stages-of-action]].</p>
</div>

</div>

---

## 4. Classic Case Studies: When the System Image Fails

### Case A: The Thermostat Fallacy (Valve Model vs. Binary Switch)
- **The User's Model (The Valve Fallacy):** When a room is freezing, the user turns the dial to 30°C (86°F), believing the heater will pump out hotter air faster—just like turning a water faucet wider releases more water.
- **The Design Model (Binary Furnace Switch):** A thermostat is a binary bang-bang controller. The furnace is either 100% ON or 100% OFF. Setting it to 30°C does not accelerate warming; it only wastes fuel and overheats the house an hour later.
- **Why the System Image Failed:** A single dial with gradated numbers suggests a continuous throttle (valve). The system image provided zero visibility into the binary furnace state.

```
┌─────────────────────────────────┬─────────────────────────────────┐
│        USER'S VALVE MODEL       │      ACTUAL BANG-BANG MODEL     │
├─────────────────────────────────┼─────────────────────────────────┤
│ High Temp Dial ──► Blasts Fire  │ Heater is 100% ON or 100% OFF.  │
│ Low Temp Dial  ──► Trickle Fire │ Temp dial only sets target cutoff.│
│                                 │                                 │
│ Result: Dial set to 30°C in     │ Result: No speed boost; burns   │
│ hopes of heating twice as fast. │ energy & overshoots target.     │
└─────────────────────────────────┴─────────────────────────────────┘
```

### Case B: The Refrigerator Dual-Dial Mystery (DOET Ch. 1)
- **The Problem:** A refrigerator has two dials: one for the fresh food compartment (1–9) and one for the freezer (A–E).
- **The User's Model:** Dial 1 controls the fresh food cooling coil; Dial 2 controls the freezer cooling coil independently.
- **The Design Model:** There is **only one compressor and cooling coil**. One dial controls the thermostat cutoff; the other controls a mechanical flap dividing cold airflow between the two sections. Turning one dial alters the temperature of *both* compartments!
- **The Flaw:** The dials look completely independent. The System Image lied about the underlying physical relationship, making optimal calibration impossible.

---

## 5. Why it matters for software engineers
Software engineers regularly build user interfaces that mirror their **database architecture** rather than the **user's task mental model**:
- **Database Model (Design Model):** `UserEntity` has a foreign key to `TenantMembership`, which cascades into `RolePermissions`, requiring status validation.
- **User's Model:** *"I want to invite Sarah from my team to edit this document."*
- **The Failure Mode:** Forcing the user to understand database concepts (e.g., exposing raw API enum codes, requiring foreign key selection, or demanding multi-screen admin setup) offloads architectural complexity onto human users.
- **The Engineering Rule:** Design the System Image to reflect the **user's conceptual model of the task**, not the server's relational database schema.

---

## Related concepts
- [[gulf-of-execution]]
- [[gulf-of-evaluation]]
- [[slips-vs-mistakes]]
- [[seven-stages-of-action]]
- [[signifier]]
- [[feedback]]
