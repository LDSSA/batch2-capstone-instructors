## Predicting vehicle crash survival

In this dataset, you are given a set of features that are known about a scenario for a particular person in the moments
before a car crash occurs. Imagine that you are watching a video of a car crash and you pause it a few seconds before
the crash actually occurs and your job is to look at all people in the immediate vicinity and predict which of them will
die by extracting the features found in `X_train`

This is a very difficult predicition task using only data so don't expect your scores to be super high.

## The dataset

- Each row in the dataset corresponds to a single person, involved in a car crash.
- The data column names and values are supposed to be quite explicit - there is no data dictionary to be supplied.
- The entries in `y_train` are: `1=died`, and `0=survived`
    - This means that a prediction of `1` is absolute certainty that a person will die.

## Exploring the dataset and modeling

You are expected to explore and understand the dataset, and train a predictive model that outputs the *probability of death* of a person involved in a car crash.

You have already taken a look at many datasets. However, good practices are always good to remember:
* Take a good overview of the dataset before anything else - numerical variables, categorical variables, anomalies, outliers, missing values, etc. Basically, perform an Exploratory Data Analysis (EDA).  
* Quickly create a baseline model - this will be your starting point from where you will improve (or not!).  
* Think beyond what you have in your hands - you cannot fully guarantee that the data your model will see in production has exactly the same characteristics of the training dataset. Plan for failure.  
* Pipelines are life savers. You probably remember them. You generally have one initial notebook so messy with EDA, that you need to create one with the decisions (steps) you would like to have in your pipeline.  
* Don't overcomplicate your final solution - the more complicated it is, the more problems it might have in production.  

## Deploying and testing

Follow the guidelines for [deploying a model on heroku](https://github.com/LDSSA/heroku-model-deploy) and use the
`test-server.py` script to test your deployment. What you'll want to do is start your server and then run 
`python test-server.py`. There are a few options to use with it. Here are a few examples of how to use the script:

```bash
# This assumes that you have a file called X_train.csv in the data directory
# and you have started your server on your localhost because you are developing it
python test-server.py "data/X_train.csv" "http://127.0.0.1:5000/"

# This is the same scenario but with 100 observations instead of the default 10
python test-server.py "final_datasets/X_train.csv" "http://127.0.0.1:5000/" -n 100

# This will use a different random state to select the observations. You will use
# this after you have one set of observations working well and you want to test
# with a different set.
python test-server.py "final_datasets/X_train.csv" "http://127.0.0.1:5000/" -r 45

# now you've deployed it to heroku!
python test-server.py "final_datasets/X_train.csv" "https://deployed-model.herokuapp.com"
```

### Remember!

You only have 10K rows on the free tier of heroku so after testing, you will want to clear out your database to make
sure that you aren't taking up any precious space for when we actually start the simulator!
