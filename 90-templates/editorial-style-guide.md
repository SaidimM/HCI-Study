---
type: style-guide
title: "The Editorial Knowledge System: Layout & Typography Guidelines"
created: 2026-10-13
tags: [style-guide, typography, tufte, swiss-grid, layout]
---

# The Editorial Knowledge System
## Layout, Typography & Visual Ergonomics for Obsidian

> *"Design is not decoration. It is the visual clarification of thought."* — Josef Müller-Brockmann

---

## 1. Theoretical Foundations

Our vault layout is engineered on seminal research from cognitive science, information visualization, and classical publication typography:

```
┌────────────────────────────────────────────────────────────────────────┐
│                   THE THREE PILLARS OF EDITORIAL DESIGN                │
├──────────────────────┬──────────────────────┬──────────────────────────┤
│   EDWARD TUFTE       │   MÜLLER-BROCKMANN   │   ROBERT BRINGHURST      │
│   (Information Vis)  │   (Swiss Grid)       │   (Typography)           │
├──────────────────────┼──────────────────────┼──────────────────────────┤
│ • Maximize Data-Ink  │ • Asymmetric Grid    │ • Typographic Measure    │
│ • Zero Chartjunk     │ • Order & Proportion │   (45–75 chars/line)     │
│ • Integrated graphics│ • Whitespace relief  │ • Vertical rhythm        │
└──────────────────────┴──────────────────────┴──────────────────────────┘
```

### A. The Data-Ink Ratio (Edward Tufte, 1983)
$$\text{Data-Ink Ratio} = \frac{\text{Data-Ink}}{\text{Total ink used to print the graphic}}$$
* **The Rule:** Every pixel that does not communicate information is noise. Avoid garish multi-colored cards (lime green, neon yellow, hot pink). They produce **Chartjunk** and clash violently with custom Obsidian themes.
* **The Remedy:** 100% theme-adaptive typography, pure monochrome TUI ASCII boxes, and real photographic artifacts.

### B. Eliminating the Split-Attention Effect (John Sweller, 1988)
* When explanatory text and visual evidence are separated vertically (e.g., text above, image below), the human brain incurs cognitive overhead scanning back and forth.
* By placing the **Introduction on the left (60%)** and the **Visual Artifact on the right (40%)**, the eye connects concept to proof in peripheral vision with zero cognitive friction.

### C. The Golden Measure (Robert Bringhurst, 1992)
* Text columns stretching across modern wide displays (120+ characters) cause eye tracking fatigue.
* The side-by-side flexbox naturally constrains the left text column to **45–70 characters per line**, matching Bringhurst’s optimal ergonomic reading measure.

---

## 2. The Color Discipline (Theme-Neutral Philosophy)

To ensure notes look stunning across **every Obsidian theme** (Default Dark, Minimal, Tokyo Night, Catppuccin, Gruvbox, or Clean White Paper Light):

1. **Never Hardcode Background Hex Colors:** Avoid `background: #1e1e2e;` or `border: 1px solid #3b82f6;`.
2. **Use Theme-Adaptive CSS Properties:**
   - Text color: inherits theme automatically (`color: inherit;`).
   - Subtle borders / lines: `border-left: 2px solid currentColor; opacity: 0.6;`
   - Image captions: `font-size: 0.82em; opacity: 0.75; line-height: 1.4;`
   - Image styling: `border-radius: 6px; width: 100%; box-shadow: 0 4px 12px rgba(0,0,0,0.12);`

---

## 3. Reusable Editorial Layout Components

### Component A: The Editorial Side-by-Side Card (Text Left, Image Right)

```html
<div style="display: flex; gap: 24px; align-items: flex-start; margin: 20px 0;">
  <!-- Left Column: The Narrative Argument (~60%) -->
  <div style="flex: 1.2;">
    <p style="font-size: 0.75em; text-transform: uppercase; letter-spacing: 1.5px; opacity: 0.6; margin-bottom: 4px;">
      CATEGORY / KICKER
    </p>
    <h4 style="margin-top: 0;">Heading Title</h4>
    <p>Detailed analysis connecting human intention to physical system mechanics...</p>
  </div>

  <!-- Right Column: Visual Artifact & Argumentative Caption (~40%) -->
  <div style="flex: 0.8; max-width: 260px; flex-shrink: 0;">
    <img src="assets/image-name.jpg" alt="Description" style="border-radius: 6px; width: 100%; box-shadow: 0 4px 12px rgba(0,0,0,0.15);">
    <p style="font-size: 0.82em; line-height: 1.4; opacity: 0.75; margin-top: 6px; border-left: 2px solid currentColor; padding-left: 8px;">
      <strong>Argumentative Caption:</strong> Explaining *why* this artifact proves or violates the theoretical principle.
    </p>
  </div>
</div>
```

---

### Component B: The Magazine Pull-Quote

```markdown
> *"A door that needs a sign that says 'PUSH' or 'PULL' is a confession of design failure."*  
> — **Don Norman**, *The Design of Everyday Things*
```

---

### Component C: The Pure Monochrome TUI ASCII Architecture Box

```text
┌────────────────────────────────────────────────────────────────────────┐
│                        TUI SYSTEM ARCHITECTURE                         │
├────────────────────┬───────────────────────────────────────────────────┤
│ Concept Layer      │ Concrete Explanation / Action                      │
├────────────────────┼───────────────────────────────────────────────────┤
│ 1. VISCERAL        │ Immediate sensory perception (<100ms response)    │
│ 2. BEHAVIORAL      │ Subconscious motor fluency & muscle memory         │
│ 3. REFLECTIVE      │ Conscious evaluation, storytelling & mental models │
└────────────────────┴───────────────────────────────────────────────────┘
```

---

### Component D: Argumentative Caption Rules

In high-end editorial publications, **captions are never lazy labels**:
- ❌ **Label:** *"Figure 1: Tesla door handle."*
- ✅ **Argument:** *"Tesla Model 3 Exterior Handle: The flush aerodynamic design strips away physical affordances and visible signifiers, causing first-time users to pause for 10+ seconds and experience self-blame."*

---

## 4. Magazine Components (added 2026-10-18)

Borrowed from The Economist, Wired, Monocle, Businessweek and Tufte. They organize reading; none need heavy CSS.

### Note anatomy (every note)
```
KICKER · DOMAIN
# Title
*Standfirst: one-sentence takeaway.*
> [!abstract] At a glance   (definition · why · example)
Body: short sections, ≤ 70 chars/line, `---` between sections
Pull-quote
Sidebar (callout)
Editor's intention · Why it matters for HCI
My thoughts
Sources[^1]
```

### Component E: Kicker + Standfirst
```markdown
<p style="font-size: 0.8em; text-transform: uppercase; letter-spacing: 2px; opacity: 0.6; margin-bottom: 2px;">HCI CORE CONCEPT · WEEK 01</p>

# Signifier

*A signal that tells you where the action happens, and what state the system is in.*
```

### Component F: At-a-glance box
```markdown
> [!abstract] At a glance
> **What:** one-line definition
> **Why:** the problem it solves
> **See it:** one concrete example
```

### Component G: Sidebar (Monocle-style)
Side material that must not interrupt the argument.
```markdown
> [!note] Sidebar · Gibson vs. Norman
> Gibson's affordance is relational; Norman's signifier is the perceivable cue.
```

### Component H: Big-number callout (Businessweek-style)
```html
<p style="font-size: 2.4em; font-weight: 700; line-height: 1; margin: 0;">50 ms</p>
<p style="font-size: 0.8em; opacity: 0.7; margin-top: 2px;">time users need to judge a website's visual appeal (Lindgaard et al.)</p>
```

### Component I: Footnotes as marginalia (Tufte)
Put sources and asides in `[^1]` footnotes so the body stays clean.

### Rules
- One idea per note, ≤ 1 screen per section.
- Fixed section names per note type ("departments") so the reader always knows where to look.
- Monochrome and theme-adaptive; hierarchy via size, weight, space, never color.
