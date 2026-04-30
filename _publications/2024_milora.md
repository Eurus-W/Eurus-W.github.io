---
title: "MiLoRA: Harnessing Minor Singular Components for Parameter-Efficient LLM Finetuning"
collection: publications
category: conferences
permalink: /publication/2025_milora
excerpt: 'Author: <b>Hanqing Wang</b>, Yixia Li, Shuo Wang, Guanhua Chen, Yun Chen'
date: 2024-06-03
venue: 'NAACL 2025'
paperurl: 'https://eurus-w.github.io/files/2406.09044v3.pdf'
---

## TL;DR

Initializes LoRA adapters using the *minor* singular components of pre-trained weights (rather than random init or principal components), reducing interference with the base model's existing knowledge while still enabling effective task adaptation.

## Abstract

Efficient finetuning of large language models (LLMs) aims to adapt the LLMs with reduced computational and memory costs. Previous LoRA-based approaches initialize the low-rank matrices with Gaussian distribution and zero values while keeping the original weight matrices frozen. However, the trainable model parameters optimized in an unguided subspace might interfere with the well-learned subspace of the pretrained weight matrices. In this paper, we propose MiLoRA, a simple yet effective LLM finetuning approach that only updates the minor singular components of the weight matrix while keeping the principal singular components frozen. It is observed that the minor matrix corresponds to the noisy or long-tail information, while the principal matrix contains important knowledge. The MiLoRA initializes the low-rank matrices within a subspace that is orthogonal to the principal matrix, thus the pretrained knowledge is expected to be well preserved. During finetuning, MiLoRA makes the most use of the less-optimized subspace for learning the labeled dataset. Extensive experiments on commonsense reasoning, math reasoning, instruction following and visual instruction following benchmarks present the superior performance of our method.

## Links

- [Paper](https://aclanthology.org/2025.naacl-long.248/)
- [Code](https://github.com/sufenlp/MiLoRA)

## BibTeX

<details markdown="1">
<summary>Click to expand</summary>

```bibtex
@inproceedings{wang-etal-2025-milora,
    title = "{M}i{L}o{RA}: Harnessing Minor Singular Components for Parameter-Efficient {LLM} Finetuning",
    author = "Wang, Hanqing  and
      Li, Yixia  and
      Wang, Shuo  and
      Chen, Guanhua  and
      Chen, Yun",
    editor = "Chiruzzo, Luis  and
      Ritter, Alan  and
      Wang, Lu",
    booktitle = "Proceedings of the 2025 Conference of the Nations of the Americas Chapter of the Association for Computational Linguistics: Human Language Technologies (Volume 1: Long Papers)",
    month = apr,
    year = "2025",
    address = "Albuquerque, New Mexico",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2025.naacl-long.248/",
    doi = "10.18653/v1/2025.naacl-long.248",
    pages = "4823--4836",
    ISBN = "979-8-89176-189-6"
}
```

</details>
