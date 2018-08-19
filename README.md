# batch2-capstone-instructors

Please note that running the notebook isn't possible until they merge the fix for categorical_encoders.OrdinalEncoder referenced [in this issue](https://github.com/scikit-learn-contrib/categorical-encoding/issues/100) is fixed. If you do want to run it, you'll have to make the change mentioned in the issue yourself after pip installing

## The notebooks and datasets

The `final_datasets` directory contains the dataset [referenced in the spec](https://github.com/LDSSA/batch2-capstone#the-dataset)

All of the interesting stuff is in the `benchmark-and-obfuscate.ipynb` notebooks. This is where we create and run benchmarks on the datasets and then write them out to `final_datasets`. The final dataset that will be used is only looking at the survival rate (died or didn't die) using a subset of the dataset which is only features that could have been known prior to the accident. This dataset looks very difficult to get a good roc_auc score on because the signal is quite low and the feature that contains the most (age) is very aggressively su setted for the training set (see notebook for details)

The other notebook is just for processing the original dataset [from here](http://sci2s.ugr.es/keel/dataset.php?cod=191)

## The story and the assignment

Check out `brief.md` for the actual assignment. Note that there will be a bit of work involved in taking the relevant
parts of this repo and moving them to the capstone project repo.
