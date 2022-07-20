item-type:: [[preprint]]
date:: [[Sun, 2022/03/13]]
tags:: Computer Science - Computation and Language
authors:: Yuxian Gu, Xu Han, Zhiyuan Liu, Minlie Huang
links:: [Local library](zotero://select/library/items/B96NUZXJ), [Web library](https://www.zotero.org/users/9034808/items/B96NUZXJ)
title:: PPT: Pre-trained Prompt Tuning for Few-shot Learning

- [[Abstract]]
	- Prompts for pre-trained language models (PLMs) have shown remarkable performance by bridging the gap between pre-training tasks and various downstream tasks. Among these methods, prompt tuning, which freezes PLMs and only tunes soft prompts, provides an efficient and effective solution for adapting large-scale PLMs to downstream tasks. However, prompt tuning is yet to be fully explored. In our pilot experiments, we find that prompt tuning performs comparably with conventional full-model fine-tuning when downstream data are sufficient, whereas it performs much worse under few-shot learning settings, which may hinder the application of prompt tuning in practice. We attribute this low performance to the manner of initializing soft prompts. Therefore, in this work, we propose to pre-train prompts by adding soft prompts into the pre-training stage to obtain a better initialization. We name this Pre-trained Prompt Tuning framework "PPT". To ensure the generalization of PPT, we formulate similar classification tasks into a unified task form and pre-train soft prompts for this unified task. Extensive experiments show that tuning pre-trained prompts for downstream tasks can reach or even outperform full-model fine-tuning under both full-data and few-shot settings. Our approach is effective and efficient for using large-scale PLMs in practice.
- [[Attachments]]
	- [arXiv.org Snapshot](https://arxiv.org/abs/2109.04332) {{zotero-imported-file X4Y224E8, "2109.html"}}
	- [PPT - Pre-trained Prompt Tuning for Few-shot Learning_2022_Gu_Han_Liu_Huang_.pdf](zotero://select/library/items/Z39QBBLA) {{zotero-linked-file "attachments:prompt/PPT - Pre-trained Prompt Tuning for Few-shot Learning_2022_Gu_Han_Liu_Huang_.pdf"}}