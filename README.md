# README.md

### Files in this repository
* README.md  - which you are currently reading
* run_analysis.R  - the R code for the course project
* tidy_data.txt  - the tidy data set created using run_analysis.R
* CODEBOOK.md  - describes data, variables, and any transformations


The project is the following:


The purpose of this project is to demonstrate your ability to collect, work with, and clean a data set. The goal is to prepare tidy data that can be used for later analysis. You will be graded by your peers on a series of yes/no questions related to the project. You will be required to submit: 1) a tidy data set as described below, 2) a link to a Github repository with your script for performing the analysis, and 3) a code book that describes the variables, the data, and any transformations or work that you performed to clean up the data called CodeBook.md. You should also include a README.md in the repo with your scripts. This repo explains how all of the scripts work and how they are connected. 

Here are the data for the project
https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip


## A Guide to the R code

>The project description states ...
>You should create one R script called run_analysis.R that does the following. 

1. Merge the training and the test sets to create one data set.
2. Extract only the measurements on the mean and standard deviation for each measurement. 
3. Use descriptive activity names to name the activities in the data set
4. Appropriately label the data set with descriptive variable names. 
5. From the data set in step 4, create a second, independent tidy data set with the average of each variable for each activity and each subject.


####Load required package
library(dplyr)

#### Set working directory
setwd("C:/Users/XXXXXXXX/Documents/UCI HAR Dataset")

#### Read the data from the various files

##### Names of column variables and labels for linking the training and testing files
1. activity_labels <- read.table('./activity_labels.txt', header = FALSE) 
2. features <- read.table('./features.txt', header = FALSE) 

##### Read data from training files
1. subjectTrain <- read.table('./train/subject_train.txt', header = FALSE)
2. xTrain <- read.table('./train/X_train.txt', header = FALSE) 
3. yTrain <- read.table('./train/y_train.txt', header = FALSE)

##### Read data from testing files
1. subjectTest <- read.table('./test/subject_test.txt', header = FALSE)
2. xTest <- read.table('./test/X_test.txt', header = FALSE) 
3. yTest <- read.table('./test/y_test.txt', header = FALSE)

#### Add column labels to the above data sets

1. colnames(activity_labels) = c("activityId", "activityName")
2. colnames(subjectTrain) = "subjectId"
3. colnames(xTrain) = features[,2]
4. colnames(yTrain) = "activityId"
5. colnames(subjectTest) = "subjectId"
6. colnames(xTest) = features[,2]
7. colnames(yTest) = "activityId"

