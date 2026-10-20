---
type: paper
week: 2
date: 2026-10-20
title: "Heuristic Evaluation of User Interfaces"
authors: "Jakob Nielsen & Rolf Molich"
venue: "CHI '90 (Proceedings of the SIGCHI Conference on Human Factors in Computing Systems)"
year: 1990
tags: [paper, week/02, heuristic-evaluation, nielsen, discount-usability]
---

<p style="font-size: 0.8em; text-transform: uppercase; letter-spacing: 2px; opacity: 0.6; margin-bottom: 2px;">
SEMINAL HCI PAPER · CHI 1990 · WEEK 02
</p>

# Paper Note: Heuristic Evaluation of User Interfaces (1990)

> **Title**: Heuristic Evaluation of User Interfaces  
> **Authors**: Jakob Nielsen (Technical University of Denmark) & Rolf Molich (Baltica Finans A/S)  
> **Venue & Year**: *ACM CHI '90*, pp. 249–256 (Seattle, WA, April 1990)  
> **Link**: [DOI: 10.1145/97243.97281](https://doi.org/10.1145/97243.97281)  
> **Tags**: `#heuristic-evaluation`, `#discount-usability`, `#nielsen`, `#empirical-study`

---

## 1. One-Sentence TL;DR
Nielsen and Molich proved that replacing 1,000-rule usability manuals with a compact checklist of 9 heuristics works—**but only if you aggregate 3 to 5 independent evaluators** (~60–75% of bugs caught), because even the smartest single evaluator only catches **~35%** of usability problems on average.

---

## 2. Research Questions & Historical Motivation
- **The Industry Bottleneck (1990):** Existing usability standards (such as Smith & Mosier's 1986 guide with **944 separate guidelines**) were intimidating and ignored by working software engineers, while formal user-testing laboratories were perceived as too slow and costly.
- **RQ1 (Feasibility of Heuristics):** Can non-experts and regular computer scientists identify real interface problems using just 9 broad "rules of thumb" (heuristics)?
- **RQ2 (Evaluator Reliability & Aggregation):** How well does a single evaluator perform, and how many independent evaluators are needed to reach high coverage?

---

## 3. The Intervention: From 944 Rules to 9 Core Heuristics
Nielsen and Molich distilled decades of human factors standards into 9 intuitive principles (which Nielsen refined into the canonical [[nielsen-heuristics|10 Usability Heuristics]] in 1994):
1. Simple and natural dialogue
2. Speak the user's language
3. Minimize user memory load
4. Be consistent
5. Provide feedback
6. Provide clearly marked exits
7. Provide shortcuts
8. Good error messages
9. Prevent errors

---

## 4. Empirical Evaluation across 4 Systems

The authors tested Heuristic Evaluation across **four distinct interfaces** with between **34 and 77 evaluators** per system:

| System | Interface Domain | Evaluators ($N$) | Total Known Problems | Avg. Found by 1 Evaluator |
|---|---|---|---|---|
| **Teledata** | Screen-based videotex system | 37 CS students | 52 | **51%** |
| **Mantel** | Written spec for telephone UI | 77 industry/academic | 30 | **38%** |
| **Savings** | Voice-response banking menu | 34 CS students | 48 | **26%** |
| **Transport** | Voice-response logistics UI | 34 CS students | 34 | **20%** |

### Key Empirical Findings:
1. **The "Smart Lone Wolf" Fallacy (~35% Average):** Even the best single evaluator never found more than ~50% of the usability bugs. Across all four experiments, a single evaluator found only **20% to 51%** of the issues.
2. **Orthogonal Blind Spots (Different People See Different Bugs):** It was *not* the case that everyone found the "easy" bugs and missed the "hard" ones. Some of the most glaring usability flaws were completely missed by top evaluators, while some of the hardest problems were caught by evaluators who otherwise found very few issues.
3. **The 3–5 Evaluator Sweet Spot:** By taking the **mathematical union** of independent evaluations from **3 to 5 people**, coverage jumped to **~60%–75%** across all four systems. Beyond 5 evaluators, the curve flattened into diminishing returns.
4. **Strict Independence Before Debriefing:** To prevent groupthink and anchoring bias, each evaluator must inspect the interface **individually** and record their findings before any group aggregation meeting takes place.

```text
  % of Usability Problems Found (Empirical Aggregation Curve)
    100% ┼
     75% ┼                   ●───────●───────●  <-- Diminishing returns (>5)
     60% ┼             ●─────┘
     50% ┼         ●───┘  <-- 3–5 Evaluators = "Magic Number" (60%–75%)
     35% ┼     ●───┘      <-- 1 Evaluator alone averages only ~20%–51%!
      0% ┼─────┴───┴───┴─────┴───────┴───────┴────
               1   2   3     5       8      10   Number of Evaluators
```

---

## 5. Software Engineer Critique & Modern AI Reflection
- **Why "Have Our Senior Dev Check It" Fails:** In engineering teams, managers often ask one senior developer or designer to "do a quick UI pass." As this paper proves empirically, even the smartest person has cognitive blind spots and will miss ~65% of the bugs. Having **3 engineers each spend 30 minutes independently** beats having 1 expert spend 3 hours.
- **Limitations of Heuristic Evaluation:**
  - Finds **false positives** (issues that don't actually bother real users in context).
  - Cannot replace [[contextual-inquiry|Contextual Inquiry]] or real usability testing because heuristics evaluate the system against known rules, not unanticipated domain workflows.
- **Modern AI / Multi-Agent HCI Angle:** Could we simulate the "3–5 independent evaluators" curve using **multi-persona LLM agents** (e.g., Agent A prompted as a rushed novice, Agent B as a keyboard-only power user, Agent C auditing strictly for state feedback `H1`/`H9`), or do LLM evaluators suffer from correlated blind spots unlike human evaluators?

---

## 6. Social Media Hook
> *"Why did your team's smartest senior engineer miss 65% of the UI bugs? In 1990, Jakob Nielsen tested 182 evaluators across 4 systems and discovered a law of human blind spots: 1 person catches 35% of usability flaws, but 3–5 independent people catch 75%."*
