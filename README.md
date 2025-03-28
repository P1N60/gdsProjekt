# Project - Reproduction Steps
To reproduce our results, the libraries listed in the 'Dependencies' section of `model_trainer.ipynb` and `data_cleaner.ipynb` should be installed beforehand. A `requirements.txt` file has been prepared with only `seaborn`, `imbalanced-learn` and `tqdm` as those libraries will install the rest (depencies). Running `pip install -r requirements` whilst having navigated into the folder in which it lies will ensure all the libraries used are installed.

`data_cleaner.ipynb` is used to clean our raw data. The result is exported as `<size>_data_cleaned_fr.csv` ('fr' for fake/reliable), where the `<size>` can be modified.

`model_trainer.ipynb` is used to load the data and train the model. We have provided our cleaned data `10,000_data_cleaned_fr.csv`, which can be split, vectorized, and used to train and evaluate our model. We have in the same way cleaned data for the 'liar' dataset and our own scraped BBC dataset.

In order to run reproduce our exact results, only the `model_trainer.ipynb` would have to run, using the `10,000_data_cleaned_fr.csv` file which can be found in the folder `fake_news_dataset`.
If you however wish to run our program with the entire 995,000 articles, you can do so by swapping out `"fake_news_dataset/10,000_data_raw.csv"` in the second cell ("Loading the raw data") with the filepath to the `"995,000_rows.csv"`, which we unfortunately cannot upload due to it having a too large size for even LFS on GitHub.

The rest of the notebooks are used to visualize data and get useful insight.
