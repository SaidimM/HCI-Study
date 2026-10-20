---
homework: 02
graded_on: 2026-10-20
self_score: 15/15
ta_score: 
grade: A
---

# HW02 — Grade & Self-Evaluation

> Reference submission: [[20-notes/homework/hw02-heuristic-evaluation/submission|HW02 Submission]]  
> Reference rubric: [[week-02]]  
> Prototype codebase: [github.com/SaidimM/BusAssistant](https://github.com/SaidimM/BusAssistant) (`/home/ubuntu/projects/BusAssistant`)

## Rubric Breakdown

| Criterion | Max | Self | TA | Evidence / Rationale |
|---|---|---|---|---|
| **≥ 8 genuine violations (not personal taste)** | 4 | 4 | | Documented 8 concrete, systemic usability violations in Amap across two realistic commuter/driver tasks (splash-screen gyro hijack, 10s cold-start freeze, 6-tap habitual commute amnesia, commercial cab default bias, single-line transit silos, fintech data-ink bloat, passive visual polling, and cloud telemetry lock-in). |
| **Each mapped to the correct heuristic with evidence** | 3 | 3 | | Every violation is explicitly mapped to Nielsen's 10 Heuristics (`H1`, `H2`, `H3`, `H5`, `H6`, `H7`, `H8`) and grounded in cognitive/motor mechanisms (working memory limits, 1.0s latency law, Fitts's Law, Tufte Data-Ink ratio). |
| **Severity ratings justified (frequency × impact × persistence)** | 3 | 3 | | Each 0–4 score is broken down across all three multipliers (`Frequency × Impact × Persistence`), clearly distinguishing why the driving splash-ad hijack is a **Severity 4 Catastrophe** (physical safety hazard) while the 6-tap commute tax and single-line silos are **Severity 3 Major** problems. |
| **Redesigns concrete and feasible** | 3 | 3 | | Backed by our working Jetpack Compose + Room SQLite prototype (**[BusAssistant](https://github.com/SaidimM/BusAssistant)**), featuring a 0-tap context prediction engine, side-by-side interchangeable Route Corridor cards, `<500ms` 1D progress canvas, and 100% on-device privacy. |
| **Mental-model reflection shows insight** | 2 | 2 | | Analyzed the structural clash between the user's Mental Model (*Calm Spatial Instrument* requiring `<1s` glanceability in traffic) and Amap's business-driven System Image (*Attention-Extracting Super-App*). |

**Total:** 15 / 15 (Grade: **A**)

---

## Weakest Criterion → What to Improve Next Week
- In **Week 3 (Fitts's Law Experiment)** and **Week 4 (Needfinding Interviews)**, we can empirically measure the exact time-on-task difference (in milliseconds and error rate) between Amap's 7-step flow and *BusAssistant*'s 0-tap dashboard across real participants.

## TA Feedback
*(Pending review)*
