---
name: metasurface-deeplearning-paper-writing
description: A Codex skill for writing, rewriting, reviewing, and polishing journal manuscripts on deep-learning-assisted metasurface and metamaterial absorber design.
---

# Metasurface DL Paper Writing Skill

## 1. Role and scope

You are assisting with a journal-level manuscript in the field of deep learning assisted metasurface/metamaterial absorber design. The target style should be close to high-quality photonics/materials papers, especially the writing logic of:

- Deep-learning-enabled inverse design of large-scale metasurfaces with full-wave accuracy.
- GLSaT: a spectral-aware transformer-based network enabling highly efficient and precise inverse design in metasurface optical filters.
- Related absorber/spectral-learning papers using surrogate models, inverse design, transformer/attention modules, spectral data, and experimental or full-wave validation.

Use this skill when the user asks you to:

- rewrite Introduction, Abstract, Methods, Results, Discussion, or Conclusion;
- polish English paragraphs for a deep-learning + metasurface absorber paper;
- produce Overleaf/LaTeX-ready manuscript text;
- organize figures, captions, contribution statements, or related work;
- make the paper sound like a rigorous journal article rather than a project report;
- check terminology consistency in a metasurface absorber manuscript.

The current user’s manuscript context is an ITO/PET/PMI multilayer metasurface absorber with deep-learning-assisted forward prediction and inverse design. The model predicts or optimizes absorption spectra. The manuscript should consistently use “absorption spectrum” or “absorptance response” unless the actual quantity being plotted is an S-parameter.

---

## 2. Core writing philosophy

Do not present the work as simply “using deep learning to design a metasurface.” Frame it as a physics-aware, spectrum-driven, data-driven design framework that addresses a specific bottleneck in absorber design.

The preferred logic is:

1. Metasurfaces/metamaterial absorbers provide compact and powerful electromagnetic wave manipulation.
2. Conventional design relies on parameter sweeps, empirical tuning, and repeated full-wave simulations.
3. As structural degrees of freedom, spectral objectives, and device constraints increase, this conventional forward-design process becomes inefficient.
4. Deep learning can serve as a fast surrogate model that maps structural parameters to electromagnetic responses.
5. Inverse design is more challenging because the mapping from spectra to structures is non-unique.
6. For absorbers, the spectrum is not a set of independent points; it contains local resonances, broadband trends, and frequency-correlated features.
7. A forward predictor, spectral-aware module, physical constraints, and CST/full-wave validation are therefore needed to make the inverse design reliable.

Keep every paragraph anchored to a clear problem, not to a list of techniques.

---

## 3. Content preservation rules

When rewriting or translating user-provided manuscript text:

- preserve the original order of arguments;
- preserve the original causal relationships and reasoning chain;
- preserve the information density and claim boundaries;
- do not introduce new scientific claims, results, citations, or methods;
- do not remove limitations merely to make the work appear stronger;
- do not substantially reorganize paragraphs or sections unless explicitly requested;
- improve terminology, grammar, coherence, and academic style without changing the underlying scientific meaning.

## 4. Preferred terminology

### 4.1 Use these terms consistently

| Concept | Preferred term |
|---|---|
| 超表面吸波体 | metasurface absorber |
| 超材料吸波体 | metamaterial absorber |
| 单元结构 | unit cell / meta-atom |
| 结构参数 | structural parameters / design variables |
| 吸收谱 | absorption spectrum / absorptance response |
| 目标吸收谱 | target absorption spectrum |
| 预测吸收谱 | predicted absorption spectrum |
| 正向预测网络 | forward prediction network |
| 替代模型 | data-driven surrogate model / learned surrogate |
| 逆向设计 | inverse design |
| 按需设计 | on-demand design |
| 谱序列相关性 | spectral correlation / spectral dependency |
| 局部频谱特征 | local spectral features |
| 宽带趋势 | broadband absorption trend |
| 非唯一逆问题 | non-unique inverse problem / one-to-many mapping |
| 物理约束 | physics-guided constraints / physically meaningful constraints |
| 加工约束 | fabrication-aware constraints / fabrication-feasible ranges |
| CST验证 | CST-based full-wave validation / CST-validated response |
| 消融实验 | ablation study |
| 基线对比 | baseline comparison |

### 4.2 Avoid or use carefully

- Avoid “S11 spectrum” as a target unless the plotted or predicted quantity is truly S11. For absorbers, prefer “absorption spectrum.”
- Avoid “reverse design”; use “inverse design.”
- Avoid “AI model magically designs”; use “data-driven surrogate,” “forward-guided inverse design,” or “target-spectrum-driven optimization.”
- Do not claim “full-wave accuracy” unless the manuscript includes quantitative CST/FDTD/FEM validation.
- Do not claim “large-scale aperiodic metasurface design” unless the method explicitly supports non-periodic arrays and has array-scale validation.
- Do not claim “experimental validation” unless real measured data are included.

---

## 5. Paper-level structure to emulate

### 5.1 Abstract structure

Use a six-part abstract:

1. **Field background**: metasurface absorbers enable compact and broadband electromagnetic control.
2. **Bottleneck**: conventional forward design relies on parameter sweeps and repeated full-wave simulations.
3. **Specific challenge**: broadband absorption spectra involve coupled resonances and strong spectral correlations; inverse design is non-unique.
4. **Proposed framework**: introduce the model, preferably as a forward prediction network plus inverse design/optimization framework.
5. **Validation**: report quantitative prediction accuracy, CST validation, inverse-designed samples, ablation/baseline comparisons, and experimental/RCS validation if available.
6. **Significance**: emphasize rapid, physically constrained, spectrum-driven design of metasurface absorbers.

Template:

> Metasurface absorbers offer a compact platform for tailoring electromagnetic absorption, yet their broadband design remains challenging because conventional parameter sweeps and full-wave simulations become increasingly inefficient as the number of structural degrees of freedom grows. Here, we propose a deep-learning-enabled framework for the forward prediction and inverse design of an ITO-based multilayer metasurface absorber. The framework employs a spectral-aware forward predictor to map physically constrained structural parameters to absorption spectra, while the inverse design stage is guided by the pretrained predictor to address the non-unique spectrum-to-structure mapping. Quantitative comparisons with CST simulations, ablation studies, and baseline models demonstrate [...]. This work provides a rapid and physically interpretable route toward target-spectrum-driven design of broadband microwave metasurface absorbers.

Replace bracketed content only with real results.

---

### 5.2 Introduction structure

Use a funnel-shaped Introduction with five paragraphs.

#### Paragraph 1: Metasurface capability and application relevance

Purpose: establish the importance of metasurfaces/metamaterial absorbers.

Template:

> Metasurfaces, composed of subwavelength meta-atoms arranged on a planar interface, have enabled unprecedented control over electromagnetic waves, including amplitude, phase, polarization, and spectral responses. Among them, metasurface absorbers are particularly attractive for broadband absorption, electromagnetic shielding, stealth, sensing, and energy-related applications because strong wave–matter interactions can be engineered within an ultrathin multilayer architecture.

#### Paragraph 2: Conventional design bottleneck

Purpose: move from general field to the pain point.

Template:

> Despite these advantages, the design of high-performance metasurface absorbers is still commonly performed through empirical modeling, parameter sweeps, and repeated full-wave simulations. Such a forward-design strategy can be effective for simple unit cells or single-frequency targets, but it becomes inefficient when broadband absorption, multilayer materials, resistive films, and multiple geometric parameters are simultaneously involved.

#### Paragraph 3: Deep learning and inverse design

Purpose: introduce the field, but do not overclaim.

Template:

> Deep learning has recently emerged as a promising tool for accelerating metasurface design by learning the nonlinear mapping between structural parameters and electromagnetic responses from pre-simulated datasets. Once trained, a forward prediction network can serve as a data-driven surrogate model, enabling rapid spectral evaluation compared with repeated full-wave simulations and facilitating inverse design from desired optical or electromagnetic responses to candidate structures.

#### Paragraph 4: Remaining gap for absorber spectral design

Purpose: state why existing DL methods are insufficient.

Template:

> However, broadband absorber design presents challenges that are not fully addressed by conventional fully connected or purely parameter-regression networks. First, the inverse mapping from a target absorption spectrum to structural parameters is intrinsically non-unique, since different configurations may produce similar spectral responses. Second, the absorption spectrum is a correlated sequence containing local resonance features and global broadband trends, rather than independent frequency points. Neglecting these spectral dependencies may lead to inaccurate reconstruction of resonance positions, bandwidths, and absorption levels.

#### Paragraph 5: This work and contributions

Purpose: concise contribution statement.

Template:

> In this work, we develop a deep-learning-assisted framework for the forward prediction and inverse design of a multilayer ITO/PET/PMI metasurface absorber. The framework integrates [...], [...], and [...]. The main contributions are threefold: (i) [...]; (ii) [...]; and (iii) [...].

Use three contributions maximum unless the user explicitly requests more.

---

## 6. Method section structure

Use a modular framework. Each module must answer: what is being modeled, why it is needed, and how it is validated.

### Recommended section order

1. **Metasurface absorber structure and parameterization**
   - Describe the ITO/PET/PMI multilayer structure.
   - Define all design variables and physical ranges.
   - Explain absorption calculation.
   - Use “structural parameters” or “design variables.”

2. **Dataset generation and full-wave simulation**
   - CST setup, boundary conditions, frequency range, sampling strategy.
   - Dataset split: training/validation/test.
   - Avoid vague statements like “many samples were generated.” Give numbers.

3. **Forward prediction network**
   - Define input and output mapping.
   - Emphasize surrogate-model role.
   - Explain attention/Conv1D/smooth-prior modules in terms of spectral dependencies, not just architecture names.

4. **Inverse design or inverse optimization**
   - State the non-uniqueness issue.
   - Explain why the pretrained forward network is used to guide inverse design.
   - If neural-adjoint optimization is used, say that structural parameters are optimized through gradients of the frozen forward predictor.

5. **Loss function and physical constraints**
   - Separate prediction loss, frequency-weighted loss, physics/smoothness loss, and constraint terms.
   - Connect every loss term to a physical or design purpose.

6. **Evaluation metrics**
   - MAE, MSE/RMSE, R², peak/resonance error, bandwidth error, average absorption in target band, CST back-validation error.

---

## 7. Results section logic

Do not present figures randomly. Use an escalating validation chain.

### 7.1 Forward prediction accuracy

- Compare predicted and CST/reference absorption spectra.
- Show multiple representative cases.
- Show distribution of error over all test samples and all frequency points.
- Use language such as “the agreement demonstrates the capability of the model to capture both local resonance features and broadband spectral trends.”

### 7.2 Inverse design performance

- Start from target absorption spectra.
- Show optimized/predicted spectra.
- Validate the inverse-designed parameters in CST.
- Discuss where errors occur: resonance shift, bandwidth narrowing, absorption drop.

### 7.3 Ablation study

- Each module should be removed separately.
- Explain what each removed module damages: convergence, local resonance accuracy, broadband smoothness, robustness.

### 7.4 Baseline comparison

Compare against FCN, MLP, CNN, Transformer-only, or other baselines. Avoid saying “our model is best” without metrics.

### 7.5 Physical interpretation

Explain the designed absorber in terms of impedance matching, ohmic loss in ITO layers, dielectric spacer effect, resonance coupling, and broadband loss mechanism. This is crucial for avoiding a purely algorithmic paper.

### 7.6 Device-level validation

If RCS reduction or physical measurements are included, place them after unit-cell prediction/inverse design. Present them as independent physical validation, not merely as another ML metric.

---

## 8. Figure and caption strategy

### Recommended figure sequence

1. **Figure 1**: Overall framework and unit-cell structure.
   - Include structure, parameters, data generation, forward model, inverse design flow.
2. **Figure 2**: Network architecture.
   - Show input structural parameters, spectral-aware feature extraction, decoder, output absorption spectrum.
3. **Figure 3**: Forward prediction results.
   - Representative spectra + error distribution.
4. **Figure 4**: Inverse design results.
   - Target vs optimized/predicted vs CST-validated spectra.
5. **Figure 5**: Ablation and baseline comparison.
   - Validation curves, error histograms, and model comparison.
6. **Figure 6**: Physical/device validation.
   - RCS reduction, array simulation, or experimental measurement.

### Caption style

Use captions that explain the function of the figure, not just list subpanels.

Template:

> Figure X. Forward prediction performance of the proposed model. (a–c) Representative comparisons between CST-simulated and network-predicted absorption spectra for test samples. (d) Absolute spectral error distribution over the full test set. (e) Comparison of prediction accuracy among the proposed model and baseline architectures. The results demonstrate that the proposed spectral-aware architecture captures both localized resonance features and broadband absorption trends.

Keep captions concise but complete.

---

## 9. Sentence patterns to emulate

Use these rhetorical patterns often, but adapt them to the real content.

### Problem framing

- “However, the conventional forward-design strategy becomes inefficient as the structural degrees of freedom and spectral constraints increase.”
- “This approximation reduces the computational burden but fails to capture [...].”
- “Despite these advances, several challenges remain for broadband absorber design.”
- “The inverse mapping is intrinsically non-unique, since multiple structures can yield similar spectral responses.”

### Method introduction

- “Here, we propose a deep-learning-enabled framework for [...].”
- “The framework integrates a forward prediction network as a learned surrogate model and an inverse optimization module for target-spectrum-driven design.”
- “To capture spectral dependencies, the model incorporates [...].”
- “To enforce physically meaningful designs, all predicted parameters are constrained within fabrication-feasible ranges.”

### Validation language

- “The agreement between the predicted and CST-simulated spectra demonstrates [...].”
- “The ablation results confirm that [...] contributes primarily to [...].”
- “Compared with baseline architectures, the proposed model achieves [...], indicating a better balance between prediction accuracy and computational efficiency.”
- “CST back-validation further verifies that the inverse-designed parameters retain the desired absorption behavior.”

### Discussion language

- “These results suggest that the model learns not only pointwise spectral values but also the underlying frequency-dependent response patterns.”
- “The residual discrepancy can be attributed to [...].”
- “Although the present framework is demonstrated on [...], the same strategy can be extended to [...].”

---

## 10. Claim control rules

When polishing or generating text, always check whether the claim is supported by the manuscript.

### Safe claims if data exist

- “rapid forward prediction” if inference time is reported or obviously much faster than CST.
- “CST-validated inverse design” if inverse-designed structures are re-simulated in CST.
- “spectral-aware prediction” if the model contains attention/Conv1D/sequence modules.
- “broadband absorption” if a continuous band reaches a defined absorption threshold.

### Unsafe claims unless explicitly proven

- “full-wave accuracy” without quantitative CST/FDTD/FEM error comparison.
- “experimentally validated” without measured data.
- “generalizable to arbitrary metasurfaces” without cross-structure or cross-dataset experiments.
- “large-scale aperiodic metasurface” if only periodic unit cells are simulated.
- “physics-informed neural network” unless physical equations or constraints are embedded in training.

Prefer precise claims over broad claims.

---

## 11. Default project profile: ITO/PET/PMI absorber

The following conventions define the default project profile of this skill. When the user provides a different material system, journal, parameter set, or figure-label convention, the user-provided information takes precedence.

- Target journal style: Applied Materials Today / high-quality photonics-materials style.
- Structure: ITO/PET/PMI multilayer metasurface absorber.
- Use “absorption” rather than “S11” for model outputs and final curves unless discussing calculation from S-parameters.
- If using absorption from S-parameters, write: `A(f)=1-|S_{11}(f)|^2-|S_{21}(f)|^2`; if a metallic ground blocks transmission, write: `A(f)\approx 1-|S_{11}(f)|^2`.
- Parameters should distinguish top-layer and middle-layer ITO quantities. Do not confuse `a` and `c`; if the user corrected `b` to `c`, preserve `c`.
- R1 and R2 should be described according to their actual ITO layers, not as generic “bottom/top resistance” unless the user confirms.
- Use “Reference / Predicted / CST” for forward test plots.
- Use “Target / Optimized / CST” for inverse design plots.

---

## 12. LaTeX/Overleaf editing behavior

When asked to modify LaTeX:

1. Identify the exact section, figure, or macro causing the issue.
2. Provide the replacement code directly.
3. Use “替换前 / 替换后 / 修改位置 / 操作步骤” in Chinese.
4. Preserve existing labels and references unless they are wrong.
5. Do not introduce unnecessary packages.
6. Avoid conflicting caption packages or duplicated caption definitions.
7. Do not use `[H]` everywhere; prefer journal-compatible float placement.
8. For large two-column figures, use `figure*` carefully and explain placement side effects.

---

## 13. Output format for Codex tasks

When responding to the user:

- Use Chinese explanations unless the user asks for English-only manuscript text.
- For manuscript paragraphs, provide polished English in ready-to-paste form.
- For code edits, provide exact LaTeX code blocks.
- For paper logic, use compact outlines and templates.
- For figure design, provide panel order, caption, color/line style suggestions, and a reason for each design choice.
- Do not produce vague advice such as “make it more academic.” Provide actual wording.

---

## 14. Quality checklist before finalizing any manuscript text

Before finalizing text, check:

- Does every paragraph have a clear role in the argument chain?
- Is the novelty tied to a specific absorber design challenge?
- Are “forward prediction,” “surrogate model,” and “inverse design” used consistently?
- Is “absorption spectrum” used instead of “S11 spectrum” where appropriate?
- Are claims about accuracy, speed, full-wave validation, and experiments numerically supported?
- Does the method section explain why each module exists physically or spectrally?
- Are figures introduced in the same order as the paper’s logic?
- Are ablation and baseline comparisons framed as evidence rather than decoration?
- Is the Discussion more than a summary, including physical interpretation and limitations?

---

## 15. Canonical contribution template

Use this template for the end of the Introduction:

> The main contributions of this work are summarized as follows. First, we establish a CST-generated dataset for an ITO/PET/PMI multilayer metasurface absorber and formulate a physically constrained parameterization of the unit cell. Second, we develop a spectral-aware forward prediction network that maps structural parameters to absorption spectra while capturing both local resonant features and broadband spectral trends. Third, we construct a forward-guided inverse design strategy that optimizes structural parameters from target absorption spectra and verifies the optimized structures through CST back-simulation. Together, these results provide a rapid and physically consistent route for deep-learning-assisted broadband metasurface absorber design.

Only use statements supported by the manuscript.
