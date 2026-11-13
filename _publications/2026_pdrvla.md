---
title: "PDRVLA: A Vision-Language-Action Model with Physical Dynamics Representations"
collection: publications
category: preprints
permalink: /publication/2026_pdrvla
excerpt: 'Author: <b>Hanqing Wang</b><sup>*</sup>, Zhaotian Cai<sup>*</sup>, Ruichuan An<sup>*</sup>, Bohan Zeng<sup>*</sup>, Tao Zhang<sup>*</sup>, Yilin Chen<sup>*</sup>, Xu Jiang, Kaiquan Chen, Chongyang Wu, Haoran Li, Fan Yang, Mingan Lin, Wentao Zhang, Zenan Zhou, Youzheng Wu, Xiaodong He'
date: 2026-10-30
venue: 'arXiv preprint arXiv:2610.37381'
paperurl: 'https://arxiv.org/pdf/2610.37381'
---

*Featured as **Hugging Face Daily Paper #2** and **Monthly Paper #4**.*

## TL;DR

Introduces a lightweight **Physical Dynamics Module** that extracts compact physical tokens from intermediate VLM features via direct future RGB/depth/optical-flow prediction and frozen video world-model supervision — conditioning VLA action generation without online video generation latency. Achieves **99.3%** on LIBERO, **89.9%** on LIBERO-Plus, **93.6%** on RoboTwin 2.0, and **81.5%** on SimplerEnv.

## Abstract

Vision–Language–Action (VLA) models generate robot actions from visual observations and language instructions, but their understanding of physical dynamics remains limited. Video world models can capture scene dynamics, yet generating future videos introduces high latency into the control loop. We introduce PDRVLA, whose lightweight Physical Dynamics Module extracts physical tokens from vision–language features to condition action generation without online video generation. The module learns through direct prediction of future RGB, depth, and optical-flow features, with auxiliary supervision through a frozen pretrained video world model. Training relies entirely on publicly available data, expanded through human-to-robot synthesis, subtask annotation, and embodied chain-of-thought (ECoT) annotation. Across four simulation benchmarks, PDRVLA achieves success rates of 99.3% on LIBERO, 89.9% on LIBERO-Plus, 93.6% on RoboTwin 2.0, and 81.5% on SimplerEnv. Ablations show improved future prediction with world-model supervision and evaluate how subtask conditioning, future object-pose supervision, and ECoT training affect action success.

## Links

- [Paper (arXiv)](https://arxiv.org/abs/2610.37381)
- [Hugging Face Paper](https://huggingface.co/papers/2610.37381)

## BibTeX

<details markdown="1">
<summary>Click to expand</summary>

```bibtex
@article{wang2026pdrvla,
  title   = {PDRVLA: A Vision-Language-Action Model with Physical Dynamics Representations},
  author  = {Wang, Hanqing and Cai, Zhaotian and An, Ruichuan and Zeng, Bohan and Zhang, Tao and Chen, Yilin and Jiang, Xu and Chen, Kaiquan and Wu, Chongyang and Li, Haoran and Yang, Fan and Lin, Mingan and Zhang, Wentao and Zhou, Zenan and Wu, Youzheng and He, Xiaodong},
  journal = {arXiv preprint arXiv:2610.37381},
  year    = {2026},
  url     = {https://arxiv.org/abs/2610.37381}
}
```

</details>
