---
title: "Delta-CoMe: Training-Free Delta-Compression with Mixed-Precision for Large Language Models"
collection: publications
category: conferences
permalink: /publication/2024_delta_come
excerpt: 'Author: Bowen Ping, Shuo Wang, <b>Hanqing Wang</b>, Xu Han, Yuzhuang Xu, Yukun Yan, Yun Chen, Baobao Chang, Zhiyuan Liu, Maosong Sun'
date: 2024-05-22
venue: 'NeurIPS 2024'
paperurl: 'https://eurus-w.github.io/files/18992_Delta_CoMe_Training_Free.pdf'
---

## TL;DR

Compresses the *delta* (fine-tuned weights minus base weights) of an aligned LLM with mixed-precision quantization — assigning more bits to influential singular components — recovering near-full performance with a fraction of storage and zero retraining.

## Abstract

Fine-tuning is a crucial process for adapting large language models (LLMs) to diverse applications. In certain scenarios, such as multi-tenant serving, deploying multiple LLMs becomes necessary to meet complex demands. Recent studies suggest decomposing a fine-tuned LLM into a base model and corresponding delta weights, which are then compressed using low-rank or low-bit approaches to reduce costs. In this work, we observe that existing low-rank and low-bit compression methods can significantly harm the model performance for task-specific fine-tuned LLMs (e.g., WizardMath for math problems). Motivated by the long-tail distribution of singular values in the delta weights, we propose a delta quantization approach using mixed-precision. This method employs higher-bit representation for singular vectors corresponding to larger singular values. We evaluate our approach on various fine-tuned LLMs, including math LLMs, code LLMs, chat LLMs, and even VLMs. Experimental results demonstrate that our approach performs comparably to full fine-tuned LLMs, surpassing both low-rank and low-bit baselines by a considerable margin. Additionally, we show that our method is compatible with various backbone LLMs, such as Llama-2, Llama-3, and Mistral, highlighting its generalizability.

## Links

- [Paper](https://openreview.net/pdf?id=cr5EQRJlRn)
- [Code](https://github.com/thunlp/Delta-CoMe)

## BibTeX

<details markdown="1">
<summary>Click to expand</summary>

```bibtex
@inproceedings{ping2024deltacome,
  title     = {Delta-CoMe: Training-Free Delta-Compression with Mixed-Precision for Large Language Models},
  author    = {Ping, Bowen and Wang, Shuo and Wang, Hanqing and Han, Xu and Xu, Yuzhuang and Yan, Yukun and Chen, Yun and Chang, Baobao and Liu, Zhiyuan and Sun, Maosong},
  booktitle = {Advances in Neural Information Processing Systems 38 (NeurIPS 2024)},
  year      = {2024},
  url       = {https://openreview.net/forum?id=cr5EQRJlRn}
}
```

</details>
