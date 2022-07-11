date:: [[Mon, 2021/08/09]]
conference-name:: Twenty-Ninth International Joint Conference on Artificial Intelligence
extra:: ISSN: 1045-0823
doi:: 10.24963/ijcai.2021/295
title:: Conditional Self-Supervised Learning for Few-Shot Classification
pages:: 2140-2146
volume:: 3
item-type:: [[conferencePaper]]
access-date:: 2022-07-11T03:22:15Z
original-title:: Conditional Self-Supervised Learning for Few-Shot Classification
language:: en
url:: https://www.ijcai.org/proceedings/2021/295
authors:: [[Yuexuan An]], [[Hui Xue]], [[Xingyu Zhao]], [[Lu Zhang]]
library-catalog:: www.ijcai.org
links:: [Local library](zotero://select/library/items/N3PBV23T), [Web library](https://www.zotero.org/users/9034808/items/N3PBV23T)

- [[Abstract]]
	- Electronic proceedings of IJCAI 2021
- [[Attachments]]
	- [Conditional Self-Supervised Learning for Few-Shot Classification_2021_An_Xue_Zhao_Zhang_.pdf](zotero://select/library/items/RBVAQ7EP) {{zotero-linked-file "attachments:Few-shot/Conditional Self-Supervised Learning for Few-Shot Classification_2021_An_Xue_Zhao_Zhang_.pdf"}}
	- [Snapshot](https://www.ijcai.org/proceedings/2021/295) {{zotero-imported-file Y6F7RHRZ, "295.html"}}
- [[note]]
	- 论文将Few-shot learning和对比学习相结合, 整个模型用三部分完成了这个设计
	- 第一部分: ((62cb9e69-b31d-414e-be1e-5543e580f3b6)) 正常训练Few-shot的特征提取器
		- 训练 $f_\theta(\cdot)$ 作为特征提取器
		- 对每一个support set中的同类元素的特征平均作为prototype
		- similarity的衡量是两个向量经过一个线性层 $F_\omega()$ , 再进行cos相似
		- 分类概率: 数据抽出来feature, 分母是和每一类的prototype进行比较, 分子是该类的相似度
		- 优化参数是$\theta$ 和 $\omega$, 也就是分类器 和 相似度计算前的那个线性层
	- 第二部分: ((62cb9f12-07b7-46f3-b45c-ee741aaecb83)) 自训练部分
		- 使用SimSiam的对比学习方法, 利用孪生网络和EM算法去拟合两个极大似然的参数
		- 这种方式学出来的和$f_\theta(\cdot)$去对齐, 衡量损失
		- 得出另一个特征提取器称为$g_\xi (\cdot)$
	- 第三部分 ((62cbcac7-7d08-4980-ac62-a3138dd81c9e)) 元训练阶段
		- 步骤如下:
		  1. 用$f_\theta(\cdot)$ 和 $g_xi(\cdot)$去得到两个feature, 将其结合 (例如concat)
		  2. 这样拼出来一个矩阵, 矩阵每一列都是一个拼好的feature