links:: [Local library](zotero://select/library/items/BPCGYB33), [Web library](https://www.zotero.org/users/9034808/items/BPCGYB33)
library-catalog:: arxiv.org
authors:: Hengyi Zheng, Rui Wen, Xi Chen, Yifan Yang, Yunyan Zhang, Ziheng Zhang, Ningyu Zhang, Bin Qin, Ming Xu, Yefeng Zheng
short-title:: PRGC
url:: https://arxiv.org/abs/2106.09895v1
language:: en
original-title:: PRGC: Potential Relation and Global Correspondence Based Joint Relational Triple Extraction
access-date:: 2022-06-08T00:59:37Z
item-type:: [[journalArticle]]
title:: PRGC: Potential Relation and Global Correspondence Based Joint Relational Triple Extraction
doi:: 10.48550/arXiv.2106.09895
date:: [[Fri, 2021/06/18]]

- [[Abstract]]
	- Joint extraction of entities and relations from unstructured texts is a crucial task in information extraction. Recent methods achieve considerable performance but still suffer from some inherent limitations, such as redundancy of relation prediction, poor generalization of span-based extraction and inefficiency. In this paper, we decompose this task into three subtasks, Relation Judgement, Entity Extraction and Subject-object Alignment from a novel perspective and then propose a joint relational triple extraction framework based on Potential Relation and Global Correspondence (PRGC). Specifically, we design a component to predict potential relations, which constrains the following entity extraction to the predicted relation subset rather than all relations; then a relation-specific sequence tagging component is applied to handle the overlapping problem between subjects and objects; finally, a global correspondence component is designed to align the subject and object into a triple with low-complexity. Extensive experiments show that PRGC achieves state-of-the-art performance on public benchmarks with higher efficiency and delivers consistent performance gain on complex scenarios of overlapping triples.
- [[Attachments]]
	- [PRGC - Potential Relation and Global Correspondence Based Joint Relational_2021_Zheng_Wen_Chen_Yang_Zhang_Zhang_Zhang_Qin_Xu_Zheng_.pdf](zotero://select/library/items/UX4538YS) {{zotero-linked-file "attachments:ACL/PRGC - Potential Relation and Global Correspondence Based Joint Relational_2021_Zheng_Wen_Chen_Yang_Zhang_Zhang_Zhang_Qin_Xu_Zheng_.pdf"}}
	- [Snapshot](https://arxiv.org/abs/2106.09895) {{zotero-imported-file 43KCG7IP, "2106.html"}}
- [[note]]
	- 和casrel和tplinker进行对比:
		- casrel是对每一个可能个关系都进行对比
		- tplinker也是和每一个关系处理 泛化性较差
		- 他认为span-based不好
	- 候选关系
	- RE:Subject和Object两个BIO序列标注(为了解决SOO重叠)
	- 用一个$n\times n$的方形矩阵输入, 定一个阈值, 作为sub-rel-obj三元组关系的最终判断
	- 想法步骤:
		- ((62baa5c3-06f8-4e0d-be4e-0af05eb73e8d))
			- 给定一个句子输出, 对这个句子可能拥有的关系种类进行判断
		- ((62baa60a-249f-4ebc-88ec-cb3903a8dc47))
			- 对于每一个句子下可能存在的每一种关系, 为这个句子的这个关系下进行BIO标注
			- 疑问 : 没有该关系, 那么实体还标注嘛
		- ((62baa6a2-9341-4a54-8c34-3fce20387bc3))
			- 设句子长度为$n$, 这里用一个$n\times n$的表格来评定主实体-客实体的mark
	- 编码器使用的是BERT, 经过Encoder之后变成隐藏的特征向量$
	-