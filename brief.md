## Predicting vehicle crash survival

In this dataset, you are given a set of features that are known about a scenario for a particular person in the moments
before a car crash occurs. Imagine that you are watching a video of a car crash and you pause it a few seconds before
the crash actually occurs and your job is to look at all people in the immediate vicinity and predict which of them will
die by extracting the features found in `X_train`

This is a very difficult predicition task using only data so don't expect your scores to be super high.

## The dataset

- Each row in the dataset corresponds to a single person.
- The data column names and values are supposed to be quite explicit - there is no data dictionary to be supplied
- The entries in `y_train` are: `1=died`, and `0=survived`
    - This means that a prediction of `1` is absolute certainty they will die

## Exploring the dataset

You are expected to explore and understand the dataset, train a predictive model that outputs predictions of survival.
Use the following guidelines: TODO - fill in from Hugo

## Deploying the model

Follow the guidelines for [deploying a model on heroku](https://github.com/LDSSA/heroku-model-deploy) and use the
following script to test your deployment: TODO - fill in after example deployment is made

