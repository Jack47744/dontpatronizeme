# dontpatronizeme Challenge

NLP Coursework for classifying the text contains patronising and condescending language

## Contributors

- Metis Sotangkur (ms922@ic.ac.uk, metis.sota@gmail.com)
- Natthorn Suwannapasri (ns2423@ic.ac.uk)
- Wutikorn Ratanapan (wr323@ic.ac.uk)

## Problem Description

While words like “poor-families” and ‘’homeless” can be directly considered a PCL, their absence does not mean a sentence is not PCL. Identifying PCL poses challenges to Natural Language Processing (NLP) due to the subjective nature of PCL.

Inspired by SemEval 2022 competition (task 4), the goal of this research is to train a model to detect patronizing and condescending language that outperforms RoBERTa-baseline. 


## DistilBERT with T5 paraphrasing

- We trained using the DistilBERT as our classifier.
- We augmented the data using T5 model to paraphrase the patronizing text and append the paraphrased positive-class text to the original training data.
- We augmented the text by randomly swapping the words after the first epoch.

<!-- ## Used External Libraries

- Give instructions on how to install the external libraries if you have used any in your code. -->

# Installation Instructions

To set up your environment for the project, you will need to install `simpletransformers`.

```bash
pip install -q simpletransformers gdown 
```
# Prediction Code

To make predictions for dev and test data, run the following jupyter notebook:

```bash
code/00_predict.ipynb
```

## Results

Our model could achieve F1-Score in the DEV set of 52.15%.
