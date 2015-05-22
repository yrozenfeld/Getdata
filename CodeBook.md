# Code book

This document describes the code inside run_analysis.R and features based on which the summary statistics were calculated

##Feature Selection 

The features selected for this project come from the accelerometer and gyroscope 3-axial raw signals tAcc-XYZ and tGyro-XYZ. These time domain signals (prefix 't' to denote time) were captured at a constant rate of 50 Hz. Then they were filtered using a median filter and a 3rd order low pass Butterworth filter with a corner frequency of 20 Hz to remove noise. Similarly, the acceleration signal was then separated into body and gravity acceleration signals (tBodyAcc-XYZ and tGravityAcc-XYZ) using another low pass Butterworth filter with a corner frequency of 0.3 Hz. 

Subsequently, the body linear acceleration and angular velocity were derived in time to obtain Jerk signals (tBodyAccJerk-XYZ and tBodyGyroJerk-XYZ). Also the magnitude of these three-dimensional signals were calculated using the Euclidean norm (tBodyAccMag, tGravityAccMag, tBodyAccJerkMag, tBodyGyroMag, tBodyGyroJerkMag). 

Finally a Fast Fourier Transform (FFT) was applied to some of these signals producing fBodyAcc-XYZ, fBodyAccJerk-XYZ, fBodyGyro-XYZ, fBodyAccJerkMag, fBodyGyroMag, fBodyGyroJerkMag. (Note the 'f' to indicate frequency domain signals). 

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
* fBodyAccJerkMag
* fBodyGyroMag
* fBodyGyroJerkMag

Then the summary statistics are calculated (see readme.md for more details)
## Steps in R

* Creates data subfolder after checking if this subfodler exists
* Unzips the data set after downloading it from the https://  address
* Reads activity test and train data using read.table statements
* Reads Subject test and train data using read.table statements
* Reads features test and train data using read.table statements
* Combine test and train sets separately for subjets, activities, and features using rbind statement by rows
* Set names to features 
* Merge columns using cbind to bring all data
* Extract all variable with has part of the name mean() and std() using grep statement that looks
 for matches to argument pattern within each element of a char vector
* Read activity categories file using read.table statement
* Factorize activity values by using factor function which encodes a vector as a factor
* Naming using descriptives
* Create tidy data set using plyr package
* Write tidedata.txt file using write.table command
