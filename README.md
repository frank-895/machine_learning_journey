# Manual Linear Leaner and Neural Network for MNIST Classification

This project demonstrates the implementation of a linear learner model from scratch and the transition to a simple neural network (NN) to classify handwritten digits from the MNIST dataset. By building the models step-by-step, it showcases foundational concepts in machine learning and neural networks, emphasizing data preparation, model creation, loss calculation, and optimization.

## Overview

The project uses the MNIST dataset, which contains images of handwritten digits (0-9). The main objectives include:

1. Building a manual linear learner model to classify digits.
2. Enhancing the model by introducing non-linearity through activation functions, transforming it into a neural network.
3. Demonstrating the impact of using deeper architectures (NN) on model accuracy.

## Process and Implementation

### Data Preparation
- Dataset: Images were loaded using untar_data from FastAI.
- Normalization: Each image was scaled to a range of [0, 1] for uniformity.
- Flattening: Each image (28x28 pixels) was flattened into a 784-dimensional vector.
- Labels: Integer-encoded labels (0-9) were associated with each image.
- Dataset Creation: Combined features and labels into training and validation datasets.

### Linear Learner Model

- Weights and Bias Initialization: 
    - Weights initialized randomly with a shape of (784, 10) for multi-class classification.
    - Bias initialized as a (10,) vector.
- Model Architecture:
    - Single linear layer: `y = XW + b`, where `W` is weights and `b` is bias.
- Loss Function:
    - Cross-entropy loss for multi-class classification.
- Optimization:
    - Gradient descent with learning rate `η = 0.1`.
    - Gradients calculated using PyTorch’s backward() for efficient backpropagation.

### Transition to Neural Network
- Added non-linearity using the ReLU activation function.
- Redesigned the model as a 3-layer NN using PyTorch’s nn.Sequential:
    - Layer 1: Fully connected layer (784 → 30 neurons).
    - Layer 2: ReLU activation.
    - Layer 3: Fully connected layer (30 → 10 neurons).
- Improved accuracy from ~63% (linear model) to ~75% (NN).

### Training and Evaluation
- Training: Both models trained using a Learner from FastAI.
- Validation: Accuracy calculated using a batch-wise accuracy function.
- Epochs:
    - Linear model: 20 epochs.
    - Neural network: 20 epochs.
- Optimization: Stochastic Gradient Descent (SGD).

## Results
- Linear Model:
    - Achieved ~63% accuracy after 20 epochs.
- Neural Network:
    - Improved to ~75% accuracy after 20 epochs, demonstrating the power of non-linear transformations and deeper architectures.

## Key Learnings
1. Linear Learner: Demonstrates basic matrix operations, gradient descent, and the limitations of linear models for complex tasks.
2. Neural Networks: Showcases the importance of non-linearity in learning complex patterns.
3. Optimization: Explains how SGD updates weights to minimize loss and improve predictions.

## How to Run
1. Clone this repository
`
git clone https://github.com/your-username/manual-linear-learner
cd manual-linear-learner
`
2. Run the notebook or script
`
python train_model.py
`
