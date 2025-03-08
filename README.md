# Final-Project-MAT-442---Finance
Complete statistical analysis

## 1. DVC Setup
- **Add data/ in .gitignore file** : making sure git doesn't track data versions
- **dvc init** : initialized dvc 
- **mkdir s3** : Made an virtual database although i have not setup s3 bucket in AMW still for reference created an folder s3
- **dvc remote add -d myremoteS3 s3** : added s3 to save the data versions we have added this to dvc though it's locally stored not remote
- **dvc add data/** : Here i have added data folder containing users_data.csv and cards_data.csv which will be tracked by DVC 
- **git add . and git commit -m "DVC initiated with data version 1 " and git push origin main** : Now git will keep track of version ID of data 

## 2. 