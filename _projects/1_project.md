---
layout: page
title: project 1
description: CSCI 214 (Pattern Recognition)
img: assets/img/12.jpg
importance: 1
category: acad
related_publications: false
---

## Project Summary
I sought to compare performances of modified neural network architectures in predicting poverty of Filipino households using non-financial indicators. Three standard, four-layer MLPs with different activation functions (ReLU, Swish-Beta, and Mish) were trained using the 2022 Annual Poverty Indicators Survey data from PSA. An emerging architecture, the Neural Additive Model (NAM), was also used as a more transparent, interpretable alternative model. Results show that non-ReLU activations improved gradient flow, evidenced by lower training loss values, but model generalization was not necessarily guaranteed. In contrast, NAM outperformed all other models across multiple metrics like accuracy and precision. Hence, a structured, feature-wise additive modeling technique may be more useful for poverty prediction tasks.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/cs214_table1.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Performance metrics used to compare the neural network architectures featured in this project. BaseNN refers to the ReLU-activated feedforward MLP.
</div>

## Artifacts
The written report can be accessed [here](https://drive.google.com/file/d/1zzINxiNdwl2Y1FYdwX4-C9jq5ejc1Ryc/view).