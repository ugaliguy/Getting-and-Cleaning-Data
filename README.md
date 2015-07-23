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

 You should create one R script called run_analysis.R that does the following. 

    Merges the training and the test sets to create one data set.
    Extracts only the measurements on the mean and standard deviation for each measurement. 
    Uses descriptive activity names to name the activities in the data set
    Appropriately labels the data set with descriptive variable names. 

    From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.

Good luck!



## A Guide to the R code

####Load required package
library(dplyr)

#### Set working directory
setwd("C:/Users/XXXXXXXX/Documents/UCI HAR Dataset")

#### Read the data from the various files
1. Names of column variables and labels for linking the training and testing files

activity_labels <- read.table('./activity_labels.txt', header = FALSE) ..
features <- read.table('./features.txt', header = FALSE) ..

2. Read data from training files

subjectTrain <- read.table('./train/subject_train.txt', header = FALSE)
xTrain <- read.table('./train/X_train.txt', header = FALSE) 
yTrain <- read.table('./train/y_train.txt', header = FALSE)

3. Read data from testing files

subjectTest <- read.table('./test/subject_test.txt', header = FALSE)
xTest <- read.table('./test/X_test.txt', header = FALSE) 
yTest <- read.table('./test/y_test.txt', header = FALSE)

