# LLM Policies for Text-based Reinforcement Learning: An Interactive Tutorial

[**Mauricio Tec**](mauriciogtec.com), *Harvard University*, [`mauriciogtec@hsph.harvard.edu`](mailto:mauriciogtec@hsph.harvard.edu)


[**Link to tutorial**](https://github.com/mauriciogtec/llm_policies_for_text_based_rl_tutorial/blob/main/llm_policies_for_text_based_rl_tutorial.ipynb)

# Overview


**Summary**. This interactive notebook demonstrates how to train a reinforcement-learning agent in text-based environments using an LLM-parameterized policy. The ability to understand and generate natural language is essential for AI systems that need to interact with humans in a variety of domains, including customer service, healthcare, and education. By training reinforcement-learning agents in text-based environments, we can develop AI systems that are better able to understand and respond to human language, leading to more effective and versatile AI applications. The challenges faced by text-based agents are shared with other unstructured data environments, such as images and video. Investigating LLMs has implication beyond text, while maintaining the advantage of the emergence of highly capable text-based foundation models (LLMs) that can be finetuned with standard GPUs.

In this tutorial, we will specifically train an agent interacting with the [Textworld (Côté et al. 2019)](https://arxiv.org/abs/1806.11532) environment, which was used in the [2019 Textworld competition](https://www.microsoft.com/en-us/research/project/textworld/competition/) organized by Microsoft Research. Other text-based environments could be considered, such as the classic [Zork game (Anderson et al., 1977)](https://en.wikipedia.org/wiki/Zork) or the Jericho’s suit of games [(Hausknecht et al., 2019)](https://arxiv.org/pdf/1909.05398). Nonetheless, Textworld provides a fast and highly parameterizable environment. We will use an easy-to-solve configuration for the purpose of this tutorial.

**Target Audience**. This tutorial is designed for researchers familiar with reinforcement learning but with possibly limited hands-on experience in training and fine-tuning LLMs.

**Learning Objective**. The tutorial covers key topics such as (1) parameterizing a policy using an LLM for text generation, (2) supervised fine-tuning with expert demonstrations, and (3) reinforcement learning with proximal policy optimization. The tutorial highlights strategies for efficient computation and memory management, including quantization and low-rank adaptation, which are crucial for scenarios with limited computational resources.

### Contributions

* It facilitates barrier to entry to RL folks
* It highlights elements to pay attention and challenges in the area
* Provides a useful starting code

The structure of training a text-based agents bears similarities with reinforcement learning from human feedback (RLHF). However, in constrat to RLHF, the environment dynamics and reward function are externally by the environment [(Carta et al. 2023)](https://arxiv.org/pdf/2302.02662v3). This difference requires an outer loop to control the experience collection.
