# 生物基础模型

<a id="evo-2"></a>

## Evo 2：跨生命域的基因组建模与设计

**日期与团队：** 2026-03-04，*Nature* 在线发表；Garyk Brixi、Matthew Durrant、Jerome Ku 等，Arc Institute 联合 Stanford、NVIDIA 等。[论文](https://pubmed.ncbi.nlm.nih.gov/41781614/) · [代码与模型](https://github.com/ArcInstitute/evo2)

**标签：** `生物基础模型` · `基因组语言模型` · `序列设计`

**简述：** StripedHyena 2 用注意力与卷积对 DNA 做下一碱基预测，在 8.8 万亿余核苷酸的语料上训练，长上下文约 100 万碱基。评测包括用序列似然差预测变异效应、用表征识别外显子，以及实验验证部分生成序列的调控效果。

**追问 | 长上下文证明了什么？** 先用较短序列预训练，再扩展上下文。needle-in-a-haystack 将短片段藏入长序列，测模型能否找回它，不直接证明模型理解远端调控。序列生成看起来像天然基因组，也不能证明功能、存活或复制。[Arc 进展](https://arcinstitute.org/news/evo-2-one-year-later) · [Goodfire 解释研究](https://www.goodfire.ai/research/interpreting-evo-2) · [Asimov Press 外部解读](https://press.asimov.com/articles/evo-2)

<a id="signature"></a>

## SIGnature：解释单细胞基础模型中的基因重要性

**日期与团队：** 2026-05-27，*Nature Biotechnology*；Genentech 与 Boston Children's Hospital、Harvard Medical School 等合作，通讯作者包括 Graham Heimberg、Tommaso Biancalani。[论文](https://www.nature.com/articles/s41587-026-03112-5) · [工具教程](https://genentech.github.io/SIGnature/)

**标签：** `生物基础模型` · `单细胞` · `可解释性`

**简述：** 用积分梯度等归因方法估计基因对细胞表征的重要性，将基因集归因聚合成细胞级分数。研究跨队列检索炎症程序，发现川崎病相关信号，并做了体外验证。

**追问 | 是新模型吗？能判断因果吗？** 它是现有模型的解释工具。归因高表示模型表征对该基因敏感，适合提出待验证假设，不等于敲除该基因必然改变细胞功能。

**交叉阅读：** [HoloCell](../virtual-cell-and-biodesign/README.md#holocell)是面向虚拟细胞的生成式单细胞多组学基础模型。
