---
title: "StyleBART: Decorate Pretrained Model with Style Adapters for Unsupervised Stylistic Headline Generation"
collection: publications
category: conferences
permalink: /publication/2023_style_bart
excerpt: 'Author: <b>Hanqing Wang</b><sup>*</sup>, Yajing Luo<sup>*</sup>, Boya Xiong, Guanhua Chen, Yun Chen'
date: 2023-06-20
venue: 'Findings of EMNLP 2023'
paperurl: 'https://eurus-w.github.io/files/2023.findings-emnlp.697.pdf'
---

## TL;DR

Adds lightweight style adapters on top of frozen BART to generate stylistic news headlines (e.g., humorous, romantic) without paired training data, decoupling content faithfulness from stylistic transfer.

## Abstract

Stylistic headline generation is the task to generate a headline that not only summarizes the content of an article, but also reflects a desired style that attracts users. As style-specific article-headline pairs are scarce, previous researches focus on unsupervised approaches with a standard headline generation dataset and mono-style corpora. In this work, we follow this line and propose StyleBART, an unsupervised approach for stylistic headline generation. Our method decorates the pretrained BART model with adapters that are responsible for different styles and allows the generation of headlines with diverse styles by simply switching the adapters. Different from previous works, StyleBART separates the task of style learning and headline generation, making it possible to freely combine the base model and the style adapters during inference. We further propose an inverse paraphrasing task to enhance the style adapters. Extensive automatic and human evaluations show that StyleBART achieves new state-of-the-art performance in the unsupervised stylistic headline generation task, producing high-quality headlines with the desired style.

## Links

- [Paper](https://aclanthology.org/2023.findings-emnlp.697/)

## BibTeX

<details markdown="1">
<summary>Click to expand</summary>

```bibtex
@inproceedings{wang-etal-2023-stylebart,
    title = "{S}tyle{BART}: Decorate Pretrained Model with Style Adapters for Unsupervised Stylistic Headline Generation",
    author = "Wang, Hanqing  and
      Luo, Yajing  and
      Xiong, Boya  and
      Chen, Guanhua  and
      Chen, Yun",
    editor = "Bouamor, Houda  and
      Pino, Juan  and
      Bali, Kalika",
    booktitle = "Findings of the Association for Computational Linguistics: EMNLP 2023",
    month = dec,
    year = "2023",
    address = "Singapore",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2023.findings-emnlp.697/",
    doi = "10.18653/v1/2023.findings-emnlp.697",
    pages = "10387--10399"
}
```

</details>
