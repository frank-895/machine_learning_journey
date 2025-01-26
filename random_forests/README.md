# Random Forests - Spaceship Titanic 🚀🚀🚀

This repository demonstrates the gradual and manual production of a random forest to predict the number of people launched into an alternate dimension in a futuristic Titanic disaster on an interstellar space voyage. See the link to the Kaggle competition here: [Spaceship Titanic](https://www.kaggle.com/competitions/spaceship-titanic/overview). 

## Overview

**Task**: Predict the number of people launched into an alternate dimension during the interstellar disaster. 
**Data**: Data was provided in two datasets for training and testing. The testing dataset (containing no labels) was used to evaluate the position on the Kaggle leaderboard. The training dataset contained information about each passenger such as `HomePlanet`, `Destination` and `Age`. 

### Data Cleaning and Feature Engineering
Using Pandas the data was cleaned of `NaN` values and features were engineering to be continuous or categorical. The categorical variables were encoded to be used in binary splits. The training data was split into train and validation sets. 

### Binary Splits
We started by creating binary splits, to understand the fundamentals behind decision trees and by extension, random forests. The binary split produced a MAE of 0.73 when used on the validation data. 

### Decision Trees
Now that we understood binary splits, we could create a decision tree. We visualised the decision tree using `graphviz` and used `scikit-learn` to produce a detailed model. Our decision tree had a MAE of 0.22, a drastic improvement compared to the binary split. **When submitted to Kaggle our prediction had an accuracy of 0.784, scoring in the top 75% on the leaderboard.**

### Random Forests
Our final model was a random forest, an **ensemble** of uncorrelated decision trees. We built the random forest manually first, then using `scitkit-learn`. **Our final MAE was 0.18, with an accuracy on Kaggle of 0.797 putting our prediction in the top 35%!** We used the random forest to plot the importance of features, giving valuable insights for future deep learning approached. 

## Results

The final accuracy on the test data was 0.797, **scoring in the top 35% of predictions** submitted to the Kaggle competition. 

## Key Learnings

This project was not intended to aim for the highest possible score on Kaggle, but to demonstrate how random forests work and their benefits. Scoring in the top 35% of the Kaggle leaderboard shows the power of such as simple model. 

- We learnt about the relationship between binary splits, decision trees and random forests. We understand how random forests work and how to easily create them.
- We strengthened our skills working with complex dataframes and feature engineering with `Pandas`. 
- We learnt that if we are working with a dataset that had thousands of features, random forests are extremely useful in quickly sorting through the data to find the most important variables. Then, efforts can be focused on collecting, analysing and feature engineering with the most important predictors. This also allows us to save time if we are producing a deep learning model, as we can immediately discard variables, reducing training time.
- We learnt that random forests/binary splits/decision trees can be fantastic benchmark models. You may find that these models provide all the accuracy you need, and if not, they can help you sort through the features to make deep learning more efficient!
- We learnt that random forests are not complicated and very hard to mess up! Unlike other regression tasks or deep learning, it is very hard to overfit! You don't have to worry about normalizations and non-linear transformations. This makes it a powerful and quick model to try out before moving to something more advanced.

## Credits
This code is based on code provided by the fastai course, especially a number of Kaggle notebooks accessible through their website: https://www.fast.ai. The FastAI team has provided tools and resources that helped in developing this work. I have adapted the code and content to demonstrate my own learning and to help others!
