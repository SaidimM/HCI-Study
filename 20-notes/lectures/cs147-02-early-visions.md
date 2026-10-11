---
week: 1
date: 2026-10-11
source: "Stanford CS147: Early Visions (Prof. James Landay)"
tags: [lecture, week/01, history, spatial-computing]
---

# Lecture Notes — CS147 Lecture 2: Early Visions

> Lecture slides: [02-early-visions.pdf](https://hci.stanford.edu/courses/cs147/)  
> Key historical lineage: Vannevar Bush → J.C.R. Licklider → Ivan Sutherland → Douglas Engelbart → Alan Kay / Xerox PARC → Mark Weiser

---

## 1. Douglas Engelbart & The Invention of the Mouse

### Historical Origin & NASA Context
- In the mid-1960s at SRI (Stanford Research Institute), Douglas Engelbart and Bill English received NASA funding to test pointing devices for radar/display consoles.
- They tested light pens, joysticks, trackballs, knee-operated sliders, and a wooden box with two orthogonal metal wheels—the **mouse**.
- The mouse was empirically proven fastest and lowest in error rate (later modeled formally via [[fitts-law]]).

### From 1D to 2D: Narrows the Gulf of Execution
> *"Before the mouse, computing was 1-dimensional (command-line text and punch cards). The user had to translate a physical spatial goal into syntax. The invention of the mouse transformed interfaces into a 2D spatial plane, narrowing the [[gulf-of-execution]]."* — Personal Reflection

- **Command-line (CLI):** User must *Recall & Specify* syntax, coordinates, or line numbers. High cognitive friction.
- **Mouse + GUI (Direct Manipulation):** User sees an object on screen, moves their hand, and clicks. Hand motion maps continuously to cursor position.

---

## 2. Mark Weiser: Ubiquitous & Calm Computing

### The Disappearing Computer
- Mark Weiser (Xerox PARC, 1991): *"The most profound technologies are those that disappear. They weave themselves into the fabric of everyday life until they are indistinguishable from it."*
- **Calm Technology:** Good design does not scream for constant attention. It sits comfortably in the periphery of our consciousness and only moves to the center when needed.
- **Modern Reflection:** Seen in the clean, uncluttered ergonomics of macOS and well-designed physical devices where the tool gets out of the way of the task.

---

## 3. Cinematic UIs vs. Ergonomic Reality: *Minority Report* & "Gorilla Arm"

### The Hollywood Illusion
- In *Minority Report* (2002), Tom Cruise gestures in mid-air to scrub and manipulate floating 3D holographic archives.
- It looks visually dramatic on film, but fails as practical human-centered design.

### The Problem: Gorilla Arm Syndrome
- **Biomechanical Fatigue:** Holding human arms outstretched unsupported in the air causes acute muscle strain (deltoids, trapezius) and lactic acid buildup within 2–5 minutes.
- In HCI, this is known as **Gorilla Arm Syndrome**. Vertical touchscreens and mid-air waving fail for prolonged daily work.

### The Research Frontier: What is the "Mouse" for 3D?
- The mouse solved the transition from **1D (CLI) → 2D (Desktop GUI)**.
- For **3D Spatial Computing (VR/AR/Spatial Data)**, mid-air waving is not sustainable.
- **Modern Solutions & Future Directions:**
  - Micro-gestures resting in the lap with eye tracking (e.g., Apple Vision Pro).
  - Spatial stylus / 6-DOF pens on physical resting surfaces.
  - Multimodal combinations: gaze for intent + micro-tap for execution.

---

## 💡 Concept Connections & Terms
- [[direct-manipulation]] — Continuous representation of objects with rapid, reversible incremental actions.
- [[gulf-of-execution]] — The distance between user intent and physical input mechanisms.
- [[ubiquitous-computing]] — Calm, embedded technology.
- [[gorilla-arm-syndrome]] — Physical fatigue from prolonged mid-air gesture.

---

## ❓ Open Questions (→ [[questions]])
- *What is the ergonomic 3D equivalent of the mouse that enables precise spatial manipulation without arm fatigue?*
