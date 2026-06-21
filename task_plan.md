# Task Plan: feiman-v1 — 《费曼物理学讲义》卷1 中译

## Goal
将 Richard Feynman 的《The Feynman Lectures on Physics, Volume I》(1963, Caltech)
全书 52 章从在线 HTML 翻译为结构化中文 Markdown，通过 GitHub Pages (Jekyll + MathJax) 发布。

## Source
- 主站: https://www.feynmanlectures.caltech.edu/
- 卷1目录: https://www.feynmanlectures.caltech.edu/I_toc.html
- 各章: https://www.feynmanlectures.caltech.edu/I_01.html ~ I_52.html

## Book Structure (52 Chapters)

### Part I: 力学基础 (Mechanics Foundations) — Ch1-12
| 章节 | 原标题 | 中文标题 |
|------|--------|----------|
| Ch01 | Atoms in Motion | 运动中的原子 |
| Ch02 | Basic Physics | 基础物理学 |
| Ch03 | The Relation of Physics to Other Sciences | 物理学与其他科学的关系 |
| Ch04 | Conservation of Energy | 能量守恒 |
| Ch05 | Time and Distance | 时间与距离 |
| Ch06 | Probability | 概率 |
| Ch07 | The Theory of Gravitation | 引力理论 |
| Ch08 | Motion | 运动 |
| Ch09 | Newton's Laws of Dynamics | 牛顿动力学定律 |
| Ch10 | Conservation of Momentum | 动量守恒 |
| Ch11 | Vectors | 矢量 |
| Ch12 | Characteristics of Force | 力的特性 |

### Part II: 能量、相对论与旋转 (Energy, Relativity & Rotation) — Ch13-20
| 章节 | 原标题 | 中文标题 |
|------|--------|----------|
| Ch13 | Work and Potential Energy (A) | 功与势能 (上) |
| Ch14 | Work and Potential Energy (conclusion) | 功与势能 (下) |
| Ch15 | The Special Theory of Relativity | 狭义相对论 |
| Ch16 | Relativistic Energy and Momentum | 相对论性能量与动量 |
| Ch17 | Space-Time | 时空 |
| Ch18 | Rotation in Two Dimensions | 二维空间中的旋转 |
| Ch19 | Center of Mass; Moment of Inertia | 质心与转动惯量 |
| Ch20 | Rotation in Space | 三维空间中的旋转 |

### Part III: 振动、波与光学 (Oscillations, Waves & Optics) — Ch21-36
| 章节 | 原标题 | 中文标题 |
|------|--------|----------|
| Ch21 | The Harmonic Oscillator | 谐振子 |
| Ch22 | Algebra | 代数 |
| Ch23 | Resonance | 共振 |
| Ch24 | Transients | 瞬态 |
| Ch25 | Linear Systems and Review | 线性系统与复习 |
| Ch26 | Optics: The Principle of Least Time | 光学：最小时间原理 |
| Ch27 | Geometrical Optics | 几何光学 |
| Ch28 | Electromagnetic Radiation | 电磁辐射 |
| Ch29 | Interference | 干涉 |
| Ch30 | Diffraction | 衍射 |
| Ch31 | The Origin of the Refractive Index | 折射率的起源 |
| Ch32 | Radiation Damping. Light Scattering | 辐射阻尼与光散射 |
| Ch33 | Polarization | 偏振 |
| Ch34 | Relativistic Effects in Radiation | 辐射中的相对论效应 |
| Ch35 | Color Vision | 色觉 |
| Ch36 | Mechanisms of Seeing | 视觉机制 |

### Part IV: 量子力学、统计力学与热力学 (Quantum, Statistical & Thermal) — Ch37-46
| 章节 | 原标题 | 中文标题 |
|------|--------|----------|
| Ch37 | Quantum Behavior | 量子行为 |
| Ch38 | The Relation of Wave and Particle Viewpoints | 波与粒子观点的关系 |
| Ch39 | The Kinetic Theory of Gases | 气体动理论 |
| Ch40 | The Principles of Statistical Mechanics | 统计力学原理 |
| Ch41 | The Brownian Movement | 布朗运动 |
| Ch42 | Applications of Kinetic Theory | 动理论的应用 |
| Ch43 | Diffusion | 扩散 |
| Ch44 | The Laws of Thermodynamics | 热力学定律 |
| Ch45 | Illustrations of Thermodynamics | 热力学示例 |
| Ch46 | Ratchet and Pawl | 棘轮与棘爪 |

### Part V: 声学与对称性 (Sound & Symmetry) — Ch47-52
| 章节 | 原标题 | 中文标题 |
|------|--------|----------|
| Ch47 | Sound. The Wave Equation | 声音·波动方程 |
| Ch48 | Beats | 拍 |
| Ch49 | Modes | 模式 |
| Ch50 | Harmonics | 谐波 |
| Ch51 | Waves | 波 |
| Ch52 | Symmetry in Physical Laws | 物理定律中的对称性 |

## Phases

### Phase 1: 素材采集 (Ingest)
- [ ] 批量 fetch 52 章 HTML → raw/I_XX.txt (6 batch × ~9 chapters)
- [ ] 提取数学公式和图表标注
- [ ] 建立术语表 glossary.md 初稿
- **Status:** pending

### Phase 2: 深度研究与并行翻译 (Research + Translate)
- [ ] Mythos 深度研究每部分物理概念 (5 parts × mythos)
- [ ] Paper Agent 批量并行翻译 (6-8 agents per batch, ~7 batches)
- [ ] 每章输出到 docs/chXX_中文标题.md
- **Status:** pending

### Phase 3: 一致性与数学公式 QA (Quality)
- [ ] 术语一致性检查 (vs glossary.md)
- [ ] kramdown 数学公式验证 (verify_math_kramdown.rb)
- [ ] 逐章 promo/fix math
- **Status:** pending

### Phase 4: 组装与发布 (Assemble & Publish)
- [ ] 生成 docs/index.md, docs/_sidebar.md
- [ ] 配置 _config.yml, head-custom.html (MathJax 3)
- [ ] GitHub Pages 推送 + 浏览器验证
- **Status:** pending

## Parallel Translation Batches (Phase 2 detail)

| Batch | Chapters | Agents | Est. output |
|-------|----------|--------|-------------|
| B1 | Ch01-Ch08 | 8 | ~160KB |
| B2 | Ch09-Ch16 | 8 | ~160KB |
| B3 | Ch17-Ch24 | 8 | ~160KB |
| B4 | Ch25-Ch32 | 8 | ~160KB |
| B5 | Ch33-Ch40 | 8 | ~160KB |
| B6 | Ch41-Ch48 | 8 | ~160KB |
| B7 | Ch49-Ch52 | 4 | ~80KB |

## Decisions
| Decision | Rationale |
|----------|-----------|
| 输出为物理教科书风格 | 与《物理定律的本性》的讲座风格不同，此为正式教材 |
| 保留原 52 章结构 | Feynman 的教学顺序经过精心设计 |
| 数学公式全部用 $$...$$ | kramdown 兼容性，GitHub Pages 安全渲染 |
| batch 7 组并行翻译 | 52 章量大，每次 6-8 agent 并行可控 |
| 按 5 部分分别 mythos 研究 | 每部分主题一致，研究聚焦 |

## Output Template (per chapter)
```markdown
# 第N章: 中文标题
> 原书: The Feynman Lectures on Physics, Volume I, 1963
> 在线阅读: https://www.feynmanlectures.caltech.edu/I_NN.html

## 一、本章概要
- 核心物理问题与动机
- 与前后章节的逻辑关系

## 二、核心概念与物理论证
- 关键定义 (中英对照)
- 完整数学推导 ($$...$$ 格式)
- 物理直觉与费曼式解释

## 三、关键示例与应用
- 费曼的原例解析
- 数值估算与量纲分析

## 四、费曼的核心洞察 (Feynman's Insights)
- 3-5 个关键物理洞察
- 教学法评价

## 五、延伸思考与练习
- 开放问题
- 推荐习题与延伸阅读
```
