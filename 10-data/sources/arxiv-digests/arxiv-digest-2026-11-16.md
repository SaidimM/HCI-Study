---
date: 2026-11-16
type: arxiv-digest
category: cs.HC
tags: [hci, arxiv, reading-queue]
---

# 📡 arXiv cs.HC Digest — 2026-11-16

> Automated intake of the latest Human-Computer Interaction preprints.
> Pick 1–2 papers that look promising to dissect using [[90-templates/paper-note|Paper Note Template]].

---

### 1. Between Obligations and Evidence: A Participatory Study of Translating the EU AI Act into Technical Requirements
- **Authors**: Helma Torkamaan, Masoud Mansoury, Yanan Xin et al. (12 authors)
- **Date**: 2026-11-13 | **Links**: [Abstract](https://arxiv.org/abs/2611.18439v1) | [PDF](https://arxiv.org/pdf/2611.18439v1)
- **Status**: [ ] Unread  |  [ ] Dissected for Social Post

<details>
<summary><b>📖 Abstract / Summary (click to expand)</b></summary>

The EU AI Act imposes technical and organizational requirements for high-risk AI systems, but applying these requirements involves contextual choices about what to measure and what evidence supports a compliance claim. We investigate these challenges through a participatory workshop involving 32 researchers, policymakers, and practitioners from different disciplines, using realistic scenarios in healthcare, recruitment, and public transport to examine how regulatory obligations are interpreted, translated into technical requirements, and evaluated in practice. Through a thematic analysis of workshop data, we identify recurring tensions between how regulatory obligations are translated into measurable system properties, how responsibility and human oversight are exercised in practice, and how the validity of compliance evidence is affected by changing operational conditions and system uses. For example, participants highlighted how fairness metrics could conceal discrimination in recruitment, how time pressure and limited information could undermine human oversight in public transport, and how changes in patient populations could invalidate previously established evidence of system performance. Our findings suggest that technical, organizational, and evidentiary challenges are interdependent, and that establishing and maintaining compliance requires attention not only to technical assessments but also to how AI systems are used, governed, and monitored over time. We discuss implications for supporting context-sensitive and ongoing compliance.

</details>

---

### 2. Toward On-Device Markerless 6DoF Tracking of a Physical Manipulative on a Mixed-Reality Headset: A Preliminary Study
- **Authors**: Guangxi Feng, Philip Yasskin, Wei Yan
- **Date**: 2026-11-13 | **Links**: [Abstract](https://arxiv.org/abs/2611.18438v1) | [PDF](https://arxiv.org/pdf/2611.18438v1)
- **Status**: [ ] Unread  |  [ ] Dissected for Social Post

<details>
<summary><b>📖 Abstract / Summary (click to expand)</b></summary>

AR-Classroom uses physical models and virtual overlays to help learners explore spatial transformations. To align these overlays on a standalone headset, we developed a markerless six-degree-of-freedom(6DoF) tracker for a LEGO airplane on the Meta Quest 3. A compact YOLO model trained on synthetic Unity renders predicts 20 keypoints from dynamic RGB crops resized to 128 by 128 pixels. A perspective-n-point solver estimates the airplane's pose from these predictions and the corresponding 3D landmarks. In a paired evaluation on 1,000 synthetic validation images, cropping guided by ground-truth boxes increased the detection rate on annotated images from 32.5 to 46.2 percent. Mean keypoint F1 increased from 42.9 to 44.6 percent, with lower keypoint precision in the cropped view. In preliminary headset tests, 2 Hz was the highest tested tracking target at which the application maintained approximately 72 frames per second. A headset demonstration illustrates virtual overlay alignment with the physical airplane before and after a manual rotation. Quantitative 6DoF pose accuracy on real headset footage will be measured in future work.

</details>

---

### 3. Voice-Based Conversational Agents as AI Care Assistants: Evaluating Personalization, Intervention Delivery Fidelity, and Privacy Expectations in Older Adults' Care
- **Authors**: Thalia Viranda, Shupeng Wang, Jia Bo et al. (11 authors)
- **Date**: 2026-11-13 | **Links**: [Abstract](https://arxiv.org/abs/2611.18385v1) | [PDF](https://arxiv.org/pdf/2611.18385v1)
- **Status**: [ ] Unread  |  [ ] Dissected for Social Post

<details>
<summary><b>📖 Abstract / Summary (click to expand)</b></summary>

Generative AI enables voice-based conversational agents to play more active roles in older adults' care, including personalizing support and operating alongside clinicians and care partners. This shift creates two challenges: how to personalize support while faithfully delivering evidence-based interventions, and how to manage personal-data use and sharing across AI and care stakeholders. We designed and evaluated ARC, a voice-based conversational agent that operationalizes multidomain lifestyle intervention through sessions with predefined goals, participant context, and evidence-based components. In a 3-day remote study, 80 older adults completed 473 sessions across six session types (9,183 turns; averaging 19.4 turns and 6 minutes per session). Participants reported favorable usability, acceptability, and use intentions. System-level analyses showed strong domain-level but modest participant-specific contextual reuse, no significant personalization-fidelity association, and fidelity limitations centered on incomplete delivery of intervention components rather than off-protocol drift. Within care relationships, expectations for personal-data use and sharing varied by data type and recipient. Our findings support feasibility of conversational delivery of multidomain lifestyle intervention, offer methods and system-design insights for longitudinal evaluation, and motivate an evaluation agenda for generative AI health interventions: user-experience and outcome measures should be complemented by evidence of whether intended intervention processes were delivered as designed.

</details>

---

### 4. Clean Tickets, Wrong Orders: Catching Silent Errors with a Language Model in Your Browser Tab
- **Authors**: Umar Ahmed, Maxim Dunaev, Mohammad Nour Al Awad et al. (5 authors)
- **Date**: 2026-11-13 | **Links**: [Abstract](https://arxiv.org/abs/2611.18284v1) | [PDF](https://arxiv.org/pdf/2611.18284v1)
- **Status**: [ ] Unread  |  [ ] Dissected for Social Post

<details>
<summary><b>📖 Abstract / Summary (click to expand)</b></summary>

A small language model that turns a typed order into structure can fail in two ways. It can print something broken, which any system rejects. Or it can print a clean, well formed order that nobody placed. Our companion work calls the second kind a silent error, and it is the dangerous one. We present a web demo in which a fine-tuned 0.8B parameter model runs entirely inside the visitor's browser tab, through llama.cpp compiled to WebAssembly. No order text leaves the device. The page parses orders as the visitor types, scores every ticket with the PIZZA benchmark's own matcher ported to TypeScript, refuses anything off the menu with "?" so the model can face the open web, and lets visitors hunt for silent errors or try to cause one. Run in the browser on all 1,357 PIZZA test orders, the deployed model writes the same output as the server evaluation for 99.0% of them and reaches the same exact match (0.882); we also report its latency on 3 consumer laptops. Demo: https://wrong.cuyor.com

</details>

---

### 5. Personalization of Basic and Moral Values Guiding LLM-Controlled Assistant Robots
- **Authors**: Mateusz Wozniak, Qi Gao, Agnieszka Wykowska
- **Date**: 2026-11-13 | **Links**: [Abstract](https://arxiv.org/abs/2611.18230v1) | [PDF](https://arxiv.org/pdf/2611.18230v1)
- **Status**: [ ] Unread  |  [ ] Dissected for Social Post

<details>
<summary><b>📖 Abstract / Summary (click to expand)</b></summary>

Personal assistant robots powered by large language models (LLMs) are likely to enter everyday life within the next decade, but the values that should guide their behaviour remain largely unspecified. Current alignment practice steers a single model toward an aggregate of human values, ignoring that individual users may prefer a robot whose value profile differs from their own. We administer parallel self- and robot-targeted versions of three established psycho-metric instruments - the simplified Schwartz Values Survey (SVS), the Portrait Values Questionnaire (PVQ-21), and the Moral Foundations Questionnaire (MFQ) - to potential future users (N=22), capturing both their personal values and the values they would want an assistant robot to embody. We compare the three instruments as personalization tools using the UEQ-S and benchmark fifteen contemporary LLMs against the resulting profiles. Participants wanted their robot to score markedly lower than themselves on personal-focus values and higher on social-focus values; moral profiles were nearly identical. LLMs prompted to act as robots shifted only weakly toward the desired profile, indicating that default model behaviour and prompt engineering are no substitute for explicit value personalization.

</details>

---

### 6. What a Memory Preview Cannot Tell You: Ambiguity in AI Memory Permissions
- **Authors**: Sadia Noman Tonni, Nafis Fuad Shahid
- **Date**: 2026-11-13 | **Links**: [Abstract](https://arxiv.org/abs/2611.17874v1) | [PDF](https://arxiv.org/pdf/2611.17874v1)
- **Status**: [ ] Unread  |  [ ] Dissected for Social Post

<details>
<summary><b>📖 Abstract / Summary (click to expand)</b></summary>

A memory rule states when an assistant may reuse a remembered event, and an editor can confirm a rule by previewing one use it allows and one it blocks. We ask what such a preview lets a person infer about the rule they saved. For an editor with six or twelve valid rules, we enumerate every rule compatible with a preview. Splitting the rules most evenly does not target the question a user cares about. For an explicit preference, two adaptive tests leave all three recommendation scopes open (for a one-off choice the outcome turns on a tie), while one test of transfer to another task settles the question. Weak previews are also the default. Under the intended rule, 36 of 39 possible allowed/blocked pairs contain a blocked example that no rule allows, and no pair identifies the rule. Three or four tests suffice here; when permissions depend on each other, a fixed checklist grows to six or nine and adaptive questioning needs at most five or seven. These counts use a specified rule vocabulary and fictional events. In a small pilot, 10 of 20 people who saw such a weak preview of a rule they had just chosen mispredicted, or were unsure about, at least one of two uses, and none of those 10 said the outcomes matched what they wanted. Whether better previews help people is untested.

</details>

---

### 7. DECODE: Diagnosing Interpretability Failures in Automated Interpretation Process
- **Authors**: Dohyun Kim, Jaeung Lee, Donghee Hong et al. (4 authors)
- **Date**: 2026-11-13 | **Links**: [Abstract](https://arxiv.org/abs/2611.17856v1) | [PDF](https://arxiv.org/pdf/2611.17856v1)
- **Status**: [ ] Unread  |  [ ] Dissected for Social Post

<details>
<summary><b>📖 Abstract / Summary (click to expand)</b></summary>

Tools for interpreting the internal representations of Large Language Models (LLMs) increasingly rely on LLMs themselves to both generate and evaluate explanations, creating a self-referential automated interpretation process with minimal human oversight. This automation raises significant reliability concerns, which are exacerbated by the absence of ground truth. In practice, it is difficult to validate explanations or to attribute interpretability failures to their source -- whether they originate from the tool's extracted representations or from the LLM used in the process. To address these challenges, we present DECODE, a visual analytics system that reintroduces human oversight into the automated interpretation process. Our approach decomposes the diagnostic workflow into three progressive stages, isolating failure sources ranging from structural defects to explanation-level misalignments. Drawing inspiration from inter-coder consensus in qualitative analysis, we utilize consensus among independently generated explanations and their evaluation metrics as a proxy for reliability. To further scale human inspection, we employ a three-phase active seeding protocol that strategically recommends high-priority instances for manual review. Finally, we demonstrate the effectiveness of our approach through a case study on 16,384 Sparse Autoencoder features, showing that it can efficiently identify and attribute interpretability failures at scale.

</details>

---

### 8. Alleviating Interview Stress: Effects of Robot Persona and Reactive Backchanneling on High-Pressure Mock Interviews
- **Authors**: Haochen Yang, Zhuoran Gao, Geqing Tao et al. (5 authors)
- **Date**: 2026-11-13 | **Links**: [Abstract](https://arxiv.org/abs/2611.17830v1) | [PDF](https://arxiv.org/pdf/2611.17830v1)
- **Status**: [ ] Unread  |  [ ] Dissected for Social Post

<details>
<summary><b>📖 Abstract / Summary (click to expand)</b></summary>

High-pressure job interviews induce anxiety and impair performance. Existing mock training suffers from a trade-off among cost, standardization, and physical presence. This study investigated how a robot interviewer's verbal persona (supportive vs. challenging) and nonverbal backchanneling (active vs. negative) affect users' psychological states and facial expressions in a simulated interview. In a 2x2 between-subjects experiment (N=28), participants interacted with a NAO robot. Subjective measures (state anxiety, self-efficacy, social presence) and objective facial emotion recognition were collected. Results showed that a supportive persona reduced task load, increased perceived robot warmth and mind perception, and decreased perceived surveillance and robot discomfort. Active backchanneling increased non-neutral (p = .021) and anxiety-tension facial affect (p = .048). A significant interaction effect between persona and backchanneling was found on social presence (p = .045). The subjective-objective consistency was 67.9%, indicating complementary measurement modalities. The findings provide preliminary support for the social buffering hypothesis in human-robot interaction.

</details>

---
