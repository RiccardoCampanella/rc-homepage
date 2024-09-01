---
title: "3D Voxel-based Person Tracking"
excerpt: "Offline color modeling and real-time voxel labeling for multi-person tracking"
tags: [ComputerVision, 3DReconstruction, Clustering, ColorModeling, RealTimeTracking, VoxelAnalysis]
collection: portfolio
---

## Project Overview

This project aims to develop a robust system for multi-person tracking using 3D voxel reconstruction and color modeling. The system operates in two phases: an offline phase for creating personalized color models, and an online phase for real-time tracking and labeling.

## Key Objectives

1. Create individual color models for each person in an offline process
2. Label voxels in real-time based on the pre-computed color models

## Methodology

### Offline Phase

1. **Camera Calibration**: Ensure accurate spatial relationships between multiple cameras
2. **3D Reconstruction**: Convert 2D frames into a 3D voxel representation
3. **Voxel Clustering**: Apply K-means clustering to group voxels by position
4. **Color Model Generation**: Project voxels onto camera views to create person-specific color models

### Online Phase

1. **Real-time Voxel Model**: Construct voxel model from incoming frames
2. **Voxel Clustering**: Group voxels using the established clustering method
3. **Color Model Matching**: Compare online color models with offline models
4. **Position Tracking**: Record 2D floor positions of clusters over time

## Key Features

- Multi-camera setup for comprehensive spatial coverage
- 3D voxel reconstruction for robust spatial representation
- K-means clustering for efficient voxel grouping
- Gaussian Mixture Models (GMMs) for color modeling
- Real-time tracking and labeling of multiple persons

## Technologies Used

- OpenCV for image processing and camera calibration
- scikit-learn for K-means clustering and GMM implementation
- Matplotlib for visualization of tracking results
- Scipy

## Challenges and Solutions

- **Occlusion Handling**: The 3D voxel approach helps in managing partial occlusions
- **Real-time Performance**: Efficient algorithms and optimized code ensure real-time processing
- **Color Ambiguity**: Person-specific color models improve distinction between similarly clothed individuals



## Resources

- [Project Repository](https://github.com/RiccardoCampanella/Computer_Vision/tree/main/color-based_voxel_labeling)
- [Demo Video](https://drive.google.com/file/d/1IP3RUehhRxGeZmYhYHIlPANqkQXWf8xw/view)

---
