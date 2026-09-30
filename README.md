<a id="readme-top"></a>

<div align="center">

<h1><em>Physical RSI</em></h1>

<p align="center"><strong>Physical Recursive Self-Improvement</strong></p>

<p align="center">A paper-aligned, evidence-auditable map of recursive improvement in embodied systems.</p>

<p align="center">
  <a href="#paper-catalog"><img src="https://img.shields.io/badge/featured_catalog-65_papers-2563eb?style=flat-square" alt="65 papers in the featured catalog"></a>
  <a href="docs/paper-reference-index.md"><img src="https://img.shields.io/badge/bibliography-102%2F102-0f766e?style=flat-square" alt="102 of 102 unique paper references indexed"></a>
  <a href="#capability-map"><img src="https://img.shields.io/badge/taxonomy-L1--L5-7c3aed?style=flat-square" alt="L1 to L5 capability taxonomy"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/license-MIT-475569?style=flat-square" alt="MIT License"></a>
</p>

<p align="center">
  <a href="#reading-paths">Reading paths</a> &nbsp;|&nbsp;
  <a href="#scope-and-relevance">Scope</a> &nbsp;|&nbsp;
  <a href="#capability-map">L1-L5</a> &nbsp;|&nbsp;
  <a href="#featured-evidence-register">Evidence register</a> &nbsp;|&nbsp;
  <a href="#three-views-of-one-system">Research map</a> &nbsp;|&nbsp;
  <a href="#paper-catalog">Paper catalog</a> &nbsp;|&nbsp;
  <a href="docs/paper-reference-index.md">All references</a>
</p>

</div>

Physical RSI asks a narrower question than whether robots can keep learning:

> **Can evidence from physical interaction improve the process that produces the robot's next
> improvement?**

A robot may collect more data, recover from a failed grasp, or fine-tune a policy after deployment.
Those are useful forms of adaptation, but they are not recursive by themselves. Recursion begins
when a retained change reaches the mechanism that generates, evaluates, or selects later updates.
It becomes *physical* when real interaction has a causal role in deciding what mechanism changes or
survives.

This repository follows the evidence boundaries of the **Physical Recursive Self-Improvement**
paper. It is a reading map, not a leaderboard: labels such as "self-improving," "autonomous," or
"lifelong" are not treated as evidence on their own.

<a id="latest-update"></a>

## Latest Update <sub><a href="#readme-top">top</a></sub>

**2026-09-30 - Evidence audit added.** The repository now separates a featured 65-paper catalog
from the complete 102-work bibliography, adds reading paths and scope rules, and records grounding,
updated objects, and evidence boundaries for representative physical-improvement workflows.

<a id="reading-paths"></a>

## Reading Paths <sub><a href="#readme-top">top</a></sub>

The catalog is designed for reference. These shorter routes are better starting points:

| Goal | Suggested route |
| --- | --- |
| **Understand the claim** | Read [The boundary](#the-boundary), then compare inheritance, persistent improvement, structural recursion, and beneficial recursion. |
| **Place a physical workflow** | Use the [L1-L5 capability map](#capability-map), then inspect the [featured evidence register](#featured-evidence-register). |
| **Study autonomous robot learning** | Start with [SELFI](https://proceedings.mlr.press/v270/hirose25a.html), [VERITAS](https://arxiv.org/abs/2606.18247), and [SOAR](https://arxiv.org/abs/2407.20635), then browse [Training](#2-training). |
| **Study mechanism improvement** | Read [ENPIRE](https://arxiv.org/abs/2606.19980) beside the digital precedents [Darwin Godel Machine](https://arxiv.org/abs/2505.22954) and [HyperAgents](https://arxiv.org/abs/2603.19461). |
| **Study trustworthy recursion** | Follow [Verification](#3-verification), the beneficial-recursion protocol, and the verification papers in the [catalog](#verification-evaluation-and-safety). |
| **Audit coverage** | Check the [complete reference index](docs/paper-reference-index.md) and [data provenance](#data-provenance-and-validation). |

<a id="scope-and-relevance"></a>

## Scope and Relevance <sub><a href="#readme-top">top</a></sub>

This repository includes several kinds of work because the paper uses them for different parts of
the argument. Inclusion is not a claim that every paper demonstrates Physical RSI.

| Scope | Inclusion rule | What it establishes |
| --- | --- | --- |
| **Physical capability evidence** | A reported workflow uses robot interaction to support a specific L1-L5 claim. | Evidence only for the marked capability and experimental regime. |
| **Physical supporting method** | A method contributes execution, training, memory, reward, or verification machinery to an embodied improvement loop. | A component of the loop, not necessarily recursion. |
| **Simulation mechanism** | A simulated system changes rewards, curricula, skills, policies, or training artifacts. | A mechanism precedent without real-world physical grounding. |
| **Digital RSI precedent** | A software or agent system revises an inherited improvement process. | Structural or evaluation precedent without embodied grounding. |
| **L5 candidate** | Physical evidence revises and reuses a mechanism that governs later improvement. | Structural Physical RSI; strict L5 still requires a matched beneficial-recursion comparison. |

Standard robot execution, one-off fine-tuning, or a better successor alone does not establish
recursive improvement. Likewise, a paper's use of "self-improving" or "self-evolving" is never
treated as sufficient evidence.

<a id="improvement-loop-anatomy"></a>

## Improvement-Loop Anatomy <sub><a href="#readme-top">top</a></sub>

Every claimed workflow can be read through the same closed loop:

> **physical experience -> evaluation and credit -> candidate update -> verification and consolidation -> successor re-entry**

| Component | Audit question |
| --- | --- |
| **System boundary** | What counts as the changing self: policy, memory, verifier, training code, or the wider embodied system? |
| **Experience** | Which real, simulated, or imagined interaction supplies evidence for the change? |
| **Updated object** | What persists: weights, data, skills, reward, verifier, harness, or improvement mechanism? |
| **Improver** | What proposes the candidate, and is that procedure itself fixed or revisable? |
| **Verifier** | Who controls admission or release, and is the evidence independent of the candidate? |
| **Inheritance** | Is the accepted change actually reused in a later episode or improvement cycle? |
| **Later-round effect** | Does the evidence show recovery, persistent learning, transfer, structural recursion, or beneficial recursion? |

Three questions catch most overclaims: **Where does the loop close? What is updated and inherited?
Which improvement decisions remain external?**

<a id="evidence-tags"></a>

## How to Read the Evidence Tags <sub><a href="#readme-top">top</a></sub>

The featured register uses four independent fields:

| Field | Values used here |
| --- | --- |
| **Capability** | `L1` to `L5 candidate`; levels are non-exclusive evidence claims, not quality rankings. |
| **Grounding** | `Physical`, `Hybrid`, `Simulation`, or `Digital`; this records where the relevant evidence comes from. |
| **Updated object** | Policy, data, memory, skill, reward, verifier, model, harness, training code, or improvement mechanism. |
| **Status** | `Supported`, `Candidate`, or `Context`; this separates demonstrated evidence from a useful precedent. |

The four fields should not be collapsed. A physically deployed system can still have a fixed
improver, and a structurally recursive digital system can still lack physical grounding.

<a id="the-boundary"></a>

## The Boundary <sub><a href="#readme-top">top</a></sub>

The relevant "self" is the complete embodied improvement system: policy, safety guard, verifier,
memory, data pipeline, training procedure, and the infrastructure that decides which changes
persist. Deploying a fixed improvement loop on a robot is not enough.

Four claims that are often collapsed should be kept separate:

| Claim | What must be shown |
| --- | --- |
| **Inheritance** | A change from one cycle is retained and used later. |
| **Persistent improvement** | The retained change contributes to better later performance. |
| **Structural recursion** | The retained change modifies the process that produces later updates. |
| **Beneficial recursion** | Under matched conditions, the revised process produces better successors than the process it replaced. |

<p align="center">
  <a href="docs/figures/beneficial-recursion.jpg"><img src="docs/figures/beneficial-recursion.jpg" alt="From inheritance to beneficial recursion, with a matched improver comparison" width="96%"></a>
</p>
<p align="center"><sub><strong>Figure 14.</strong> Beneficial recursion requires testing the improver, not only its latest successor.</sub></p>

Structural recursion establishes the recursive form. Beneficial recursion establishes that the
recursive change actually helped. A persuasive comparison starts from the same system, uses the
same task conditions and protected evaluation criterion, and accounts for robot trials, resets,
hardware wear, compute, search, and human effort.

<a id="capability-map"></a>

## Capability Map <sub><a href="#readme-top">top</a></sub>

L1-L5 are **independent evidence claims**, not a maturity ladder. A workflow may support several
capabilities, and a higher number does not silently establish the levels below it. Classification
applies to the demonstrated workflow, not to the title of a paper.

<p align="center">
  <a href="docs/figures/capability-levels.png"><img src="docs/figures/capability-levels.png" alt="Five capability categories from human-supported improvement to physically grounded mechanism revision" width="100%"></a>
</p>
<p align="center"><sub><strong>Figure 3.</strong> Five capability categories of physical self-improvement.</sub></p>

| Capability | Deciding question | Representative evidence |
| --- | --- | --- |
| **L1: Human-supported improvement** | Does a person supply the corrective information that determines what changes? | [ConRFT](https://arxiv.org/abs/2502.05450) learns from robot trajectories containing operator corrections. |
| **L2: Autonomous error recognition and recovery** | Does the system detect an unsatisfactory execution and choose how to recover? | [DoReMi](https://sites.google.com/view/doremi-paper) detects task-constraint violations and replans; [REFLECT](https://arxiv.org/abs/2306.15724) explains failures and proposes repairs. |
| **L3: Autonomous learning across episodes** | Does physical experience produce a system-directed, retained change used later? | [SELFI](https://proceedings.mlr.press/v270/hirose25a.html) improves navigation through autonomous practice; [VERITAS](https://arxiv.org/abs/2606.18247) returns verified rollouts to policy training. |
| **L4: Transfer of acquired experience** | Is the contribution of prior experience demonstrated in another task, scene, environment, or embodiment? | [SOAR](https://arxiv.org/abs/2407.20635) isolates cross-scene experience; [ASPIRE](https://arxiv.org/abs/2607.00272) retrieves discovered skills for real-robot programming. |
| **L5: Physically grounded mechanism improvement** | Does physical evidence revise an inherited improvement mechanism, and does that mechanism produce better later improvements? | [ENPIRE](https://arxiv.org/abs/2606.19980) revises and reuses robot-training code, making it an important **L5 candidate**. It does not yet provide the matched improver comparison required for confirmed L5. |

The paper finds strong evidence for the lower capabilities and early evidence for physically grounded
mechanism revision. It does **not** identify a reviewed physical workflow that conclusively
demonstrates strict, beneficial L5.

<a id="featured-evidence-register"></a>

## Featured Evidence Register <sub><a href="#readme-top">top</a></sub>

This compact register makes the classification decision inspectable. Capability, grounding, and
updated object are recorded independently; the final column states the main evidential limit rather
than repeating the paper's abstract claim.

| Workflow | Capability | Grounding | Updated object | Status and boundary |
| --- | --- | --- | --- | --- |
| [ConRFT](https://arxiv.org/abs/2502.05450) | `L1` | `Physical` | Policy, critic, replay data | **Supported:** operator corrections determine the learning signal. |
| [DoReMi](https://sites.google.com/view/doremi-paper) | `L2` | `Hybrid` | Plan, failure detector | **Supported:** recovery is online; detector transfer is offline. |
| [REFLECT](https://arxiv.org/abs/2306.15724) | `L2 candidate` | `Physical` | Explanation, repair plan | **Candidate:** physical failures inform recovery, but the autonomy claim depends on the evaluated setup. |
| [SELFI](https://proceedings.mlr.press/v270/hirose25a.html) | `L3` | `Physical` | Policy, critic | **Supported:** autonomous practice produces retained cross-episode learning. |
| [VERITAS](https://arxiv.org/abs/2606.18247) | `L3` | `Physical` | Policy, verified data | **Supported:** verified real-world rollouts return to policy training. |
| [RISE](https://arxiv.org/abs/2602.11075) | `L3 candidate` | `Hybrid` | Policy, dynamics, value | **Candidate:** physical grounding is followed by imagined refinement. |
| [SOAR](https://arxiv.org/abs/2407.20635) | `L3`, `L4` | `Physical` | Policy, robot data | **Supported:** persistent learning and cross-scene transfer are evaluated. |
| [Robometer](https://arxiv.org/abs/2603.02115) | `L4` | `Physical` | Reward model, target policies | **Supported:** a transferred reward model supplies feedback for target policies. |
| [ASPIRE](https://arxiv.org/abs/2607.00272) | `L4` | `Hybrid` | Programs, repair skills | **Supported:** simulation-discovered skills are retrieved for real-robot programs. |
| [ENPIRE](https://arxiv.org/abs/2606.19980) | `L5 candidate` | `Physical` | Training code, recipes | **Candidate:** the mechanism is revised and reused, but beneficial recursion is not isolated under matched conditions. |

The register is intentionally selective. It identifies representative evidence needed to understand
the taxonomy; the [paper catalog](#paper-catalog) provides broader reading coverage, and the
[reference index](docs/paper-reference-index.md) records every unique work cited by the manuscript.

<a id="three-views-of-one-system"></a>

## Three Views of One System <sub><a href="#readme-top">top</a></sub>

Agent participation, training, and verification are complementary views of the same improvement
system. The first asks what an agent's output controls; the second asks how experience becomes a
persistent update; the third asks what the system is allowed to carry forward.

<p align="center">
  <a href="docs/figures/research-landscape.png"><img src="docs/figures/research-landscape.png" alt="Physical RSI research landscape across agent participation, training, and verification" width="82%"></a>
</p>
<p align="center"><sub><strong>Figure 5.</strong> The paper's research landscape and representative systems.</sub></p>

### 1. Agent participation

Agent roles are classified by the later use of their outputs, not by whether those outputs are code,
weights, or text.

| Loop | What the output controls | Representative work |
| --- | --- | --- |
| **Loop 1: Task execution** | The current task: specification, planning, tool use, execution, or outcome interpretation. | [SayCan](https://arxiv.org/abs/2204.01691), [Code as Policies](https://arxiv.org/abs/2209.07753), [Code-as-Monitor](https://arxiv.org/abs/2412.04455) |
| **Loop 2: Capability improvement** | A harness or model capability used in later tasks. | [SOAR](https://arxiv.org/abs/2407.20635), [RoboGen](https://arxiv.org/abs/2311.01455), [DrEureka](https://arxiv.org/abs/2406.01967), [SHAPER](https://arxiv.org/abs/2608.11350) |
| **Loop 3: Meta-improvement** | The procedure that produces or selects future capability improvements. | [ENPIRE](https://arxiv.org/abs/2606.19980), [EvoTrainer](https://arxiv.org/abs/2606.03108), [HyperAgents](https://arxiv.org/abs/2603.19461), [Darwin Godel Machine](https://arxiv.org/abs/2505.22954) |

A reward written for one training run is a Loop 2 input. Changing the procedure that generates or
selects rewards belongs to Loop 3. Digital and simulation studies clarify this boundary, but they do
not become evidence of Physical RSI without physical grounding and inherited use in the same
workflow.

### 2. Training

Training is a continuing, gated process rather than a one-off offline stage:

> **experience collection -> evaluation and credit -> parameter update -> verification and consolidation**

The main architectural substrates expose different objects to this loop:

- **Causal VLA Transformers:** [SARM2](https://arxiv.org/abs/2606.10305) couples stage estimation and value learning to produce dense progress feedback.
- **Unified world-action models:** [Motus2](https://arxiv.org/abs/2608.30237) shares policy, simulator, and evaluator interfaces; [RISE](https://arxiv.org/abs/2602.11075) separates dynamics from progress evaluation for imagined RL.
- **Video-generative world models:** [SC3-Eval](https://arxiv.org/abs/2606.18610) evaluates policies through dynamics, cross-view, and test-time consistency.
- **Constrained diffusion post-training:** [PACT](https://arxiv.org/abs/2606.08414) aligns a pretrained policy under safety and task-progress constraints.

Data selection matters as much as generation. Failures must be represented, imagined experience
must remain calibrated to the real world, and protected evaluation data must not leak into the
self-evolving loop. [FAR](https://arxiv.org/abs/2607.01111), for example, attributes failures to
action blocks and returns successful recoveries to training.

### 3. Verification

Verification enters the loop at three different points:

1. **Behavior verification:** should the current action or trajectory continue?
2. **Data admission:** should this experience enter memory or training?
3. **Update release:** should the resulting change become part of the persistent system?

A trajectory score is not an update-release test. Release may also require retention tests,
out-of-distribution evaluation, safety checks, and evidence that old capabilities have not regressed.
[Robometer](https://arxiv.org/abs/2603.02115), [WorldEval](https://arxiv.org/abs/2505.19017),
[RoboArena](https://arxiv.org/abs/2506.18123), and [SC3-Eval](https://arxiv.org/abs/2606.18610)
cover different parts of this problem.

Two forms of independence matter. **Control independence** prevents a candidate from choosing,
modifying, or bypassing its evaluator. **Information independence** prevents repeated feedback from
turning a protected criterion into another optimization target. More judges do not create independent
evidence when they share the same blind spot.

<a id="paper-catalog"></a>

## Paper Catalog <sub><a href="#readme-top">top</a></sub>

The list below follows the compact citation style used by research-map repositories: linked title,
authors, and year. Papers are grouped by their primary role in the Physical RSI argument; some
support more than one perspective. See the [complete paper reference index](docs/paper-reference-index.md)
for all 102 unique works cited in the manuscript.

### Physical improvement and capability evidence

- [ConRFT: A Reinforced Fine-Tuning Method for VLA Models via Consistency Policy](https://arxiv.org/abs/2502.05450) by Yuhui Chen et al. 2025.
- [DoReMi: Grounding Language Model by Detecting and Recovering from Plan-Execution Misalignment](https://sites.google.com/view/doremi-paper) by Yanjiang Guo et al. 2024.
- [REFLECT: Summarizing Robot Experiences for Failure Explanation and Correction](https://arxiv.org/abs/2306.15724) by Zeyi Liu, Arpit Bahety, and Shuran Song. 2023.
- [Self-Improving Robots: End-to-End Autonomous Visuomotor Reinforcement Learning](https://proceedings.mlr.press/v229/sharma23b.html) by Archit Sharma et al. 2023.
- [SELFI: Autonomous Self-Improvement with RL for Vision-Based Navigation Around People](https://proceedings.mlr.press/v270/hirose25a.html) by Noriaki Hirose et al. 2025.
- [RoboCat: A Self-Improving Generalist Agent for Robotic Manipulation](https://openreview.net/forum?id=vsDnJ2WR4x) by Konstantinos Bousmalis et al. 2024.
- [Autonomous Improvement of Instruction Following Skills via Foundation Models](https://arxiv.org/abs/2407.20635) by Zhiyuan Zhou et al. 2024.
- [Visual Verification Enables Inference-Time Steering and Autonomous Policy Improvement](https://arxiv.org/abs/2606.18247) by Mingtong Zhang and Dhruv Shah. 2026.
- [ASPIRE: Agentic Skills Discovery for Robotics](https://arxiv.org/abs/2607.00272) by Runyu Lu et al. 2026.
- [ENPIRE: Agentic Robot Policy Self-Improvement in the Real World](https://arxiv.org/abs/2606.19980) by Wenli Xiao et al. 2026.

### Agent participation and harnesses

- [Grounded Vision-Language Interpreter for Long-Horizon Bimanual Task and Motion Planning](https://arxiv.org/abs/2506.03270) by Jeremy Siburian et al. 2025.
- [Do As I Can, Not As I Say: Grounding Language in Robotic Affordances](https://arxiv.org/abs/2204.01691) by Michael Ahn et al. 2022.
- [Open-World Task and Motion Planning via Vision-Language Model Generated Constraints](https://arxiv.org/abs/2411.08253) by Nishanth Kumar et al. 2024.
- [Trust the PRoC3S: Solving Long-Horizon Robotics Problems with LLMs and Constraint Satisfaction](https://arxiv.org/abs/2406.05572) by Aidan Curtis et al. 2024.
- [Code as Policies: Language Model Programs for Embodied Control](https://arxiv.org/abs/2209.07753) by Jacky Liang et al. 2022.
- [Code-as-Monitor: Constraint-Aware Visual Programming for Reactive and Proactive Robotic Failure Detection](https://arxiv.org/abs/2412.04455) by Enshen Zhou et al. 2024.
- [RoboGen: Towards Unleashing Infinite Data for Automated Robot Learning via Generative Simulation](https://arxiv.org/abs/2311.01455) by Yufei Wang et al. 2024.
- [GenSim2: Scaling Robot Data Generation with Multi-Modal and Reasoning LLMs](https://arxiv.org/abs/2410.03645) by Pu Hua et al. 2024.
- [Eureka: Human-Level Reward Design via Coding Large Language Models](https://arxiv.org/abs/2310.12931) by Yecheng Jason Ma et al. 2024.
- [DrEureka: Language Model Guided Sim-to-Real Transfer](https://arxiv.org/abs/2406.01967) by Yecheng Jason Ma et al. 2024.
- [HARBOR: A Harness Framework for Agentic Robot Reinforcement Learning](https://arxiv.org/abs/2606.08610) by Zechu Li et al. 2026.
- [Self-Evolving Embodied Agents via Skill-Harness Evolution](https://arxiv.org/abs/2608.11350) by Peidong Wang et al. 2026.

### Training, data, and world models

- [Robot Self-Improvement via Human-Video Dynamics Models](https://arxiv.org/abs/2606.21406) by Hanzhi Chen et al. 2026.
- [SARM2: Multi-Task Stage Aware Reward Modeling for Self Improving Robotic Manipulation](https://arxiv.org/abs/2606.10305) by Qianzhong Chen et al. 2026.
- [Motus2: A Self-Evolving General World Model for Dexterous Manipulation](https://arxiv.org/abs/2608.30237) by Hongzhe Bi et al. 2026.
- [RISE: Self-Improving Robot Policy with Compositional World Model](https://arxiv.org/abs/2602.11075) by Jiazhi Yang et al. 2026.
- [PACT: Self-Evolving Physical Safety Alignment for Diffusion Policies in Embodied Manipulation](https://arxiv.org/abs/2606.08414) by Lingxuan Wu et al. 2026.
- [FAR: Failure-Aware Retry for Test-Time Recovery and Continual Policy Improvement](https://arxiv.org/abs/2607.01111) by Haoran Hao et al. 2026.
- [Practice Makes Policies: Bootstrapping and Consolidating Robotic Capabilities from Zero Human Demonstrations](https://arxiv.org/abs/2607.26809) by Jialiang Li et al. 2026.
- [Self-Evolving Learning for Embodied AI with Criticality Model](https://arxiv.org/abs/2607.28251) by Linxuan He et al. 2026.
- [DenseReward: Dense Reward Learning via Failure Synthesis for Robotic Manipulation](https://arxiv.org/abs/2607.13033) by Yu Fang et al. 2026.
- [Evolve Vision-Language-Action Model into an Agent with On-the-Fly Tool Use](https://arxiv.org/abs/2608.14047) by Yi Ding et al. 2026.
- [Zetta: An Efficient Closed-Loop Embodied Harness for Self-Evolving Physical Intelligence](https://arxiv.org/abs/2608.16590) by Xin Ding et al. 2026.
- [Open X-Embodiment: Robotic Learning Datasets and RT-X Models](https://arxiv.org/abs/2310.08864) by the Open X-Embodiment Collaboration. 2024.

### Verification, evaluation, and safety

- [Unpacking Failure Modes of Generative Policies: Runtime Monitoring of Consistency and Progress](https://arxiv.org/abs/2410.04640) by Christopher Agia et al. 2024.
- [RoboArena: Distributed Real-World Evaluation of Generalist Robot Policies](https://arxiv.org/abs/2506.18123) by Pranav Atreya et al. 2025.
- [SAFE: Multitask Failure Detection for Vision-Language-Action Models](https://arxiv.org/abs/2506.09937) by Qiao Gu et al. 2025.
- [VLA-FAIL: Efficient Task Failure Detection for Finetuned Vision-Language-Action Models](https://arxiv.org/abs/2606.21386) by Florian Seligmann et al. 2026.
- [RoVer: Robot Reward Model as Test-Time Verifier for Vision-Language-Action Model](https://arxiv.org/abs/2510.10975) by Mingtong Dai et al. 2025.
- [RoboMonkey: Scaling Test-Time Sampling and Verification for Vision-Language-Action Models](https://arxiv.org/abs/2506.17811) by Jacky Kwok et al. 2025.
- [Robometer: Scaling General-Purpose Robotic Reward Models via Trajectory Comparisons](https://arxiv.org/abs/2603.02115) by Anthony Liang et al. 2026.
- [WorldEval: World Model as Real-World Robot Policies Evaluator](https://arxiv.org/abs/2505.19017) by Yaxuan Li et al. 2025.
- [GigaWorld-1: A Roadmap to Build World Models for Robot Policy Evaluation](https://arxiv.org/abs/2607.02642) by the GigaWorld Team. 2026.
- [SC3-Eval: Evaluating Robot Foundation Models via Self-Consistent Video Generation](https://arxiv.org/abs/2606.18610) by Wei-Cheng Tseng et al. 2026.
- [ROBOGATE: Adaptive Failure Discovery for Safe Robot Policy Deployment via Two-Stage Boundary-Focused Sampling](https://arxiv.org/abs/2603.22126) by Azuki Kim. 2026.
- [Robust Finetuning of Vision-Language-Action Robot Policies via Parameter Merging](https://arxiv.org/abs/2512.08333) by Yajat Yadav et al. 2026.
- [RoboLab: A High-Fidelity Simulation Benchmark for Analysis of Task Generalist Policies](https://arxiv.org/abs/2604.09860) by Jenai Xuning Yang et al. 2026.
- [BenchShield: Formal Model-Backed Instrumentation for Reward Integrity in LLM-Agent Evaluation Infrastructure](https://arxiv.org/abs/2609.11028) by Shenghan Zheng et al. 2026.
- [No Free Checker: A Survey of Verifiers for Robot Policies](https://arxiv.org/abs/2609.09250) by Yang Wan et al. 2026.

### Recursive and meta-improvement

- [Godel Machines: Fully Self-Referential Optimal Universal Self-Improvers](https://doi.org/10.1007/978-3-540-68677-4_7) by Jurgen Schmidhuber. 2007.
- [Self-Taught Optimizer: Recursively Self-Improving Code Generation](https://arxiv.org/abs/2310.02304) by Eric Zelikman et al. 2023.
- [Godel Agent: A Self-Referential Agent Framework for Recursively Self-Improvement](https://aclanthology.org/2025.acl-long.1354/) by Xunjian Yin et al. 2025.
- [Darwin Godel Machine: Open-Ended Evolution of Self-Improving Agents](https://arxiv.org/abs/2505.22954) by Jenny Zhang et al. 2026.
- [HyperAgents](https://arxiv.org/abs/2603.19461) by Jenny Zhang et al. 2026.
- [EvoTrainer: Co-Evolving LLM Policies and Training Harnesses for Autonomous Agentic Reinforcement Learning](https://arxiv.org/abs/2606.03108) by Guhong Chen et al. 2026.
- [GEAR: Genetic AutoResearch for Agentic Code Evolution](https://arxiv.org/abs/2605.13874) by Ahmadreza Jeddi et al. 2026.
- [CALM: Co-Evolution of Algorithms and Language Model for Automatic Heuristic Design](https://arxiv.org/abs/2505.12285) by Ziyao Huang et al. 2025.
- [Algorithm Discovery with LLMs: Evolutionary Search Meets Reinforcement Learning](https://arxiv.org/abs/2504.05108) by Anja Surina et al. 2025.
- [Learning to Discover at Test Time](https://arxiv.org/abs/2601.16175) by Mert Yuksekgonul et al. 2026.
- [PAST-Bench: Benchmarking the Foundations of Recursive Self-Improvement in Personal Agents](https://arxiv.org/abs/2608.04003) by Shuhan Xue et al. 2026.
- [AI4AI-Bench: Benchmarking LLM Agents in Algorithmic Design for Recursive Self-Improvement](https://arxiv.org/abs/2608.20318) by Yizhe Chi et al. 2026.
- [SBCO: Self-Supervised, Verifier-Grounded Harness Optimization for Planning Agents](https://arxiv.org/abs/2608.10157) by Vivek Kulkarni et al. 2026.
- [Self-Taught Evaluators](https://arxiv.org/abs/2408.02666) by Tianlu Wang et al. 2024.
- [Self-Trained Verification for Training- and Test-Time Self-Improvement](https://arxiv.org/abs/2605.30290) by Chen Henry Wu and Aditi Raghunathan. 2026.
- [Meta-Rewarding Language Models: Self-Improving Alignment with LLM-as-a-Meta-Judge](https://arxiv.org/abs/2407.19594) by Tianhao Wu et al. 2024.

<a id="open-questions"></a>

## Open Questions <sub><a href="#readme-top">top</a></sub>

- **Weight-level self-modification:** no physical system has demonstrated a complete, sustained loop in which its own weight-update process improves and continues to benefit.
- **Judge reliability:** verifier and reward-model errors propagate through the training loop.
- **Imagination-reality gap:** world-model error limits imagined training and evaluation.
- **Forgetting and stability:** new policies, values, and world models can erase earlier competence.
- **Sustained safety:** a continuously changing policy needs more than a one-time safety check.
- **Longitudinal evaluation:** repeated self-evaluation needs protected tests and explicit anti-leakage rules.
- **Transfer of training methods:** transferring a skill is not the same as transferring the procedure that learns it.
- **Theory of recursive training:** we lack conditions for convergence when policy, world model, and evaluator train one another.

<a id="paper-reference-coverage"></a>

## Paper Reference Coverage <sub><a href="#readme-top">top</a></sub>

The supplied paper contains **105 bibliography records**. AutoRT, Robometer, and Darwin Godel
Machine each appear twice as preprint and publication records. After consolidating those three
pairs, the repository indexes **all 102 unique works**:

> [Browse the complete Physical RSI paper reference index](docs/paper-reference-index.md)

The full index is separate from the conceptual map on this page so that completeness does not bury
the paper's argument. Inclusion in the bibliography does not imply that a work demonstrates
Physical RSI; the L1-L5 evidence standard still applies.

<a id="contributing"></a>

## Contributing <sub><a href="#readme-top">top</a></sub>

For a new paper, include its canonical title, primary link, year, the object that changes, the
physical evidence used, whether the change persists, and the comparison that supports the claimed
capability. Use this reviewable entry format:

```markdown
1. **Paper Title**
   [[Paper](https://arxiv.org/abs/YYMM.NNNNN)] | arXiv:YYMM.NNNNN
   `Capability-L3` `Grounding-Physical` `Target-Policy`
   *Evidence:* physical outcome -> admitted experience -> persistent update -> later-round effect
   *Boundary:* verifier and training procedure remain fixed
```

Simulation-only and digital RSI work are welcome when their scope is stated explicitly. A title or
abstract using "self-improving" is not enough: the entry must identify where the loop closes and
what is inherited.

Please open an issue or pull request for additions and corrections. The repository is intentionally
lightweight: the README carries the conceptual map, and the paper index carries bibliographic
coverage.

<a id="data-provenance-and-validation"></a>

## Data Provenance and Validation <sub><a href="#readme-top">top</a></sub>

This repository was checked against the supplied 37-page manuscript rather than assembled from
search results alone.

| Check | Result |
| --- | --- |
| Source snapshot | `IEEE_TPAMI__Physical_RSI-2.pdf` |
| Source SHA-256 | `dcb0083e70ad39183935074d5a41e26c03539c6779032c5557b8d6699f43e4a8` |
| Bibliography reconciliation | 105 records -> 102 unique works |
| Consolidated versions | AutoRT, Robometer, and Darwin Godel Machine |
| arXiv coverage | 87 identifiers parsed from the manuscript; all 87 occur in the full index |
| Featured-to-index check | 65 README entries; all map to the 102-work index |
| Figure provenance | Figures 3, 5, and 14 extracted from the supplied manuscript |
| Repository policy | The source PDF is excluded by `.gitignore`; only the three cited figures are tracked. |
| Last audit | 2026-09-30 |

Counts describe this manuscript snapshot. Future additions to the living catalog should be labeled
as repository extensions rather than silently included in the paper's bibliography count.

<a id="license"></a>

## License <sub><a href="#readme-top">top</a></sub>

This repository is released under the [MIT License](LICENSE).
