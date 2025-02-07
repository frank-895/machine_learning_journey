# Multi-target Classification - Paddy Doctor Competition

In this notebook, we'll be making a submission to this [Kaggle competition](https://www.kaggle.com/competitions/paddy-disease-classification/data?select=test_images). The goal of the competition is to use photos of rice to determine if the rice has a disease and which disease it has. 

However, for the purpose of this notebook, we will not be working towards making the best possible submission! We are using this competition as an opportunity to learn about multi-target classification, as in addition to predicting which disease the rice has, *we will also be predicting the rice's variety.* 

We have used **multi-class classification**, where one instance can belong to >2 classes. **Multi-target classification** is different, as we are predicting two (or more) separate attributes of each instance. 

I would like to give credit to this notebook [Multi-target: Road to the Top, Part 4](https://www.kaggle.com/code/jhoward/multi-target-road-to-the-top-part-4/comments) from which the code is taken. I've adapted a lot of the prose to demonstrate my own understanding.

## Overview
- **Data Engineering**: Extracted training images from Kaggle API and defined a DataLoaders object for multi-target classification.
- **Create model**: Defined cross-entropy loss functions, error functions and created a learner to predict both variety and disease.
- **Train model**: We trained the model using 5 epochs and a learning rate of 0.01.

## Results
We predicted the disease with 4.52% error rate and variety with a 0.87% error rate, training the model in approximately 6 minutes using Colab's free GPU.

## Key Learnings
- **Multi-class vs multi-target classification**: The key differences between these two types of classification were established. In this project, we performed multi-class classification on both disease and variety (as there were 10 classes for each) and multi-target classification by predicting two separate features for each image. 
- **`DataBlock` API from FastAI**: Learnt how to use the `DataBlock` API to create a DataLoaders object on a lower-level for more flexibility. This is necessary when creating a multi-target model.
- **Cross-entropy loss**: Went through in specific detail how **softmax** and **cross-entropy** are calculated, not just relying on mathematical formulas, but applying them to an example. I now understand exactly how we can create a single loss for a batch of inputs that output >2 predictions. I also learnt where loss functions are stored in PyTorch (both as a class and as a function).
- **Multi-target model**: Finally, I learnt how to define and train a multi-target model using FastAI, by defining our loss functions, metrics and number of outputs.

## Credits
This code is based on code provided by the fastai course, especially a number of Kaggle notebooks accessible through their website: https://www.fast.ai. The FastAI team has provided tools and resources that helped in developing this work. I have adapted the code and content to demonstrate my own learning and to help others!
