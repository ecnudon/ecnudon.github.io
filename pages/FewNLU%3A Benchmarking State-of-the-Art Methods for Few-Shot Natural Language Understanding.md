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
				- label有K种
		-