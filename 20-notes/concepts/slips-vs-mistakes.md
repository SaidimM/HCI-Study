---
type: concept
first_seen: week-01
source: "Norman, The Design of Everyday Things (Ch. 2)"
tags: [concept, week/01, norman, human-error]
---

# Slips vs. Mistakes

*A slip is the right plan done wrong; a mistake is the wrong plan done right.*

> [!abstract] At a glance
> **What:** Slips are execution errors; mistakes are goal or plan errors.
> **Why:** They need different design remedies: layout and constraints for slips, clear models for mistakes.
> **See it:** Hitting the wrong adjacent key vs. setting a thermostat to 30 C to heat faster.

## Definition (my own words, ≤ 3 sentences)
Human errors are fundamentally divided into **Slips** and **Mistakes**. A **Slip** occurs when the user has the correct goal and plan, but the subconscious motor execution fails or acts incorrectly (e.g., clicking the wrong adjacent button). A **Mistake** occurs when the user forms the wrong goal or plan due to an inaccurate mental model, even though they execute their planned actions with perfect physical precision.

```
                    ┌─────────────────────────┐
                    │      USER INTENTION     │
                    └────────────┬────────────┘
                                 │
                 Is the Goal / Plan correct?
                   /                       \
             [ YES ]                       [ NO ]
                │                             │
    Execution fails in motor act     Plan is based on false model
        (Subconscious / Behavioral)      (Conscious / Reflective)
                │                             │
          ▼     ▼                       ▼     ▼
          ▶   SLIP   ◀                  ▶  MISTAKE  ◀
    (Accidental typo, missed key,   (Setting thermostat to 30°C to heat
     clicking wrong adjacent icon)    faster; adding oil when belt broke)
```

---

## Detailed Comparison

| Dimension | Slip | Mistake |
|---|---|---|
| **Underlying Cause** | Lapses in attention, habit intrusion, fatigue, or clumsy proximity | Inaccurate mental model, misunderstanding system rules |
| **Stage of Action** | **Specify** or **Perform** (Execution stages) | **Goal** or **Plan** (Planning stages) |
| **Cognitive Level** | **Behavioral** (Subconscious routines) | **Reflective** (knowledge-based) or **Behavioral** (rule-based) |
| **User Awareness** | Often detected immediately via feedback (*"Oops, that slipped!"*) | Hard to detect; user believes they did the right thing until system fails |

> [!warning] Correction · 2026-10-18
> The note omitted Norman's subtypes. Verify wording against DOET Ch. 5 before citing.

```
┌─────────────────────────────┬──────────────────────────────────────────┐
│ SLIPS (right goal, bad act) │ MISTAKES (wrong goal or plan)            │
├─────────────────────────────┼──────────────────────────────────────────┤
│ Action-based slip           │ Rule-based mistake (wrong rule applied)  │
│  (capture, description,     │ Knowledge-based mistake (wrong model)    │
│   mode-error slips)         │ Memory-lapse mistake (forgot a step      │
│ Memory-lapse slip           │  while planning)                         │
│  (forgot a step in action)  │                                          │
└─────────────────────────────┴──────────────────────────────────────────┘
```

---

## Real-World Case Studies

### 1. Scene A — Accidental Deletion (The Slip)
- **Scenario:** A user wants to delete a single selected file, but hits "Delete All" or accidentally presses Delete instead of Backspace because they are adjacent on the keyboard layout.
- **Why it's a Slip:** The intention was completely correct. The subconscious motor hand movement slipped.
- **Design Remedy:**
  - **Spatial Separation:** Physically move destructive actions away from everyday actions.
  - **Forcing Functions & Constraints:** Require a deliberate 2-step confirmation dialog with a specific typed confirmation (e.g., typing the repo name to delete a GitHub repository).

### 2. Scene B — Thermostat Valve Theory (The Mistake)
- **Scenario:** A user feels freezing cold and sets the room thermostat to 30°C (86°F), assuming the heating unit will pump out hotter air faster.
- **Why it's a Mistake:** Most HVAC heaters operate as binary systems: they are either 100% on or 100% off until the target temperature is reached. Setting it to 30°C does not accelerate heating; it simply wastes energy and overheats later. The user executed their intended action flawlessly, but their **mental model was false**.
- **Design Remedy:**
  - Provide a clear **[[Conceptual Model, System Image and Real usage|System Image]]**. Show an interface with an estimated time to reach temperature, explicitly indicating: *"Heater running at full capacity: ETA 15 mins"*.

---

## Why it matters for software engineers
Engineers frequently log user errors in telemetry and dismiss them as "user error".
- When telemetry shows high **Slips**, you have a UI layout problem: hitboxes are too small, buttons are too close, or default keybindings clash.
- When telemetry shows high **Mistakes**, you have a communication/information problem: your documentation, labels, or system model are confusing the user.

---

## Related concepts
- [[seven-stages-of-action]]
- [[three-levels-of-processing]]
- [[gulf-of-execution]]
- [[gulf-of-evaluation]]
- [[Conceptual Model, System Image and Real usage]]
