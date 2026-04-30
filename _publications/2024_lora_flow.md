---
title: "LoRA-Flow: Dynamic LoRA Fusion for Large Language Models in Generative Tasks"
collection: publications
category: conferences
permalink: /publication/2024_lora_flow
excerpt: 'Author: <b>Hanqing Wang</b><sup>*</sup>, Bowen Ping<sup>*</sup>, Shuo Wang, Xu Han, Yun Chen, Zhiyuan Liu, Maosong Sun'
date: 2024-02-21
venue: 'ACL 2024'
paperurl: 'https://eurus-w.github.io/files/2024.acl-long.695.pdf'
---

## TL;DR

Replaces fixed LoRA fusion weights with a per-token dynamic gate, letting multiple task-specific LoRA adapters be combined adaptively during generation rather than averaged with a static recipe.

## Abstract

LoRA employs lightweight modules to customize large language models (LLMs) for each downstream task or domain, where different learned additional modules represent diverse skills. Combining existing LoRAs to address new tasks can enhance the reusability of learned LoRAs, particularly beneficial for tasks with limited annotated data. Most prior works on LoRA combination primarily rely on task-level weights for each involved LoRA, making different examples and tokens share the same LoRA weights. However, in generative tasks, different tokens may necessitate diverse skills to manage. Taking the Chinese math task as an example, understanding the problem description may depend more on the Chinese LoRA, while the calculation part may rely more on the math LoRA. To this end, we propose LoRA-Flow, which utilizes dynamic weights to adjust the impact of different LoRAs. The weights at each step are determined by a fusion gate with extremely few parameters, which can be learned with only 200 training examples. Experiments across six generative tasks demonstrate that our method consistently outperforms baselines with task-level fusion weights. This underscores the necessity of introducing dynamic fusion weights for LoRA combination.

## Links

- [Paper](https://aclanthology.org/2024.acl-long.695/)
- [Code](https://github.com/thunlp/LoRAFlow)

## BibTeX

<details markdown="1">
<summary>Click to expand</summary>

```bibtex
@inproceedings{wang-etal-2024-lora-flow,
    title = "{L}o{RA}-Flow: Dynamic {L}o{RA} Fusion for Large Language Models in Generative Tasks",
    author = "Wang, Hanqing  and
      Ping, Bowen  and
      Wang, Shuo  and
      Han, Xu  and
      Chen, Yun  and
      Liu, Zhiyuan  and
      Sun, Maosong",
    editor = "Ku, Lun-Wei  and
      Martins, Andre  and
      Srikumar, Vivek",
    booktitle = "Proceedings of the 62nd Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers)",
    month = aug,
    year = "2024",
    address = "Bangkok, Thailand",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2024.acl-long.695/",
    doi = "10.18653/v1/2024.acl-long.695",
    pages = "12871--12882"
}
```

</details>
