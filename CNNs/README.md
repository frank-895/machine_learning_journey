# Convolution Neural Networks - Deep Dive
So far, we've learnt about the start of a machine learning models - the inputs. These can be categories, embeddings (basically a one-hot-encoded category) or continuous numbers.

We've also learnt about what comes out the end of the model - activations. These are tensors of numbers which we can constrain with softmax.

We've also had a little look at what can be in the middle, like matrix multipliers and activation functions.

But, there are other things that can go in the middle. A convolutional neural network (CNN) is a type of NN that works very well in computer vision applications.

## Overview
This notebook does not contain any code but instead diagrams and my personal notes from chapter 8 of the FastAI Practical Deep Learning for Coders course. I've included them in my portfolio as it demonstrates my understanding of the underlying logic behind CNNs.

My notebook includes the following topics:

- **What are convolutions?**
- **How does a CNN work** and what is?
  - Maxpool
  - Average pool
  - A dense layer
- **What is dropout?**

## Credits
This code is based on code provided by the fastai course, especially a number of Kaggle notebooks accessible through their website: https://www.fast.ai. The FastAI team has provided tools and resources that helped in developing this work. I have adapted the code and content to demonstrate my own learning and to help others!
