# Say No Too Often: Over-Refusals in Foundation Models

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![Contributions Welcome](https://img.shields.io/badge/Contributions-Welcome-blue)](#)

> This project provides a curated list of papers related to the survey: **Say No Too Often: Over-Refusals in Foundation Models** (Continually Updated).

## Table of Contents

- [Overview](#overview)
- [Paper List](#paper-list)
  - [Benchmarks](#benchmarks)
    - [LLMs — Single-Turn Questions](#llms--single-turn-questions)
    - [LLMs — Complex Contexts](#llms--complex-contexts)
    - [Vision-Language Models (VLMs)](#vision-language-models-vlms)
    - [Other Modalities and Domains](#other-modalities-and-domains)
  - [Mitigation Methods](#mitigation-methods)
    - [Training-based Methods](#training-based-methods)
    - [Inference-Time Methods](#inference-time-methods)
    - [Explanation-based Methods](#explanation-based-methods)
  - [Challenges and Future Directions](#challenges-and-future-directions)
  - [Applications](#applications)

## Overview

**Over-refusal** occurs when foundation models reject benign queries due to overly conservative safety alignment, undermining usability without improving safety. In contrast to *under-refusal* (harmful compliance), over-refusal arises from excessive safety mechanisms that suppress legitimate user requests. This survey provides a comprehensive taxonomy of over-refusal benchmarks, evaluation metrics, and mitigation strategies across multiple modalities including LLMs, VLMs, audio language models, and text-to-image models.

## Paper List

### Benchmarks

#### LLMs — Single-Turn Questions

* XSTest: A Test Suite for Identifying Exaggerated Safety Behaviours in Large Language Models (Röttger et al., NAACL 2024) [📖](https://aclanthology.org/2024.naacl-long.301/)
* Navigating the OverKill in Large Language Models (Shi et al., ACL 2024)
* Automatic Pseudo-Harmful Prompt Generation for Evaluating False Refusals in Large Language Models (An et al., COLM 2024)
* OR-Bench: An Over-Refusal Benchmark for Large Language Models (Cui et al., ICML 2025) [📖](https://proceedings.mlr.press/v267/cui25a.html)
* FalseReject: A Resource for Improving Contextual Safety and Mitigating Over-Refusals in LLMs via Structured Reasoning (Zhang et al., COLM 2025) [📖](https://openreview.net/forum?id=1w9Hay7tvm)
* SCOPE: Scalable and Adaptive Evaluation of Misguided Safety Refusal in LLMs (Zeng et al., 2025) [📖](https://openreview.net/forum?id=72H3w4LHXM)
* EVOREFUSE: Evolutionary Prompt Optimization for Evaluation and Mitigation of LLM Over-Refusal to Pseudo-Malicious Instructions (Wu et al., NeurIPS 2025) [📖](https://openreview.net/forum?id=dbq6NZfi3c)
* ORFuzz: Fuzzing the "Other Side" of LLM Safety — Testing Over-Refusal (Zhang et al., arXiv 2025) [📖](https://arxiv.org/abs/2508.11222)

#### LLMs — Complex Contexts

* Beyond Over-Refusal: Scenario-Based Diagnostics and Post-Hoc Mitigation for Exaggerated Refusals in LLMs (Yuan et al., arXiv 2025) [📖](https://arxiv.org/abs/2510.08158) — *Multi-turn dialogue*
* COVER: Context-Driven Over-Refusal Verification in LLMs (Sullutrone et al., ACL Findings 2025) — *Long-context*
* Steering Over-refusals Towards Safety in Retrieval Augmented Generation (Maskey et al., arXiv 2025) [📖](https://arxiv.org/abs/2510.10452) — *RAG*
* Understanding and Mitigating Overrefusal in LLMs from an Unveiling Perspective of Safety Decision Boundary (Pan et al., EMNLP 2025) — *Multilingual*

#### Vision-Language Models (VLMs)

* Don't Always Say No to Me: Benchmarking Safety-Related Refusal in Large VLM (Liu et al., 2024) [📖](https://openreview.net/forum?id=OLEQJoAED6)
* MOSSBench: Is Your Multimodal Language Model Oversensitive to Safe Queries? (Li et al., ICLR 2025) [📖](https://openreview.net/forum?id=QsA3YzNUxA)
* DUAL-Bench: Measuring Over-Refusal and Robustness in Vision-Language Models (Ren et al., arXiv 2025) [📖](https://arxiv.org/abs/2510.10846)

#### Other Modalities and Domains

* OVERT: A Benchmark for Over-Refusal Evaluation on Text-to-Image Models (Cheng et al., NeurIPS 2025) — *Text-to-Image*
* Reshaping Representation Space to Balance the Safety and Over-rejection in Large Audio Language Models (Yang et al., EMNLP 2025) — *Audio Language Models*
* Health-ORSC-Bench: A Benchmark for Measuring Over-Refusal and Safety Completion in Health Context (Zhang et al., arXiv 2026) [📖](https://arxiv.org/abs/2601.17642) — *Healthcare*

---

### Mitigation Methods

#### Training-based Methods

**Supervised Fine-Tuning (SFT)**

* POROver: Improving Safety and Reducing Overrefusal in Large Language Models with Overgeneration and Preference Optimization (Karaman et al., 2025) [📖](https://openreview.net/forum?id=5EuAMDMPRK)
* There Is More to Refusal in Large Language Models than a Single Direction (Joad et al., arXiv 2026) [📖](https://arxiv.org/abs/2602.02132)

**RL-based Post-Training**

* Understanding and Mitigating Overrefusal in LLMs from an Unveiling Perspective of Safety Decision Boundary (Pan et al., EMNLP 2025) — *DPO*
* Reshaping Representation Space to Balance the Safety and Over-rejection in Large Audio Language Models (Yang et al., EMNLP 2025) — *DPO + Activation*
* Pragma-VL: Towards a Pragmatic Arbitration of Safety and Helpfulness in MLLMs (Wen et al., ICLR 2026) — *GRPO*

#### Inference-Time Methods

**Prompt Engineering**

* Mitigating Exaggerated Safety in Large Language Models (Ray et al., arXiv 2024) [📖](https://arxiv.org/abs/2405.05418)
* Navigating the OverKill in Large Language Models (Shi et al., ACL 2024) — *CoT, ICL*

**Activation Steering**

* SCANS: Mitigating the Exaggerated Safety for LLMs via Safety-Conscious Activation Steering (Cao et al., AAAI 2025)
* Surgical, Cheap, and Flexible: Mitigating False Refusal in Language Models via Single Vector Ablation (Wang et al., ICLR 2025) [📖](https://openreview.net/forum?id=SCBn8MCLwc)
* Just Enough Shifts: Mitigating Over-Refusal in Aligned Language Models with Targeted Representation Fine-Tuning (Dabas et al., ICML 2025) [📖](https://proceedings.mlr.press/v267/dabas25a.html)
* SafeConstellations: Steering LLM Safety to Reduce Over-Refusals Through Task-Specific Trajectory (Maskey et al., arXiv 2025) [📖](https://arxiv.org/abs/2508.11290)
* Mitigating Over-Refusal in Aligned Large Language Models via Inference-Time Activation Energy (Jiang et al., arXiv 2026) [📖](https://arxiv.org/abs/2510.08646)
* Steering to Say No: Configurable Refusal via Activation Steering in Vision Language Models (Yang et al., arXiv 2026) [📖](https://arxiv.org/abs/2602.07013)
* There Is More to Refusal in Large Language Models than a Single Direction (Joad et al., arXiv 2026) [📖](https://arxiv.org/abs/2602.02132)

**Decoding-Level Calibration**

* Navigating the OverKill in Large Language Models (Shi et al., ACL 2024) — *Self-contrastive decoding*
* Steering Multimodal Large Language Models Decoding for Context-Aware Safety (Liu et al., arXiv 2025) [📖](https://arxiv.org/abs/2509.19212)
* There Is More to Refusal in Large Language Models than a Single Direction (Joad et al., arXiv 2026) [📖](https://arxiv.org/abs/2602.02132)

#### Explanation-based Methods

* Beyond Over-Refusal: Scenario-Based Diagnostics and Post-Hoc Mitigation for Exaggerated Refusals in LLMs (Yuan et al., arXiv 2025) [📖](https://arxiv.org/abs/2510.08158)

---

### Challenges and Future Directions

The survey identifies five key open challenges for future research:

1. **Human Perception of Over-Refusal** — Moving beyond model-centric metrics to capture how users perceive refusal behaviors.
2. **Utility Functions in Explanation-based Methods** — Designing refusal-oriented utility functions for more accurate attribution.
3. **Domain-Specific Over-Refusal** — Adapting mitigation strategies to specialized domains such as healthcare, finance, education, and law.
4. **Over-Refusal in Different Modalities** — Extending research to under-explored modalities such as video-language models and embodied systems.
5. **Ambiguous Safety Boundaries** — Addressing the inherent ambiguity in distinguishing benign from harmful queries under different safety policies.

### Applications

Over-refusal mitigation is critical across several real-world domains:

- **Software Engineering & Cybersecurity** — Enabling vulnerability analysis and security auditing.
- **Healthcare** — Avoiding withholding benign health-related guidance.
- **Education** — Supporting legitimate learning queries that contain sensitive keywords.
- **Legal Systems** — Facilitating legal consultation and case analysis.
- **Military & Defense** — Ensuring reliable processing of legitimate analytical requests.
