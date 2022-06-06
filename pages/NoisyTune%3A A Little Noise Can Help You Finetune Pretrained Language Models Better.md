links:: [Local library](zotero://select/library/items/L8TF3IHB), [Web library](https://www.zotero.org/users/9034808/items/L8TF3IHB)
library-catalog:: ACLWeb
authors:: Chuhan Wu, Fangzhao Wu, Tao Qi, Yongfeng Huang
short-title:: NoisyTune
url:: https://aclanthology.org/2022.acl-short.76
original-title:: NoisyTune: A Little Noise Can Help You Finetune Pretrained Language Models Better
access-date:: 2022-06-06T01:06:00Z
item-type:: [[conferencePaper]]
pages:: 680–685
title:: NoisyTune: A Little Noise Can Help You Finetune Pretrained Language Models Better
doi:: 10.18653/v1/2022.acl-short.76
proceedings-title:: Proceedings of the 60th Annual Meeting of the Association for Computational Linguistics (Volume 2: Short Papers)
conference-name:: ACL 2022
place:: "Dublin, Ireland"
publisher:: Association for Computational Linguistics
date:: 2022

- [[Abstract]]
	- Effectively finetuning pretrained language models (PLMs) is critical for their success in downstream tasks. However, PLMs may have risks in overfitting the pretraining tasks and data, which usually have gap with the target downstream tasks. Such gap may be difficult for existing PLM finetuning methods to overcome and lead to suboptimal performance. In this paper, we propose a very simple yet effective method named NoisyTune to help better finetune PLMs on downstream tasks by adding some noise to the parameters of PLMs before fine-tuning. More specifically, we propose a matrix-wise perturbing method which adds different uniform noises to different parameter matrices based on their standard deviations. In this way, the varied characteristics of different types of parameters in PLMs can be considered. Extensive experiments on both GLUE English benchmark and XTREME multilingual benchmark show NoisyTune can consistently empower the finetuning of different PLMs on different downstream tasks.
- [[Attachments]]
	- [NoisyTune - A Little Noise Can Help You Finetune Pretrained Language Models_2022_Wu_Wu_Qi_Huang_.pdf](zotero://select/library/items/VDFXKATG) {{zotero-linked-file "attachments:ACL/NoisyTune - A Little Noise Can Help You Finetune Pretrained Language Models_2022_Wu_Wu_Qi_Huang_.pdf"}}
- [[paper_note]]
	- 论文实际工作是加入了以下代码:
	- ```python
	  for name ,para in model.named parameters ():
	    model.state dict()[name][:] +=(torch.rand(para.size())−0.5)*noise_lambda*torch.std(para)
	  ```
	- AINLP 的作者的实验认定`random_lambda`在 0.2 的时候效果最好.
	-
-