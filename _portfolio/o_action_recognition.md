---
title: "Action Recognition in Still Images and Videos"
excerpt: "Implementation of a Two-stream network for classifying actions"
tags: [ComputerVision, DeepLearning, ActionRecognition, CNN, TwoStreamNetwork, OpticalFlow, 
TransferLearning, PyTorch, OpenCV, HMDB51, Stanford40, Finetuning, DataFusion]
collection: portfolio
---

## Project Overview

This project focuses on performing action classification in still images and videos using Convolutional Neural Networks (CNNs). We implement a Two-stream network architecture, combining spatial and temporal information for improved action recognition.

## Key Components

1. **Datasets**:
   - Still images: Stanford40
   - Videos: HMDB51
   - Custom two-stream dataset

2. **Models**:
   - Frames CNN (Spatial model)
   - Optical Flow CNN (Temporal model)
   - Two-stream CNN (Combined model)

3. **Techniques**:
   - Transfer learning
   - Fine-tuning
   - Optical flow extraction
   - CNN output fusion

## Methodology

1. Train and evaluate the Spatial model on Stanford40
2. Fine-tune the Spatial model on HMDB51
3. Train and evaluate the Temporal model on HMDB51
4. Combine pre-trained weights in the Two-stream model
5. Evaluate the Two-stream model on the custom dataset

## Two-stream Hypothesis

The project leverages the Two-stream hypothesis of the human visual cortex:
- Ventral stream: Object recognition
- Dorsal stream: Action recognition

By combining a DeepCNN for object recognition from still images with motion data extracted from optical flow, we aim to achieve better performance in action recognition tasks.

## Resources

- **Code Repository**: [GitHub - Action Recognition](https://github.com/RiccardoCampanella/Computer_Vision/tree/main/action_recognition)
- **Course**: Computer Vision at Utrecht University

---