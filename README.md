# GDS Projekt
To reproduce our results, the libraries listed in the 'Dependencies' section of `model_trainer.ipynb` and `data_cleaner.ipynb` should be installed beforehand. We simply used `pip install <library>` for this.

`data_cleaner.ipynb` is used to clean our raw data. The result is exported as `data_cleaned_fr_<size>` ('fr' for fake/reliable).

`model_trainer.ipynb` is used to load the data and train the model. We use our cleaned data `data_cleaned_fr_100000`, which we split, vectorized, and used to train and evaluate our model.