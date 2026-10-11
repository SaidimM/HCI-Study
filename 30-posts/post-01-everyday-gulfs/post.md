---
title: "I Watched Someone Struggle to Open a Car Door for 30 Seconds. Here's What Don Norman Would Say."
type: homework-report
status: ready
week: 1
source_notes:
  - "[[20-notes/homework/hw01-everyday-gulfs/submission]]"
  - "[[20-notes/concepts/gulf-of-execution]]"
  - "[[20-notes/concepts/seven-stages-of-action]]"
wp_category: HCI
tags: [post, week-01, don-norman, tesla, design-thinking]
---

# I Watched Someone Struggle to Open a Car Door for 30 Seconds. Here's What Don Norman Would Say.

## Hook

A few days ago, I watched a friend walk up to a parked electric vehicle. She stopped. She looked at the door. She pushed her flat palm against the center of the flush door handle like an elevator button. Nothing happened. 

She chuckled nervously and whispered: *"Uh, how do I open this? What am I doing wrong?"*

If you have ever been in a new electric car, you have probably felt that exact same pang of embarrassment. Maybe you were on a first date, or in a rideshare, tugging at a piece of trim or hunting for an unmarked electronic button on the armrest, wondering why you suddenly forgot how to operate the oldest piece of hardware in modern history: **a door**.

Here is what Don Norman, the godfather of user-centered design, wrote in 1988:
> *"When simple things need pictures, labels, or instructions, the design has failed. And when users fail, they invariably blame themselves—even when the fault is entirely the designer's."*

---

## The Problem: The "Norman Door" Goes High-Tech

In his seminal book *The Design of Everyday Things*, Don Norman introduced the concept of the **Norman Door**: a door with a flat brass plate that looks like it should be pushed, but actually requires you to pull a concealed handle.

Over the past decade, automotive designers set out to make vehicles aerodynamic and visually sleek. In doing so, they replaced protruding mechanical door handles with flush, hidden levers. 

Aesthetically, it looks futuristic. Ergonomically, it created a massive breakdown in human-machine communication known as the **Gulf of Execution**.

---

## What I Did: A Field Walkthrough with Norman's 7 Stages of Action

As part of my weekly HCI fieldwork, I observed a first-time passenger (P1) trying to enter a Tesla Model 3 and mapped every hesitation against Norman's **Seven Stages of Action**:

1. **Goal:** Enter the vehicle.
2. **Plan:** Release the door latch.
3. **Specify Action:** Where do I push or pull? *(Total cognitive breakdown here: flat sheet metal contains no visible signifier).*
4. **Execute:** P1 tried pressing the center with a flat palm, then pressed the thin left side. Neither worked. The handle requires an inverted physical grip: you must press the wide right side with your thumb to pivot the skinny left side outward, then switch fingers to pull.
5. **Perceive:** A quiet electronic click, and the frameless window drops half an inch.
6. **Interpret:** Is the door unlocked? Do I shove the heavy frame with my elbow?
7. **Compare:** Success was finally achieved after 26 seconds—but only after external verbal instructions from the driver.

```
       [Goal: Enter Car]
               │
   ┌───────────┴───────────┐
   ▼                       ▼
[Gulf of Execution]     [Gulf of Evaluation]
• No signifier on body  • Subtle electronic micro-click
• Counter-intuitive     • Ambiguity: Is the latch free?
  thumb-pivot motion
```

---

## What I Found: Three Everyday Design Lessons

Beyond car doors, observing real-world breakdowns across physical and digital tools revealed three universal truths:

### 1. Affordance Without a Signifier is Invisible
A flush door handle technically has the physical capability (affordance) to pivot. But without a physical bevel, texture, or indicator (signifier), the affordance is invisible to the human brain. Good design never forces a user to guess physics.

### 2. Feature Bloat Destroys "Calm Technology"
I compared two music applications: **NetEase Cloud Music** and **Apple Music**. 
NetEase has an incredible catalog, but opening the app subjects users to splash ads, pop-up microloan offers, live-streaming badges, and TikTok-style video feeds. Launching a song requires fighting through monetization noise. 

In contrast, Apple Music adheres to Mark Weiser’s 1991 vision of *Calm Technology*: the app gets out of the way, displaying only clean playback with fluid animated background artwork. When tools respect human attention, the Gulf of Execution drops to near zero.

### 3. Forcing Functions Beat Human Memory
We often blame ourselves when we lock our keys inside our apartment. We tell ourselves: *"I just need to remember better."* 
Norman shows that human working memory is inherently fragile and prone to **action slips**. The solution is not willpower; it is a **Forcing Function (Interlock)**: engineering locks that cannot physically engage from the outside without the key inserted in the deadbolt cylinder. Constraints liberate humans from cognitive burden.

---

## Takeaways for Software & Hardware Builders

If you build tools for people—whether mobile apps, web dashboards, or physical hardware—remember:

1. **Never make users feel stupid:** If a user pauses, hesitates, or asks for help on a primary action, your signifiers failed.
2. **Beware of aesthetic minimalism:** Eliminating buttons and visual cues doesn't make an interface "simpler"—it just hides the manual in the user's head.
3. **Design for the recovery, not just the happy path:** When a user's gesture fails, provide immediate, visible, and unambiguous feedback explaining what state the system is in.

The next time you struggle to open an EV door, don't apologize. Blame the design.
