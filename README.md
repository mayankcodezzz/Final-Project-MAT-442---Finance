# Final-Project-MAT-442---Finance
Complete statistical analysis

## 1. DVC Setup

- **Add data/ in .gitignore file** : making sure git doesn't track data versions
- **`````dvc init`````** : initialized dvc 
- **`````mkdir s3`````** : Made an virtual database although i have not setup s3 bucket in AWS still for reference created an folder s3
- **`````dvc remote add -d myremoteS3 s3`````** : added s3 to save the data versions we have added this to dvc though it's locally stored not remote
- **`````dvc add data/`````** : Here i have added data folder containing users_data.csv and cards_data.csv which will be tracked by DVC 
- **`````git add . and git commit -m "DVC initiated with data version 1 "````` and `````git push origin main`````** : Now git will keep track of version ID of data 
- **`````dvc commit````` and `````dvc push`````** : Although we have local data storage still we have not yet stored it in s3 to do so we use this command and also add s3 to .gitignore

## 2. Data Preprocessing 

- **Removing card_on_dark_web column** : Since All values of column is NO
- **Updating columns with $ sign before numbers** : making sure numeric values are taken as floating values not string.
-- **Updating account opening date** : Account Opening date is of type string we converted it to datetime
-- **Finally All changes saved in data folder inside cards and users csv file**
