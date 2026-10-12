`<a id="readme-top"></a>`

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
  <a href="#the-boundary">Boundary</a>  | 
  <a href="#capability-map">L1-L5</a>  | 
  <a href="#featured-evidence-register">Evidence register</a>  | 
  <a href="#three-views-of-one-system">Research map</a>  | 
  <a href="#paper-catalog">Paper catalog</a>  | 
  <a href="docs/paper-reference-index.md">All references</a>
</p>

</div>

<p align="center">
  <img src="docs/figures/darwin-haeckel-evolutionary-trees.png" alt="Darwin's first evolutionary tree sketch beside Haeckel's nineteenth-century pedigree of humankind" width="400">
</p>
<p align="center"><em>Life is not repetition, but creation. Duration carries the whole of reality: a boundless river flowing toward a horizon with no predetermined end.</em><br>
<sub>Darwin's <a href="https://commons.wikimedia.org/wiki/File:Darwin_Tree_1837.png">first evolutionary tree</a> (1837), beside Haeckel's <a href="https://commons.wikimedia.org/wiki/File:Pedigree_of_man_(Haeckel_1874).jpg"><em>Pedigree of Man</em></a> (1874). Both works are public domain.</sub></p>

`<a id="from-evolution-to-physical-rsi"></a>`

## From Evolution to Physical RSI `<sub><a href="#readme-top">`top `</a></sub>`

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

The repository is organized to be read from definitions and evidence to methods, papers, and
open questions:

- [From Evolution to Physical RSI](#from-evolution-to-physical-rsi)
- [The Boundary](#the-boundary)
- [Capability Map](#capability-map)
- [Featured Evidence Register](#featured-evidence-register)
- [Harness Adaptation, Training, and Verification](#three-views-of-one-system)
- [Paper Catalog](#paper-catalog)
- [Open Questions](#open-questions)
- [License](#license)

> **Version note.** The sections below follow `IEEE_TPAMI__Physical_RSI-33.pdf` (12 October 2026).
> The opening introduction and badges are retained from the earlier README; their L1–L5 taxonomy,
> real-only grounding language, and bibliography counts should not be read as claims about this snapshot.
> The current framework and coverage are specified below.

---

`<a id="the-boundary"></a>`

## The Boundary `<sub><a href="#readme-top">`top `</a></sub>`

The paper separates the **task-execution system** from the **procedure that improves it**.
Their roles, rather than whether they are implemented as code, text, or weights, determine what
has changed and which claim the evidence supports.

| Object                                                       | Role in the improvement system                                                                                                          |
| ------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------- |
| **Execution system `M = (Θ, H)`**                   | Learned execution models `Θ` and the model-external harness `H`: prompts, memory, skills, tools, and orchestration.                |
| **Improvement procedure `Φ = (Adapt, Train, Ver)`** | Harness adaptation, data preparation and model training, and verification of candidate updates. These stages may themselves be revised. |
| **Experience `D`**                                   | Execution records and improvement histories, including attempted changes and their outcomes.                                            |
| **Protected evaluation `E/Q`**                       | Tasks and scoring rules outside `Φ`, used to evaluate the systems it produces and to judge revisions of `Ver`.                     |

<p align="center">
  <a href="docs/figures/physical-rsi-v33-overview.png"><img src="docs/figures/physical-rsi-v33-overview.png" alt="Physical RSI architecture and L0–L5 framework" width="96%"></a>
</p>
<p align="center"><sub><strong>Figure 1.</strong> Task execution, the improvement procedure, safety and control, and the L0–L5 framework.</sub></p>

Four claims that are often collapsed should be kept separate:

| Claim                                 | What must be shown                                                                                                                                                                  |
| ------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Inheritance**                 | An accepted change persists beyond its originating episode and is used later.                                                                                                       |
| **Retained capability gain**    | The inherited change contributes to better later task performance.                                                                                                                  |
| **Meta-level self-inheritance** | The procedure produces a revision of its own stages, which is retained and used in later improvement.                                                                               |
| **Recursive gain across tasks** | Successive revised procedures produce better subsequent systems than their predecessors from matched starting systems and experience, under equal budgets and protected evaluation. |

Replanning within an execution is not inheritance. Revising a procedure is not proof that it
improves more effectively. A persuasive comparison accounts for robot trials, resets, hardware wear,
compute, search, and human effort—not only the final successor's score.

**Grounding and deployment are different records.** Definitions 1–2 and Section 5.2 allow grounding
through physics simulation or real interaction. Simulated feedback is not evidence of hardware
safety; learned-model imagination alone does not meet the grounding condition. Deploying a frozen
result on a robot does not retroactively make its earlier revisions depend on real-robot feedback.

`<a id="capability-map"></a>`

## Capability Map `<sub><a href="#readme-top">`top `</a></sub>`

L1–L4 cross two dimensions: **the update target** and **the scope of the demonstrated gain**.
They are not a simple ladder from human assistance to autonomy. L5 builds on L4 and adds verified
recursive gain. A level applies to a specified improvement workflow and evaluation protocol—not
to every experiment in a paper.

| Scope of gain          | Capability-level update to `M = (Θ, H)`                                                                                                               | Meta-level update to `Φ`                                                                                                                                  |
| ---------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Same task**    | **L1:** an autonomously inherited capability update yields a retained same-task gain, with the improvement procedure fixed.                        | **L2:** an autonomously revised and inherited procedure is reused for same-task improvement, with retained capability gain.                            |
| **Across tasks** | **L3:** source-task experience produces an inherited capability change that contributes to target-task gain, with the improvement procedure fixed. | **L4:** a procedure revision formed through source-task improvement is inherited and used for improvement across tasks, with retained capability gain. |

- **L0 — no autonomous retained-improvement loop in the assessed workflow.** This includes
  execution-only correction and, under the paper's autonomy rule, retained updates that depend on
  human intervention or labeling during improvement.
- **L5 — verified recursive gain across tasks.** Beyond L4, successive inherited revisions of `Φ`
  must produce better subsequent improvements than their predecessors from matched starting
  systems and experience, under equal budgets and protected evaluation.

**Procedure change is not sufficient for L5.** Revising training code, a curriculum, or an acceptance
rule establishes a changed mechanism only when the revision is retained and used. Its superiority
requires a separate comparison of the subsequent systems produced by the old and new procedures.
The manuscript's Figure 3 reports **no confirmed L5 case among its selected systems**.

### What counts as another task?

The manuscript describes a task through its required **skill sequence `κ`** and its **instance
parameters `ξ`**. A change in object pose or scene difficulty does not establish across-task transfer
if the required sequence remains unchanged. A new skill or a new ordering or composition of existing
skills changes `κ`.

- Grasping a cup from two different exposed positions: potentially the **same task**, with different `ξ`.
- Grasping a cup versus opening a cabinet and then grasping it: **different tasks**.
- `navigate → open → grasp` versus `grasp → navigate → open`: **different skill sequences**.

<p align="center">
  <a href="docs/figures/physical-rsi-v33-update-targets-and-tasks.png"><img src="docs/figures/physical-rsi-v33-update-targets-and-tasks.png" alt="Capability versus meta-level updates, and task identity through skill sequences" width="100%"></a>
</p>
<p align="center"><sub><strong>Manuscript Figure 2.</strong> Update targets and task identity. New scenes or embodiments should not automatically be counted as new tasks.</sub></p>

Cross-task evidence must also show that the retained source change is actually used and contributes
to target performance. Running the same fixed procedure independently on many tasks is not enough.

`<a id="featured-evidence-register"></a>`

## Featured Evidence Register `<sub><a href="#readme-top">`top `</a></sub>`

The entries below follow the manuscript's selected protocols in Section 2.3 and Figure 3.
They separate the inherited object from the setting that supplies its feedback. The register is
selective and does not replace the underlying experiments or their autonomy conditions.

| Selected workflow                                                                                                            | Reading under the current framework                           | Evidence and boundary                                                                                                                                                                                                                                             |
| ---------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [ConRFT](https://arxiv.org/abs/2502.05450), operator-assisted learning                                                          | **L0 reference workflow**                               | Human corrections contribute to retained learning. This is useful robot improvement, but not autonomous improvement under the manuscript's level-assignment rule.                                                                                                 |
| [DoReMi](https://sites.google.com/view/doremi-paper), execution recovery                                                        | **L0 reference workflow**                               | Detecting a mismatch and replanning during execution does not by itself establish a retained update to `M` or `Φ`.                                                                                                                                           |
| [SOAR](https://arxiv.org/abs/2407.20635) and [SELFI](https://proceedings.mlr.press/v270/hirose25a.html), autonomous robot learning | **L1 in the selected workflows**                        | Real-robot experience supports retained capability updates. A new scene or further training round is not automatically a new `κ` or an updated improvement procedure.                                                                                          |
| [ENPIRE](https://arxiv.org/abs/2606.19980), pin-insertion training-code revision                                                | **L2 in the selected same-task protocol**               | Robot outcomes guide revisions to training code and recipes. The selected experiment does not establish across-task procedure improvement or the successive matched gains required for L5.                                                                        |
| [ASPIRE](https://arxiv.org/abs/2607.00272), retained library transfer                                                           | **L3 in the selected simulation protocol**              | Guidance accumulated on LIBERO-90 is applied to held-out long-horizon tasks without further debugging or task-specific library updates. The retained library belongs to `H`; separate real-robot transfer does not change the source of its discovery feedback. |
| [RPG](https://arxiv.org/abs/2610.02204), skill and prompt improvement                                                           | **L3 in the manuscript's selected workflow**            | Simulation practice updates the execution system, which is then frozen for real deployment. Retaining an improved skill library is not the same as revising the method that builds the library.                                                                   |
| [Hyperagents](https://arxiv.org/html/2603.19461v1), transferable meta-improvement                                               | **L4 comparator in Figure 3; methodological precedent** | The manuscript uses this work to discuss editable improvement procedures and transfer. Its digital/meta-level evidence should not be relabeled as a demonstration of real-robot L5.                                                                               |

**Autonomy needs its own record.** Human setup, scene resets, hardware repair, and authorization for
physical operation should be reported separately from human labeling, corrective intervention,
code edits, or update selection. The latter can determine what is inherited and therefore affect
the level claim; the former do not change the level by themselves, but still contribute cost and risk.

`<a id="three-views-of-one-system"></a>`

## Harness Adaptation, Training, and Verification `<sub><a href="#readme-top">`top`</a></sub>`

Harness adaptation and model training are two pathways through the same improvement system.
Safety constrains both; verification decides what can be inherited; independent evaluation asks
whether the retained changes helped. Sections 3–6 organize these complementary roles.

### 1. Harness adaptation

The harness carries execution resources across tasks: memory, skill implementations, interfaces,
and orchestration or recovery logic. Its update loop connects physical evidence to later use:

> **execution evidence → diagnosis and edit scope → candidate change → verification → inheritance**

| Question                                                | Update target                                                  | Representative work                                                                                                                                                          |
| ------------------------------------------------------- | -------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **What execution resource should change?**        | Memory, programs, skills, prompts, or workflows in `H`.      | [ASPIRE](https://arxiv.org/abs/2607.00272), [RPG](https://arxiv.org/abs/2610.02204), [RoboFoundry](https://arxiv.org/html/2609.32862v1), [KnowBody](https://arxiv.org/html/2609.28530v1) |
| **How should later harness changes be produced?** | The diagnosis, construction, or selection method in `Adapt`. | Digital precedents include[STOP](https://arxiv.org/pdf/2310.02304v3), [MemSkill](https://arxiv.org/abs/2602.02474v2), and [VERSE](https://arxiv.org/abs/2610.02616v1).                |

Adding a skill changes an execution resource. Changing the method that discovers or selects future
skills targets the improvement procedure. Digital examples help explain this distinction; their
inclusion does not establish physical grounding.

### 2. Model training

Training connects collected and selected experience to inherited model updates:

> **experience preparation → IL / SSL / RL → model update → verification → later interaction**

The paper reviews data preparation, imitation learning, self-supervised learning, reinforcement
learning, and VLA, world, and reward models. [SOAR](https://arxiv.org/abs/2407.20635) and
[SELFI](https://proceedings.mlr.press/v270/hirose25a.html) illustrate continued robot learning;
[EmbodiRSI](https://arxiv.org/abs/2609.38905) and [F4R](https://arxiv.org/abs/2609.35575v2)
provide adaptation examples; [ENPIRE](https://arxiv.org/abs/2606.19980) illustrates training-code revision.

Better weights under a fixed objective do not establish a better improvement procedure. A reward
or world model used only during training may belong to `Φ`, but fitting it to a prescribed target is
not automatically meta-improvement. Identify a retained change to the objective, update rule,
curriculum, training configuration, or decision procedure, and assess its later effect.

### 3. Safety and control

Safety must be reassessed across updates, rather than checked only for the final policy.

| Decision                          | Required distinction                                                                                             |
| --------------------------------- | ---------------------------------------------------------------------------------------------------------------- |
| **Attempt a trial**         | Check operating assumptions, action constraints, uncertainty, and feasible stopping or recovery.                 |
| **Accept an update**        | Decide whether the candidate should be inherited; check affected interfaces, capabilities, and safeguards.       |
| **Authorize operation**     | Establish the conditions under which the system may operate physically; acceptance alone does not grant release. |
| **Assess accumulated risk** | Include rejected trials, resets, recovery, interventions, and hardware wear—not only successful execution.      |

A safe final policy does not show that its learning process was safe. Earlier guarantees remain
usable only while their assumptions and statistical bounds remain valid. The paper reviews
component guarantees under stated conditions, not a safety guarantee for unrestricted Physical RSI.

### 4. Verification and evaluation

**Verification asks what may be retained. Evaluation asks what its later use achieved.**
Section 6 separates these roles: `Ver` belongs to `Φ`; protected `E/Q` assesses the resulting system.

<p align="center">
  <a href="docs/figures/physical-rsi-v33-verification-evaluation.png"><img src="docs/figures/physical-rsi-v33-verification-evaluation.png" alt="Candidate verification and independent evaluation" width="96%"></a>
</p>
<p align="center"><sub><strong>Figure 10.</strong> Candidate construction, implementation, effectiveness and preservation checks, and the independent evaluator.</sub></p>

| Verification check                | Deciding question                                                                            |
| --------------------------------- | -------------------------------------------------------------------------------------------- |
| **Implementation validity** | Can the candidate run with the required syntax, interfaces, formats, and outputs?            |
| **Repair effectiveness**    | Does it address the targeted failure under the tested conditions?                            |
| **Capability preservation** | Does it retain earlier successful behavior and revalidate dependent knowledge?               |
| **Meta-verification**       | If `Ver` changes, do independent outcomes of the systems it accepts justify that revision? |

Passing an implementation check establishes testability, not improvement. More accepted updates
under a revised verifier do not establish that the verifier is better.

Improvement evaluation follows three questions:

1. **Performance and retention:** what improves over rounds, and which earlier capabilities remain?
2. **Attribution and transfer:** what retained change causes the gain, and does it transfer to a new `κ`?
3. **Efficiency and autonomy:** what interaction, compute, human assistance, and physical risk produced it?

For L5, compare successive versions of `Φ` from the same starting execution system and initial
experience, with equal budgets, matched safety and stopping conditions, and protected across-task
evaluation. Use repeated trials and uncertainty estimates. Report the cost of developing a revision
separately from the cost of using it to produce later improvements.

Two forms of independence matter. **Control independence** prevents a candidate from changing or
bypassing the protected evaluator. **Information independence** prevents adaptive feedback from
turning the final test into an optimization target. Keeping `E/Q` outside `Φ` is not enough if its
decisions repeatedly guide later proposals. Use fresh evidence or appropriate statistical correction;
if the evaluation set changes, retain a fixed anchor or re-evaluate earlier generations.

### 5. Benchmark resources

Section 6.3 and Table 4 group resources by what they assess, not by an assigned RSI level.
This selected map also includes process-oriented resources discussed in the text.

| Family                      | Evaluation focus                                      | Representative resources                                                               |
| --------------------------- | ----------------------------------------------------- | -------------------------------------------------------------------------------------- |
| **Embodied**          | Task performance and generalization                   | Meta-World, LIBERO, ManiSkill3, BEHAVIOR-1K, RoboCasa365                               |
| **Embodied**          | Robustness and physical evaluation                    | LIBERO-PRO, SIMPLER, RoboTwin, RoboArena                                               |
| **Embodied**          | Feedback and evaluation reliability                   | FailBench, RoboRewardBench, WorldEval, dWorldEval, SC3-Eval, RBM-EVAL                  |
| **Embodied**          | Robot engineering and development                     | CaP-Bench within CaP-X, EmboCoach-Bench as named in the manuscript, RLE-Bench          |
| **Primarily digital** | AI research, training algorithms, and data strategies | AI4AI-Bench, RSIBench-Data, MLAgentBench, MLE-bench, MLGym-Bench, MLRC-Bench, RE-Bench |
| **Primarily digital** | Method or harness development and retained experience | RSI-Exam, HarnessDev, PAST-Bench                                                       |

These resources probe different parts of the problem. An iterative agent benchmark is not, by that
fact alone, a complete Physical RSI evaluation. Verified recursive gain across tasks under matched
conditions remains a gap identified in the manuscript's reviewed resources.

`<a id="paper-catalog"></a>`

## Paper Catalog `<sub><a href="#readme-top">`top `</a></sub>`

### Model Training

Training is a continuing, gated process rather than a one-off offline stage:

> **experience collection -> evaluation and credit -> parameter update -> verification and consolidation**

#### 1. Data Preparation

Experience generation and selection determine what the learner practices and which trajectories become training data.

##### Task, environment, and practice generation

-**[Self-Improving Robots: End-to-End Autonomous Visuomotor Reinforcement Learning](https://proceedings.mlr.press/v229/sharma23b.html)** (2023) — Autonomous real-world practice connects visuomotor policy learning with reset and training infrastructure.

-**[Find Something You Can&#39;t Do: Agentic Real-World Reinforcement Learning for Self-Improving VLA Models](https://arxiv.org/abs/2609.32069v1)** (2026) — Scene-conditioned, weakness-aware task selection directs real-world practice; residual RL improves a frozen VLA.

-**[GenSim: Generating Robotic Simulation Tasks via Large Language Models](https://arxiv.org/abs/2310.01361)** (2024) — LLMs generate robotic simulation tasks to expand the experience available for policy learning.

-**[GenSim2: Scaling Robot Data Generation with Multi-modal and Reasoning LLMs](https://arxiv.org/abs/2410.03645)** (2024) — Multimodal and reasoning LLMs scale simulated task construction and robot-data generation.

-**[CurricuLLM: Automatic Task Curricula Design for Learning Complex Robot Skills using Large Language Models](https://arxiv.org/abs/2409.18382)** (2024) — LLMs organize task curricula for learning increasingly complex robot skills.

-**[RoboGen: Towards Unleashing Infinite Data for Automated Robot Learning via Generative Simulation](https://arxiv.org/abs/2311.01455)** (2024) — Generative simulation constructs tasks, scenes, rewards, and demonstrations for automated robot learning.

-**[Scaling Sim-to-Real VLA Reinforcement Learning with Generative 3D Worlds](https://arxiv.org/abs/2603.18532)** (2026) — Generative 3D environments broaden simulation coverage for sim-to-real VLA reinforcement learning.

-**[SimWorld Studio: Automatic Environment Generation with Evolving Coding Agent for Embodied Agent Learning](https://arxiv.org/abs/2605.09423)** (2026) — An evolving coding agent generates simulation environments for embodied-agent training.

-**[HomeBody: A Humanoid That Explores, Remembers, and Acts on Its Own](https://tml.stanford.edu/homebody/)** (2026) — Observation- and SLAM-derived digital twins support spatial reasoning and execution; this is an environment-preparation precedent.

##### Experience selection, human guidance, and recovery

-**[MAGMA-GEN: Validated Recovery Supervision from Ambiguous Failures via Counterfactual Re-Execution](https://arxiv.org/abs/2609.20056)** (2026) — Coach-proposed recovery actions undergo matched-state counterfactual re-execution, generating validated supervision from the policy's failed rollouts.

-**[Robot Learning on the Job: Human-in-the-Loop Autonomy and Learning During Deployment](https://arxiv.org/abs/2211.08416)** (2023) — Human interventions and deployment experience support continuing robot-policy learning.

-**[Precise and Dexterous Robotic Manipulation via Human-in-the-Loop Reinforcement Learning](https://arxiv.org/abs/2410.21845)** (2025) — Human-guided real-world RL combines demonstrations, corrections, and online interaction for dexterous manipulation.

-**[ThriftyDAgger: Budget-Aware Novelty and Risk Gating for Interactive Imitation Learning](https://arxiv.org/abs/2109.08273)** (2021) — Novelty and risk gates allocate a limited human-query budget during interactive imitation learning.

-**[Zero2Skill: Bootstrapping Robot Skills through Autonomous Data Collection, Training, and Deployment](https://arxiv.org/abs/2607.14047v3)** (2026) — A collection–training–deployment workflow bootstraps robot skills with human correction memory.

-**[EgoRecovery: Acquiring Failure Recovery Ability Through Human Recovery Demonstration](https://arxiv.org/abs/2607.19745)** (2026) — Human recovery demonstrations supply supervision for learning from failure states.

-**[Autonomous Improvement of Instruction Following Skills via Foundation Models](https://arxiv.org/abs/2407.20635)** (2024) — Foundation-model-guided autonomous collection admits successful robot experience for subsequent policy improvement.

-**[FAR: Failure-Aware Retry for Test-Time Recovery and Continual Policy Improvement](https://arxiv.org/abs/2607.01111)** (2026) — Failure-aware retries recover execution and return successful recovery experience to continual policy training.

-**[Self-Evolving Learning for Embodied AI with Criticality Model](https://arxiv.org/abs/2607.28251)** (2026) — An updated criticality predictor focuses experience collection on failure-prone states.

##### Adaptive simulation distributions and exploration

-**[Closing the Sim-to-Real Loop: Adapting Simulation Randomization with Real World Experience](https://arxiv.org/abs/1810.05687)** (2019) — Real-world experience updates simulation-randomization distributions for later policy training.

-**[Data-Efficient Domain Randomization With Bayesian Optimization](https://doi.org/10.1109/LRA.2021.3052391)** (2021) — Real-world policy returns guide Bayesian optimization of domain-randomization distributions.

-**[Neural Posterior Domain Randomization](https://proceedings.mlr.press/v164/muratore22a.html)** (2022) — Neural posterior inference estimates simulator-parameter distributions from observed experience.

-**[Planning to Explore via Self-Supervised World Models](https://arxiv.org/abs/2005.05960)** (2020) — World-model uncertainty guides exploration and the collection of informative experience.

#### 2. Training Methods

Pretraining establishes behavioral and perceptual priors; imitation, self-supervision, and reinforcement learning incorporate subsequent experience.

##### Overview

-**[Training Methods and Generation Technologies for Embodied Intelligent Robot Manipulation Skill Models: A Systematic Review](https://www.techscience.com/cmc/v89n1/68409)** (2026) — A review of robot manipulation training, skill generation, motion control, and deployment challenges.

-**[Vision-Language-Action Models for Robotics: A Review Towards Real-World Applications](http://dx.doi.org/10.1109/ACCESS.2025.3609980)** (2025) — A review of VLA architectures, training strategies, and challenges in real-world deployment.

-**[World Model for Robot Learning: A Comprehensive Survey](https://arxiv.org/abs/2605.00080)** (2026) — A review of predictive models for policy learning, planning, learned simulation, evaluation, and data generation.

-**[Towards AI That Improves Itself: A Survey of Recursive Self-Improvement](https://lee1003-lee.github.io/Awesome-RSI-Research/assets/rsi-survey.pdf)** (year not specified in PSI.bib) — A general RSI framework covering model/data evolution, retained updates, and improvement of research processes.

-**[Recursive Self-Improvement in AI: A Survey](https://www.preprints.org/manuscript/202609.2680/v1)** (2026, preprint) — A mechanism-oriented review connecting self-training, AutoML, meta-learning, and editable improvement procedures.

##### Imitation learning

-**[ReGuide: From Test-Time Guidance to Self-Improving Diffusion Policies](https://arxiv.org/abs/2606.28939)** (2026) — Successful phase-guided recovery rollouts are reused for iterative diffusion-policy fine-tuning or retraining in simulation.

-**[RoboCat: A Self-Improving Generalist Agent for Robotic Manipulation](https://openreview.net/forum?id=vsDnJ2WR4x)** (2023) — A generalist manipulation model uses demonstrations and self-generated data for later training and adaptation.

-**[What Matters in Learning from Offline Human Demonstrations for Robot Manipulation](https://arxiv.org/abs/2108.03298)** (2021) — Studies dataset and algorithm choices for learning manipulation policies from offline human demonstrations.

-**[OpenVLA: An Open-Source Vision-Language-Action Model](https://arxiv.org/abs/2406.09246)** (2024) — An open VLA supports action-token prediction and parameter-efficient or full model adaptation.

-**[FAST: Efficient Action Tokenization for Vision-Language-Action Models](https://arxiv.org/abs/2501.09747)** (2025) — Compressed action tokens make autoregressive VLA training more efficient.

-**[Diffusion Policy: Visuomotor Policy Learning via Action Diffusion](https://arxiv.org/abs/2303.04137)** (2024) — Action-distribution learning through diffusion supplies a generative behavior-cloning policy.

-**[π₀: A Vision-Language-Action Flow Model for General Robot Control](https://arxiv.org/abs/2410.24164)** (2024 preprint; RSS 2025) — Flow matching learns continuous action chunks on top of pretrained vision-language representations.

-**[One-Step Diffusion Policy: Fast Visuomotor Policies via Diffusion Distillation](https://arxiv.org/abs/2410.21257)** (2024) — Teacher-policy distillation replaces iterative diffusion sampling with a one-step action generator.

-**[Generative Adversarial Imitation Learning](https://arxiv.org/abs/1606.03476)** (2016) — Adversarial distribution matching provides an alternative imitation-learning objective.

-**[One-Shot Imitation from Observing Humans via Domain-Adaptive Meta-Learning](https://arxiv.org/abs/1802.01557)** (2018) — Domain-adaptive meta-learning supplies a precedent for learning an imitation objective from cross-domain demonstrations.

##### Self-supervised learning

-**[Real-World Robot Learning with Masked Visual Pre-training](https://arxiv.org/abs/2210.03109)** (2022) — Masked visual reconstruction provides representations for downstream robot-policy learning.

-**[Latent Action Pretraining from Videos](https://arxiv.org/abs/2410.11758)** (2025) — Latent actions learned from videos reduce dependence on expert action labels during pretraining.

-**[Structured World Models from Human Videos](https://arxiv.org/abs/2308.10901)** (2023) — Human-video predictive priors are adapted with robot experience for world-model-based learning.

-**[DayDreamer: World Models for Physical Robot Learning](https://proceedings.mlr.press/v205/wu23c.html)** (2023) — Real robot trajectories update a world model that supplies imagined experience for policy learning.

-**[VLAW: Iterative Co-Improvement of Vision-Language-Action Policy and World Model](https://arxiv.org/abs/2602.12063)** (2026) — Real rollouts refine a video world model, which generates supplemental data for iterative VLA improvement.

-**[RoboTTT: Context Scaling for Robot Policies](https://arxiv.org/abs/2607.15275)** (2026) — Test-time training scales policy context; fast-weight updates support adaptation during execution.

-**[Automated Self-Supervised Learning for Graphs](https://arxiv.org/abs/2106.05470)** (2022) — Searches combinations and weights of self-supervised objectives for graphs; a digital methodological precedent.

##### Reinforcement learning

-**[Embodied Learning under Policy and Dynamics Shifts](https://doi.org/10.1093/nsr/nwag506)** (2026) — OMPO corrects policy and dynamics shifts when reusing historical replay for continual RL adaptation on control and manipulation benchmarks.

-**[SELFI: Autonomous Self-Improvement with RL for Vision-Based Navigation around People](https://proceedings.mlr.press/v270/hirose25a.html)** (2025) — Autonomous real-world interaction improves vision-based navigation around people.

-**[Lifelong Autonomous Improvement of Navigation Foundation Models in the Wild](https://proceedings.mlr.press/v270/stachowicz25a.html)** (2025) — Deployment experience continually adapts navigation foundation models in real environments.

-**[Continuously Improving Mobile Manipulation with Autonomous Real-World RL](https://proceedings.mlr.press/v270/mendonca25a.html)** (2025) — Autonomous real-world RL supports continuing improvement of mobile-manipulation policies.

-**[Learning While Deploying: Fleet-Scale Reinforcement Learning for Generalist Robot Policies](https://arxiv.org/abs/2605.00416)** (2026) — Fleet-scale deployment experience feeds reinforcement learning of generalist robot policies.

-**[Cal-QL: Calibrated Offline RL Pre-Training for Efficient Online Fine-Tuning](https://arxiv.org/abs/2303.05479)** (2024) — Calibrated offline RL pretraining provides a starting point for efficient online fine-tuning.

-**[ConRFT: A Reinforced Fine-tuning Method for VLA Models via Consistency Policy](https://arxiv.org/abs/2502.05450)** (2025) — Consistency-policy fine-tuning combines prior data, online robot interaction, and human corrections.

-**[π*₀.₆: a VLA That Learns From Experience](https://arxiv.org/abs/2511.14759)** (2025) — RECAP combines demonstrations, deployment rollouts, and expert interventions through advantage-conditioned VLA learning.

-**[Diffusion Policy Policy Optimization](https://arxiv.org/abs/2409.00588)** (2024) — Reinforcement learning fine-tunes diffusion policies through their denoising process.

-**[Steering Your Diffusion Policy with Latent Space Reinforcement Learning](https://arxiv.org/abs/2506.15799)** (2025) — A learned latent-space controller steers a frozen diffusion policy.

-**[EvoHIL: Self-Evolving Reward and Flow-Matched Policy Optimization for Robust Human-in-the-Loop Reinforcement Learning](https://arxiv.org/abs/2608.03872)** (2026) — Human-confirmed outcomes adapt the reward model alongside flow-matched policy optimization.

-**[Efficient Language-instructed Skill Acquisition via Reward-Policy Co-Evolution](https://arxiv.org/abs/2412.13492)** (2024) — Iterative reward-code and policy co-evolution supports language-instructed skill acquisition.

-**[Discovering State-of-the-Art Reinforcement Learning Algorithms](https://doi.org/10.1038/s41586-025-09761-x)** (2025) — Meta-learning discovers policy and prediction update rules on digital RL benchmarks.

-**[Differentiable Evolutionary Reinforcement Learning](https://arxiv.org/abs/2512.13399)** (2026) — Policy-validation performance trains a meta-optimizer that generates future reward structures in digital tasks.

#### 3. Learning Models

The same learning paradigms can update action generation, predictive dynamics, or the signals that guide future learning.

##### Vision-language-action models

-**[SEES: A Self-Evolving Embodied System via Failure-Guided VLA Policy Adaptation](https://arxiv.org/abs/2609.32698)** (2026) — Failure bottlenecks trigger targeted simulation tasks and RL updates to shared VLA adapters, supporting transfer across related skills.

-**[RedFlow: Redirect Failure into Action-level Corrections for Flow-matching VLA Policy](https://arxiv.org/abs/2607.27782)** (2026) — Offline post-training uses fixed rollouts, matched execution contexts, and higher-quality action chunks to derive corrective targets for flow-matching VLAs.

-**[Zeva-Ego: Egocentric Mid-Training with In-Context Causal Learning for Robot Manipulation](https://arxiv.org/abs/2609.24411)** (2026) — Action-centered supervision from egocentric video supports VLA mid-training; deployment-time causal adaptation uses interaction feedback without parameter updates.

-**[RT-2: Vision-Language-Action Models Transfer Web Knowledge to Robotic Control](https://proceedings.mlr.press/v229/zitkovich23a.html)** (2023) — Action-token training transfers web-scale vision-language knowledge into robot control.

-**[Octo: An Open-Source Generalist Robot Policy](https://doi.org/10.15607/RSS.2024.XX.090)** (2024) — A generalist robot policy uses a diffusion action head and supports downstream adaptation.

-**[RDT-1B: a Diffusion Foundation Model for Bimanual Manipulation](https://arxiv.org/abs/2410.07864)** (2025) — A diffusion foundation model supplies continuous action generation for bimanual manipulation.

-**[Knowledge Insulating Vision-Language-Action Models: Train Fast, Run Fast, Generalize Better](https://doi.org/10.52202/085713-3439)** (2025) — Gradient isolation separates discrete-action backbone training from the continuous-action expert.

-**[RT-H: Action Hierarchies using Language](https://doi.org/10.15607/RSS.2024.XX.049)** (2024) — Language-conditioned action hierarchies structure high-level interpretation and low-level control.

-**[Hi Robot: Open-Ended Instruction Following with Hierarchical Vision-Language-Action Models](https://arxiv.org/abs/2502.19417)** (2025) — Hierarchical VLAs coordinate open-ended instruction interpretation with action generation.

-**[GR00T N1: An Open Foundation Model for Generalist Humanoid Robots](https://arxiv.org/abs/2503.14734)** (2025) — An open humanoid foundation model combines high-level vision-language reasoning with action generation.

-**[RL Token: Bootstrapping Online RL with Vision-Language-Action Models](https://arxiv.org/abs/2604.23073)** (2026) — A compact RL-token interface supports online actor–critic learning around a pretrained VLA.

##### World models and world-action models

-**[Self-Improving Robot Policy with Compositional World Model](https://www.roboticsproceedings.org/rss22/p012.html)** (2026) — A compositional world model supports repeated policy optimization through imagined rollouts.

-**[World-VLA-Loop: Closed-Loop Learning of Video World Model and VLA Policy](https://arxiv.org/abs/2602.06508)** (2026) — Improved-policy rollouts refine a video world model used for subsequent VLA post-training.

-**[Learning Universal Policies via Text-Guided Video Generation](https://arxiv.org/abs/2302.00111)** (2023) — Text-guided video generation and inverse dynamics connect predicted outcomes to robot actions.

-**[TD-MPC2: Scalable, Robust World Models for Continuous Control](https://arxiv.org/abs/2310.16828)** (2024) — Latent world-model learning supports scalable planning and continuous control.

-**[WorldEval: World Model as Real-World Robot Policies Evaluator](https://arxiv.org/abs/2505.19017)** (2025) — A world model predicts policy outcomes for evaluation; its role differs from direct policy training.

-**[Learning Interactive Real-World Simulators](https://arxiv.org/abs/2310.06114)** (2024) — An interactive generative simulator supplies synthetic experience for policy learning.

-**[Ctrl-World: A Controllable Generative World Model for Robot Manipulation](https://arxiv.org/abs/2510.10125)** (2026) — Action-conditioned, multi-view predictions support policy ranking and synthetic-data fine-tuning.

-**[Motus2: A Self-Evolving General World Model for Dexterous Manipulation](https://arxiv.org/abs/2608.30237)** (2026) — Shared weights expose policy, simulator, and evaluator interfaces in a unified decision-and-learning loop.

-**[WAM-RL: World-Action Model Reinforcement Learning with Reconstruction Rewards and Online Video SFT](https://arxiv.org/abs/2606.17906)** (2026) — World-action-model RL combines reconstruction rewards with online video supervised fine-tuning.

##### Reward models and value learning

-**[LIV: Language-Image Representations and Rewards for Robotic Control](https://arxiv.org/abs/2306.00958)** (2023) — Language-image representations provide task-progress and reward signals for robotic control.

-**[RoboReward: General-Purpose Vision-Language Reward Models for Robotics](https://arxiv.org/abs/2601.00675)** (2026) — General-purpose vision-language reward modeling supplies task-outcome feedback.

-**[Robometer: Scaling General-Purpose Robotic Reward Models via Trajectory Comparisons](https://arxiv.org/abs/2603.02115)** (2026) — Trajectory comparisons train a general-purpose robotic reward model.

-**[SARM2: Multi-Task Stage Aware Reward Modeling for Self Improving Robotic Manipulation](https://arxiv.org/abs/2606.10305)** (2026) — Stage estimation and value learning provide dense rewards for subsequent VLA policy improvement.

-**[DenseReward: Dense Reward Learning via Failure Synthesis for Robotic Manipulation](https://arxiv.org/abs/2607.13033)** (2026) — Synthesized failure examples support dense reward learning for manipulation.

-**[Robo-Dopamine: General Process Reward Modeling for High-Precision Robotic Manipulation](https://arxiv.org/abs/2512.23703)** (2025) — Process reward modeling supplies fine-grained feedback for high-precision manipulation.

-**[PEBBLE: Feedback-Efficient Interactive Reinforcement Learning via Relabeling Experience and Unsupervised Pre-training](https://arxiv.org/abs/2106.05091)** (2021) — Preference-based reward updates alternate with policy learning and replay-experience relabeling.

-**[Flora: Sample-Efficient Preference-Based Rl Via Low-Rank Style Adaptation of Reward Functions](https://doi.org/10.1109/ICRA55743.2025.11127633)** (2025) — Low-rank reward adaptation incorporates new preferences while limiting interference with prior reward knowledge.

-**[Beyond Imitation: Self-Improving Robot Policies via Off-Policy Q-Planning](https://arxiv.org/abs/2608.21204)** (2026) — Successful and failed rollouts update a Q-function for action selection while behavior-cloning weights remain frozen.

#### 4. Knowledge Transfer and Training Procedure Improvement

Transfer retains useful capabilities across tasks; procedure improvement changes how later data or model updates are produced.

##### Cross-task transfer and retention

-**[SRSA: Skill Retrieval and Adaptation for Robotic Assembly Tasks](https://arxiv.org/abs/2503.04538)** (2025) — Retrieved source policies initialize and accelerate learning for new assembly tasks.

-**[EXTRACT: Efficient Policy Learning by Extracting Transferable Robot Skills from Offline Data](https://proceedings.mlr.press/v270/zhang25c.html)** (2025) — Offline robot experience yields transferable skills for efficient downstream policy learning.

-**[PRISE: LLM-Style Sequence Compression for Learning Temporal Action Abstractions in Control](https://arxiv.org/abs/2402.10450)** (2024) — Sequence compression learns reusable temporal action abstractions.

-**[LOTUS: Continual Imitation Learning for Robot Manipulation Through Unsupervised Skill Discovery](https://arxiv.org/abs/2311.02058)** (2024) — Unsupervised skill discovery and skill selection support continual imitation learning.

-**[Sparse Diffusion Policy: A Sparse, Reusable, and Flexible Policy for Robot Learning](https://arxiv.org/abs/2407.01531)** (2024) — Sparse policy modules support reuse and flexible adaptation across robot tasks.

-**[Knowledge Diversion for Efficient Morphology Control and Policy Transfer](https://arxiv.org/abs/2512.09796)** (2025) — Shared and task-specific controller components support efficient transfer across morphologies and tasks.

-**[Towards Human-like Physical Intelligence: Lifelong Vision-Language-Action Learning for Robotic Manipulation](https://arxiv.org/abs/2607.14852)** (2026) — Lifelong VLA learning studies the incorporation of new manipulation capabilities while retaining earlier knowledge.

-**[Robust Finetuning of Vision-Language-Action Robot Policies via Parameter Merging](https://arxiv.org/abs/2512.08333)** (2026) — Parameter merging balances new-task fine-tuning with retention of pretrained VLA behavior.

-**[Pretrained Vision-Language-Action Models are Surprisingly Resistant to Forgetting in Continual Learning](https://arxiv.org/abs/2603.03818)** (2026) — Examines resistance to forgetting during continual adaptation of pretrained VLAs.

-**[Can Vision-Language-Action Models Learn from Real-World Data Continually without Forgetting?](https://arxiv.org/abs/2605.26820)** (2026) — Studies continual real-world VLA learning and preservation of previously learned capabilities.

##### Data-preparation improvement

-**[RoboCoach: World Models as Active Coaches for Compositional Robot Skills](https://arxiv.org/abs/2609.39685)** (2026) — Imagined subtask failures guide demonstration requests and selective expert-adapter updates under matched data budgets.

-**[Curating Demonstrations using Online Experience](https://arxiv.org/abs/2503.03707)** (2025) — Online policy experience helps score and curate demonstrations for later learning.

-**[CUPID: Curating Data your Robot Loves with Influence Functions](https://arxiv.org/abs/2506.19121)** (2025) — Influence functions estimate which robot demonstrations are useful for the learner.

-**[DataMIL: Selecting Data for Robot Imitation Learning with Datamodels](https://arxiv.org/abs/2505.09603)** (2026) — Datamodels select prior data by predicted downstream-policy benefit rather than visual similarity alone.

-**[Re-Mix: Optimizing Data Mixtures for Large Scale Imitation Learning](https://arxiv.org/abs/2408.14037)** (2024) — Learner-dependent mixture optimization adjusts how multiple data sources contribute to imitation learning.

-**[RSIBench-Data: Benchmarking Data-Centric Research for Recursive Self-Improvement](https://arxiv.org/abs/2607.25886)** (2026) — A digital benchmark tests feedback-driven revision of training-data strategies under a fixed post-training stack.

##### Training-method and workflow improvement

-**[Eureka: Human-Level Reward Design via Coding Large Language Models](https://arxiv.org/abs/2310.12931)** (2024) — LLMs revise reward code using training feedback; reward-design search is distinct from changing the search procedure.

-**[EvoTrainer: Co-Evolving LLM Policies and Training Harnesses for Autonomous Agentic Reinforcement Learning](https://arxiv.org/abs/2606.03108)** (2026) — Digital-task feedback co-evolves LLM policies, diagnostics, and retained training-harness strategies.

-**[ENPIRE: Agentic Robot Policy Self-Improvement in the Real World](https://arxiv.org/abs/2606.19980)** (2026) — Real-robot rollouts guide retained revisions to training infrastructure, algorithm code, and recipes.

-**[HARBOR: A Harness Framework for Agentic Robot Reinforcement Learning](https://arxiv.org/abs/2606.08610)** (2026) — Agents automate simulation RL through gated stages, reusable artifacts, and experience from earlier training runs.

### Safety, Assurance, and Failure Monitoring

Safety-related works are collected here across training, control, execution, deployment, and
evaluation integrity. Failure detection is not a safety guarantee; digital reward-integrity
safeguards are not physical-safety evidence. Benchmark resources remain in the benchmark group.

#### Learning, Control, and Integrity Safeguards

- [PACT: Self-Evolving Physical Safety Alignment for Diffusion Policies in Embodied Manipulation](https://arxiv.org/abs/2606.08414) by Lingxuan Wu et al. 2026.
- [BenchShield: Formal Model-Backed Instrumentation for Reward Integrity in LLM-Agent Evaluation Infrastructure](https://arxiv.org/abs/2609.11028) by Shenghan Zheng et al. 2026.
- [Safe Continual Domain Adaptation after Sim2Real Transfer of Reinforcement Learning Policies in Robotics](https://arxiv.org/abs/2503.10949) by Josip Josifovski et al. 2025.
- [Preventing Undesirable Behavior of Intelligent Machines](https://doi.org/10.1126/science.aag3311) by Philip S. Thomas et al. 2019.
- [Control Barrier Function Based Quadratic Programs for Safety Critical Systems](https://doi.org/10.1109/TAC.2016.2638961) by Aaron D. Ames et al. 2017.
- [Constrained Policy Optimization](https://proceedings.mlr.press/v70/achiam17a.html) by Joshua Achiam et al. 2017.
- [High Confidence Policy Improvement](https://proceedings.mlr.press/v37/thomas15.html) by Philip S. Thomas et al. 2015.

#### Failure Monitoring and Deployment Checks

- [VLA-FAIL: Efficient Task Failure Detection for Finetuned Vision-Language-Action Models](https://arxiv.org/abs/2606.21386) by Florian Seligmann et al. 2026.
- [ROBOGATE: Adaptive Failure Discovery for Safe Robot Policy Deployment via Two-Stage Boundary-Focused Sampling](https://arxiv.org/abs/2603.22126) by Azuki Kim. 2026.
- [SAFE: Multitask Failure Detection for Vision-Language-Action Models](https://arxiv.org/abs/2506.09937) by Qiao Gu et al. 2025.
- [Unpacking Failure Modes of Generative Policies: Runtime Monitoring of Consistency and Progress](https://proceedings.mlr.press/v270/agia25a.html) by Christopher Agia et al. 2025.
- [Code-as-Monitor: Constraint-Aware Visual Programming for Reactive and Proactive Robotic Failure Detection](https://arxiv.org/abs/2412.04455) by Enshen Zhou et al. 2024.

`<a id="catalog-verification"></a>`

### Verification and Evaluation Methods

Verifier design, test-time verification, and learned evaluators. This group separates methods
for constructing or using judgments from benchmark resources for testing those judgments;
safety-specific monitors remain in [Safety and Assurance](#catalog-safety).

#### Robot Policy Verification

- [No Free Checker: A Survey of Verifiers for Robot Policies](https://arxiv.org/abs/2609.09250) by Yang Wan et al. 2026.
- [RoVer: Robot Reward Model as Test-Time Verifier for Vision-Language-Action Model](https://arxiv.org/abs/2510.10975) by Mingtong Dai et al. 2025.
- [RoboMonkey: Scaling Test-Time Sampling and Verification for Vision-Language-Action Models](https://arxiv.org/abs/2506.17811) by Jacky Kwok et al. 2025.

#### Evaluator Learning and Self-Verification in Digital Systems

- [Self-Trained Verification for Training- and Test-Time Self-Improvement](https://arxiv.org/abs/2605.30290) by Chen Henry Wu and Aditi Raghunathan. 2026.
- [Self-Taught Evaluators](https://arxiv.org/abs/2408.02666) by Tianlu Wang et al. 2024.
- [Meta-Rewarding Language Models: Self-Improving Alignment with LLM-as-a-Meta-Judge](https://arxiv.org/abs/2407.19594) by Tianhao Wu et al. 2024.

`<a id="catalog-benchmarks"></a>`

### Benchmarks, Datasets, and Evaluation Resources

A single home for benchmark-related references, regardless of where they appear in the manuscript.
The **47 entries** below cover all **38 resources named in v33 Table 4**, plus nine other benchmark,
dataset, and evaluation-resource entries. These include GemBench from the task discussion, DROID
from the introduction, and HarnessDev, RSI-Exam, and PAST-Bench from Section 6.3.
See the [resource-to-paper coverage audit](docs/v33-benchmark-coverage.md) for the complete mapping
and the distinction between Table 4 entries and additional resources.

The subgroups distinguish task suites and datasets, robustness and physical-world evaluation,
feedback reliability, robot development, and digital research. Supporting frameworks and shared
datasets are included explicitly: not every entry is a standalone benchmark. A paper may contribute
both a method and a benchmark; resource aliases identify the benchmark without duplicating the paper.
Cited years follow v33 and may differ from first preprint dates.

#### Robot Task Suites and Shared Datasets

- [RoboCasa365: A Large-Scale Simulation Framework for Training and Benchmarking Generalist Robots](https://arxiv.org/abs/2603.04356) by Soroush Nasiriany et al. 2026.
- [RoboLab: A High-Fidelity Simulation Benchmark for Analysis of Task Generalist Policies](https://arxiv.org/abs/2604.09860) by Jenai Xuning Yang et al. 2026.
- [EmbodiedBench: Comprehensive Benchmarking Multi-modal Large Language Models for Vision-Driven Embodied Agents](https://proceedings.mlr.press/v267/yang25f.html) by Rui Yang et al. 2025.
- [ManiSkill3: GPU Parallelized Robotics Simulation and Rendering for Generalizable Embodied AI](https://arxiv.org/abs/2410.00425) by Stone Tao et al. 2025.
- [Towards Generalizable Vision-Language Robotic Manipulation: A Benchmark and LLM-guided 3D Policy](https://arxiv.org/abs/2410.01345) by Ricardo Garcia et al. 2025. *Benchmark resource: GemBench; discussed in v33 Section 2 (p. 10).*
- [VLABench: A Large-Scale Benchmark for Language-Conditioned Robotics Manipulation with Long-Horizon Reasoning Tasks](https://openaccess.thecvf.com/content/ICCV2025/html/Zhang_VLABench_A_Large-Scale_Benchmark_for_Language-Conditioned_Robotics_Manipulation_with_Long-Horizon_ICCV_2025_paper.html) by Shiduo Zhang et al. 2025.
- [BEHAVIOR-1K: A Human-Centered, Embodied AI Benchmark with 1,000 Everyday Activities and Realistic Simulation](https://arxiv.org/abs/2403.09227) by Chengshu Li et al. 2024.
- [DROID: A Large-Scale In-The-Wild Robot Manipulation Dataset](https://www.roboticsproceedings.org/rss20/p120.html) by Alexander Khazatsky et al. 2024. *Shared dataset cited in the v33 introduction; not a Table 4 benchmark.*
- [Open X-Embodiment: Robotic Learning Datasets and RT-X Models](https://arxiv.org/abs/2310.08864) by the Open X-Embodiment Collaboration. 2024.
- [LIBERO: Benchmarking Knowledge Transfer for Lifelong Robot Learning](https://arxiv.org/abs/2306.03310) by Bo Liu et al. 2023.
- [VIMA: Robot Manipulation with Multimodal Prompts](https://proceedings.mlr.press/v202/jiang23b.html) by Yunfan Jiang et al. 2023. *Benchmark resource: VIMA-Bench.*
- [CALVIN: A Benchmark for Language-Conditioned Policy Learning for Long-Horizon Robot Manipulation Tasks](https://arxiv.org/abs/2112.03227) by Oier Mees et al. 2022.
- [What Matters in Learning from Offline Human Demonstrations for Robot Manipulation](https://arxiv.org/abs/2108.03298) by Ajay Mandlekar et al. 2021. *Resource: robomimic.*
- [Meta-World: A Benchmark and Evaluation for Multi-Task and Meta Reinforcement Learning](https://proceedings.mlr.press/v100/yu20a.html) by Tianhe Yu et al. 2020.
- [robosuite: A Modular Simulation Framework and Benchmark for Robot Learning](https://arxiv.org/abs/2009.12293) by Yuke Zhu et al. 2020.
- [RLBench: The Robot Learning Benchmark &amp; Learning Environment](https://arxiv.org/abs/1909.12271) by Stephen James et al. 2019.

#### Robustness and Physical-World Evaluation

- [RoboDojo: A Unified Sim-and-Real Benchmark for Comprehensive Evaluation of Generalist Robot Manipulation Policies](https://arxiv.org/abs/2607.04434) by Tianxing Chen et al. 2026.
- [RoboTwin 2.0: A Scalable Data Generator and Benchmark with Strong Domain Randomization for Robust Bimanual Robotic Manipulation](https://proceedings.mlr.press/v306/chen26j.html) by Tianxing Chen et al. 2026.
- [VLA-Arena: An Open-Source Framework for Benchmarking Vision-Language-Action Models](https://proceedings.mlr.press/v306/zhang26cp.html) by Borong Zhang et al. 2026.
- [AutoEval: Autonomous Evaluation of Generalist Robot Manipulation Policies in the Real World](https://arxiv.org/abs/2503.24278v1) by Zhiyuan Zhou et al. 2025.
- [LIBERO-Plus: In-depth Robustness Analysis of Vision-Language-Action Models](https://arxiv.org/abs/2510.13626) by Senyu Fei et al. 2025.
- [LIBERO-PRO: Towards Robust and Fair Evaluation of Vision-Language-Action Models Beyond Memorization](https://arxiv.org/abs/2510.03827) by Xueyang Zhou et al. 2025.
- [REALM: A Real-to-Sim Validated Benchmark for Generalization in Robotic Manipulation](https://arxiv.org/abs/2512.19562) by Martin Sedlacek et al. 2025.
- [RoboArena: Distributed Real-World Evaluation of Generalist Robot Policies](https://proceedings.mlr.press/v305/atreya25a.html) by Pranav Atreya et al. 2025.
- [RoboTwin: Dual-Arm Robot Benchmark with Generative Digital Twins](https://arxiv.org/abs/2504.13059) by Yao Mu et al. 2025.
- [Evaluating Real-World Robot Manipulation Policies in Simulation](https://arxiv.org/abs/2405.05941) by Xuanlin Li et al. 2024. *Evaluation resource: SIMPLER.*
- [THE COLOSSEUM: A Benchmark for Evaluating Generalization for Robotic Manipulation](https://arxiv.org/abs/2402.08191) by Wilbert Pumacay et al. 2024.

#### Feedback Reliability and Model-Based Evaluation

- [dWorldEval: Scalable Robotic Policy Evaluation via Discrete Diffusion World Model](https://arxiv.org/abs/2604.22152) by Yaxuan Li et al. 2026.
- [FailBench: How Reliable Are VLMs at Judging Robot Task Success?](https://arxiv.org/abs/2609.03611v1) by Zaruhi Navasardyan et al. 2026.
- [GigaWorld-1: A Roadmap to Build World Models for Robot Policy Evaluation](https://arxiv.org/abs/2607.02642) by the GigaWorld Team. 2026.
- [Robometer: Scaling General-Purpose Robotic Reward Models via Trajectory Comparisons](https://arxiv.org/abs/2603.02115) by Anthony Liang et al. 2026. *Benchmark resource in v33: RBM-EVAL.*
- [RoboReward: General-Purpose Vision-Language Reward Models for Robotics](https://arxiv.org/abs/2601.00675) by Tony Lee et al. 2026. *Benchmark resource in v33: RoboRewardBench.*
- [SC3-Eval: Evaluating Robot Foundation Models via Self-Consistent Video Generation](https://arxiv.org/abs/2606.18610) by Wei-Cheng Tseng et al. 2026.
- [WorldEval: World Model as Real-World Robot Policies Evaluator](https://arxiv.org/abs/2505.19017) by Yaxuan Li et al. 2025.

#### Robot Engineering and Development Benchmarks

- [CaP-X: A Framework for Benchmarking and Improving Coding Agents for Robot Manipulation](https://proceedings.mlr.press/v306/fu26u.html) by Letian Fu et al. 2026. *Benchmark resource in v33: CaP-Bench.*
- [From Digital to Physical: Digital Agents as Autonomous Coaches for Physical Intelligence](https://arxiv.org/abs/2601.21570) by Zixing Lei et al. 2026. *Associated with the EmboCoach-Bench entry in the manuscript; preserve the paper/benchmark version distinction.*
- [RLE-Bench: A Qualifying Exam for Coding Agents as Robot Learning Engineers](https://arxiv.org/abs/2609.34210) by Haitong Ma et al. 2026.

#### Digital Research and Improvement Benchmarks

- [AI4AI-Bench: Benchmarking LLM Agents in Algorithmic Design for Recursive Self-Improvement](https://arxiv.org/abs/2608.20318) by Yizhe Chi et al. 2026.
- [HarnessDev: Can LLMs Create and Evolve Their Own Agent Harness?](https://arxiv.org/abs/2609.01437) by Yuhao Wu et al. 2026.
- [PAST-Bench: Benchmarking the Foundations of Recursive Self-Improvement in Personal Agents](https://arxiv.org/abs/2608.04003) by Shuhan Xue et al. 2026.
- [RSI-Exam: Benchmarking Recursive Self-Improvement through Executable Research](https://github.com/aiming-lab/RSI-Exam) by RSI-Exam Team. 2026. *Repository resource cited by the manuscript.*
- [RSIBench-Data: Benchmarking Data-Centric Research for Recursive Self-Improvement](https://arxiv.org/abs/2607.25886) by Fanqing Meng et al. 2026.
- [MLGym: A New Framework and Benchmark for Advancing AI Research Agents](https://arxiv.org/abs/2502.14499) by Deepak Nathani et al. 2025. *Benchmark resource: MLGym-Bench.*
- [MLRC-Bench: Can Language Agents Solve Machine Learning Research Challenges?](https://arxiv.org/abs/2504.09702) by Yunxiang Zhang et al. 2025.
- [RE-Bench: Evaluating Frontier AI R&amp;D Capabilities of Language Model Agents against Human Experts](https://proceedings.mlr.press/v267/wijk25a.html) by Hjalmar Wijk et al. 2025.
- [MLAgentBench: Evaluating Language Agents on Machine Learning Experimentation](https://proceedings.mlr.press/v235/huang24y.html) by Qian Huang et al. 2024.
- [MLE-bench: Evaluating Machine Learning Agents on Machine Learning Engineering](https://arxiv.org/abs/2410.07095) by Jun Shern Chan et al. 2024.

`<a id="open-questions"></a>`

## Open Questions `<sub><a href="#readme-top">`top `</a></sub>`

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

`<a id="license"></a>`

## License `<sub><a href="#readme-top">`top `</a></sub>`

This repository is released under the [MIT License](LICENSE). Linked papers and third-party
materials remain subject to their respective licenses.
