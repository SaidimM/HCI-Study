---
date: 2026-11-02
type: arxiv-digest
category: cs.HC
tags: [hci, arxiv, reading-queue]
---

# 📡 arXiv cs.HC Digest — 2026-11-02

> Automated intake of the latest Human-Computer Interaction preprints.
> Pick 1–2 papers that look promising to dissect using [[90-templates/paper-note|Paper Note Template]].

---

### 1. GazeRIB: Systematic Evaluation of Multi-Reader Gaze-Guided Chest X-ray Learning
- **Authors**: Nattakorn Kittisut, Roy M. Gabriel, Marly van Assen et al. (7 authors)
- **Date**: 2026-10-30 | **Links**: [Abstract](https://arxiv.org/abs/2610.42152v1) | [PDF](https://arxiv.org/pdf/2610.42152v1)
- **Status**: [ ] Unread  |  [ ] Dissected for Social Post

<details>
<summary><b>📖 Abstract / Summary (click to expand)</b></summary>

Radiologists' visual attention can supervise medical image learning, but how reader panel composition affects its value remains untested. We evaluated GazeRIB (Gaze-guided Radiologist-Informed Blackout), which masks unviewed regions during training and uses unmasked images at inference. Eight experts repeatedly read the same 80 chest X-rays (CXRs). We compared individual readers with three-, five- and eight-reader panels across seven architectures and 10 seeds, evaluating 910 models on a separate 2,897-CXR cohort for four-class severity prediction. Every panel improved macro F1 over the no-gaze baseline by 5.33-7.47 percentage points (pp; Bonferroni-adjusted p < 0.007); no individual reader reached significance on this endpoint. Three readers captured 73-80% of the eight-reader gain in macro F1, the area under the receiver-operating-characteristic curve (ROC-AUC) and the area under the precision-recall curve (AU-PRC). On external validation without retraining, all four panels improved ROC-AUC on SIIM-FISABIO-RSNA by +1.93 to +4.24 pp (p <= 0.004); on MIMIC-Eye no panel differed significantly from baseline, whereas the single-reader average declined (-1.40 pp, p = 0.008). Reader composition therefore influenced performance, although transfer depended on the cohort.

</details>

---

### 2. AutoAnalysis: An automated, self-updating meta-analysis of human-AI collaboration
- **Authors**: Michelle Vaccaro, Abdullah Almaatouq, Thomas W. Malone
- **Date**: 2026-10-30 | **Links**: [Abstract](https://arxiv.org/abs/2610.42001v1) | [PDF](https://arxiv.org/pdf/2610.42001v1)
- **Status**: [ ] Unread  |  [ ] Dissected for Social Post

<details>
<summary><b>📖 Abstract / Summary (click to expand)</b></summary>

As generative artificial intelligence (AI) becomes more capable and widely used, understanding when and how humans should work with these systems is becoming increasingly important. However, the empirical evidence in this space offers conflicting recommendations, which leaves individuals and organizations without clear guidance on when to combine human and AI capabilities. Existing meta-analyses can help reconcile these findings, but they require substantial manual effort and cannot readily incorporate new evidence as it emerges. To address this challenge, we introduce AutoAnalysis: an automated, self-updating meta-analysis of when humans and AI work better together, and when they work better alone. AutoAnalysis' most recent run synthesizes 1,955 effect sizes from 420 papers. Across this body of work, we found that, on average, human-AI combinations performed significantly better than humans alone, but they performed significantly worse than the better of humans or AI alone. These findings highlight the important distinction between improving human performance and achieving human-AI synergy and underscore the need to evaluate collaboration against both human and AI performance alone. As new studies emerge, AutoAnalysis will integrate their findings into the meta-analysis, providing cumulative evidence about when humans and AI perform better together and how human-AI performance varies across AI agents, tasks, and processes.

</details>

---

### 3. SimXAI: A Simple Drop-in Layer Increases Interaction Quality and Understanding in Conversational XAI
- **Authors**: Van Bach Nguyen, Qianli Wang, Nils Feldhus et al. (5 authors)
- **Date**: 2026-10-30 | **Links**: [Abstract](https://arxiv.org/abs/2610.41856v1) | [PDF](https://arxiv.org/pdf/2610.41856v1)
- **Status**: [ ] Unread  |  [ ] Dissected for Social Post

<details>
<summary><b>📖 Abstract / Summary (click to expand)</b></summary>

Conversational explainable AI (ConvXAI) agents often use GUS-style architectures with separate modules for intent recognition, dialogue management, and template-based response generation. While faithful to the underlying XAI methods, these pipelines are hard to adapt and often struggle with context-dependent follow-up questions. We present SimXAI, a lightweight LLM-centric conversational layer that replaces these modules with a single tool-calling LLM that bridges access to existing XAI resources. Rather than a standalone agent, SimXAI serves as a modular interface that enables conversational access to external XAI resources. We further introduce an evaluation suite for single- and multi-turn parsing, faithfulness, and contextualization. Across existing and new datasets, SimXAI achieves strong function-selection accuracy and high faithfulness while better handling context-dependent requests. In a user study replacing only the conversational layer of TalkToModel, a representative GUS-based agent, users completed tasks more accurately and in fewer turn. Overall, SimXAI improves GUS-based design while preserving faithfulness and improving conversational quality.

</details>

---

### 4. MERIDIAN: Memory-Encoded Rituals for Intimacy across Distance in an Interactive, Asynchronous Neighbourhood
- **Authors**: Jingyi Chen, Yifan Yang
- **Date**: 2026-10-30 | **Links**: [Abstract](https://arxiv.org/abs/2610.41776v1) | [PDF](https://arxiv.org/pdf/2610.41776v1)
- **Status**: [ ] Unread  |  [ ] Dissected for Social Post

<details>
<summary><b>📖 Abstract / Summary (click to expand)</b></summary>

How can shared memories become playable structures for partners who live in different time zones? We present MERIDIAN, a pre-deployment design case of Yi Town, a bilingual browser game developed by one member of a long-distance couple as a gift for the other. Nine levels translate personally meaningful events, places and cultural references into tasks within a navigable pixel town. A birthday prologue and a fictional wedding frame the intended experience. Drawing on research through design, we reconstruct four design changes from 109 development commits, 28 changelog versions and three design specifications. These records support six situated design commitments, including memory-derived mechanics, staged access, local progress storage and bilingual coverage. The implementation combines a union-based progress model with manually exchanged, checksummed codes and time-zone-dependent scenery. An implementation audit reproduced 153 passing unit tests and examined all 1,024 canonical progress codes, while identifying limits involving resets, unversioned level registries and residual transcription errors. The application has no author-operated backend for progress, but external media services and browser speech recognition limit its privacy and offline guarantees. No recipient evaluation or relationship outcomes are reported. The contribution is an inspectable account of design decisions and their trade-offs, including the tension between authoring a personal gift and preserving the recipient's freedom to interpret, decline or reshape it. The game is playable at https://jingyifan.love and its source is public at https://github.com/rayford295/yi-town.

</details>

---

### 5. When Architectural Spaces Start to Act
- **Authors**: Alex Binh Vinh Duc Nguyen
- **Date**: 2026-10-30 | **Links**: [Abstract](https://arxiv.org/abs/2610.41724v1) | [PDF](https://arxiv.org/pdf/2610.41724v1)
- **Status**: [ ] Unread  |  [ ] Dissected for Social Post

<details>
<summary><b>📖 Abstract / Summary (click to expand)</b></summary>

Architectural spaces are increasingly gaining robotic capabilities. Architectural robots such as robotic partitions, ceilings, furniture, facades, and other spatial components can autonomously move and reconfigure in response to occupants' needs and activities. Yet, when architectural robots start shaping the spatial conditions in which people continuously live, work, and interact, we may begin to experience the architectural space itself as robotic. What does this shift mean for how we inhabit such spaces? Drawing on our previous studies, I reflect on how architectural robots interact with people not only through their motions, but also through the spatial configurations that persist after those motions stop; how their actions may benefit some occupants while disadvantaging others; and how multiple robots may together make a whole architectural space appear to act. I argue that as computation gains the capacity to physically reconfigure our environments, interaction extends beyond the moment of computational action into the spatial conditions that people continue to inhabit. Understanding robotic architecture therefore requires us to look beyond short-term human-robot interaction and toward how people inhabit, negotiate, and maintain control over spaces that can autonomously reconfigure.

</details>

---

### 6. Designing wearable haptic cueing for neurological gait rehabilitation: user requirements across residential care and community settings
- **Authors**: Riasat Islam, Annemarie Zijlema, Theodoros Georgiou et al. (8 authors)
- **Date**: 2026-10-30 | **Links**: [Abstract](https://arxiv.org/abs/2610.41680v1) | [PDF](https://arxiv.org/pdf/2610.41680v1)
- **Status**: [ ] Unread  |  [ ] Dissected for Social Post

<details>
<summary><b>📖 Abstract / Summary (click to expand)</b></summary>

Wearable haptic cueing offers rhythmic prompts for neurological gait rehabilitation while leaving hearing available for communication and environmental awareness. We investigated the user, design, and implementation requirements needed to make these systems usable in practice. We analysed six linked studies involving 17 people with neurological conditions affecting gait and three physiotherapists across formative sessions, residential care, and community self-management. Wearable devices served as technology probes. Observations, interviews, diaries, physiotherapist records, gait analysis, and activity logs informed thematic analysis and cross-study comparison. Seven recurring requirement areas concerned haptic perceptibility and placement, wearability and fastening, interaction burden, rhythm personalisation, real-world walking contexts, supported use, and perceived value beyond gait outcomes. Requirements interacted: perceptible cue locations could be difficult to access for fastening or control, while fixed rhythms did not always accommodate terrain, fatigue, interruptions, or changing pace. Carers and clinicians supported configuration, operation, safety, and interpretation. Participants described confidence, routine formation, and willingness to walk; these accounts were interpreted as perceived value rather than evidence of therapeutic efficacy. Low sensation, cognitive burden, and mobility limitations could make wearable cueing impractical. Future systems should offer adjustable haptic output, flexible placement, accessible fastening, simple controls, personalised rhythms, and robustness during everyday walking. Design should accommodate support from carers and clinicians and consider trade-offs between requirements. These findings inform wearable rehabilitation design rather than establish clinical efficacy.

</details>

---

### 7. Look Over There! Dynamic Visual Guidance for AI-Narrated Slides
- **Authors**: Jiongning Allen Lian, Yutong Alison Mei, Ho Ting Cheung et al. (10 authors)
- **Date**: 2026-10-30 | **Links**: [Abstract](https://arxiv.org/abs/2610.41645v1) | [PDF](https://arxiv.org/pdf/2610.41645v1)
- **Status**: [ ] Unread  |  [ ] Dissected for Social Post

<details>
<summary><b>📖 Abstract / Summary (click to expand)</b></summary>

Slides present information spatially, but narration unfolds linearly, leaving the viewer struggling to locate what the narration refers to. This split attention between audio and visual channels forces viewers to search the slide manually, imposing extraneous cognitive load and disrupting comprehension. The problem is especially acute on mobile devices, where dense layouts compressed onto small screens make visual search particularly effortful. In teacher-led settings, however, instructors naturally direct attention through pointing, pacing, and emphasis. Inspired by this, we present GuideSlide, a system that automatically generates Dynamic Visual Guidance for slide presentations, providing viewers with narration-synchronized visual cues that direct attention in real time. Given a PDF slide deck, GuideSlide automatically produces region-level zoom and time-aligned highlights without manual annotation. In a within-subjects study with 24 participants, GuideSlide substantially reduced perceived cognitive load and yielded higher immediate comprehension scores compared to static slides with identical narration. Participants strongly preferred the Dynamic Visual Guidance condition, reporting that it made narration easier to follow and reduced uncertainty about where to look. These findings suggest that narration-synchronized visual guidance is a valuable design strategy for slide-based presentations, with potential to extend to other instructional and presentation scenarios.

</details>

---

### 8. Altered Visual Hand Feedback in Virtual Reality: An Exploratory Study in Essential Tremor
- **Authors**: Alejandro Pascual-Valdunciel, Marcos Sacristán-Moraleda, Verónica Giménez de Béjar et al. (7 authors)
- **Date**: 2026-10-30 | **Links**: [Abstract](https://arxiv.org/abs/2610.41496v1) | [PDF](https://arxiv.org/pdf/2610.41496v1)
- **Status**: [ ] Unread  |  [ ] Dissected for Social Post

<details>
<summary><b>📖 Abstract / Summary (click to expand)</b></summary>

Pathological tremor is the most prevalent movement disorder worldwide, characterized by involuntary muscular oscillations within a frequency of 3 to 12 Hz. Despite extensive research, the underlying mechanisms that generate and modulate tremor are not yet understood, and treatments are usually insufficient. While it is known that visual feedback is an important afferent pathway, little is known about the impact of altering the hand's visual representation on tremor expression. With the development of immersive technologies, VR poses an excellent tool to study how alterations to the representation of the hands affect tremor. In this work, we study this through two complementary experiments. In the first one, we show that a consumer-level hand-tracking system substantially attenuates tremor-band movements without preventing successful task completion. In the second one, with eight patients with essential tremor, we observe task-dependent differences in physical tremor between VR and the real world, with several patients exhibiting lower tremor-band activity in both hand kinematics and muscle oscillations, particularly during reaching tasks. Our findings represent an initial step toward validating the use of VR as an experimental tool for the research and treatment of pathological tremor, while highlighting strong user- and task-dependent effects.

</details>

---
