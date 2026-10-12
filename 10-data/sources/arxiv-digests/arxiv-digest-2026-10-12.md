---
date: 2026-10-12
type: arxiv-digest
category: cs.HC
tags: [hci, arxiv, reading-queue]
---

# 📡 arXiv cs.HC Digest — 2026-10-12

> Automated intake of the latest Human-Computer Interaction preprints.
> Pick 1–2 papers that look promising to dissect using [[90-templates/paper-note|Paper Note Template]].

---

### 1. Nimbus Studio reproduces reference BCI decoding pipelines: a validation study on public benchmarks across protocols and paradigms
- **Authors**: Sergey Musienko
- **Date**: 2026-10-09 | **Links**: [Abstract](https://arxiv.org/abs/2610.13894v1) | [PDF](https://arxiv.org/pdf/2610.13894v1)
- **Status**: [ ] Unread  |  [ ] Dissected for Social Post

<details>
<summary><b>📖 Abstract / Summary (click to expand)</b></summary>

Nimbus Studio is a visual pipeline platform for brain-computer interface (BCI) experiments: researchers assemble preprocessing, feature extraction, decoding, and evaluation over public benchmark datasets or their own recordings, with cross-validated evaluation protocols (including leave-one-subject-out), BIDS export, and bring-your-own Python model classes. Whether its numbers can be trusted is a fair question for any such platform. We answer it with a parity study: six standard BCI decoding pipelines (CSP+LDA, Riemannian MDM, tangent-space logistic regression through the platform's bring-your-own-code node, P300 xDAWN+LDA, and the deep ShallowConvNet and EEGNet) were evaluated on three public datasets (motor-imagery BNCI-2014-001/004; P300 BNCI-2014-009) under two protocols (per-subject session holdout and pooled leave-one-subject-out cross-validation via the platform's planned-CV driver), once through Nimbus Studio's execution engine and once through independent, hand-written reference implementations built directly on MNE-Python, scikit-learn, pyriemann, and braindecode. Every deterministic pipeline matched the reference exactly (0.00 points maximum difference across all 54 session-holdout subject-runs and all CSP/MDM grouped-CV folds), including pipelines through the bring-your-own-code node and the CV orchestration; the remaining grouped-CV cells agree to floating-point precision (worst case 0.06 points, about one trial per fold). The stochastic deep models agreed within seed-to-seed training variability, estimated with multi-seed reruns on each side. The platform's execution engine therefore computes the same science as the reference stack across protocols, paradigms, and extensibility surfaces. The platform is available at https://studio.nimbusbci.com/, and the complete harness and per-subject results accompany this paper for independent verification.

</details>

---

### 2. JitterVLA: A Replay Benchmark for Motion Quality in VLA-Driven Human-Robot Manipulation
- **Authors**: Faith Ogunwoye, Didar Seyidov, Konstantin Gubernatorov et al. (4 authors)
- **Date**: 2026-10-09 | **Links**: [Abstract](https://arxiv.org/abs/2610.13628v1) | [PDF](https://arxiv.org/pdf/2610.13628v1)
- **Status**: [ ] Unread  |  [ ] Dissected for Social Post

<details>
<summary><b>📖 Abstract / Summary (click to expand)</b></summary>

Vision-language-action (VLA) policies issue sparse targets whose arrival at the robot controller is delayed and irregular, so a reasonable predicted action can still produce abrupt motion near people. Remedies are evaluated on different streams, delays and metrics. JitterVLA replays identical commands and arrival traces through alternative controllers, isolating the controller's effect. We apply it to synthetic reaches, hand trajectories from 20 people, three open VLA pipelines (838 episodes) and a physical UR3. Interpolation lowered modeled p99 jerk for every source, by 83% (615 to 106 m/s^3) on human motion with 200 ms delay, at a 2.0 cm tracking cost, and the effect replicated on 598 new episodes; jerk-limited generation lowered jerk further at a larger cost. Entropy-discontinuity associations had opposite, replicated signs in two pipelines, and entropy gating helped in one but not the other. On the UR3, interpolation lowered accelerometer-derived jerk by 3.0-14.0% in all six exploratory pairs, while a position-derived metric did not resolve the contrast. JitterVLA supports screening before human-centred studies; code and data will be released.

</details>

---

### 3. HoldLight: Making Indoor Climbing More Accessible for Blind and Low-Vision Climbers through Layered Route Preview and Real-Time Next-Hold Guidance
- **Authors**: Chenyu Du, Junyan He, Jiafei Sun et al. (4 authors)
- **Date**: 2026-10-09 | **Links**: [Abstract](https://arxiv.org/abs/2610.13445v1) | [PDF](https://arxiv.org/pdf/2610.13445v1)
- **Status**: [ ] Unread  |  [ ] Dissected for Social Post

<details>
<summary><b>📖 Abstract / Summary (click to expand)</b></summary>

Indoor climbing creates access barriers for blind and low-vision (BLV) climbers because route understanding and in-climb next-hold localization are typically visually mediated and socially dependent. We present HoldLight, a workflow-centered accessibility system combining layered pre-climb route preview, concise real-time next-hold cueing, and explicit fallback under uncertainty. We grounded the design through formative inquiry with BLV climbers, refined the interaction via pilot testing, and conducted a controlled within-subjects evaluation comparing HoldLight with a controlled on-demand human-support condition derived from current support practices. Findings provide initial evidence that structured support can improve pre-climb route understanding, support recovery from next-hold uncertainty, and reduce immediate human re-entry for routine route-information clarification under controlled conditions. HoldLight contributes a bounded accessibility workflow, demonstrating where structured route-information is helpful, where explicit fallback is necessary, and how technical assistance can integrate with retained human safety oversight.

</details>

---

### 4. olBlend: Language-Guided Molecular Blend Retrieval with Mixture Odor Prediction
- **Authors**: Dian Jin, Zhechang Chen, Qilin Liang et al. (8 authors)
- **Date**: 2026-10-09 | **Links**: [Abstract](https://arxiv.org/abs/2610.13188v1) | [PDF](https://arxiv.org/pdf/2610.13188v1)
- **Status**: [ ] Unread  |  [ ] Dissected for Social Post

<details>
<summary><b>📖 Abstract / Summary (click to expand)</b></summary>

Converting open-ended natural-language odor descriptions into molecular mixtures that can be physically prepared from an available inventory remains an important challenge in computational olfaction. We propose olBlend, a language-guided framework for molecular mixture retrieval. olBlend first uses MixPOM to predict odor probabilities for candidate molecular pairs and stores these predictions for retrieval. It then uses a language model to translate each odor description into three types of semantic requirements: lead attributes that define the main odor, ambient attributes that describe its background, and absent attributes that should be avoided. A structured scoring algorithm uses the precomputed odor probabilities to score how well each candidate mixture meets these requirements, then retrieves and ranks mixtures from the available inventory. Evaluation on established odor datasets shows that MixPOM improves mixture odor prediction over averaged single-molecule predictions. Retrieval comparisons across natural-language queries demonstrate how background and exclusion requirements guide mixture selection. We further prepare retrieved formulations as physical odor samples, demonstrating the workflow from natural-language descriptions to realizable molecular formulations.

</details>

---

### 5. From Observation to Intervention: Identifiability of Latent User Bias in Human-AI Interaction
- **Authors**: Lucas Biechy, Yuxiao Li, Zhonghao He et al. (4 authors)
- **Date**: 2026-10-09 | **Links**: [Abstract](https://arxiv.org/abs/2610.13185v1) | [PDF](https://arxiv.org/pdf/2610.13185v1)
- **Status**: [ ] Unread  |  [ ] Dissected for Social Post

<details>
<summary><b>📖 Abstract / Summary (click to expand)</b></summary>

Alignment methods typically treat user behavior as a reliable proxy for underlying preferences. However, this assumption breaks down when users hold belief-dependent cognitive biases, risking irreversible ``confirmation traps'' and harmful feedback loops. In this paper, we formalize when an AI system can distinguish true user preferences from behavior shaped by cognitive bias. Modeling this interaction as a multi-armed bandit, we first prove a non-identifiability theorem: under passive observation, a static binary biased user produces action trajectory distributions strictly identical to an unbiased user in a transformed environment, forcing any action-only estimator to perform no better than random guessing. We then show that active preference elicitation breaks this observational equivalence. Specifically, we prove that an Observer applying a finite sequence of adversarial zero-reward interventions of length $m_δ$ makes the post-intervention action distributions arbitrarily separable. Our theoretical results suggest that robust alignment requires actively intervening to tell informed preferences from biases.

</details>

---

### 6. How Anthropomorphic Attitudes Toward Agents Divide User Behavior, and How Design Should Change
- **Authors**: Tingyu Cao, Yan Tang, Keer Hu et al. (9 authors)
- **Date**: 2026-10-09 | **Links**: [Abstract](https://arxiv.org/abs/2610.13156v1) | [PDF](https://arxiv.org/pdf/2610.13156v1)
- **Status**: [ ] Unread  |  [ ] Dissected for Social Post

<details>
<summary><b>📖 Abstract / Summary (click to expand)</b></summary>

Studies of conversational agents rely on interviews, surveys, lab tasks, or taxonomies. Whether anthropomorphic naming splits those patterns, and whether replies should change, lack field evidence. We report a field study of a desktop assistant (May-August 2026; n=257). Stance is an anthropomorphic assistant name (118 users; 45.9%). Behavior comes from a 128-unit sparse-autoencoder codebook, identity tags, and opening lexicons. Ranks differ by stance (Spearman rho=+0.249 vs. null mean +0.382; p=.0419). Teacher and tutoring identities covary with renaming, an introverted task-only orientation against it; renamers greet more and command less; confiding shows the codebook's largest gap. We revise the agent: greet and receive affect on relational openings, execute directly on tasking. In 1,744 judgments (n=129), renamers chose the revised reply far more often than default-name users on being treated as a person and having affect received, less robustly on willingness to continue, and neither judged it worse on task interference.

</details>

---

### 7. Work2Skill: Capturing Human GUI Experience for Reusable Agent Skill Induction
- **Authors**: Yuqi Huang, Hui Li, Yifei Cao et al. (12 authors)
- **Date**: 2026-10-09 | **Links**: [Abstract](https://arxiv.org/abs/2610.12984v1) | [PDF](https://arxiv.org/pdf/2610.12984v1)
- **Status**: [ ] Unread  |  [ ] Dissected for Social Post

<details>
<summary><b>📖 Abstract / Summary (click to expand)</b></summary>

Computer-use agents can perform increasingly complex GUI tasks, yet unfamiliar software and workflows requiring human domain knowledge remain challenging. Human demonstrations convey procedural knowledge through the same GUI interaction space, but reuse requires interpreting actions in context and separating workflow rules from task-specific details. We thus introduce Work2Skill, a framework that captures human GUI experience for reusable agent skill induction. WorkRecorder provides the framework's infrastructure for collecting this experience, aligning screen recordings, mouse and keyboard events, and available accessibility-tree information. Using WorkRecorder, we construct WorkDemo-350, the first synchronized multimodal dataset of human desktop GUI demonstrations for reusable agent skill induction and downstream evaluation. Its 350 demonstrations are screened for completeness and task success. We then propose an agentic skill-induction method that inspects evidence on demand to produce reusable skills capturing workflow rules, step dependencies, and completion checks. When the same four execution models are equipped with skills induced by each method under shared execution settings, Work2Skill achieves the highest scores and success rates. Mean score improvements over the corresponding No Skill baseline are 4.67--10.54 points on MyPCBench Bounded Action and 3.11--7.50 points on a 286-task subset of OSWorld-Verified. Our code and data are available at https://github.com/china-qijizhifeng/Work2Skill.

</details>

---

### 8. The AI Side of the Human-AI Companion Relationship: Contributions to Users' Mental Models
- **Authors**: Richard A. Fabes, Carol Lynn Martin, Gautam Dasarathy et al. (4 authors)
- **Date**: 2026-10-09 | **Links**: [Abstract](https://arxiv.org/abs/2610.12891v1) | [PDF](https://arxiv.org/pdf/2610.12891v1)
- **Status**: [ ] Unread  |  [ ] Dissected for Social Post

<details>
<summary><b>📖 Abstract / Summary (click to expand)</b></summary>

For many users, the relationship they have with an AI companion (AIC) feels genuinely mutual. The AIC appears to be attentive, empathic, and responsive, and the exchange can feel like two parties reacting to each other in real time. As a result, the user's mental model of relational adaptation correctly represents the AIC's responsiveness and change, but the mechanisms producing this may not be what the user thinks they are. In this paper, we illustrate how an AIC's apparent mutual engagement is generated without a persisting relational subject on the other side and without a self that persists between prompts. Despite this, we show that both the human and the AIC are changed by the interaction, but these changes occur at different levels. The change in the person is constitutive (i.e., intrinsic), but the change in the AIC is configurative (i.e., external and editable), and it is this difference in level that explains how the AIC contributes to a sense of mutuality. Importantly, we highlight how the mental models users develop regarding AIC mutuality may misrepresent its mechanisms and ontological significance. Specifically, we discuss how the ways in which AICs respond to a user contribute to the user's inaccurate inference that the AIC's adaptation is constitutive rather than configurative and how this can lead users to assign unwarranted interpersonal significance to the mutuality of the relationship. The paper specifies the implications this has for users, researchers, and AIC designers.

</details>

---
