---
homework: 01
week: 1
title: "Everyday Gulfs Field Observation"
due: 2026-10-11
status: submitted
participants: [P1]
tags: [homework, week/01, field-observation, gulfs]
---

# HW01 — Everyday Gulfs Field Observation

> Course: Stanford CS147 / HCI Core Curriculum  
> Brief & Rubric: [[week-01]]  
> Concepts referenced: [[gulf-of-execution]], [[gulf-of-evaluation]], [[seven-stages-of-action]], [[affordance]], [[signifier]], [[feedback]]

---

## Interface 1 (Physical): Flush & Hidden Electric Vehicle Door Handles

### Context & Description
Modern electric vehicles (most notably Tesla Model 3 and Model Y) replace traditional protruding mechanical door handles with aerodynamic flush handles. To open from the outside, the user must press the wide rear portion with their thumb to pivot the skinny front portion outwards, then grasp the lever with their fingers to pull the door open. On the interior, opening the door requires pressing an unmarked electronic button on the armrest rather than pulling a mechanical latch.

### User Goal
Enter or exit the vehicle smoothly without confusion or physical hesitation.

### Walkthrough Across Norman's 7 Stages of Action

```
      [Goal: Exit / Enter Vehicle]
                 │
  ┌──────────────┴──────────────┐
  ▼                             ▼
[Gulf of Execution]           [Gulf of Evaluation]
• Plan: Release door latch    • Perceive: Window drops slightly / silent click
• Specify: Guess touch target • Interpret: Did the latch release or fail?
• Execute: Awkward 2-motion   • Compare: Door still closed → confusion & shame!
  push-and-pull grip
```

1. **Goal:** Open the car door to get in or out.
2. **Plan:** Unlatch the door mechanism.
3. **Specify:** 
   * *Exterior:* Figure out where to push or pull on a completely flat metal surface with no visual cue.
   * *Interior:* Distinguish the tiny flat electric release button from the window switches and emergency release latch.
4. **Execute:** 
   * *Exterior:* Apply asymmetrical thumb pressure to one side of the flush lever while catching the protruding lip with remaining fingers.
   * *Interior:* Press the thumb against the flat button on the door handle.
5. **Perceive:** A faint electronic micro-click occurs, and the frameless window drops 5mm.
6. **Interpret:** The user is unsure whether the door popped ajar or if they need to push the heavy frame outward with their shoulder.
7. **Compare:** If the passenger pulls too quickly before pushing, the door remains locked. The user feels awkward, confused, or embarrassed.

### Gulf Analysis
* **Gulf of Execution (Severe):** The physical [[affordance]] to pull a door handle is contradicted by the lack of [[signifier]]. Flat sheet metal does not signify "push thumb here to pivot opposite side out." The user’s preexisting [[conceptual-model]] of a car door (grab and pull) fails completely.
* **Gulf of Evaluation (Moderate to High):** The tactile feedback of the electronic actuator is subtle. Unlike a mechanical latch that gives immediate progressive resistance, the electronic button provides almost no haptic stroke, leaving the user guessing whether the action succeeded.

### Concrete Redesign Idea
1. **Contoured Tactile Signifier:** Add an ergonomic thumb indent with an illuminated icon/glyph indicating the pivot action.
2. **Predictive Pop-Out (Presence Detection):** When the key fob or phone approaches, motorized handles should automatically extend outward, restoring the classic "grab-and-pull" affordance.
3. **Interior Mechanical Indicator:** Pair the electronic push-button with a distinct tactile texture and illuminated rim, plus clear separation from the manual emergency release.

---

## Interface 2 (Software): Super-App Feature Bloat (NetEase Cloud Music vs. Apple Music)

### Context & Description
NetEase Cloud Music is a major music streaming platform with a vast catalog and vibrant social comments. Over years of commercial expansion, however, the app has accumulated massive feature bloat: splash screen advertisements, floating microloan ("financial credit") promotions, live-streaming feeds, and TikTok-style vertical video carousels directly on the primary music navigation interface.

### User Goal
Open the app, find an artist or playlist, and begin listening to music without distraction.

### Walkthrough Across Norman's 7 Stages of Action
1. **Goal:** Listen to a favorite playlist.
2. **Plan:** Launch music app and hit play.
3. **Specify:** Locate the playback controls or library tab amid modal pop-ups and full-screen loan promotions.
4. **Execute:** Tap tiny 'X' dismiss buttons on 1–2 sequential ad overlays, avoid accidental clicks on financial banners, then navigate to "My Music".
5. **Perceive:** A barrage of competing visual noise (animations, promotional red badges, autoplaying live-stream previews).
6. **Interpret:** High cognitive load; the user must actively filter commercial noise to verify they are in their personal library.
7. **Compare:** The user finally hears music, but after substantial cognitive friction and visual irritation.

### Gulf Analysis
* **Gulf of Execution (High):** The intended action path (Goal $\rightarrow$ Play) is intercepted by extraneous commercial tasks (close ad, dismiss loan offer, ignore video feeds). The UI elements for core music tasks are dwarfed by monetization banners.
* **Gulf of Evaluation (Low to Moderate):** Once playback starts, auditory feedback is immediate. However, while navigating the interface, evaluating where you are within the app is confusing due to shifting dynamic promotional tabs.

### Contrast with Calm Design (Apple Music)
In contrast, Apple Music adheres to Mark Weiser’s [[ubiquitous-computing|Calm Technology]] principle:
* The interface features minimal top-level tabs (Listen Now, Browse, Library, Search).
* The now-playing screen uses a gorgeous "fluid animated background" that reflects the album art colors without clutter. The software gets out of the way, focusing entirely on the listening experience.

### Concrete Redesign Idea
* **"Pure Audio / Minimal Mode":** Introduce a togglable distraction-free mode that completely strips out financial offers, livestreams, and short-video tabs, presenting only the Library, Search, and Player with clean typography and album artwork.

---

## Interface 3 (Physical): Apartment Door Lockouts & Forcing Functions

### Context & Description
Leaving an apartment for work and accidentally locking keys inside. Attempting to place keys on a hook near the door serves as an informal visual signifier, but users still experience action slips when rushing or distracted.

### User Goal
Leave the apartment and lock the door securely while ensuring the physical key is in hand.

### Walkthrough Across Norman's 7 Stages of Action
1. **Goal:** Head out to work with keys safely in hand.
2. **Plan:** Grab belongings, step into the hallway, shut the door.
3. **Specify:** Trigger the routine automatic motor program for leaving home.
4. **Execute:** Pull the door shut firmly until the spring latch engages.
5. **Perceive:** Hear the loud mechanical "thud/click" of the spring latch catching.
6. **Interpret:** The door is securely locked.
7. **Compare:** Immediate realization moments later: *the keys are still on the table inside!*

### Gulf & Error Analysis
* **Error Classification:** An **Action Slip** (specifically a *Lapse* of memory or *Capture Slip* where a familiar automated routine bypasses conscious verification).
* **Gulf of Evaluation:** Feedback arrives too late. The tactile and acoustic feedback (the door latching) informs the user of success, but provides zero feedback regarding the presence of the key until the system is already irrevocably locked.

### Concrete Redesign Idea: Norman's Forcing Function
Apply Don Norman's concept of an **Interlock Forcing Function**:
* **Physical Deadbolt Requirement:** The door lock is engineered such that it **cannot be locked from the outside without physically inserting and rotating the key in the cylinder**. 
* Because closing the door does not automatically lock it, the user is physically forced to hold the key in their fingers to secure the apartment, making lockout virtually impossible.
* Alternatively: Smart biometric/keypad electronic locks remove physical keys entirely, resolving the cognitive failure mode.

---

## Observation Log — P1 (Participant Field Test)

* **Context:** Observing participant (P1, 24yo graduate student) attempting to enter a parked Tesla Model 3 for the first time.
* **Consent:** Verbal consent obtained.

| Time | User Action | Observed Hesitation, Error, or Quote | Stage / Gulf Implicated |
|---|---|---|---|
| `00:00` | Approaches front passenger door with backpack. | Walks up to the door and stops 0.5m away. Looks at the door panel for 3 seconds. | Goal $\rightarrow$ Plan |
| `00:04` | Extends right hand toward flush handle. | Pushes flat palm against the center of the flush handle expecting a push-button mechanism. Nothing moves. | Gulf of Execution (missing signifier) |
| `00:07` | Withdraws hand, looks at driver. | User chuckles nervously: *"Uh, how do I open this? Do I tap something?"* | Self-blame / Social awkwardness |
| `00:12` | Tries pressing the skinny front end. | Presses index finger firmly on the left (thin) side of the handle. Handle does not pivot. | Action Error (inverted lever physics) |
| `00:16` | Driver gives verbal instruction. | Driver explains: *"Push the wide part on the right with your thumb, then grab the skinny handle."* | External instruction needed |
| `00:20` | Presses thumb on wide end. | Handle pivots outward ~30 degrees. P1 looks surprised, then uses left hand to pull the released handle while holding thumb down. | Gulf of Evaluation (awkward 2-handed recovery) |
| `00:26` | Door unlatches and swings open. | P1 breathes a sigh of relief: *"Why didn't they just leave a normal handle? That felt so unnatural."* | Evaluation / Compare |

---

## Synthesis & Reflection

### What Surprised Me
What struck me most during both my personal experience and the P1 observation was the **psychological reaction of self-blame**. When P1 could not open the door, her immediate reaction was nervous laughter and embarrassment, asking *"What am I doing wrong?"* 
This matches Don Norman's thesis in Chapter 1 of *The Design of Everyday Things*: **when an interface fails due to poor design, users instinctively blame their own competence rather than the designer's poor signifiers.**

### Concepts Applied
* [[gulf-of-execution]] — The distance between wanting to enter/exit and executing non-standard physical gestures.
* [[gulf-of-evaluation]] — The absence of immediate, unambiguous sensory feedback confirming whether an electronic latch has released.
* [[affordance]] vs. [[signifier]] — The presence of physical capability without visible indicators of operation.
* [[seven-stages-of-action]] — Tracing each failure point from goal formulation to sensory interpretation.
* **Forcing Functions** — Solving memory slips through mechanical constraints.
