# Reading Comprehension with ALBERT (and similar)

Author: [@techno246](https://twitter.com/techno246)

Blog Post: https://www.spark64.com/post/machine-comprehension

## Introduction

Reading comprehension, otherwise known as question answering systems, are one of the tasks that NLP tries to solve. The goal of this task is to be able to answer an arbitary question given a context. For instance, given the following context:

> New Zealand (Māori: Aotearoa) is a sovereign island country in the southwestern Pacific Ocean. It has a total land area of 268,000 square kilometres (103,500 sq mi), and a population of 4.9 million. New Zealand's capital city is Wellington, and its most populous city is Auckland.

We ask the question

> How many people live in New Zealand?

We expect the QA system is to respond with something like this:

> 4.9 million

Since 2017, transformer models have shown to outperform existing approaches for this task. Many pretrained transformer models exist, including BERT, GPT-2, XLNET. One of the newcomers to the group is ALBERT (A Lite BERT) which was published in September 2019. The research group claims that it outperforms BERT, with much less parameters (shorter training and inference time). 

This tutorial demonstrates how you can fine-tune ALBERT for the task of QnA and use it for inference. For this tutorial, we will use the transformer library built by Hugging Face, which is an extremely nice implementation of the transformer models (including ALBERT) in both TensorFlow and PyTorch. You can just use a fine-tuned model from their [model repository](https://huggingface.co/models) (which I encourage in general to save money and reduce emissions). However for educational purposes I will also show you how to finetune it yourself so you can adapt it for your own data. 

Note that the goal of this is not to build an optimised, production ready system, but to demonstrate the concept with as little code as possible. Therefore a lot of code will be retrofitted for this purpose. 

Get started below:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/spark-ming/albert-qa-demo/blob/master/Question_Answering_with_ALBERT.ipynb)

