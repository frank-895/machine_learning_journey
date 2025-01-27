# Predict Global Sticker Sales

As I continue my machine learning (ML) journey, it seemed like I had accumulated sufficient knowledge to participate in a Kaggle competition. As such, I decided to produce a model to submit to this competition: [Forecasting Sticker Sales](https://www.kaggle.com/competitions/playground-series-s5e1/overview).

## Overview

In this Kaggle competition, the goal is to predict the number of sticker sales based on training data which includes past sticker sales as well as:
- `date`
- `country`
- `store`
- `product`

This competition is aimed to be approachable, for people to practice their ML skills. But, it still provides real-world data and hidden test sets. I'm excited to demonstrate my ML knowledge through this challenge!

So far, I've learnt deep learning as part of my machine learning journey, so this is the approach I took when solving the problem. However, it would also be worth attempting an **ensemble of decision trees** based approach, given we are working with structured data (i.e., tabular data).

## Process
- **Data extraction and feature engineering**: Used `Pandas` to clean the data `fastai`'s `add_datepart()` function to perform feature engineering on the date column.
- **Defined metric**: Created a custom metric for the Kaggle competition called **MAPE** or **Mean Absolute Percentage Error**.
- **Created a validation set**: Aimed for meaningful validation set, choosing a subset of the later sales instead of random values.
- **Fit the model**: Used `fastai`'s `tabular_learner` and advanced features to select the best learning rate.
- **Pseudo-labelling**: Independently researched pseudo-labelling to use the full dataset, including unlabelled training data. Filtered pseudo-labelled data using **confidence** and a **threshold** value. Retrained the model to produce the best results.

## Results
After making our Kaggle submission our score put us in the top 27% of Kaggle submissions, which is a terrific effort for our first competition. Our MAPE was 0.093.

## Key Learnings
- **Pseudo-labelling**: I was completely unfamiliar with this machine learning technique prior to this project.
- **add_datepart**: I was able to learn some amazing state-of-the-art feature engineering tools provided by fastai.
- **Indendent Project**: It was fantastic working on an independent project on a completely new dataset without any assistance. This project has given me confidence in my skills and enthusiasm to keep learning!
