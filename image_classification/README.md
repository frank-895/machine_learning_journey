# Image Multiclass Classification - Estonian Mushrooms 🍄‍🟫🍄‍🟫🍄‍🟫
We will be entering this [Kaggle competition](https://www.kaggle.com/competitions/mushroom-multiclass-classification), which is a multiclass image classification project on Estonian mushrooms. The aim is to predict the type of mushroom to improve public safety and knowledge.

This project is an iterative approach to deep learning and I intend on trying a few different models to put forward multiple submissions.

The mushrooms are labelled 0-9 and each number corresponds to the following mushroom type:

0. amanita
1. boletus
2. chantelle
3. deterrimus
4. rufus
5. torminosus
6. aurantiacum
7. procera
8. involutus
9. russula

We have 300 images for each category - 3000 images in total.

## Overview

### Data Extraction
We used the Kaggle API to extract our images, sorting them based on a Pandas dataframe using `os` and `shutil` Python libraries. We decided to use a random validation set, as this was the method opted for in the test dataset.

### Baseline Model
We created a baseline model using the resnet family of architectures, focusing on speed. We used `to_fp16()` to increase our training speed further and `lr_find()` to select an appropriate learning rate.

### Convnext Architecture
We encapsulated a `train()` function and a `csv()` function so we can quickly test important hyperparameters and augmentation approaches. We upgraded architectures to Convnext, as our GPU was being underworked due to a bottleneck with the CPU. 

### Convnext with Padding
At this point, we had tried both squishing and cropping and now opted for **padding** the images. 

### Convnext with Padding & TTA
We used our convnext with padding model, but employed test time augmentation (TTA) to improve the predictions on the test set.

## Results

### Baseline Model
0.82 accuracy on the test set, scoring at the bottom of the leaderboard. 

### Convnext Architecture
0.910 accuracy on the test set, scoring 3rd on the leaderboard. 

### Convnext with Padding
0.913 accuracy on the test set, scoring 3rd on the leaderboard. 

### Convnext with Padding & TTA
0.92976 accuracy on the test set, **scoring 1st on the leaderboard!**

## Key Learnings
- **Kaggle API**: Instead of manually uploading our data, we can use the Kaggle API to extract it directly in our code.
- **Secrets in Colab**: We can use the secrets feature of Colab to store API keys, keeping it safe but convenient. 
- **`OS` and `Shutil`**: We can these Python libraries to manipulate our file structure, to reorganise in a way that is most convenient during processing time. 
- **`to_fp16()`**: We can use this function to convert to half-precision floating point, increasing our training speed. This normally does not reduce our accuracy by a noteable amount and is good while rapidly iterating. 
- **Power of iteration**: By using smaller models and half-precision floating point to gauge the most appropriate settings, data augmentation, and hyperparameters, we could quickly iterate. Then, once the best settings were found, we could finalise and maximise our results on a larger model. In this situation, this wasn't even necessary to score at the top of the leaderboard!
- **Test time augmentation**: A useful boost to our test set predictions, where we take an augmented batch of each test image and take the mode of the predictions made on the batch. 

## Credits
This code is based on code provided by the fastai course, especially a number of Kaggle notebooks accessible through their website: https://www.fast.ai. The FastAI team has provided tools and resources that helped in developing this work. I have adapted the code and content to demonstrate my own learning and to help others!
