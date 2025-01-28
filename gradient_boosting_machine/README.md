# Gradient Boosting Machines - Forecasting Sticker Sales

After learning about **ensembles of decision trees** as an approach to modelling tabular data, I've decided to have another shot at the [Forecasting Sticker Sales](https://www.kaggle.com/competitions/playground-series-s5e1) Kaggle competition.

While I initially approached the problem with **deep learning**, I wanted to use a different approach that is sometimes better for structured data.

In my last notebook I covered **random forests** which is one approach of ensembling decision trees. However, there is another area of ensembling I wish to learn more about, called **gradient boosting machines (GBMs)**.

## Overview

- **Data engineering**: I used Pandas to read in training data, perform feature engineering and create a `TabularPandas` with training and validation sets.
- **Random forest**: Since random forests are easier to implement, not as prone to overfitting and faster to train, I started with this architecture. 
- **Gradient boosting machine**: Using Scikit-learn, I built a GBM and used it to make predictions on the test set, which was submitted to Kaggle.

## Results
The random forest scored a MAPE on the test set of 0.162 while the GBM score 0.164 on the test set. This was not an improvement on the deep learning model, which was highly optimised using more advanced techniques including pseudo-labelling.

## Key Learnings
- How to use the `TabularPandas` class from FastAI.
- How GBMs work compared to random forests.
- How ensembles of decisions trees can predict continuous variables for regression tasks.
- When to use GBMs vs random forests.
- How to create GBMs using Scikit-learn.

## Credits

This code is based on code provided by the fastai course, especially a number of Kaggle notebooks accessible through their website: https://www.fast.ai. The FastAI team has provided tools and resources that helped in developing this work. I have adapted the code and content to demonstrate my own learning and to help others!
