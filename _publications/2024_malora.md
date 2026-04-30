---
title: "MALoRA: Mixture of Asymmetric Low-Rank Adaptation for Enhanced Multi-Task Learning"
collection: publications
category: conferences
permalink: /publication/2025_malora
excerpt: 'Author: Xujia Wang, Haiyan Zhao, Shuo Wang, <b>Hanqing Wang</b>, Zhiyuan Liu'
date: 2024-10-15
venue: 'Findings of NAACL 2025'
paperurl: 'https://eurus-w.github.io/files/2410.22782v1.pdf'
---

## TL;DR

Mixes multiple LoRA adapters with *asymmetric* low-rank structures — sharing down-projection weights across tasks while keeping up-projections task-specific — to improve multi-task learning efficiency over symmetric LoRA mixtures.

## Abstract

Parameter-Efficient Fine-Tuning (PEFT) methods such as LoRA have significantly improved the adaptation of LLMs to downstream tasks in a resource-efficient manner. However, in multi-task scenarios, challenges such as training imbalance and the seesaw effect frequently emerge. Mixture-of-LoRA (MoLoRA), which combines LoRA with sparse Mixture-of-Experts, mitigates some of these issues by promoting task-specific learning among experts. Despite this, MoLoRA remains inefficient in terms of training speed, parameter utilization, and overall multi-task performance. In this paper, we propose Mixture of Asymmetric Low-Rank Adaptation (MALoRA), a flexible fine-tuning framework that leverages asymmetric optimization among LoRA experts. MALoRA reduces the number of trainable parameters by 30% to 48%, increases training speed by 1.2x, and matches the computational efficiency of single-task LoRA models. Additionally, MALoRA addresses overfitting issues commonly seen in high-rank configurations, enhancing performance stability. Extensive experiments across diverse multi-task learning scenarios demonstrate that MALoRA consistently outperforms all baseline methods in both inter-domain and intra-domain tasks.

## Links

- [Paper](https://aclanthology.org/2025.findings-naacl.312/)

## BibTeX

<details markdown="1">
<summary>Click to expand</summary>

```bibtex
@inproceedings{wang-etal-2025-malora,
    title = "{MAL}o{RA}: Mixture of Asymmetric Low-Rank Adaptation for Enhanced Multi-Task Learning",
    author = "Wang, Xujia  and
      Zhao, Haiyan  and
      Wang, Shuo  and
      Wang, Hanqing  and
      Liu, Zhiyuan",
    editor = "Chiruzzo, Luis  and
      Ritter, Alan  and
      Wang, Lu",
    booktitle = "Findings of the Association for Computational Linguistics: NAACL 2025",
    month = apr,
    year = "2025",
    address = "Albuquerque, New Mexico",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2025.findings-naacl.312/",
    doi = "10.18653/v1/2025.findings-naacl.312",
    pages = "5624--5641",
    ISBN = "979-8-89176-195-7"
}
```

</details>
