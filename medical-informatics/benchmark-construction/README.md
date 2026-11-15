# Benchmark 构建

<a id="med-evidence-bench"></a>

## Med Evidence Bench（MEB）：让临床推理的每个评分点可溯源

**日期与团队：** 2026-11-10，arXiv 预印本；Zhiqun Zhao、Xiaodong Yang、Bruce Gu 等，山东大学齐鲁医学院、山东第一医科大学附属省立医院、山东省计算中心等，联合临床专家与计算团队构建评测。[论文](https://arxiv.org/html/2611.13562v1) · [项目](https://www.medevidencebench.org.cn/)

**标签：** `Benchmark 构建` · `临床推理` · `证据溯源` · `指南`

**简述：** 医师构建 1,536 道中文题，分为指南知识、标准化临床场景和真实世界检验场景三层。每条涉及医学主张的评分标准都链接到带版本的来源原文。10 个模型在指南知识层得分接近满分，但在真实世界检验场景，识别临床信息的平均分为 0.770，匹配证据和给出建议分别只有 0.165、0.160。基准结果不等于真实临床效用。

**可借鉴：** 给评分点绑定具体指南版本与原文片段，把「识别病例事实」「匹配证据」「给出建议」拆开评分；人工复核也要重点抽查证据应用。可对照 [ChronoEvo](../guidelines-rag/README.md#chronoevo)，区分会背指南和能把新版指南用到病例里。

<a id="findlink"></a>

## FindLink / GI-TraceBench：引文都是真的，结论就成立吗？

**日期与团队：** 2026-11-02，arXiv 预印本；Jingxuan Wei、Song Tan、Xiaohan Liu 等，齐鲁工业大学、山东省计算中心、中国科学院大学及中国科学院自动化研究所，研究聚焦可溯源的科学推理。[论文](https://arxiv.org/html/2611.02545v1) · [数据](https://huggingface.co/datasets/Sereints/FindLink)

**标签：** `Benchmark 构建` · `跨文献推理` · `证据溯源` · `假设评估`

**简述：** GI-TraceBench 收录 10,282 道胃肠肿瘤学问题，分别评测证据定位、连接发现和假设评估。配套方法 FindLink 先把主张绑定到原文和研究条件，再判断多条前提共同支持什么。在 1,545 道固定证据测试题上，相对同骨干直接监督微调，按任务族均衡汇总的得分由 67.95 升至 87.25。固定证据结果不代表端到端检索表现；程序只检查结构和来源绑定，不能自动证明科学结论成立。

**可借鉴：** 分别给「引文找对」「证据间关系成立」「证据足以支持结论」打分；专门加入引文都真实、但人群或实验条件不匹配的反例。可对照 [MetKG-CRC](../knowledge-graphs/README.md#met-sc) 的多跳路径审查。

**交叉阅读：** [TrialDesignBench](../trial-design/README.md#trialdesignbench)用专家规则建立试验设计标签；[结构化科学证据抽取](../knowledge-extraction/README.md#structured-evidence-extraction)区分字段、完整记录与汇总结果。
