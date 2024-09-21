# DiaLong: Benchmarking Reminiscence in Long Context Dialogues

This repository contains code and data for the DiaLong paper, which introduces a dataset and framework for long-context memory evaluation in Large Language Models. Download the DiaLong dataset [here]. (https://github.com/sameraslan/DiaLong/blob/4bcd860ff806e803487262cdd33fd6bcb4cb612c/DiaLong.csv). Read the full DiaLong paper [here](https://github.com/user-attachments/files/17085486/DiaLong.Paper.Sep.2024.pdf).

## Introduction
DiaLong is a dataset of long-context dialogues, parsed into four distinguishable sessions between two users, with an accompanying list of true and false facts about each session. Looking to benchmark your LLM's memory? With DiaLong, it is possible to test a model's ability to actively retain and retrieve information, serving as a critical measure of its memory within extended conversational contexts.


### Background
Large Language Model (LLM) performance is constrained by limited context length, which hinders the ability to conduct natural language processing tasks. This limitation, known as the problem of forgetfulness, results from LLMs' inability to recall information outside their context window, a challenge exacerbated in long-context dialogues. Despite attempts to extend the attention window to enhance memory capabilities, these efforts fall short due to the impractical demands of computational resources and the degradation in performance for longer contexts.

### Where does DiaLong come in?
We introduce a novel dataset (DiaLong) and memory benchmark designed to rigorously evaluate the capacity of current LLMs and emerging memory solutions in sustaining and retrieving information across prolonged dialogues, highlighting the necessity for further research to improve LLMs' memory functions for more coherent, accurate, and trustworthy conversational interactions.

Here is an overview of the memory task:
<p align="center">
  <img src="https://github.com/sameraslan/DiaLong/assets/82460915/bbee6c88-8b03-4ba2-a84c-e3416a03c841" width=400>
</p>

### Access the Dataset
Please find the DiaLong dataset in the [dialong.csv file](https://github.com/sameraslan/DiaLong/blob/4bcd860ff806e803487262cdd33fd6bcb4cb612c/DiaLong.csv).

## Run the Code
For those interested in modifying/extending the dataset or evaluating on their own models, we provide google colab notebooks to create long context conversations with associated true and false facts, create prompts, and evaluate.

### Dataset Creation
This notebook uses GPT-4 to make the multi-session chat conversations longer and more fluid, and generates accompanying true and false facts.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1lgQcPf96tA3d8aqw9uQYamejB0IjMkHn?usp=sharing)


### Prompt Creation
This notebook uses the created dataset to generate associated prompts for testing the ability of LLMs to differentiate between true and false facts.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1JXjlHGWJoGeOQWoBSckHssbOgxdFCNbk?usp=sharing)


### Response Generation and Evaluation
We open-source our response generation and evaluation notebooks for GPT-3.5 and GPT-4. Plug and play with your own OpenAI API key or modify the response generation to benchmark your own models.

#### Response Generation
This notebook runs the generated prompts on GPT-3.5 and GPT-4, via the OpenAI API.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1vG-pH1CyI87vJxN80IkTOMPyaxA-xxcc?usp=sharing)

#### Evaluation
This notebook compares the predicted true and false facts from the LLM responses with the ground truth, and generates metrics for in-context and out-of-context prompting. In-context refers to questions that must be answered by referring to the conversation within an LLMs context window, and out-of-context refers to questions where the answer resides further in the past (out of the context window).

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/10Ywkjj_47GoelNS31-ksp12ZvyB3yDHt?usp=sharing)

## Citation
If you use the DiaLong dataset or memory evaluation framework, feel free to cite us.
**TODO: Insert Creck Ciation**
