---
layout: page
title: Challenges in Language Model Evaluations
---
<head>
  <link rel="icon" type="image/svg+xml" href="./img/ICML-logo.svg">
</head>
<div class="venue" style="font-size: 27px; display: block; font-family: 'Open Sans', 'Helvetica Neue', Helvetica, Arial, sans-serif; font-weight: 300; color: #404040; text-align: center;">
  <a target="_blank" href="https://icml.cc/virtual/2024/tutorial/35227"><strong>Video Recording</strong></a>
  <br>
  <strong>July 22, 2024<br>3:30-5:30pm GMT+2</strong>
</div>



<div class="sharethis-inline-share-buttons"></div>
<meta name="thumbnail" content="./img/ICML-logo.svg" />


# Overview

NLP and Machine Learning rely on benchmarks and evaluation to accurately track progress in the field and assess the efficacy of new models and methodologies. For this reason, good evaluation practices and accurate reporting are crucial. 

However, language models (LMs) not only inherit the challenges previously faced in benchmarking, but also introduce a slew of novel considerations which can make proper comparison across models difficult, misleading, or near-impossible. 

In this tutorial, we aim to bring attendees up to speed on the state of language model evaluation, and highlight current challenges in evaluating language model performance through discussing the various methods of evaluation, tasks and benchmarks commonly associated with evaluating progress in language model research. We will then discuss how these common pitfalls can be addressed and what considerations should be taken to enhance future work. 

<hr>


# Presenters
<div align="center" class="container" style="margin-top: 25px;margin-bottom: 25px;">
  <div class="row">
    {% for p in site.data.presenters %}
    {% if forloop.index<=4 %}
    {% capture id %}{{ p[0] }}{% endcapture %}
    {% include profile.html p=p %}
    {% endif %}
    {% endfor %}
  </div>
  <div class="row">
    {% for p in site.data.presenters %}
    {% capture id %}{{ p[0] }}{% endcapture %}
    {% if forloop.index>4 and forloop.index<=7%}
    {% include profile.html p=p %}
    {% endif %}
    {% endfor %}
  </div>
</div>
<hr>

<!-- # Panelists
<div class="container" style="margin-top: 20px;margin-bottom: 0px;">
  <div class="row">
    {% for p in site.data.panelists %}
    {% if forloop.index<=5 %}
    {% capture id %}{{ p[0] }}{% endcapture %}
    {% include profile.html p=p %}
    {% endif %}
    {% endfor %}
  </div>
  <div class="row">
    {% for p in site.data.panelists %}
    {% capture id %}{{ p[0] }}{% endcapture %}
    {% if forloop.index>5 and forloop.index<=10%}
    {% include profile.html p=p %}
    {% endif %}
    {% endfor %}
  </div>
  <div class="row">
    {% for p in site.data.panelists %}
    {% capture id %}{{ p[0] }}{% endcapture %}
    {% if forloop.index>10%}
    {% include profile.html p=p %}
    {% endif %}
    {% endfor %}
  </div>
</div>
<hr> -->

# Schedule

The tutorial will be held at 3:30-5:30pm GMT+2 on July 22nd. A preliminary outline of the schedule is as follows:

**LM Evaluation Fundamentals**
We will review the fundamentals of evaluating autoregressive LMs, covering the tools available to practitioners including: 
- Measurements such as perplexity, loglikelihood-based multiple choice, and text generation.
- Associated commonly-used metrics 
- A brief summary of the in-context learning (ICL) and prompting paradigm.

**Challenges Resulting From LMs**
We will then cover a number of challenges resulting from the Language Model side of LM evaluation--concerns that are novel or exacerbated by LMs.
- Reproducibility challenges unique to LMs, including the importance of prompting, prompt engineering, and non-robustness to implementation details
- Data contamination rendering evaluations invalid, skewed, or gameable
- Drawing fair comparisons across methods where factors such as architecture, dataset, or compute may vary--which is often contextual and goal-dependent
- The challenges inherent in attempting to reliably score natural language outputs. 

**Challenges Resulting From Benchmarks**
Next, we will discuss broader concerns and challenges faced in evaluation and benchmarking as a whole, which apply to LM evaluation as well.
- What qualities or tasks do practitioners wish to evaluate in LMs?
- The typical life cycle of a benchmark dataset, and the [steering effects of popular benchmarks on the field](https://arxiv.org/abs/2107.07002)
- Challenges in measurement validity, including for LMs in particular.
- Improving the rigor of typical evaluation setups, such as by introducing statistical significance testing or, when possible, the use of multiple seeds (both of which are not common practice in LM research).

**Addressing Pitfalls, and Where To Go From Here**
- We will highlight libraries commonly used to improve reproducibility and comparability of typical LM benchmarks, such as the [LM Evaluation Harness](https://github.com/EleutherAI/lm-evaluation-harness), [HELM](https://github.com/stanford-crfm/helm), and others.
- Brief discussion of several novel research threads in this subfield, as well as further minimum best practices for improving evaluation rigor.

# Materials

Slides will be posted after the tutorial, and a larger number of related references will also be uploaded closer to the tutorial.

## Relevant Papers

The material in this presentation is loosely modeled off of [Lessons From the Trenches on Reproducible Evaluation of Language Models (Biderman, Schoelkopf, Sutawika et al. 2024)](https://arxiv.org/abs/2405.14782). We recommend reviewing this paper if interested in learning more about this area, for a number of other references and resources.

## Code

[Language Model Evaluation Harness](https://github.com/EleutherAI/lm-evaluation-harness) is a library for prompted zero- and few-shot language model evaluations built around incorporating and mitigating a number of the challenges we discuss in this tutorial.


# Citation

<p>If you find this tutorial useful, please consider citing the following works:</p>
<div class="container" style="margin-top: 20px;margin-bottom: 0px;">
{% raw %}
<pre><code>@misc{sutawika2024challenges,
  author = {Sutawika, Lintang and Schoelkopf, Hailey},
  title = {{ICML} Tutorial on Challenges in Language Model Evaluations},
  year = {2024},
  howpublished = {\url{https://lm-evaluation-challenges.github.io}},
}</code></pre>

<pre><code>@misc{biderman2024lessons,
      title={Lessons from the Trenches on Reproducible Evaluation of Language Models}, 
      author={Stella Biderman and Hailey Schoelkopf and Lintang Sutawika and Leo Gao and Jonathan Tow and Baber Abbasi and Alham Fikri Aji and Pawan Sasanka Ammanamanchi and Sidney Black and Jordan Clive and Anthony DiPofi and Julen Etxaniz and Benjamin Fattori and Jessica Zosa Forde and Charles Foster and Mimansa Jaiswal and Wilson Y. Lee and Haonan Li and Charles Lovering and Niklas Muennighoff and Ellie Pavlick and Jason Phang and Aviya Skowron and Samson Tan and Xiangru Tang and Kevin A. Wang and Genta Indra Winata and François Yvon and Andy Zou},
      year={2024},
      eprint={2405.14782},
      archivePrefix={arXiv},
      primaryClass={cs.CL}
}</code></pre>

<pre><code>@misc{eval-harness,
  author       = {Gao, Leo and Tow, Jonathan and Abbasi, Baber and Biderman, Stella and Black, Sid and DiPofi, Anthony and Foster, Charles and Golding, Laurence and Hsu, Jeffrey and Le Noac'h, Alain and Li, Haonan and McDonell, Kyle and Muennighoff, Niklas and Ociepa, Chris and Phang, Jason and Reynolds, Laria and Schoelkopf, Hailey and Skowron, Aviya and Sutawika, Lintang and Tang, Eric and Thite, Anish and Wang, Ben and Wang, Kevin and Zou, Andy},
  title        = {A framework for few-shot language model evaluation},
  month        = 12,
  year         = 2023,
  publisher    = {Zenodo},
  version      = {v0.4.0},
  doi          = {10.5281/zenodo.10256836},
  url          = {https://zenodo.org/records/10256836}
}</code></pre>
{% endraw %}
</div>
<hr>

# Contact

{hailey, lintang}@eleuther.ai

# Acknowledgements

This site is modeled after [https://machine-learning-for-theorem-proving.github.io/](https://machine-learning-for-theorem-proving.github.io/).
