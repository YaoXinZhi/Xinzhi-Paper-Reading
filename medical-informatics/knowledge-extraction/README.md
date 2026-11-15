# 知识抽取

<a id="structured-evidence-extraction"></a>

## 结构化科学证据抽取：字段都抽对了，也可能配错组

**日期与团队：** 2026-10-28，*International Journal on Digital Libraries*；Zhiyin Tan、Jennifer D’Souza、Sören Auer，德国莱布尼茨汉诺威大学 L3S 研究中心与德国国家科技图书馆（TIB），研究聚焦科学知识表示与结构化抽取。[论文](https://doi.org/10.1007/s00799-026-00449-9) · [代码与标注](https://github.com/zhiyintan/llm-scientific-evidence-extraction)

**标签：** `知识抽取` · `证据结构化` · `字段绑定` · `分层评测`

**简述：** 在五个科学领域的论文全文上，按「单字段识别 → 多字段组成完整记录 → 跨论文精确统计」分层评测。模型较擅长找出孤立字段，却容易把变量对、统计方法和效应量绑定到错误记录；这些错配会在汇总时放大。逐篇处理往往改善中间抽取，但不保证最终统计正确。该研究是跨学科的错误诊断，不是临床专用基准。

**可借鉴：** 以研究、比较组和结局标识约束字段归属，每条记录保留原文；分别测字段准确率、整条记录准确率和最终统计。先验证记录的归属与单位，再用确定性代码汇总。

**交叉阅读：** [Starling](../evidence-and-knowledge/README.md#starling)给出大规模证据抽取与溯源的实现；[MEB](../benchmark-construction/README.md#med-evidence-bench)将类似的分层评测思路用于临床推理。
