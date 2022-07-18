item-type:: [[preprint]]
date:: [[Mon, 2022/04/25]]
tags:: Computer Science - Computation and Language
authors:: Rabeeh Karimi Mahabadi, Luke Zettlemoyer, James Henderson, Marzieh Saeidi, Lambert Mathias, Veselin Stoyanov, Majid Yazdani
links:: [Local library](zotero://select/library/items/KMTMC66G), [Web library](https://www.zotero.org/users/9034808/items/KMTMC66G)
title:: PERFECT: Prompt-free and Efficient Few-shot Learning with Language Models

- [[Abstract]]
	- Current methods for few-shot fine-tuning of pretrained masked language models (PLMs) require carefully engineered prompts and verbalizers for each new task to convert examples into a cloze-format that the PLM can score. In this work, we propose PERFECT, a simple and efficient method for few-shot fine-tuning of PLMs without relying on any such handcrafting, which is highly effective given as few as 32 data points. PERFECT makes two key design choices: First, we show that manually engineered task prompts can be replaced with task-specific adapters that enable sample-efficient fine-tuning and reduce memory and storage costs by roughly factors of 5 and 100, respectively. Second, instead of using handcrafted verbalizers, we learn new multi-token label embeddings during fine-tuning, which are not tied to the model vocabulary and which allow us to avoid complex auto-regressive decoding. These embeddings are not only learnable from limited data but also enable nearly 100x faster training and inference. Experiments on a wide range of few-shot NLP tasks demonstrate that PERFECT, while being simple and efficient, also outperforms existing state-of-the-art few-shot learning methods. Our code is publicly available at https://github.com/facebookresearch/perfect.git.
- [[Attachments]]
	- [arXiv.org Snapshot](https://arxiv.org/abs/2204.01172) {{zotero-imported-file 8AEDY7JB, "2204.html"}}
	- [PERFECT - Prompt-free and Efficient Few-shot Learning with Language Models_2022_Mahabadi_Zettlemoyer_Henderson_Saeidi_Mathias_Stoyanov_Yazdani_.pdf](zotero://select/library/items/RWC4SFVP) {{zotero-linked-file "attachments:Few-shot/PERFECT - Prompt-free and Efficient Few-shot Learning with Language Models_2022_Mahabadi_Zettlemoyer_Henderson_Saeidi_Mathias_Stoyanov_Yazdani_.pdf"}}
- [[note]]
	- 主要的思想是使用adapter-finetune.