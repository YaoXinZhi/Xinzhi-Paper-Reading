# 循证与知识计算

<a id="starling"></a>

## Starling：从大规模生物医学文献构建可溯源数据集

**日期与团队：** 2026-05-07 arXiv 首版，2026-06-16 更新至 v3；Haydn Jones 等，宾夕法尼亚大学相关团队。[论文](https://arxiv.org/abs/2605.07022) · [项目](https://github.com/starling-labs/starling)

**标签：** `循证与知识计算` · `BioNLP` · `药物证据抽取`

**简述：** 在约 2,250 万篇 PubMed 文献组成的语料上做实体标注和混合检索，再由多 Agent 设计查询与字段、抽取结构化记录。与一次性 RAG 问答不同，输出可复用的数据，包括实验条件和支持片段。

**可借鉴：** 保存关系、证据原句和适用条件；如两条生物利用度记录冲突，先核对是否为空腹、不同物种或不同给药途径。自动审核不等于人工金标准，文本关联也不等于因果。

## Evidence Triangulator：用 LLM 辅助多源医学证据三角互证

**2025-08-09 · Nature Communications · 标签：** `循证与知识计算` · `证据综合`。[论文](https://www.nature.com/articles/s41467-025-62783-x)

把不同研究设计的证据整理为可比较信息，辅助识别结论的汇合与分歧；不等同于自动完成荟萃分析。

## 从妊娠糖尿病到痴呆：用知识图谱重建风险路径

**2025-12-18 在线 · JAMIA · 标签：** `循证与知识计算` · `医学知识图谱` · `因果假设`。[论文](https://pmc.ncbi.nlm.nih.gov/articles/PMC12981626/)

Shuang Wang、Yang Zhang、Jian Du 等，北京大学健康医疗大数据国家研究院与北京大学第一医院团队。用图谱增强 LLM，提出生命历程风险路径候选；候选路径需要单独验证，不是已确立的因果链。

## 主要医学期刊中因果 DAG 的构建与应用

**2026-01-14 · JAMA Network Open · 标签：** `循证与知识计算` · `因果推断`。[论文](https://jamanetwork.com/journals/jamanetworkopen/fullarticle/2843882)

调查观察性研究如何报告因果假设、绘制 DAG，并基于图选择调整变量。可用作检查因果假设与实际分析是否一致的阅读线索。

## EpiKG2DAG：从生物医学文本生成候选因果图

**2026-08-11 · medRxiv 预印本 · 标签：** `循证与知识计算` · `医学知识图谱` · `因果假设`。[预印本](https://www.medrxiv.org/content/10.64898/2026.08.09.26360023v1)

从文献摘要抽取流行病学关联，辅助提出带证据出处的候选 DAG。文本关系只能提示路径，方向、混杂与遗漏变量仍需专家判断。

**交叉阅读：** [儿童流感中成药问答](../medication-kg/README.md#pediatric-influenza-kg)展示了如何把证据片段和来源保留到用药问答。

[Delphi-2M](../disease-trajectories/README.md#delphi-2m)从队列数据预测疾病发生顺序与时间，可与文献知识图谱生成的候选风险路径对照；两者都不能单独证明因果。
