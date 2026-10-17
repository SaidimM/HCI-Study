---
type: concept
first_seen: week-{{week}}
source: "{{source}}"
tags: [concept, week/{{week}}, {{tag}}]
---

<p style="font-size: 0.8em; text-transform: uppercase; letter-spacing: 2px; opacity: 0.6; margin-bottom: 2px;">
HCI CORE CONCEPT · WEEK {{week}}
</p>

# {{title}}

*{{standfirst: one-sentence takeaway}}*

> [!abstract] At a glance
> **What:** {{one-line definition}}
> **Why:** {{the problem it solves}}
> **See it:** {{one concrete example}}

> *"{{quote}}"* — {{author}}

---

## 1. Definition (my own words, ≤ 3 sentences)
{{definition}}

---

## 2. Core Architecture: Theoretical Model

```
┌────────────────────────────────────────────────────────────────────────┐
│                        {{title}} SYSTEM MODEL                          │
└───────────────────────────────────┬────────────────────────────────────┘
                                    │
                                    ▼
                         [ TUI ASCII DIAGRAM ]
```

---

## 3. Real-World Physical & Digital Artifacts

<div style="display: flex; gap: 24px; align-items: flex-start; margin: 20px 0;">
  <!-- Left Column: The Narrative Argument (~60%) -->
  <div style="flex: 1.2;">
    <p style="font-size: 0.75em; text-transform: uppercase; letter-spacing: 1.5px; opacity: 0.6; margin-bottom: 4px;">
      ARTIFACT 01 · REAL-WORLD ANALYSIS
    </p>
    <h4 style="margin-top: 0;">Case Name</h4>
    <p>Detailed analysis of how this physical or digital interface illustrates the concept in practice...</p>
  </div>

  <!-- Right Column: Visual Evidence & Argumentative Caption (~40%) -->
  <div style="flex: 0.8; max-width: 260px; flex-shrink: 0;">
    <img src="assets/example.jpg" alt="Example Artifact" style="border-radius: 6px; width: 100%; box-shadow: 0 4px 12px rgba(0,0,0,0.15);">
    <p style="font-size: 0.82em; line-height: 1.4; opacity: 0.75; margin-top: 6px; border-left: 2px solid currentColor; padding-left: 8px;">
      <strong>Argumentative Caption:</strong> Explaining *why* this artifact proves or violates the core HCI theory.
    </p>
  </div>
</div>

---

## 4. Analytical Contrasts & Failure Modes

```
┌─────────────────────────────────┬─────────────────────────────────┐
│        OPTIMAL PATTERN          │       PATHOLOGICAL BREAKDOWN    │
├─────────────────────────────────┼─────────────────────────────────┤
│ • Strong, natural mapping       │ • Missing or deceptive signals  │
│ • Subconscious motor fluency    │ • Conscious cognitive friction  │
│ • Immediate sensory feedback    │ • User self-blame & error loops │
└─────────────────────────────────┴─────────────────────────────────┘
```

---

## 5. Why it matters for software engineers
{{engineering_reflection}}

---

## Related concepts
- [[ ]]
- [[ ]]

---

## Sources
[^1]: {{citation}}
