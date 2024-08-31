---
title: "MEG Data Analysis Using Deep Learning"
excerpt: "Exploring VisionTransformers and RNNs for brain state classification"
collection: portfolio
---

## Project Overview

This project tackles the challenge of analyzing magnetoencephalography (MEG) data using deep learning techniques. The primary goal is to classify brain activities into distinct categories, advancing our understanding of neurological disorders and cognitive processes.

## Key Components

1. **Data Preparation**:
   - Loading datasets and labels (Intra and Cross)
   - Downsampling from 2034Hz to 125Hz
   - Z-score normalization for numerical stability

2. **Model Architectures**:
   - Convolutional Neural Networks (CNNs)
   - Recurrent Neural Networks (RNNs)
   - Video Vision Transformer (ViViT)

3. **Training Approaches**:
   - Intra-subject classification
   - Cross-subject classification
   - Hyperparameter tuning using grid search and random search

4. **ViViT Implementation**:
   - MEG data treated as "video" input
   - 2D spatial representation of brain's magnetic field
   - Spatiotemporal patch division
   - Transformer encoder for processing
   - Classification head for final output

## Methodology

1. **Data Processing**:
   - Mapping MEG sensors to 2D grid
   - Treating time points as video frames
   - Normalizing data for consistent scale

2. **ViViT Adaptation**:
   - Using Hugging Face implementation
   - Tubelet embedding for token mapping
   - 4D tensor input: (batch_size, time_points, height, width)

3. **Model Training**:
   - Separate training for intra and cross datasets
   - Hyperparameter tuning on cross dataset
   - Validation using test1 + test2 datasets
   - Final testing on test3 dataset

## Advantages of ViViT for MEG Data

- Captures both spatial and temporal dependencies
- Handles long-range dependencies crucial for brain activity analysis
- Self-attention mechanism identifies important spatiotemporal patterns
- Requires fewer computational resources compared to CNNs

## Technologies Used

PyTorch, Wandb, Sklearn, Keras, H5py

## Comparison of Attention Mechanisms: GRU vs ViViT

Both the GRU model and ViViT use attention mechanisms, but they differ in several key aspects:

| Aspect | GRU Attention | ViViT Attention |
|--------|---------------|-----------------|
| Dimensionality | 1D (sequence) | 3D (spatial + temporal) |
| Scope | Local context | Global dependencies |
| Parallelization | Limited | Highly parallelizable |
| Parameter Efficiency | Less efficient for long sequences | More efficient for long sequences |
| Interpretability | Easier to interpret | More complex patterns |
| Computation | Weighted sum of input states | Self-attention with Query, Key, Value matrices |
| Application to MEG | Focus on temporal dynamics | Captures complex spatiotemporal patterns |

The ViViT attention mechanism may be more suitable for capturing complex spatiotemporal patterns across the entire brain in MEG data, while GRU attention could be more focused on temporal dynamics within specific regions.


---

#AttentionMechanism #BrainStateClassification #Neuroimaging #SupervisedLearning 
#Transformers #RNNs #DataProcessing #IntraCrossPatientTraining #DeepLearning #MEG