# Reddit Depression Symptom Prediction with NLP Techniques

## Project Overview

This project focuses on analyzing contextual data from Reddit posts to predict symptoms of depression. The goal is to leverage advanced NLP techniques to identify linguistic patterns that may indicate depressive tendencies among users.

## Features and Methodology

To achieve this, the project utilizes two key types of linguistic features:

**Latent Dirichlet Allocation (LDA)**: This is used to extract thematic content from the text, capturing the underlying topics within Reddit posts.\
**RoBERTa (Robustly Optimized BERT Pretraining Approach)**: A powerful language representation model that provides deep contextualized word embeddings, capturing the nuanced usage of language in different contexts.\
**Random Forest Classifier**, a robust machine learning model, to predict the likelihood of depression symptoms based on the linguistic patterns observed in the posts.

## Repository Structure

data: Contains the dataset extracted from Reddit. \
models: Includes the trained LDA and RoBERTa models. \
notebooks: Google Colab notebooks with data exploration and model training. \
src: Source code for data processing, feature extraction, and model training. \
main: Main function to run Random Forest Classifier with linguistic features. \
README.md: Project description and guidelines.

## Model Result
### LDA
LDA is a type of probabilistic topic model that assumes documents are mixtures of topics and that topics are mixtures of words. In this project, LDA is used to identify topics within the Reddit posts that correlate with known symptoms of depression. Each symptom's likelihood is expressed through an LDA Score, representing how strongly the associated words with the symptom appear as a topic in the text.

### RoBERTa
RoBERTa, building on BERT's language understanding capabilities, is fine-tuned here to classify text based on the presence of depressive symptoms. RoBERTa Score indicates the model's confidence in the symptom's presence within the text, with a higher score suggesting a greater likelihood of the symptom being expressed.

## Results
The table below summarizes the detection scores for each depression symptom:

| Symptom | LDA Score | RoBERTa Score |
|---------|-----------|---------------|
| Loneliness | 0.857270 | 0.886347 |
| Anxiety | 0.904333 | 0.933635 |
| Anhedonia | 0.889810 | 0.935636 |
| Sleep Problem | 0.843853 | 0.926923 |
| ... | ... | ... |

## Conclusion
The preliminary results are promising, showing that LDA and RoBERTa can effectively identify a range of symptoms associated with depression from text data. RoBERTa's deep learning approach complements LDA's topic modeling to provide a robust analysis of the data.

