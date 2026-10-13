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
