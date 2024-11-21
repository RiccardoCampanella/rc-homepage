---
title: "(NLP) Exploring LSTM for UPOS Tagging and BERT for Word Sense Disambiguation"
excerpt: "Evaluating sequence labeling and contextual embeddings for linguistic tasks"
tags: [MachineLearning, NLP, LSTM, BERT, UPOS, WSD, LinguisticProcessing]
collection: portfolio
---

## Abstract

This study explores the effectiveness of deep learning models for two critical natural language processing (NLP) tasks: Universal Part-of-Speech (UPOS) tagging and Word Sense Disambiguation (WSD). Long Short-Term Memory (LSTM) networks are evaluated for sequence labeling tasks such as UPOS tagging, while BERT embeddings are applied to WSD to leverage contextual representations. The experiments highlight model performance, optimization techniques, and the implications of leveraging contextual information in NLP tasks.

## Introduction

Natural language understanding tasks often rely on accurate linguistic annotation and contextual comprehension. UPOS tagging is essential for syntactic analysis, while WSD is critical for interpreting semantic context. This study employs:
- **LSTM models** for UPOS tagging to leverage sequential patterns in text.
- **BERT embeddings** for WSD to capture contextual nuances of polysemous words.

## Methods

### Data Preparation
- Datasets: Preprocessed linguistic datasets containing annotated sentences for UPOS tagging and WSD tasks.
- Features: Tokenized text sequences with associated UPOS tags and sense labels.
- Preprocessing: Lowercasing, tokenization, and sequence padding for uniform input lengths.

### Models and Architectures
1. **LSTM for UPOS Tagging**:
   - Sequential LSTM layers for processing token sequences.
   - Embedding layers for representing words.
   - Softmax output layer for predicting UPOS tags.

2. **BERT for WSD**:
   - Pretrained BERT embeddings used to generate contextual representations of words.
   - Fine-tuned classification head to predict word senses based on contextual embeddings.

### Training and Evaluation
- Optimizer: Adam optimizer with learning rate scheduling.
- Loss Function: Categorical cross-entropy for both tasks.
- Metrics: Accuracy and F1-score for performance evaluation.
- Validation Split: Train-validation split to prevent overfitting.

### Explainability Techniques
- Attention Weights: For analyzing word dependencies in LSTM.
- Embedding Visualization: To observe the semantic clustering in BERT embeddings.

## Results

### UPOS Tagging with LSTM
- The LSTM model achieved robust performance with an accuracy of over 95% on the validation set.
- Sequential dependencies in the text were effectively captured, with minimal misclassifications for ambiguous tokens.

### WSD with BERT
- Leveraging BERT embeddings improved word sense disambiguation accuracy to 88%.
- Contextual representation of polysemous words was a significant advantage, with fewer errors for closely related senses.

### Comparison
| Task            | Model  | Accuracy | Observations                                                                 |
|------------------|--------|----------|------------------------------------------------------------------------------|
| **UPOS Tagging** | LSTM   | 95%      | Effective for syntactic annotation but limited in capturing semantic nuances.|
| **WSD**          | BERT   | 88%      | Superior contextual understanding; benefits from pretraining on large corpora.|

## Discussion

### Model Strengths
- **LSTM**:
  - Captures sequential structure effectively.
  - Lightweight and interpretable for sequence tagging tasks.
- **BERT**:
  - Context-aware embeddings significantly improve semantic tasks.
  - Generalizes well across diverse linguistic contexts.

### Limitations
- LSTM struggles with long-distance dependencies compared to transformers.
- BERT's computational cost and memory requirements are higher than traditional models.

### Future Work
- Incorporating transformer-based architectures for UPOS tagging to compare with LSTM.
- Extending WSD experiments with multilingual datasets to evaluate cross-linguistic capabilities.

## Conclusion

The integration of LSTM for UPOS tagging and BERT for WSD demonstrates the potential of deep learning architectures in NLP. While LSTM excels in sequence labeling tasks, BERT provides a robust approach for semantic disambiguation, showcasing the power of contextual embeddings. These findings underscore the importance of model selection and task-specific optimization in NLP pipelines.

## Libraries and Tools
- TensorFlow, Keras, Hugging Face Transformers
- NLTK, Scikit-learn, Matplotlib

---
## Resources
- **Code Repository**: (https://github.com/RiccardoCampanella/Natural_Language_Processing/blob/main/LSTM_UPOS_Tagging_and_BERT_WSD.ipynb)
- **Datasets**: [Universal Dependencies for UPOS](https://universaldependencies.org/), [WordNet for WSD](https://wordnet.princeton.edu/)
---
