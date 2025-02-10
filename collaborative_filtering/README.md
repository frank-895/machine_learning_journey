# Collaborative Filtering - Predicting Movie Reviews

This project is a deep dive into how collaborative filtering works. I will be using collaborative filtering to recommend movies based on the preferences of other users and I will build the model from scratch, to help me gain a deeper understanding.

We will be approaching collaborative filtering with 2 techniques:
1. **Probabilistic matrix factorization** (PMF) - dot product approach
2. **Deep learning** - neural network and concatenation approach

This notebook is based on similar work done in the FastAI course, specifically from this Kaggle notebook, [Collaborative Filtering Deep Dive](https://www.kaggle.com/code/jhoward/collaborative-filtering-deep-dive/notebook).

## Overview
- **Data extraction**: Data was taken from the **MovieLens dataset** and presented in a cross-tabulated way to understand the idea of **matrix completion**.
- **Creating the PMF model**: An OOP approach was taken using PyTorch, were the model `DotProduct` was created and placed in a PyTorch `Learner`. Then, we used a **bias term** to define an even better model called `DotProductBias`.
- **Weight decay**: We used regularization to reduce overfitting, introducing the idea of weight decay.
- **Creating an embedding module**: We understood the underlying logic of embedding modules and how they are optimised to 'search' on the GPU.
- **Embedding analysis**: We used the embedding vectors and bias terms to analyse the movies and users, and make meaningful comparisons based on **principle component analysis** and **cosine similarity**.
- **Creating the deep learning model**: We used PyTorch and FastAI to built a simple NN, adding in 2 hidden layers.
- **Bootstrapping and feedback loops**: We introduced the idea of the **bootstrapping problems** and the tendency of collaborative filtering models to amplify bias through feedback loops. 

## Results
The PMF model dot product approach had a validation loss of 0.854 and the deep learning model had a validation loss of 0.870. The deep learning model has the potential to incorporate metadata but does not take advantage of the specific problem domain, hence the worse result. However, the result was less important, as the aim of this notebook was to understand collaborative filtering, rather than develop a world-class model!

## Key Learnings
- What collaborative filtering is and when it might be used.
- How to build a collaborative filtering model based on **probabilistic matrix factorization** and dot product of embedding vectors.
- How to build a collaborative filtering model based on **deep learning** and concatenation of embedding vectors.
- What **latent factors** are.
- What an **embedding** is and how PyTorch implements this with an **embedding layer**.
- The idea of **class inheritance** in OOP.
- Why a **bias term** is important with collaborative filtering.
- What **weight decay** is and why it improves the model.
- How to create our own **embedding module**.
- How to analyse collaborative filtering models using:
  - The **bias term**
  - The **embedding vectors**
  - **Principle component analysis**
  - **Embedding distance**
- What **bootstrapping** is and when it needs to be used.
- How collaborative filtering models can perpetuate **bias** through a special type of **feedback loop**.

## Credits
This code is based on code provided by the fastai course, especially a number of Kaggle notebooks accessible through their website: https://www.fast.ai. The FastAI team has provided tools and resources that helped in developing this work. I have adapted the code and content to demonstrate my own learning and to help others!
