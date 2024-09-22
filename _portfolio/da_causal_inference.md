---
title: "Causal Inference Projects: Predicting Intervention Results & PC Algorithm"
excerpt: "Exploring structural causal models and the PC algorithm for causal discovery"
tags: [CausalInference, SCM, PCAlgorithm, Interventions, DataGeneration]
collection: portfolio
---

## Project Overview

This portfolio entry includes two projects that explore different aspects of causal inference. The first project investigates the prediction of intervention results using a Structural Causal Model (SCM), while the second focuses on causal discovery using the PC algorithm.

## 1. Prediction of Intervention Results Using SCM

This project aims to predict the outcomes of interventions on a causal system by modeling the relationships between variables using a Structural Causal Model (SCM).

### Key Components

1. **SCM Model Definition:**
    - Variables \(X\), \(Y\), and \(Z\) represent dosage, health outcome, and genetic information, respectively.
    - Relationships among variables are defined as:
        - \(Z \rightarrow X\)
        - \(X \rightarrow Y \leftarrow Z\)

2. **Generating Observational Data:**
    - Observational data is generated using the model \(P(X, Y, Z)\), following the dependencies in the SCM.

3. **Intervening on the System:**
    - Interventions were made on \(X\) (dosage) by setting \(do(X = x_i)\) for specific values of \(x\), generating new data distributions.
    - The intervention mechanism uses random values \(x_i \in \{0, 2, 4, 8\}\) uniformly for each individual.

### Comparison of Observational vs Interventional Data:

| Aspect                | Observational Data       | Interventional Data        |
|-----------------------|--------------------------|----------------------------|
| Data Source           | SCM simulation            | Interventions on \(do(X)\)  |
| Variable Relationships| Inferred from SCM         | Controlled via intervention |
| Outcome Prediction    | Derived from SCM structure| Derived from modified SCM   |

## 2. Causal Discovery Using the PC Algorithm

The second project applies the PC algorithm, a well-known method for discovering causal structures from observational data.

### Key Components

1. **Independence Testing:**
    - The algorithm tests conditional independence between variables to prune non-causal edges in the graph.
    - An oracle for conditional independence testing was used to verify results against a known graph.

2. **Graph Estimation:**
    - The PC algorithm iteratively removes edges by checking conditional independencies.
    - The final output is a partially directed acyclic graph (DAG), which represents causal relationships.

3. **Performance Evaluation:**
    - The results of the algorithm were validated by comparing the discovered graph against a ground truth causal graph.
    - The accuracy of the PC algorithm was evaluated by the match between the predicted and actual causal structure.

### PC Algorithm Summary:

| Step                    | Description                                           |
|-------------------------|-------------------------------------------------------|
| Initialize Fully Connected Graph | Start with a fully connected undirected graph  |
| Conditional Independence Tests  | Perform independence tests to remove edges      |
| Edge Orientation         | Apply rules to orient remaining edges                 |
| Final Graph              | Outputs a partially directed graph representing causal structure |

## Resources

- **Code Repository**: 

[GitHub - Prediction of interventions](https://github.com/RiccardoCampanella/Reinforcement_Learning/tree/main/Predicting_results_of_interventions)
[GitHub - PC Algorithm](https://github.com/RiccardoCampanella/Reinforcement_Learning/tree/main/PC_algorithm)

- **Reference Paper**: "Causal Inference in Statistics: A Primer"
