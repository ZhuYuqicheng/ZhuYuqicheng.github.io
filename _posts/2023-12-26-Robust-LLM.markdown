---
layout: post
title:  Robust Knowledge Extraction from Large Language Models
description: Large-language models (LLMs) have the potential to support a wide range of applications. However, they are ill-suited for query answering in high-stake domains like medicine because they generate answers at random and their answers are typically not robust - even the same query can result in different answers when prompted multiple times.
date:   2022-12-26 15:23:35 +0300
image:  '/images/06.jpg'
tags:   [LLM, Robustness, Social Choice Theory]
---
# Robust Knowledge Extraction from Large Language Models using Social Choice Theory

If you ever tried Large Language Models (LLMs) such as chatGPT by yourself, you might have noticed: asking even exactly the same question can yield different answers. While that is not an issue for applications like creative writing, it is more critical for query answering in high-stake domains like medicine. In order to improve the robustness of LLM queries, we propose using ranking queries repeatedly and to aggregate the queries using methods from social choice theory in our [paper](https://arxiv.org/abs/2312.14877) (accepted as full paper with oral presentation at AAMAS'24, Auckland). We study ranking queries in diagnostic settings like medical and fault diagnosis and discuss how the Partial Borda Choice function from the literature can be applied to merge multiple query results. We discuss some additional interesting properties in our setting and evaluate the robustness of our approach empirically.

![AAMAS_visual](/images/AAMAS_visual.png)

## The Root of the Robustness Issue

Why do we encounter the robustness issue in LLMs' outputs? The essential reason is the randomness of the decoding process of LLMs. For simplicity, we can treat pre-trained LLM models as black-boxes that take text sequence as input and output a conditional distribution over the next token given the previous tokens. We randomly select tokens from the distribution to generate the answer sequence. Therefore, different answer sequence can be generated if we repeat the decoding process, in our ranking query setting, the random selection process would lead to different rankings.

![robustness issue](/images/AAMAS_blog_decoding.png)

There is a parameter called *temperature* (*t*) that can make the conditional distribution over next token sharper (t<1) or flater (t>1). In extreme case (t=0) the text generation process is deterministic, i.e., the model will always select the most likely token in each step. Would it solve the problem? 

First of all, we argue that the deterministic answers provided by greedy search will be somewhat random because it corresponds to some local optimum found by LLMs. Secondly, most users only have access to the web version of chatGPT, therefore can not change *temperature*. Instead of setting temperature to 0, we allows some randomness in the answer, but increasing the robustness.

> Follow-up content coming soon. :)
