[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/zain2525/SkimLit-NLP/blob/main/NLP_Project.ipynb)

# SkimLit-NLP
#### Build an NLP model to make reading medical abstracts.

## Problem in a sentence
The number of RCT papers released is continuing to increase, those without structured abstracts can be hard to read and in turn slow down researchers moving through the literature.

## Solution in a sentence
Create an NLP model to classify abstract sentences into the role they play (e.g. objective, methods, results, etc) to enable researchers to skim through the literature (hence SkimLit 🤓🔥) and dive deeper when necessary.

## What we're going to cover
  * Downloading a text dataset (PubMed RCT200k from GitHub)
  * Writing a preprocessing function to prepare our data for modelling
  * Setting up a series of modelling experiments (5) models
    * Deep models with different combinations of: token embeddings, character embeddings, pretrained embeddings, positional embeddings
  * Building our first multimodal model (taking multiple types of data inputs)
    * Replicating the model architecture from https://arxiv.org/pdf/1612.05251.pdf 
  * Find the most wrong predictions
  * Making predictions on PubMed abstracts from the wild
  
## What we're going to do!
### 1. Get The data
### 2. Preprocess data
  * Get lists of sentences
### 3. Make numeric labels (ML models require numeric labels)
  * Label encode labels
### 4. Creating a series of model experiments
### 5. Preparing our data for deep sequence models
  * Create text vectorizer
  * Create custom text embedding
### 6. Create datasets (as fast as possible)
### 7. Model 1: Conv1D with token embeddings
### 8. Model 2: Feature extraction with pretrained token embeddings
  * Building and fitting an NLP feature extraction model from TensorFlow Hub
### 9. Model 3: Conv1D with character embeddings
  * Creating a character-level tokenizer
  * Creating a character-level embedding
  * Building a Conv1D model to fit on character embeddings
### 10. Model 4: Combining pretrained token embeddings + character embeddings (hybrid embedding layer)
  * Combining token and character data into a tf.data dataset
  * Fitting a model on token and character-level sequences
### 11. Model 5: Transfer Learning with pretrained token embeddings + character embeddings + positional embeddings
  * Create positional embeddings
  * Building a tribrid embedding model
  * Create tribrid embedding datasets and fit tribrid model
### 12. Compare model results
### 13. Save and load best performing model
  * Make predictions and evalaute them against the truth labels
### 14. Evaluate model on test dataset
### 15. Find most wrong

