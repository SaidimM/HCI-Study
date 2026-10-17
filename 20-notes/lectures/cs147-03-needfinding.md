---
week: 2
date: 2026-10-17
source: "Stanford CS147: Design Discovery & Needfinding (Prof. James Landay)"
tags: [lecture, week/02, needfinding, design-thinking, engelbart, norman]
---

# Lecture Notes — CS147 Lecture 3: Needfinding & Design Discovery

> Lecture slides: [02-design-discovery.pdf](https://hci.stanford.edu/courses/cs147/) / CS147 Needfinding  
> Key thematic contrast: **Superficial Styling vs. Human Needfinding** (Starck / Fukasawa vs. Douglas Engelbart)

---

## 1. The Opening Provocation: What is Design?

In the opening 20 minutes of the Needfinding lecture, Prof. James Landay confronts the class with two celebrated icons of modern industrial design:

```text
┌────────────────────────────────────────────────────────────────────────┐
│                   THE FORM VS. FUNCTION PARADOX                        │
├────────────────────┬─────────────────────────────┬─────────────────────┤
│ Artifact           │ Designer & Aesthetic Vision │ Usability Breakdown │
├────────────────────┼─────────────────────────────┼─────────────────────┤
│ **Wall-Mounted**   │ **Naoto Fukasawa (1999)**   │ Hidden controls, no │
│ **CD Player**      │ Minimalist, poetic metaphor │ track signifiers,   │
│ (Muji)             │ ("ventilation fan cord")    │ exposed disc dust   │
├────────────────────┼─────────────────────────────┼─────────────────────┤
│ **Juicy Salif**    │ **Philippe Starck (1990)**  │ Splatters juice,    │
│ **Citrus Juicer**  │ Sculptural centerpiece,     │ drips on legs, pips │
│ (Alessi)           │ alien spider silhouette     │ drop into glass     │
└────────────────────┴─────────────────────────────┴─────────────────────┘
```

---

## 2. Artifact Deconstruction: Don Norman's Three Levels of Processing

Why do museums (like MoMA) celebrate these objects while usability engineers cringe? Don Norman's framework in [[three-levels-of-processing]] explains the split:

<div style="display: flex; gap: 24px; align-items: flex-start; margin: 20px 0;">
  <!-- Left Column: The Narrative Argument (~60%) -->
  <div style="flex: 1.2;">
    <p style="font-size: 0.75em; text-transform: uppercase; letter-spacing: 1.5px; opacity: 0.6; margin-bottom: 4px;">
      MINIMALIST POETRY · THE "WITHOUT THOUGHT" METAPHOR
    </p>
    <h4 style="margin-top: 0;">A. The Muji Wall-Mounted CD Player (Naoto Fukasawa, 1999)</h4>
    <p>Fukasawa modeled this player on a traditional kitchen exhaust fan: pulling the dangling cord starts the disc spinning, filling the room with music like a fresh breeze.</p>
    <ul>
      <li><strong>Hidden Controls:</strong> The pull-cord toggles power/play, but track skipping and volume are tiny, indistinguishable nubs tucked blindly on the top rim.</li>
      <li><strong>Missing Signifiers & Evaluation:</strong> No digital track display, no elapsed time, no shuffle/repeat indicators.</li>
      <li><strong>Exposed Mechanics:</strong> An open spinning disc at ~500 RPM leaves optics and media vulnerable to airborne dust and accidental touch.</li>
      <li><strong>Verdict:</strong> An exquisite triumph of <strong>Visceral</strong> and <strong>Reflective</strong> design, but severely compromised in <strong>Behavioral</strong> usability.</li>
    </ul>
  </div>

  <!-- Right Column: Visual Artifact & Argumentative Caption (~40%) -->
  <div style="flex: 0.8; max-width: 280px; flex-shrink: 0;">
    <img src="assets/muji-wall-mounted-cd-player.jpg" alt="Muji Wall-Mounted CD Player designed by Naoto Fukasawa" style="border-radius: 6px; width: 100%; box-shadow: 0 4px 12px rgba(0,0,0,0.15);">
    <p style="font-size: 0.82em; line-height: 1.4; opacity: 0.75; margin-top: 6px; border-left: 2px solid currentColor; padding-left: 8px;">
      <strong>Muji Wall-Mounted CD Player (Naoto Fukasawa, 1999):</strong> By adopting the ventilation fan cord metaphor, Fukasawa achieved iconic Zen minimalism at the expense of primary controls and operational feedback.
    </p>
  </div>
</div>

<div style="display: flex; gap: 24px; align-items: flex-start; margin: 20px 0;">
  <!-- Left Column: The Narrative Argument (~60%) -->
  <div style="flex: 1.2;">
    <p style="font-size: 0.75em; text-transform: uppercase; letter-spacing: 1.5px; opacity: 0.6; margin-bottom: 4px;">
      SCULPTURE VS. UTILITY · CONVERSATION PIECE
    </p>
    <h4 style="margin-top: 0;">B. Philippe Starck's "Juicy Salif" (Alessi, 1990)</h4>
    <p>Sketched on a pizzeria napkin in Italy, Starck's cast-aluminum spider squeezer is an iconic museum piece whose designer famously proclaimed: <em>"It is not meant to squeeze lemons, it is meant to start conversations."</em></p>
    <ul>
      <li><strong>Countertop Splatter:</strong> Juice tracks down the outward-splayed spider legs, splattering onto the counter rather than channeling cleanly into a cup.</li>
      <li><strong>Zero Filtering:</strong> Without a perforated basin or sieve, lemon pips and pulp drop straight into the drinking glass.</li>
      <li><strong>Unstable Tripod Physics:</strong> Downward rotational force on a high center of gravity creates tipping torque.</li>
      <li><strong>Verdict:</strong> Pure <strong>Reflective / Sculptural Art</strong> masquerading as an everyday tool. Behavioral usability = 1/10.</li>
    </ul>
  </div>

  <!-- Right Column: Visual Artifact & Argumentative Caption (~40%) -->
  <div style="flex: 0.8; max-width: 280px; flex-shrink: 0;">
    <img src="assets/philippe-starck-juicy-salif.jpg" alt="Philippe Starck Juicy Salif lemon squeezer for Alessi" style="border-radius: 6px; width: 100%; box-shadow: 0 4px 12px rgba(0,0,0,0.15);">
    <p style="font-size: 0.82em; line-height: 1.4; opacity: 0.75; margin-top: 6px; border-left: 2px solid currentColor; padding-left: 8px;">
      <strong>Juicy Salif (Philippe Starck, Alessi, 1990):</strong> The definitive example of form prioritized over function. The tripod geometry splatters acid on countertops and drops seeds directly into the glass.
    </p>
  </div>
</div>


---

## 3. Landay's Core Question: Why Did Douglas Engelbart Invent His Tools?

Landay asks the class: *“Try to remember last lecture—Douglas Engelbart's inventions. Why did he invent those?”*

```text
┌────────────────────────────────────────────────────────────────────────┐
│                   STYLING VS. ENGELBARTIAN NEEDFINDING                 │
├───────────────────────┬────────────────────────────────────────────────┤
│ Industrial Styling    │ Starts with form, aesthetic novelty, or tech;  │
│ (Starck / Gadgeteers) │ forces humans to adapt to the artifact.        │
├───────────────────────┼────────────────────────────────────────────────┤
│ Engelbartian HCI      │ Starts with a critical, unaddressed HUMAN NEED;│
│ (Augmentation)        │ engineers tools to amplify human capability.   │
└───────────────────────┴────────────────────────────────────────────────┘
```

### The Genesis of NLS (1962–1968)
In 1962, Douglas Engelbart published his manifesto, ***Augmenting Human Intellect: A Conceptual Framework***. His starting point was not: *"Wouldn't a wooden box with rolling wheels look futuristic?"*

His starting point was an existential observation about human civilization:
1. **Exponential Complexity vs. Biological Bottleneck:** The urgent problems confronting humanity (post-war geopolitical tension, global health, climate, large-scale systems engineering) were scaling at an **exponential rate**.
2. **Cognitive Stagnation:** The biological human brain has finite working memory (~4–7 chunks), linear processing speed, and localized presence.
3. **The Urgent Human Need:** Unless we build external cognitive prosthetics to **augment** human intellect and enable high-bandwidth collaboration, humanity will be overwhelmed by the complexity of its own creations.

### Every Engelbart Invention Was Rooted in a Specific Need:
- **The Mouse (1964):** *Need:* How can a knowledge worker rapidly and precisely target any symbolic token on a 2D CRT screen without taking their eyes off the text? (Tested empirically against light pens, tracking balls, and knee pedals).
- **Hypertext & Outline Processors:** *Need:* How can researchers navigate complex associative trails of thought rather than being trapped in flat, linear paper documents?
- **Real-Time Collaborative Screen Sharing & Video (1968):** *Need:* Complex problems cannot be solved in cognitive isolation; distributed teams need shared conceptual synchronization across distance.
- **The 5-Key Chorded Keyset:** *Need:* Allow continuous alphanumeric commands with the left hand concurrently while the right hand maneuvers the mouse—maximizing throughput for the expert knowledge worker.

---

## 4. The Pedagogical Takeaway: Why Needfinding Precedes Everything

Landay's juxtaposition delivers the foundational premise of CS147:

1. **Design is NOT Superficial Styling:**
   - Styling makes things look enticing on a store shelf or in a design magazine.
   - Design solves real, observed human breakdowns.
2. **Technology for Technology's Sake Fails:**
   - Building a system without understanding the user's real task and context produces either high-tech paperweights or frustrating hazards.
3. **Needfinding Uncovers Latent Needs:**
   - Users often cannot articulate what they need (e.g., knowledge workers in 1962 did not ask for a "mouse" or "hypertext").
   - By observing real human workflows, identifying physical and cognitive friction, and understanding their goals, designers discover **deep needs** rather than superficial wants.

---

---

## 5. Empathy & The Golden Rule: "You Are Not The Customer"

> *"The fastest way to build a catastrophic interface is to assume the user thinks like you."*  
> — **Prof. James Landay**

```text
┌────────────────────────────────────────────────────────────────────────┐
│                   THE DESIGNER PROJECTION BIAS TRAP                    │
├────────────────────┬───────────────────────────────────────────────────┤
│ The Designer /     │ • Deep technical literacy & architectural knowledge│
│ Engineer's Mind    │ • Knows underlying data structures & edge cases   │
│                    │ • Tolerates high cognitive abstraction            │
├────────────────────┼───────────────────────────────────────────────────┤
│ The Real Customer /│ • Task-oriented: wants to complete a goal fast    │
│ User's Reality     │ • Fragmented attention, stress, and noise         │
│                    │ • Operates on habit, heuristics, and recognition  │
└────────────────────┴───────────────────────────────────────────────────┘
```

- **Cognitive Bias Grounding:** Known in cognitive psychology as the **False Consensus Effect** (or *Curse of Knowledge*). Designers unconsciously project their own mental models onto users.
- **Empathy as an Engineering Requirement:** Empathy is not soft sentimentality; it is a systematic methodology to suspend your assumptions and observe the genuine physical, cognitive, and social constraints of another human being.

---

## 6. The Four Phases of the Design Process

```text
┌────────────────────────────────────────────────────────────────────────┐
│                    THE 4-PHASE HCI DESIGN LIFECYCLE                    │
├───────────────────┬────────────────────────────────────────────────────┤
│ Phase             │ Primary Activities & Deliverables                  │
├───────────────────┼────────────────────────────────────────────────────┤
│ **1. Discovery**  │ • Needfinding & Contextual Inquiry                 │
│                   │ • Understand users in their actual environments    │
│                   │ • Competitive analysis & evaluating existing tools │
├───────────────────┼────────────────────────────────────────────────────┤
│ **2. Design**     │ • Divergent ideation & brainstorming (HMW)        │
│    **Exploration**│ • Scenarios, personas, storyboards                 │
│                   │ • Low-fidelity paper / digital prototypes          │
├───────────────────┼────────────────────────────────────────────────────┤
│ **3. Design**     │ • Medium-to-high fidelity interactive prototypes   │
│    **Refinement** │ • Formative usability testing & pilot evaluations  │
│                   │ • Heuristic evaluations (Nielsen's 10)             │
├───────────────────┼────────────────────────────────────────────────────┤
│ **4. Production** │ • Implementation (clean code, APIs, design systems)│
│                   │ • Summative evaluation & A/B testing telemetry     │
│                   │ • Post-launch monitoring & iterative maintenance   │
└───────────────────┴────────────────────────────────────────────────────┘
```

---

## 7. Contextual Inquiry: The Master-Apprentice Model (MAP)

When gathering user needs, traditional methods have fatal blind spots:
- **Surveys:** Tell you what users *claim* they want (rationalized, shallow, prone to self-report bias).
- **Conference Room Interviews:** Users recount an idealized fairy tale of their workflow, omitting real hacks, workarounds, and mistakes.
- **A/B Testing:** Excellent for tweaking existing local optima (button colors, placement), but completely incapable of discovering *what new paradigm needs to exist*.

```text
┌────────────────────────────────────────────────────────────────────────┐
│                   THE MASTER-APPRENTICE MODEL (MAP)                    │
├────────────────────┬───────────────────────────────────────────────────┤
│ The User = Master  │ The craftsman who holds deep, tacit domain skills.│
│ (The Expert)       │ Performs work naturally in context.               │
├────────────────────┼───────────────────────────────────────────────────┤
│ The Designer =     │ Humble learner who shadows the master. Observes   │
│ Apprentice         │ concrete actions, notices workarounds, and asks   │
│ (The Observer)     │ clarifying questions without interrupting flow.   │
└────────────────────┴───────────────────────────────────────────────────┘
```

### "Where, What, and How Leads to Why"
You cannot uncover deep needs by bluntly asking *"Why do you need this?"* (users will fabricate logical-sounding excuses). Instead:
1. **WHERE:** Observe the physical and social setting (lighting, noise, interruptions, multi-window clutter).
2. **WHAT:** Observe the concrete artifacts used (paper sticky notes, cheat-sheet printouts, side spreadsheets).
3. **HOW:** Observe the specific micro-actions, hesitations, sighs, and repeated steps.
4. **WHY (The Latent Need):** The pattern of *Where, What, and How* illuminates the unarticulated root problem.

---

## 8. The Seminal Reading: Beyer & Holtzblatt on *Contextual Design*

The article Landay references is the foundational text by **Hugh Beyer & Karen Holtzblatt**:
> **Beyer, H., & Holtzblatt, K. (1999). *Contextual Design*. ACM Interactions, 6(1)**  
> *(And their seminal book: Contextual Design: Defining Customer-Centered Systems, Morgan Kaufmann)*

### What the Article Is About:
1. **The Tacit Knowledge Problem:**
   - Expert users cannot articulate how they do their work because expertise is stored in subconscious, procedural memory (tacit knowledge).
   - If you remove them from their desk to an interview room, you sever their cognitive triggers.
2. **The Four Core Principles of Contextual Inquiry:**
   - **Context:** Go to where the work happens. Observe ongoing, real tasks in real time rather than retrospective summaries.
   - **Partnership:** Establish a collaborative Master-Apprentice relationship. The user teaches; the apprentice observes and interprets.
   - **Interpretation:** Develop a shared understanding of what observed behaviors mean. When an apprentice notices a strange step, they propose an interpretation to the master in real time (*"I see you checked that external sheet first—is that because the database doesn't auto-sync?"*), allowing the user to confirm or refine it.
   - **Focus:** Keep the observation anchored in your project's problem space, while remaining open to unexpected breakthroughs.

*(Note: In CS147, this is paired with **Dev Patnaik & Robert Becker (1999), "Needfinding: The Essence of Design"**, which establishes that **needs outlast solutions**—solutions change with technology, but underlying human needs endure across decades).*

---

---

## 9. Contextual Inquiry in Practice: "Unique or One of Many?"

```text
┌────────────────────────────────────────────────────────────────────────┐
│                   THE "UNIQUE OR ONE OF MANY?" FILTER                  │
├────────────────────┬───────────────────────────────────────────────────┤
│ Unique Quirk       │ An idiosyncratic preference or unusual workaround │
│ (The n=1 Trap)     │ of a single individual. Don't redesign for this!  │
├────────────────────┼───────────────────────────────────────────────────┤
│ One of Many        │ A specific manifestation of a widespread, systemic│
│ (Systemic Need)    │ breakdown shared across the user population.      │
└────────────────────┴───────────────────────────────────────────────────┘
```

### What It Means & Why It Matters
When you observe a user doing something peculiar or struggling with a tool, you must immediately ask: *"Is this behavior **unique** to this one eccentric user, or is it **one of many** ways people cope with a deeper systemic failure?"*

- **Example (The Post-It Note on the Terminal):**
  - *Observation:* You shadow a software developer who writes down git branch names and ticket numbers on a physical yellow sticky note stuck to their bezel.
  - *Is it Unique?* If you think it's unique, you might dismiss it: *"Oh, this developer just loves paper."*
  - *Or is it One of Many?* When you observe three other developers:
    - Developer B keeps a scratchpad file `notes.txt` open in a split pane.
    - Developer C runs `git status` every 90 seconds because they can't remember their current branch context.
  - *Synthesis:* The sticky note is **one of many** workarounds for the exact same underlying breakdown: **poor branch state persistence in the CLI**. The latent need is continuous peripheral awareness of branch and task context.

### The Interpretation Principle: Sharing Your Mental Pathway
Users naturally speak in **summaries** (*"I usually just import the dataset and it works fine"*). As an apprentice, you must push for **concrete details** (*"Can you show me the last time you did it?"*).
When you notice a strange action, **share your interpretation immediately** to validate your mental model:
- *"I noticed you paused and opened a separate spreadsheet before submitting that form. It seems like you're verifying exchange rates because this tool doesn't update currencies automatically—is that right?"*
- This gives the user the chance to say: *"Actually, no! I do that because this form has a bug where it crashes if I don't format the commas first."* Sharing the reasoning prevents false designer assumptions.

---

## 10. Field Interview Craft: Mechanics & Mindset

### A. The Two-Person Rule
Never conduct field interviews alone if you can avoid it:
1. **The Interviewer (Driver):** Maintains continuous eye contact, active listening, builds empathy and rapport, and guides the conversational flow.
2. **The Scribe / Observer (Recorder):** Takes verbatim notes, records exact quotes, logs non-verbal cues (hesitations, sighs, body language), and captures timestamps.

### B. Decoupling Ego from Critique
When interviewing, users will often vent intense frustration or criticize existing tools:
- **Rule:** *"It is NOT about you."*
- Even if the user is criticizing a prototype *you personally spent 40 hours building*, do not defend the design.
- Treat criticism as pure gold: a user's anger marks the exact location of a severe **Gulf of Execution** or cognitive friction point. Our sole objective is to discover how to make life easier for them.

---

## 11. *In Situ* vs. Retrospective Surveys vs. ESM (Experience Sampling)

```text
┌────────────────────────────────────────────────────────────────────────┐
│                   RESEARCH CAPTURE METHODS COMPARED                    │
├───────────────────┬───────────────────┬────────────────────────────────┤
│ Method            │ Capture Timing    │ Cognitive Vulnerability        │
├───────────────────┼───────────────────┼────────────────────────────────┤
│ **Retrospective** │ Hours or days     │ Heavy memory distortion,       │
│ **Survey**        │ after the event   │ Recency Bias, Peak-End Rule.   │
├───────────────────┼───────────────────┼────────────────────────────────┤
│ **In Situ**       │ In the exact room │ Minimal memory loss; captures  │
│ **Observation**   │ while work happens│ authentic physical context.    │
├───────────────────┼───────────────────┼────────────────────────────────┤
│ **ESM / EMA**     │ Prompted in-the-  │ Interruption friction, but raw │
│ (Experience Sample│ moment via device │ ecological momentary truth.    │
└───────────────────┴───────────────────┴────────────────────────────────┘
```

### A. Why Retrospective Surveys Yield Distorted Data
Daniel Kahneman's behavioral economics proved that human memory evaluates past experiences using the **Peak-End Rule**:
- People remember only the most intense emotional moment (the "peak") and the final moment (the "end"), completely ignoring the duration or everyday baseline reality.
- *Software Example:* Ask an engineer on Friday: *"How was the deploy tool this week?"* If the deploy succeeded smoothly 10 minutes ago, they say *"Great!"* (ignoring 4 days of grueling configuration hell).
- **In Situ ("in place"):** Observing the user live in their natural environment bypasses reflective storytelling and reveals the ground truth.

### B. ESM (Experience Sampling Method) & Context-Triggered Sampling
- **Traditional ESM:** A smartphone or smartwatch prompts the user at random or fixed times (*"What are you doing right now? Rate your cognitive load 1–5"*).
- **Context-Triggered Sampling (Smart ESM):** Sensors trigger micro-surveys based on events (e.g., prompting immediately after a build fails, after a 2-hour coding sprint, or upon exiting a physical location).

### C. The Ethical Tension: Research Value vs. Surveillance & Privacy
You raised a vital critique: *Doesn't context-triggered sampling feel creepy, intrusive, or offensive like targeted ad surveillance (TikTok, Amazon, Taobao)?*

```text
┌────────────────────────────────────────────────────────────────────────┐
│               HCI RESEARCH SAMPLING VS. SURVEILLANCE ADS               │
├───────────────────────┬────────────────────────────────────────────────┤
│ Commercial Ads        │ Covert, non-consensual tracking, hidden in     │
│ (Surveillance Cap.)   │ terms of service; monetizes private behavior.  │
├───────────────────────┼────────────────────────────────────────────────┤
│ HCI Context-Triggered │ Explicit informed consent (IRB approved);      │
│ Research Sampling     │ user volunteers; transparent purpose & control.│
└───────────────────────┴────────────────────────────────────────────────┘
```

1. **Informed Consent & Voluntary Partnership:** In academic/ethical HCI, participants voluntarily install the sampling tool with clear disclosures of what sensors are active and can snooze or opt out anytime.
2. **The "Interruption Fatigue" Tax:** Even with consent, popping up surveys during high-focus tasks causes **attention residue** and resentment. Good HCI sampling uses:
   - *Micro-interactions:* 1-tap rating (< 3 seconds).
   - *Task Boundaries:* Pinging only at natural transition points (e.g., after closing an app, not in the middle of typing a line of code).
3. **The "Creepiness Boundary":** The moment software acts as if it is "listening" or peering into private lives without visible signifiers, trust collapses. Systems must maintain strict transparency and on-device processing.

---

## 💡 Concept Connections & Terms

- [[three-levels-of-processing]] — Visceral, Behavioral, and Reflective levels (Norman).
- [[contextual-inquiry]] — Field research grounded in the Master-Apprentice relationship.
- [[experience-sampling-method]] — In situ momentary sampling (ESM/EMA).
- [[peak-end-rule]] — Cognitive heuristic causing retrospective survey distortion (Kahneman).
- [[gulf-of-execution]] — The distance between user intent and the artifact's physical interface.
- [[gulf-of-evaluation]] — The lack of feedback/signifiers.
- [[mental-model]] — The user's internal simulation vs. the designer's projection bias.

---

## ❓ Open Questions (→ [[questions]])

- *When designing AI-augmented interfaces, how do we distinguish between genuine "Engelbartian augmentation" (amplifying human problem-solving) and superficial "Starckian novelty" (gratuitous chat widgets and animated confetti)?*
- *How does the Master-Apprentice model apply when studying knowledge workers collaborating with autonomous AI agents whose internal states are black boxes?*
- *How can context-triggered sampling be designed to detect opportune cognitive boundaries without causing attention fragmentation or surveillance paranoia?*


