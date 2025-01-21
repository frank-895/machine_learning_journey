# Hugging Face Transformers for Regression: Pearson Correlation

This project demonstrates the use of Hugging Face Transformers to predict the similarity score between pairs of sentences. The model is fine-tuned on a pre-trained transformer to solve a regression task and evaluates performance using the Pearson correlation coefficient.

## Overview

- **Task**: Predict similarity between sentence pairs.
- **Metric**: Pearson correlation coefficient for evaluating regression performance.
- **Model**: Fine-tuned pre-trained DeBERTa-v3 for regression.
- **Dataset**: Kaggle competition data.

## Key Steps

1. **Data Preparation**:
   - Tokenize and normalize the text data.
   - Split the dataset into training and validation sets.

2. **Model**:
   - Use Hugging Face's pre-trained DeBERTa-v3 model.
   - Fine-tune for a regression task with a single output.

3. **Training**:
   - Use the `Trainer` API with specified hyperparameters (batch size, learning rate, epochs).

4. **Evaluation**:
   - Compute Pearson correlation between predictions and ground truth.
   - Clip predictions to the [0, 1] range.

5. **Submission**:
   - Create a Kaggle submission file from the predictions.

## Results

- **Pearson Correlation**: Achieved a final score of **0.83**.
- **Prediction Clipping**: Ensured predictions are within [0, 1].

## Key Learnings

- **Transfer Learning**: Leveraging pre-trained models like DeBERTa-v3 significantly improved model performance, especially with limited data.
- **Regression with Transformers**: Fine-tuning a transformer for a regression task requires careful handling of output layers and metrics.
- **Pearson Correlation**: Using Pearson correlation as a metric is effective for evaluating similarity in regression tasks, but is sensitive to outliers.
- **Model Fine-Tuning**: Even with a relatively simple architecture and a few epochs, fine-tuning a pre-trained model can yield impressive results.
