# Processed UCI Human Activity Recognition Using Smartphones Dataset

This data comes from the UCI Human Activity Recognition Using Smartphones 
Dataset. The dataset is the result of an experiment by Jorge L. Reyes-Ortiz, 
Davide Anguita, Alessandro Ghio and Luca Oneto, involving the recording of 
accelerometer and gyroscope data from smartphones attached to the waists of 
participants as they performed different activities.

## Included Files

### Information

`README.md` (this file) contains information on the files in this repository

`CodeBook.md` contains information on the variables in the tidy dataset 
`tidy_data.txt` produced by `run_analysis.R`.  

### Processing Scripts

`run_analysis.R` is the complete R script which performs the following steps:  
* Downloads the zipped dataset and extracts it (if not already present), 
creating the `UCI HAR Dataset` directory  
* Concatenates the data from the files `sample_train`, `y_train` and `X_train`, 
found  under `UCI HAR Dataset/train`, column-wise, and does the same for the 
files `sample_test`, `y_test` and `X_test`, found under `UCI HAR Dataset/test`   
* Concatenates the resulting training and test sets row-wise to create a 
complete dataset  
* Discards variables which are not the `mean()` or `sd()` of a signal  
* Replaces the integer activity indentifier with descriptive names  
* Labels the columns with descriptive variable names  
* Summarizes the dataset by providing the mean of each measurement variable for 
every unique subject-activity combination  
* Saves this tidy summary to `tidy_data.txt`  

This script depends on the `dplyr` package. The analysis was performed
using R version 3.5.0 and dplyr version 0.7.5.  

### Datasets

`tidy_data.txt` is the dataset produced by running `run_analysis.R`  
