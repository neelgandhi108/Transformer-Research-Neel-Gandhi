# Transformer-Research-Neel-Gandhi-NeurIPS

### Student - Neel Gandhi

### Professor Soroush Vosoughi

# **Interpreting reasoning behind language models for generating stereotypical text**

In this research work, we aim to understand the mechanisms and underlying logic that lead language models to generate text that perpetuates stereotypes. By interpreting the reasoning behind the generation of stereotypical text by language models, we hope to shed light on the potential biases present in these models and identify potential avenues for mitigating them. This work is being conducted under the supervision of Professor Soroush Vosoughi

# Interpretability of complex NLP models with Huggingface Transformers is made possible through the use of Captum.

I recently learned about Captum, a package developed by Meta (Facebook) that provides tools for interpreting and explaining the results of complex natural language processing (NLP) models. The package includes several widely accepted interpretation techniques and is designed to be used with the Huggingface transformer library. I decided to try out Captum for myself and followed a tutorial that demonstrated how to use it to interpret the results of a sentiment analysis model. Specifically, I used the Huggingface sentiment analysis pipeline.

To prepare for this tutorial, I installed several required packages and set up a virtual environment. Then, I set up the sentiment analysis model with just a few lines of code. To use Captum, I implemented a wrapper class that would allow me to generate feature importance through a process called Layer Integrated Gradients. Using this wrapper was as simple as a few more lines of code.

When I ran the code, I was able to see which words had the greatest impact on the model's prediction of positive or negative sentiment. Overall, I found Captum to be a promising framework for interpreting and explaining the results of NLP models, although it is still in its beta version and may require some patience to work with. I plan to continue exploring Captum and potentially even develop a python package to make it more user-friendly.

# Stereoset
I am trying to understand the biases of language models by using a test suite called Stereoset. It tests for biases in gender, profession, race, and religion. The test suite has two types of test cases: intersentence and intrasentence. In intersentence tests, we are given a context sentence and three candidate sentences, and we must predict how likely each of the three sentences are given the context. In intrasentence tests, we are given a context sentence with a missing word and three candidate words to fill in the blank. Stereoset has released 25% of their data as a development set, which includes 2123 intersentence cases and 2106 intrasentence cases. I will be evaluating the language model on this development set using three evaluation metrics: language modeling score (lms), stereotype score (ss), and idealized CAT score (icat). The lms measures the ability of the model to make meaningful associations, the ss measures the preference for stereotypical associations over anti-stereotypical associations, and the icat is a combination of the lms and ss.

# Wino_bias
WinoBias is a dataset designed to study coreference resolution in terms of gender bias using natural language processing, with a focus on detecting and addressing gender bias. It consists of sentences written in the Winograd schema style, in which entities are referred to by their occupation (e.g. "the nurse", "the doctor", "the carpenter"). The goal of WinoBias is to improve the accuracy of coreference resolution systems in identifying and disambiguating these entities.
This code is for analyzing and removing gender bias in natural language text. It begins by importing several libraries and loading a dataset called "wino_bias". It then defines a list of gendered terms and a dictionary for mapping these terms to gender. The code then iterates through a list of sentences, extracting any words that are within brackets and storing them in a list. If any of the gendered terms are found within this list, they are removed and the gender is recorded. The code then counts the number of occurrences of each gender for each extracted word and filters the results to show only those words that are associated with a single gender or are unisex. Finally, the code formats the input text as a JSON object and uses it to train a model to recognize and remove gender bias in text.


# CrowS-Pairs dataset
The CrowS-Pairs dataset is used to measure the presence of stereotypical biases in masked language models (MLMs). There have been significant issues found with the noise and reliability of the data in CrowS-Pairs, making it potentially unreliable for measuring biases in LMs, according to research by Blodgett et al. (2021). The dataset consists of 1,508 sentence pairs, each demonstrating or violating a stereotype about a historically disadvantaged group in the United States and a contrasting advantaged group. It covers nine types of biases: race/color, gender/gender identity, sexual orientation, religion, age, nationality, disability, physical appearance, and socioeconomic status. The data is stored in the file "crows_pairs_anonymized.csv" and can be used with the Python code to measure biases in the BERT, RoBERTa, and ALBERT MLMs. The script will output a CSV file with the sentence scores for each example and a binary score indicating whether the model is biased towards the more stereotypical sentence.




