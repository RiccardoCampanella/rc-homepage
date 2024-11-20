---
title: "ERA: A Goal-Based Agent Integrating LLMs and Ontology for Fake News Detection"
excerpt: "Analyzing the ERA agent's architecture, functionalities, and its applications in determining the veracity of news headlines"
tags: [AI, Fact-Checking, Ontology, LargeLanguageModels, Explainability, NewsVerification]
collection: portfolio
---



## Expert Reasoner Agent (ERA) Documentation

---

## Project Overview

This project presents the ERA agent, an AI-powered system designed to verify the truthfulness of news headlines. By combining a trusted ontology and a large language model (LLM), the ERA agent offers a robust framework for evidence gathering and decision-making. The system leverages state-management techniques, structured queries, and performance metrics to provide reliable verdicts and confidence scores for user-provided statements.

---

## Demo and Resources

### Poster
[![Project Poster](https://riccardocampanella.github.io/rc-homepage/images/IntelligentAgents-Poster.png)](https://riccardocampanella.github.io/rc-homepage/files/Intelligent_Agents_Final_Poster.pdf)

[Download Project Poster (PDF)](https://riccardocampanella.github.io/rc-homepage/files/Intelligent_Agents_Final_Poster.pdf)

### Demo Video
[![Demo Video](https://riccardocampanella.github.io/rc-homepage/images/ERA_Demo_thumbnail.jpg)](https://drive.google.com/file/d/1wQRHP-e1hsf_yXJwDukNKdG5ZmKvXHoO/view?usp=drive_link)

[Watch Demo Video](https://drive.google.com/file/d/1wQRHP-e1hsf_yXJwDukNKdG5ZmKvXHoO/view?usp=drive_link)

### Resources
- [Code Repository](https://github.com/RiccardoCampanella/Goal-based_LLM_Agent)
- [Dataset Source](https://www.kaggle.com/clmentbisaillon/fake-and-real-news-dataset)

---

## Overview

The **Expert Reasoner Agent (ERA)** is an AI-powered fake news detection system designed to analyze news headlines, provide verdicts on their truthfulness, and generate supporting arguments. ERA integrates trusted ontological knowledge with insights from a large language model (LLM) to balance reliability with breadth, ensuring robust and transparent decision-making.

---

## Goals and Challenges of AI-Based Fake News Detection

### Goals

1. **Verdict with Supporting Arguments:** ERA delivers a verdict on a headline's truthfulness, presenting pro and contra arguments for transparency and understanding.
2. **Integration of Diverse Sources:** Combines reliable ontological knowledge with the expansive capabilities of LLMs.
3. **User-Friendly Interaction:** Simplified inputs and detailed outputs, including confidence scores, for ease of use.
4. **Transparency and Verifiability:** Presents evidence-based conclusions to build trust and accountability.
5. **Continuous Learning:** Adapts through dynamic state transitions and historical data analysis to improve over time.

### Challenges

1. **Over-reliance on LLMs:** Managing biases and hallucinations inherent in LLM-generated content.
2. **Ontology Limitations:** Expanding the scope and keeping content updated for comprehensive coverage.
3. **Ethical and Privacy Concerns:** Safeguarding user data and preventing misuse.
4. **Balancing Trust and Confidence:** Integrating information reliability across sources for accurate scoring.
5. **Complex Planning:** Ensuring robust state transitions in dynamic environments.

---

## Architecture and Interactions

ERA adopts a **goal-based architecture** to dynamically plan, adapt, and respond to user inputs.

### Goal-Based Design

- **Main Goal:** Deliver a truthful verdict with supporting arguments.
- **Sub-goals:** Execute tasks like querying the ontology, interacting with the LLM, and generating confidence scores through hierarchical goal management.

### State Management System

- **State Transitions:** Defined states (*Idle, Input Processing, Information Gathering, Reasoning,* and *Output Generation*) guide ERA's operations.
- **Dynamic Decision-Making:** ERA learns from past actions and adapts decisions using contextual data and metrics.

### External Interactions

1. **Ontology:**  
   A trusted knowledge base organized across domains (e.g., health, environment). ERA uses SPARQL queries to extract structured information and validate user inputs.

2. **Large Language Model (LLM):**  
   Provides broader contextual arguments using prompt engineering to structure responses. The agent processes outputs to merge similar arguments and calculate reliability scores.

### Confidence Calculation

Trust scores from the ontology and LLM, combined with argument strength, are synthesized into a confidence score for each verdict.

---

## Query Formulation and Argument Analysis with the LLM

The ERA agent’s interaction with the LLM follows a structured two-stage query formulation process, followed by multi-step argument analysis.

### Query Formulation

1. **Generating Questions:**
   - Transforms the user statement into four questions, including two negations of the statement (avoiding the word "not").
   - Each question elicits varied perspectives to ensure comprehensive coverage.

   **Example:**  
   - *User Statement:* "Daily coffee boosts productivity."  
   - *Generated Questions:*  
      1. Does daily coffee boost productivity?  
      2. Is daily coffee a key factor in increased productivity?  
      3. Does daily coffee hinder productivity? (negation)  
      4. Is daily coffee's impact on productivity overstated? (negation)  

2. **Requesting Arguments:**
   - Each question is embedded in prompts instructing the LLM to provide concise arguments and assign reliability scores (1-10).

   **Example Prompt:**  
   *"Does daily coffee hinder productivity? (negation)" Present arguments concisely, focusing on evidence without speculation, and structure the response as evidence for or against the statement. Please give every statement a score from 1-10 on how reliable it is.*

### Argument Analysis

1. **Reliability Score Assessment:**  
   - Evaluates the LLM's assigned scores to gauge argument validity.

2. **Similarity Analysis and Merging:**  
   - Tokenizes arguments, uses cosine similarity to detect redundancies, and merges similar ones, averaging their reliability scores.

3. **Verdict and Confidence Calculation:**  
   - Aggregates arguments to determine whether the statement is true or false.
   - Confidence levels are calculated using base trust scores (LLM: 0.8) and adjusted for argument support or contradiction.

---

## The Role of the Ontology

The ontology underpins ERA’s fact-checking by providing structured and verified domain-specific knowledge.

### Contributions

1. **Structured Representation:** Organizes information for targeted queries.
2. **Domain Expertise:** Offers nuanced insights within its scope.
3. **Trusted Source:** Acts as a reliable counterbalance to the LLM.
4. **Supports Argumentation:** Enhances LLM-generated arguments with verified facts.

### Limitations

1. **Limited Scope:** Coverage is restricted to predefined domains.
2. **Static Nature:** Requires regular updates for ongoing relevance.

---

## Comparison of Agent Architectures

| **Characteristic**               | **Reflex-Based**                | **Utility-Based**             | **BDI**                      | **Goal-Based (ERA)**                      |
|-----------------------------------|---------------------------------|--------------------------------|--------------------------------|-------------------------------------------|
| **Decision Style**                | Predefined Rules                | Maximizes Utility              | Action-Driven Intentions      | Contextual Planning and Reasoning         |
| **Planning Capability**           | None                            | Short-Term Optimization        | Impulsive Plans               | Long-Term Causal Planning                 |
| **Adaptability**                  | Static                          | Moderate                       | Context-Aware                 | High                                      |
| **Transparency**                  | Low                             | Moderate                       | Low                           | High (Evidence and Confidence Provided)   |
| **Use Case Fit**                  | Simple, Static Scenarios        | Optimization Tasks             | Reactive Systems              | Complex, Dynamic Real-Life Scenarios      |

---

## Why a Goal-Based Architecture?

ERA's goal-based design supports dynamic decision-making, learning from prior interactions, and integrating multiple data sources. This architecture provides:

1. **Contextual Decision-Making:** Adapts to new inputs and environments for flexible reasoning.
2. **Long-Term Planning:** Prioritizes goal achievement with sequential, state-based planning.
3. **Transparent Reasoning:** Delivers transparent outputs supported by evidence, ensuring user trust.
4. **Balanced Integration:** Combines structured ontology data with the LLM’s expansive insights.

---

## Conclusion

The Expert Reasoner Agent (ERA) demonstrates the effectiveness of a goal-based architecture in addressing the challenges of AI-powered fake news detection. By combining reliable ontological data with the contextual breadth of LLMs, ERA offers a robust solution for delivering transparent, evidence-based verdicts in complex and dynamic scenarios.
```