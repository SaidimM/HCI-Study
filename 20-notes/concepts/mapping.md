---
type: concept
first_seen: week-02
source: "Norman, The Design of Everyday Things (Ch. 1 & Ch. 4)"
tags: [concept, week/02, norman, mapping, spatial-correspondence]
---

<p style="font-size: 0.8em; text-transform: uppercase; letter-spacing: 2px; opacity: 0.6; margin-bottom: 2px;">
HCI CORE CONCEPT · WEEK 02
</p>

# Mapping (Natural Mapping)

*Like a Java `Map<Control, WorldEffect>`, good mapping aligns the spatial layout and movement of controls directly with the things they control in the real world.*

> [!abstract] At a glance
> **What:** The technical relationship between the layout/movement of **controls** (`Key`) and their **effects in the world** (`Value`).
> **Why:** Natural mapping eliminates mental translation, allowing users to operate multi-control systems immediately without reading labels.
> **See it:** The 2×2 matrix of power window switches on a car driver's armrest matching the exact 2×2 layout of the car's four windows.

> *"Natural mapping, by which I mean taking advantage of spatial analogies, leads to immediate understanding."* — Don Norman

---

## 1. Definition (my own words, ≤ 3 sentences)
Borrowed from mathematics and programming (like a `Key → Value` hash map), **Mapping** in HCI describes how a designed control (`Key`) corresponds to the target object and state change in the physical or digital world (`Value`). **Natural Mapping** uses physical, spatial, and kinematic analogies so that the arrangement and direction of controls directly mirror the real-world target. When mapping is natural, users instantly know which control operates which device and which direction to move it without conscious mental effort or text labels.

---

## 2. Core Architecture: Norman's Three Tiers of Spatial Mapping

```text
┌────────────────────────────────────────────────────────────────────────┐
│                 NORMAN'S HIERARCHY OF NATURAL MAPPING                  │
├──────────────────┬─────────────────────────────────────────────────────┤
│ TIER 1: BEST     │ Controls are mounted DIRECTLY ON the target object. │
│ (Direct Contact) │ • Ex: Touching/dragging an object on an iPad screen;│
│                  │   pushing directly on the edge of a swinging door.  │
├──────────────────┼─────────────────────────────────────────────────────┤
│ TIER 2: SECOND   │ Controls sit immediately adjacent and mimic the     │
│ (Iconic Proxy)   │ exact geometry of the target.                       │
│                  │ • Ex: Car seat adjustment switches shaped like a    │
│                  │   miniature seat on the door panel.                 │
├──────────────────┼─────────────────────────────────────────────────────┤
│ TIER 3: THIRD    │ Controls are arranged in the exact same 2D/3D       │
│ (Spatial Grid)   │ spatial layout as the distant targets.              │
│                  │ • Ex: Driver's 2×2 window switch cluster matching   │
│                  │   Front-Left, Front-Right, Rear-Left, Rear-Right.   │
└──────────────────┴─────────────────────────────────────────────────────┘
```

---

## 3. Classic Contrast: The Stove Burner & Switch Problem

Why do people constantly flip the wrong wall switch in conference rooms or turn on the wrong burner on a kitchen stove? Because engineers arrange controls in a **1D linear row** to control targets arranged in a **2D spatial plane**:

```text
┌───────────────────────────────────┬───────────────────────────────────┐
│   ARBITRARY MAPPING (1D → 2D)     │     NATURAL MAPPING (2D → 2D)     │
│   (Requires Labels & Memory)      │     (Zero Labels Needed)          │
├───────────────────────────────────┼───────────────────────────────────┤
│   Targets in World (2D Grid):     │   Targets in World (2D Grid):     │
│     [ Rear-L ]     [ Rear-R ]     │     [ Rear-L ]     [ Rear-R ]     │
│     [ Front-L]     [ Front-R]     │     [ Front-L]     [ Front-R]     │
│                                   │                                   │
│   Controls on Panel (1D Row):     │   Controls on Panel (2D Cluster): │
│     ( O )  ( O )  ( O )  ( O )    │       ( O )          ( O )        │
│      FL     RL     RR     FR      │       ( O )          ( O )        │
│                                   │                                   │
│ • High Gulf of Execution          │ • Instant behavioral fluency      │
│ • Frequent slips (wrong burner)   │ • Matches driver's window cluster │
└───────────────────────────────────┴───────────────────────────────────┘
```

### Real-World Exemplar: The Driver's Four-Window Switch Cluster
On the left armrest of a car door, the driver controls four windows across the cabin:
1. **Spatial Mapping (Which window?):** The switches are arranged in a **2×2 grid** (`Front-Left`, `Front-Right`, `Rear-Left`, `Rear-Right`) that mirrors the exact floorplan of the car seats. The driver never needs to look down at the armrest—proprioception and spatial mapping identify the correct switch blind.
2. **Kinematic Mapping (Which direction?):** Pulling the rocker switch **upward** raises the window glass **upward**; pressing the switch **downward** pushes the window glass **downward**.

---

## 4. Cultural & Biological Nuances in Mapping

Not all mappings are purely geometric; some rely on **frames of reference** (Ego-Moving vs. World-Moving):

```text
┌────────────────────────────────────────────────────────────────────────┐
│               SCROLLING: THE FRAME-OF-REFERENCE CLASH                  │
├──────────────────────┬─────────────────────────────────────────────────┤
│ Traditional Desktop  │ "Moving the Scrollbar / Viewport"               │
│ (Windows Mouse Wheel)│ • Pull wheel DOWN ──► Viewport moves DOWN the   │
│                      │   document (text pixels move UP).               │
├──────────────────────┼─────────────────────────────────────────────────┤
│ Touchscreen / macOS  │ "Moving the Content Sheet (Natural Scrolling)"  │
│ ("Natural" Gesture)  │ • Drag fingers UP ──► Pushes the physical paper │
│                      │   sheet UP (revealing lower content).           │
└──────────────────────┴─────────────────────────────────────────────────┘
```

> [!note] Sidebar · Mapping vs. Signifiers
> A common trap is confusing **Mapping** with **[[signifier|Signifiers]]**. A male/female pictogram on a restroom door is a *cultural signifier* (it labels a passive room, not an interactive control-to-effect relationship). **Mapping** specifically governs how an *input control action* (`Key`) maps to a *target system output* (`Value`).

---

## 5. Why it matters for software engineers
In software UI and 3D tools (like our [[bimanual-interaction|Desk-Anchored 6-DOF Trackpad]] analysis), poor mapping forces users to memorize arbitrary keyboard shortcuts (`Alt+Shift+R`) or hunt through nested dropdown menus to manipulate on-screen objects. Whenever possible:
1. **Prefer Direct Manipulation (Tier 1 Mapping):** Let users drag table columns, resize panels, or scrub timeline playheads directly on the visual element.
2. **Match Control Geometry to Viewport Geometry:** If a split-screen editor has Left and Right panes, place the pane-control toggles on the Left and Right respectively—never stacked vertically in a top-right menu.

---

## Related concepts
- [[constraints]]
- [[signifier]]
- [[affordance]]
- [[bimanual-interaction]]
- [[gulf-of-execution]]
- [[seven-stages-of-action]]

---

## Sources
[^1]: Norman, D. A. (2013). *The Design of Everyday Things: Revised and Expanded Edition*. Basic Books. Chapter 1 (*Natural Mapping*) & Chapter 4 (*Constraints That Force the Desired Interpretation*).
