---
layout: single
title: "Curriculum Vitae"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

<div class="cv-download">
  <a href="/files/cv.pdf" class="btn btn--primary"><i class="fas fa-download"></i> Download PDF</a>
</div>

## Education

<div class="cv-entry">
  <div class="cv-entry-header">
    <span class="cv-entry-title">Shanghai University of Finance and Economics, China</span>
  </div>
  <div class="cv-entry-item">
    <span class="cv-entry-role">Ph.D. Candidate in Management Science and Engineering</span>
    <span class="cv-entry-date">Sep. 2022 – Jul. 2027 (Expected)</span>
  </div>
  <ul>
    <li>Supervised by Dr. Yun Chen</li>
  </ul>
  <div class="cv-entry-item">
    <span class="cv-entry-role">Bachelor of Computer Science</span>
    <span class="cv-entry-date">Sep. 2018 – Jul. 2022</span>
  </div>
</div>

## Research Interests

Large Language Models (LLMs), Parameter Efficient Fine-Tuning (PEFT), LLM Agents

## Technical Skills

- **Programming Languages:** Python, C/C++, SQL
- **Frameworks & Tools:** PyTorch, Hugging Face Transformers, DeepSpeed, vLLM, CUDA, Git

## Selected Research Experience

<div class="cv-entry">
  <div class="cv-entry-header">
    <span class="cv-entry-title">Tsinghua University NLP Lab (THUNLP) & QY Lab, China</span>
  </div>
  <div class="cv-entry-item">
    <span class="cv-entry-role">Research Intern</span>
    <span class="cv-entry-date">Sep. 2023 – Jan. 2025</span>
  </div>
  <ul>
    <li><b>Objective:</b> Research on parameter-efficient fine-tuning and model compression for large language models, supervised by Shuo Wang.</li>
    <li><b>Results:</b> Led LoRA-Flow (ACL 2024), a dynamic LoRA fusion mechanism for generative tasks; collaborated on Delta-CoMe (NeurIPS 2024), training-free delta compression with mixed-precision for LLMs.</li>
  </ul>
</div>

<div class="cv-entry">
  <div class="cv-entry-item">
    <span class="cv-entry-role">Enhancing Text-to-SQL with Fine-Grained Guidance from Pivot Programming Languages (Pi-SQL)</span>
    <span class="cv-entry-date">Co-First Author</span>
  </div>
  <ul>
    <li><b>Status:</b> Accepted to Findings of EMNLP 2025</li>
    <li><b>Method & Result:</b> Proposed using pivot programming languages (e.g., Python) as an intermediate representation to provide fine-grained structural guidance for Text-to-SQL generation.</li>
    <li><b>Links:</b> <a href="https://aclanthology.org/anthology-files/pdf/findings/2025.findings-emnlp.1369.pdf">[Paper]</a> | <a href="https://github.com/sustech-nlp/Pi-SQL">[Code]</a></li>
  </ul>
</div>

<div class="cv-entry">
  <div class="cv-entry-item">
    <span class="cv-entry-role">Harnessing Minor Singular Components for PEFT (MiLoRA)</span>
    <span class="cv-entry-date">First Author</span>
  </div>
  <ul>
    <li><b>Status:</b> Accepted to NAACL 2025</li>
    <li><b>Method & Result:</b> Proposed initializing LoRA adapters with minor singular components of pre-trained weight matrices, reducing interference with existing knowledge while enabling more effective task-specific adaptation.</li>
    <li><b>Links:</b> <a href="https://aclanthology.org/2025.naacl-long.248.pdf">[Paper]</a> | <a href="https://github.com/sufenlp/MiLoRA">[Code]</a></li>
  </ul>
</div>

<div class="cv-entry">
  <div class="cv-entry-item">
    <span class="cv-entry-role">Dynamic LoRA Fusion for LLMs in Generative Tasks (LoRA-Flow)</span>
    <span class="cv-entry-date">Co-First Author</span>
  </div>
  <ul>
    <li><b>Status:</b> Accepted to ACL 2024</li>
    <li><b>Method & Result:</b> Designed a dynamic gating mechanism that automatically determines token-level fusion weights across multiple LoRA modules during inference, enabling more flexible multi-task generalization.</li>
    <li><b>Links:</b> <a href="https://aclanthology.org/2024.acl-long.695.pdf">[Paper]</a> | <a href="https://github.com/thunlp/LoRAFlow">[Code]</a></li>
  </ul>
</div>

## Full Publications

**[1] Pi-SQL: Enhancing Text-to-SQL with Fine-Grained Guidance from Pivot Programming Languages**
Yongdong Chi\*, **Hanqing Wang**\*, Zonghan Yang, Jian Yang, Xiao Yan, Yun Chen, Guanhua Chen. *Findings of EMNLP 2025*
\[[Paper](https://aclanthology.org/anthology-files/pdf/findings/2025.findings-emnlp.1369.pdf)\]\[[Code](https://github.com/sustech-nlp/Pi-SQL)\]


**[2] MALoRA: Mixture of Asymmetric Low-Rank Adaptation for Enhanced Multi-Task Learning**
Xujia Wang, Haiyan Zhao, Shuo Wang, **Hanqing Wang**, Zhiyuan Liu. *Findings of NAACL 2025*
\[[Paper](https://aclanthology.org/2025.findings-naacl.312.pdf)\]

**[3] MiLoRA: Harnessing Minor Singular Components for Parameter-Efficient LLM Finetuning**
**Hanqing Wang**, Yixia Li, Shuo Wang, Guanhua Chen, Yun Chen. *NAACL 2025*
\[[Paper](https://aclanthology.org/2025.naacl-long.248.pdf)\] \[[Code](https://github.com/sufenlp/MiLoRA)\]

**[4] Delta-CoMe: Training-Free Delta-Compression with Mixed-Precision for Large Language Models**
Bowen Ping, Shuo Wang, **Hanqing Wang**, Xu Han, Yuzhuang Xu, Yukun Yan, Yun Chen, Baobao Chang, Zhiyuan Liu, Maosong Sun. *NeurIPS 2024*
\[[Paper](https://openreview.net/pdf?id=cr5EQRJlRn)\] \[[Code](https://github.com/thunlp/Delta-CoMe)\]

**[5] LoRA-Flow: Dynamic LoRA Fusion for Large Language Models in Generative Tasks**
**Hanqing Wang**\*, Bowen Ping\*, Shuo Wang, Xu Han, Yun Chen, Zhiyuan Liu, Maosong Sun. *ACL 2024*
\[[Paper](https://aclanthology.org/2024.acl-long.695.pdf)\] \[[Code](https://github.com/thunlp/LoRAFlow)\]

**[6] StyleBART: Decorate Pretrained Model with Style Adapters for Unsupervised Stylistic Headline Generation**
**Hanqing Wang**\*, Yajing Luo\*, Boya Xiong, Guanhua Chen, Yun Chen. *Findings of EMNLP 2023*
\[[Paper](https://aclanthology.org/2023.findings-emnlp.697.pdf)\]

**[7] Multilingual Sentence Transformer as A Multilingual Word Aligner**
Weikang Wang, Guanhua Chen, **Hanqing Wang**, Yue Han, Yun Chen. *Findings of EMNLP 2022 (short)*
\[[Paper](https://aclanthology.org/2022.findings-emnlp.215.pdf)\]


## Honors & Awards

<div class="cv-awards" markdown="1">

**Ph.D. Student (2022–Present)**

| Award | Year |
|-------|------|
| **"Academic Star"** — Highest honor at SUFE; 5 graduate students selected per year university-wide | Dec. 2025 |
| **National PhD Scholarship** — Awarded to ~3% of PhD students by the Ministry of Education, China | Sep. 2025 |
| **First-Class Academic Scholarship**, SUFE | Sep. 2024 |

**Undergraduate (2018–2022)**

| Award | Year |
|-------|------|
| **Outstanding Graduate**, SUFE | Jun. 2022 |
| **Honorary Bachelor**, SUFE | Jun. 2022 |
| **First Prize**, Chinese Undergraduate Computer Design Competition | Aug. 2021 |

</div>

## Professional Service

- Reviewer, ACL Rolling Review (ACL ARR); CCL 2025

## Others

- Member of the University Table Tennis Team and the School Basketball Team.
