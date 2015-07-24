# CODEBOOK.md

### Data Set Information

 A full description is available at the site where the data was obtained:

<http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones>

The following description is taken from the above site:

"The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data.

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain."

### Attribute Information

For each record in the dataset it is provided:
* Triaxial acceleration from the accelerometer (total acceleration) and the estimated body acceleration.
* Triaxial Angular velocity from the gyroscope.
* A 561-feature vector with time and frequency domain variables.
* Its activity label.
* An identifier of the subject who carried out the experiment. 

### Feature Selection

The features selected for this database come from the accelerometer and gyroscope 3-axial raw signals tAcc-XYZ and tGyro-XYZ. These time domain signals (*prefix 't' to denote time*) were captured at a constant rate of 50 Hz. Then they were filtered using a median filter and a 3rd order low pass Butterworth filter with a corner frequency of 20 Hz to remove noise. Similarly, the acceleration signal was then separated into body and gravity acceleration signals (tBodyAcc-XYZ and tGravityAcc-XYZ) using another low pass Butterworth filter with a corner frequency of 0.3 Hz. 

The body linear acceleration and angular velocity were derived in time to obtain Jerk signals (tBodyAccJerk-XYZ and tBodyGyroJerk-XYZ). Also the magnitude of these three-dimensional signals were calculated using the Euclidean norm (tBodyAccMag, tGravityAccMag, tBodyAccJerkMag, tBodyGyroMag, tBodyGyroJerkMag). 

A Fast Fourier Transform (FFT) was applied to some of these signals producing fBodyAcc-XYZ, fBodyAccJerk-XYZ, fBodyGyro-XYZ, fBodyAccJerkMag, fBodyGyroMag, fBodyGyroJerkMag. (*Note the 'f' to indicate frequency domain signals*). 
These signals were used to estimate variables of the feature vector for each pattern:  
'-XYZ' is used to denote 3-axial signals in the X, Y and Z directions.

* tBodyAcc-XYZ
* tGravityAcc-XYZ
* tBodyAccJerk-XYZ
* tBodyGyro-XYZ
* tBodyGyroJerk-XYZ
* tBodyAccMag
* tGravityAccMag
* tBodyAccJerkMag
* tBodyGyroMag
* tBodyGyroJerkMag
* fBodyAcc-XYZ
* fBodyAccJerk-XYZ
* fBodyGyro-XYZ
* fBodyAccMag
* fBodyBodyAccJerkMag
* fBodyBodyGyroMag
* fBodyBodyGyroJerkMag
 
The variables that were estimated from these signals are:
* mean(): Mean Value
* std(): Standard Deviation
 
We transform the above variable names to more descriptive variable names under the following rules:
* 't' becomes 'time'
* 'f' becomes 'freq' (short for 'frequency')
* 'std()' becomes'StdDev'
* 'mean()' becomes 'MEAN'
* 'BodyBody' becomes'Body'
 
For example, the variable fBodyBodyGyroJerkMag-std() becomes freqBodyGyroJerkMag-StdDev.

### Variable Descriptions

| Variable | Description |
|----------|-------------|
|SubjectId| Subject ID |
|activityName| Activty Name|
|activityId| Activty ID|
|timeBodyAcc-Mean-X| Mean time for acceleration of body for X direction |
|timeBodyAcc-Mean-Y| Mean time for acceleration of body for Y direction |
|timeBodyAcc-Mean-Z| Mean time for acceleration of body for Z direction |
|timeBodyAcc-StdDev-X| Standard deviation of time for acceleration of body for X direction |
|timeBodyAcc-StdDev-Y| Standard deviation of time for acceleration of body for Y direction |
|timeBodyAcc-StdDev-Z| Standard deviation of time for acceleration of body for Z direction |
|timeGravityAcc-Mean-X| Mean time of acceleration of gravity for X direction |
|timeGravityAcc-Mean-Y| Mean time of acceleration of gravity for Y direction |
|timeGravityAcc-Mean-Z| Mean time of acceleration of gravity for Z direction |
|timeGravityAcc-StdDev-X| Standard deviation of time of acceleration of gravity for X direction |
|timeGravityAcc-StdDev-Y| Standard deviation of time of acceleration of gravity for Y direction |
|timeGravityAcc-StdDev-Z| Standard deviation of time of acceleration of gravity for Z direction |
|timeBodyAccJerk-Mean-X| Mean time of body acceleration jerk for X direction |
|timeBodyAccJerk-Mean-Y| Mean time of body acceleration jerk for Y direction |
|timeBodyAccJerk-Mean-Z| Mean time of body acceleration jerk for Z direction |
|timeBodyAccJerk-StdDev-X| Standard deviation of time of body acceleration jerk for X direction |
|timeBodyAccJerk-StdDev-Y| Standard deviation of time of body acceleration jerk for Y direction |
|timeBodyAccJerk-StdDev-Z| Standard deviation of time of body acceleration jerk for Z direction |
|timeBodyGyro-Mean-X| Mean body gyroscopic measurement for X direction |
|timeBodyGyro-Mean-Y| Mean body gyroscopic measurement for Y direction |
|timeBodyGyro-Mean-Z| Mean body gyroscopic measurement for Z direction |
|timeBodyGyro-StdDev-X| Standard deviation of body gyroscopic measurement for X direction |
|timeBodyGyro-StdDev-Y| Standard deviation of body gyroscopic measurement for Y direction |
|timeBodyGyro-StdDev-Z| Standard deviation of body gyroscopic measurement for Z direction |
|timeBodyGyroJerk-Mean-X| Mean jerk signal of body for X direction |
|timeBodyGyroJerk-Mean-Y| Mean jerk signal of body for Y direction |
|timeBodyGyroJerk-Mean-Z| Mean jerk signal of body for Z direction |
|timeBodyGyroJerk-StdDev-X| Standard deviation of jerk signal of body for X direction |
|timeBodyGyroJerk-StdDev-Y| Standard deviation of jerk signal of body for Y direction |
|timeBodyGyroJerk-StdDev-Z| Standard deviation of jerk signal of body for Z direction |
|timeBodyAccMag-Mean|Mean magnitude of body Acceleration|
|timeBodyAccMag-StdDev|Standard deviation of magnitude of body Acceleration|
|timeGravityAccMag-Mean| Mean gravity acceleration magnitude |
|timeGravityAccMag-StdDev| Standard deviation of gravity acceleration magnitude |
|timeBodyAccJerkMag-Mean| Mean magnitude of body acceleration jerk |
|timeBodyAccJerkMag-StdDev| Standard deviation of magnitude of body acceleration jerk |
|timeBodyGyroMag-Mean| Mean magnitude of body gyroscope measurement |
|timeBodyGyroMag-StdDev| Standard deviation of magnitude of body gyroscopic measurement |
|timeBodyGyroJerkMag-Mean| Mean magnitude of body gyroscopic jerk measurement |
|timeBodyGyroJerkMag-StdDev | Standard deviation of magnitude of body body gyroscopic jerk measurement|
|freqBodyAcc-Mean-X| Mean frequency of body acceleration for X direction |
|freqBodyAcc-Mean-Y| Mean frequency of body acceleration for Y direction |
|freqBodyAcc-Mean-Z| Mean frequency of body acceleration for Z direction |
|freqBodyAcc-StdDev-X| Standard deviation of frequency of body acceleration for X direction |
|freqBodyAcc-StdDev-Y| Standard deviation of frequency of body acceleration for Y direction |
|freqBodyAcc-StdDev-Z| Standard deviation of frequency of body acceleration for Z direction |
|freqBodyAccJerk-Mean-X| Mean frequency of body accerlation jerk for X direction |
|freqBodyAccJerk-Mean-Y| Mean frequency of body accerlation jerk for Y direction |
|freqBodyAccJerk-Mean-Z| Mean frequency of body accerlation jerk for Z direction |
|freqBodyAccJerk-StdDev-X| Standard deviation frequency of body accerlation jerk for X direction |
|freqBodyAccJerk-StdDev-Y| Standard deviation frequency of body accerlation jerk for Y direction |
|freqBodyAccJerk-StdDev-Z| Standard deviation frequency of body accerlation jerk for Z direction |
|freqBodyGyro-Mean-X|Mean frequency of body gyroscopic measurement for X direction|
|freqBodyGyro-Mean-Y|Mean frequency of body gyroscopic measurement for Y direction|
|freqBodyGyro-Mean-Z|Mean frequency of body gyroscopic measurement for Z direction|
|freqBodyGyro-StdDev-X| Standard deviation frequency of body gyroscopic measurement for X direction |
|freqBodyGyro-StdDev-Y| Standard deviation frequency of body gyroscopic measurement for Y direction |
|freqBodyGyro-StdDev-Z| Standard deviation frequency of body gyroscopic measurement for Z direction |
|freqBodyAccMag-Mean| Mean frequency of body acceleration magnitude |
|freqBodyAccMag-StdDev| Standard deviation of frequency of body acceleration magnitude |
|freqBodyAccJerkMag-Mean| Mean frequency of body acceleration jerk magnitude |
|freqBodyAccJerkMag-StdDev| Standard deviation of frequency of body acceleration jerk magnitude |
|freqBodyGyroMag-Mean| Mean frequency of magnitude of body gyroscopic measurement |
|freqBodyGyroMag-StdDev| Standard deviation of frequency of magnitude of body gyroscopic measurement |
|freqBodyGyroJerkMag-Mean| Mean magnitude of body gyroscopic jerk measurement |
|freqBodyGyroJerkMag-StdDev| Standard deviation frequency of magnitude of body gyroscopic jerk measurement |
