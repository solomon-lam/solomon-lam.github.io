---
layout: post
categories: fastai
---

## Data cleaning


The key point in the second lecture is that one can first train the model and then do the data cleaning. However, the fastai data cleaning widget does not work on Kaggle. I do not manage to make this work so as other people online.

As I increase the number of images input, the data is not always correct because there are not that many good clouds images online. Initially I tried to put all 10 common cloud types in the classifier but then it became too slow to train (30 minutes per epoch). Then I focused on only 4 types because I think they are more likely to be misidentified (5 minutes per epoch). In this exercise, the difficult classification is between cumulus and cumulonimbus. To a large extent, I think this is a consequeunce of poor input data quality. As I can see the issues from the prediction/ actual/ loss/ probability output from the validation data. 

Unforunately, as the data clean part has programming issue. I do not deploy another classifier here. In principle, the data cleaning would remove incorrectly labelled images or unreasonable images (e.g. powerpoint slides). But since this does not work out, I reduced the number of image inputs to ensure the quality of image for training of the 4-cloud type classifier. 
