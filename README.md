# Getting And Cleaning Data - Peer Graded Assignment

This repo is created by **Mark Joseph Tigno** for the project submission of the course Getting and Cleaning Data.

## Dataset
[Human Activity Recognition Using Smartphones](http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones)

## Files
- `CodeBook.md` - contains all the descriptions of the variables, data, and transformations I used to clean up the data.
- `run_analysis.R` - R code that executes data preparation and followed the 5 steps described in the course project
    - Merging the training and test sets to create one data set.
    - Extracting only the measurements of mean and standard deviation for each measurement.
    - It uses descriptive activity names for each data set.
    - Appropriate labels for each activity names.
    - Step 4 dataset creates a second independent tidy data with average of each variable per activity and subject.
- `FinalData.txt` is the exported final data output after all steps are executed.
