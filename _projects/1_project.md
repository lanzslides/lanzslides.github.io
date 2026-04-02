---
layout: page
title: Evaluating Neural Network Variations for Prediction of Multidimensional Poverty in the Philippines
description: CSCI 214 (Pattern Recognition)
img: assets/img/12.jpg
importance: 1
category: acads
related_publications: false
---

## **Overview**

This paper explores the use of modified neural network architectures for predicting household-level poverty in the Philippines using multidimensional, non-financial indicators from the 2022 Annual Poverty Indicators Survey. A standard four-layer, ReLU-activated MLP was implemented as a baseline model and compared against MLPs with Swish-Beta and Mish activation functions. An emerging architecture, the Neural Additive Model (NAM), was also employed to present a more transparent, interpretable alternative.

Results showed that non-ReLU activations improved gradient flow, evidenced by lower training loss values, but model generalization was not necessarily guaranteed. In contrast, NAM outperformed all other models across multiple metrics like accuracy and precision. Hence, a structured, feature-wise additive modeling technique may be more useful for poverty prediction tasks.

## **Context**

Poverty is traditionally defined as the lack of sufficient of financial resources for an individual or a household to secure basic necessities and sustain a decent quality of life. However, recent decades have seen a substantial shift in poverty research beyond purely resourcist definitions. Leaning on Amartye Sen's capability approach, development and observance of various non-financial indicators were done to cater towards a more expansive definition of poverty.

Neural networks have shown promising performance to allow modeling of nonlinear interactions and complex feature relationships. Using the household-level Annual Poverty Indicators Survey (APIS) data, a nuanced view of poverty in the Philippines can be realized by considering its material and non-monetary dimensions.

## **Data and Methods**

The dataset used in this study was derived from the 2022 APIS, the most recent iteration released by the Philippine Statistics Authority. APIS presents a wide range of variables that reflect the socioeconomic profile of Filipino households. Particularly, it includes indicators related to housing materials and conditions, water and sanitation, access to basic utilities, ownership of appliances, internet use, enrollment and schooling patterns, receipt of government assistance programs, incidence of loans, and perceptions of safety within the community and institutions.

The neural network models were all implemented using Python, particularly via the machine learning framework PyTorch. The 85-feature, 43 517-row curated APIS dataset was divided into three random sets for training, validation, and testing, respectively, with an 80-10-10 split.

Model training was conducted under a consistent hyperparameter configuration across all experiments: the Adam optimizer was used with a learning rate of 0.001, a maximum of 50 training epochs, and early stopping function based on validation loss to prevent overfitting. To ensure reproducibility, all random seeds were set to 42. The evaluation of model performance was done by measuring the four standard metrics: accuracy, precision, recall and F1-score, together with the test loss and AUC-ROC.

## **Results**

<div class="row">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/cs214_table1.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Performance metrics used to compare the neural network architectures featured in this project. BaseNN refers to the ReLU-activated feedforward MLP.
</div>

The modifications on the neural network architecture has evidently affected model learning and predictive power in distinct ways relative to the baseline MLP that used the typical ReLU activation. Swish-Beta and Mish, both being smooth activation functions, improved gradient loss but their benefits to model generalization was not necessarily apparent. This could be attributed to the sparseness of the dataset. In contast, the NAM outperformed other models across multiple metrics of interest, providing robust predictive performance and inherent interpretability.
