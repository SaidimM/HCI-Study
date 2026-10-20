---
type: concept
first_seen: week-02
source: "Jakob Nielsen (1994), 'Severity Ratings for Usability Problems'"
tags: [concept, week/02, nielsen, severity-rating, heuristic-evaluation, prioritization]
---

<p style="font-size: 0.8em; text-transform: uppercase; letter-spacing: 2px; opacity: 0.6; margin-bottom: 2px;">
HCI CORE CONCEPT · WEEK 02
</p>

# Severity Rating (0–4 Scale)

*Not all usability bugs are created equal; severity ratings triage heuristic violations by Frequency, Impact, and Persistence so engineering teams fix what actually matters first.*

> [!abstract] At a glance
> **What:** Jakob Nielsen's 0-to-4 numerical scale for prioritizing usability problems discovered during a [[nielsen-heuristics|Heuristic Evaluation]].
> **Why:** Engineering time is finite; a severity score separates subjective cosmetic nitpicks (`0`–`1`) from workflow-blocking bugs (`3`) and data-destroying catastrophes (`4`).
> **See it:** Scoring a forced auto-scroll viewport hijack as **Severity 3 (Major)** because it happens every time (*high frequency/persistence*) and disrupts reading (*high UX impact*), though it does not destroy user data (which would be a **4**).

> *"Severity ratings can be used to allocate the most resources to fix the most serious problems and can also provide a rough estimate of the need for additional usability efforts."* — Jakob Nielsen (1994)

---

## 1. Definition (my own words, ≤ 3 sentences)
A **Severity Rating** is a 0-to-4 prioritization score assigned to each usability violation found during a heuristic evaluation to guide engineering triage. Rather than guessing a number on gut feeling, an evaluator computes severity as the combined product of three orthogonal dimensions: **Frequency** (how often it occurs), **Impact** (how badly it hurts the user or data), and **Persistence** (whether users can learn to bypass it or get trapped every time).

---

## 2. Core Architecture: The Three Severity Multipliers

```text
                  ┌───────────────────────────────────┐
                  │     USABILITY PROBLEM DETECTED    │
                  └─────────────────┬─────────────────┘
                                    │
          ┌─────────────────────────┼─────────────────────────┐
          ▼                         ▼                         ▼
  ┌───────────────┐         ┌───────────────┐         ┌───────────────┐
  │ 1. FREQUENCY  │   ×     │   2. IMPACT   │   ×     │ 3. PERSISTENCE│
  ├───────────────┤         ├───────────────┤         ├───────────────┤
  │ Is it common  │         │ Is it easy or │         │ Is it a one-  │
  │ or rare in    │         │ hard for the  │         │ time surprise │
  │ everyday workflows?     │ user to overcome?       │ or a permanent│
  │               │         │ Does it lose  │         │ recurring trap│
  │               │         │ data?         │         │ every session?│
  └───────┬───────┘         └───────┬───────┘         └───────┬───────┘
          └─────────────────────────┼─────────────────────────┘
                                    ▼
                  ┌───────────────────────────────────┐
                  │    NIELSEN SEVERITY SCORE (0–4)   │
                  └───────────────────────────────────┘
```

---

## 3. Nielsen's 0–4 Severity Scale

```text
┌───────┬──────────────────────────┬─────────────────────────────────────┐
│ Score │ Rating Category          │ Engineering Triage Mandate          │
├───────┼──────────────────────────┼─────────────────────────────────────┤
│   0   │ Not a Usability Problem  │ Ignore. Pure personal taste/opinion.│
│   1   │ Cosmetic Problem Only    │ Fix only if spare UI polish time.   │
│   2   │ Minor Usability Problem  │ Low priority; causes brief pause.   │
│   3   │ Major Usability Problem  │ High priority! Must fix soon;       │
│       │                          │ repeatedly disrupts user workflow.  │
│   4   │ Usability Catastrophe    │ Imperative to fix BEFORE release!   │
│       │                          │ Blocks core task or destroys data.  │
└───────┴──────────────────────────┴─────────────────────────────────────┘
```

---

## 4. Applied Triage: Distinguishing Severity 3 vs. Severity 4

A critical skill in HCI evaluation is justifying *why* a bug is a **3 (Major)** rather than a **2 (Minor)** or a **4 (Catastrophe)**. Consider our diagnosis of the **Windows Horizontal List Auto-Scroll Hijack** ([[2026-10-16]]):

```text
┌────────────────────────────────────────────────────────────────────────┐
│       CASE STUDY: HORIZONTAL AUTO-SCROLL HIJACK → SEVERITY 3           │
├──────────────────────┬─────────────────────────────────────────────────┤
│ Violation Summary    │ Background index advances and forces viewport   │
│                      │ back to the active item while the user is       │
│                      │ scrolled backward reading an older item.        │
├──────────────────────┼─────────────────────────────────────────────────┤
│ 1. Frequency         │ HIGH — Happens every time a user inspects an    │
│                      │ earlier item during live background indexing.   │
├──────────────────────┼─────────────────────────────────────────────────┤
│ 2. Persistence       │ HIGH — Even when the user expects it, they      │
│                      │ cannot prevent the timer from yanking their     │
│                      │ scroll position away every few seconds.         │
├──────────────────────┼─────────────────────────────────────────────────┤
│ 3. Impact            │ MODERATE-HIGH — Severely degrades reading UX    │
│                      │ and breaks working memory, BUT does not corrupt │
│                      │ or delete underlying data.                      │
├──────────────────────┼─────────────────────────────────────────────────┤
│ Final Verdict        │ SEVERITY 3 (Major Usability Problem)            │
│                      │ Must be fixed soon (via Sticky Scroll-Lock),    │
│                      │ reserving Severity 4 for unrecoverable crashes  │
│                      │ or silent data loss.                            │
└──────────────────────┴─────────────────────────────────────────────────┘
```

---

## 5. Why it matters for software engineers
When product teams run a bug bash or usability audit without a structured severity rubric, the backlog gets flooded with noisy cosmetic complaints (misaligned icons, button color opinions) that drown out severe interaction flaws. Requiring every usability ticket to justify **Frequency × Impact × Persistence** aligns designers and backend engineers on objective engineering priority.

---

## Related concepts
- [[nielsen-heuristics]]
- [[constraints]]
- [[slips-vs-mistakes]]
- [[gulf-of-execution]]
- [[gulf-of-evaluation]]

---

## Sources
[^1]: Nielsen, J. (1994). *Usability Engineering*. Morgan Kaufmann. Chapter 5: *Heuristic Evaluation (Severity Ratings)*.
