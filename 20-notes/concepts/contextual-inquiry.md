---
type: concept
first_seen: week-02
source: "Beyer & Holtzblatt, Contextual Design (1999); Stanford CS147"
tags: [concept, week/02, contextual-inquiry, needfinding, methods]
---

<p style="font-size: 0.8em; text-transform: uppercase; letter-spacing: 2px; opacity: 0.6; margin-bottom: 2px;">
HCI CORE METHODOLOGY · QUALITATIVE DISCOVERY
</p>

# Contextual Inquiry

*Watch people do real work in their real setting, and let them teach you.*

> [!abstract] At a glance
> **What:** A field research method built on the master-apprentice model.
> **Why:** It reveals tacit reasons behind breakdowns that interviews miss.
> **See it:** Shadowing a user at their desk instead of asking them in a meeting room.

> *"If you want to understand how a master craftsman works, you don't send them a survey or invite them to a conference room. You go to their workshop, watch their hands, and learn as an apprentice."* — Hugh Beyer & Karen Holtzblatt

---

## 1. Definition (my own words, ≤ 3 sentences)
Contextual Inquiry is a field-based qualitative research method where the researcher shadows and interviews users in their actual working environment while they perform real tasks. It replaces passive interrogations with the **Master-Apprentice Model**, where the user teaches and the researcher observes concrete details rather than abstract summaries. By grounding observation in the *Where, What, and How*, designers uncover the tacit, unarticulated *Why* behind user breakdowns.

---

## 2. Theoretical Architecture: The Four Core Principles

```text
┌────────────────────────────────────────────────────────────────────────┐
│                   THE 4 PRINCIPLES OF CONTEXTUAL INQUIRY               │
├────────────────────┬───────────────────────────────────────────────────┤
│ 1. Context         │ Go to the actual site. Observe ongoing real-world │
│                    │ practices in situ, not sanitized lab simulations. │
├────────────────────┼───────────────────────────────────────────────────┤
│ 2. Partnership     │ The Master-Apprentice Model. Elevate the user as  │
│                    │ the expert craftsman; the designer is apprentice. │
├────────────────────┼───────────────────────────────────────────────────┤
│ 3. Interpretation  │ Shared sense-making. Share your mental reasoning  │
│                    │ in real-time to validate hypotheses with the user.│
├────────────────────┼───────────────────────────────────────────────────┤
│ 4. Focus           │ Steer observations toward the project's scope     │
│                    │ while remaining receptive to surprising anomalies.│
└────────────────────┴───────────────────────────────────────────────────┘
```

---

## 3. The "Unique or One of Many?" Heuristic

When observing a user struggling or deploying a custom workaround, the researcher must filter the observation:
1. **Unique (Idiosyncratic Quirk):** A personal preference or habit unique to one individual ($n=1$). Redesigning around this risks breaking standard workflows for others.
2. **One of Many (Systemic Need):** A localized manifestation of a universal breakdown. Different users may adopt different workarounds (e.g., sticky notes, text scratchpads, repeated CLI status commands), but all are compensating for the *same* underlying system flaw.

---

## 4. Why Retrospective Recalls Fail (The In Situ Advantage)

```text
┌────────────────────────────────────────────────────────────────────────┐
│                  RETROSPECTIVE RECALL VS. IN SITU REALITY              │
├───────────────────────┬────────────────────────────────────────────────┤
│ Retrospective Survey  │ • Governed by Kahneman's Peak-End Rule.        │
│ (Recalled Summary)    │ • Distorted by rationalization and ego defense.│
│                       │ • Omits tacit habits, workarounds, and bugs.   │
├───────────────────────┼────────────────────────────────────────────────┤
│ In Situ Observation   │ • Captures grounded moment-to-moment reality.  │
│ (Contextual Inquiry)  │ • Reveals physical artifacts (notes, cheats).  │
│                       │ • Exposes genuine cognitive breakdowns live.   │
└───────────────────────┴────────────────────────────────────────────────┘
```

---

## 5. Related Concepts

- [[mental-model]] — The user's internal simulation vs. designer assumptions.
- [[gulf-of-execution]] — Uncovering what actions users struggle to perform.
- [[gulf-of-evaluation]] — Identifying missing system feedback in situ.
- [[experience-sampling-method]] — Automated momentary in-context data capture.
