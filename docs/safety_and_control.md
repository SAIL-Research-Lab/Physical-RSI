# Safety and Control of Physical RSI

[Back to the repository](../README.md) · [Safety paper catalog](../README.md#catalog-safety) · [Paper](https://arxiv.org/abs/2610.18842)

A robot can improve its task performance while making its next learning cycle less safe. Changes to the execution system can alter which states it visits, while changes to the improvement procedure can alter which trials it runs and which updates it retains. Environmental drift can invalidate evidence for either one.

This guide follows Section 5 of the paper. It organizes the cited work around a common question: **which safety evidence remains valid after a change, and what must be reassessed before further operation?** The literature provides guarantees and empirical results for particular components and update families. Those results do not establish safety for arbitrary revisions of the improvement procedure.

## Reading map

1. [Safe exploration and continual adaptation](#safe-exploration-and-continual-adaptation): constrain the experience-gathering process and check whether safety survives adaptation.
2. [Safe transfer and update acceptance](#safe-transfer-and-update-acceptance): distinguish evidence for retaining an update from evidence for deploying it.
3. [Runtime assurance under environmental drift](#runtime-assurance-under-environmental-drift): connect detection to a feasible intervention or recovery action.
4. [Oversight of an evolving improvement procedure](#oversight-of-an-evolving-improvement-procedure): protect requirements, evaluation, and interruption as update procedures change.
5. [Safety evidence across generations](#safety-evidence-across-generations): track assumptions, adaptive evaluation effects, and cumulative physical exposure.

The [README catalog](../README.md#paper-catalog) keeps each work under its primary topic. This guide also connects relevant work cataloged under harness adaptation, model training, and evaluation. The method summaries describe the cited results. The reassessment guidance and evidence table are our synthesis for Physical RSI.

## Framework and evidence boundaries

The paper distinguishes the execution system `M = (Θ, H)` from its improvement procedure `Φ = (Adapt, Train, Ver)`. Runtime safeguards are part of `M`, with learned parameters in `Θ` and control or switching code in `H`. Mechanisms within the improvement procedure that generate or internally verify inherited updates belong to `Φ`. The independent evaluator `E` and scoring criterion `Q` remain protected from modification by `Φ`.

Three decisions require different evidence:

| Decision | What the evidence must support |
| --- | --- |
| **Acceptance** | Whether an update should be retained. Internal `Ver` judges execution-system and improvement-method updates. Revisions to `Ver` require external assessment through the systems retained under competing verifier versions. |
| **Release** | Whether a particular system may operate under specified conditions and safeguards, including restricted trials used to gather evidence. |
| **Recursive gain** | Whether successive, autonomously inherited procedure revisions produce better subsequent improvements across tasks under matched conditions and protected independent evaluation. |

Physical grounding can come from interaction in a physics simulator or the real world, including for an L5 claim. Learned world-model predictions alone do not establish this grounding. Separately, simulation evidence does not by itself establish that a hardware deployment is safe. Neither passing safety checks nor obtaining a higher task score settles all three decisions above.

## Safe Exploration and Continual Adaptation

**Safety during learning.** A policy that is safe after training may still cause harm while gathering experience. [A Review of Safe Reinforcement Learning](https://doi.org/10.1109/TPAMI.2024.3457538) distinguishes methods and their assumptions. For each result, identify the constrained quantity, when it is constrained, and what kind of evidence supports the claim.

- [Constrained Policy Optimization](https://proceedings.mlr.press/v70/achiam17a.html) approximately maintains expected-cost limits during policy updates. An expected-cost constraint can still permit individual violations.
- [SafeVLA](https://proceedings.neurips.cc/paper_files/paper/2025/hash/e185c7be603426028c32ae1003a59d78-Abstract-Conference.html) applies constrained learning to unsafe behaviors of vision-language-action models. [PCRPO](https://doi.org/10.1609/aaai.v38i19.30102) addresses conflicts between reward and safety gradients, while [ROSCOM](https://doi.org/10.1109/TASE.2024.3431530) studies robust safe learning with stochastic constraints. Their relevance to a deployment depends on whether the modeled costs capture its physical hazards.

**Safety retention after adaptation.** [Safe Continual Domain Adaptation (SCDA)](https://arxiv.org/abs/2503.10949) combines safe RL with a penalty on changes to important policy parameters after varied simulation pretraining. Robot experiments provide evidence of reduced forgetting and controlled average costs under tested conditions. Continuing to fit reward and cost estimators does not by itself establish a meta-level update. In simulated non-stationary benchmarks, [Safe Continual Reinforcement Learning](https://arxiv.org/abs/2604.19737) finds that reducing forgetting does not reliably preserve safety performance. Evaluate both previous and current operating conditions, including the adaptation trials themselves.

**Exploration with supported return paths.** [Gaussian-process controller optimization](https://doi.org/10.1109/ICRA.2016.7487170) restricts quadrotor trials to settings predicted to satisfy a safety threshold. [Sequential safe exploration](https://papers.nips.cc/paper_files/paper/2016/hash/9a49a25d845a483fae4be7e341368e36-Abstract.html) additionally accounts for reachability and returnability. [Stability-based safe model learning](https://papers.nips.cc/paper_files/paper/2017/hash/766ebcd59621e305170616ba3d3dac32-Abstract.html) supports joint improvement of a controller and its estimated safe region under regularity and uncertainty assumptions.

After a system or procedure update, reassess the affected cost estimates, uncertainty bounds, and return paths. Environmental drift may shrink the supported region. If no available trial supports safe continuation under the stated assumptions, physical exploration must pause.

## Safe Transfer and Update Acceptance

**Transfer assumptions travel with the evidence.** [Sim-to-Lab-to-Real](https://doi.org/10.1016/j.artint.2022.103811) combines a backup policy, shielding, and statistical generalization bounds. Its generalization argument assumes that laboratory and deployment environments follow the same distribution. [Robust Transfer of Safety-Constrained RL Agents](https://proceedings.iclr.cc/paper_files/paper/2025/file/e59bf9a9077c361ed57180fc79c5b8d8-Paper-Conference.pdf) uses a guide whose uncertainty tolerance covers the target environment. Its expected-cost guarantee depends on compatible action spaces and a state mapping that preserves safety conditions. An encoder or action-interface change can invalidate these assumptions even when the task remains the same.

**Acceptance needs evidence beyond relative improvement.** Several methods support parts of this decision:

- [High Confidence Policy Improvement](https://proceedings.mlr.press/v37/thomas15.html) bounds the probability of accepting a policy below a return threshold. This is a return claim, not automatically a physical-safety claim.
- [The Seldonian framework](https://doi.org/10.1126/science.aag3311) tests specified behavioral constraints and can return no solution when evidence is insufficient. The constraints must capture the behavior that matters.
- [COptiDICE](https://openreview.net/forum?id=FLA55mBee6Q) addresses offline constrained learning, while [CVaR-based optimization](https://proceedings.neurips.cc/paper/2015/hash/64223ccf70bbb65a3a4aceac37e21016-Abstract.html) accounts for tail outcomes beyond average return. Both depend on how risks and costs are represented.
- [Doubly robust off-policy evaluation](https://proceedings.mlr.press/v48/jiang16.html) supports value estimation from logs. [Safe Policy Improvement with Baseline Bootstrapping](https://proceedings.mlr.press/v97/laroche19a.html) limits changes where evidence is sparse. Data coverage and estimation assumptions remain essential, and [work on non-stationary MDPs](https://proceedings.neurips.cc/paper/2020/hash/680390c55bbd9ce416d1d69a9ab4760d-Abstract.html) addresses the additional difficulty of changing conditions.

Improving over an unsafe baseline is insufficient. For release, assess the policy, observation processing, action interface, monitor, and backup controller together. Harness changes can alter skill preconditions, invocation timing, and handover states. Model updates can break compatibility with the retained harness. Hardware assessment also needs sensing errors, actuator limits, and control timing. [Measurement-robust control barrier functions](https://arxiv.org/abs/2104.14030) illustrate how bounded sensing errors can enter such an assessment.

Record the conditions under which operation is permitted. A higher score under `E,Q` does not replace this evidence, and a previously accepted component does not automatically make a new component combination safe.

## Runtime Assurance under Environmental Drift

**Enforcement requires a feasible response.** Runtime assurance restricts proposed actions or switches to a backup before safe continuation becomes infeasible.

- [Control barrier functions](https://doi.org/10.1109/TAC.2016.2638961) preserve a safe region under model and control-feasibility assumptions. [Continuous-action safety layers](https://arxiv.org/abs/1801.08757) and [learning with barrier functions](https://ojs.aaai.org/index.php/AAAI/article/view/4213) incorporate learned constraint or dynamics information into action correction.
- [Reachability-based safety](https://doi.org/10.1109/TAC.2018.2876389) accounts for modeled disturbances. [Predictive safety filters](https://doi.org/10.1016/j.automatica.2021.109597) check future constraints and safe continuation, with [learning-based racing control](https://doi.org/10.1109/LRA.2021.3097073) providing an application.
- [Shielding](https://doi.org/10.1609/aaai.v32i1.11797) enforces logical specifications. [Realizable continuous-space shields](https://proceedings.mlr.press/v283/kim25c.html) also address whether those specifications can be satisfied with the available controls.
- [CBF-RL](https://arxiv.org/abs/2510.14959) uses filtering during training. Removing a filter removes its direct runtime enforcement. Logs should distinguish proposed actions from executed actions, since frequent corrections can hide an unsafe underlying policy.

**Detection is not enforcement.** A warning is useful only if there is enough time and control authority to respond.

- [Statistically grounded visual failure prediction](https://www.roboticsproceedings.org/rss18/p042.pdf) bounds prediction errors for defined outcomes. [Uncertainty-based failure detection for LLM planners](https://arxiv.org/abs/2406.00430) examines warning signals from uncertain judgments.
- [Sentinel](https://proceedings.mlr.press/v270/agia25a.html) monitors consistency and progress. [SAFE](https://proceedings.neurips.cc/paper_files/paper/2025/hash/392d0d05e2f514063e6ce6f8b370834c-Abstract-Conference.html) detects failures from policy features, but its calibration concerns false alarms on successful trajectories. It does not establish a bound on missed failures or guarantee safe intervention.
- [DoReMi](https://sites.google.com/view/doremi-paper) and [Code-as-Monitor](https://openaccess.thecvf.com/content/CVPR2025/html/Zhou_Code-as-Monitor_Constraint-aware_Visual_Programming_for_Reactive_and_Proactive_Robotic_Failure_CVPR_2025_paper.html) connect execution deviations to replanning or geometric checks. [FIPER](https://arxiv.org/abs/2510.09459) and [FIDEL](https://arxiv.org/abs/2604.13788v1) study distinctions between unusual observations and likely failures.

Policy and encoder updates can change the visited states and the features on which detection depends. Recalibration therefore needs evidence from the updated system. Raising alarm thresholds solely to reduce interventions can conceal declining safety.

**Recovery depends on the current physical state.** [SOTER](https://escholarship.org/uc/item/78g5j78r) and [Neural Simplex](https://www3.cs.stonybrook.edu/~stoller/papers/nfm2020.pdf) combine switching rules with backup control. [Recovery RL](https://ieeexplore.ieee.org/document/9392290/) learns recovery behavior from estimates of future violations. These approaches require a recoverable state and an effective controller. Restoring earlier software cannot reverse a mechanical fault or changed friction.

[Leave No Trace](https://openreview.net/forum?id=S1vuO-bCW), [MEDAL](https://proceedings.mlr.press/v162/sharma22a.html), and [Self-Improving Robots](https://proceedings.mlr.press/v229/sharma23b.html) develop resetting or return behaviors for autonomous practice. These behaviors also require physical trials and can fail. In shared workspaces, [multirobot barrier certificates](https://doi.org/10.1109/TRO.2017.2659727) address coordinated safety under specified control assumptions.

After changes to a policy, monitor, or backup, jointly check missed hazards, response delays, handover states, and recovery feasibility. The improvement procedure must carry these checks into later updates. Abrupt environmental changes outside the assumed disturbance bounds remain outside the guarantee.

## Oversight of an Evolving Improvement Procedure

**Assess how successors are produced.** A revision to `Adapt`, `Train`, or `Ver` can change trial selection and inheritance decisions. Its safety assessment must cover the development trials and subsequent systems it produces. Omitting interventions from experience records can make assisted success appear to establish unassisted policy safety.

[Verifiably Safe Off-Model Reinforcement Learning](https://doi.org/10.1007/978-3-030-17462-0_28) provides a concrete starting point for structured updates. It revises models, control logic, and associated proofs, then eliminates inconsistent models during operation. Its safety result requires an accurate model to remain in the candidate set. This supports the specified update family, not arbitrary revisions of `Φ`.

**Protect the requirements and the evaluator.** Updated cost estimators must continue to represent the protected hazards. Shared errors are a concern when one model both proposes actions and evaluates their safety. `Ver` can drift toward accepting updates that pass local checks while increasing physical risk. Specify safety criteria for accepting verifier revisions before testing and protect them from candidate modification. Assess competing verifier versions through their retained systems using protected `E,Q`.

[Indirect prompt injection](https://arxiv.org/abs/2302.12173) shows how external content can redirect an agent. Logs and retrieved material read by `Φ` must not acquire authority to change safety requirements or disable stopping mechanisms.

**Separate human safety control from autonomous inheritance.** Human assistance has several roles:

- [HG-DAgger](https://arxiv.org/abs/1810.02890), [SIRIUS](https://arxiv.org/abs/2211.08416), [HIL-SERL](https://arxiv.org/abs/2410.21845), and [ConRFT](https://www.roboticsproceedings.org/rss21/p019.html) use human feedback or interventions for learning. [Learning from suboptimal interventions](https://arxiv.org/abs/2512.24288v1) addresses limitations of that guidance. Emergency stops should remain distinguishable from successful demonstrations.
- [ThriftyDAgger](https://proceedings.mlr.press/v164/hoque22a.html), [Fleet-DAgger](https://proceedings.mlr.press/v205/hoque23a.html), and [KnowNo](https://proceedings.mlr.press/v229/ren23a.html) allocate human attention or request help. Reduced supervision demand does not ensure help arrives before danger.
- [AutoRT](https://arxiv.org/abs/2401.12963) and [SOP](https://arxiv.org/abs/2601.03044v1) provide supervision or intervention infrastructure. [Safely Interruptible Agents](https://auai.org/uai2016/proceedings/papers/68.pdf) and [The Off-Switch Game](https://www.ijcai.org/Proceedings/2017/0032) address incentives around interruption. Physical stopping additionally depends on sensing, communication, actuation, and response time.

Under the paper's taxonomy, workflows whose retained improvement depends on human intervention or labeling during improvement belong to L0. Direct human edits and human selection of retained updates must also be distinguished from autonomous inheritance. Authorization for physical operation is a separate decision. Record operational safety interventions and human contributions to learning or update selection separately so that the autonomy claim can be assessed.

Before retaining a procedure revision, check how it changes trial selection, interpretation of interventions, and update acceptance. Preserve protected requirements and effective stopping mechanisms. Replacing a safeguard also requires a compatible controller and a recoverable state at handover.

## Safety Evidence across Generations

Each generation needs records linking system and procedure versions to operating conditions, interventions, and outcomes. The following table summarizes what changes can invalidate earlier evidence. Its reassessment column is our synthesis, not an additional guarantee from the cited methods.

| Change and example | Evidence and limits | Reassess before reuse |
| --- | --- | --- |
| Policy adaptation, as in SCDA | Empirical cost control and reduced forgetting in tested conditions. | Costs under previous and current conditions, including adaptation trials. |
| Domain transfer, as in Sim-to-Lab-to-Real and robust safe transfer | Statistical or expected-cost bounds under transfer assumptions. | Target coverage, state mappings, and action compatibility. |
| Dynamics or interfaces, as in barrier-function control | Safe-region preservation under valid models and feasible control. | Sensing errors, actuator limits, timing, and handover states. |
| Monitors or recovery, as in SAFE and Recovery RL | False-alarm calibration or learned recovery estimates. Intervention can still fail. | Feature validity, missed hazards, response delays, and recovery feasibility. |
| Structured updates, as in Fulton and Platzer | Proof-preserving model and controller revisions within a specified family. | Whether an accurate model remains in the candidate set and proof assumptions and controller compatibility still hold. |
| Repeated selection, as in adaptive data analysis | Statistical validity depends on controlling adaptive feedback reuse. | Error control across rounds and separation of development feedback from independent evaluation. Account for physical exposure separately. |

### Risk across rounds

A bound for one round does not establish a lifetime guarantee. If `V_k` denotes a physical violation in round `k`, and valid bounds `Pr(V_k) ≤ δ_k` hold for the adaptive process, then

$$
\Pr\!\left(\bigcup_{k=1}^{K} V_k\right) \leq \sum_{k=1}^{K} \delta_k.
$$

The union bound needs no independence, but the per-round bounds must remain valid for the adaptive process. Estimates based on obsolete models cannot supply them. Count exposure from rejected trials, resetting, and recovery, and track wear that changes later safety assumptions. Distinguish the risk incurred while developing a procedure revision from the risk incurred during its subsequent use.

False acceptance and physical harm are different events. [Generalization in Adaptive Data Analysis and Holdout Reuse](https://proceedings.neurips.cc/paper/2015/hash/bad5f33780c42f2588878a9d07405083-Abstract.html) addresses the statistical consequences of adaptive feedback reuse. If judgments from `Ver` or `E` enter experience records and influence later proposals or acceptance, that evidence cannot also be treated as untouched final evaluation. Use fresh evidence or an appropriate statistical correction. Protecting evaluation tasks and `Q` from direct access or modification does not by itself remove adaptive selection effects.

### Evaluation after change

Report violation frequency and severity, near misses, missed failures, intervention delays, and recovery success throughout adaptation. Include rejected trials and resets. Test immediately after updates, revisit previous conditions, and compare fixed and updated systems under both stable and drifting conditions.

L5 additionally requires independently established recursive gain across tasks. Follow the paper's matched comparisons of procedure revisions from the same starting system and experience under matched tasks and resource budgets. For safety, also match the safety rules, stopping and reset conditions, and arrangements for human oversight and operational authorization. Record actual interventions and deviations from the comparison conditions. Repeated trials help account for physical variability.

## Open Direction: Safety across Recursive Updates

The challenge is to extend component-level safety results to inherited changes in the procedure that generates and accepts updates. Structured proof-preserving updates provide one starting point, but do not cover arbitrary changes to `Φ` or drift in `Ver`. Revalidating every assumption after every revision is costly, and hardware trials can themselves cause harm. Selective reassessment should identify affected assumptions, reuse evidence that remains valid, and focus the available trial budget on unresolved safety questions. It must also maintain valid risk bounds under adaptive updates, preserve protected requirements and effective interruption, and account for rejected trials, resets, and recovery. Matched, independent comparisons can then test whether recursive gain can be established under these safety constraints.

This is an open direction scoped to the reviewed evidence. It builds on existing verification, safe learning, and runtime-assurance methods rather than claiming that selective reassessment or safety under adaptation has never been studied.

Related reading: [model training](model_training.md), [verification and evaluation](../README.md#catalog-verification), and [the manuscript reference index](paper-reference-index.md).
