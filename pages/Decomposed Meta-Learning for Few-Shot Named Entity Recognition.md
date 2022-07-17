links:: [Local library](zotero://select/library/items/UTALHYM2), [Web library](https://www.zotero.org/users/9034808/items/UTALHYM2)
authors:: [[Tingting Ma]], [[Huiqiang Jiang]], [[Qianhui Wu]], [[Tiejun Zhao]], [[Chin-Yew Lin]]
tags:: [[Computer Science - Computation and Language]]
date:: [[Wed, 2022/04/13]]
item-type:: [[preprint]]
title:: Decomposed Meta-Learning for Few-Shot Named Entity Recognition

- [[Abstract]]
	- Few-shot named entity recognition (NER) systems aim at recognizing novel-class named entities based on only a few labeled examples. In this paper, we present a decomposed meta-learning approach which addresses the problem of few-shot NER by sequentially tackling few-shot span detection and few-shot entity typing using meta-learning. In particular, we take the few-shot span detection as a sequence labeling problem and train the span detector by introducing the model-agnostic meta-learning (MAML) algorithm to find a good model parameter initialization that could fast adapt to new entity classes. For few-shot entity typing, we propose MAML-ProtoNet, i.e., MAML-enhanced prototypical networks to find a good embedding space that can better distinguish text span representations from different entity classes. Extensive experiments on various benchmarks show that our approach achieves superior performance over prior methods.
- [[Attachments]]
	- [arXiv.org Snapshot](https://arxiv.org/abs/2204.05751) {{zotero-imported-file F7TQFRRZ, "2204.html"}}
	- [Decomposed Meta-Learning for Few-Shot Named Entity Recognition_2022_Ma_Jiang_Wu_Zhao_Lin_.pdf](zotero://select/library/items/YGA5IAHX) {{zotero-linked-file "attachments:Few-shot/Decomposed Meta-Learning for Few-Shot Named Entity Recognition_2022_Ma_Jiang_Wu_Zhao_Lin_.pdf"}}
- [[note]]
	- 先分span 再实体分类 而且都用的MAML
	- 之前的小样本NER大多是基于token级的度量学习,  用token去和prototype比较
	- 这篇论文首先把所有的实习先按照BIOES的标准进行标注, 对每个token的BIOES进行训练
		- 第一步的softmax对不同类别的实体进行区分, 所有实体都只是先划分出span来
		- 在loss函数把最大值重复加进去了, 缓解大损失token学习不足的问题
		- feature extractor 的训练:
			- 使用MAML的训练方式: 随机采样出一组Support, Query, Test
			- 在同样的$\Theta$上利用support进行梯度反向传播优化, 成为$\Theta'$
			- 每一个$\Theta'_i$在Query上评估得到损失, 再优化$\Theta$自身.
	- 抽取出了span, 之后是实体分类任务
		- 用另一个encoder 对token编码, 跨度中所有的token表征取平均代表span的表征
		- 遵循『原型网络』的设置, support set里的所有的同一类的实体, 的跨度特征 再平均
-