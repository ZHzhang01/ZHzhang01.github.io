---
permalink: /
title: "<span class='homepage-title'><img src='/images/实验室logo.png' class='homepage-title-logo' alt='CAUSAL Lab logo'><span>CAUSAL Lab | Zhiheng Zhang（张智恒）| SSDS, SUFE</span></span>"
author_profile: true
classes: wide
home_language_switcher: true
redirect_from:
  - /about/
  - /about.html
---

<style>
.page__content a,
.page__content a:visited,
.page__content a:hover,
.page__content a:focus {
  color: #0b3d91;
}

html[data-theme="dark"] .page__content a,
html[data-theme="dark"] .page__content a:visited,
html[data-theme="dark"] .page__content a:hover,
html[data-theme="dark"] .page__content a:focus {
  color: #79b8ff;
}

.homepage-title {
  display: flex;
  align-items: center;
  gap: 12px;
  width: 100%;
  max-width: 100%;
  line-height: 1.25;
  white-space: normal;
}

.homepage-title > span {
  min-width: 0;
  overflow-wrap: anywhere;
}

.homepage-title-logo {
  width: auto;
  height: 58px;
  flex: 0 0 auto;
  border-radius: 0;
  object-fit: contain;
}

.page__header--with-language-switcher {
  display: grid;
  grid-template-columns: minmax(0, 1fr) auto;
  align-items: center;
  gap: 1rem 1.5rem;
  margin-bottom: 1.5rem;
}

.page__header--with-language-switcher .page__title {
  min-width: 0;
  margin: 0;
}

.home-language-switcher {
  z-index: 10;
  display: flex;
  justify-content: flex-end;
  margin: 0;
  pointer-events: none;
}

.home-language-switcher__inner {
  display: inline-flex;
  align-items: center;
  gap: 0.3rem;
  padding: 0.28rem;
  border: 1px solid var(--global-border-color);
  border-radius: 999px;
  background: var(--global-bg-color);
  box-shadow: 0 5px 18px rgba(15, 23, 42, 0.1);
  pointer-events: auto;
}

.home-language-switcher__label {
  padding: 0 0.55rem 0 0.7rem;
  color: var(--global-text-color-light);
  font-size: 0.72em;
  font-weight: 600;
  letter-spacing: 0.02em;
}

.home-language-switcher button {
  min-width: 4.7rem;
  margin: 0;
  padding: 0.42rem 0.78rem;
  border: 0;
  border-radius: 999px;
  color: var(--global-text-color);
  background: transparent;
  font: inherit;
  font-size: 0.78em;
  font-weight: 650;
  line-height: 1.2;
  cursor: pointer;
  transition: color 160ms ease, background-color 160ms ease, box-shadow 160ms ease;
}

.home-language-switcher button:hover {
  background: var(--global-border-color);
}

.home-language-switcher button[aria-pressed="true"] {
  color: #fff;
  background: #0b3d91;
  box-shadow: 0 2px 7px rgba(11, 61, 145, 0.28);
}

.home-language-switcher button:focus-visible {
  outline: 3px solid rgba(11, 61, 145, 0.3);
  outline-offset: 2px;
}

html[data-theme="dark"] .home-language-switcher__inner {
  box-shadow: 0 5px 18px rgba(0, 0, 0, 0.28);
}

html[data-theme="dark"] .home-language-switcher button[aria-pressed="true"] {
  color: #10233f;
  background: #8fc4ff;
}

.home-language-panel {
  display: none;
  animation: home-language-fade 180ms ease-out;
}

html:not([data-home-lang]) .home-language-panel[data-lang="zh"],
html[data-home-lang="zh"] .home-language-panel[data-lang="zh"],
html[data-home-lang="en"] .home-language-panel[data-lang="en"] {
  display: block;
}

.home-language-panel > :first-child {
  margin-top: 0;
}

.recruitment-card {
  margin: 1.4rem 0 1.75rem;
  padding: 1.15rem 1.25rem;
  border: 1px solid var(--global-border-color);
  border-left: 4px solid #b42318;
  border-radius: 10px;
  background: #f8fafc;
  box-shadow: 0 4px 14px rgba(15, 23, 42, 0.05);
}

.recruitment-card h3 {
  margin: 0 0 0.8rem;
  color: #a31515;
  font-weight: 700;
}

.recruitment-card > :last-child {
  margin-bottom: 0;
}

html[data-theme="dark"] .recruitment-card {
  background: rgba(255, 255, 255, 0.055);
}

html[data-theme="dark"] .recruitment-card h3 {
  color: #ff9b96;
}

.home-language-panel h2 {
  margin-top: 2.15rem;
}

.home-language-panel li + li {
  margin-top: 0.42rem;
}

.home-language-panel img {
  border-radius: 8px;
}

@keyframes home-language-fade {
  from { opacity: 0; transform: translateY(3px); }
  to { opacity: 1; transform: translateY(0); }
}

@media (prefers-reduced-motion: reduce) {
  .home-language-panel {
    animation: none;
  }

  .home-language-switcher button {
    transition: none;
  }
}

@media (max-width: 1350px) {
  .home-language-switcher__label {
    display: none;
  }
}

@media (max-width: 900px) {
  .page__header--with-language-switcher {
    grid-template-columns: minmax(0, 1fr);
    align-items: start;
  }

  .home-language-switcher {
    justify-self: end;
  }
}

@media (max-width: 600px) {
  .homepage-title {
    gap: 9px;
    font-size: 0.88em;
  }

  .homepage-title-logo {
    height: 46px;
  }

  .home-language-switcher button {
    min-width: 4.2rem;
  }

  .recruitment-card {
    padding: 1rem;
  }
}
</style>

<script>
(function () {
  var savedLanguage = null;
  try {
    savedLanguage = window.localStorage.getItem("causal-lab-language");
  } catch (error) {
    savedLanguage = null;
  }

  var preferredLanguage = savedLanguage === "zh" || savedLanguage === "en"
    ? savedLanguage
    : ((window.navigator.language || "").toLowerCase().indexOf("zh") === 0 ? "zh" : "en");

  document.documentElement.setAttribute("data-home-lang", preferredLanguage);
  document.documentElement.lang = preferredLanguage === "zh" ? "zh-CN" : "en";
}());
</script>

<section class="home-language-panel" data-lang="zh" lang="zh-CN" markdown="1">

欢迎访问张智恒的主页！本实验室名为 **CAUSAL**（**C**ausal **A**nalysis for **U**nderlying **S**tructures **A**nd **L**earning），致力于在弱假设和复杂环境下发展高效、通用、自动化的因果推断方法，聚焦潜在结构的刻画，并将其与现代学习算法和决策系统相融合。[请查看 CAUSAL 实验室因果推断入门指南](https://github.com/ZHzhang01/ZHzhang01.github.io/blob/master/CAUSAL_Lab_Onboarding_Guide(3).pdf)。

张智恒（英文姓名读音近似 “Zhee-hung Jahng”）自 2025 年 8 月起任[上海财经大学](https://www.sufe.edu.cn/)[统计与数据科学学院](https://ssds.sufe.edu.cn/)常任轨助理教授，同时兼职隶属于[上海财经大学大数据研究院](https://ibdr.sufe.edu.cn/)。此前，他于[清华大学交叉信息研究院](https://iiis.tsinghua.edu.cn/)（IIIS）获得博士学位，博士生导师为[王禹皓](https://yuhaow.github.io/)教授。他担任 2025 年度 [CCF—滴滴盖亚联合科研基金项目](https://outreach.didichuxing.com/app-outreach/CRFYS)“统一的多处理长期价值（LTV）因果模型”联合负责人，并担任 AAAI 2025 人工智能与因果技术方向（AICT track）领域主席。

他正在招收[博士生、硕士生和科研实习生](https://mp.weixin.qq.com/s/XkFc2gSXFDegj9HVEHGPaQ)。 请申请者完成[开源项目研究申请考核](/open-source-project-questionnaire/)或者[理论/方法研究申请考核](https://causal-lab-application.pelusojoule28475.chatgpt.site/)；入组成员请阅读[实验室规范与培养要求](/lab-guidelines/)。也可发送邮件至 zhangzhiheng@mail.shufe.edu.cn。此外，欢迎对因果推断感兴趣的老师和同学参加实验室的论文讨论会；可通过[微信公众号 CAUSAL-lab-SSDS-SUFE](https://raw.githubusercontent.com/ZHzhang01/ZHzhang01.github.io/master/images/reading_group_link.jpg)加入。

<div class="recruitment-card" markdown="1">

### 📢 招生信息

我正在招收若干**博士生和硕士生**，同时**长期招收科研实习生（支持远程线上实习）**。

**我对博士生的基本期望是：**

1. 具备良好的品德与沟通能力，内驱力强，作风扎实，热爱科研探索。鼓励自主探索感兴趣的方向：在我的能力范围内，我会尽力指导；超出我能力范围的方向，我会协助建立合作；
2. 至少具备以下两项能力之一：扎实的数学基础（尤其是概率统计，专业不限）；出色的编程能力；
3. 有志于未来从事科研工作。

**我对硕士生的基本期望是：**

1. 具备良好的品德与沟通能力，作风扎实；
2. 对于有志于学界的学生，我会与博士生共同指导其开展科研，并支持其继续深造；对于有志于业界的学生，我希望其主动求职目标是**算法科研**岗位，并会根据适配度推荐其前往相关方向的前沿研究部门实习。此外，每位硕士生至少应在读期间与我完成一项由自己主导的科研课题，并以此作为毕业论文。

如有兴趣，欢迎随时与我联系。计划申请博士者请至少提前半年联系；计划申请硕士者请至少提前两个月联系。我们将通过前期合作判断彼此是否合适。

</div>

![学术体系图](/_pages/research_roadmap_%203_01.png)

## 研究陈述

**为理解并构建因果学习系统的核心理论结构，实验室的长期目标可概括为以下三个基础问题：**

1. **观测性研究：** 如何系统刻画“模型假设—观测数据—可识别边界”之间的传导机制，从而揭示不同因果假设对可识别性的根本影响？
2. **实验设计与推断：** 如何定量刻画并评估“应用场景属性—实验设计与算法结构—统计效率”之间的性能极限，并据此开发具有最优（或近似最优）性质的设计与推断框架？
3. **离线与在线学习及决策：** 如何从数学结构上统一机器学习、经济与管理、统计推断等领域的优化目标，并揭示它们之间的基本兼容性与最优可达边界？

**为回答上述问题，实验室的总体研究路线遵循从理论到方法、再从方法到实践的逐层递进结构：**

1. 从基础假设的违背出发，构建包容性更强的因果推断框架，例如研究无混杂性（unconfoundedness）、重叠性（overlap）和稳定单元处理值假设（SUTVA）遭到违背的情形；
2. 将这些基础结构与现代统计和机器学习方法相融合，发展更高效、更稳定、更具可扩展性的识别与估计技术，例如最优传输、代理变量与负控方法、共形预测、极小极大优化和在线学习等；
3. 进一步将相关理论与方法扩展到具有现实约束的任务设定，例如复杂的输入或输出结构、小样本学习，以及动态或部分观测的网络结构；
4. 最终形成能够有效辐射现实场景的因果推断体系，服务于社交网络分析、博弈论环境和基于优化的决策，并应用于推荐系统、派单机制、市场干预策略和大模型行为建模。

在这一递进路线中，第 1 步关注输入层面更宽松的结构假设；第 2 步聚焦算法层面精准且高效的识别—估计机制；第 3—4 步主要面向输出层面复杂且贴近现实的决策与推断任务。

**为逐步推进上述目标，目前实验室主要围绕以下四个具体方向开展研究：**

1. **因果理论评估：** 面向基于设计的推断（design-based inference）开展 Lean 形式化证明，维护开放问题，并基于对偶理论筛选和评估算法；
2. **结构规律发现：从实验设计走向科学发现——构建因果驱动的可信 AI 决策系统。** 面对高维处理、网络暴露、组合行动空间和复杂行为轨迹，单个实验已难以充分刻画真实系统中的干预机制。未来的核心挑战不再只是设计更复杂的实验，而是如何将分散的实验对象、实验结果与情境条件组织为可计算、可比较、可桥接的因果结构，从而支撑长期可解释、可评估、可控制的 AI 决策系统。为此，我们将借助大模型的语义表征与生成能力，首先构建连接实验档案与科学发现的因果图谱层，将既有实验中的处理（treatment）、结果（outcome）、情境（context）与效应（effect）统一映射到结构化因果空间，研究多个实验何时可以组合、何时存在结论冲突、何处只能得到部分识别边界，并进一步通过最优桥接实验（bridge experiments）主动缩小不可识别区域。在此基础上，面向多智能体互动、平台机制、市场干预与大模型行为系统，我们将设计因果伪奖励、遗憾校准分配、动态网络控制和战略因果 AI 机制，使复杂系统不仅具有良好的短期表现，而且能在长期演化中保持可靠性。进一步地，我们还将通过稀疏 LLM 比较、低秩任务—模型能力结构与不确定性认证，构建可解释的因果路由器，使 AI 系统能够判断不同模型和策略在何种任务、何种环境下具有真正可迁移、可部署的因果优势。由此，整个研究形成一个闭环：从整理历史实验、构建因果图谱、发现识别冲突，到设计桥接实验、优化在线决策，再由新证据反哺图谱。最终，研究重点将从“如何设计复杂实验”推进到“如何组织实验空间、识别机制边界并构建可信决策机制”，从而形成面向科学发现的可识别学习理论；
3. **智能估计与决策：** 大语言模型奖励建模（LLM reward modeling）、因果表格数据基础模型（foundation models for causal tabular data），以及随机算法中的因果性；
4. **面向产业的交叉应用：** 针对产业现实约束的因果推断方法论，包括 RCT & OBS、pre & opt、结构化数据类型，以及网络结构下的在线实验设计与推断。

![ATLAS 计划](/_pages/main_direction_Causal_ATLAS_7papers_0625.png)

他始终欢迎相关交流与合作。如有兴趣，可发送邮件或添加他的 [WeChat](https://raw.githubusercontent.com/ZHzhang01/ZHzhang01.github.io/master/images/wechat_617.png)。

## 代表性荣誉

2018 年全国大学生数学竞赛决赛（CMC）金牌（全国前 10 名）

## 学术服务

- **审稿人：** ICML、NeurIPS、ICLR、AISTATS、UAI、AAAI、ACM Transactions on Information Systems（TOIS）、IEEE Transactions on Mobile Computing（TMC）、Journal of Machine Learning Research（JMLR）、Journal of the Royal Statistical Society: Series B（JRSSB）、Journal of the American Statistical Association（JASA）、Electronic Journal of Statistics（EJS）、Journal of Computational and Graphical Statistics（JCGS）
- **领域主席：** AAAI 2025，Artificial Intelligence with Causal Techniques（AICT）方向
- **分会场主席：** Causality and Machine Learning，Tsinghua Sanya International Mathematics Forum（TSIMF）2026
- **理事：** 中国现场统计研究会因果推断分会

</section>

<section class="home-language-panel" data-lang="en" lang="en" markdown="1">

Welcome to Zhiheng's homepage! The lab is named **CAUSAL** (**C**ausal **A**nalysis for **U**nderlying **S**tructures **A**nd **L**earning). We develop efficient, general-purpose, and automated methods for causal inference under weak assumptions and in complex environments, with an emphasis on characterizing underlying structures and integrating them with modern learning algorithms and decision-making systems. [Read the CAUSAL Lab Onboarding Guide to Causal Inference](https://github.com/ZHzhang01/ZHzhang01.github.io/blob/master/CAUSAL_Lab_Onboarding_Guide(3).pdf).

Since August 2025, Zhiheng Zhang (pronounced “Zhee-hung Jahng”) has been a tenure-track Assistant Professor at the [Shanghai University of Finance and Economics](https://www.sufe.edu.cn/), with his appointment in the [School of Statistics and Data Science](https://ssds.sufe.edu.cn/). He is also affiliated with the [Institute of Big Data Research](https://ibdr.sufe.edu.cn/). Previously, he received his PhD from the [Institute for Interdisciplinary Information Sciences](https://iiis.tsinghua.edu.cn/) (IIIS) at Tsinghua University, where he was advised by Professor [Yuhao Wang](https://yuhaow.github.io/). He is a co-Principal Investigator of the 2025 [CCF–DiDi Gaia Collaborative Research Fund project](https://outreach.didichuxing.com/app-outreach/CRFYS), “A Unified Causal Model for Multi-Treatment Lifetime Value (LTV),” and served as an Area Chair for the Artificial Intelligence with Causal Techniques (AICT) track at AAAI 2025.

He is recruiting [PhD students, master’s students, and research interns](https://mp.weixin.qq.com/s/XkFc2gSXFDegj9HVEHGPaQ). Applicants are requested to complete either the [Open-Source Project Research Application Assessment](/open-source-project-questionnaire/) or the [Theoretical/Methodological Research Application Assessment](https://causal-lab-application.pelusojoule28475.chatgpt.site/); new lab members should read the [Lab Guidelines and Training Requirements](/lab-guidelines/). Applications may also be sent by email to zhangzhiheng@mail.shufe.edu.cn. In addition, faculty members and students interested in causal inference are welcome to attend the lab’s paper discussion group; you can join via the [WeChat Official Account CAUSAL-lab-SSDS-SUFE](https://raw.githubusercontent.com/ZHzhang01/ZHzhang01.github.io/master/images/reading_group_link.jpg).


<div class="recruitment-card" markdown="1">

### 📢 Recruitment

I am recruiting several **PhD and master's students** and also welcome **research interns on an ongoing basis (remote internships are available)**.

**What I expect from PhD students:**

1. Integrity, strong communication skills, self-motivation, diligence, and a genuine enthusiasm for research. Students are encouraged to explore topics that interest them independently: I will provide the best guidance I can within my areas of expertise and help establish collaborations when a topic extends beyond them;
2. At least one of the following: a solid mathematical foundation, particularly in probability and statistics, regardless of undergraduate major; or excellent programming skills;
3. An aspiration to pursue a research career.

**What I expect from master's students:**

1. Integrity, strong communication skills, and diligence;
2. For students planning an academic career, I will mentor their research jointly with PhD students and support their pursuit of further study. For students planning an industry career, I expect them to target **research-oriented algorithm roles** proactively and, when there is a good fit, will recommend them for internships in leading research groups in relevant areas. In addition, each master's student should complete at least one self-directed research project with me during the degree and develop it into their thesis.

If you are interested, please feel free to contact me. Prospective PhD applicants should reach out at least six months in advance, and prospective master's applicants at least two months in advance. We will use preliminary collaboration to determine whether we are a good mutual fit.

</div>

![Research roadmap](/_pages/research_roadmap_%203_01.png)

## Research Statement

**To understand and develop the core theoretical structure of causal learning systems, the lab's long-term agenda centers on the following three foundational questions:**

1. **Observational studies:** How can we systematically characterize the mechanism linking model assumptions, observed data, and identification boundaries, thereby revealing the fundamental effects of different causal assumptions on identifiability?
2. **Experimental design and inference:** How can we quantitatively characterize and evaluate the performance limits arising from the interplay among application-setting attributes, experimental designs and algorithmic structures, and statistical efficiency, and on this basis develop design and inference frameworks with optimal or near-optimal properties?
3. **Offline and online learning and decision-making:** How can we mathematically unify the optimization objectives of machine learning, economics and management, and statistical inference, and reveal their fundamental compatibility and optimal attainable frontiers?

**To answer these questions, the lab follows a layered research trajectory that proceeds from theory to methodology and from methodology to practice:**

1. Begin with violations of foundational assumptions and construct more inclusive causal-inference frameworks—for example, by studying violations of unconfoundedness, overlap, and the stable unit treatment value assumption (SUTVA);
2. Integrate these foundational structures with modern statistical and machine-learning methods to develop more efficient, stable, and scalable techniques for identification and estimation, including optimal transport, proxy-variable and negative-control methods, conformal prediction, minimax optimization, and online learning;
3. Extend the resulting theory and methodology to tasks with realistic constraints, such as complex input or output structures, small-sample learning, and dynamic or partially observed network structures;
4. Ultimately establish a causal-inference framework that translates effectively into real-world settings, supporting social-network analysis, game-theoretic environments, and optimization-based decision-making, with applications to recommender systems, dispatch mechanisms, market interventions, and the behavioral modeling of large models.

In this progression, Step 1 focuses on more flexible structural assumptions at the input level; Step 2 develops precise and efficient identification–estimation mechanisms at the algorithmic level; and Steps 3–4 address complex, realistic decision and inference tasks at the output level.

**To advance this agenda, the lab is currently pursuing four concrete research directions:**

1. **Causal theory evaluation:** Lean formalization for design-based inference, maintenance of open problems, and algorithm screening and evaluation based on duality theory;
2. **Discovery of structural regularities: From experimental design to scientific discovery—building causality-driven trustworthy AI decision systems.** Given high-dimensional treatments, network exposure, combinatorial action spaces, and complex behavioral trajectories, no single experiment can adequately characterize intervention mechanisms in real-world systems. The central challenge ahead is therefore no longer simply to design more complex experiments, but to organize dispersed experimental objects, findings, and contextual conditions into causal structures that can be computed, compared, and bridged, thereby supporting AI decision systems that remain interpretable, evaluable, and controllable over the long term. To this end, we will leverage the semantic representations and generative capabilities of large models to first build a causal-atlas layer linking experimental archives to scientific discovery. This layer will map the treatments, outcomes, contexts, and effects from prior experiments into a unified, structured causal space; determine when findings across experiments can be combined, when conclusions conflict, and where only partial-identification bounds are available; and use optimal bridge experiments to actively shrink unidentified regions. Building on this foundation, we will develop causal pseudo-rewards, regret-calibrated allocation, dynamic network control, and strategic causal-AI mechanisms for multi-agent interactions, platform mechanisms, market interventions, and large-model behavioral systems, enabling complex systems not only to perform well in the short term but also to remain reliable as they evolve over time. We will further construct interpretable causal routers through sparse LLM comparisons, low-rank task–model capability structures, and uncertainty certification, allowing AI systems to determine which models and strategies possess genuinely transferable and deployable causal advantages in which tasks and environments. Together, these components form a closed loop: from organizing historical experiments, building causal atlases, and detecting identification conflicts, through designing bridge experiments and optimizing online decisions, to feeding new evidence back into the atlas. The goal is to shift the research focus from “how to design complex experiments” to “how to organize the experimental space, identify mechanism boundaries, and build trustworthy decision mechanisms,” thereby establishing a theory of identifiable learning for scientific discovery;
3. **Intelligent estimation and decision-making:** LLM reward modeling, foundation models for causal tabular data, and causality in stochastic algorithms;
4. **Industry-facing interdisciplinary applications:** Causal-inference methodologies tailored to real-world industrial constraints, including RCT & OBS, pre & opt, structural data types, and online experimental design and inference under network structures.

![ATLAS initiative](/_pages/main_direction_Causal_ATLAS_7papers_0625.png)

He always welcomes discussions and collaborations in related areas. If you are interested, please email him or add him on [WeChat](https://raw.githubusercontent.com/ZHzhang01/ZHzhang01.github.io/master/images/wechat_617.png).

## Selected Honors

Gold Medal, 2018 Chinese Undergraduate Mathematics Competition Final (CMC; Top 10 nationwide)

## Academic Service

- **Reviewer:** ICML, NeurIPS, ICLR, AISTATS, UAI, AAAI, ACM Transactions on Information Systems (TOIS), IEEE Transactions on Mobile Computing (TMC), Journal of Machine Learning Research (JMLR), Journal of the Royal Statistical Society: Series B (JRSSB), Journal of the American Statistical Association (JASA), Electronic Journal of Statistics (EJS), and Journal of Computational and Graphical Statistics (JCGS)
- **Area Chair:** AAAI 2025, Artificial Intelligence with Causal Techniques (AICT) track
- **Session Chair:** Causality and Machine Learning, Tsinghua Sanya International Mathematics Forum (TSIMF) 2026
- **Council Member:** Causal Inference Branch, Chinese Association for Applied Statistics (CAAS)

</section>

<script>
(function () {
  var labels = {
    zh: {
      title: "CAUSAL 实验室 | 张智恒 | 上海财经大学统计与数据科学学院",
      navigation: {
        "/publications/": "学术论文",
        "/teaching/": "教学",
        "/talks/": "学术报告",
        "/portfolio/": "实验室成员"
      },
      bio: "我是一名主要研究因果推断的交叉学科研究者。",
      location: "中国上海",
      employer: "上海财经大学",
      contact: "联系信息",
      email: "邮箱",
      follow: "关注：",
      feed: "订阅"
    },
    en: {
      title: "CAUSAL Lab | Zhiheng Zhang | SSDS, SUFE",
      navigation: {
        "/publications/": "Publications",
        "/teaching/": "Teaching",
        "/talks/": "Invited Talks",
        "/portfolio/": "Lab Members"
      },
      bio: "I am an interdisciplinary researcher primarily focusing on causal inference.",
      location: "Shanghai, China",
      employer: "Shanghai University of Finance and Economics",
      contact: "Contact",
      email: "Email",
      follow: "Follow:",
      feed: "Feed"
    }
  };

  function replaceTextAfterIcon(element, value) {
    if (!element) return;
    Array.prototype.slice.call(element.childNodes).forEach(function (node) {
      if (node.nodeType === 3) element.removeChild(node);
    });
    element.appendChild(document.createTextNode(value));
  }

  function updateSharedInterface(language) {
    var copy = labels[language];
    document.title = copy.title;

    document.querySelectorAll("#site-nav a[href]").forEach(function (link) {
      var path = null;
      try {
        path = new URL(link.href, window.location.href).pathname;
      } catch (error) {
        path = null;
      }
      if (path && copy.navigation[path]) link.textContent = copy.navigation[path];
    });

    var bio = document.querySelector(".author__bio");
    if (bio) bio.textContent = copy.bio;

    var authorDetails = document.querySelectorAll(".author__urls .author__desktop");
    if (authorDetails[0]) replaceTextAfterIcon(authorDetails[0], copy.location);
    if (authorDetails[1]) replaceTextAfterIcon(authorDetails[1], copy.employer);

    var contactButton = document.querySelector(".author__urls-wrapper > button");
    if (contactButton) contactButton.textContent = copy.contact;

    var emailLink = document.querySelector('.author__urls a[href^="mailto:"]');
    replaceTextAfterIcon(emailLink, copy.email);

    var followLabel = document.querySelector(".page__footer-follow strong");
    if (followLabel) followLabel.textContent = copy.follow;

    var feedLink = document.querySelector('.page__footer-follow a[href$="feed.xml"]');
    replaceTextAfterIcon(feedLink, copy.feed);

    var themeIcon = document.querySelector("#theme-icon");
    if (themeIcon) themeIcon.setAttribute("title", language === "zh" ? "切换主题" : "Toggle theme");

    var footerCopyright = document.querySelector(".page__footer-copyright");
    if (footerCopyright) {
      var footerText = footerCopyright.textContent || "";
      var dateMatch = footerText.match(/\d{4}-\d{2}-\d{2}/);
      var yearMatch = footerText.match(/©\s*(\d{4})/);
      var updatedDate = dateMatch ? dateMatch[0] : "";
      var copyrightYear = yearMatch ? yearMatch[1] : String(new Date().getFullYear());
      var jekyllLink = '<a href="http://jekyllrb.com" rel="nofollow">Jekyll</a>';
      var academicPagesLink = '<a href="https://github.com/academicpages/academicpages.github.io">AcademicPages</a>';
      var minimalMistakesLink = '<a href="https://mademistakes.com/work/minimal-mistakes-jekyll-theme/" rel="nofollow">Minimal Mistakes</a>';

      footerCopyright.innerHTML = language === "zh"
        ? "© " + copyrightYear + " Zhiheng Zhang（张智恒），由 " + jekyllLink + " 与 " + academicPagesLink + " 提供支持；AcademicPages 衍生自 " + minimalMistakesLink + "。<br>网站最后更新于 " + updatedDate
        : "© " + copyrightYear + " Zhiheng Zhang (张智恒), Powered by " + jekyllLink + " &amp; " + academicPagesLink + ", a fork of " + minimalMistakesLink + ".<br>Site last updated " + updatedDate;
    }
  }

  function setLanguage(language, remember) {
    var nextLanguage = language === "en" ? "en" : "zh";
    document.documentElement.setAttribute("data-home-lang", nextLanguage);
    document.documentElement.lang = nextLanguage === "zh" ? "zh-CN" : "en";

    document.querySelectorAll("[data-set-home-lang]").forEach(function (button) {
      button.setAttribute("aria-pressed", button.getAttribute("data-set-home-lang") === nextLanguage ? "true" : "false");
    });

    updateSharedInterface(nextLanguage);

    if (remember) {
      try {
        window.localStorage.setItem("causal-lab-language", nextLanguage);
      } catch (error) {
        /* The switch still works when browser storage is unavailable. */
      }
    }
  }

  document.querySelectorAll("[data-set-home-lang]").forEach(function (button) {
    button.addEventListener("click", function () {
      setLanguage(button.getAttribute("data-set-home-lang"), true);
    });
  });

  setLanguage(document.documentElement.getAttribute("data-home-lang"), false);
}());
</script>
