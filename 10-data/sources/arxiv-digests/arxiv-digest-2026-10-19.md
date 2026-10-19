---
date: 2026-10-19
type: arxiv-digest
category: cs.HC
tags: [hci, arxiv, reading-queue]
---

# 📡 arXiv cs.HC Digest — 2026-10-19

> Automated intake of the latest Human-Computer Interaction preprints.
> Pick 1–2 papers that look promising to dissect using [[90-templates/paper-note|Paper Note Template]].

---

### 1. Bad Diagnosis: Analyzing Consent and Data Collection Practices of Mobile Medical Apps
- **Authors**: Ethan Myers, Lorenzo De Carli, Shantanu Sharma et al. (6 authors)
- **Date**: 2026-10-16 | **Links**: [Abstract](https://arxiv.org/abs/2610.23851v1) | [PDF](https://arxiv.org/pdf/2610.23851v1)
- **Status**: [ ] Unread  |  [ ] Dissected for Social Post

<details>
<summary><b>📖 Abstract / Summary (click to expand)</b></summary>

Mobile health (mHealth) apps collect personally-identifiable information while handling uniquely sensitive medical data, ranging from mental health records to real-time glucose or heart rate monitoring -- yet they remain poorly understood at scale. We present the first comprehensive analysis of consent and data collection practices across 10,000+ mHealth apps on the Google Play Store, combining static analysis and privacy policy examination. We develop a rigorous operational definition to distinguish health apps from general wellness programs, and design a measurement framework to detect misuse of permissions and violations of consent. Our analyses reveal a troubling ecosystem: 69.15% of apps request at least one permission unrelated to their stated purpose, with over 52.9% apps requesting location data, and 50.5% and 34.9% apps requesting camera and microphone access, respectively -- despite no functional justification based on app descriptions and stated purposes. Most alarmingly, nearly 93% of apps fail to provide users with a consent form, directly violating regulatory requirements such as GDPR; and even among the remaining 7%, 1 in 14 demonstrate a gap between the obtained consent and collection of personally identifiable information. These findings demonstrate an urgent need for stronger enforcement of privacy regulations in mHealth apps. We plan to release our dataset and measurement tools for continued monitoring of this critical space.

</details>

---

### 2. Sensory Comfort Across Multisensory XR Prototypes for Autistic Adults
- **Authors**: Yibo Meng, Xiujun Chen, Bingyi Liu et al. (4 authors)
- **Date**: 2026-10-16 | **Links**: [Abstract](https://arxiv.org/abs/2610.23833v1) | [PDF](https://arxiv.org/pdf/2610.23833v1)
- **Status**: [ ] Unread  |  [ ] Dissected for Social Post

<details>
<summary><b>📖 Abstract / Summary (click to expand)</b></summary>

Multisensory XR may support informal learning for autistic adults, but sensory-friendly design often emphasizes reducing input. We conducted a mixed-methods, counterbalanced within-subjects study with 20 Chinese autistic adults who evaluated five complete XR configurations presenting the same popular-science content. Comfort differed substantially across the configurations (Friedman chi-square(4) = 46.39, p < .001, Kendall's W = .58). L3 received the lowest mean rating (2.97/5) and was tied for lowest for 16/20 participants, whereas L5 received the highest mean rating (4.43/5) and was tied for highest for 17/20. Participants described the static configurations in terms of clarity and self-pacing, L3 in terms of abruptness, simultaneous demands, insufficient warning, and limited disengagement, and L4/L5 in terms of gradual transitions, opportunities to disengage, and coordinated narrative cues. The study provides a configuration-level account of sensory comfort and identifies participant-described qualities that can inform future controlled studies of multisensory XR.

</details>

---

### 3. "To Boldly Go Where No One Has Gone Before" What Has AI Let Developers Unlock?
- **Authors**: Rudrajit Choudhuri, Jenna L. Butler, Christian Bird et al. (6 authors)
- **Date**: 2026-10-16 | **Links**: [Abstract](https://arxiv.org/abs/2610.23708v1) | [PDF](https://arxiv.org/pdf/2610.23708v1)
- **Status**: [ ] Unread  |  [ ] Dissected for Social Post

<details>
<summary><b>📖 Abstract / Summary (click to expand)</b></summary>

Measuring AI by how much faster developers work is like judging electricity by how much faster it spun a steam-era factory. A fuller measure asks what new work becomes possible. We surveyed 331 software developers at Microsoft about what AI lets them do that they could not do before and analyzed their answers using reflexive thematic analysis with a human-in-the-loop, multi-model AI council. Developers described doing familiar work faster (Faster, 45%), undertaking work previously beyond their reach (Further, 36.9%), and taking on new kinds of work centered on building for and directing AI agents (Afresh, 12.4%). Across these accounts, learning and scaffolding ran in both directions: developers learned new skills with AI while externalizing their tacit knowledge as the context and standards that guide AI's work. Drawing on Vygotsky's zone of proximal development, we frame developers and AI as joint learners whose zones meet at the skill-judgment nexus: AI can supply skill faster than it can reliably judge its own work, and developers must continuously bridge that gap. Whether they do sets them on one of two paths. On one, developers' judgment grows alongside AI's skill, and they codify what they learn so the loop keeps turning. On the other, they become hollow orchestrators, approving work they can no longer judge and losing the identity and meaning they once drew from it. Based on our findings, we offer a two-way scaffolding playbook to help developers, teams, and tool builders take the first path.

</details>

---

### 4. PresenceBench: An Exploratory Evaluation of Large Language Model Adaptation to User State
- **Authors**: Peña Arroyo Gallego, Mauro Ruiz Moreno, Alejandro Acien et al. (5 authors)
- **Date**: 2026-10-16 | **Links**: [Abstract](https://arxiv.org/abs/2610.23625v1) | [PDF](https://arxiv.org/pdf/2610.23625v1)
- **Status**: [ ] Unread  |  [ ] Dissected for Social Post

<details>
<summary><b>📖 Abstract / Summary (click to expand)</b></summary>

Presence-aware intelligence is the capacity of an AI system's intelligence layer to adapt appropriately to the functional state of the person it serves (here readiness, flow, and stability) while preserving task quality and safety. We introduce PresenceBench, an instrument for measuring it. PresenceBench evaluates how the intelligence layer uses a supplied state, not how that state is sensed, and breaks the capability into measurable properties. Two are tested here. Receptivity: does the model take up the state and give a better response than with no signal? Specificity: does any improvement depend on the correct state, rather than on extra structured context? A third, adaptation across states, is a required endpoint not measured in this release. A five-arm causal design answers both questions, against each model's own baseline and an equally structured mismatched-state control, scored by a correctness-gated human paired comparison. The exploratory evaluation covered four models across eighteen single-turn, six fixed three-turn and six simulated natural-conversation scenarios. Supplying a synthetic state, raw or translated into a response policy, gave human-preference point estimates above 0.5 for all four models (Claude Sonnet 5, DeepSeek V4 Pro, Gemini 3.6 Flash, GPT-5.6 Terra), with three of eight 95% intervals excluding chance. Specificity was not resolved: no per-model interval excluded chance, and the design cannot yet separate the state values from a generic instruction to adapt. Policy delivery reduced priced cost and output tokens against each model's baseline; these are resource-use changes, not efficiency gains, because correctness non-inferiority was not established. Safety-floor failures were rare (13 of 360 cases), with a non-significant excess under policy delivery. We report the instrument, the frozen results, and the controls a confirmatory study needs.

</details>

---

### 5. mmPencil: Toward Writing-Style-Independent In-Air Handwriting Recognition via mmWave Radar and Large Vision-Language Model
- **Authors**: Yifan Guo, Zhu Wang, Qian Qin et al. (9 authors)
- **Date**: 2026-10-16 | **Links**: [Abstract](https://arxiv.org/abs/2610.23419v1) | [PDF](https://arxiv.org/pdf/2610.23419v1)
- **Status**: [ ] Unread  |  [ ] Dissected for Social Post

<details>
<summary><b>📖 Abstract / Summary (click to expand)</b></summary>

In-air handwriting recognition based on radio frequency (RF) signals offers a promising solution for human-computer interaction, yet existing methods are often limited by predefined writing planes, constrained writing styles, and small recognition vocabularies. To address these limitations, we propose m^2VLMs, a modality mapping architecture that bridges millimeter-wave (mmWave) radar sensing and large vision-language models (VLMs), and develop mmPencil, a 3D in-air handwriting word recognition system. mmPencil reconstructs 3D handwriting trajectories from mmWave signals using a multi-stage spatial trajectory reconstruction algorithm and maps them into visual representations through a spatial-to-visual mapping algorithm, enabling VLMs to recognize handwriting while reducing sensitivity to writing styles and environmental factors. We collect and release a 3D mmWave handwriting dataset containing 7,664 samples of 200 words from 12 users across 22 writing scenarios. Extensive experiments demonstrate that mmPencil achieves robust word recognition under variations in writing position, range, angle, speed, size, direction, and user movement. It achieves 97.60% accuracy on 200 word classes for seen users and 92.50% zero-shot accuracy on 50 word classes for unseen users, outperforming state-of-the-art baselines.

</details>

---

### 6. Wait for It: A Component-Level Analysis of Latency Feedback Mechanisms for LLM Agents in VR
- **Authors**: Pratham Arora, Abhinav Lodha, Siddharth Siddharth
- **Date**: 2026-10-16 | **Links**: [Abstract](https://arxiv.org/abs/2610.23336v1) | [PDF](https://arxiv.org/pdf/2610.23336v1)
- **Status**: [ ] Unread  |  [ ] Dissected for Social Post

<details>
<summary><b>📖 Abstract / Summary (click to expand)</b></summary>

Delays in AI responses pose a significant challenge to immersive Virtual Reality experiences. While previous research demonstrates that feedback can reduce the perception of waiting, we lack understanding of which types work best and why. We conducted a within-subjects study with 18 participants to systematically compare three isolated feedback approaches during VR agent interactions: verbal fillers (e.g., um..., hmm...), visual indicators (loading spinners), and embodied gestures (thinking animations). Our results revealed that embodied gestures significantly outperformed visual loading indicators across multiple dimensions, making agents feel more lifelike and socially present. Interestingly, explicit visual feedback like loading spinners actually degraded perceived humanness and broke immersion by forcing users to shift from social to technical mental models. These findings suggest that natural, behavior-based feedback maintains the illusion of conversing with a thinking entity, while technical indicators expose the computational substrate. We present empirically-grounded design guidelines for creating more engaging AI-powered VR agents.

</details>

---

### 7. Designing for Imperfect Prompts: A Simulation-Based Evaluation of an LLM-Based Enterprise Data Assistant Using Knowledge Graphs
- **Authors**: Niklas Wagner, Alexander Mädche
- **Date**: 2026-10-16 | **Links**: [Abstract](https://arxiv.org/abs/2610.23304v1) | [PDF](https://arxiv.org/pdf/2610.23304v1)
- **Status**: [ ] Unread  |  [ ] Dissected for Social Post

<details>
<summary><b>📖 Abstract / Summary (click to expand)</b></summary>

Enterprise data assistants using large language models (LLMs) promise democratized data access in organizations. Yet in our real-world deployment within the CFO unit's data lake at an industry partner, we observed that business users frequently pose imperfect prompts that include domain-specific vocabulary and lack schema references or structural information. This Design Science Research study examines automatic resolution using a semantic mediation layer. We design and evaluate two design variants: schema-based mediation via semantic similarity, and knowledge graph-based mediation leveraging an automatically constructed knowledge graph from the data lake. Our simulation-based evaluation using real-world data, supported by LLM-as-a-Judge assessments and human validation, shows that knowledge graph-based mediation outperforms the schema-based approach in Precision, Recall, F1, and preserving user intent. We propose a design principle for knowledge graph-based mediation, demonstrating that structured knowledge representation bridges user intent and database structure and guides the design of enterprise data assistants across skill levels.

</details>

---

### 8. Annotrace: A Workbench for Step-Level Annotation of Agent Traces
- **Authors**: Arun Josephraj Arokiaraj, Chenyi Huang, Sahan Bulathwela et al. (5 authors)
- **Date**: 2026-10-16 | **Links**: [Abstract](https://arxiv.org/abs/2610.23284v1) | [PDF](https://arxiv.org/pdf/2610.23284v1)
- **Status**: [ ] Unread  |  [ ] Dissected for Social Post

<details>
<summary><b>📖 Abstract / Summary (click to expand)</b></summary>

Every study of why LLM agents fail begins by labelling traces by hand, and every such study builds its own throwaway tool. Observability platforms record agent traces but offer no structured labelling; annotation tools label text but have no notion of a step, a delegation or a tool call, leaving it unclear what the smallest unit of execution to label should be. Annotrace reads six trace formats, including OpenTelemetry GenAI, LangSmith and Langfuse, and turns each run into an ordered, nested list of steps. The annotator writes their own labelling codebook; a frontier model proposes a starting set from a sample of their own traces, answers first, and is asked exactly the questions the human is asked, making annotation a joint human-AI process. Annotrace measures agreement between any two annotators, human or AI. On a multi-agent question-answering corpus it reproduces a previous manual effort's 235 annotation units exactly, and two models labelling the same traces agree 91% of the time at $κ= 0.82$.

</details>

---
