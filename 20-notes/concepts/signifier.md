---
type: concept
first_seen: week-01
source: "Norman, The Design of Everyday Things (Ch. 1 & 2)"
tags: [concept, week/01, norman, signifier, presentation]
---

# Signifier

> *"Affordances define what actions are possible. Signifiers specify where the action should take place."* — Don Norman

![[signifier-dimensions.svg]]

---

## 1. Definition (my own words, ≤ 3 sentences)
A signifier is any perceivable signal, mark, or physical trace that communicates the presence of an [[affordance]] or the state of a system to an agent. While an affordance determines what actions are physically possible, a signifier specifies **what** action can be taken, **where** that action should take place, **how** it should be performed, and **what state** the system is currently in. Signifiers can be deliberately designed or naturally emergent from use.

---

## 2. Core Architecture: How Signifiers Bridge the Action Gap

```
┌──────────────────────────────────────────────────────────────┐
│                    THE HUMAN - MACHINE GAP                   │
└──────────────────────────────┬───────────────────────────────┘
                               │
                               ▼
                   ┌───────────────────────┐
                   │   PHYSICAL OBJECT     │
                   │   (Actual Affordance) │
                   └───────────┬───────────┘
                               │
          Is the affordance directly perceivable by human senses?
                         /           \
                   [ YES ]           [ NO ]
                      │                 │
                      │        ┌────────┴────────┐
                      │        │ SIGNIFIER REQ'D │
                      │        │ (Signal / Mark) │
                      │        └────────┬────────┘
                      │                 │
                      ▼                 ▼
         ┌─────────────────────────────────────────┐
         │       PERCEIVED ACTIONABLE WORLD        │
         │       (User Mental Model Formed)        │
         └────────────────────┬────────────────────┘
                              │
          ┌───────────────────┴───────────────────┐
          ▼                                       ▼
  [ Gulf of Execution ]                   [ Gulf of Evaluation ]
  • "Where do I push/tap?"                • "Did my press register?"
  • "Which direction to pull?"            • "What state is it in now?"
```

---

## 3. The Four Questions Answered by a Signifier

```
┌────────────────────────────────────────────────────────────────────────┐
│                       THE 4 SIGNIFIER DIMENSIONS                       │
├──────────────────┬──────────────────┬──────────────────┬───────────────┤
│     1. WHAT      │    2. WHERE      │     3. HOW       │   4. STATE    │
│  (Action Type)   │ (Spatial Target) │ (Motor Gesture)  │(System Health)│
├──────────────────┼──────────────────┼──────────────────┼───────────────┤
│  [ Trash Pedal ] │ [ Toilet Button] │ [  BottomSheet ] │ [ App Badge ] │
│     ┌──────┐     │     ┌──────┐     │     ┌──────┐     │    ┌──────┐   │
│     │ STEP │     │     │ PUSH │     │     │ DRAG │     │    │  (3) │   │
│     └──────┘     │     └──────┘     │     └──▲───┘     │    └──────┘   │
│        ▼         │        ▼         │        │         │        ▼      │
│ "Lid will open"  │ "Flush volume"   │ "Slide upward"   │ "3 new alerts"│
└──────────────────┴──────────────────┴──────────────────┴───────────────┘
```

<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(210px, 1fr)); gap: 14px; margin: 16px 0;">

<div style="border: 1px solid #3b82f6; border-radius: 8px; padding: 14px; background: rgba(59,130,246,0.05);">
  <h4 style="margin: 0 0 8px 0; color: #60a5fa;">01 · WHAT is possible?</h4>
  <p><strong>Trash Can Foot Pedal:</strong> The ribbed lever at floor level signifies that foot depression triggers lid opening, preserving sanitary hands.</p>
</div>

<div style="border: 1px solid #10b981; border-radius: 8px; padding: 14px; background: rgba(16,185,129,0.05);">
  <h4 style="margin: 0 0 8px 0; color: #34d399;">02 · WHERE to act?</h4>
  <p><strong>Toilet Dual-Flush Button:</strong> Recessed chrome crescents demarcate the exact physical touch target and mechanical water volume choice.</p>
</div>

<div style="border: 1px solid #f59e0b; border-radius: 8px; padding: 14px; background: rgba(245,158,11,0.05);">
  <h4 style="margin: 0 0 8px 0; color: #fbbf24;">03 · HOW to do it?</h4>
  <p><strong>BottomSheet Grabber:</strong> A horizontal oval pill signals vertical axis dragging, reinforced by introductory animated slide peek (Feedforward).</p>
</div>

<div style="border: 1px solid #ef4444; border-radius: 8px; padding: 14px; background: rgba(239,68,68,0.05);">
  <h4 style="margin: 0 0 8px 0; color: #f87171;">04 · System STATE?</h4>
  <p><strong>Badges & Kettle LEDs:</strong> Red counter pills or green glowing rings communicate the invisible background status of the system.</p>
</div>

</div>

---

## 4. Deliberate vs. Accidental Signifiers

Signifiers do not only originate on a designer's canvas. They are split into two fundamental classes:

```
                  ┌───────────────────────────────┐
                  │       SIGNIFIER ORIGIN        │
                  └───────────────┬───────────────┘
                                  │
                 ┌────────────────┴────────────────┐
                 ▼                                 ▼
      [ DELIBERATE (Designed) ]         [ ACCIDENTAL (Physical Traces) ]
      • Painted road lines              • Desire paths across grass
      • Labeled CTA buttons             • Smudges on frequently pushed glass
      • Touchscreen grabber bars        • Worn wood on tavern door latch
      • Haptic buzz patterns            • Steam rising from kettle spout
```

* **Deliberate:** Intentionally engineered by creators to communicate affordances.
* **Accidental / Incidental:** Natural physical traces left by previous users or the environment. Shrewd designers observe accidental signifiers (e.g. desire paths) to discover genuine user intentions before laying paved paths.

---

## 5. Strong vs. Weak Signifiers (Norman's Rule)

> *"A door that needs a sign that says 'PUSH' or 'PULL' is a confession of design failure."* — Don Norman

```
┌─────────────────────────────────┬─────────────────────────────────┐
│        STRONG SIGNIFIERS        │         WEAK SIGNIFIERS         │
│     (Visceral & Behavioral)     │          (Reflective)           │
├─────────────────────────────────┼─────────────────────────────────┤
│ • Flat brass push plate         │ • Printed sticker: "PUSH"       │
│ • Contoured ergonomic grip      │ • Manual: "Turn left 90°"       │
│ • Physical slot sized to coin   │ • Warning text / tooltip banner │
│                                 │                                 │
│ Operates via geometry & muscle  │ Requires conscious reading;     │
│ memory; zero reading needed.    │ fails when rushed or dark.      │
└─────────────────────────────────┴─────────────────────────────────┘
```

---

## 6. The Screen Reality: Why Norman Apologized

In the 1988 edition of *The Design of Everyday Things*, Norman used "affordance" loosely, leading software engineers to declare: *"I designed an affordance for this button."*

In the 2013 revised edition, Norman explicitly corrected this:
- On a glass touch display, the **physical affordances are fixed**—the glass affords tapping, sliding, and pinching anywhere across its surface.
- A button drawn on a screen **has no physical affordance**; it is entirely a **signifier** signaling an underlying virtual capability.
- **The Flat Design Trap:** When designers stripped away drop shadows, borders, and bevels (e.g., early iOS 7), they removed critical signifiers, drastically widening the [[gulf-of-execution]] because users could no longer distinguish interactive elements from static labels.

---

## 7. Why it matters for software engineers
Engineers frequently build powerful APIs and UI controls without intuitive signifiers, expecting users to "just know" or read documentation. If users struggle to locate where to click, guess whether an item is draggable, or miss destructive actions, the fault lies in missing or deceptive signifiers. Clear signifiers make virtual affordances discoverable.

---

## Related concepts
- [[affordance]]
- [[gulf-of-execution]]
- [[gulf-of-evaluation]]
- [[feedback]]
- [[seven-stages-of-action]]
