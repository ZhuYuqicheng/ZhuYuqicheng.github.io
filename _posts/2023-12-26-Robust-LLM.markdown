---
layout: post
title:  Robust Knowledge Extraction from Large Language Models
description: Large-language models (LLMs) have the potential to support a wide range of applications. However, they are ill-suited for query answering in high-stake domains like medicine because they generate answers at random and their answers are typically not robust - even the same query can result in different answers when prompted multiple times.
date:   2022-12-26 15:23:35 +0300
image:  '/images/06.jpg'
tags:   [LLM, Robustness]
---
# Robust Knowledge Extraction from Large Language Models using Social Choice Theory

If you ever tried Large Language Models (LLMs) by yourself, you might have noticed that even if you ask the same question to LLM models such as chatGPT, you will get different answers. That is not an issue, even good for applications like creative writing, but it is more critical for query answering in high-stake domains like medicine. In order to improve the robustness of LLM queries, we propose using ranking queries repeatedly and to aggregate the queries using methods from social choice theory in our [paper](https://arxiv.org/abs/2312.14877) (accepted as full paper with oral presentation at AAMAS'24, Auckland). We study ranking queries in diagnostic settings like medical and fault diagnosis and discuss how the Partial Borda Choice function from the literature can be applied to merge multiple query results. We discuss some additional interesting properties in our setting and evaluate the robustness of our approach empirically.

