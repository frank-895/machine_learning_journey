# Gradient Boosting Machines - Forecasting Sticker Sales

After learning about **ensembles of decision trees** as an approach to modelling tabular data, I've decided to have another shot at the [Forecasting Sticker Sales](https://www.kaggle.com/competitions/playground-series-s5e1) Kaggle competition.

While I initially approached the problem with **deep learning**, I wanted to use a different approach that is sometimes better for structured data.

In my last notebook I covered **random forests** which is one approach of ensembling decision trees. However, there is another area of ensembling I wish to learn more about, called **gradient boosting machines (GBMs)**.

As such, this notebook is primarily intended as a way of understanding GBMs. However, in the process, I discuss ensembles of decision trees, feature importance, partial dependence and some general limitations when working with this type of modelling process. The information contained in this notebook is my personal learnings from the [FastAI textbook](https://course.fast.ai/Resources/book.html) chapter 9.

## Overview

- **Data engineering**: I used Pandas to read in training data, perform *feature engineering* and create a `TabularPandas` with training and validation sets.
- **Random forest**: Since random forests are easier to implement, not as prone to overfitting and faster to train, I started with this architecture. 
- **Gradient boosting machine**: Using Scikit-learn, I built a GBM and used it to make predictions on the test set, which was submitted to Kaggle. We also calculated the *confidence* of our predictions using the standard deviation across multiple *estimators*.
- **Feature importance**: I calculated feature importance and removed a large number of unhelpful features.
- **Partial dependence**: I created a partial dependence plot and understood how this is created and why.
- **Waterfall chart**: I created a waterfall chart that depicts what factors are important in making a prediction for a particular row of data. This is particularly useful when using a model in production.
- **Limiations and considerations**: I discussed the possibility of *data leakage* and the limitations of ensembles of decision trees in *extrapolation*. I explained the *domain shift*.
  
## Results
The random forest scored a MAPE on the test set of 0.162 while the GBM score 0.164 on the test set. This was not an improvement on the deep learning model, which was highly optimised using more advanced techniques including *pseudo-labelling*.

## Key Learnings
- How to use the `TabularPandas` class from FastAI.
- How GBMs work compared to random forests.
- How ensembles of decisions trees can predict continuous variables for regression tasks.
- When to use GBMs vs random forests.
- How to create GBMs using Scikit-learn.
- How to visualise feature importance.
- How to build a partial dependence plot and understand it.
- How to create a waterfall chart for a particular row of data.
- What data leakage is.
- Why ensembles of decision trees are limited in their ability to extrapolate.
- What domain shift is.

## Credits

This code is based on code provided by the fastai course, especially a number of Kaggle notebooks accessible through their website: https://www.fast.ai. The FastAI team has provided tools and resources that helped in developing this work. I have adapted the code and content to demonstrate my own learning and to help others!
