---
layout: post
title:  Calibration
description: placeholder for conformal prediction notes.
date:   2025-01-15 22:13:35 +0300
image:  '/images/06.jpg'
#tags:   [LLM, Robustness, Social Choice Theory]
---
# Calibration

### Definition of Calibration

Denote $X$ and $Y$ as input and output for neural network, respectively. Let $h$ be a neural network with $h(X)=(\hat Y, \hat P)$, where $\hat Y$ is a class prediction and $\hat P$ is its associated confidence, i.e., probability of correctness. *Perfect calibration* is defined as $$\mathbb{P}(\hat Y = Y\mid \hat P=p)=p, \forall p\in [0,1]$$



