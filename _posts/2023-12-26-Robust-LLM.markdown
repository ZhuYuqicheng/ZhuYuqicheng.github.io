---
layout: post
title:  Robust Knowledge Extraction from Large Language Models
description: Large-language models (LLMs) have the potential to support a wide range of applications. However, they are ill-suited for query answering in high-stake domains like medicine because they generate answers at random and their answers are typically not robust - even the same query can result in different answers when prompted multiple times.
date:   2022-12-26 15:23:35 +0300
image:  '/images/06.jpg'
tags:   [LLM, Robustness]
---
Large-language models (LLMs) have the potential to support a wide range of applications like conversational agents, creative writing, text improvement, and general query answering. However, they are ill-suited for query answering in high-stake domains like medicine because they generate answers at random and their answers are typically not robust - even the same query can result in different answers when prompted multiple times. In order to improve the robustness of LLM queries, we propose using ranking queries repeatedly and to aggregate the queries using methods from social choice theory. We study ranking queries in diagnostic settings like medical and fault diagnosis and discuss how the Partial Borda Choice function from the literature can be applied to merge multiple query results. We discuss some additional interesting properties in our setting and evaluate the robustness of our approach empirically.

Arxiv version: [https://arxiv.org/abs/2312.14877](https://arxiv.org/abs/2312.14877)