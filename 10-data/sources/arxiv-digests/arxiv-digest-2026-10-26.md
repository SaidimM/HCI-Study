---
date: 2026-10-26
type: arxiv-digest
category: cs.HC
tags: [hci, arxiv, reading-queue]
---

# 📡 arXiv cs.HC Digest — 2026-10-26

> Automated intake of the latest Human-Computer Interaction preprints.
> Pick 1–2 papers that look promising to dissect using [[90-templates/paper-note|Paper Note Template]].

---

### 1. Measure Before You Train: Typed Decision Models vs. a Classical Baseline vs. a Generative LLM for Routing a Personal Multilingual Inbox
- **Authors**: Federico Lucca
- **Date**: 2026-10-23 | **Links**: [Abstract](https://arxiv.org/abs/2610.32955v1) | [PDF](https://arxiv.org/pdf/2610.32955v1)
- **Status**: [ ] Unread  |  [ ] Dissected for Social Post

<details>
<summary><b>📖 Abstract / Summary (click to expand)</b></summary>

Personal email agents decide, for every message, what it is, whether it is urgent, whether to draft a reply, create a task, or ignore it. Their error rate is rarely measured: the stored labels were written by the system itself. We present Foyer, a self-hosted personal inbox agent in daily use, and a measurement protocol (stratified sampling, frozen snapshots, thread-grouped splits, pre-registered hypotheses, human labels in the agent's review loop) that yields ground truth before any training. On 739 real Italian/English emails labelled by the owner (231 unbiased, 500 adversarially sampled), we compare nine systems under thread-grouped cross-validation: the production keyword rules, a TF-IDF + logistic-regression baseline, local typed decision models (Tev1, Nimble), a hosted decision model (Nimble v4-max), and hosted generative LLMs (Qwen2.5-7B, Gemma 4 26B/31B). Four results. The production rules score 28% on message type against a 58% majority class: the field shown most prominently carried no information. With ~200 labels, logistic regression has the highest accuracy on every field (type 0.79, urgency 0.74, needs-reply 0.83, is-noise 0.90), though it never predicts the two rarest classes and is statistically tied with Gemma 4 on type; few-shot prompting does not close the gap. The sender's relationship (client, supplier, service) is recovered from other emails of the same contact with 98.6% accuracy where the contact has been seen, and is not inferable from a single message by any model: it belongs in the contact graph, not the prompt. Finally, accuracy is not the product metric: composed into actions, the most accurate system most often ignores emails needing action (18% vs 4% for the best LLM); a cost-chosen threshold on its noise probability halves that rate and makes it the cheapest system.

</details>

---

### 2. Runtime BiDi Structural Verification Catches Right-to-Left Layout Defects that Accessibility, Actionability, and Logical-Property Linting Miss
- **Authors**: Karan Yadav
- **Date**: 2026-10-23 | **Links**: [Abstract](https://arxiv.org/abs/2610.32934v1) | [PDF](https://arxiv.org/pdf/2610.32934v1)
- **Status**: [ ] Unread  |  [ ] Dissected for Social Post

<details>
<summary><b>📖 Abstract / Summary (click to expand)</b></summary>

Bidirectional (right-to-left, RTL) layout defects arise when interfaces authored with physical directional CSS (margin-left, border-left, text-align:left) are rendered under dir="rtl" without being mirrored. Accessibility engines (axe-core), actionability engines (Playwright), and even Stylelint's current core logical-property rule fail to localise these defects. We present runtime structural invariants -- a zero-golden mode over computed style and geometry, and a bidi-conservative differential mode -- that catch them in a headless browser. On a held-out benchmark of 14 real RTL bugs reconstructed from dated fix commits in Bootstrap and Material Components Web, the detector recovers 13/14 (2 via zero-golden, 11 via the differential mode), with no false alarm on any patched version; on the actual committed historical bootstrap.rtl.css it catches 1 of 2 attempted. It reports 0 false positives on 16 negative LTR-island cases and, in both modes, on 43 unmodified real components across four design systems and three RTL architectures (rule-of-three 95% upper bound <= 7%), and it surfaced a real directional defect in the current Bulma 1.0.4. By contrast, Stylelint's core rule emits an identical 1744 warnings on Bootstrap's LTR and correct-RTL builds, pseudo-localisation detects none of the mirroring bugs, and a naive pixel mirror-and-diff reaches only F1 0.87 with a test-set-tuned threshold. The two modes are complementary: zero-golden is the sole detector of the decoration/styling-asymmetry class (5/6) but false-flags the correct logical border-inline-end, while the differential detects none of that class yet never false-alarms and is empirically exact on the block-level inset/margin class. We scope this paper to detection; repair is future work.

</details>

---

### 3. STROKE: Simple Sparse Structural Occlusions for Black-Box Adversarial Attacks
- **Authors**: Ankit Gupta, Akshat Pandya, Paul Lin et al. (5 authors)
- **Date**: 2026-10-23 | **Links**: [Abstract](https://arxiv.org/abs/2610.32932v1) | [PDF](https://arxiv.org/pdf/2610.32932v1)
- **Status**: [ ] Unread  |  [ ] Dissected for Social Post

<details>
<summary><b>📖 Abstract / Summary (click to expand)</b></summary>

We introduce STROKE, a query-efficient score-based black-box adversarial attack that constructs perturbations from simple oriented rectangular occlusions. STROKE optimizes these perturbations through a lightweight greedy add-and-refine procedure. Across diverse image classifiers, STROKE achieves high attack success with low query counts at nominal 1--2\% area settings, showing favorable performance relative to existing patch-based attacks in several configurations. Matched comparisons further demonstrate substantial reductions in wall-clock attack time, while ablation studies examine the key design choices and effectiveness across structural primitives. These findings suggest that simple structural occlusions offer an effective and computationally efficient search space for black-box adversarial attacks.

</details>

---

### 4. What Mean Error Misses: Device-Clock Diagnostics for Evaluating Eye Tracking across Three Virtual Reality Headsets
- **Authors**: Aleksandr Chernysh, Mehedi Hasan Raju, Kamrul Hasan et al. (7 authors)
- **Date**: 2026-10-23 | **Links**: [Abstract](https://arxiv.org/abs/2610.32915v1) | [PDF](https://arxiv.org/pdf/2610.32915v1)
- **Status**: [ ] Unread  |  [ ] Dissected for Social Post

<details>
<summary><b>📖 Abstract / Summary (click to expand)</b></summary>

Gaze research in virtual reality needs eye trackers of known error. Thirty participants completed the same protocol on the Meta Quest Pro (QP), HTC VIVE Pro Eye (PE) and HTC VIVE Focus Vision (FV); to our knowledge, this is the first evaluation of the FV eye tracker. In a random-saccade task, median participant mean error was 1.04° on QP, 1.50° on PE and 2.41° on FV, which remained least accurate after linear recalibration. In a later block with a darker background, PE error rose by 0.70°. FV samples were positively correlated: dispersion was 9.8 times the sample-to-sample root mean square. The device clocks showed losses that mean error hides. QP paused for up to 6.04 s, and FV skipped single samples. During instructed eye closures, QP flagged every sample valid while gaze moved 9.74°. Evaluations should report repeated timestamps, loss composition on the device clock and validity during eye closures.

</details>

---

### 5. When Should I Trust This? Designing and Evaluating Factuality Indicators for LLM-based Chatbots
- **Authors**: Greta Warren, Jessica Heal, Sila Eser et al. (6 authors)
- **Date**: 2026-10-23 | **Links**: [Abstract](https://arxiv.org/abs/2610.32883v1) | [PDF](https://arxiv.org/pdf/2610.32883v1)
- **Status**: [ ] Unread  |  [ ] Dissected for Social Post

<details>
<summary><b>📖 Abstract / Summary (click to expand)</b></summary>

Generative AI systems increasingly mediate how people seek information, yet communicating AI factuality to laypeople remains challenging. Through a mixed-methods investigation involving interviews (N=8), a survey (N=1,000), and an experiment (N=5,151), we examine how people evaluate AI-generated information for gardening, mathematical, and medical queries, and how factuality indicators (confidence and sources) shape perceptions. Our interviews and survey show people selectively verify AI responses using external and AI-provided evidence, moderated by contextual factors. Although confidence-indicators affected trust and accuracy perceptions, people hold diverse, ambiguous interpretations of AI confidence. Sources were viewed as crucial, yet users raised concerns about source reliability and verification effort. Our experiment showed that confidence and source-based indicators influenced initial perceptions, but effects disappeared once participants learned the response's correctness. Medical queries elicited skepticism regardless of indicator. Findings motivate helping users interpret model confidence and integrating source information into the interface to support calibrated trust in AI-supported information-seeking.

</details>

---

### 6. Beyond pass or fail: an information-processing account of the Turing Test
- **Authors**: Qiwei Zhao, Oriana Pansardi, James W. Strachan et al. (12 authors)
- **Date**: 2026-10-23 | **Links**: [Abstract](https://arxiv.org/abs/2610.32868v1) | [PDF](https://arxiv.org/pdf/2610.32868v1)
- **Status**: [ ] Unread  |  [ ] Dissected for Social Post

<details>
<summary><b>📖 Abstract / Summary (click to expand)</b></summary>

The Turing Test is passed when a human interrogator cannot distinguish machine-generated responses from human ones. Yet behavioral indistinguishability can reflect two fundamentally different failures: a failure of encoding, in which machine and human output distributions overlap so closely that source information is effectively absent; or a failure of readout, in which source information is present but the interrogator fails to extract it. To dissociate these possibilities, we inverted the Turing Test, placing humans and AI systems in symmetrical interrogator roles. Using a quantitative information-processing framework, we separated encoding, the information contained in the text; readout, the extraction of that information by an interrogator; and meta-readout, the interrogator's explicit access to the features guiding its own judgments. Across two series of experiments involving more than 3800 human interrogators and two generations of GPT models (GPT-4 and GPT-5), we found a striking dissociation across processing levels and interrogator types. As AI-generated responses became more human-like from GPT-4 to GPT-5, source information became more difficult for human interrogators to extract. GPT-5 interrogators, by contrast, read out source-discriminating information more accurately than GPT-4 interrogators. This improvement, however, came with a specific limitation: GPT-5 explanations only partially aligned with the feature weightings that actually predicted their judgments. Human interrogators showed the complementary pattern, with modest readout alignment but comparatively higher meta-readout alignment. Together, these findings suggest a double dissociation between readout and meta-readout across human and GPT interrogators.

</details>

---

### 7. SPOOK: Sparse Pixel Optimization for Off-Manifold Knowledge in Vision Encoders
- **Authors**: Ankit Gupta, Akshat Pandya, Christoph Adami et al. (4 authors)
- **Date**: 2026-10-23 | **Links**: [Abstract](https://arxiv.org/abs/2610.32835v1) | [PDF](https://arxiv.org/pdf/2610.32835v1)
- **Status**: [ ] Unread  |  [ ] Dissected for Social Post

<details>
<summary><b>📖 Abstract / Summary (click to expand)</b></summary>

Modern vision encoders are widely used as semantic representations, but the relationship between embedding similarity and human-visible semantics can become unclear far from the natural-image manifold. We probe this regime in a black-box setting by applying sparse pixel edits to blank canvases with a simple pixel-level hill-climbing procedure. Across ImageNet and Flickr30k, we evaluate whether these edited blank canvases can retrieve chosen targets in multimodal contrastive encoders and self-supervised visual encoders. On OpenCLIP, inputs optimized toward class prompts achieve strong top-1 and top-5 targeted retrieval performance; on DINOv3, inputs optimized toward class prototypes achieve high target alignment and near-top prototype ranks. These results show that sparse edits on otherwise blank, visually non-semantic inputs can enter target semantic basins in both language-aligned and self-supervised visual representation spaces. Our findings identify a shared off-manifold failure mode of modern vision encoders and suggest sparse blank-canvas optimization as a simple probe of representation geometry.

</details>

---

### 8. EMG Tokenization Preserves Movement Information at a Fraction of the Bitrate
- **Authors**: Raul C. Sîmpetru, Amin Olamazadeh, Devon Rohlf et al. (5 authors)
- **Date**: 2026-10-23 | **Links**: [Abstract](https://arxiv.org/abs/2610.32674v1) | [PDF](https://arxiv.org/pdf/2610.32674v1)
- **Status**: [ ] Unread  |  [ ] Dissected for Social Post

<details>
<summary><b>📖 Abstract / Summary (click to expand)</b></summary>

Wireless electromyography (EMG) interfaces must balance electrode coverage against transmission bandwidth. Here, we show that compact EMG tokens substantially reduce payload while retaining information for three-dimensional hand-pose decoding. We evaluate two causal tokenizers fitted without pose labels: an encoder pretrained to reconstruct EMG spectra and one based on SPAR, an engineered spectral-spatial representation of neighbouring electrodes. In personalized, within-session experiments with 320-channel EMG from nine participants, we compare tokenized and continuous features using matched decoder architectures and training procedures. Averaged across decoders, tokenization changed mean error by +0.01 mm for SPAR (95% confidence interval: -0.12 to 0.14) and +0.45 mm for the learned representation (0.10 to 0.82). Both increases met a 1 mm non-inferiority criterion. Stored token arrays reduced payloads 41-fold relative to raw EMG and 36-fold relative to continuous SPAR features. On sampled windows of the public emg2pose benchmark's test partition, absolute differences in mean error between learned tokens and continuous features were below 0.05 mm across 176 participants and in the subset of 20 participants unseen during training. Electrode coverage, calibration, and unseen recordings affected SPAR decoding more than quantization did. In a computational benchmark, optimized SPAR generated tokens for 63 channels within 20 ms on a Cortex-M55 microcontroller. These findings support tokenization as a compact interface between wearable sensing and movement decoding, allowing decoders to be updated while the wearable encoder and transmitted representation remain fixed.

</details>

---
