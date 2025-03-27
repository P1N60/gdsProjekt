# GDS Projekt
To reproduce our results, the libraries listed in the 'Dependencies' section of `model_trainer.ipynb` and `data_cleaner.ipynb` should be installed beforehand. A `requirements.txt` file has been prepared with only `seaborn`, `imbalanced-learn` and `tqdm` as those libraries will install the rest (depencies). Running `pip install -r requirements` whilst having navigated into the folder in which it lies will ensure all the libraries used are installed.

`data_cleaner.ipynb` is used to clean our raw data. The result is exported as `data_cleaned_fr_<size>` ('fr' for fake/reliable).

`model_trainer.ipynb` is used to load the data and train the model. We use our cleaned data `data_cleaned_fr_100000`, which we split, vectorized, and used to train and evaluate our model.
