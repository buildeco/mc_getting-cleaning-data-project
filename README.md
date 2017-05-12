# GETTING AND CLEANING DATA PROJECT

# Michael Crawley, MBA, PMP, M.ED. - Learning and Technology

Repository for the submission of the Johns Hopkins University, "Getting and Cleaning Data" course project.

### Overview
In this project, I provide a demonstration of collecting and cleaning the tidy data set. I then do data analysis using the cleansed tidy data.

The following link empowers you to view a full description of the data used in this project 
[The UCI Machine Learning Repository](http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones)

[The source data for this project can be found here.](https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip)

### Repository Composition
1. CodeBook.md: details information about raw as well as tidy data sets as well as tranformation intricacies.
2. LICENSE: Code and Text license terms.
3. README.md: file you are currently viewing.
4. run_analysis.R: the R script which performs the transformation from the raw data set to the tidy one.

### Human Activity Recognition Using Smartphones Dataset : tidy data set creation process
Merge the test and train sets; pull the activity labels and subject identifiers in order to create a soley integrated data set. 
Translate identifiers into human-readable names, retaining the standard deviation and the mean variables.  Summmarize the retained variables via generation of each subject-activity pair mean.  [Wickman] (http://vita.had.co.nz/papers/tidy-data.pdf) wide-formatted data; consits of a single row for each subject-activity pairing along with a single column for each measurement.

The tidyMeans.txt file contains the final data set.  Via read.table("tidyMeans.txt", header = TRUE), this tidyMeans.txt file may be read into R. CodeBook.md contains a detailed description of the variables. Mean{timeOrFreq}{measurement}{meanOrStd}{XYZ} represents the basic naming convention.

Time or Frequency are represented as timeOrFreq.  The aforementioned is an indication of whether the measurement comes from either the time or frequency domain, measurement is one of the original measurement features, meanOrStd is either Mean or StdDev: providing an indication as to whether the measurement represented either a mean or standard deviation variable; XYZ represents X, Y, or Z, this is an indication of  the axis along which the measurement was taken or could also be nothing as is the case for magnitude measurements.

### steps towards getting tidy data
1. clone this repository: git clone git@github.com:maurotrb/getting-cleaning-data-2014-project.git.
2. download compressed raw data.
3. unzip raw data and copy the directory UCI HAR Dataset to the cloned repository root directory.
4. open a R console and set the working directory to the repository root (use setwd()).
5. source run_analisys.R script (it requires the plyr package): source('run_analysis.R')

 The file sensor_avg_by_act_sub.txt with the tidy data set is located in the repository root directory.

### Project Summary
The following description summarizes instructions for this project.

You should create one R script called run_analysis.R that does the following. 
1. Merges the training and the test sets to create one data set.
2. Extracts only the measurements on the mean and standard deviation for each measurement. 
3. Uses descriptive activity names to name the activities in the data set
4. Appropriately labels the data set with descriptive activity names.  
5. Creates a second, independent tidy data set with the average of each variable for each activity and each subject. 

### Additional Information
The CodeBook.MD file provides you with additional details about the variables, data and transformations used in this project.

