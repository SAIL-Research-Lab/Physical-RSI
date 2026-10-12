<a id="readme-top"></a>

<div align="center">

<h1><em>Physical RSI</em></h1>

<p align="center"><strong>Physical Recursive Self-Improvement</strong></p>

<p align="center"><em>From adaptation to inherited improvement.</em></p>

<p align="center">A paper-aligned, evidence-auditable map of recursive improvement in embodied systems.</p>

<p align="center">
  <a href="#paper-catalog"><img src="https://img.shields.io/badge/featured_catalog-65_papers-2563eb?style=flat-square" alt="65 papers in the featured catalog"></a>
  <a href="docs/paper-reference-index.md"><img src="https://img.shields.io/badge/bibliography-102%2F102-0f766e?style=flat-square" alt="102 of 102 unique paper references indexed"></a>
  <a href="#capability-map"><img src="https://img.shields.io/badge/taxonomy-L1--L5-7c3aed?style=flat-square" alt="L1 to L5 capability taxonomy"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/license-MIT-475569?style=flat-square" alt="MIT License"></a>
</p>

<p align="center">
  <a href="#the-boundary">Boundary</a> &nbsp;|&nbsp;
  <a href="#capability-map">L1-L5</a> &nbsp;|&nbsp;
  <a href="#three-views-of-one-system">Research map</a> &nbsp;|&nbsp;
  <a href="#paper-catalog">Paper catalog</a> &nbsp;|&nbsp;
  <a href="docs/paper-reference-index.md">All references</a>
</p>

</div>

<p align="center">
  <img src="docs/figures/darwin-haeckel-evolutionary-trees.png" alt="Darwin's first evolutionary tree sketch beside Haeckel's nineteenth-century pedigree of humankind" width="400">
</p>
<p align="center"><em>Life is not repetition, but creation. Duration carries the whole of reality: a boundless river flowing toward a horizon with no predetermined end.</em><br>
<sub>Darwin's <a href="https://commons.wikimedia.org/wiki/File:Darwin_Tree_1837.png">first evolutionary tree</a> (1837), beside Haeckel's <a href="https://commons.wikimedia.org/wiki/File:Pedigree_of_man_(Haeckel_1874).jpg"><em>Pedigree of Man</em></a> (1874). Both works are public domain.</sub></p>

<a id="from-evolution-to-physical-rsi"></a>

## From Evolution to Physical RSI <sub><a href="#readme-top">top</a></sub>

Natural evolution did not become powerful because organisms changed once. Variation mattered
because selection acted on it, and inheritance carried the consequences forward. Across
generations, the environment became part of the history of what life could become.

Physical RSI asks whether an embodied artificial system can form an engineered counterpart to
this chain. Physical interaction supplies experience, verification determines which changes are
admitted, and inheritance returns accepted changes to the next improvement cycle.

> **Can the world change not only what a machine does, but how it produces its next
> improvement?**

The analogy deliberately stops there. Natural selection does not owe us a protected objective,
an audit trail, or a matched resource budget. An engineered recursive system does. A robot may
collect more data, recover from a failed grasp, or fine-tune a policy after deployment, but these
remain forms of adaptation until a retained change reaches the mechanism that generates,
evaluates, or selects later updates. The recursion becomes *physical* only when real interaction
has a causal role in deciding what mechanism changes or survives.

This repository is for **Physical Recursive Self-Improvement** research, where we study how
physical interaction can drive retained changes in embodied systems and the processes that improve
them. It follows the evidence boundaries of the accompanying paper and serves as a reading map,
not a leaderboard: labels such as "self-improving," "autonomous," or "lifelong" are not treated as
evidence on their own.

This repository is actively maintained. If an author would prefer not to have a paper listed here,
please contact <shangding.gu@berkeley.edu>. Constructive comments, corrections, and suggestions are
welcome.

You are also welcome to update the collection. To suggest a missing paper or correct an existing
entry, you can:

- fork this repository and open a pull request;
- [report an issue](https://github.com/SAIL-Research-Lab/Physical-RSI/issues);
- or email <shangding.gu@berkeley.edu>.

**Content**

Explore the framework, paper collection, and open questions:

- [From Evolution to Physical RSI](#from-evolution-to-physical-rsi)
- [The Boundary](#the-boundary)
- [Capability Map](#capability-map)
- [Harness Adaptation, Training, and Verification](#three-views-of-one-system)
- [Paper Catalog](#paper-catalog)
- [Open Questions](#open-questions)
- [License](#license)

> **Version note.** The sections below follow `IEEE_TPAMI__Physical_RSI-33.pdf` (12 October 2026).
> The opening introduction and badges are retained from the earlier README; their L1–L5 taxonomy,
> real-only grounding language, and bibliography counts should not be read as claims about this snapshot.
> The current framework and coverage are specified below.

---

<a id="the-boundary"></a>

## The Boundary <sub><a href="#readme-top">top</a></sub>

Physical RSI distinguishes the **execution system `M = (Θ, H)`**—models and their harness—from
its **improvement procedure `Φ = (Adapt, Train, Ver)`**. Improving task performance is not the
same as improving the procedure that produces future updates.

<p align="center">
  <a href="docs/figures/physical-rsi-v33-overview.png"><img src="docs/figures/physical-rsi-v33-overview.png" alt="Physical RSI architecture and L0–L5 framework" width="96%"></a>
</p>
<p align="center"><sub>Task execution, inherited improvement, and the L0–L5 framework.</sub></p>

<a id="capability-map"></a>

## Capability Map <sub><a href="#readme-top">top</a></sub>

The framework separates **what changes** from **where the retained gain transfers**:

- **L0:** no autonomous retained-improvement loop.
- **L1 / L3:** inherited execution-system updates improve the same task / transfer across tasks.
- **L2 / L4:** inherited improvement-procedure updates support same-task / cross-task improvement.
- **L5:** successive procedure revisions produce better subsequent improvements under matched
  budgets and protected cross-task evaluation—not merely a changed procedure.

<p align="center">
  <a href="docs/figures/physical-rsi-v33-update-targets-and-tasks.png"><img src="docs/figures/physical-rsi-v33-update-targets-and-tasks.png" alt="Capability versus meta-level updates, and task identity through skill sequences" width="100%"></a>
</p>
<p align="center"><sub>Update targets and task identity: a new scene alone does not establish a new task.</sub></p>

<a id="three-views-of-one-system"></a>

## Harness Adaptation, Training, and Verification <sub><a href="#readme-top">top</a></sub>

- **Harness adaptation:** update memory, skills, tools, and workflows using execution feedback.
- **Model training:** turn collected experience into retained model updates.
- **Safety and control:** constrain trials and reassess safeguards as the system changes.
- **Verification and evaluation:** decide which changes may be retained, then independently
  measure their later benefit.
- **Benchmarks:** assess task performance, robustness, feedback reliability, and development
  processes; see [Benchmarks and Evaluation Resources](#catalog-benchmarks).

<p align="center">
  <a href="docs/figures/physical-rsi-v33-verification-evaluation.png"><img src="docs/figures/physical-rsi-v33-verification-evaluation.png" alt="Candidate verification and independent evaluation" width="96%"></a>
</p>
<p align="center"><sub>Candidate verification within the improvement loop, with independent evaluation of its outcomes.</sub></p>

<a id="paper-catalog"></a>

## Paper Catalog <sub><a href="#readme-top">top</a></sub>

Browse **116 papers and resources** by research topic. Each work has one primary home;
categories are reading aids, not capability-level assignments.

<details>
<summary><strong>Browse by topic</strong></summary>

- [Agent Harnesses and Execution](#catalog-agent-harnesses)
  - [Memory and Knowledge Management](#harness-memory)
  - [Skill Libraries and Tool Construction](#harness-skills)
  - [Planning and Workflows](#harness-workflows)
  - [Failure Diagnosis and Execution Recovery](#harness-recovery)
- [Model Training and Adaptation](#catalog-model-training)
  - [Data Preparation and Generation](#training-data)
  - [Imitation Learning and Generalist Policies](#training-imitation)
  - [Reinforcement Learning and Autonomous Practice](#training-rl)
  - [World Models for Policy Learning](#training-world-models)
  - [Reward Models and Learning Feedback](#training-reward-models)
  - [Continual Adaptation and Knowledge Transfer](#training-transfer)
- [Self-Improvement and Meta-Optimization](#catalog-meta-improvement)
  - [Self-Modifying Systems and Recursive Improvement](#meta-recursive-systems)
  - [Harness and Memory-Construction Optimization](#meta-harness-optimization)
  - [Training Procedures, Curricula, and Algorithm Optimization](#meta-training-optimization)
- [Safety and Assurance](#catalog-safety)
  - [Safe Exploration and Constrained Learning](#safety-learning)
  - [Safe Transfer and Update Acceptance](#safety-transfer)
  - [Runtime Control and Failure Monitoring](#safety-runtime)
  - [Oversight and Integrity Protection](#safety-oversight)
- [Verification and Evaluation Methods](#catalog-verification)
  - [Robot Policy Verification and Candidate Selection](#verification-robot-policies)
  - [Learned Evaluators and Meta-Verification](#verification-learned-evaluators)
- [Benchmarks, Datasets, and Platforms](#catalog-benchmarks)
  - [Shared Robot Datasets](#benchmarks-datasets)
  - [Task and Long-Horizon Learning Benchmarks](#benchmarks-tasks)
  - [Robustness and Transfer Evaluation](#benchmarks-robustness)
  - [Real-Robot and Sim-and-Real Evaluation Platforms](#benchmarks-real-robot)
  - [Feedback and Reward Evaluation](#benchmarks-feedback)
  - [World-Model-Based Evaluation](#benchmarks-world-models)
  - [Robot Engineering Benchmarks](#benchmarks-engineering)
  - [Research Agent and Self-Improvement Benchmarks](#benchmarks-research-agents)

</details>

<a id="catalog-agent-harnesses"></a>

### Agent Harnesses and Execution

Memory, skills, tools, and workflows used during task execution. Methods that revise how these resources are built belong under [Self-Improvement and Meta-Optimization](#catalog-meta-improvement).

<a id="harness-memory"></a>

#### Memory and Knowledge Management

- [Know Your Body: A Harness for Direct and Self-Improving Robot Control with VLMs](https://arxiv.org/html/2609.28530v1) by Zeyu Lou et al. 2026.

<a id="harness-skills"></a>

#### Skill Libraries and Tool Construction

- [ASPIRE: Agentic Skills Discovery for Robotics](https://arxiv.org/abs/2607.00272) by Runyu Lu et al. 2026.
- [Self-Evolving Embodied Agents via Skill-Harness Evolution](https://arxiv.org/abs/2608.11350) by Peidong Wang et al. 2026.
- [Reconstruct, Practice, Go Real: Guided Self-Improvement for Embodied Agents](https://arxiv.org/abs/2610.02204) by Yen-Jen Wang et al. 2026.
- [Evolve Vision-Language-Action Model into an Agent with On-the-Fly Tool Use](https://arxiv.org/abs/2608.14047) by Yi Ding et al. 2026.
- [Code as Policies: Language Model Programs for Embodied Control](https://arxiv.org/abs/2209.07753) by Jacky Liang et al. 2022.

<a id="harness-workflows"></a>

#### Planning and Workflows

- [RoboFoundry: System-as-Policy Evolution for Self-Learning Embodied Agents](https://arxiv.org/html/2609.32862v1) by Jingsong Liang et al. 2026.
- [HarnessPAI: An Evolving Harness for Physical AI](https://arxiv.org/html/2609.29166v1) by Xin Wang et al. 2026.
- [Zetta: An Efficient Closed-Loop Embodied Harness for Self-Evolving Physical Intelligence](https://arxiv.org/abs/2608.16590) by Xin Ding et al. 2026.
- [Grounded Vision-Language Interpreter for Long-Horizon Bimanual Task and Motion Planning](https://arxiv.org/abs/2506.03270) by Jeremy Siburian et al. 2025.
- [Open-World Task and Motion Planning via Vision-Language Model Generated Constraints](https://arxiv.org/abs/2411.08253) by Nishanth Kumar et al. 2024.
- [Trust the PRoC3S: Solving Long-Horizon Robotics Problems with LLMs and Constraint Satisfaction](https://arxiv.org/abs/2406.05572) by Aidan Curtis et al. 2024.
- [Do As I Can, Not As I Say: Grounding Language in Robotic Affordances](https://arxiv.org/abs/2204.01691) by Michael Ahn et al. 2022.

<a id="harness-recovery"></a>

#### Failure Diagnosis and Execution Recovery

- [DoReMi: Grounding Language Model by Detecting and Recovering from Plan-Execution Misalignment](https://sites.google.com/view/doremi-paper) by Yanjiang Guo et al. 2024.
- [REFLECT: Summarizing Robot Experiences for Failure Explanation and Correction](https://arxiv.org/abs/2306.15724) by Zeyi Liu, Arpit Bahety, and Shuran Song. 2023.

<a id="catalog-robot-learning"></a>
<a id="catalog-learning-resources"></a>
<a id="catalog-model-training"></a>

### Model Training and Adaptation

Data preparation and learning methods for improving robot policies, world models, and reward models, including continual adaptation and knowledge transfer.

<a id="training-data"></a>

#### Data Preparation and Generation

- [Self-Evolving Learning for Embodied AI with Criticality Model](https://arxiv.org/abs/2607.28251) by Linxuan He et al. 2026.
- [FAR: Failure-Aware Retry for Test-Time Recovery and Continual Policy Improvement](https://arxiv.org/abs/2607.01111) by Haoran Hao et al. 2026.
- [GenSim2: Scaling Robot Data Generation with Multi-Modal and Reasoning LLMs](https://arxiv.org/abs/2410.03645) by Pu Hua et al. 2024.
- [RoboGen: Towards Unleashing Infinite Data for Automated Robot Learning via Generative Simulation](https://arxiv.org/abs/2311.01455) by Yufei Wang et al. 2024.

<a id="training-imitation"></a>

#### Imitation Learning and Generalist Policies

- [RoboCat: A Self-Improving Generalist Agent for Robotic Manipulation](https://openreview.net/forum?id=vsDnJ2WR4x) by Konstantinos Bousmalis et al. 2024.

<a id="training-rl"></a>

#### Reinforcement Learning and Autonomous Practice

- [Practice Makes Policies: Bootstrapping and Consolidating Robotic Capabilities from Zero Human Demonstrations](https://arxiv.org/abs/2607.26809) by Jialiang Li et al. 2026.
- [ConRFT: A Reinforced Fine-Tuning Method for VLA Models via Consistency Policy](https://arxiv.org/abs/2502.05450) by Yuhui Chen et al. 2025.
- [SELFI: Autonomous Self-Improvement with RL for Vision-Based Navigation around People](https://proceedings.mlr.press/v270/hirose25a.html) by Noriaki Hirose et al. 2025.
- [Autonomous Improvement of Instruction Following Skills via Foundation Models](https://arxiv.org/abs/2407.20635) by Zhiyuan Zhou et al. 2024.
- [Self-Improving Robots: End-to-End Autonomous Visuomotor Reinforcement Learning](https://proceedings.mlr.press/v229/sharma23b.html) by Archit Sharma et al. 2023.

<a id="training-world-models"></a>

#### World Models for Policy Learning

- [Motus2: A Self-Evolving General World Model for Dexterous Manipulation](https://arxiv.org/abs/2608.30237) by Hongzhe Bi et al. 2026.
- [Robot Self-Improvement via Human-Video Dynamics Models](https://arxiv.org/abs/2606.21406) by Hanzhi Chen et al. 2026.
- [RISE: Self-Improving Robot Policy with Compositional World Model](https://arxiv.org/abs/2602.11075) by Jiazhi Yang et al. 2026.

<a id="training-reward-models"></a>

#### Reward Models and Learning Feedback

- [DenseReward: Dense Reward Learning via Failure Synthesis for Robotic Manipulation](https://arxiv.org/abs/2607.13033) by Yu Fang et al. 2026.
- [SARM2: Multi-Task Stage Aware Reward Modeling for Self Improving Robotic Manipulation](https://arxiv.org/abs/2606.10305) by Qianzhong Chen et al. 2026.

<a id="training-transfer"></a>

#### Continual Adaptation and Knowledge Transfer

- [EmbodiRSI: Recursive Self-Improvement for Data-Efficient Robot Adaptation](https://arxiv.org/abs/2609.38905) by Haoran Lang et al. 2026.
- [F4R: Failure-Driven Recognition, Reconstruction, Refinement, and Redeployment for Continual Robot Self-Improvement](https://arxiv.org/abs/2609.35575v2) by Zhuoyuan Yu et al. 2026.
- [Robust Finetuning of Vision-Language-Action Robot Policies via Parameter Merging](https://arxiv.org/abs/2512.08333) by Yajat Yadav et al. 2026.

<a id="catalog-meta-improvement"></a>

### Self-Improvement and Meta-Optimization

Self-modifying systems and methods for optimizing resource construction, training procedures, and algorithms. Digital precedents are included without implying physical grounding or verified recursive gain.

<a id="meta-recursive-systems"></a>

#### Self-Modifying Systems and Recursive Improvement

- [Hyperagents](https://arxiv.org/html/2603.19461v1) by Jenny Zhang et al. 2026.
- [Darwin Gödel Machine: Open-Ended Evolution of Self-Improving Agents](https://arxiv.org/abs/2505.22954) by Jenny Zhang et al. 2025.
- [Godel Agent: A Self-Referential Agent Framework for Recursively Self-Improvement](https://aclanthology.org/2025.acl-long.1354/) by Xunjian Yin et al. 2025.
- [Self-Taught Optimizer (STOP): Recursively Self-Improving Code Generation](https://arxiv.org/pdf/2310.02304v3) by Eric Zelikman et al. 2024.
- [Godel Machines: Fully Self-Referential Optimal Universal Self-Improvers](https://doi.org/10.1007/978-3-540-68677-4_7) by Jurgen Schmidhuber. 2007.

<a id="meta-harness-optimization"></a>

#### Harness and Memory-Construction Optimization

- [SBCO: Self-Supervised, Verifier-Grounded Harness Optimization for Planning Agents](https://arxiv.org/abs/2608.10157) by Vivek Kulkarni et al. 2026.
- [VERSE: Verified Self-Evolving Optimizer for Agent Harnesses](https://arxiv.org/abs/2610.02616v1) by Zekai Wang et al. 2026.
- [MemSkill: Learning and Evolving Memory Skills for Self-Evolving Agents](https://arxiv.org/abs/2602.02474v2) by Haozhen Zhang et al. 2026.

<a id="meta-training-optimization"></a>

#### Training Procedures, Curricula, and Algorithm Optimization

- [ENPIRE: Agentic Robot Policy Self-Improvement in the Real World](https://arxiv.org/abs/2606.19980) by Wenli Xiao et al. 2026.
- [HARBOR: A Harness Framework for Agentic Robot Reinforcement Learning](https://arxiv.org/abs/2606.08610) by Zechu Li et al. 2026.
- [EvoTrainer: Co-Evolving LLM Policies and Training Harnesses for Autonomous Agentic Reinforcement Learning](https://arxiv.org/abs/2606.03108) by Guhong Chen et al. 2026.
- [GEAR: Genetic AutoResearch for Agentic Code Evolution](https://arxiv.org/abs/2605.13874) by Ahmadreza Jeddi et al. 2026.
- [Learning to Discover at Test Time](https://arxiv.org/abs/2601.16175) by Mert Yuksekgonul et al. 2026.
- [CALM: Co-Evolution of Algorithms and Language Model for Automatic Heuristic Design](https://arxiv.org/abs/2505.12285) by Ziyao Huang et al. 2025.
- [Algorithm Discovery with LLMs: Evolutionary Search Meets Reinforcement Learning](https://arxiv.org/abs/2504.05108) by Anja Surina et al. 2025.
- [DrEureka: Language Model Guided Sim-to-Real Transfer](https://arxiv.org/abs/2406.01967) by Yecheng Jason Ma et al. 2024.
- [Eureka: Human-Level Reward Design via Coding Large Language Models](https://arxiv.org/abs/2310.12931) by Yecheng Jason Ma et al. 2024.

<a id="catalog-safety"></a>

### Safety and Assurance

Safeguards across learning, update acceptance, execution, and oversight. Failure detection and evaluation-integrity checks are distinct from guarantees of physical safety.

<a id="safety-learning"></a>

#### Safe Exploration and Constrained Learning

- [PACT: Self-Evolving Physical Safety Alignment for Diffusion Policies in Embodied Manipulation](https://arxiv.org/abs/2606.08414) by Lingxuan Wu et al. 2026.
- [Safe Continual Domain Adaptation after Sim2Real Transfer of Reinforcement Learning Policies in Robotics](https://arxiv.org/abs/2503.10949) by Josip Josifovski et al. 2025.
- [Constrained Policy Optimization](https://proceedings.mlr.press/v70/achiam17a.html) by Joshua Achiam et al. 2017.

<a id="safety-transfer"></a>

#### Safe Transfer and Update Acceptance

- [High Confidence Policy Improvement](https://proceedings.mlr.press/v37/thomas15.html) by Philip S. Thomas et al. 2015.

<a id="safety-runtime"></a>

#### Runtime Control and Failure Monitoring

- [VLA-FAIL: Efficient Task Failure Detection for Finetuned Vision-Language-Action Models](https://arxiv.org/abs/2606.21386) by Florian Seligmann et al. 2026.
- [ROBOGATE: Adaptive Failure Discovery for Safe Robot Policy Deployment via Two-Stage Boundary-Focused Sampling](https://arxiv.org/abs/2603.22126) by Azuki Kim. 2026.
- [SAFE: Multitask Failure Detection for Vision-Language-Action Models](https://arxiv.org/abs/2506.09937) by Qiao Gu et al. 2025.
- [Unpacking Failure Modes of Generative Policies: Runtime Monitoring of Consistency and Progress](https://proceedings.mlr.press/v270/agia25a.html) by Christopher Agia et al. 2025.
- [Code-as-Monitor: Constraint-Aware Visual Programming for Reactive and Proactive Robotic Failure Detection](https://arxiv.org/abs/2412.04455) by Enshen Zhou et al. 2024.
- [Control Barrier Function Based Quadratic Programs for Safety Critical Systems](https://doi.org/10.1109/TAC.2016.2638961) by Aaron D. Ames et al. 2017.

<a id="safety-oversight"></a>

#### Oversight and Integrity Protection

- [BenchShield: Formal Model-Backed Instrumentation for Reward Integrity in LLM-Agent Evaluation Infrastructure](https://arxiv.org/abs/2609.11028) by Shenghan Zheng et al. 2026.
- [Preventing Undesirable Behavior of Intelligent Machines](https://doi.org/10.1126/science.aag3311) by Philip S. Thomas et al. 2019.

<a id="catalog-verification"></a>

### Verification and Evaluation Methods

Methods for constructing and using verifiers or evaluators. Resources for testing their reliability are listed under [Benchmarks, Datasets, and Platforms](#catalog-benchmarks).

<a id="verification-robot-policies"></a>

#### Robot Policy Verification and Candidate Selection

- [Visual Verification Enables Inference-Time Steering and Autonomous Policy Improvement](https://arxiv.org/abs/2606.18247) by Mingtong Zhang and Dhruv Shah. 2026.
- [No Free Checker: A Survey of Verifiers for Robot Policies](https://arxiv.org/abs/2609.09250) by Yang Wan et al. 2026.
- [RoVer: Robot Reward Model as Test-Time Verifier for Vision-Language-Action Model](https://arxiv.org/abs/2510.10975) by Mingtong Dai et al. 2025.
- [RoboMonkey: Scaling Test-Time Sampling and Verification for Vision-Language-Action Models](https://arxiv.org/abs/2506.17811) by Jacky Kwok et al. 2025.

<a id="verification-learned-evaluators"></a>

#### Learned Evaluators and Meta-Verification

- [Self-Trained Verification for Training- and Test-Time Self-Improvement](https://arxiv.org/abs/2605.30290) by Chen Henry Wu and Aditi Raghunathan. 2026.
- [Self-Taught Evaluators](https://arxiv.org/abs/2408.02666) by Tianlu Wang et al. 2024.
- [Meta-Rewarding Language Models: Self-Improving Alignment with LLM-as-a-Meta-Judge](https://arxiv.org/abs/2407.19594) by Tianhao Wu et al. 2024.

<a id="catalog-benchmarks"></a>

### Benchmarks, Datasets, and Platforms

Shared datasets, task suites, evaluation protocols, and supporting platforms. Papers contributing both methods and evaluation resources have one primary entry here, with resource aliases retained where applicable.

<a id="benchmarks-datasets"></a>

#### Shared Robot Datasets

- [DROID: A Large-Scale In-The-Wild Robot Manipulation Dataset](https://www.roboticsproceedings.org/rss20/p120.html) by Alexander Khazatsky et al. 2024. *Shared dataset cited in the v33 introduction; not a Table 4 benchmark.*
- [Open X-Embodiment: Robotic Learning Datasets and RT-X Models](https://arxiv.org/abs/2310.08864) by the Open X-Embodiment Collaboration. 2024.

<a id="benchmarks-tasks"></a>

#### Task and Long-Horizon Learning Benchmarks

- [RoboCasa365: A Large-Scale Simulation Framework for Training and Benchmarking Generalist Robots](https://arxiv.org/abs/2603.04356) by Soroush Nasiriany et al. 2026.
- [RoboLab: A High-Fidelity Simulation Benchmark for Analysis of Task Generalist Policies](https://arxiv.org/abs/2604.09860) by Jenai Xuning Yang et al. 2026.
- [EmbodiedBench: Comprehensive Benchmarking Multi-modal Large Language Models for Vision-Driven Embodied Agents](https://proceedings.mlr.press/v267/yang25f.html) by Rui Yang et al. 2025.
- [ManiSkill3: GPU Parallelized Robotics Simulation and Rendering for Generalizable Embodied AI](https://arxiv.org/abs/2410.00425) by Stone Tao et al. 2025.
- [Towards Generalizable Vision-Language Robotic Manipulation: A Benchmark and LLM-guided 3D Policy](https://arxiv.org/abs/2410.01345) by Ricardo Garcia et al. 2025. *Benchmark resource: GemBench; discussed in v33 Section 2 (p. 10).*
- [VLABench: A Large-Scale Benchmark for Language-Conditioned Robotics Manipulation with Long-Horizon Reasoning Tasks](https://openaccess.thecvf.com/content/ICCV2025/html/Zhang_VLABench_A_Large-Scale_Benchmark_for_Language-Conditioned_Robotics_Manipulation_with_Long-Horizon_ICCV_2025_paper.html) by Shiduo Zhang et al. 2025.
- [BEHAVIOR-1K: A Human-Centered, Embodied AI Benchmark with 1,000 Everyday Activities and Realistic Simulation](https://arxiv.org/abs/2403.09227) by Chengshu Li et al. 2024.
- [LIBERO: Benchmarking Knowledge Transfer for Lifelong Robot Learning](https://arxiv.org/abs/2306.03310) by Bo Liu et al. 2023.
- [VIMA: Robot Manipulation with Multimodal Prompts](https://proceedings.mlr.press/v202/jiang23b.html) by Yunfan Jiang et al. 2023. *Benchmark resource: VIMA-Bench.*
- [CALVIN: A Benchmark for Language-Conditioned Policy Learning for Long-Horizon Robot Manipulation Tasks](https://arxiv.org/abs/2112.03227) by Oier Mees et al. 2022.
- [What Matters in Learning from Offline Human Demonstrations for Robot Manipulation](https://arxiv.org/abs/2108.03298) by Ajay Mandlekar et al. 2021. *Resource: robomimic.*
- [Meta-World: A Benchmark and Evaluation for Multi-Task and Meta Reinforcement Learning](https://proceedings.mlr.press/v100/yu20a.html) by Tianhe Yu et al. 2020.
- [robosuite: A Modular Simulation Framework and Benchmark for Robot Learning](https://arxiv.org/abs/2009.12293) by Yuke Zhu et al. 2020.
- [RLBench: The Robot Learning Benchmark & Learning Environment](https://arxiv.org/abs/1909.12271) by Stephen James et al. 2019.

<a id="benchmarks-robustness"></a>

#### Robustness and Transfer Evaluation

- [RoboTwin 2.0: A Scalable Data Generator and Benchmark with Strong Domain Randomization for Robust Bimanual Robotic Manipulation](https://proceedings.mlr.press/v306/chen26j.html) by Tianxing Chen et al. 2026.
- [VLA-Arena: An Open-Source Framework for Benchmarking Vision-Language-Action Models](https://proceedings.mlr.press/v306/zhang26cp.html) by Borong Zhang et al. 2026.
- [LIBERO-Plus: In-depth Robustness Analysis of Vision-Language-Action Models](https://arxiv.org/abs/2510.13626) by Senyu Fei et al. 2025.
- [LIBERO-PRO: Towards Robust and Fair Evaluation of Vision-Language-Action Models Beyond Memorization](https://arxiv.org/abs/2510.03827) by Xueyang Zhou et al. 2025.
- [REALM: A Real-to-Sim Validated Benchmark for Generalization in Robotic Manipulation](https://arxiv.org/abs/2512.19562) by Martin Sedlacek et al. 2025.
- [RoboTwin: Dual-Arm Robot Benchmark with Generative Digital Twins](https://arxiv.org/abs/2504.13059) by Yao Mu et al. 2025.
- [Evaluating Real-World Robot Manipulation Policies in Simulation](https://arxiv.org/abs/2405.05941) by Xuanlin Li et al. 2024. *Evaluation resource: SIMPLER.*
- [THE COLOSSEUM: A Benchmark for Evaluating Generalization for Robotic Manipulation](https://arxiv.org/abs/2402.08191) by Wilbert Pumacay et al. 2024.

<a id="benchmarks-real-robot"></a>

#### Real-Robot and Sim-and-Real Evaluation Platforms

- [RoboDojo: A Unified Sim-and-Real Benchmark for Comprehensive Evaluation of Generalist Robot Manipulation Policies](https://arxiv.org/abs/2607.04434) by Tianxing Chen et al. 2026.
- [AutoEval: Autonomous Evaluation of Generalist Robot Manipulation Policies in the Real World](https://arxiv.org/abs/2503.24278v1) by Zhiyuan Zhou et al. 2025.
- [RoboArena: Distributed Real-World Evaluation of Generalist Robot Policies](https://proceedings.mlr.press/v305/atreya25a.html) by Pranav Atreya et al. 2025.

<a id="benchmarks-feedback"></a>

#### Feedback and Reward Evaluation

- [FailBench: How Reliable Are VLMs at Judging Robot Task Success?](https://arxiv.org/abs/2609.03611v1) by Zaruhi Navasardyan et al. 2026.
- [Robometer: Scaling General-Purpose Robotic Reward Models via Trajectory Comparisons](https://arxiv.org/abs/2603.02115) by Anthony Liang et al. 2026. *Benchmark resource in v33: RBM-EVAL.*
- [RoboReward: General-Purpose Vision-Language Reward Models for Robotics](https://arxiv.org/abs/2601.00675) by Tony Lee et al. 2026. *Benchmark resource in v33: RoboRewardBench.*

<a id="benchmarks-world-models"></a>

#### World-Model-Based Evaluation

- [dWorldEval: Scalable Robotic Policy Evaluation via Discrete Diffusion World Model](https://arxiv.org/abs/2604.22152) by Yaxuan Li et al. 2026.
- [GigaWorld-1: A Roadmap to Build World Models for Robot Policy Evaluation](https://arxiv.org/abs/2607.02642) by the GigaWorld Team. 2026.
- [SC3-Eval: Evaluating Robot Foundation Models via Self-Consistent Video Generation](https://arxiv.org/abs/2606.18610) by Wei-Cheng Tseng et al. 2026.
- [WorldEval: World Model as Real-World Robot Policies Evaluator](https://arxiv.org/abs/2505.19017) by Yaxuan Li et al. 2025.

<a id="benchmarks-engineering"></a>

#### Robot Engineering Benchmarks

- [CaP-X: A Framework for Benchmarking and Improving Coding Agents for Robot Manipulation](https://proceedings.mlr.press/v306/fu26u.html) by Letian Fu et al. 2026. *Benchmark resource in v33: CaP-Bench.*
- [From Digital to Physical: Digital Agents as Autonomous Coaches for Physical Intelligence](https://arxiv.org/abs/2601.21570) by Zixing Lei et al. 2026. *Associated with the EmboCoach-Bench entry in the manuscript; preserve the paper/benchmark version distinction.*
- [RLE-Bench: A Qualifying Exam for Coding Agents as Robot Learning Engineers](https://arxiv.org/abs/2609.34210) by Haitong Ma et al. 2026.

<a id="benchmarks-research-agents"></a>

#### Research Agent and Self-Improvement Benchmarks

- [AI4AI-Bench: Benchmarking LLM Agents in Algorithmic Design for Recursive Self-Improvement](https://arxiv.org/abs/2608.20318) by Yizhe Chi et al. 2026.
- [HarnessDev: Can LLMs Create and Evolve Their Own Agent Harness?](https://arxiv.org/abs/2609.01437) by Yuhao Wu et al. 2026.
- [PAST-Bench: Benchmarking the Foundations of Recursive Self-Improvement in Personal Agents](https://arxiv.org/abs/2608.04003) by Shuhan Xue et al. 2026.
- [RSI-Exam: Benchmarking Recursive Self-Improvement through Executable Research](https://github.com/aiming-lab/RSI-Exam) by RSI-Exam Team. 2026. *Repository resource cited by the manuscript.*
- [RSIBench-Data: Benchmarking Data-Centric Research for Recursive Self-Improvement](https://arxiv.org/abs/2607.25886) by Fanqing Meng et al. 2026.
- [MLGym: A New Framework and Benchmark for Advancing AI Research Agents](https://arxiv.org/abs/2502.14499) by Deepak Nathani et al. 2025. *Benchmark resource: MLGym-Bench.*
- [MLRC-Bench: Can Language Agents Solve Machine Learning Research Challenges?](https://arxiv.org/abs/2504.09702) by Yunxiang Zhang et al. 2025.
- [RE-Bench: Evaluating Frontier AI R&D Capabilities of Language Model Agents against Human Experts](https://proceedings.mlr.press/v267/wijk25a.html) by Hjalmar Wijk et al. 2025.
- [MLAgentBench: Evaluating Language Agents on Machine Learning Experimentation](https://proceedings.mlr.press/v235/huang24y.html) by Qian Huang et al. 2024.
- [MLE-bench: Evaluating Machine Learning Agents on Machine Learning Engineering](https://arxiv.org/abs/2410.07095) by Jun Shern Chan et al. 2024.

<a id="open-questions"></a>

## Open Questions <sub><a href="#readme-top">top</a></sub>

Section 7 identifies open problems beyond autonomous execution and learning:

- **Reliable learning signals:** partial and noisy physical feedback can compound errors across generations.
- **Cross-component attribution:** similar failures may originate in perception, skills, orchestration, training, or their interactions.
- **Cumulative knowledge:** skills and improvement histories must remain usable as interfaces and physical conditions change.
- **Safety under evolving procedures:** inherited revisions may invalidate earlier assumptions, safeguards, or guarantees.
- **Reward hacking and leakage:** repeated judgments can become optimization targets instead of independent evidence.
- **Verified recursive gain:** successive procedures need controlled comparisons of the later across-task improvements they produce.
- **Affordable physical meta-updates:** simulation, imagination, logged experience, and real trials have different costs and grounding limits.
- **Comparable autonomy:** setup, resets, labeling, takeovers, editing, and update selection need separate records.

These are gaps scoped to the reviewed manuscript, not claims that no related work exists elsewhere.

<a id="license"></a>

## License <sub><a href="#readme-top">top</a></sub>

This repository is released under the [MIT License](LICENSE). Linked papers and third-party
materials remain subject to their respective licenses.
