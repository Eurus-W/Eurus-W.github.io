---
title: "Multilingual Sentence Transformer as A Multilingual Word Aligner"
collection: publications
category: conferences
permalink: /publication/2022_word_alignment
excerpt: 'Author: Weikang Wang, Guanhua Chen, <b>Hanqing Wang</b>, Yue Han, Yun Chen'
date: 2022-06-30
venue: 'Findings of EMNLP 2022, short'
paperurl: 'https://eurus-w.github.io/files/2022.findings-emnlp.215.pdf'
---

## TL;DR

Shows that an off-the-shelf multilingual sentence transformer can be repurposed as an effective cross-lingual word aligner without alignment-specific supervision, beating prior dedicated aligners on standard benchmarks.

## Abstract

Multilingual pretrained language models (mPLMs) have shown their effectiveness in multilingual word alignment induction. However, these methods usually start from mBERT or XLM-R. In this paper, we investigate whether multilingual sentence Transformer LaBSE is a strong multilingual word aligner. This idea is non-trivial as LaBSE is trained to learn language-agnostic sentence-level embeddings, while the alignment extraction task requires the more fine-grained word-level embeddings to be language-agnostic. We demonstrate that the vanilla LaBSE outperforms other mPLMs currently used in the alignment task, and then propose to finetune LaBSE on parallel corpus for further improvement. Experiment results on seven language pairs show that our best aligner outperforms previous state-of-the-art models of all varieties. In addition, our aligner supports different language pairs in a single model, and even achieves new state-of-the-art on zero-shot language pairs that does not appear in the finetuning process.

## Links

- [Paper](https://aclanthology.org/2022.findings-emnlp.215/)

## BibTeX

<details markdown="1">
<summary>Click to expand</summary>

```bibtex
@inproceedings{wang-etal-2022-multilingual,
    title = "Multilingual Sentence Transformer as A Multilingual Word Aligner",
    author = "Wang, Weikang  and
      Chen, Guanhua  and
      Wang, Hanqing  and
      Han, Yue  and
      Chen, Yun",
    editor = "Goldberg, Yoav  and
      Kozareva, Zornitsa  and
      Zhang, Yue",
    booktitle = "Findings of the Association for Computational Linguistics: EMNLP 2022",
    month = dec,
    year = "2022",
    address = "Abu Dhabi, United Arab Emirates",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2022.findings-emnlp.215/",
    doi = "10.18653/v1/2022.findings-emnlp.215",
    pages = "2952--2963"
}
```

</details>
