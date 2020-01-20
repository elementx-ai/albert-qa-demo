# Reading Comprehension with ALBERT (and similar)

Author: [@techno246](https://twitter.com/techno246)

## Introduction

Reading comprehension, otherwise known as Question Answer systems, are one of the tasks that NLP tries to solve. The goal of this task is to be able to answer an arbitary question given a context. For instance, given the following context:

> New Zealand (Māori: Aotearoa) is a sovereign island country in the southwestern Pacific Ocean. The country has two main landmasses — the North Island (Te Ika-a-Māui), and the South Island (Te Waipounamu) — and around 600 smaller islands. It has a total land area of 268,000 square kilometres (103,500 sq mi), and a population of 4.9 million.  Because of its remoteness, it was one of the last lands to be settled by humans. During its long period of isolation, New Zealand developed a distinct biodiversity of animal, fungal, and plant life. The country's varied topography and its sharp mountain peaks, such as the Southern Alps, owe much to the tectonic uplift of land and volcanic eruptions. New Zealand's capital city is Wellington, and its most populous city is Auckland.

We ask the question

> What is the capital of New Zealand? 

We expect the QA system is to respond with something like this:

> Wellington

Since 2017, transformer models have shown to outperform existing approaches for this task. Many variations of transformer models exist, including BERT, RoBERTA, XLNET. One of the newcomers to the group is ALBERT (A Lite BERT) which was published in September 2019. The research group claims that it outperforms BERT, with much less parameters (shorter training and inference time). 

This tutorial demonstrates how you can fine-tune a transformer model for the task of QnA and use it for inference. Note you can also skip the training step and just try out a pre trained model on the same dataset (save some time and carbon emissions). We will use the transformer library built by Hugging Face, which is an extremely nice implementation of the transformer models (including ALBERT) in both TensorFlow and PyTorch. 

Note that the goal of this is not to build an optimised, production ready system, but to demonstrate the concept with as little code as possible. Therefore a lot of code will be retrofitted for this purpose. 

Get started below:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/spark-ming/albert-qa-demo/blob/master/Question_Answering_with_ALBERT.ipynb)

