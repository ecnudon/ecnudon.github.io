title:: Training Data is More Valuable than You Think: A Simple and Effective Method by Retrieving from Training Data

- report-number:: arXiv:2203.08773
  links:: [Local library](zotero://select/library/items/ZAHJTNMD), [Web library](https://www.zotero.org/users/9034808/items/ZAHJTNMD)
  library-catalog:: arXiv.org
  authors:: Shuohang Wang, Yichong Xu, Yuwei Fang, Yang Liu, Siqi Sun, Ruochen Xu, Chenguang Zhu, Michael Zeng
  short-title:: Training Data is More Valuable than You Think
  url:: http://arxiv.org/abs/2203.08773
  original-title:: Training Data is More Valuable than You Think: A Simple and Effective Method by Retrieving from Training Data
  access-date:: 2022-06-02T12:08:10Z
  item-type:: [[report]]
  title:: Training Data is More Valuable than You Think: A Simple and Effective Method by Retrieving from Training Data
  date:: [[Mar 16th, 2022]]
  tags:: Computer Science - Artificial Intelligence, Computer Science - Computation and Language, Computer Science - Information Retrieval
  institution:: arXiv
- [[Abstract]]
	- Retrieval-based methods have been shown to be effective in NLP tasks via introducing external knowledge. However, the indexing and retrieving of large-scale corpora bring considerable computational cost. Surprisingly, we found that REtrieving from the traINing datA (REINA) only can lead to significant gains on multiple NLG and NLU tasks. We retrieve the labeled training instances most similar to the input text and then concatenate them with the input to feed into the model to generate the output. Experimental results show that this simple method can achieve significantly better performance on a variety of NLU and NLG tasks, including summarization, machine translation, language modeling, and question answering tasks. For instance, our proposed method achieved state-of-the-art results on XSum, BigPatent, and CommonsenseQA. Our code is released, https://github.com/microsoft/REINA .
- [[Attachments]]
	- [Training Data is More Valuable than You Think - A Simple and Effective Method by_2022_Wang_Xu_Fang_Liu_Sun_Xu_Zhu_Zeng_.pdf](zotero://select/library/items/37VYLPUF) {{zotero-linked-file "attachments:Augmentation/Training Data is More Valuable than You Think - A Simple and Effective Method by_2022_Wang_Xu_Fang_Liu_Sun_Xu_Zhu_Zeng_.pdf"}}
- [[paper_note]]
	- ![image.png](../assets/image_1654186744493_0.png)
	- ((6298e309-6550-4ace-b50d-afeafe9bcd74))
	- 之前的做法:类似于数据增强, 在大规模语料库中将输入信息『扩充』一下, 而不会把『训练数据』扯上
	- 类似于: 同一类数学题, 给了一个题目, 再给三个没有答案的类似的题目
	- 现在微软做法: 把课上讲的例题堆在一起喂进去)
	- 而且之前是在『题库』里搜, 现在直接在『例题库』搜索, 会快很多
	- 模型输入从之前的 $M(x)$ 变成了 $M(f(x, (k_1, v_1), ..., (k_i,v_i), ... ))$
	- 使用 **BM25** 算法寻找和 $x$ 最相近的 $k$ 个句子
	-
-