---
title: "Symbolic, Subsymbolic, and Hybrid Approaches in AI: A Philosophical Perspective"
excerpt: "Exploring the ongoing debate in AI between symbolic, subsymbolic, and hybrid approaches, with a focus on deep learning limitations and the promise of neuro-compositional systems."
tags: [AI, Philosophy, SymbolicAI, DeepLearning, NeuroCompositionalComputing, CognitiveScience]
collection: portfolio
---

## Symbolic, Subsymbolic, and Hybrid Approaches in AI

---

### Project Overview

This project explores the philosophical and technical dimensions of AI through the lens of symbolic, subsymbolic, and hybrid approaches. Drawing from a debate between Gary Marcus and Yann LeCun, we delve into the strengths and limitations of deep learning, the role of symbolic reasoning, and the potential of hybrid neuro-compositional systems.

The discussion highlights the interplay between **System 1 Thinking** (automatic, biased, and subsymbolic) and **System 2 Thinking** (rational, deliberate, and symbolic), illustrating how these cognitive frameworks map onto AI methodologies. We also examine the principles underpinning **Neurocompositional Computing (NCC)**, which integrates symbolic reasoning with the fluid adaptability of neural networks.

---

## Presentation Resources

### Download the Presentation
<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vSgzv6rGNG6kaOkCIM-DhNeTjQ1NrHURX8jg7XaORm5V5_cwzldkLle8_D6stmrs4qG_HrRqkz-1PI2/embed?start=true&loop=false&delayms=5000" frameborder="0" width="1280" height="749" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

---

## Deep Learning: Strengths and Critiques

### Strengths of Deep Learning
Deep learning, as a subsymbolic approach, has demonstrated exceptional capabilities in pattern recognition and representation. Its flexibility and scalability make it the go-to methodology for applications like image recognition, natural language processing, and reinforcement learning.

### Critiques by Gary Marcus
However, Gary Marcus identifies several fundamental limitations:
1. **Shallow Understanding:**  
   - Deep learning systems excel at identifying patterns but fail to grasp abstract concepts or hierarchies, particularly in language understanding.  
   - Example: Struggles with compositional generalization, such as understanding that "lock" → "lockable" requires recognizing symbolic relationships.

2. **Opacity:**  
   - Operates as a "black box," making it unsuitable for tasks that require explainability or human trust.  
   - Example: In medical AI, lack of interpretability hinders adoption.

3. **Scalability Issues:**  
   - Scaling data and computational resources doesn't guarantee progress in abstraction or reasoning.  
   - Solutions like unsupervised learning and insights from cognitive psychology are needed to bridge this gap.

4. **Rigidity in Reasoning:**  
   - Deep learning lacks mechanisms for symbolic manipulation or higher-order reasoning, critical for human-like intelligence.

---

## Neurocompositional Computing: Bridging Symbolic and Neural Paradigms

### Abstract

To achieve human-level cognition, AI systems must be robust, accurate, and comprehensible. **Neurocompositional Computing (NCC)** provides a pathway by uniting two critical principles: **compositionality** and **continuity**. This hybrid paradigm overcomes the limitations of traditional symbolic and subsymbolic systems by encoding and processing information as vectors, allowing for symbolic reasoning and generalization while maintaining the fluid adaptability of neural networks.

---

### Principles of NCC
1. **Continuity:**  
   - Information is encoded as real-valued vectors, enabling smooth generalization to similar vectors.  
   - Neural networks learn patterns through gradual tuning, allowing them to generalize across similar inputs.  
   - Example: Words with similar contexts in training data (e.g., “lock” and “secure”) are encoded as nearby vectors, facilitating analogy-based learning.

2. **Compositionality:**  
   - Complex information is built by composing simpler structures.
   - TPRs explicitly encode relationships, such as "lock" and "lockable," or structured roles in language, math, and logic.
   - Symbolic structures, like phrase trees in language or chains of logical reasoning, are represented as activation vectors in a compositional manner.

---

### Central Paradox of Cognition
Human cognition is both **neural** and **compositional**, yet traditional AI systems have struggled to fully capture this dual nature:
- **Symbolic AI:** Satisfies compositionality but lacks the adaptability of continuous structures.
- **Subsymbolic AI (Deep Learning):** Satisfies continuity but fails to handle complex compositional generalizations, such as "lock" → "lockable."

NCC addresses these challenges by encoding information as **Tensor Product Representations (TPRs)**, which disentangle **what** (symbolic entities) and **where** (their structural roles) while ensuring continuity.

---

## Advantages and Applications of NCC

### Key Benefits
NCC systems offer:
- **Robust Learning:** Stronger generalization with less overfitting.
- **Explainability:** Reduced opacity compared to black-box models.
- **Control:** Precise manipulation of internal representations, reducing societal risks like misinformation or bias.

### Applications
1. **Math Problem Solving:**  
   Represent mathematical relationships like ratios using TPRs that encode numerator-denominator relations.

2. **Language Understanding (STORYNET):**  
   Encodes narrative events in a continuous graph structure.  
   Example: From "Mary went to the office," the model answers, "Where is Mary?" by generalizing unseen entity-task pairs.

3. **Robot Control (ROBONET):**  
   Transforms commands like "Jump twice" into precise actions by adjusting TPR encodings for dynamic control.  
   Example: Adjust "Jump twice" to "Jump thrice" by altering the vector representation.

4. **Image Captioning (CAPTIONNET):**  
   Generates captions by learning roles (e.g., object, action) and their relationships within image data.

5. **Question Answering (QANET):**  
   Encodes grammatical and semantic structures to answer questions from text sources like Wikipedia.

---

## Limitations and Future Directions

### Limitations
- **Restricted Generalization:** NCC still struggles with compositionality in highly abstract scenarios, such as nested structures.
- **Learning Efficiency:** While TPRs improve generalization, they require significant computational resources for training.
- **Interpretability:** Despite advances, disentangling complex TPRs in large-scale applications remains a challenge.

---

## Conclusion

The ongoing debate between symbolic and subsymbolic approaches highlights the need for a middle ground. **Neurocompositional Computing** offers a promising hybrid paradigm, addressing deep learning's shortcomings while retaining its strengths. By leveraging continuity and compositionality, NCC provides the foundation for AI systems that are robust, transparent, and capable of human-like reasoning.

--- 

## Resources

- **References**: [Compositional Structures in Neural Embeddings and Interaction Decompositions](https://arxiv.org/html/2407.08934v1), [Deep Learning a Critical Appraisal](https://arxiv.org/abs/1801.00631), [Deep Learning is Hitting a Wall](https://nautil.us/deep-learning-is-hitting-a-wall-238440/), [What AI Can Tell Us About Human Intelligence](https://www.noemamag.com/what-ai-can-tell-us-about-intelligence/), [Deep Learning Alone Isn't Getting Us To Human-Like AI](https://www.noemamag.com/deep-learning-alone-isnt-getting-us-to-human-like-ai/)
- **Course**: Philosophy of AI