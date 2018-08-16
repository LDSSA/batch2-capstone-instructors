# batch2-capstone-instructors

Please note that running the notebook isn't possible until they merge the fix for categorical_encoders.OrdinalEncoder referenced [in this issue](https://github.com/scikit-learn-contrib/categorical-encoding/issues/100) is fixed. If you do want to run it, you'll have to make the change mentioned in the issue yourself after pip installing

## The notebooks and dataset

All of the interesting stuff is in the `benchmark-and-obfuscate.ipynb` notebooks. This is where we create and run benchmarks on the dataset [referenced in the spec](https://github.com/LDSSA/batch2-capstone#the-dataset). The final dataset that will be used is only looking at the survival rate (died or didn't die) using a subset of the dataset which is only features that could have been known prior to the accident. This dataset looks very difficult to get a good roc_auc score on because the signal is quite low and the feature that contains the most (age) is very aggressively su setted for the training set (see notebook for details)

The other notebook is just for processing the original dataset [from here](http://sci2s.ugr.es/keel/dataset.php?cod=191)

## The story and the assignment

I would like to preserve the original intention and meaning of the dataset. I think that it is obfuscated enough that we can do this. Plus, it is so aggressively subsetted and obfuscated that even if they were able to find it online, it would be very difficult to translate into something usable in your model.

**IS THIS OKAY???**
