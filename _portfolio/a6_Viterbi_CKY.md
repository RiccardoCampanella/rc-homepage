---
title: "(NLP) Exploring Parsing Algorithms: Viterbi and CKY"
excerpt: "Analyzing probabilistic parsing techniques for syntactic structure recognition"
tags: [MachineLearning, NLP, Parsing, Viterbi, CKY, Syntax, ProbabilisticParsing]
collection: portfolio
---

## Abstract

This study investigates two foundational parsing algorithms in natural language processing: the Viterbi algorithm and the Cocke-Kasami-Younger (CKY) algorithm. Both are implemented and evaluated for syntactic parsing within a probabilistic context-free grammar (PCFG) framework. The experiments demonstrate their effectiveness in decoding sentence structures and discuss their computational trade-offs.

## Introduction

Parsing is a fundamental task in computational linguistics, enabling syntactic analysis of sentences to support downstream NLP applications such as machine translation and information retrieval. Probabilistic parsing incorporates statistical information into grammar rules, improving accuracy in ambiguous contexts. This work evaluates:
- The **Viterbi algorithm** for finding the most probable parse tree.
- The **CKY algorithm** for efficient syntactic parsing using dynamic programming.

## Methods

### Data Preparation
- Grammar: A probabilistic context-free grammar (PCFG) is designed with rules, non-terminals, and probabilities.
- Sentences: Input sentences are tokenized and mapped to the grammar for parsing.

### Parsing Algorithms
1. **Viterbi Algorithm**:
   - A dynamic programming approach to identify the most likely parse tree.
   - Utilizes a probability table to track the likelihood of subtrees during parsing.

2. **CKY Algorithm**:
   - Operates on a CNF (Chomsky Normal Form) grammar.
   - Constructs parse trees bottom-up by combining smaller constituents into larger ones.

### Implementation
- Both algorithms are implemented in Python, with emphasis on modularity for reusability and extensibility.
- Probabilities are calculated at each step to ensure the most probable parses are selected.

### Evaluation Metrics
- **Parsing Accuracy**: Measures the correctness of the parse tree structure.
- **Efficiency**: Computational complexity and execution time are analyzed for scalability.

## Results

### Parsing Accuracy
- Both algorithms successfully parsed input sentences, with identical results for ambiguous sentences under the given PCFG.

### Computational Efficiency
- **Viterbi Algorithm**: Higher computational overhead due to backtracking.
- **CKY Algorithm**: Demonstrated better efficiency with clear advantages in parsing longer sentences due to its bottom-up approach.

### Comparative Analysis

| **Algorithm**   | **Strengths**                                   | **Limitations**                                       |
|------------------|------------------------------------------------|------------------------------------------------------|
| **Viterbi**      | Finds the most probable parse tree.            | Computationally intensive for large grammars.        |
| **CKY**          | Efficient for CNF grammars with fewer rules.   | Limited to grammars in Chomsky Normal Form (CNF).    |

## Discussion

### Observations
- The Viterbi algorithm provides robust probabilistic parsing but is computationally demanding.
- The CKY algorithm is faster and more suitable for large-scale parsing tasks, provided the grammar is in CNF.

### Limitations
- Ambiguities in grammar can lead to multiple valid parse trees; resolving these requires additional semantic information.
- CKY's reliance on CNF conversion introduces preprocessing overhead.

### Future Work
- Extending the Viterbi algorithm to handle semantic disambiguation.
- Integrating machine learning models to optimize PCFG probabilities.

## Conclusion

The comparative study of Viterbi and CKY algorithms highlights their respective strengths and limitations in probabilistic parsing. Viterbi excels in probabilistic accuracy, while CKY offers computational efficiency. Together, they provide foundational tools for syntactic analysis in modern NLP systems.

## Libraries and Tools
- Python, NLTK, NumPy

---
## Resources
- **Code Repository**: [Viterbi and CKY](https://github.com/RiccardoCampanella/Natural_Language_Processing/blob/main/VIterbi_CKY.ipynb)
- **References**: [Viterbi Algorithm Paper](https://www2.isye.gatech.edu/~yxie77/ece587/viterbi_algorithm.pdf)
---
