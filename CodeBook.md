# John Hopkins University "GETTING AND CLEANING DATA" Course PROJECT

## Michael Crawley, MBA, PMP, M.ED. - Learning and Technology
 
 ### Data Source
 [The UCI Machine Learning Repository](http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones) details a full description of the data used that this project uses. 
[The source data for this project can be found here.](https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip)
 +
 ### Subjects, Activities and other data set details
 +Subject: the integer subject ID (volunteers within specified age range).
 +Activity: the string (each volunteer) activity (6) name: Walking, Walking Upstairs, Walking Downstairs, Sitting, Standing, and Laying.
 +Wearble: smartphone (on wrist).
 +Dataset: randomly partitioned.
 + 
 ### Variables
+ x_train, y_train, x_test, y_test, subject_train and subject_test contain the data from the downloaded files.
+ x_data, y_data and subject_data merge the previous datasets to further analysis.
+ features contains the correct names for the x_data dataset, which are applied to the column names stored in mean_and_std_features, a numeric vector used to extract the desired data.
+ A similar approach is taken with activity names through the activities variable.
+ all_data merges x_data, y_data and subject_data in a big dataset.
+ Finally, averages_data contains the relevant averages which will be later stored in a .txt file. ddply() from the plyr package is used to apply colMeans() and ease the development.

 ### 1. Merges the training and the test sets to create one data set (read the following into tables):
 +- features.txt, activity_labels.txt, subject_train.txt, x_train.txt, y_train.txt, subject_test.txt, x_test.txt, y_test.txt
 +
 ## 2. Extracts only the measurements on the mean and standard deviation for each measurement. 
 Time domain body acceleration mean along X, Y, and Z: ; MeanTimeBodyAccMeanX, MeanTimeBodyAccMeanY, MeanTimeBodyAccMeanZ, Time domain body acceleration standard deviation along X, Y, and Z:
MeanTimeBodyAccStdDevX, MeanTimeBodyAccStdDevY, MeanTimeBodyAccStdDevZ, Time domain gravity acceleration mean along X, Y, and Z:, MeanTimeGravityAccMeanX, 
MeanTimeGravityAccMeanY, MeanTimeGravityAccMeanZ, Time domain gravity acceleration standard deviation along X, Y, and Z:, MeanTimeGravityAccStdDevX, 
MeanTimeGravityAccStdDevY, MeanTimeGravityAccStdDevZ, Time domain body jerk mean along X, Y, and Z:, MeanTimeBodyAccJerkMeanX, MeanTimeBodyAccJerkMeanY, 
MeanTimeBodyAccJerkMeanZ, Time domain body jerk standard deviation along X, Y, and Z:, MeanTimeBodyAccJerkStdDevX, MeanTimeBodyAccJerkStdDevY, 
MeanTimeBodyAccJerkStdDevZ, Time domain gyroscope mean along X, Y, and Z:, MeanTimeBodyGyroMeanX, MeanTimeBodyGyroMeanY, MeanTimeBodyGyroMeanZ,
Time domain gyroscope standard deviation along X, Y, and Z, MeanTimeBodyGyroStdDevX, MeanTimeBodyGyroStdDevY, MeanTimeBodyGyroStdDevZ, Time domain gyroscope jerk mean along X, Y, and Z:,
MeanTimeBodyGyroJerkMeanX, MeanTimeBodyGyroJerkMeanY, MeanTimeBodyGyroJerkMeanZ, Time domain gyroscope jerk standard deviation along X, Y, and Z:, MeanTimeBodyGyroJerkStdDevX,
MeanTimeBodyGyroJerkStdDevY, MeanTimeBodyGyroJerkStdDevZ; Time domain body acceleration magnitude mean: MeanTimeBodyAccMagMean; Time domain body acceleration magnitude standard deviation: MeanTimeBodyAccMagStdDev; Time domain gravity acceleration magnitude mean: MeanTimeGravityAccMagMean; Time domain gravity acceleration magnitude standard deviation: MeanTimeGravityAccMagStdDev; Time domain body jerk magnitude mean: MeanTimeBodyAccJerkMagMean; Time domain body jerk magnitude standard deviation: MeanTimeBodyAccJerkMagStdDev; Time domain gyroscope magnitude mean: MeanTimeBodyGyroMagMean; Time domain gyroscope magnitude standard deviation: MeanTimeBodyGyroMagStdDev; Time domain gyroscope jerk magnitude mean: MeanTimeBodyGyroJerkMagMean; Time domain gyroscope jerk magnitude standard deviation: MeanTimeBodyGyroJerkMagStdDev; Frequency domain body acceleration mean along X, Y, and Z: MeanFrequencyBodyAccMeanX, MeanFrequencyBodyAccMeanY, MeanFrequencyBodyAccMeanZ; Frequency domain body acceleration standard deviation along X, Y, and Z: MeanFrequencyBodyAccStdDevX, MeanFrequencyBodyAccStdDevY, MeanFrequencyBodyAccStdDevZ; Frequency domain body jerk mean along X, Y, and Z:MeanFrequencyBodyAccJerkMeanX, MeanFrequencyBodyAccJerkMeanY, MeanFrequencyBodyAccJerkMeanZ; Frequency domain body jerk standard deviation along X, Y, and Z: MeanFrequencyBodyAccJerkStdDevX, MeanFrequencyBodyAccJerkStdDevY, MeanFrequencyBodyAccJerkStdDevZ; Frequency domain gyroscope mean along X, Y, and Z: MeanFrequencyBodyGyroMeanX, MeanFrequencyBodyGyroMeanY, MeanFrequencyBodyGyroMeanZ; Frequency domain gyroscope standard deviation along X, Y, and Z: MeanFrequencyBodyGyroStdDevX, MeanFrequencyBodyGyroStdDevY, MeanFrequencyBodyGyroStdDevZ; Frequency domain body acceleration magnitude mean:MeanFrequencyBodyAccMagMean; Frequency domain body acceleration magnitude standard deviation: MeanFrequencyBodyAccMagStdDev; Frequency domain body jerk magnitude mean: MeanFrequencyBodyAccJerkMagMean; Frequency domain body jerk magnitude standard deviation: MeanFrequencyBodyAccJerkMagStdDev; Frequency domain gyroscope magnitude mean:MeanFrequencyBodyGyroMagMean; Frequency domain gyroscope magnitude standard deviation:MeanFrequencyBodyGyroMagStdDev; Frequency domain gyroscope jerk magnitude mean:MeanFrequencyBodyGyroJerkMagMean; Frequency domain gyroscope jerk magnitude standard deviation:MeanFrequencyBodyGyroJerkMagStdDev, Contact GitHub API Training Shop Blog 
 +
 ## 3. Uses descriptive activity names to name the activities in the data set
 +
 ## 4. Appropriately labels the data set with descriptive variable names.
 +
 ## 5. From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.
