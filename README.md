# Project - Reproduction Steps
To reproduce our results, the libraries listed in the 'Dependencies' section of `model_trainer.ipynb` and `data_cleaner.ipynb` should be installed beforehand. A `requirements.txt` file has been prepared with only `seaborn`, `imbalanced-learn` and `tqdm` as those libraries will install the rest (depencies). Running `pip install -r requirements` whilst having navigated into the folder in which it lies will ensure all the libraries used are installed.

`data_cleaner.ipynb` is used to clean our raw data. The result is exported as `<size>_data_cleaned_fr.csv` ('fr' for fake/reliable), where the `<size>` can be modified.

`model_trainer.ipynb` is used to load the data and train the model. We have provided our cleaned data `10,000_data_cleaned_fr.csv`, which can be split, vectorized, and used to train and evaluate our model. We have in the same way cleaned data for the 'liar' dataset and our own scraped BBC dataset.

### Alternative execution of `model_trainer.ipynb`
In order to run reproduce our exact results, only the `model_trainer.ipynb` would have to run, using the `10,000_data_cleaned_fr.csv` file which can be found in the folder `fake_news_dataset`.
If you however wish to run our program with the entire 995,000 articles, you can do so by swapping out `"fake_news_dataset/10,000_data_raw.csv"` in the second cell ("Loading the raw data") with the filepath to the `"995,000_rows.csv"`, which we unfortunately cannot upload due to it having a too large size for even LFS on GitHub.


### Alternative execution of `data_exploration.ipynb`
If you want to run our code in `data_exploration.ipynb` with a lighter load, you can apply the following changes: change the file paths to smaller files as the files we use are very large in comprehensive data exploration's can change `"100000_raw.csv"` to `10,000_data_raw.csv`.

In the next code block named **"Fake/Reliable comparrison"**, you can use file `10,000_data_cleaned_fr.csv`, instead of `"data_cleaned_fr_100000.csv"`, then you need to also change the types from *"reliable"* to **1** and *"fake"* to **0** because the 2 kinds of news are represented as integers in the smaller file. To be specific it is in this line `if row['type'] == 'reliable':` where reliable needs to be **1**. And in this line: `elif row['type'] == 'fake':` where fake needs to be changed to **0**.

In the next code block called 'Reduction rate' the following will need to be changed from 
```py
file1 = "100000_raw.csv"
file2 = "data_cleaned_fr_100000.csv"
```
to
```py
file1 = "10,000_raw.csv"
file2 = "10,000_cleaned_fr" 
```
if you want to run on smaller files

Finally, in the code block named **'Data exploration on domains'** you can use 
```py
df = pd.read_csv("10,000_data_cleaned_fr.csv")
```
instead of 
```py
df = pd.read_csv("data_cleaned_fr_100000.csv")
```

and again use 1 and 0 instead of reliable and fake in this part:

### Filter the data for reliable articles
```py
reliable_data = train_data[train_data['type'] == 'reliable']
```

### Filter the data for fake articles
```py
fake_data = train_data[train_data['type'] == 'fake']
```



**The rest of the notebooks are used to visualize data and get useful insight.**



# Program execution order
1. `data_cleaner.ipynb`
2. `data_exploration.ipynb`
3. `liar.ipynb`
4. `model_trainer.ipynb`