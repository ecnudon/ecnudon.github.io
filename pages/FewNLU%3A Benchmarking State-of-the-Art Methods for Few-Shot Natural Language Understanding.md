item-type:: [[preprint]]
date:: [[Tue, 2022/03/15]]
tags:: Computer Science - Computation and Language, Computer Science - Machine Learning
authors:: Yanan Zheng, Jing Zhou, Yujie Qian, Ming Ding, Chonghua Liao, Jian Li, Ruslan Salakhutdinov, Jie Tang, Sebastian Ruder, Zhilin Yang
links:: [Local library](zotero://select/library/items/YMFCNXQI), [Web library](https://www.zotero.org/users/9034808/items/YMFCNXQI)
title:: FewNLU: Benchmarking State-of-the-Art Methods for Few-Shot Natural Language Understanding

- [[Abstract]]
	- The few-shot natural language understanding (NLU) task has attracted much recent attention. However, prior methods have been evaluated under a disparate set of protocols, which hinders fair comparison and measuring progress of the field. To address this issue, we introduce an evaluation framework that improves previous evaluation procedures in three key aspects, i.e., test performance, dev-test correlation, and stability. Under this new evaluation framework, we re-evaluate several state-of-the-art few-shot methods for NLU tasks. Our framework reveals new insights: (1) both the absolute performance and relative gap of the methods were not accurately estimated in prior literature; (2) no single method dominates most tasks with consistent performance; (3) improvements of some methods diminish with a larger pretrained model; and (4) gains from different methods are often complementary and the best combined model performs close to a strong fully-supervised baseline. We open-source our toolkit, FewNLU, that implements our evaluation framework along with a number of state-of-the-art methods.
- [[Attachments]]
	- [arXiv.org Snapshot](https://arxiv.org/abs/2109.12742) {{zotero-imported-file Q5NL23YI, "2109.html"}}
	- [FewNLU - Benchmarking State-of-the-Art Methods for Few-Shot Natural Language_2022_Zheng_Zhou_Qian_Ding_Liao_Li_Salakhutdinov_Tang_Ruder_Yang_.pdf](zotero://select/library/items/XNCLNR9E) {{zotero-linked-file "attachments:Few-shot/FewNLU - Benchmarking State-of-the-Art Methods for Few-Shot Natural Language_2022_Zheng_Zhou_Qian_Ding_Liao_Li_Salakhutdinov_Tang_Ruder_Yang_.pdf"}}
- [[note]]
	- 同样的超参数, 算出来的结果也不太一样; 所以评价Few-shot learning应该有更新的评判标准
	- ((62c7dba8-8ff8-4dd0-a672-9f860a818123))
		- 本质做法比较简单:
			- 所有有标记数据分类为label和test;
				- label有K种随机分的方式, 每一种的方式我在support上训练, 在query上评估;
				- K种方式的取平均 + 标准差 来衡量这一套超参数下的表现.
				- (但是注意其实这之中label和test都还没换, 是不是继续用k-fold来验证呢)
	- 结论 1: 小样本学习方法的绝对性能和相对性能差异，在先前文献中未被准确估计。此外小样本方法（例如 ADAPET）在像 DeBERTa 这样的大型模型上的优势会显著降低。半监督小样本方法（例如 iPET 和 Noisy Student）增益在较大的模型也可以保持一致性。
	- 结论 2: 不同小样本学习方法的增益在很大程度上是互补的。通过将目前各种先进方法加以组合，它们可以在很大程度上实现优于任意单一方法的小样本学习性能。目前最佳组合方法的小样本学习性能，接近 RoBERTa 上实现的全监督性能；然而和目前 DeBERTa 上实现的最优全监督性能相比，它仍然存在较大的差异性。
	- 结论 3: 目前已有相关工作中不存在单一的小样本学习方法能够在大多数 NLU 任务上取得主导性优势性能。这为未来进一步开发出具有跨任务一致性和鲁棒性的小样本学习方法提出新的挑战。
		-