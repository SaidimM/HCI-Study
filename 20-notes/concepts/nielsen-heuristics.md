---
type: concept
first_seen: week-02
source: "Jakob Nielsen & Rolf Molich (1990), CHI '90; Jakob Nielsen (1994), 10 Usability Heuristics"
tags: [concept, week/02, nielsen, heuristics, evaluation, usability]
---

<p style="font-size: 0.8em; text-transform: uppercase; letter-spacing: 2px; opacity: 0.6; margin-bottom: 2px;">
HCI CORE CONCEPT · WEEK 02
</p>

# Nielsen's 10 Usability Heuristics

*Ten high-leverage rules of thumb that let engineers catch the majority of interface breakdowns before recruiting a single test user.*

> [!abstract] At a glance
> **What:** Ten broad principles of interaction design distilled by Jakob Nielsen and Rolf Molich for "discount usability engineering."
> **Why:** Running full laboratory user studies is slow and expensive; inspecting an interface against these 10 heuristics uncovers ~60–75% of usability bugs in hours (with 3–5 evaluators).
> **See it:** A background auto-scroll timer yanking a user's viewport away while they are reading an older item violates **H3: User Control and Freedom**.

> *"They are called 'heuristics' because they are broad rules of thumb and not specific usability guidelines."* — Jakob Nielsen (1994)

---

## 1. Definition (my own words, ≤ 3 sentences)
Nielsen's 10 Usability Heuristics are a foundational set of ten design principles used to systematically inspect user interfaces for usability problems (a method called **Heuristic Evaluation**). Rather than memorizing ten isolated rules, they can be understood as four functional families grounded in Don Norman's theory: **State & Feedback** (bridging the [[gulf-of-evaluation]]), **Mental Models & Language** (aligning the [[Conceptual Model, System Image and Real usage|System Image]]), **User Control & Safety** (preventing and recovering from [[slips-vs-mistakes]]), and **Cognitive Load & Efficiency** (supporting both novices and experts).

---

## 2. Core Architecture: The 10 Heuristics Grouped by Cognitive Function

```text
┌────────────────────────────────────────────────────────────────────────┐
│           NIELSEN'S 10 HEURISTICS (GROUPED BY NORMAN'S LOGIC)          │
├────────────────────────────────────────────────────────────────────────┤
│ FAMILY A: STATE & FEEDBACK (Bridging the Gulf of Evaluation)           │
│  H1. Visibility of System Status  → Keep users informed about what is  │
│      going on through appropriate, timely feedback (<100ms–1s).        │
│  H9. Help Users Recognize, Diagnose & Recover from Errors → Express    │
│      errors in plain language (no raw hex codes), state the cause,     │
│      and constructively suggest a fix.                                 │
├────────────────────────────────────────────────────────────────────────┤
│ FAMILY B: MENTAL MODELS & CONVENTIONS (System Image Matches User)      │
│  H2. Match Between System & Real World → Speak the user's vocabulary,  │
│      not internal database schemas; follow natural real-world mapping. │
│  H4. Consistency & Standards → Follow platform conventions (Jakob's    │
│      Law); don't make users wonder if different words mean the same.   │
├────────────────────────────────────────────────────────────────────────┤
│ FAMILY C: USER CONTROL & SAFETY (Preventing & Undoing Slips/Mistakes)  │
│  H3. User Control & Freedom → Provide clearly marked "emergency exits" │
│      (Undo, Redo, Cancel) and never hijack the user's locus of control.│
│  H5. Error Prevention → Even better than good error messages is a      │
│      careful design with constraints/interlocks that prevents errors.  │
├────────────────────────────────────────────────────────────────────────┤
│ FAMILY D: COGNITIVE LOAD & EFFICIENCY (Novice Tricycle + Pro Bicycle)  │
│  H6. Recognition Rather Than Recall → Minimize working memory load by  │
│      making objects, actions, and options visible in situ.             │
│  H7. Flexibility & Efficiency of Use → Provide accelerators (hotkeys,  │
│      macros) unseen by novices that speed up expert interaction.       │
│  H8. Aesthetic & Minimalist Design → Maximize Tufte's Data-Ink ratio;  │
│      every extra unit of info competes with relevant units of info.    │
│  H10. Help & Documentation → Provide concise, searchable, task-focused │
│       steps focused on the user's concrete current workflow.           │
└────────────────────────────────────────────────────────────────────────┘
```

---

## 3. Real-World Engineering Case Study: The Auto-Scroll Hijack (H3 vs. H1)

In our [[2026-10-16|Oct 16 Engineering Analysis]], we diagnosed a Windows desktop application with a horizontal list of items driven by a live background process:

```text
┌────────────────────────────────────────────────────────────────────────┐
│         DIAGNOSING THE HORIZONTAL LIST AUTO-SCROLL BREAKDOWN           │
├──────────────────────┬─────────────────────────────────────────────────┤
│ The Naive Pattern    │ Background process advances index → forces      │
│ (3.5s Snap-Back)     │ viewport to scroll back to active item while    │
│                      │ user is reading an older item's description.    │
├──────────────────────┼─────────────────────────────────────────────────┤
│ Heuristic Violated   │ H3: User Control and Freedom                    │
│                      │ The system steals the locus of control mid-task │
│                      │ without user consent, interrupting reflection.  │
├──────────────────────┼─────────────────────────────────────────────────┤
│ The Heuristic Fix    │ Sticky Scroll-Lock + "[ ● Live: #14 → ]" Pill   │
│ (H3 + H1 Harmony)    │ • H3 Preserved: Viewport stays parked on manual │
│                      │   scroll backward (zero forced timeout).        │
│                      │ • H1 Preserved: Edge pill signals live status   │
│                      │   and offers 1-click return to active index.    │
└──────────────────────┴─────────────────────────────────────────────────┘
```

---

## 4. How to Conduct a Heuristic Evaluation (The Two-Pass Protocol)

Nielsen & Molich (1990) established that a single evaluator only catches **~35%** of usability problems, whereas aggregating **3 to 5 independent evaluators** catches **~60–75%** before hitting diminishing returns:

1. **Pass 1 (Flow & Context):** Walk through the defined user tasks from start to finish to understand the overall interaction flow and mental model without stopping to nitpick.
2. **Pass 2 (Systematic Inspection):** Step through each screen state a second time, comparing every control, dialog, and feedback cue against **H1–H10** and logging each violation with a [[severity-rating|Severity Rating (0–4)]].

> [!note] Sidebar · Genuine Violation vs. Personal Taste
> A common novice trap in Heuristic Evaluation is logging subjective preferences (*"I don't like this shade of blue"* = Severity 0). Every logged violation must cite the specific **Heuristic (`H1`–`H10`)** and explain the concrete **cognitive or motor friction** it inflicts on the user's task.

---

## 5. Why it matters for software engineers
Engineers often treat UI review as a vague aesthetic vibe check (*"Looks good to me, ship it"*). Nielsen's 10 Heuristics turn usability review into a **deterministic static analysis linter for human-computer interaction**. Just as a compiler catches type errors before runtime, a 1-hour two-pass heuristic audit catches missing loading states (`H1`), exposed database jargon (`H2`), missing undo paths (`H3`), and unguarded destructive actions (`H5`) before code ever reaches production.

---

## Related concepts
- [[severity-rating]]
- [[constraints]]
- [[mapping]]
- [[gulf-of-execution]]
- [[gulf-of-evaluation]]
- [[slips-vs-mistakes]]
- [[Conceptual Model, System Image and Real usage]]

---

## Sources
[^1]: Nielsen, J., & Molich, R. (1990). *Heuristic evaluation of user interfaces*. Proceedings of the SIGCHI Conference on Human Factors in Computing Systems (CHI '90), 249–256.
[^2]: Nielsen, J. (1994). *Enhancing the explanatory power of usability heuristics*. Proceedings of the SIGCHI Conference on Human Factors in Computing Systems (CHI '94), 152–158.
