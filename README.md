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

- **Updating account opening date** : Account Opening date is of type string we converted it to datetime

- **Finally All changes saved in data folder inside cards and users csv file**

- **`````dvc commit````` and `````dvc push`````** : update the changes in dvc for new data

## 3. Feature Engineering

- **1. Added a new column containing categorical variable - Retired, Not Retired**

- **2. Divided Age into four Groups and Created a new column age_group containing 4 categorical variables**
### **Although there is no such direct analysis possible this variable is used to detect for fruad detection likelihood still we will consider it for the analysis**

- **3. Flag if PIN Change is Due**

- **4. Since total debt is a very perspective dependent variable suppose - Person A having Yearly Income $500k for him having an debt of $20k is not an big issue than for a Person B having Yearly Income $20k having an debt of $10k though it seems that Person A has More debt than Person B, if we take the Debt_to_income ratio we see the actuall significance for Person A - 0.04(4% of income) and for Person B - 0.5(50% of income)**

- **Merging Both Tables**

- **Finally All changes saved in data folder and a new csv file is created merging both csv file**

- **`````dvc commit````` and `````dvc push`````** : update the changes in dvc for new data