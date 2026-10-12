# v33 Benchmark and Evaluation-Resource Coverage

[Back to the Paper Catalog](../README.md#catalog-benchmarks)

## Scope and counting

- Audited on October 12, 2026 against `IEEE_TPAMI__Physical_RSI-33.pdf` (54 pages).
- PDF SHA-256: `5841ba7da398549142ef89c36f48c06b19166b0c6504a524b73303bac4efd65d`.
- Scope: Section 6.3 (p. 28), Table 4 (p. 29), benchmark mentions elsewhere in the manuscript,
  and the corresponding bibliography records (pp. 31–54).
- Before this update, the 90-entry catalog included 21 benchmark/dataset/evaluation-resource
  entries, of which only 14 corresponded to Table 4's 38 named resources.
- This update adds the 24 missing Table 4 references, plus GemBench and DROID from elsewhere
  in the manuscript: **26 additions**, **47 resource entries**, and **116 total catalog entries**.
- Each publication has one catalog entry. Resource names are mapped to their associated papers;
  resource coverage is not the same as the number of standalone benchmark papers.

## Table 4 reconciliation

“Present” means present before this update; “Added” means introduced by this update.
All 38 named resources now map to a catalog entry. The groups below record Table 4 provenance;
the README remains organized by resource type rather than manuscript section.

| Table 4 evaluation focus | Named resources | Previously present | Added | Now covered |
| --- | ---: | ---: | ---: | ---: |
| Task Learning, Performance & Generalization | 12 | 3 | 9 | 12 |
| Robustness & Physical-World Evaluation | 10 | 1 | 9 | 10 |
| Feedback & Evaluation Reliability | 6 | 6 | 0 | 6 |
| Robot Engineering & Development | 3 | 2 | 1 | 3 |
| AI Research & Algorithm Improvement | 7 | 2 | 5 | 7 |
| **Total** | **38** | **14** | **24** | **38** |

### Task Learning, Performance & Generalization

| Resource in Table 4 | Catalog paper / resource | Change |
| --- | --- | --- |
| Meta-World | [Meta-World: A Benchmark and Evaluation for Multi-Task and Meta Reinforcement Learning](https://proceedings.mlr.press/v100/yu20a.html) | Present |
| RLBench | [RLBench: The Robot Learning Benchmark & Learning Environment](https://arxiv.org/abs/1909.12271) | Added |
| LIBERO | [LIBERO: Benchmarking Knowledge Transfer for Lifelong Robot Learning](https://arxiv.org/abs/2306.03310) | Present |
| ManiSkill3 | [ManiSkill3: GPU Parallelized Robotics Simulation and Rendering for Generalizable Embodied AI](https://arxiv.org/abs/2410.00425) | Added |
| CALVIN | [CALVIN: A Benchmark for Language-Conditioned Policy Learning for Long-Horizon Robot Manipulation Tasks](https://arxiv.org/abs/2112.03227) | Added |
| BEHAVIOR-1K | [BEHAVIOR-1K: A Human-Centered, Embodied AI Benchmark with 1,000 Everyday Activities and Realistic Simulation](https://arxiv.org/abs/2403.09227) | Added |
| RoboCasa365 | [RoboCasa365: A Large-Scale Simulation Framework for Training and Benchmarking Generalist Robots](https://arxiv.org/abs/2603.04356) | Present |
| robosuite | [robosuite: A Modular Simulation Framework and Benchmark for Robot Learning](https://arxiv.org/abs/2009.12293) | Added |
| robomimic | [What Matters in Learning from Offline Human Demonstrations for Robot Manipulation](https://arxiv.org/abs/2108.03298) | Added |
| VIMA-Bench | [VIMA: Robot Manipulation with Multimodal Prompts](https://proceedings.mlr.press/v202/jiang23b.html) | Added |
| VLABench | [VLABench: A Large-Scale Benchmark for Language-Conditioned Robotics Manipulation with Long-Horizon Reasoning Tasks](https://openaccess.thecvf.com/content/ICCV2025/html/Zhang_VLABench_A_Large-Scale_Benchmark_for_Language-Conditioned_Robotics_Manipulation_with_Long-Horizon_ICCV_2025_paper.html) | Added |
| EmbodiedBench | [EmbodiedBench: Comprehensive Benchmarking Multi-modal Large Language Models for Vision-Driven Embodied Agents](https://proceedings.mlr.press/v267/yang25f.html) | Added |

### Robustness & Physical-World Evaluation

| Resource in Table 4 | Catalog paper / resource | Change |
| --- | --- | --- |
| LIBERO-PRO | [LIBERO-PRO: Towards Robust and Fair Evaluation of Vision-Language-Action Models Beyond Memorization](https://arxiv.org/abs/2510.03827) | Added |
| SIMPLER | [Evaluating Real-World Robot Manipulation Policies in Simulation](https://arxiv.org/abs/2405.05941) | Added |
| RoboTwin | [RoboTwin: Dual-Arm Robot Benchmark with Generative Digital Twins](https://arxiv.org/abs/2504.13059) | Added |
| RoboDojo | [RoboDojo: A Unified Sim-and-Real Benchmark for Comprehensive Evaluation of Generalist Robot Manipulation Policies](https://arxiv.org/abs/2607.04434) | Added |
| THE COLOSSEUM | [THE COLOSSEUM: A Benchmark for Evaluating Generalization for Robotic Manipulation](https://arxiv.org/abs/2402.08191) | Added |
| LIBERO-Plus | [LIBERO-Plus: In-depth Robustness Analysis of Vision-Language-Action Models](https://arxiv.org/abs/2510.13626) | Added |
| VLA-Arena | [VLA-Arena: An Open-Source Framework for Benchmarking Vision-Language-Action Models](https://proceedings.mlr.press/v306/zhang26cp.html) | Added |
| RoboTwin 2.0 | [RoboTwin 2.0: A Scalable Data Generator and Benchmark with Strong Domain Randomization for Robust Bimanual Robotic Manipulation](https://proceedings.mlr.press/v306/chen26j.html) | Added |
| REALM | [REALM: A Real-to-Sim Validated Benchmark for Generalization in Robotic Manipulation](https://arxiv.org/abs/2512.19562) | Added |
| RoboArena | [RoboArena: Distributed Real-World Evaluation of Generalist Robot Policies](https://proceedings.mlr.press/v305/atreya25a.html) | Present |

### Feedback & Evaluation Reliability

| Resource in Table 4 | Catalog paper / resource | Change |
| --- | --- | --- |
| FailBench | [FailBench: How Reliable Are VLMs at Judging Robot Task Success?](https://arxiv.org/abs/2609.03611v1) | Present |
| RoboRewardBench | [RoboReward: General-Purpose Vision-Language Reward Models for Robotics](https://arxiv.org/abs/2601.00675) | Present |
| WorldEval | [WorldEval: World Model as Real-World Robot Policies Evaluator](https://arxiv.org/abs/2505.19017) | Present |
| dWorldEval | [dWorldEval: Scalable Robotic Policy Evaluation via Discrete Diffusion World Model](https://arxiv.org/abs/2604.22152) | Present |
| SC3-Eval | [SC3-Eval: Evaluating Robot Foundation Models via Self-Consistent Video Generation](https://arxiv.org/abs/2606.18610) | Present |
| RBM-EVAL | [Robometer: Scaling General-Purpose Robotic Reward Models via Trajectory Comparisons](https://arxiv.org/abs/2603.02115) | Present |

### Robot Engineering & Development

| Resource in Table 4 | Catalog paper / resource | Change |
| --- | --- | --- |
| CaP-Bench (CaP-X) | [CaP-X: A Framework for Benchmarking and Improving Coding Agents for Robot Manipulation](https://proceedings.mlr.press/v306/fu26u.html) | Present |
| EmboCoach-Bench | [From Digital to Physical: Digital Agents as Autonomous Coaches for Physical Intelligence](https://arxiv.org/abs/2601.21570) | Present |
| RLE-Bench | [RLE-Bench: A Qualifying Exam for Coding Agents as Robot Learning Engineers](https://arxiv.org/abs/2609.34210) | Added |

### AI Research & Algorithm Improvement

| Resource in Table 4 | Catalog paper / resource | Change |
| --- | --- | --- |
| AI4AI-Bench | [AI4AI-Bench: Benchmarking LLM Agents in Algorithmic Design for Recursive Self-Improvement](https://arxiv.org/abs/2608.20318) | Present |
| RSIBench-Data | [RSIBench-Data: Benchmarking Data-Centric Research for Recursive Self-Improvement](https://arxiv.org/abs/2607.25886) | Present |
| MLAgentBench | [MLAgentBench: Evaluating Language Agents on Machine Learning Experimentation](https://proceedings.mlr.press/v235/huang24y.html) | Added |
| MLE-bench | [MLE-bench: Evaluating Machine Learning Agents on Machine Learning Engineering](https://arxiv.org/abs/2410.07095) | Added |
| MLGym-Bench | [MLGym: A New Framework and Benchmark for Advancing AI Research Agents](https://arxiv.org/abs/2502.14499) | Added |
| MLRC-Bench | [MLRC-Bench: Can Language Agents Solve Machine Learning Research Challenges?](https://arxiv.org/abs/2504.09702) | Added |
| RE-Bench | [RE-Bench: Evaluating Frontier AI R&D Capabilities of Language Model Agents against Human Experts](https://proceedings.mlr.press/v267/wijk25a.html) | Added |

## Nine entries outside Table 4

These entries are not counted toward the 38/38 Table 4 coverage total. Not every additional
entry is a benchmark, and not every inherited catalog entry is cited in v33.

| Entry | Provenance / scope | Change |
| --- | --- | --- |
| [RoboLab](https://arxiv.org/abs/2604.09860) | Inherited simulation-benchmark entry; not found in the v33 extracted text or bibliography. | Present |
| [Open X-Embodiment](https://arxiv.org/abs/2310.08864) | Shared dataset/model resource cited in the introduction, p. 3; not a standalone evaluation benchmark. | Present |
| [AutoEval](https://arxiv.org/abs/2503.24278v1) | Real-world evaluation platform named in Section 7, p. 30; Zhou et al. (2025c), bibliography p. 54. | Present |
| [GigaWorld-1](https://arxiv.org/abs/2607.02642) | Inherited evaluation-world-model entry; not found in the v33 extracted text or bibliography. | Present |
| [HarnessDev](https://arxiv.org/abs/2609.01437) | Named in Section 6.3, p. 28; not included in Table 4. | Present |
| [RSI-Exam](https://github.com/aiming-lab/RSI-Exam) | Named in Section 6.3, p. 28; cited as a repository resource, not a peer-reviewed paper. | Present |
| [PAST-Bench](https://arxiv.org/abs/2608.04003) | Named in Section 6.3, p. 28; not included in Table 4. | Present |
| [GemBench](https://arxiv.org/abs/2410.01345) | Discussed in Section 2, p. 10; Garcia et al. (2025), bibliography p. 37. | Added |
| [DROID](https://www.roboticsproceedings.org/rss20/p120.html) | Shared dataset cited as Khazatsky et al. (2024) in the introduction, p. 3; bibliography pp. 40–41. | Added |

## Citation and version checks

- All 47 linked source pages were retrieved successfully during this audit. For the 46 paper
  entries, titles and author information were compared with official arXiv, PMLR, CVF, or RSS
  pages. RSI-Exam was checked against the project repository and remains labeled as a repository.
  Title capitalization and collective-author formatting are not treated as different works.
- The 26 new entries use titles and first-author names from those primary-source pages.
  For example, the abbreviated `X. Zhou et al.` in the PDF is expanded to `Xueyang Zhou et al.`
  for LIBERO-PRO. The PMLR title for VIMA is retained as *VIMA: Robot Manipulation with
  Multimodal Prompts*, with `VIMA-Bench` identified separately as the resource.
- Citation years follow the v33 bibliography, not uniformly the first arXiv submission date.
  For example, ManiSkill3 and GemBench are cited as 2025 although their preprints began in 2024;
  CALVIN is cited as 2022 although its preprint began in 2021. RLBench retains v33's 2019
  preprint citation. These dates must not be mixed when comparing counts or sorting records.
- Resource/paper aliases include **robomimic**, **VIMA-Bench**, **SIMPLER**, **RoboRewardBench**,
  **RBM-EVAL**, **CaP-Bench**, **EmboCoach-Bench**, **MLGym-Bench**, and **GemBench**.
  The resource label does not replace the source paper's title or establish version equivalence.
- RoboTwin and RoboTwin 2.0 are separate cited works, as are LIBERO, LIBERO-PRO, and LIBERO-Plus.
  They are not collapsed just because they share a family name.
- The `LIBERO-Pro Long` protocol mentioned on p. 11 is not independently equated here with the
  Table 4 `LIBERO-PRO` paper. The manuscript cites the original LIBERO work in that discussion;
  protocol/version identity requires a separate check of the relevant experiment and release.
- The PDF has duplicate bibliography records for the robomimic-associated paper
  (Mandlekar et al., 2021a/2021b, pp. 43–44) and WorldEval
  (Li et al., 2025a/2025b, p. 42). Each is counted once in the catalog.
- EmboCoach-Bench remains mapped to the paper *From Digital to Physical* as in Table 4;
  the existing paper/benchmark version caveat is retained.

This is a resource-coverage and citation-metadata audit. It does **not** validate every scientific
claim, experimental result, benchmark release, or Physical RSI capability assignment in v33.
No PDF content or bibliography was modified.
