# Gradient Accumulation and Ensembling Deep Learning Models

In this notebook, I made a submission to the following Kaggle competition: [Natural Language Processing with Disaster Tweets](https://www.kaggle.com/competitions/nlp-getting-started/data).

The goal was to use **natural language processing** to predict if a tweet is talking about a real natural disaster or not. If `target = 1`, the tweet is talking about a real disaster. If `target = 0` the tweet is **not** talking about a real disaster.

## Overview
- **Data Processing**: Extracted data, combining the features into a single input string to be **tokenized** and **numericalized**.
- **Gradient accumulation**: Introduced the concept of gradient accumulation, which was critical in using Colab's **free** GPU to train larger pretrained NLP models.
- **Trained the models**: Each model was trained and saved using Hugging Face's `Trainer` API. We used Python's **garbage collector** and PyTorch's `empty_cache()` to optimise GPU usage.
- **Ensembling**: The predictions on the test set were made for each of the four models and combined using tensors (which are optimised for matrices). Predictions were averaged to produce our final results, which were submitted to Kaggle. 

## Results
UPDATE HERE

## Credit
This code is based on code provided by the fastai course, especially a number of Kaggle notebooks accessible through their website: https://www.fast.ai. The FastAI team has provided tools and resources that helped in developing this work. I have adapted the code and content to demonstrate my own learning and to help others!
