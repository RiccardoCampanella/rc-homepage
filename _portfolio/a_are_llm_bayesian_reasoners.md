---
title: "Are LLM Belief Updates Consistent with Bayes’ Theorem?"
excerpt: "This paper evaluates whether large language models (LLMs) update their beliefs over propositions in a Bayesian-consistent manner as they scale in size and capability."
tags: [AI, BayesianInference, LanguageModels, CognitiveModeling, Epistemology, MachineLearning]
collection: research
---

## Are LLM Belief Updates Consistent with Bayes’ Theorem?

### 🔗 [Read the full paper on OpenReview](https://openreview.net/forum?id=Bki9T98mfr)

---

### Summary

This paper investigates whether larger and more capable language models (LLMs) update their "beliefs" more consistently with **Bayes’ theorem** when presented with new evidence in context.

---

### Key Contributions

- **Bayesian Coherence Error (BCE):**  
  A novel metric that quantifies how far LLMs deviate from Bayes’ rule when updating beliefs.

- **Dataset Generation:**  
  Custom datasets spanning 10 class categories with structured histories and evidential prompts were created to measure BCE.

- **Empirical Evaluation:**  
  BCE was computed for multiple models from five different LLM families using token-level probability estimates.

---

### Findings

- **Surprising Result:**  
  Contrary to expectations, **larger and more capable LLMs exhibit *greater* deviation** from Bayes' rule (i.e., higher BCE).

- **No Consistent Improvement with Scale or Data:**  
  BCE did not improve with model size, training data volume, or benchmark performance.

- **Explanations Proposed:**  
  - The **"reversal curse"**—LLMs struggle with token inversion (e.g., "A is B" vs. "B is A").
  - Pretraining may encourage heuristic learning over consistent probabilistic reasoning.
  - Token probability might not be a valid proxy for belief in abstract propositions.

---

### Implications

- Larger LLMs may **not** be moving toward coherent Bayesian reasoning as hypothesized.
- If belief updates remain inconsistent, LLMs may **not exhibit** expected utility maximization, **reducing risk** from certain alignment concerns—but also limiting interpretability and reliability.

---

### Future Directions

- Extend analysis to **fine-tuned models** and **larger-scale LLMs**.
- Use **known priors/likelihoods** (e.g., coin flips) for better benchmarking.
- Explore models not affected by token order constraints (e.g., **diffusion-based** or **bidirectional** LLMs).

---
