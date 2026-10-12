# v34：Paper Catalog 分类—章节映射与参考文献核对

> **对齐前快照：** 本报告及 `v34-catalog-audit.csv`、`v34-reference-audit.csv` 记录原来的116项目录，保留作为变更依据。当前README已按v34对齐为278项，覆盖292条原始书目记录；最新对应关系见 [参考索引](paper-reference-index.md) 和 [对齐后CSV](v34-catalog-aligned.csv)。

核对日期：2026-10-12。对象：本地 `IEEE_TPAMI__Physical_RSI-34.pdf` 与当前 `README.md` 的 Paper Catalog。
本报告不修改 README、不提交、不推送。页码均为 PDF 从第一页开始的物理页码。

## 1. 结论与计数口径

**116 不是 v34 参考文献总数，而是 README 的精选目录条目数。**

| 对象 | 数量 | 口径 |
|---|---:|---|
| README Paper Catalog | 116 | 6 个一级主题、27 个二级分类中的论文/资源条目 |
| PDF 参考文献表 | 292 | 第31–54页的独立书目记录；以292个 `cite.` 目标和提取记录交叉核对 |
| 已确认重复组 | 13 | 12组各2条、1组3条，共27条记录代表13项工作 |
| 重复带来的额外记录 | 14 | 12×1 + 1×2 |
| 合并上述重复后的工作/资源 | 278 | 292−14；同一工作预印本/发表版合并，不把它称为278篇全部不同的研究论文 |

参考文献表首项是 Achiam 等人的 *Constrained Policy Optimization*（2017），末项是 Zweiger 等人的 *Self-adapting language models*（2025）。292项均可找到正文引用链接；这不表示各项都是不同工作。

## 2. 分类与章节：主题对应，不是逐篇引用位置

| 一级主题 | 条目数 | 主要对应 |
|---|---:|---|
| Agent Harnesses and Execution | 15 | §3 Harness Adaptation for Physical RSI |
| Model Training and Adaptation | 18 | §4 Model Training of Physical RSI |
| Self-Improvement and Meta-Optimization | 17 | §3.4 与 §4.4；§2 提供定义和级别框架 |
| Safety and Assurance | 12 | §5 Safety and Control of Physical RSI |
| Verification and Evaluation Methods | 7 | §6.1 与 §6.2 |
| Benchmarks, Datasets, and Platforms | 47 | 主要 §6.3；共享训练数据主题对应 §4.1 |

下表是按当前类别语义给出的阅读映射，不能用来断言类内每一篇文献都在所列章节被引用。

### Agent Harnesses and Execution

| 当前二级分类 | 主题对应章节 | 解释/边界 |
|---|---|---|
| Memory and Knowledge Management | §3.2；补充 §3.3 | 执行记忆、知识维护与继承记录。 |
| Skill Libraries and Tool Construction | §3.2 | 执行技能、工具与可复用程序的构建；不是自动等于元改进。 |
| Planning and Workflows | §3.2；补充 §3 开篇 | 规划、编排和执行工作流。 |
| Failure Diagnosis and Execution Recovery | §3.1；补充 §5.3 | 更新前的故障诊断对应 §3.1；运行时监测和恢复对应 §5.3。 |

### Model Training and Adaptation

| 当前二级分类 | 主题对应章节 | 解释/边界 |
|---|---|---|
| Data Preparation and Generation | §4.1 | 经验生成、选择和数据准备。 |
| Imitation Learning and Generalist Policies | §4.2；补充 §4.3 | 模仿学习是训练方法；通用/VLA策略是被学习的模型对象。 |
| Reinforcement Learning and Autonomous Practice | §4.2；补充 §4.1 | 强化学习方法与自主采集/练习互相关联。 |
| World Models for Policy Learning | §4.3；补充 §4.2 | 模型对象属于 §4.3，自监督学习方法属于 §4.2。 |
| Reward Models and Learning Feedback | §4.3 | 奖励模型和用于训练的反馈。 |
| Continual Adaptation and Knowledge Transfer | §4.4 | 模型适应、知识积累与跨轮次迁移。 |

### Self-Improvement and Meta-Optimization

| 当前二级分类 | 主题对应章节 | 解释/边界 |
|---|---|---|
| Self-Modifying Systems and Recursive Improvement | §3.4；概念关联 §2.1–§2.3 | 递归和程序自修改的概念跨章；没有独立的“元优化”总章。 |
| Harness and Memory-Construction Optimization | §3.4 | 改变构建、诊断、选择未来 Harness/记忆的方法。 |
| Training Procedures, Curricula, and Algorithm Optimization | §4.4 | 改变训练流程、课程、算法或学习目标，而不只是训练得到新权重。 |

### Safety and Assurance

| 当前二级分类 | 主题对应章节 | 解释/边界 |
|---|---|---|
| Safe Exploration and Constrained Learning | §5.1 | 安全探索、约束学习与持续适应。 |
| Safe Transfer and Update Acceptance | §5.2 | 安全证据迁移、接受与发布的边界。 |
| Runtime Control and Failure Monitoring | §5.3 | 环境漂移下的运行时约束、监测、备份控制和恢复。 |
| Oversight and Integrity Protection | §5.4；补充 §5.2、§5.5 | 对演化程序的监督；完整性与跨代证据还涉及接受和记录。 |

### Verification and Evaluation Methods

| 当前二级分类 | 主题对应章节 | 解释/边界 |
|---|---|---|
| Robot Policy Verification and Candidate Selection | §6.1 | 候选实现有效性、修复有效性与能力保持。 |
| Learned Evaluators and Meta-Verification | §6.1；补充 §6.2 | 可学习验证器及其外部评价；当前三篇目录条目均未在v34参考文献表定位。 |

### Benchmarks, Datasets, and Platforms

| 当前二级分类 | 主题对应章节 | 解释/边界 |
|---|---|---|
| Shared Robot Datasets | 主题对应 §4.1；资源导航关联 §6.3 | DROID和Open X-Embodiment在此PDF的可定位引用为 §1；不能写成已列入 §6.3。 |
| Task and Long-Horizon Learning Benchmarks | §6.3；补充 §2.3 | 对应表4任务学习/表现/泛化；部分基准在级别讨论中被引用。 |
| Robustness and Transfer Evaluation | §6.3 | 对应表4鲁棒性与物理世界评估。 |
| Real-Robot and Sim-and-Real Evaluation Platforms | §6.3 | 对应表4物理世界评估；不是每个目录平台都在此节被引用。 |
| Feedback and Reward Evaluation | §6.3；补充 §4.3、§6.1 | 按基准角色归 §6.3；若讨论奖励模型本身则关联 §4.3。 |
| World-Model-Based Evaluation | §6.3；补充 §4.3 | 与使用世界模型训练策略的分类按用途区分。 |
| Robot Engineering Benchmarks | §6.3 | 对应表4 Robot Engineering & Development。 |
| Research Agent and Self-Improvement Benchmarks | §6.3 | 主要数字领域的研究代理与改进过程评估。 |

### 不能忽略的差别

- **主题映射不是引用位置。** EmbodiRSI 和 F4R 放在持续适应类合理，但本版PDF的引用/名称出现在 §6.2 的评价案例中，不应据此说它们在 §4.4 被讨论。
- **执行恢复不自动是继承更新。** DoReMi 的名称出现在 §2.3 的框架展示，带链接的正式引用位于 §5.3；故障诊断类与 §3.1 是主题关联。
- **目录含额外阅读。** Learned Evaluators and Meta-Verification 的 Self-Trained Verification、Self-Taught Evaluators、Meta-Rewarding 三项都未在本PDF的参考文献表定位。映射 §6.1 只能是主题关联。
- **共享数据不等于表4基准。** DROID 和 Open X-Embodiment 在本版的可定位引用为 §1。
- **当前分类没有覆盖章节的全部内容。** §3.3 的改进历史、§5.5 的跨代安全证据，以及 §6.2 的归因、保留、效率、自主性和受保护评价，不都有单独目录分类；§4.2 的自监督学习也没有独立子类。
- §2 是范围、架构、L0–L5 的分析框架，不是某一目录类的专属章节；目录类别不用于分配能力级别。

## 3. 13组重复书目记录

同名/同作者及共享标识符共同核对；同一工作预印本和发表版在这里视为一项。`Rxxx` 是本报告按书目顺序分配的审计编号，不是PDF原有编号。

| 工作 | 审计编号 | PDF页 | 合并减少记录数 |
|---|---|---|---:|
| Recursive self-improvement in AI: From bounded self-refinement to autonomous research loops | R024, R025 | 33 | 1 |
| ConRFT: A Reinforced Fine-tuning Method for VLA Models via Consistency Policy | R030, R031 | 33 | 1 |
| Thriftydagger: Budget-aware novelty and risk gating for interactive imitation learning | R091, R092 | 38 | 1 |
| Worldeval: World model as real-world robot policies evaluator | R130, R131 | 41 | 1 |
| Pretrained vision-languageaction models are surprisingly resistant to forgetting in continual learning | R140, R141 | 42 | 1 |
| ASPIRE: Agentic Skills Discovery for Robotics | R147, R148 | 42 | 1 |
| Precise and dexterous robotic manipulation via human-in-the-loop reinforcement learning | R149, R150 | 43 | 1 |
| Eureka: Human-level reward design via coding large language models | R153, R154 | 43 | 1 |
| What matters in learning from offline humandemonstrationsforrobotmanipulation | R155, R156 | 43 | 1 |
| Self-improving robots: Endto-end autonomous visuomotor reinforcement learning | R197, R198, R199 | 46 | 2 |
| Lifelong Robot Library Learning: Bootstrapping Composable and Generalizable Skills for Embodied Control with Language Models | R215, R216 | 47, 48 | 1 |
| RoboGen: Towards unleashing infinite data for automated robot learning via generative simulation | R230, R231 | 49 | 1 |
| Self-taught optimizer (STOP): Recursively self-improving code generation | R259, R260 | 51 | 1 |

## 4. README与PDF的覆盖关系

匹配以相同标识符、标题/作者和可识别的发表版本为依据，不要求年份和排版完全相同。RISE的README标题带前缀，PDF的发表版标题不带RISE前缀，已人工核对标题与作者后归为对应工作。

| 一级主题 | 目录总数 | 可对应工作 | 相关但版本不同 | 未在参考文献表定位 |
|---|---:|---:|---:|---:|
| Agent Harnesses and Execution | 15 | 8 | 0 | 7 |
| Model Training and Adaptation | 18 | 16 | 0 | 2 |
| Self-Improvement and Meta-Optimization | 17 | 10 | 1 | 6 |
| Safety and Assurance | 12 | 8 | 0 | 4 |
| Verification and Evaluation Methods | 7 | 2 | 0 | 5 |
| Benchmarks, Datasets, and Platforms | 47 | 44 | 0 | 3 |
| **合计** | **116** | **88** | **1** | **27** |

- 88项对应PDF的97条原始记录；原始记录数较多是因为PDF存在重复书目。
- 合并上述重复后，278项中有88项明确对应README，**190项没有同作匹配的目录条目**；这190项中包含1项Gödel Machines版本关系待统一的情况。
- 如果把Gödel Machines相关版本按同一研究线索计作已覆盖，则是89项覆盖、189项未覆盖。这里不把相关版本强行视为完全相同书目。
- 所以116项不仅没有收齐v34参考文献，而且还收录了该版参考文献表之外的补充阅读。

### Gödel Machines版本差异

README：*Godel Machines: Fully Self-Referential Optimal Universal Self-Improvers*，2007，书章DOI。
PDF R193：*Goedel Machines: Self-Referential Universal Problem Solvers Making Provably Optimal Self-Improvements*，2003，arXiv技术报告；§3.4引用。
二者属于同一研究线索，但当前标题、年份、出版载体不同；应保留这个版本差异，而不是直接宣称完全一致。

### 27项目录补充：未在本版参考文献表定位

- **Self-Evolving Embodied Agents via Skill-Harness Evolution** — Agent Harnesses and Execution / Skill Libraries and Tool Construction（README 第204行）。
- **Evolve Vision-Language-Action Model into an Agent with On-the-Fly Tool Use** — Agent Harnesses and Execution / Skill Libraries and Tool Construction（README 第206行）。
- **Zetta: An Efficient Closed-Loop Embodied Harness for Self-Evolving Physical Intelligence** — Agent Harnesses and Execution / Planning and Workflows（README 第215行）。
- **Grounded Vision-Language Interpreter for Long-Horizon Bimanual Task and Motion Planning** — Agent Harnesses and Execution / Planning and Workflows（README 第216行）。
- **Open-World Task and Motion Planning via Vision-Language Model Generated Constraints** — Agent Harnesses and Execution / Planning and Workflows（README 第217行）。
- **Trust the PRoC3S: Solving Long-Horizon Robotics Problems with LLMs and Constraint Satisfaction** — Agent Harnesses and Execution / Planning and Workflows（README 第218行）。
- **REFLECT: Summarizing Robot Experiences for Failure Explanation and Correction** — Agent Harnesses and Execution / Failure Diagnosis and Execution Recovery（README 第226行）。
- **Practice Makes Policies: Bootstrapping and Consolidating Robotic Capabilities from Zero Human Demonstrations** — Model Training and Adaptation / Reinforcement Learning and Autonomous Practice（README 第255行）。
- **Robot Self-Improvement via Human-Video Dynamics Models** — Model Training and Adaptation / World Models for Policy Learning（README 第266行）。
- **SBCO: Self-Supervised, Verifier-Grounded Harness Optimization for Planning Agents** — Self-Improvement and Meta-Optimization / Harness and Memory-Construction Optimization（README 第304行）。
- **GEAR: Genetic AutoResearch for Agentic Code Evolution** — Self-Improvement and Meta-Optimization / Training Procedures, Curricula, and Algorithm Optimization（README 第315行）。
- **Learning to Discover at Test Time** — Self-Improvement and Meta-Optimization / Training Procedures, Curricula, and Algorithm Optimization（README 第316行）。
- **CALM: Co-Evolution of Algorithms and Language Model for Automatic Heuristic Design** — Self-Improvement and Meta-Optimization / Training Procedures, Curricula, and Algorithm Optimization（README 第317行）。
- **Algorithm Discovery with LLMs: Evolutionary Search Meets Reinforcement Learning** — Self-Improvement and Meta-Optimization / Training Procedures, Curricula, and Algorithm Optimization（README 第318行）。
- **DrEureka: Language Model Guided Sim-to-Real Transfer** — Self-Improvement and Meta-Optimization / Training Procedures, Curricula, and Algorithm Optimization（README 第319行）。
- **PACT: Self-Evolving Physical Safety Alignment for Diffusion Policies in Embodied Manipulation** — Safety and Assurance / Safe Exploration and Constrained Learning（README 第332行）。
- **VLA-FAIL: Efficient Task Failure Detection for Finetuned Vision-Language-Action Models** — Safety and Assurance / Runtime Control and Failure Monitoring（README 第346行）。
- **ROBOGATE: Adaptive Failure Discovery for Safe Robot Policy Deployment via Two-Stage Boundary-Focused Sampling** — Safety and Assurance / Runtime Control and Failure Monitoring（README 第347行）。
- **BenchShield: Formal Model-Backed Instrumentation for Reward Integrity in LLM-Agent Evaluation Infrastructure** — Safety and Assurance / Oversight and Integrity Protection（README 第357行）。
- **RoVer: Robot Reward Model as Test-Time Verifier for Vision-Language-Action Model** — Verification and Evaluation Methods / Robot Policy Verification and Candidate Selection（README 第372行）。
- **RoboMonkey: Scaling Test-Time Sampling and Verification for Vision-Language-Action Models** — Verification and Evaluation Methods / Robot Policy Verification and Candidate Selection（README 第373行）。
- **Self-Trained Verification for Training- and Test-Time Self-Improvement** — Verification and Evaluation Methods / Learned Evaluators and Meta-Verification（README 第379行）。
- **Self-Taught Evaluators** — Verification and Evaluation Methods / Learned Evaluators and Meta-Verification（README 第380行）。
- **Meta-Rewarding Language Models: Self-Improving Alignment with LLM-as-a-Meta-Judge** — Verification and Evaluation Methods / Learned Evaluators and Meta-Verification（README 第381行）。
- **RoboLab: A High-Fidelity Simulation Benchmark for Analysis of Task Generalist Policies** — Benchmarks, Datasets, and Platforms / Task and Long-Horizon Learning Benchmarks（README 第401行）。
- **GigaWorld-1: A Roadmap to Build World Models for Robot Policy Evaluation** — Benchmarks, Datasets, and Platforms / World-Model-Based Evaluation（README 第449行）。
- **MLE-bench: Evaluating Machine Learning Agents on Machine Learning Engineering** — Benchmarks, Datasets, and Platforms / Research Agent and Self-Improvement Benchmarks（README 第474行）。

### PDF中已引用、目录未收录的代表性工作

下面仅列定位清楚的例子；完整逐项结果见CSV，不把这些例子当作完整缺失清单。

- R201，Reflexion: Language Agents with Verbal Reinforcement Learning（PDF第46页；可定位引用：§3.2）。
- R277，ExpeL: LLM Agents Are Experiential Learners（PDF第52页；可定位引用：§3.1, §3.2）。
- R062，AutoGuide: Automated Generation and Selection of Context-Aware Guidelines for Large Language Model Agents（PDF第36页；可定位引用：§3.1, §3.2）。
- R026，AutoManual: Constructing Instruction Manuals by LLM Agents via Interactive Environmental Learning（PDF第33页；可定位引用：§3.1, §3.2）。
- R128，PhysMem: Scaling Test-Time Memory for Embodied Physical Reasoning（PDF第41页；可定位引用：§3.2, §3.3）。
- R058，Promptbreeder: Self-Referential Self-Improvement Via Prompt Evolution（PDF第35页；可定位引用：§3.4）。
- R034，Diffusion policy: Visuomotor policy learning via action diffusion（PDF第34页；可定位引用：§4.2）。
- R233，One-step diffusion policy: Fast visuomotor policies via diffusion distillation（PDF第49页；可定位引用：§4.2）。
- R117，Openvla: An open-source vision-language-action model（PDF第40页；可定位引用：§4.2, §4.3）。
- R120，Safe Policy Improvement with Baseline Bootstrapping（PDF第40页；可定位引用：§5.2）。
- R043，SOTER: A Runtime Assurance Framework for Programming Safe Robotics Systems（PDF第34页；可定位引用：§5.3）。
- R049，Generalization in Adaptive Data Analysis and Holdout Reuse（PDF第35页；可定位引用：§5.4, §5.5, §7）。
- R163，Rsigym: A flexible environment for recursive selfimprovement（PDF第44页；可定位引用：§6.3）。
- R176，OpenRSI Index（PDF第45页；可定位引用：§6.3）。

## 5. 版本维护建议

1. 保持主题式目录，不需要改成逐section分组。若希望对照，可在类别说明中写“Related sections”，明确它不是逐篇引用位置。
2. 将116描述为精选 papers and resources，不要描述为v34的全部参考文献。
3. 若目标是完整收录，应先清理PDF参考文献重复键和版本问题，再补齐缺失工作；无需把所有书目都强塞进面向读者的精选目录。可另设完整Reference Index。
4. README中仍有v33式说明，需另做版本同步。例如当前目录对数字教练基准使用EmboCoach-Bench相关旧说明，而v34表4用RoboCoach-Bench；这属于名称/版本一致性问题，不应再增加一个重复条目。

## 6. 审计附件与方法边界

- `v34-reference-audit.csv`：292条原始记录，含去重组、完整原始书目文本、页码、bibkey、对应README条目、可定位引用章节。
- `v34-catalog-audit.csv`：当前116条目录记录，含一级/二级类别、匹配状态和对应书目。
- 引用章节由PDF内部引用链接与章节边界提取。图片中的纯文本名称、未带链接的叙述可能不在该字段内；跨页浮动图表也可能影响边界定位。报告中涉及的关键例外另核对正文名称。
- 这是本地两份文件之间的内容/书目一致性审计，不是对每篇外部论文的存在性、实验结论或出版元数据进行联网核验。
- 278是合并本次确认的13组重复后的结果；后续如发现其他别名、版本或错误元数据，仍可继续修订工作级去重。

README SHA-256：`16707290f47501bb7d6399af8619317c7565351046616d5f1bc2a1ffe7cac887`。
