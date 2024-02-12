# DiaLong
![Fig1](https://github.com/sameraslan/DiaLong/assets/82460915/22105a9b-a812-4643-8cfc-1a03effe8a0b)

This repository contains code and data for the DiaLong paper, which introduces a dataset and framework for long-context memory evaluation in Large Language Models.

## Access the Dataset
DiaLong is a dataset of long-context dialogues, parsed into four distinguishable sessions between two users, with an accompanying list of true and false facts about each session. You can access the DiaLong dataset via the dialong.csv file.

## Modify/Extend the Dataset
For those interested in modifying or extending the dataset, we provide google colab notebooks to create long context conversations with associated true and false facts.

### Dataset Creation
This notebook uses GPT-4 to make the multi-session chat conversations longer and more fluid, and generates accompanying true and false facts.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1lgQcPf96tA3d8aqw9uQYamejB0IjMkHn?usp=sharing)


### Prompt Creation
This notebook uses the created dataset to generate associated prompts for testing the ability of LLMs to differentiate between true and false facts.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1JXjlHGWJoGeOQWoBSckHssbOgxdFCNbk?usp=sharing)
