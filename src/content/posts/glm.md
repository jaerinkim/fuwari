---
title: Generalized Linear Models
published: 2024-06-09
description: GLM Basics
image: ''
tags: [GLM, Generalized Linear Model]
category: Review
draft: true
---

## Generalized Linear Model (GLM) 

$$Y_i \sim f(\theta_i)$$

$$\theta_i = g(\mathbf{X}_i)$$

* Stochastic component: $f(\cdot)$

* Systematic component: $X$

* Link function: $g(\cdot)$

### Example: OLS

:::note[OLS Notation]
:::

$$Y_i = \alpha + \beta \mathbf{X}_i + \epsilon_i$$
 
$$\epsilon_i = \mathcal{N}(0, \sigma^2)$$

where

$$\hat{\mu}_{LS} \equiv \underset{\mu}{\arg\min} \sum_{i=1} \left( Y_i - \mu \right)^2$$

so when $\frac{\partial \hat{\mu}}{\partial \mu}=0$, we get $-2 \sum_{i=1}(y_i-\hat{\mu}) = 0$

s.t. $\hat{\mu}_{LS}=\bar{Y}$


:::note[GLM Notation]
:::

$$Y_i\sim \mathcal{N}(\mu_i, \sigma^2)$$

$$\mu_i = \alpha + \beta \mathbf{X}_i$$

where $f(y_1,y_2,...,y_n) = \prod_{i=1}^n f(y_i)$ and the log-likelihood function, $L=\sum_i \log f(y_i)$

and we get $\hat{\mu}_{GLM} = \underset{\mu}{\arg\max} L = \bar{Y}$ again.

:::tip[Some characteristics of estimators]
* Sampling Error: $\hat{\theta}-\theta$

* Bias: $\mathbb{E}(\hat{\theta}-\theta)$

* Mean Squared Error: $\mathbb{E}(\hat{\theta}-\theta)^2 = \underbrace{\mathbb{E}[\hat{\theta}-\mathbb{E}(\hat{\theta})]^2}_{\text{Variance}} + \underbrace{\mathbb{E}[\mathbb{E}(\hat{\theta})-\theta]^2}_{\text{Squared Bias}}$

:::


