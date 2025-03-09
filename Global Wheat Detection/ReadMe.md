# Global-Wheat-Detection
## Overview
The Global Wheat Detection project is aimed at identifying wheat heads from outdoor images of wheat plants. Accurate wheat head detection is crucial for estimating crop yield, assessing plant health, and optimizing agricultural practices worldwide.

## Objective
The objective was to develop machine learning models to detect wheat heads in images, estimating their number and size. The goal is to create a generalized solution that performs well across different genotypes, environmental conditions, and observational settings.

## Preprocessing and Data Augmentation
- Created a WheatDataset class to load images and annotations.

- Applied transformations for data augmentation.

- Built a DataLoader by using torch.utils.data.DataLoader to load batches efficiently.

# Model Training
I used FastRCNN model for training and prediction
I used a training loop with progress feedback and validation

## Potential uses
The model can be used for:

- Enable accurate wheat phenotyping across diverse environments.

- Help farmers make informed decisions about crop management.

- Improve global food security by optimizing wheat yield estimation.

- Reduce bias in existing object detection models for agriculture.

- By improving wheat detection, more efficient agricultural practices and food production, ultimately benefiting farmers and consumers worldwide.
