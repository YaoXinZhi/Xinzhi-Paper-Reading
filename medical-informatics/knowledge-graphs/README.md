# 知识图谱

<a id="agentic-ai-context-engineering-kg"></a>

## Agentic AI × 上下文工程 × 知识图谱：集成方式综述

**日期与团队：** 2026-04-09，QuaLLM-KG 2026（EDBT/ICDT Workshops），15 页综述；Niraj Karki、Manjila Pandey 等，Pulchowk Engineering Campus、IBM Research 等。[原文 PDF：Agentic AI, Context Engineering and Knowledge Graphs: Current Approaches, Challenges and Opportunities](https://ceur-ws.org/Vol-4192/QuaLLM_KG-paper5.pdf)

**标签：** `知识图谱` · `Agentic AI` · `上下文工程` · `综述`

**简述：** 讨论如何用 KG 为 LLM Agent 提供可靠上下文，支持检索、推理与长期记忆。上下文工程（CE）涵盖信息的动态筛选、组织和管理。综述覆盖 2020–2025 年研究，初筛 436 篇，最终纳入 35 篇。

**五类集成方式（按本文分类）：**

| 方式 | 核心思路 | 代表工作 |
| --- | --- | --- |
| 预训练集成 | 向输入或表示层注入图谱知识 | K-BERT |
| 后训练集成 | 在已训练模型上进一步适配图谱任务 | KG-Agent |
| KG 增强 | 用图结构增强检索与生成 | KG-FiD |
| 推理时集成 | 回答问题时动态查询、遍历图谱 | Think-on-Graph、HOLMES |
| 持续知识更新 | 维护动态图谱与长期记忆 | ZEP、KARMA |

**挑战与边界：** 图谱噪声与缺失、动态更新可靠性、规模成本及统一评估不足。类别存在交叉；持续更新也包含外部图谱和记忆更新。本文是跨领域方法综述。

**可借鉴：** 整理时可分别检查“检索是否准确、推理路径是否可追溯、知识更新是否可靠”，再结合具体任务评估。

<a id="met-sc"></a>

## Met-SC：代谢组平台与结直肠癌知识图谱 MetKG-CRC

**日期与团队：** 2026-11-05，*Nucleic Acids Research* 在线发表；Liliang Wen、Mingchao Wang、Zhongda Zeng 等，中国科学院大连化学物理研究所的国家基因组科学数据中心代谢组学分中心，联合中国科学院北京基因组研究所等。团队将代谢组数据、质谱资源和文献证据接入同一平台。[论文](https://doi.org/10.1093/nar/gkag1127) · [平台](https://metabolomics.dicp.ac.cn/)

**标签：** `知识图谱` · `代谢组学` · `结直肠癌` · `多跳证据`

**简述：** Met-SC 是代谢组数据库与分析平台，MetKG-CRC 是其中的结直肠癌知识图谱，围绕肿瘤代谢、菌群与宿主互作、胆汁酸代谢收录 108,679 个实体和 600,093 条带文献来源的证据三元组，去重后为 374,065 条关系。平台可检索多跳路径并展示逐边来源；专家仅抽查了 30 条候选路径，逐边有文献不等于整条机制已验证。

**可借鉴：** 为每条边保留实验对象、组织、条件和原文出处；多跳推理时再单独检查这些条件能否衔接，并标记哪些路径需要直接验证。可将候选机制连到可复查的代谢组数据。

**交叉阅读：** [用药知识图谱](../medication-kg/README.md)侧重临床用药条件和证据溯源；[FindLink](../benchmark-construction/README.md#findlink)提供评测多条证据能否共同支持结论的方法。
