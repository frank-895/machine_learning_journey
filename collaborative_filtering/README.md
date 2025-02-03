# Collaborative Filtering - Predicting Movie Reviews

This project is a deep dive into how collaborative filtering works. I will be using collaborative filtering to recommend movies based on the preferences of other users and I will build the model from scratch, to help me gain a deeper understanding.

This notebook is based on similar work done in the FastAI course, specifically from this Kaggle notebook, [Collaborative Filtering Deep Dive](https://www.kaggle.com/code/jhoward/collaborative-filtering-deep-dive/notebook).

## Overview
- **Data extraction**: Data was taken from the **MovieLens dataset** and presented in a cross-tabulated way to understand the idea of **matrix completion**.
- **Creating the model**: An OOP approach was taken using PyTorch, were the model `DotProduct` was created and placed in a PyTorch `Learner`. Then, we used a **bias term** to define an even better model called `DotProductBias`.
- **Weight decay**: We used regularization to reduce overfitting, introducing the idea of weight decay.

## Results
The model had a validation loss of 0.862 - however, the result was less important, as the aim of this notebook was to understand collaborative filtering, rather than develop a world-class model!

## Key Learnings
- How collaborative filtering works.
- What **latent factors** are.
- What **embedding** is and how PyTorch implements this with an **embedding layer**.
- The idea of **class inheritance** in OOP.
- How to create a collaborative filtering model from scratch in PyTorch.
- Why a **bias term** is important with collaborative filtering.
- What **weight decay** is and why it improves the model. 

## Credits
This code is based on code provided by the fastai course, especially a number of Kaggle notebooks accessible through their website: https://www.fast.ai. The FastAI team has provided tools and resources that helped in developing this work. I have adapted the code and content to demonstrate my own learning and to help others!
