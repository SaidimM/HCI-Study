---
type: concept
first_seen: week-02
source: "Norman, The Design of Everyday Things (Ch. 4: Knowing What to Do)"
tags: [concept, week/02, norman, constraints, forcing-functions, error-prevention]
---

<p style="font-size: 0.8em; text-transform: uppercase; letter-spacing: 2px; opacity: 0.6; margin-bottom: 2px;">
HCI CORE CONCEPT · WEEK 02
</p>

# Constraints & Forcing Functions

*Instead of writing warning labels telling users what not to do, restrict the set of possible actions so errors become impossible.*

> [!abstract] At a glance
> **What:** Physical, cultural, semantic, and logical cues that limit the range of possible actions on an artifact.
> **Why:** Humans encounter thousands of unfamiliar objects; constraints put knowledge into the world so users can operate devices without manuals or mistakes.
> **See it:** A captive-key lock that physically traps your key until you lock the door, or a 3-prong electrical plug that only fits one way.

> *"The surest way to make a device easy to use is to make it impossible to use wrongly—by constraining the actions."* — Don Norman

---

## 1. Definition (my own words, ≤ 3 sentences)
Constraints are deliberate design limitations built into an interface or object to prevent users from making errors before they even happen. Rather than blaming users when things go wrong, designers narrow the set of permissible actions using **Physical**, **Cultural**, **Semantic**, and **Logical** rules. When safety or data integrity is critical, designers escalate constraints into **Forcing Functions** (*Interlocks*, *Lock-ins*, and *Lockouts*) that mechanically or programmatically enforce safe execution sequences.

---

## 2. Core Architecture: Norman's Four Classes of Constraints

```text
┌────────────────────────────────────────────────────────────────────────┐
│                    NORMAN'S 4 CLASSES OF CONSTRAINTS                   │
├──────────────────┬─────────────────────────────────────────────────────┤
│ 1. PHYSICAL      │ Geometry, mechanics, or disabled states physically  │
│    (Hard Bounds) │ block invalid movements.                            │
│                  │ • Ex: 3-prong socket, flat push plate, SIM notch.   │
├──────────────────┼─────────────────────────────────────────────────────┤
│ 2. CULTURAL      │ Shared societal conventions and learned symbols.    │
│    (Social Norms)│ • Ex: Driving on the right side of the road; red    │
│                  │   for danger/stop; universal power icon (⏻).        │
├──────────────────┼─────────────────────────────────────────────────────┤
│ 3. SEMANTIC      │ Common-sense knowledge of how the real world works. │
│    (Meaning)     │ • Ex: Waterproof rain shoe covers must have rubber  │
│                  │   treads on the bottom (ground) and opening on top. │
├──────────────────┼─────────────────────────────────────────────────────┤
│ 4. LOGICAL       │ Pure spatial deduction, proportion, or elimination. │
│    (Deduction)   │ • Ex: Dual-flush toilet (big button = more water,   │
│                  │   small button = less water); last remaining port.  │
└──────────────────┴─────────────────────────────────────────────────────┘
```

---

## 3. Real-World Physical & Digital Artifacts

<div style="display: flex; gap: 24px; align-items: flex-start; margin: 20px 0;">
  <!-- Left Column: The Narrative Argument (~60%) -->
  <div style="flex: 1.2;">
    <p style="font-size: 0.75em; text-transform: uppercase; letter-spacing: 1.5px; opacity: 0.6; margin-bottom: 4px;">
      ARTIFACT 01 · PHYSICAL CONSTRAINT
    </p>
    <h4 style="margin-top: 0;">The Flat Door Push Plate vs. The Protruding Knob</h4>
    <p>A protruding door knob or bar handle affords both pulling and pushing—causing users to frequently pull a push-only door. A <strong>flat brass push plate</strong> introduces a strict <strong>physical constraint</strong>: human fingers cannot grasp a flush surface, making pulling physically impossible and narrowing the [[gulf-of-execution]] to a single valid action.</p>
  </div>

  <!-- Right Column: Visual Evidence & Argumentative Caption (~40%) -->
  <div style="flex: 0.8; max-width: 260px; flex-shrink: 0;">
    <img src="assets/door-push-plate.jpg" alt="Door Push Plate" style="border-radius: 6px; width: 100%; box-shadow: 0 4px 12px rgba(0,0,0,0.15);">
    <p style="font-size: 0.82em; line-height: 1.4; opacity: 0.75; margin-top: 6px; border-left: 2px solid currentColor; padding-left: 8px;">
      <strong>Physical Constraint in Action:</strong> By eliminating any graspable protrusion, the flat plate physically eliminates the possibility of a "pull" slip without needing a single word of instruction.
    </p>
  </div>
</div>

<div style="display: flex; gap: 24px; align-items: flex-start; margin: 20px 0;">
  <!-- Left Column: The Narrative Argument (~60%) -->
  <div style="flex: 1.2;">
    <p style="font-size: 0.75em; text-transform: uppercase; letter-spacing: 1.5px; opacity: 0.6; margin-bottom: 4px;">
      ARTIFACT 02 · LOGICAL & PROPORTIONAL CONSTRAINT
    </p>
    <h4 style="margin-top: 0;">The Dual-Flush Toilet Crescent</h4>
    <p>How does a user deduce which button triggers a full flush versus a half flush without text labels? Through a <strong>logical proportional constraint</strong>: the larger surface area maps logically to a larger water volume, while the smaller crescent maps to a smaller flush volume.</p>
  </div>

  <!-- Right Column: Visual Evidence & Argumentative Caption (~40%) -->
  <div style="flex: 0.8; max-width: 260px; flex-shrink: 0;">
    <img src="assets/toilet-dual-flush-button.jpg" alt="Toilet Dual-Flush Button" style="border-radius: 6px; width: 100%; box-shadow: 0 4px 12px rgba(0,0,0,0.15);">
    <p style="font-size: 0.82em; line-height: 1.4; opacity: 0.75; margin-top: 6px; border-left: 2px solid currentColor; padding-left: 8px;">
      <strong>Proportional Logic:</strong> The asymmetric split uses geometric area as a logical constraint—though when both buttons are pressed simultaneously due to weak separation, the constraint breaks down.
    </p>
  </div>
</div>

---

## 4. Forcing Functions: Interlocks, Lock-Ins, and Lockouts

When an error carries severe physical or data-loss consequences, soft constraints are upgraded into **Forcing Functions**—situations where the actions are constrained so that failure at one stage prevents the next step from happening:

```text
┌────────────────────────────────────────────────────────────────────────┐
│                    THE 3 TYPES OF FORCING FUNCTIONS                    │
├──────────────────┬─────────────────────────────────────────────────────┤
│ 1. INTERLOCK     │ Forces operations to take place in strict sequence. │
│ (Sequence Rule)  │ • Physical: "Captive-Key" locks where you CANNOT    │
│                  │   pull your key out until you lock the deadbolt.    │
│                  │ • Software: GitHub disabling the "Delete Repo"      │
│                  │   button until you type the exact repo name first.  │
├──────────────────┼─────────────────────────────────────────────────────┤
│ 2. LOCK-IN       │ Keeps an operation active to prevent premature exit.│
│ (State Preserver)│ • Physical: Washing machine locking the door while  │
│                  │   the drum is full of water mid-cycle.              │
│                  │ • Software: Unsaved changes dialog intercepting     │
│                  │   Cmd+Q so you don't accidentally lose hours of work│
├──────────────────┼─────────────────────────────────────────────────────┤
│ 3. LOCKOUT       │ Prevents entry into a dangerous space or state.     │
│ (Hazard Barrier) │ • Physical: Guardrails along a river bank; child-   │
│                  │   proof medicine bottle caps.                       │
│                  │ • Software: Disabling destructive admin toggles for │
│                  │   read-only users in a production dashboard.        │
└──────────────────┴─────────────────────────────────────────────────────┘
```

> [!note] Sidebar · The Captive-Key Interlock
> In many European apartment doors, shared bikes, and industrial cabinets, the key cannot be removed while the lock is open. Because the user *wants their keys back* before walking away, this **Interlock** harnesses the user's goal to guarantee they never forget to lock the door—eliminating **memory-lapse slips** ([[slips-vs-mistakes]]).

---

## 5. Why it matters for software engineers
Engineers often allow users to fill out an entire form with invalid states (e.g., typing letters into a phone number field, selecting an end-date earlier than a start-date, or clicking "Submit" while required fields are empty) and then punish them with a wall of red `400 Bad Request` error banners. **Good software engineering applies constraints proactively** (Nielsen's Heuristic #5: *Error Prevention*): grey out past dates in the calendar picker, mask numeric inputs, and use **Interlocks** (like GitHub's repo-name confirmation) to protect against catastrophic data loss.

---

## Related concepts
- [[affordance]]
- [[signifier]]
- [[mapping]]
- [[slips-vs-mistakes]]
- [[nielsen-heuristics]]
- [[gulf-of-execution]]

---

## Sources
[^1]: Norman, D. A. (2013). *The Design of Everyday Things: Revised and Expanded Edition*. Basic Books. Chapter 4: *Knowing What to Do: Constraints, Discoverability, and Feedback*.
