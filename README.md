# GDS Projekt
For at reproducere vores resultater, bør libraries under 'Dependencies' sektionen i 'model_trainer.ipynb' og 'data_cleaner.ipynb' være installeret på forhånd. Vi brugte blot 'pip install <library>' til dette.

'data_cleaner.ipynb' bruges til at cleane vores raw data. Resultatet bliver eksporteret som 'data_cleaned_fr' ('fr' for fake/reliable).

'model_trainer.ipynb' bruges til at loade data'en og træne modellen. Vi benytter vores cleanede data 'data_cleaned_fr', som vi splitter, vectorizer og bruger til at træne vores model.
