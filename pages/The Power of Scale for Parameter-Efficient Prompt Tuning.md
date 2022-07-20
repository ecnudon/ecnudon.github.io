links:: [Local library](zotero://select/library/items/WK99LZGV), [Web library](https://www.zotero.org/users/9034808/items/WK99LZGV)
authors:: [[Brian Lester]], [[Rami Al-Rfou]], [[Noah Constant]]
tags:: [[Computer Science - Computation and Language]]
date:: [[Thu, 2021/09/02]]
item-type:: [[preprint]]
title:: The Power of Scale for Parameter-Efficient Prompt Tuning

- [[Abstract]]
	- In this work, we explore "prompt tuning", a simple yet effective mechanism for learning "soft prompts" to condition frozen language models to perform specific downstream tasks. Unlike the discrete text prompts used by GPT-3, soft prompts are learned through backpropagation and can be tuned to incorporate signal from any number of labeled examples. Our end-to-end learned approach outperforms GPT-3's "few-shot" learning by a large margin. More remarkably, through ablations on model size using T5, we show that prompt tuning becomes more competitive with scale: as models exceed billions of parameters, our method "closes the gap" and matches the strong performance of model tuning (where all model weights are tuned). This finding is especially relevant in that large models are costly to share and serve, and the ability to reuse one frozen model for multiple downstream tasks can ease this burden. Our method can be seen as a simplification of the recently proposed "prefix tuning" of Li and Liang (2021), and we provide a comparison to this and other similar approaches. Finally, we show that conditioning a frozen model with soft prompts confers benefits in robustness to domain transfer, as compared to full model tuning.
- [[Attachments]]
	- [arXiv.org Snapshot](https://arxiv.org/abs/2104.08691) {{zotero-imported-file XHMX4KWJ, "2104.html"}}
	- [The Power of Scale for Parameter-Efficient Prompt Tuning_2021_Lester_Al-Rfou_Constant_.pdf](zotero://select/library/items/5GYNRRRT) {{zotero-linked-file "attachments:prompt/The Power of Scale for Parameter-Efficient Prompt Tuning_2021_Lester_Al-Rfou_Constant_.pdf"}}
- [[note]]
	- ((62d7d528-ded9-472d-86d9-cdfaf945f6ed))
	- 之前的prompt: 用词表中的词汇(就是英语or汉语里的), 也要经过统一的PLM的embedding编码
	- 本文想法:
	-