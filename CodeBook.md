The `run_analysis.R` script performs the data preparation and then followed by the 5 steps required as described in the course project's defintion.

1. **Download dataset**
    - Download dataset and extract the folder *UCI HAR Dataset*

2. **Assign variables for each data**
    - `features <- features.txt`
    - `activities <- activity_labels.txt`
    - `subject_test <- test/subject_test.txt`
    - `x_test <- test/X_test.txt`
    - `y_test <- test/y_test.txt`
    - `subject_train <- test/subject_train.txt`
    - `x_train <- test/X_train.txt`
    - `y_train <- test/y_train.txt`

3. **Merge the training and tests to a one data set**
    - `X` is merged by `x_train` and `x_test` using `rbind()`
    - `Y` is merged by `y_train` and `y_test` using `rbind()`
    - `Subject` is merged by `subject_train` and `subject_test` using `rbind()`
    - `Merged_Data` is merged by `Subject`, `X`, and `Y` using `cbind()`

4. **Extract only the mean and sd for each measurement**
    - Assign `TidyData` by subsetting `Merge_Data` by selecting only `subject`, `code`, and measurements of `mean` and `std`.

5. **Describe activity names in the data set**
    - All numbers in `code` column of `TidyData` is replaced with coressponding activity from the 2nd coloumn of the `activties` variable.

6. **Labels of the dataset with descriptive names**
    - `code` from `TidyData` to `activites`
    - `Acc` to `Accelerometer`
    - `Gyro` to `Gyroscope`
    - `BodyBody` to `Body`
    - `Mag` to `Magnitude`
    - `f` to `Frequency`
    - `t` to `Time`

7. **Export the final data**
    - Sumarize `TidyData` by taking the means of each variable for each activity and each subject, after groupped by subject and activity. Export the file into `FinalData.txt`.