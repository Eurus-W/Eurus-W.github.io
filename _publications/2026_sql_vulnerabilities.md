---
title: "Beyond Static Rules: Automated Discovery of Latent Vulnerabilities in Text-to-SQL"
collection: publications
category: conferences
permalink: /publication/2026_sql_vulnerabilities
excerpt: 'Author: <b>Hanqing Wang</b><sup>*</sup>, Yongdong Chi<sup>*</sup>, Jian Yang, Lei Yang, Jiehui Zhao, Yun Chen, Guanhua Chen'
date: 2026-04-07
venue: 'Findings of ACL 2026'
paperurl: 'https://aclanthology.org/2026.findings-acl.842.pdf'
---

*Method: **SAGE** — Systematic Automated Guided Exploration.*

## TL;DR

SAGE (Systematic Automated Guided Exploration) automates the discovery of latent failure patterns in LLM-based Text-to-SQL — going beyond static rule-based detection by generating vulnerability hypotheses and using a continuously evolving Vulnerability Codex to design targeted perturbations.

## Abstract

While Large Language Models (LLMs) have achieved remarkable success in Text-to-SQL tasks, their deployment in real-world environments is hindered by latent reliability issues. Identifying these latent weaknesses is critical for building trustworthy database interfaces, yet current diagnostic approaches rely heavily on static, expert-defined rules, which lack the capability for systematic and automated exploration. To bridge this gap, we propose SAGE (Systematic Automated Guided Exploration), a novel framework designed to autonomously uncover latent failure patterns in LLM-based Text-to-SQL generation. Specifically, SAGE generates vulnerability hypotheses for given samples and references a continuously evolving Vulnerability Codex to design targeted perturbations, thereby iteratively verifying and documenting potential defects. Extensive experiments on state-of-the-art open-source LLMs demonstrate that SAGE uncovers a substantial number of failure cases, highlighting the significant fragility of current models. Furthermore, our analysis reveals that the Vulnerability Codex exhibits strong cross-model transferability, indicating that the discovered patterns represent generalized structural weaknesses. Finally, we explore SAGE's potential for remediation. Furthermore, a preliminary attempt at lightweight fine-tuning on the generated samples yields promising improvements, suggesting a scalable pathway for closing the reliability loop in future work.

## Links

- [Paper](https://aclanthology.org/2026.findings-acl.842/)
- [Code](https://github.com/sustech-nlp/SAGE)

## BibTeX

<details markdown="1">
<summary>Click to expand</summary>

```bibtex
@inproceedings{wang-etal-2026-beyond-static,
  title     = {Beyond Static Rules: Automated Discovery of Latent Vulnerabilities in Text-to-{SQL}},
  author    = {Wang, Hanqing and Chi, Yongdong and Yang, Jian and Yang, Lei and Zhao, Jiehui and Chen, Yun and Chen, Guanhua},
  booktitle = {Findings of the Association for Computational Linguistics: ACL 2026},
  year      = {2026},
  publisher = {Association for Computational Linguistics},
  url       = {https://aclanthology.org/2026.findings-acl.842/}
}
```

</details>
