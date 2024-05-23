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

However, language models not only inherit the challenges previously faced in benchmarking, but also introduce a slew of novel considerations which can make proper comparison across models difficult, misleading, or near-impossible. 

In this tutorial, we aim to bring attendees up to speed on the state of language model evaluation, and highlight current challenges in evaluating language model performance through discussing the various methods of evaluation, tasks and benchmarks commonly associated with evaluating progress in language model research. We will then discuss how these common pitfalls can be addressed and what considerations should be taken to enhance future work. 

<hr>


# Presenters
<div class="container" style="margin-top: 25px;margin-bottom: 40px;">
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


# Materials

Slides will be posted after the tutorial.

## Relevant Papers

The material in this presentation is loosely modeled off of [Lessons From the Trenches on Reproducible Evaluation of Language Models (Biderman, Schoelkopf, Sutawika et al. 2024)](arxiv.org/pdf/????.????). We recommend reviewing this paper if interested in learning more about this area for a number of other references.

## Code

[Language Model Evaluation Harness](https://github.com/EleutherAI/lm-evaluation-harness) is a library for prompted zero- and few-shot language model evaluations built around incorporating and mitigating a number of the challenges we discuss in this tutorial.



# Citation

<p>If you find this tutorial useful, please cite:</p>
<div class="container" style="margin-top: 20px;margin-bottom: 0px;">
{% raw %}
<pre><code>@misc{TODO,
  author = {Sutawika, Lintang and Schoelkopf, Hailey},
  title = {{ICML} Tutorial on Challenges in Language Model Evaluations},
  year = {2024},
  howpublished = {\url{https://lm-evaluation-challenges.github.io}},
}</code></pre>
{% endraw %}
</div>
<hr>

# Contact

{hailey, lintang}@eleuther.ai

# Acknowledgements

This site is modeled after [https://machine-learning-for-theorem-proving.github.io/](https://machine-learning-for-theorem-proving.github.io/).