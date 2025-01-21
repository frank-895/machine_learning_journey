# Manual Linear Learner and Neural Network for MNIST Classification

This project demonstrates building a linear learner model and transforming it into a simple neural network (NN) for MNIST digit classification. It highlights foundational concepts in machine learning, such as data preparation, model creation, loss calculation, and optimization.

## Overview

- **Task**: Classify handwritten digits (0-9) from the MNIST dataset.
- **Models**: 
  - A linear learner model.
  - A neural network with non-linearity through activation functions.
- **Objective**: Demonstrate the impact of using deeper architectures on model accuracy.

## Process

### Data Preparation
- **Normalization**: Scaled images to [0, 1].
- **Flattening**: Converted images from 28x28 to 784-dimensional vectors.
- **Labels**: Integer labels (0-9) for classification.

### Linear Learner Model
- **Architecture**: Single linear layer (`y = XW + b`).
- **Loss**: Cross-entropy loss for multi-class classification.
- **Optimization**: Gradient descent (η = 0.1).

### Transition to Neural Network
- **Non-linearity**: Added ReLU activation.
- **Architecture**: 3-layer NN (784 → 30 → 10).
- **Accuracy**: Improved from ~63% (linear model) to ~75% (NN).

### Training and Evaluation
- **Epochs**: 20 for both models.
- **Optimization**: Stochastic Gradient Descent (SGD).

## Results
- **Linear Model**: ~63% accuracy after 20 epochs.
- **Neural Network**: ~75% accuracy after 20 epochs.

## Key Learnings
- **Linear Learner**: Illustrates basic matrix operations, gradient descent, and linear model limitations.
- **Neural Networks**: Highlights the importance of non-linearity for learning complex patterns.
- **Optimization**: Demonstrates how SGD updates weights to minimize loss.
